---
title: X++ コンテナー ランタイム関数
description: このトピックでは、コンテナー ランタイム関数について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31301
ms.assetid: 5b4741a5-dec1-4a3b-b739-6c12142ac668
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0cd819ec87e989b6c1827c48956fd7728e4db69
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408745"
---
# <a name="x-container-runtime-functions"></a><span data-ttu-id="2c4cb-103">X++ コンテナー ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2c4cb-103">X++ container runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c4cb-104">このトピックでは、コンテナー ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-104">This topic describes the container run-time functions.</span></span>

<span data-ttu-id="2c4cb-105">これらの関数はコンテナーの内容を操作します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-105">These functions manipulate the contents of containers.</span></span>

## <a name="condel"></a><span data-ttu-id="2c4cb-106">conDel</span><span class="sxs-lookup"><span data-stu-id="2c4cb-106">conDel</span></span>
<span data-ttu-id="2c4cb-107">コンテナーから指定した要素の数を削除します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-107">Removes the specified number of elements from a container.</span></span>

### <a name="syntax"></a><span data-ttu-id="2c4cb-108">構文</span><span class="sxs-lookup"><span data-stu-id="2c4cb-108">Syntax</span></span>

```xpp
container conDel(container container, int start, int number)
```

### <a name="parameters"></a><span data-ttu-id="2c4cb-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-109">Parameters</span></span>

| <span data-ttu-id="2c4cb-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-110">Parameter</span></span> | <span data-ttu-id="2c4cb-111">説明</span><span class="sxs-lookup"><span data-stu-id="2c4cb-111">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="2c4cb-112">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2c4cb-112">container</span></span> | <span data-ttu-id="2c4cb-113">要素を削除するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-113">The container to remove elements from.</span></span>                      |
| <span data-ttu-id="2c4cb-114">開始</span><span class="sxs-lookup"><span data-stu-id="2c4cb-114">start</span></span>     | <span data-ttu-id="2c4cb-115">要素の削除を開始する 1 から始まる位置。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-115">The one-based position at which to start removing elements.</span></span> |
| <span data-ttu-id="2c4cb-116">数値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-116">number</span></span>    | <span data-ttu-id="2c4cb-117">削除する要素の数。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-117">The number of elements to delete.</span></span>                           |

### <a name="return-value"></a><span data-ttu-id="2c4cb-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-118">Return value</span></span>

<span data-ttu-id="2c4cb-119">削除された要素を含まない新しいコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-119">A new container that doesn't include the removed elements.</span></span>

### <a name="example"></a><span data-ttu-id="2c4cb-120">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-120">Example</span></span>

```xpp
static void conDelExample(Args _args)
{
    container c = ["Hello world", 1, 3.14];
        // Deletes the first two items from the container.
        c = conDel(c, 1, 2);
}
```

## <a name="confind"></a><span data-ttu-id="2c4cb-121">conFind</span><span class="sxs-lookup"><span data-stu-id="2c4cb-121">conFind</span></span>
<span data-ttu-id="2c4cb-122">コンテナー内の最初の要素または一連の要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-122">Locates the first occurrence of an element or a sequence of elements in a container.</span></span>

### <a name="syntax"></a><span data-ttu-id="2c4cb-123">構文</span><span class="sxs-lookup"><span data-stu-id="2c4cb-123">Syntax</span></span>

```xpp
int conFind (container container, anytype element,... )
```

### <a name="parameters"></a><span data-ttu-id="2c4cb-124">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-124">Parameters</span></span>

| <span data-ttu-id="2c4cb-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-125">Parameter</span></span> | <span data-ttu-id="2c4cb-126">説明</span><span class="sxs-lookup"><span data-stu-id="2c4cb-126">Description</span></span>                                              |
|-----------|----------------------------------------------------------|
| <span data-ttu-id="2c4cb-127">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2c4cb-127">container</span></span> | <span data-ttu-id="2c4cb-128">検索するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-128">The container to search.</span></span>                                 |
| <span data-ttu-id="2c4cb-129">要素</span><span class="sxs-lookup"><span data-stu-id="2c4cb-129">element</span></span>   | <span data-ttu-id="2c4cb-130">1 つ以上の要素を検索し、コンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-130">One or more elements to search for, separated by commas.</span></span> |

### <a name="remarks"></a><span data-ttu-id="2c4cb-131">備考</span><span class="sxs-lookup"><span data-stu-id="2c4cb-131">Remarks</span></span>

<span data-ttu-id="2c4cb-132">順序で複数の要素を指定する場合は、これらは、コンマで区切られ、正しい順序で指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-132">If several elements are specified in the sequence, they must be separated by commas and specified in the correct sequence.</span></span> <span data-ttu-id="2c4cb-133">要素は、任意のデータ型にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-133">The elements can be of any data type.</span></span>

### <a name="return-value"></a><span data-ttu-id="2c4cb-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-134">Return value</span></span>

<span data-ttu-id="2c4cb-135">**0** 項目が見つからなかった場合。そうでなければ、項目の順序番号。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-135">**0** if the item was not found; otherwise, the sequence number of the item.</span></span>

### <a name="example"></a><span data-ttu-id="2c4cb-136">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-136">Example</span></span>

```xpp
static void conFindExample(Args _args)
{
    container c = ["item1", "item2", "item3"];
    int i;
    int j;
    i = conFind(c, "item2");
    j = conFind(c, "item4");
    print "Position of 'item2' in container is " + int2Str(i);
    print "Position of 'item4' in container is " + int2Str(j);
}
```

## <a name="conins"></a><span data-ttu-id="2c4cb-137">conIns</span><span class="sxs-lookup"><span data-stu-id="2c4cb-137">conIns</span></span>
<span data-ttu-id="2c4cb-138">コンテナーに 1 つまたは複数の要素を挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-138">Inserts one or more elements into a container.</span></span>

### <a name="syntax"></a><span data-ttu-id="2c4cb-139">構文</span><span class="sxs-lookup"><span data-stu-id="2c4cb-139">Syntax</span></span>

```xpp
container conIns (container container, int start, anytype element, ... )
```

### <a name="parameters"></a><span data-ttu-id="2c4cb-140">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-140">Parameters</span></span>

| <span data-ttu-id="2c4cb-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-141">Parameter</span></span> | <span data-ttu-id="2c4cb-142">説明</span><span class="sxs-lookup"><span data-stu-id="2c4cb-142">Description</span></span>                                          |
|-----------|------------------------------------------------------|
| <span data-ttu-id="2c4cb-143">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2c4cb-143">container</span></span> | <span data-ttu-id="2c4cb-144">要素を挿入するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-144">The container to insert elements into.</span></span>               |
| <span data-ttu-id="2c4cb-145">開始</span><span class="sxs-lookup"><span data-stu-id="2c4cb-145">start</span></span>     | <span data-ttu-id="2c4cb-146">要素を挿入する位置。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-146">The position to insert elements at.</span></span>                  |
| <span data-ttu-id="2c4cb-147">要素</span><span class="sxs-lookup"><span data-stu-id="2c4cb-147">element</span></span>   | <span data-ttu-id="2c4cb-148">1 つ以上の要素を挿入し、コンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-148">One or more elements to insert, separated by commas.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2c4cb-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-149">Return value</span></span>

<span data-ttu-id="2c4cb-150">挿入された要素を含む新しいコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-150">A new container that contains the inserted elements.</span></span>

### <a name="remarks"></a><span data-ttu-id="2c4cb-151">備考</span><span class="sxs-lookup"><span data-stu-id="2c4cb-151">Remarks</span></span>

<span data-ttu-id="2c4cb-152">コンテナーの最初の要素は、番号 **1** によって指定されます。.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-152">The first element of the container is specified by the number **1**.</span></span> <span data-ttu-id="2c4cb-153">n 番目の要素の後に挿入するには、*開始* パラメーターは n+1 でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-153">To insert after the n element, the *start* parameter should be n+1.</span></span> <span data-ttu-id="2c4cb-154">また、**+=** 演算子を使用して任意のタイプの値をコンテナに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-154">You can also use the **+=** operator to add values of any type to a container.</span></span> <span data-ttu-id="2c4cb-155">たとえば、最初の 10 ループ反復処理の自乗値を含むコンテナーを作成するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-155">For example, to create a container that contains the squared values of the first 10 loop iterations, use the following code.</span></span>

```xpp
int i;
container c;

for (i = 1; i < = 10; i++)
{
    c += i*i;
}
```

### <a name="example"></a><span data-ttu-id="2c4cb-156">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-156">Example</span></span>

```xpp
static void conInsExample(Args _arg)
{
    container c;
    int i;

    c = conIns(c,1,"item1");
    c = conIns(c,2,"item2");
    for (i = 1 ; i <= conLen(c) ; i++)
    {
        // Prints the content of a container.
        print conPeek(c, i);
    }
}
```

## <a name="conlen"></a><span data-ttu-id="2c4cb-157">conLen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-157">conLen</span></span>
<span data-ttu-id="2c4cb-158">コンテナー内の要素の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-158">Retrieves the number of elements in a container.</span></span>

### <a name="syntax"></a><span data-ttu-id="2c4cb-159">構文</span><span class="sxs-lookup"><span data-stu-id="2c4cb-159">Syntax</span></span>

```xpp
int conLen(container container)
```

### <a name="parameters"></a><span data-ttu-id="2c4cb-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-160">Parameters</span></span>

| <span data-ttu-id="2c4cb-161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-161">Parameter</span></span> | <span data-ttu-id="2c4cb-162">説明</span><span class="sxs-lookup"><span data-stu-id="2c4cb-162">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="2c4cb-163">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2c4cb-163">container</span></span> | <span data-ttu-id="2c4cb-164">要素の数を数えるコンテナー 。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-164">The container to count the number of elements in.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2c4cb-165">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-165">Return value</span></span>

<span data-ttu-id="2c4cb-166">コンテナー内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-166">The number of elements in the container.</span></span>

### <a name="example"></a><span data-ttu-id="2c4cb-167">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-167">Example</span></span>

```xpp
static void conLenExample(Args _arg)
{
    container c;
    int i;

    c = conins(["item1", "item2"], 1);
    for (i = 1 ; i <= conLen(c) ; i++)
    {
            print conPeek(c, i);
    }
}
```

## <a name="connull"></a><span data-ttu-id="2c4cb-168">conNull</span><span class="sxs-lookup"><span data-stu-id="2c4cb-168">conNull</span></span>
<span data-ttu-id="2c4cb-169">空のコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-169">Retrieves an empty container.</span></span>

```xpp
container conNull()
```

### <a name="remarks"></a><span data-ttu-id="2c4cb-170">備考</span><span class="sxs-lookup"><span data-stu-id="2c4cb-170">Remarks</span></span>

<span data-ttu-id="2c4cb-171">明示的にコンテナーの内容を破棄するには、この機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-171">Use this function to explicitly dispose of the contents of a container.</span></span>

### <a name="return-value"></a><span data-ttu-id="2c4cb-172">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-172">Return value</span></span>

<span data-ttu-id="2c4cb-173">空のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-173">An empty container.</span></span>

### <a name="example"></a><span data-ttu-id="2c4cb-174">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-174">Example</span></span>

```xpp
static void conNullExample(Args _arg)
{
    container c = ["item1", "item2", "item3"];

    print "Size of container is " + int2str(conLen(c));
    // Set the container to null.
    c = conNull();
    print "Size of container after conNull() is " + int2Str(conLen(c));
}
```

## <a name="conpeek"></a><span data-ttu-id="2c4cb-175">conPeek</span><span class="sxs-lookup"><span data-stu-id="2c4cb-175">conPeek</span></span>
<span data-ttu-id="2c4cb-176">コンテナーから特定の要素を取得し、換算が必要な場合は別のデータ型に変換します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-176">Retrieves a specific element from a container and converts it into another data type, if conversion is required.</span></span>

### <a name="syntax"></a><span data-ttu-id="2c4cb-177">構文</span><span class="sxs-lookup"><span data-stu-id="2c4cb-177">Syntax</span></span>

```xpp
anytype conPeek(container container, int number)
```

### <a name="parameters"></a><span data-ttu-id="2c4cb-178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-178">Parameters</span></span>

| <span data-ttu-id="2c4cb-179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-179">Parameter</span></span> | <span data-ttu-id="2c4cb-180">説明</span><span class="sxs-lookup"><span data-stu-id="2c4cb-180">Description</span></span>                                                                                                                                                                                                                      |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4cb-181">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2c4cb-181">container</span></span> | <span data-ttu-id="2c4cb-182">要素を返すコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-182">The container to return an element from.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="2c4cb-183">数値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-183">number</span></span>    | <span data-ttu-id="2c4cb-184">返す要素の位置。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-184">The position of the element to return.</span></span> <span data-ttu-id="2c4cb-185">最初の要素を取得するには **1** を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-185">Specify **1** to get the first element.</span></span> <span data-ttu-id="2c4cb-186">**-3**、**0** などの無効な位置番号、またはコンテナーの長さより高い番号は予期しないエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-186">An invalid position number, such as **-3**, **0**, or a number that is higher than the length of the container, might cause unpredictable errors.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2c4cb-187">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-187">Return value</span></span>

<span data-ttu-id="2c4cb-188">*number* パラメーターで指定された位置にあるコンテナーの要素。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-188">The element in the container at the position that is specified by the *number* parameter.</span></span> <span data-ttu-id="2c4cb-189">**conPeek** 関数は、参照した項目を予想される戻り値の型に自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-189">The **conPeek** function automatically converts the peeked item into the expected return type.</span></span> <span data-ttu-id="2c4cb-190">文字列は、整数と実数に自動的に変換され、整数と実数は文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-190">Strings can automatically be converted into integers and real numbers, and integers and real numbers can be converted into strings.</span></span>

### <a name="example"></a><span data-ttu-id="2c4cb-191">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-191">Example</span></span>

```xpp
static void main(Args _args)
{
    container cnI, cnJ;
    int i, j;
    anytype aty;
    info("container cnI ...");
    cnI = ["itemBlue", "itemYellow"];
    for (i=1; i <= conLen(cnI); i++)
    {
        aty = conPeek(cnI, i);
        info(int2str(i) + " :  " + aty);
    }

    info("container cnJ ...");
    cnJ = conIns(cnI, 2, "ItemInserted");
    for (j=1; j <= conLen(cnJ); j++)
    {
        aty = conPeek(cnJ, j);
        info(int2str(j) + " :  " + aty);
    }
}
/***  Output pasted from InfoLog ...
Message (10:20:03 am)
container cnI ...
1 :  itemBlue
2 :  itemYellow
container cnJ ...
1 :  itemBlue
2 :  ItemInserted
3 :  itemYellow
***/
```

## <a name="conpoke"></a><span data-ttu-id="2c4cb-192">conPoke</span><span class="sxs-lookup"><span data-stu-id="2c4cb-192">conPoke</span></span>
<span data-ttu-id="2c4cb-193">既存の要素を 1 つ以上を置換することでコンテナーを変更します。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-193">Modifies a container by replacing one or more of the existing elements.</span></span>

### <a name="syntax"></a><span data-ttu-id="2c4cb-194">構文</span><span class="sxs-lookup"><span data-stu-id="2c4cb-194">Syntax</span></span>

```xpp
container conPoke(container container, int start, anytype element, ...)
```

### <a name="parameters"></a><span data-ttu-id="2c4cb-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-195">Parameters</span></span>

| <span data-ttu-id="2c4cb-196">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c4cb-196">Parameter</span></span> | <span data-ttu-id="2c4cb-197">説明</span><span class="sxs-lookup"><span data-stu-id="2c4cb-197">Description</span></span>                                           |
|-----------|-------------------------------------------------------|
| <span data-ttu-id="2c4cb-198">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2c4cb-198">container</span></span> | <span data-ttu-id="2c4cb-199">変更するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-199">The container to modify.</span></span>                              |
| <span data-ttu-id="2c4cb-200">開始</span><span class="sxs-lookup"><span data-stu-id="2c4cb-200">start</span></span>     | <span data-ttu-id="2c4cb-201">置き換える最初の要素の位置。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-201">The position of the first element to replace.</span></span>         |
| <span data-ttu-id="2c4cb-202">要素</span><span class="sxs-lookup"><span data-stu-id="2c4cb-202">element</span></span>   | <span data-ttu-id="2c4cb-203">1 つ以上の要素を置換し、コンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-203">One or more elements to replace, separated by commas.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2c4cb-204">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c4cb-204">Return value</span></span>

<span data-ttu-id="2c4cb-205">新しい要素を含む新しいコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="2c4cb-205">A new container that includes the new elements.</span></span>

### <a name="remarks"></a><span data-ttu-id="2c4cb-206">備考</span><span class="sxs-lookup"><span data-stu-id="2c4cb-206">Remarks</span></span>

<span data-ttu-id="2c4cb-207">コンテナーの最初の要素は、番号 **1** によって指定されます。.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-207">The first element of the container is specified by the number **1**.</span></span>

### <a name="example"></a><span data-ttu-id="2c4cb-208">例</span><span class="sxs-lookup"><span data-stu-id="2c4cb-208">Example</span></span>

```xpp
static void conPokeExample(Args _arg)
{
    container c1 = ["item1", "item2", "item3"];
    container c2;
    int i;
    void conPrint(container c)
    {
        for (i = 1 ; i <= conLen(c) ; i++)
        {
            print conPeek(c, i);
        }
    }

    conPrint(c1);
    c2 = conPoke(c1, 2, "PokedItem");
    print "";
    conPrint(c2);
}
```


