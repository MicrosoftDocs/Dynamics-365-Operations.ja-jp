---
title: X++ 複合データ型
description: このトピックでは、X++ の複合データ型について説明します。
author: RobinARH
ms.date: 04/08/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150183
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d37fb8355a3a6e4a058f9720d73728a63c9ed3b
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866015"
---
# <a name="x-composite-data-types"></a><span data-ttu-id="8b1e5-103">X++ 複合データ型</span><span class="sxs-lookup"><span data-stu-id="8b1e5-103">X++ composite data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b1e5-104">このトピックでは、X++ の複合データ型について説明します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-104">This topic describes composite data types in X++.</span></span> <span data-ttu-id="8b1e5-105">X++ の複合データ型は、配列、コンテナー、データ型としてのクラス、データ型としてのデリゲート、データ型としてのテーブルです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-105">The composite data types in X++ are arrays, containers, classes as data types, delegates as data types, and tables as data types.</span></span>

## <a name="array"></a><span data-ttu-id="8b1e5-106">配列</span><span class="sxs-lookup"><span data-stu-id="8b1e5-106">Array</span></span>

<span data-ttu-id="8b1e5-107">*配列* は同じデータ型を持つ項目のリストを含む変数です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-107">An *array* is a variable that contains a list of items that have the same data type.</span></span> <span data-ttu-id="8b1e5-108">配列の要素は、整数インデックスを使用してアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-108">The elements of an array are accessed by using integer indexes.</span></span> <span data-ttu-id="8b1e5-109">配列内の各要素を初期化するには、別のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-109">You use a separate statement to initialize each element in an array.</span></span> <span data-ttu-id="8b1e5-110">コンテナー データ型または配列オブジェクトを使用してコレクションを作成するとき、1 つのステートメントを使用して複数の要素を初期化できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-110">When you use a container data type or an array object to create a collection, you can initialize multiple elements by using a single statement.</span></span> <span data-ttu-id="8b1e5-111">既定では、配列内のすべての項目は配列のデータ型の既定値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-111">By default, all the items in an array have the default value of the data type in the array.</span></span> <span data-ttu-id="8b1e5-112">*動的配列*、*固定長配列*、*ディスク配列の一部* の 3 種類の配列があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-112">There are three kinds of arrays: *dynamic arrays*, *fixed-length arrays*, and *partly on disk arrays*.</span></span>

- <span data-ttu-id="8b1e5-113">**動的配列** - これらの配列は、空の配列オプションを使用して宣言されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-113">**Dynamic arrays** – These arrays are declared by using an empty array option.</span></span> <span data-ttu-id="8b1e5-114">つまり、かっこ (\[\]) だけがあります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-114">In other words, they have only brackets (\[\]).</span></span>
- <span data-ttu-id="8b1e5-115">**固定長の配列** – これらの配列は、宣言で指定されている品目の数を保持できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-115">**Fixed-length arrays** – These arrays can hold the number of items that is specified in the declaration.</span></span> <span data-ttu-id="8b1e5-116">固定長の配列は動的配列と宣言されますが、かっこ内に長さのオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-116">Fixed-length arrays are declared like dynamic arrays, but a length option is included in the brackets.</span></span>
- <span data-ttu-id="8b1e5-117">**ディスク配列の一部** – これらの配列は、動的配列または固定長の配列として宣言され、メモリに保持する品目の数を宣言するオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-117">**Partly on disk arrays** – These arrays are declared as either dynamic arrays or fixed-length arrays that have an extra option that declares how many items should be held in memory.</span></span> <span data-ttu-id="8b1e5-118">他の項目はディスクに保存され、参照されると自動的に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-118">The other items are stored on disk and are automatically loaded when they are referenced.</span></span>

<span data-ttu-id="8b1e5-119">X++ は1次元配列のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-119">X++ supports only one-dimensional arrays.</span></span> <span data-ttu-id="8b1e5-120">ただし、複数の配列インデックスの動作を再現することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-120">However, you can mimic the behavior of multiple array indexes.</span></span> <span data-ttu-id="8b1e5-121">(詳細については、[複数の配列インデックス](#multiple-array-indexes) セクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-121">(For more information, see the [Multiple array indexes](#multiple-array-indexes) section).</span></span> <span data-ttu-id="8b1e5-122">オブジェクトとテーブル内の変数は配列として宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-122">Variables in objects and tables can be declared as arrays.</span></span> <span data-ttu-id="8b1e5-123">たとえば、この機能は、標準アプリケーションの住所明細行で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-123">For example, this functionality is used in address lines in the standard application.</span></span> <span data-ttu-id="8b1e5-124">配列コレクション クラスを配列内のオブジェクトに格納できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-124">An array collection class lets you store objects in an array.</span></span> 

<span data-ttu-id="8b1e5-125">配列インデックスは 1 から開始されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-125">Array indexes begin at 1.</span></span> <span data-ttu-id="8b1e5-126">配列の最初の項目は \[1\] で参照され、2番目の項目は、 \[2\] などで参照されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-126">The first item in the array is referenced as \[1\], the second item is referenced as \[2\], and so on.</span></span> <span data-ttu-id="8b1e5-127">次の構文は、配列要素にアクセスするために使用されます: **ArrayItemReference = ArrayVariable \[ Index \]**。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-127">The following syntax is used to access an array element: **ArrayItemReference = ArrayVariable \[ Index \]**.</span></span> <span data-ttu-id="8b1e5-128">この構文では、**ArrayVariable** は配列の識別子であり、**Index** は配列要素の数です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-128">In this syntax, **ArrayVariable** is the identifier of the array, and **Index** is the number of the array element.</span></span> <span data-ttu-id="8b1e5-129">**インデックス** には整数式を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-129">**Index** can be an integer expression.</span></span> <span data-ttu-id="8b1e5-130">項目ゼロ \[0\] は配列をクリアするために使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-130">Item zero \[0\] is used to clear the array.</span></span> <span data-ttu-id="8b1e5-131">値が配列のインデックス 0 に割り当てられている場合は、配列内のすべての要素が既定値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-131">If a value is assigned to index 0 in an array, all elements in the array are reset to their default value.</span></span>

### <a name="array-examples"></a><span data-ttu-id="8b1e5-132">配列の例</span><span class="sxs-lookup"><span data-stu-id="8b1e5-132">Array examples</span></span>

```xpp
public void ArrayMethod()
{
    int myArray[10]; // Fixed-length array with 10 integers.
    myArray[4] = 1; // Accessing the 4th element in the array.
    myArray[0] = 0; // Resets all elements in intArray. 

    // Dynamic array of integers.
    int intArray[];

    // Dynamic array of variables of type Datatype.
    //Datatype arrayVariable[];

    // Fixed-length arrays.
    boolean boolArray[100]; // Fixed-length array of booleans with 100 items.

    // Two examples of Partly On Disk Arrays.
    // Dynamic integer array with only 100 elements in memory.
    int arrayVariable [ ,100];
    // Fixed-length string array with 1000 elements, and only 200 in memory.
    str arrayVariable2 [1000,200];

    // A dynamic array of integers.
    int i[];
    // A fixed-length real array with 100 elements.
    real r[100];
    // A dynamic array of dates with only 10 elements in memory.
    date d[,10];
    // A fixed length array of NoYes variables with 100 elements and 10 in memory.
    NoYes ny[100,10];
}
```

### <a name="multiple-array-indexes"></a><span data-ttu-id="8b1e5-133">複数の配列インデックス</span><span class="sxs-lookup"><span data-stu-id="8b1e5-133">Multiple array indexes</span></span>

<span data-ttu-id="8b1e5-134">C++ および C\# などの一部の言語を使用すると、1 つ以上のインデックスを持つ配列を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-134">Some languages, such as C++ and C\#, let you declare arrays that have more than one index.</span></span> <span data-ttu-id="8b1e5-135">つまり、「配列の配列」を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-135">In other words, you can define "arrays of arrays."</span></span> <span data-ttu-id="8b1e5-136">X++ では、1 次元配列のみサポートされているため、複数の配列インデックスを直接作成できません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-136">In X++, you can't directly create multiple array indexes because only one-dimensional arrays are supported.</span></span> <span data-ttu-id="8b1e5-137">ただし、このセクションに記載されているメソッドを使用して、複数のインデックスを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-137">However, you can implement multiple indexes by using the method that is described in this section.</span></span> <span data-ttu-id="8b1e5-138">たとえば、国別分析コードにより獲得される量を保持するため、2 つの分析コードを持つ配列を宣言します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-138">For example, you want to declare an array that has two dimensions, to hold an amount that is earned by country by dimension.</span></span> <span data-ttu-id="8b1e5-139">10 の国と 3 つの分析コードがあります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-139">There are 10 countries and three dimensions.</span></span> <span data-ttu-id="8b1e5-140">C++ および C\# では、次の配列を宣言します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-140">In C++ and C\#, you declare the following array.</span></span>

```xpp
// This is C# or C++ code, not X++ code.
real earning[10, 3];
```

<span data-ttu-id="8b1e5-141">ただし、X++ はこの申告をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-141">However, X++ doesn't support this declaration.</span></span> <span data-ttu-id="8b1e5-142">代わりに、要素の数が各分析コード内の要素の製品である 1 次元配列を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-142">Instead, you can define a one-dimensional array where the number of elements is the product of the elements in each dimension.</span></span> <span data-ttu-id="8b1e5-143">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-143">Here is an example.</span></span>

```xpp
public void MultipleArrayMethod()
{
    // Step 1: define a one-dimensional array with the number
    // of elements that is the product of the elements in each dimension.
    real earnings[10*3];

    // Step 2: to refer to a specific element, such as earnings[i,j], write the following:
    // declare i and j (maybe) and assign the value to something
    int i = 1;
    int j = 2;
    real element = earnings[(i-1)*3 + j];
}

// This can be written into a macro like this:
#localmacro.earningIndex
(%1-1)*3+%2
#endmacro

public void CallTheMacro()
{
    // Next, call the specific element within the macro like this:
    int i = 1;
    int j = 2;
    real element = earnings[#earningIndex(i,j)];

    // The previous scheme can be extended to any number of dimensions.
    // The element a[i1, i2, ..., ik] can be accessed by computing the
    // offset into an array containing (d1*d2*...*dk) elements.
    //(i1 - 1)*d2*d3*..*dk +
    //(i2 - 1)*d3*d4*...*dk + .... +
    //(ik-1 -1)*dk +
    //(ik-1)
}
```

## <a name="container"></a><span data-ttu-id="8b1e5-144">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8b1e5-144">Container</span></span>

<span data-ttu-id="8b1e5-145">*コンテナー* オブジェクトは、プリミティブ データ型または複合データ型が含まれる項目の動的リストです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-145">A *container* object is a dynamic list of items that contains primitive data types or composite data types.</span></span> <span data-ttu-id="8b1e5-146">コンテナーは、クライアント層とサーバー層の間でさまざまな種類の値を渡す必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-146">A container is useful when you must pass various types of values between the client and server tiers.</span></span> <span data-ttu-id="8b1e5-147">ただし、ループ内でのリストに繰り返し追加する予定がある場合、コンテナーは適切な選択肢ではありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-147">However, if you plan to repeatedly add to a list in a loop, a container isn't a good choice.</span></span> <span data-ttu-id="8b1e5-148">コンテナーは、コンテナーのサイズまたは内容を過度に変更することがないプロセスに最も適しています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-148">Containers are most suitable for processes that don't involve excessive modification to the size or contents of the container.</span></span> <span data-ttu-id="8b1e5-149">コンテナーに過剰にデータが追加されると、コンテナーのデータを繰り返しコピーする必要があり、また新しい領域を繰り返し割り当てる必要があるため、システム全体のパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-149">When a container undergoes excessive additions of data, overall system performance can decrease because container data must be repeatedly copied and new space must be repeatedly allocated.</span></span> 

<span data-ttu-id="8b1e5-150">コンテナーはクラスではありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-150">A container isn't a class.</span></span> <span data-ttu-id="8b1e5-151">コンテナーには、プリミティブ値またはその他のコンテナーの注文済のシーケンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-151">A container contains an ordered sequence of primitive values or other containers.</span></span> <span data-ttu-id="8b1e5-152">**anytype** の柔軟性のために、コンテナーは異なるタイプの値を一緒に保存する良い方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-152">Because of the flexibility of **anytype**, a container offers a good way to store values of different types together.</span></span> <span data-ttu-id="8b1e5-153">コンテナーは、データベースに保管できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-153">A container can be stored in the database.</span></span> <span data-ttu-id="8b1e5-154">コンテナーとは、アプリケーション エクスプローラーを使用して、テーブルに列を追加する場合に選択可能な列タイプの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-154">A container is one of the column types that you can select when you use Application Explorer to add a column to a table.</span></span> <span data-ttu-id="8b1e5-155">配列に少し似た、または **List** や **Stack** クラスのようなコレクションのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-155">A container slightly resembles an array, or collections, such as the **List** or **Stack** classes.</span></span> <span data-ttu-id="8b1e5-156">ただし、コンテナーを作成した後にコンテナーのサイズまたはコンテンツを変更できません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-156">However, you can never change the size or content of a container after the container is created.</span></span> 

<span data-ttu-id="8b1e5-157">コンテナを変更するために表示される X++ ステートメントは、内部で新しいコンテナを構築して必要に応じ値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-157">X++ statements that appear to modify a container are internally building a new container and copying values as required.</span></span> <span data-ttu-id="8b1e5-158">コンテナーを別のコンテナー変数に割り当てても、コンテナーの新しいコピーは作成されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-158">Even an assignment of a container to another container variable creates a new copy of the container.</span></span> <span data-ttu-id="8b1e5-159">これらすべての工程はパフォーマンスに影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-159">All these operations can affect performance.</span></span> <span data-ttu-id="8b1e5-160">コンテナーへのアクセスを提供する関数 (**conPeek** など) では、コンテナーは 0 ベースではなく、1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-160">In the functions that provide access to a container (such as **conPeek**), the container is 1-based, not 0-based.</span></span> <span data-ttu-id="8b1e5-161">インデックスは配列に対して 1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-161">Indexing is 1-based for arrays.</span></span> <span data-ttu-id="8b1e5-162">コンテナーの既定値は **空** です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-162">The default value of a container is **empty**.</span></span> <span data-ttu-id="8b1e5-163">コンテナーには値が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-163">The container doesn't contain any values.</span></span> <span data-ttu-id="8b1e5-164">コンテナーを使用するステートメントの中には、コンテナーを変更しようとして表示されることがありますが、システム内では、コンテナーが変更されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-164">Some statements that use containers might appear to modify a container, however, inside the system, containers are never modified.</span></span> <span data-ttu-id="8b1e5-165">代わりに、元のコンテナーからのデータは、新しいコンテナーを構築するためにコマンドからのデータと結合されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-165">Instead, the data from the original container is combined with data from the command to build a new container.</span></span> <span data-ttu-id="8b1e5-166">**conDel**、**conIns**、または **conPoke** のいずれかの関数を使用して、新しいコンテナを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-166">You can create a new container by using one of the following functions: **conDel**, **conIns**, or **conPoke**.</span></span> 

<span data-ttu-id="8b1e5-167">また、**グローバル** クラスには、コンテナーを処理するための静的メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-167">Additionally, the **Global** class has static methods for handling containers.</span></span> <span data-ttu-id="8b1e5-168">これらのメソッドには、**con2ArraySource**、**con2Buf**、**con2List**、**con2Str**、**containerFromXmlNode**、**conView**、**str2Con** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-168">These methods include **con2ArraySource**, **con2Buf**, **con2List**, **con2Str**, **containerFromXmlNode**, **conView**, and **str2Con**.</span></span> <span data-ttu-id="8b1e5-169">**conIns** や **conPeek** のような、コンテナーを扱うためのいくつかの固有の関数があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-169">There are several intrinsic functions for handling a container, such as **conIns** and **conPeek**.</span></span> <span data-ttu-id="8b1e5-170">X++ **conPeek** 関数は **anytype** 型を返すため、各値の型がわからない場合はコンテナーから値を読み取る方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-170">The X++ **conPeek** function returns an **anytype** type, therefore, it's easier to read the values from a container when you don't know the type of each value.</span></span> <span data-ttu-id="8b1e5-171">**anytype** は値を変換することができればすべての X++ 値タイプに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-171">An **anytype** can be assigned to any X++ value type, provided that the value can be converted.</span></span> <span data-ttu-id="8b1e5-172">明示的なデータ型の変換を回避すると、コードは読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-172">Your code is easier to read when it avoids explicit data type conversions.</span></span> <span data-ttu-id="8b1e5-173">したがって、値をコンテナーに配置するために使用されたのと同じデータ型にコンテナーから値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-173">Therefore, assign values from a container to the same data type that was used to put the value into the container.</span></span> <span data-ttu-id="8b1e5-174">コンテナーを **エニタイプ** に割り当てることはできません。適切な変換を決定できない可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-174">You must not assign a container to an **anytype** because the system might not be able to determine the correct conversions.</span></span> <span data-ttu-id="8b1e5-175">そのような場合、予期しない動作やエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-175">In these cases, unexpected behavior or errors might occur.</span></span>

### <a name="comparing-container-to-other-options"></a><span data-ttu-id="8b1e5-176">コンテナーと他のオプションの比較</span><span class="sxs-lookup"><span data-stu-id="8b1e5-176">Comparing container to other options</span></span>

<span data-ttu-id="8b1e5-177">**コンテナー** 型は、**List** や **Stack** などの配列およびコレクション クラスなど、他の構成要素と似ています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-177">The **container** type resembles other constructs, such as arrays and collection classes, such as **List** and **Stack**.</span></span> <span data-ttu-id="8b1e5-178">**コンテナー** と **リスト** の違いは、**リスト** クラスのインスタンスが不変であるという点です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-178">The difference between a **container** and **List** is that an instance of the **List** class is mutable.</span></span> <span data-ttu-id="8b1e5-179">**リスト** オブジェクトは、最初にそのデータが消費するよりも多くの領域を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-179">A **List** object first allocates more space than its data consumes.</span></span> <span data-ttu-id="8b1e5-180">その後、データが追加されると、スペースが埋められます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-180">Then, as data is added, the space is filled.</span></span> <span data-ttu-id="8b1e5-181">この動作は、要素が追加されるたびに多くの領域を割り当てる場合よりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-181">This behavior is more efficient than allocating more space every time that an element is added.</span></span> <span data-ttu-id="8b1e5-182">**リスト** の更新はコンテナーの同様の操作よりも高速に実行します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-182">An update of a **List** performs faster than similar operations on a container.</span></span> 

<span data-ttu-id="8b1e5-183">**リスト** オブジェクトを作成するときは、**リスト** オブジェクトが格納できるデータの 1 つのタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-183">When you construct a **List** object, you determine the one type of data that the **List** object can store.</span></span> <span data-ttu-id="8b1e5-184">この制限は、コンテナの場合よりも **リスト** の柔軟性が低くなります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-184">This restriction is less flexible for a **List** than it is for a container.</span></span> <span data-ttu-id="8b1e5-185">ただし、**リスト** のオブジェクトを格納できますが、コンテナーでは値の型しか格納できません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-185">However, you can store objects in a **List**, whereas a container can store only value types.</span></span> <span data-ttu-id="8b1e5-186">コンテナーと配列の違いは、配列は宣言された型の項目だけを保持できるという点です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-186">The difference between a container and an array is that an array can hold only items of its declared type.</span></span> <span data-ttu-id="8b1e5-187">配列にメモリ容量を割り当て、後からその容量に値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-187">You can allocate memory space for an array and fill that space with values later.</span></span> <span data-ttu-id="8b1e5-188">たとえば、ループに値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-188">For example, you can fill in values in a loop.</span></span> <span data-ttu-id="8b1e5-189">この動作は効率的であり、適正に動作します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-189">This behavior is efficient and performs well.</span></span> <span data-ttu-id="8b1e5-190">新しいデータを追加して新しいコンテナーを作成するときは、**+=** 演算子かまたは **conIns** 機能のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-190">When you want to build a new container by appending new data, you can use either the **+=** operator or the **conIns** function.</span></span> <span data-ttu-id="8b1e5-191">**+=** 演算子は高速の代替です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-191">The **+=** operator is the faster alternative.</span></span> <span data-ttu-id="8b1e5-192">**conIns** 関数は、元のデータの最後のインデックスの前に新しいデータを追加する場合にのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-192">Use the **conIns** function only when you want to add new data before the last index of the original data.</span></span> 

<span data-ttu-id="8b1e5-193">Dynamics AX 2012 では、コンテナーのオブジェクト参照を格納するために X++ コンパイラを使用できましたが、結果は実行時に失敗していました。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-193">In Dynamics AX 2012, although you could use the X++ compiler to store object references in containers, the result would fail at run time.</span></span> <span data-ttu-id="8b1e5-194">ただし、Finance and Operations アピリケーションでは、コンテナー内のオブジェクト参照を格納しようとすると、コンパイラがエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-194">However, in Finance and Operations applications, when the compiler sees an attempt to store an object reference in a container, it issues an error message.</span></span> <span data-ttu-id="8b1e5-195">コンテナーに追加される要素のタイプが **anytype** である場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-195">If the type of the element that is added to the container is **anytype**, the compiler can’t determine whether the value is a reference type.</span></span> <span data-ttu-id="8b1e5-196">この場合、コンパイラはその試行を認めます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-196">In this case, the compiler allows the attempt.</span></span> <span data-ttu-id="8b1e5-197">コンパイラはコードを誤っていると診断しませんが、エラーは実行時間にスローされます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-197">Although the compiler doesn't diagnose the code as erroneous, an error will be thrown at run time.</span></span>

### <a name="container-examples"></a><span data-ttu-id="8b1e5-198">コンテナーの例</span><span class="sxs-lookup"><span data-stu-id="8b1e5-198">Container examples</span></span>

```xpp
public void ContainerExample() 
{
    // First, declare the variables you are using.  
    container myContainer;
    container myContainer4;
    container myContainer5; 
    // Three ways to declare a container.
    myContainer = [1];
    myContainer += [2];
    myContainer4 = myContainer5;

    // Declare a container.
    container cr3;

    // Assign a literal container to a container variable.
    cr3 = [22, "blue"];

    // Declare and assign a container.
    container cr2 = [1, "blue", true];

    // Mimic container modification (implicitly creates a copy).
    cr3 += [16, strMyColorString];
    cr3 = conIns(cr3, 1, 3.14);
    cr3 = conPoke(cr3, 2, "violet");

    // Assignment of a container (implicitly creates a copy).
    cr2 = cr3;

    // Read a value from the container.
    str  myStr = conPeek(cr2, 1);

    // One statement that does multiple assignments from a container.
    str myStr;
    int myInt;
    container cr4 = ["Hello", 22, 20\07\1988];
    [myStr, myInt] = cr4; // "Hello", 22

    // Example of applying the = operator to a container. The example
    // initializes myContainer2 and myContainer33.
    myContainer2 = [2, "apple"];

    // Next, you make a copy of myContainer33 and assign the copy to myContainer2.
    myContainer33 = [33, "grape"];
    myContainer2 = myContainer33;  // The container that myContainer2 had been holding is no longer available and cannot be recovered.
    // An example of building a new container by
    // assigning a new value to myContainer33 through the += operator.
    myContainer33 += [34, "banana"];
}

// Container example. In this example, variable2 and variable33 hold different containers.
static void JobC(Args _args)
{
    container variable2, variable33;
    variable2 += [98];
    variable33 = variable2;
    variable2 += [97];
}

// List class example. In this example, variable2 and variable33 refer to the same List object.
static void JobL(Args _args)
{
    List variable2,variable33;
    variable2 = new List(Types::Integer);
    variable2.addEnd(98);
    variable33 = variable2;
    variable2.addEnd(97);
}

// The automatic type conversion by anytype also applies to the special syntax for making multiple
// assignments from a container in one statement. This is shown in the following code example,
// which assigns a str to an int, and an int to a str.
static void JobContainerMultiAssignmentUsesAnytype(Args _args)
{
    container con2;
    int int4;
    str str7;
    con2 = ["11", 222];
    [int4, str7] = con2;
    info(strfmt("int4==11==(%1), str7==222==(%2)", int4, str7));
}

/***  Output:
Message (10:36:22 am)
int4==11==(11), str7==222==(222)
***/

static void UseQuery()
{
    // An example of how the compiler diagnoses attempts to store object in containers
    container c = [new Query()];   // This statement will cause the error message shown below.
    /*** Instance of type 'Query' cannot be added to a container. ***/

    // An example of a code that won't cause an error message, but will
    // cause an error message to be thrown at runtime.
    anytype a = new Query();
    container d = [a];
}
```

## <a name="classes-as-data-types"></a><span data-ttu-id="8b1e5-199">データ型としてのクラス</span><span class="sxs-lookup"><span data-stu-id="8b1e5-199">Classes as data types</span></span>

<span data-ttu-id="8b1e5-200">*クラス* は、クラスのインスタンスの変数とメソッドの両方を説明するタイプ定義です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-200">A *class* is a type definition that describes both variables and methods for instances of the class.</span></span> <span data-ttu-id="8b1e5-201">(クラスのインスタンスは *オブジェクト* ともよばれます。) クラスはオブジェクトの定義に過ぎず、すべてのオブジェクトは宣言されると **null** です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-201">(The instances of a class are also known as *objects*.) A class is only a definition for objects, and all objects are **null** when they are declared.</span></span> <span data-ttu-id="8b1e5-202">アプリケーション エクスプローラーでは、**クラス** ノードの各アプリケーション クラスはデータ型です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-202">In Application Explorer, every application class under the **Classes** node is a data type.</span></span> <span data-ttu-id="8b1e5-203">これらの種類の変数をコード内で宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-203">You can declare variables of these types in your code.</span></span> <span data-ttu-id="8b1e5-204">クラスのインスタンスを構築してインスタンスを変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-204">You can construct instances of a class and assign the instances to variables.</span></span> 

<span data-ttu-id="8b1e5-205">クラスはソース コードに入れ子にできます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-205">Classes can be nested in source code.</span></span> <span data-ttu-id="8b1e5-206">入れ子になったクラスはフォーム内 (**FormRun** を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表すために使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-206">Nested classes are available only inside forms (such as a class that extends **FormRun**), and are used to represent controls, data sources, or data fields.</span></span> <span data-ttu-id="8b1e5-207">属性の修飾で接尾語に **属性** がある場合、属性の修飾などのクラスまたはメソッドで、属性名の接尾語を省略できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-207">An attribute decoration, such as the attribute decoration on a class or a method, can omit the suffix of the attribute name if the suffix is **Attribute**.</span></span> <span data-ttu-id="8b1e5-208">したがって、X++ は **\[MyFavoriteAttribute\]** を必要とするのではなく、**\[MyFavorite\]** を許可します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-208">Therefore, X++ allows **\[MyFavorite\]** instead of requiring **\[MyFavoriteAttribute\]**.</span></span> <span data-ttu-id="8b1e5-209">また、属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらのターゲットにマップします。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-209">Additionally, attributes are now applied to the handlers of delegates and methods, to map the handlers to those targets.</span></span> 

<span data-ttu-id="8b1e5-210">AX 2012 およびそれ以前のバージョンでは、クライアントまたはサーバーのいずれかで実行するメソッドを指定することができました。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-210">In AX 2012 and earlier versions, you could designate a method to run on either the client or the server.</span></span> <span data-ttu-id="8b1e5-211">ただし、Finance and Operations のアプリケーションでは、コンパイルされたすべての X++ コードがサーバーの .NET 共通の中間言語 (CIL) として実行されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-211">However, in Finance and Operations applications, all compiled X++ code is run as .NET Common Intermediate Language (CIL) on the server.</span></span> <span data-ttu-id="8b1e5-212">クライアント サイトまたはブラウザーで評価されるコードはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-212">There is no longer any code that is evaluated at the client site or in the browser.</span></span> <span data-ttu-id="8b1e5-213">したがって、**client** キーワードと **server** キーワードは無視されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-213">Therefore, the **client** and **server** keywords are now ignored.</span></span> <span data-ttu-id="8b1e5-214">これらのキーワードが使用される場合コンパイル エラーは発生しませんが、新しいコードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-214">Although these keywords don't cause a compile error if they are used, they should not be used in any new code.</span></span>

### <a name="private-and-protected-member-variables"></a><span data-ttu-id="8b1e5-215">プライベートおよび保護されたメンバー変数</span><span class="sxs-lookup"><span data-stu-id="8b1e5-215">Private and protected member variables</span></span>

<span data-ttu-id="8b1e5-216">以前は、クラスで定義されていたすべてのメンバー変数が保護されていました。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-216">Previously, all member variables that were defined in a class were protected.</span></span> <span data-ttu-id="8b1e5-217">**private**、**protected**、および **public** キーワードを加えることにより、メンバー変数の表示を明示的にすることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-217">You can now make the visibility of member variables explicit by adding the **private**, **protected**, and **public** keywords.</span></span> <span data-ttu-id="8b1e5-218">これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-218">The interpretation of these modifiers is obvious and is aligned with the semantics for methods:</span></span>

-   <span data-ttu-id="8b1e5-219">**プライベート** – メンバー変数は、定義されているクラス内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-219">**private** – The member variable can be used only within the class where it’s defined.</span></span>
-   <span data-ttu-id="8b1e5-220">**保護されている** – メンバー変数は、それが定義されているクラスおよびクラスのすべてのサブクラスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-220">**protected** – The member variable can be used in the class where it’s defined and all subclasses of that class.</span></span>
-   <span data-ttu-id="8b1e5-221">**パブリック** – メンバー変数を任意の場所に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-221">**public** – The member variable can be used anywhere.</span></span> <span data-ttu-id="8b1e5-222">これは、定義されているクラス階層の範囲外に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-222">It’s visible outside the confines of the class hierarchy where it’s defined.</span></span>

<span data-ttu-id="8b1e5-223">既定では、明示的なモディファイアーで実装されていないメンバー変数は引き続き保護されています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-223">By default, member variables that aren’t adorned with an explicit modifier are still protected.</span></span> <span data-ttu-id="8b1e5-224">ただし、ベスト プラクティスとしては、可視性を明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-224">However, as a best practice, you should explicitly specify the visibility.</span></span> <span data-ttu-id="8b1e5-225">先に説明したように、メンバー変数が **パブリック** として定義されている場合、メンバー変数は定義されているクラス外でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-225">As we described earlier, when a member variable is defined as **public**, it can be accessed outside the class where it’s defined.</span></span> <span data-ttu-id="8b1e5-226">この場合、変数をホストしているオブジェクトを指定する修飾子を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-226">In this case, you must specify a qualifier that designates the object that is hosting the variable.</span></span> <span data-ttu-id="8b1e5-227">修飾子を指定するには、メソッド呼び出しの場合と同様にドット表記法を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-227">To specify the qualifier, use the dot notation, as you do for method calls.</span></span> 

<span data-ttu-id="8b1e5-228">次の例では、**field1** に明示的な **this** 修飾子を使用することでアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-228">In the following example, **field1** is accessed by using the explicit **this** qualifier.</span></span> <span data-ttu-id="8b1e5-229">この場合、そのアプローチは消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることをお勧めできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-229">In this case, it might not be a good idea to make a member variable public, because that approach exposes the internal workings of the class to its consumers, and therefore creates a strong dependency between the class implementation and its consumers.</span></span> <span data-ttu-id="8b1e5-230">常に、実装ではなくコントラクトにのみ依存させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-230">You should always try to depend only on a contract, not an implementation.</span></span>

```xpp
public class AnotherClass3
{
    int field1;
    str field2;
    void new()
    {
        this.field1 = 1;   // Explicit object designated.
        field2 = "Banana";  // 'this' assumed, as usual.
    }
}
```

### <a name="static-constructors-and-static-fields"></a><span data-ttu-id="8b1e5-231">静的コンストラクターおよび静的フィールド</span><span class="sxs-lookup"><span data-stu-id="8b1e5-231">Static constructors and static fields</span></span>

<span data-ttu-id="8b1e5-232">*静的フィールド* は **静的** キーワードを使用して宣言されているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-232">*Static fields* are fields that are declared by using the **static** keyword.</span></span> <span data-ttu-id="8b1e5-233">概念的には、クラスのインスタンスではなく静的フィールドに適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-233">Conceptually, static fields apply to the class, not to instances of the class.</span></span> <span data-ttu-id="8b1e5-234">静的コンストラクターは、静的呼び出しまたはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-234">Static constructors are guaranteed to run before any static calls or instance calls are made to the class.</span></span> <span data-ttu-id="8b1e5-235">静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-235">The execution of the static constructor is relative to the user’s session.</span></span> <span data-ttu-id="8b1e5-236">静的コンストラクターは明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-236">You never call the static constructor explicitly.</span></span> <span data-ttu-id="8b1e5-237">代わりに、コンパイラはコンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-237">Instead, the compiler will generate code to make sure that the constructor is called exactly one time, before any other method on the class is called.</span></span> <span data-ttu-id="8b1e5-238">静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のあるアクションを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-238">A static constructor is used to initialize any static data or perform an action that must be performed only one time.</span></span> <span data-ttu-id="8b1e5-239">静的コンストラクターのパラメーターを指定することはできず、**静的** キーワードでマークされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-239">You can't provide parameters for the static constructor, and it must be marked with the **static** keyword.</span></span>

```xpp
// An example of how a singleton (call instance in the example below)
// can be created using the static constructor.
public class Singleton
{
    private static Singleton instance;
    private void new()
    {
    }
    static void TypeNew()    // This is the static constructor.
    {
        instance = new Singleton();
    }

    public static Singleton Instance()
    {
        return Singleton::instance;
    }
}

// The singleton ensures that only one instance of the class
// will be called, which is consumed by the following. 
{
    // Your code here.
    Singleton i = Singleton::Instance();
}
```

### <a name="class-elements-in-application-explorer"></a><span data-ttu-id="8b1e5-240">アプリケーション エクスプローラーのクラス要素</span><span class="sxs-lookup"><span data-stu-id="8b1e5-240">Class elements in Application Explorer</span></span>

<span data-ttu-id="8b1e5-241">アプリケーション エクスプ ローラーのほとんどのクラス・ノードの下には、**classDeclaration** ノードと **new** ノードという 2 つの特殊ノードがあります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-241">Under most class nodes in Application Explorer, there are two special nodes: a **classDeclaration** node and a **new** node.</span></span> <span data-ttu-id="8b1e5-242">**classDeclaration** は、常に X++ **クラス** キーワードになります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-242">A **classDeclaration** always contains the X++ **class** keyword.</span></span> <span data-ttu-id="8b1e5-243">追加のキーワードは、**拡張** のように、クラスを変更するために含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-243">Additional keywords, such as **extends**, can be included to modify the class.</span></span> <span data-ttu-id="8b1e5-244">このノードには、メンバー変数の宣言も含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-244">This node can also contain declarations of member variables.</span></span>  

<span data-ttu-id="8b1e5-245">次の例では、変数 **m\_priority** および **m\_rectangle** はクラスのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-245">In the following example, the variables **m\_priority** and **m\_rectangle** are members of the class.</span></span>

```xpp
// An example of a classDeclaration.
public class YourDerivedClass extends YourBaseClass
{
    int m_priority;
    Rectangle m_rectangle;
    void new(int _length, int _width)
    {
        this.m_rectangle = new Rectangle(_length, _width);
    }
}
```

<span data-ttu-id="8b1e5-246">**新しい** 演算子には、**新しい** 演算子を使用して、クラスのインスタンスを作成するときに実行されるロジックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-246">A **new** operator contains logic that is run when the **new** operator is used to create an instance of the class.</span></span> <span data-ttu-id="8b1e5-247">**新規** メソッドのロジックは、オブジェクトを作成し、そのオブジェクトを **classDeclaration** で宣言された変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-247">The logic in the **new** method might construct an object and assign that object to a variable that is declared in the **classDeclaration**.</span></span> <span data-ttu-id="8b1e5-248">各クラスは、**新しい** 方法を 1 つだけ持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-248">Each class can have only one **new** method.</span></span> <span data-ttu-id="8b1e5-249">ただし、**新しい** メソッドでは、多くの場合基本クラスの **新しい** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-249">However, in the **new** method, you often should call the **new** method of the base class.</span></span> <span data-ttu-id="8b1e5-250">基本クラスの<**新規** メソッドを呼び出すには、**super()** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-250">To call the **new** method of the base class, call **super()**.</span></span> 

<span data-ttu-id="8b1e5-251">次の例は、前の **classDeclaration** の例の **YourDerivedClass** クラスの **new** メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-251">The following example shows the **new** method for the **YourDerivedClass** class in the previous **classDeclaration** example.</span></span> <span data-ttu-id="8b1e5-252">この **新しい** メソッドで、コードは **長方形** クラスのインスタンスを構築します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-252">In this **new** method, the code constructs an instance of the **Rectangle** class.</span></span> <span data-ttu-id="8b1e5-253">インスタンスは、**m\_rectangle** 変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-253">The instance is assigned to the **m\_rectangle** variable.</span></span> <span data-ttu-id="8b1e5-254">**この** 例で使用されているキーワードは省略可能ですが、指定した場合は、IntelliSense を使用する方が便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-254">The **this** keyword that is used in the example is optional, however, if you include it, IntelliSense might be more helpful.</span></span>

```xpp
// An example of the new method from the previous classDeclaration example.
void new(int _length, int _width)
{
    this.m_rectangle = new Rectangle(_length, _width);
}
```

### <a name="garbage-collection"></a><span data-ttu-id="8b1e5-255">ガベージ コレクション</span><span class="sxs-lookup"><span data-stu-id="8b1e5-255">Garbage collection</span></span>

<span data-ttu-id="8b1e5-256">最終的に実行中では、ほとんどのオブジェクトがそれらを指す変数はなくなります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-256">Eventually during run time, most objects no longer have any variable that points to them.</span></span> <span data-ttu-id="8b1e5-257">システムはこれらのオブジェクトをスキャンし、それらをメモリから消去します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-257">The system scans for these objects and erases them from memory.</span></span> <span data-ttu-id="8b1e5-258">その後、メモリ空間は他の用途に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-258">The memory space then becomes available for other uses.</span></span> <span data-ttu-id="8b1e5-259">**Object** クラスには、**finalize** というメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-259">The **Object** class has a method that is named **finalize**.</span></span> <span data-ttu-id="8b1e5-260">ただし、**確定** メソッドはデストラクタではありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-260">However, the **finalize** method isn't a destructor.</span></span> <span data-ttu-id="8b1e5-261">ランタイムは、オブジェクトがガベージとして収集された場合でも、**finalize** メソッドを呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-261">The runtime never calls the **finalize** method, even when an object is collected as garbage.</span></span>

### <a name="system-classes"></a><span data-ttu-id="8b1e5-262">システム クラス</span><span class="sxs-lookup"><span data-stu-id="8b1e5-262">System classes</span></span>

<span data-ttu-id="8b1e5-263">アプリケーション エクスプローラーの **システムのドキュメント** &gt; **クラス** には、カーネル クラスまたはシステム クラスの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-263">In Application Explorer, under **System Documentation** &gt; **Classes**, there is a list of the kernel classes or system classes.</span></span> <span data-ttu-id="8b1e5-264">システム クラスは、X++ で記述されておらず、ソース コードを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-264">System classes aren't written in X++, and you can't see their source code.</span></span> <span data-ttu-id="8b1e5-265">システム クラスを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-265">You can't add system classes.</span></span> <span data-ttu-id="8b1e5-266">システム クラには通常、**new** メソッドがありますが、**classDeclaration** ノードはありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-266">System classes usually have a **new** method, but they don't have a **classDeclaration** node.</span></span> <span data-ttu-id="8b1e5-267">すべてのアプリケーション クラスは **オブジェクト** システム クラスを暗黙的に拡張します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-267">Every application class implicitly extends the **Object** system class.</span></span> <span data-ttu-id="8b1e5-268">一部のシステム クラスは、類似した名前を持つアプリケーション クラスで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-268">Some system classes are extended by an application class that has a similar name.</span></span> <span data-ttu-id="8b1e5-269">たとえば、**xClassFactory** が **ClassFactory** ごとに延期されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-269">For instance, **xClassFactory** is extended by **ClassFactory**.</span></span> <span data-ttu-id="8b1e5-270">そのような場合、システム クラスは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-270">In these cases, you should not use the system class.</span></span> <span data-ttu-id="8b1e5-271">詳細については、[クラスおよびメソッド](xpp-classes-methods.md) で「システム クラスの代替アプリケーション クラス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-271">For more information, see "Substitute application classes for system classes" in [Classes and methods](xpp-classes-methods.md).</span></span>

### <a name="extension-methods"></a><span data-ttu-id="8b1e5-272">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="8b1e5-272">Extension methods</span></span>

<span data-ttu-id="8b1e5-273">拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-273">The extension method feature lets you add extension methods to a target class by writing the methods in a separate extension class.</span></span> <span data-ttu-id="8b1e5-274">次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-274">The following rules apply:</span></span>

-   <span data-ttu-id="8b1e5-275">拡張クラスは静的でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-275">The extension class must be static.</span></span>
-   <span data-ttu-id="8b1e5-276">拡張クラスの名前は、10 文字の接尾辞 **\_Extension** で終了する必要がありますが、接尾辞に先行する名前の部分には制限はありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-276">The name of the extension class must end with the ten-character suffix **\_Extension**, however, there’s no restriction on the part of the name that precedes the suffix.</span></span>
-   <span data-ttu-id="8b1e5-277">拡張子クラス内のすべての拡張子メソッドは、**パブリック静的** として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-277">Every extension method in the extension class must be declared as **public static**.</span></span>
-   <span data-ttu-id="8b1e5-278">すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-278">The first parameter in every extension method is the type that the extension method extends.</span></span> <span data-ttu-id="8b1e5-279">ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-279">However, when the extension method is called, the caller must not pass in anything for the first parameter.</span></span> <span data-ttu-id="8b1e5-280">代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-280">Instead, the system automatically passes in the required object for the first parameter.</span></span>
-   <span data-ttu-id="8b1e5-281">拡張メソッドのターゲットは、クラス、テーブル、ビュー、またはマップ アプリケーション オブジェクト タイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-281">The target of an extension method must be a class, table, view, or map application object type.</span></span>

<span data-ttu-id="8b1e5-282">拡張クラスはプライベートまたは保護された静的メソッドを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-282">An extension class can contain private or protected static methods.</span></span> <span data-ttu-id="8b1e5-283">これらのメソッドは通常、実装の詳細に使用され、拡張として公開されません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-283">These methods are typically used for implementation details and aren't exposed as extensions.</span></span> <span data-ttu-id="8b1e5-284">拡張メソッドの手法は、それを拡張するクラスのソースコードには影響しません。そのため、クラスへの追加はオーバーレイを必要なく行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-284">The extension method technique doesn’t affect the source code of the class that it extends, therefore, the addition to the class doesn't require over-layering.</span></span> 

<span data-ttu-id="8b1e5-285">ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-285">Upgrades to the target class are never affected by any existing extension methods.</span></span> <span data-ttu-id="8b1e5-286">ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-286">If an upgrade to the target class adds a method that has the same name as your extension method, your extension method can no longer be reached through objects of the target class.</span></span> <span data-ttu-id="8b1e5-287">拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-287">The extension method technique uses the same dot-delimited syntax that you often use to call regular instance methods.</span></span> <span data-ttu-id="8b1e5-288">拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトには何もアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-288">Extension methods can access all public artifacts of the target class, but they can’t access anything that is protected or private.</span></span> <span data-ttu-id="8b1e5-289">したがって、拡張メソッドは構文砂糖の一種と考えることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-289">Therefore, extension methods can be considered a type of syntactic sugar.</span></span> <span data-ttu-id="8b1e5-290">目標タイプに関係なく、拡張機能クラスはタイプに拡張メソッドを追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-290">Regardless of the target type, an extension class is used to add extension methods to the type.</span></span> <span data-ttu-id="8b1e5-291">たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されていませんし、拡張テーブルというものは存在しません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-291">For example, an extension table isn't used to add methods to a table, and there’s no such thing as an extension table.</span></span>

```xpp
// An example of an extension class holding a few extension methods.
public static class AtlInventLocation_Extension
{
    public static InventLocation refillEnabled(
        InventLocation _warehouse,
        boolean _isRefillEnabled = true)
    {
        _warehouse.ReqRefill = _isRefillEnabled;
        return _warehouse;
    }

    public static InventLocation save(InventLocation _warehouse)
    {
        _warehouse.write();
        return _warehouse;
    }
}
```

## <a name="delegates-as-data-types"></a><span data-ttu-id="8b1e5-292">データ型としてのデリゲート</span><span class="sxs-lookup"><span data-stu-id="8b1e5-292">Delegates as data types</span></span>

<span data-ttu-id="8b1e5-293">*デリゲート* は、それをサブスクライブするメソッドを収集します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-293">A *delegate* collects methods that subscribe to it.</span></span> <span data-ttu-id="8b1e5-294">デリゲートは、すべてのサブスクライバ メソッドが共有する必要があるパラメーター署名を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-294">The delegate specifies the parameter signature that all its subscriber methods must share.</span></span> <span data-ttu-id="8b1e5-295">デリゲートが呼び出されると、デリゲートはその各サブスクライバを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-295">When the delegate is called, the delegate calls each of its subscribers.</span></span> <span data-ttu-id="8b1e5-296">デリゲートは値を返しませんし、**既定値を持つことはできません**。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-296">A delegate never returns a value and **can't have a default value**.</span></span> <span data-ttu-id="8b1e5-297">最初に、すべてのデリゲートにはサブスクライブされたメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-297">At first, every delegate has no subscribed methods.</span></span> <span data-ttu-id="8b1e5-298">デリゲートが宣言できるパラメーターの数に制限はなく、これらのパラメーターの種類に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-298">There is no limit on the number of parameters that a delegate can declare, and there is no limitation on the type of those parameters.</span></span> <span data-ttu-id="8b1e5-299">デリゲートの唯一の目的は、サブスクライバが従わなければならない契約を定義することであるため、デリゲート本文は常に空です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-299">The delegate body is always empty, because the delegate's only purpose is to define the contract that subscribers must conform to.</span></span> <span data-ttu-id="8b1e5-300">デリゲートは、クラスで定義をしなくてもかまいません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-300">A delegate doesn't have to be defined in a class.</span></span> <span data-ttu-id="8b1e5-301">デリゲートは、テーブル、フォーム、またはクエリで定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-301">Delegates can also be defined in a table, form, or query.</span></span>

### <a name="delegate-examples"></a><span data-ttu-id="8b1e5-302">デリゲートの例</span><span class="sxs-lookup"><span data-stu-id="8b1e5-302">Delegate examples</span></span>

```xpp
abstract class VarDatClass
{
    // delegatemethod examples
    // An example of declaring a delegate.
    delegate void notifyChange(utcdatetime _dateTime, str _changeDescription)
    {
    }

    // An example of subscribing an event handler to a delegate.
    public static void notifyStatic(utcDateTime _dateTime, str _changeDescription)
    {
        info("A notification has occurred calling static handler:" +
            DateTimeUtil::toStr(_dateTime) +
            " Message:" +
            _changeDescription);
    }
}
```

## <a name="tables-as-data-types"></a><span data-ttu-id="8b1e5-303">データ型としてのテーブル</span><span class="sxs-lookup"><span data-stu-id="8b1e5-303">Tables as data types</span></span>

<span data-ttu-id="8b1e5-304">すべてのテーブルはクラス定義として扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-304">All tables can be treated as class definitions.</span></span> <span data-ttu-id="8b1e5-305">テーブル変数は、テーブル (class) の定義のインスタンス (オブジェクト) と見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-305">A table variable can be considered an instance (object) of the table (class) definition.</span></span> <span data-ttu-id="8b1e5-306">テーブル変数の各フィールドでは、既定値は **空** です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-306">For every field in a table variable, the default value is **empty**.</span></span> <span data-ttu-id="8b1e5-307">フィールドに注意を向けてテーブル上でメソッドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-307">You can address fields and create methods on tables.</span></span> <span data-ttu-id="8b1e5-308">これらのメソッドは、テーブルのインスタンス上で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-308">The methods can be invoked on instances of the table.</span></span> <span data-ttu-id="8b1e5-309">テーブル内のレコードを操作 (つまり、読み取り、更新、挿入、削除) するには、レコードを保持しておくための少なくとも 1 つのテーブル変数を宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-309">To manipulate (that is, read, update, insert, and delete) records in tables, you must declare at least one table variable that can hold the record in focus.</span></span> <span data-ttu-id="8b1e5-310">ベスト プラクティスは、変数の名前としてテーブルの名前を使用する必要がありますが、最初の小文字を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-310">As a best practice, you should use the name of the table as the name of the variable but use an initial lowercase letter.</span></span> <span data-ttu-id="8b1e5-311">テーブルとオブジェクト間のいくつかの重要な違いを次に示します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-311">Here are a few important differences between tables and objects:</span></span>

-   <span data-ttu-id="8b1e5-312">テーブル変数の容量を割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-312">You can't allocate space for table variables.</span></span> <span data-ttu-id="8b1e5-313">配賦は暗黙的に行われます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-313">Allocation is done implicitly.</span></span>
-   <span data-ttu-id="8b1e5-314">テーブル変数のフィールドは、パブリックです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-314">Fields in table variables are public.</span></span> <span data-ttu-id="8b1e5-315">任意の場所でそれを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-315">You can reference them anywhere.</span></span>
-   <span data-ttu-id="8b1e5-316">テーブル変数のフィールドは、式を使用して参照できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-316">Fields in table variables can be referenced by using expressions.</span></span>

<span data-ttu-id="8b1e5-317">自動変換はありませんが、**共通** として宣言されているテーブル変数は、どのテーブルからでもデータを保持できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-317">There is no automatic conversion, but table variables that are declared as **Common** can hold data from any table.</span></span>

### <a name="scope-of-table-variables"></a><span data-ttu-id="8b1e5-318">テーブル変数の範囲</span><span class="sxs-lookup"><span data-stu-id="8b1e5-318">Scope of table variables</span></span>

<span data-ttu-id="8b1e5-319">テーブル変数は、ほとんどの点で、オブジェクトと見なされますが、ただし、オブジェクトとは異なり、それらは明示的に割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-319">In most respects, table variables can be considered objects, however, unlike objects, they aren't explicitly allocated.</span></span> <span data-ttu-id="8b1e5-320">変数の宣言のみ必要です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-320">Only a variable declaration is required.</span></span> <span data-ttu-id="8b1e5-321">すべてのテーブルには **共通** のテーブルと互換性があるように、すべてのオブジェクト にも **オブジェクト** クラスの互換性があります。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-321">All tables are compatible with the **Common** table, just as all objects are compatible with the **Object** class.</span></span> <span data-ttu-id="8b1e5-322">テーブル変数は、一般的なバッファーとして宣言され、任意のテーブルからデータを保持するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-322">Table variables are declared as common buffers and can be used to hold data from any table.</span></span> <span data-ttu-id="8b1e5-323">テーブル変数を持たないテーブルにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-323">You can't access tables that don't have table variables.</span></span> <span data-ttu-id="8b1e5-324">テーブルの変数およびオブジェクトの宣言の原則は、領域の割り当てに関する点を除いて同じです。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-324">The principles for declaring table variables and objects are the same, except with regard to the allocation of space.</span></span>

### <a name="table-examples"></a><span data-ttu-id="8b1e5-325">テーブルの例</span><span class="sxs-lookup"><span data-stu-id="8b1e5-325">Table examples</span></span>

<span data-ttu-id="8b1e5-326">構文は、レコード内のフィールドを参照するさまざまな可能性を高めます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-326">The syntax enables various possibilities for referencing fields in records.</span></span> <span data-ttu-id="8b1e5-327">たとえば、**TableName.(FieldId)** 構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-327">For example, you can use the **TableName.(FieldId)** syntax.</span></span> 

<span data-ttu-id="8b1e5-328">次の例では、顧客テーブルの現在のレコードにあるフィールドの内容を出力します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-328">The following example prints the contents of the fields in the current record in the Customer table.</span></span>

```xpp
// Declares and allocates space for one CustTable record.
public void myMethod()
{
    CustomerTable custTable;
}

// An example of referencing table variables.
public void printAccountNo()
{
    CustomerTable custTable;
    print custTable.AccountNo;  // Prints the field reference.
}
```

<span data-ttu-id="8b1e5-329">次の例では、**fieldCnt** および **fieldCnt2Id** メソッドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-329">The following example uses the **fieldCnt** and **fieldCnt2Id** methods.</span></span> <span data-ttu-id="8b1e5-330">**fieldCnt** メソッドは、テーブル内のフィールドの数をカウントしますが、**fieldCnt2Id** はフィールド番号の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-330">The **fieldCnt** method counts the number of fields in a table, whereas **fieldCnt2Id** returns the ID for a field number.</span></span> <span data-ttu-id="8b1e5-331">たとえば、**fieldCnt2Id** メソッドを使用して、テーブルでそのフィールド番号 6 が ID 54 を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-331">For example, you can use the **fieldCnt2Id** method to learn that field number 6 in a table has the ID 54.</span></span> <span data-ttu-id="8b1e5-332">この変換は、表内のフィールドの ID が連続しているという保証がないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="8b1e5-332">This conversion is required, because there is no guarantee that the IDs of the fields in a table are consecutive.</span></span>

```xpp
// An example of the various possibilities for referencing fields in records.
public void printCust()
{
    int i, n, k;
    CustomerTable custTable;
    DictTable dictTable;
    dictTable = new DictTable(custTable.TableId);
    n = dictTable.fieldCnt();
    print "Number of fields in table: ", n;
    for(i=1; i<=n; i++)
    {
        k = dictTable.fieldCnt2Id(i);
        print "The ", dictTable.fieldName(k),
        " field with Id=",k, " contains '",
        custTable.(k), "'";
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]