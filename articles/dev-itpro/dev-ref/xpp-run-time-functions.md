---
title: X++ ランタイム関数
description: このトピックでは、X++ のランタイム関数について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 31461
ms.assetid: 9cf83640-536c-4a99-8e0d-7a4e97d3c91f
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 466c6e85e7f6d0fae446ea19dd631bd036c1d4ad
ms.sourcegitcommit: 1f269e1afd876bd592f88eee683664bc93fa64bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/09/2019
ms.locfileid: "1539445"
---
# <a name="x-runtime-functions"></a><span data-ttu-id="f570f-103">X++ ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="f570f-103">X++ runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f570f-104">このトピックでは、X++ のランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="f570f-104">This topic describes the X++ run-time functions.</span></span>

<span data-ttu-id="f570f-105">X++ 言語は、約 200 のシステム関数を提供しており、これらは、任意のクラスの一部ではなく、実行時に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f570f-105">The X++ language provides nearly 200 system functions that aren't part of any class and are executed at run time.</span></span> <span data-ttu-id="f570f-106">ランタイム関数は、データ型変換、算術操作などに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f570f-106">Run-time functions are used for data type conversions, mathematical operations, and so on.</span></span> <span data-ttu-id="f570f-107">いくつかの共通のランタイム関数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f570f-107">Here are some common run-time functions:</span></span>

-   <span data-ttu-id="f570f-108">**str2Int** – は、str 値から int 値を作成します。</span><span class="sxs-lookup"><span data-stu-id="f570f-108">**str2Int** – Creates an int value from a str value.</span></span>
-   <span data-ttu-id="f570f-109">**abs** – 正または負の実際の値から正の実数値を作成します。</span><span class="sxs-lookup"><span data-stu-id="f570f-109">**abs** – Creates a positive real value from a real value that is either positive or negative.</span></span>
-   <span data-ttu-id="f570f-110">**conFind** – コンテナー内の要素の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="f570f-110">**conFind** – Retrieves the location of an element in a container.</span></span>

### <a name="call-run-time-functions-from-net"></a><span data-ttu-id="f570f-111">.NET からランタイム関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="f570f-111">Call run-time functions from .NET</span></span>

<span data-ttu-id="f570f-112">X++ ランタイム関数のロジックは、次の .NET アセンブリでも実装されています。</span><span class="sxs-lookup"><span data-stu-id="f570f-112">The logic of the X++ run-time functions is also implemented in the following .NET assembly.</span></span>

    Microsoft.Dynamics.AX.Xpp.Support.DLL

<span data-ttu-id="f570f-113">このアセンブリ内で、X++ ランタイム関数は次のクラスの静的メソッドとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="f570f-113">Inside this assembly, the X++ run-time functions are implemented as static methods of the following class.</span></span>

    Microsoft.Dynamics.AX.Xpp.PredefinedFunctions

## <a name="categories-and-functions"></a><span data-ttu-id="f570f-114">カテゴリおよび機能</span><span class="sxs-lookup"><span data-stu-id="f570f-114">Categories and functions</span></span>
<span data-ttu-id="f570f-115">次のテーブルは、X++ 関数のカテゴリのみを一覧表示して説明しています。</span><span class="sxs-lookup"><span data-stu-id="f570f-115">The following table lists and describes only the categories of X++ functions.</span></span> <span data-ttu-id="f570f-116">これらのカテゴリは、多数の機能を理解するのに役立つものです。</span><span class="sxs-lookup"><span data-stu-id="f570f-116">These categories are intended to help you understand the many functions.</span></span> <span data-ttu-id="f570f-117">ただし、カテゴリでは任意の正式コンストラクトが表されません。</span><span class="sxs-lookup"><span data-stu-id="f570f-117">However, the categories don't represent any formal construct.</span></span>

| <span data-ttu-id="f570f-118">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="f570f-118">Category</span></span>                  | <span data-ttu-id="f570f-119">説明</span><span class="sxs-lookup"><span data-stu-id="f570f-119">Description</span></span>  |
|---|---|
| [<span data-ttu-id="f570f-120">勤務先</span><span class="sxs-lookup"><span data-stu-id="f570f-120">Business</span></span>](#business)     | <span data-ttu-id="f570f-121">財務データを入力し、式を計算する機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-121">Functions that enter financial data and calculate formulas.</span></span> <span data-ttu-id="f570f-122">詳細については、[X++ ビジネス ランタイム関数](xpp-business-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-122">For more information, see [X++ Business Run-Time Functions](xpp-business-run-time-functions.md).</span></span>                              |
| [<span data-ttu-id="f570f-123">コンテナ</span><span class="sxs-lookup"><span data-stu-id="f570f-123">Container</span></span>](#container)   | <span data-ttu-id="f570f-124">X++ のコンテナー データ型で操作する機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-124">Functions that operate on the container data type of X++.</span></span> <span data-ttu-id="f570f-125">詳細については、[X++ コンテナー ランタイム関数](xpp-container-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-125">For more information, see [X++ Container Run-Time Functions](xpp-container-run-time-functions.md).</span></span>                               |
| [<span data-ttu-id="f570f-126">換算</span><span class="sxs-lookup"><span data-stu-id="f570f-126">Conversion</span></span>](#conversion) | <span data-ttu-id="f570f-127">1 つのタイプのデータを別のタイプのデータに翻訳する機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-127">Functions that translate data of one type into data of another type.</span></span> <span data-ttu-id="f570f-128">詳細については、[X++ 換算ランタイム関数](xpp-conversion-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-128">For more information, see [X++ Conversion Run-Time Functions](xpp-conversion-run-time-functions.md).</span></span>                  |
| [<span data-ttu-id="f570f-129">日付</span><span class="sxs-lookup"><span data-stu-id="f570f-129">Date</span></span>](#date)             | <span data-ttu-id="f570f-130">日付データ型で操作する機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-130">Functions that operate on the date data type.</span></span> <span data-ttu-id="f570f-131">詳細については、[X++ 日付ランタイム関数](xpp-date-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-131">For more information, see [X++ Date Run-Time Functions](xpp-date-run-time-functions.md).</span></span>                                                     |
| [<span data-ttu-id="f570f-132">計算</span><span class="sxs-lookup"><span data-stu-id="f570f-132">Math</span></span>](#math)             | <span data-ttu-id="f570f-133">数学的な計算を実行する機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-133">Functions that perform mathematical calculations.</span></span> <span data-ttu-id="f570f-134">詳細については、[X++ 数学ランタイム関数](xpp-math-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-134">For more information, see [X++ Math Run-Time Functions](xpp-math-run-time-functions.md).</span></span>                                                 |
| [<span data-ttu-id="f570f-135">反映</span><span class="sxs-lookup"><span data-stu-id="f570f-135">Reflection</span></span>](#reflection) | <span data-ttu-id="f570f-136">オブジェクトに関するメタデータにアクセスし、それらに関するその他のメタデータを返す機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-136">Functions that access the metadata about objects and return other metadata about them.</span></span> <span data-ttu-id="f570f-137">詳細については、[X++ リフレクションランタイム関数](xpp-reflection-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-137">For more information, see [X++ Reflection Run-Time Functions](xpp-reflection-run-time-functions.md).</span></span> |
| [<span data-ttu-id="f570f-138">セッション</span><span class="sxs-lookup"><span data-stu-id="f570f-138">Session</span></span>](#session)       | <span data-ttu-id="f570f-139">現在のユーザー接続のコンテキストで変更またはレポートする機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-139">Functions that change or report on the context of the current user connection.</span></span> <span data-ttu-id="f570f-140">詳細については、[X++ セッション ランタイム関数](xpp-session-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-140">For more information, see [X++ Session Run-Time Functions](xpp-session-run-time-functions.md).</span></span>             |
| [<span data-ttu-id="f570f-141">文字列</span><span class="sxs-lookup"><span data-stu-id="f570f-141">String</span></span>](#string)         | <span data-ttu-id="f570f-142">str データ型で操作する機能。</span><span class="sxs-lookup"><span data-stu-id="f570f-142">Functions that operate on the str data type.</span></span> <span data-ttu-id="f570f-143">詳細については、[X++ 文字列ランタイム関数](xpp-string-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-143">For more information, see [X++ String Run-Time Functions](xpp-string-run-time-functions.md).</span></span>                                                 |
| <span data-ttu-id="f570f-144">外</span><span class="sxs-lookup"><span data-stu-id="f570f-144">Other</span></span>                     | <span data-ttu-id="f570f-145">[ビープ音](#beep)、[newGuid](#newguid)、[スリープ](#sleep)</span><span class="sxs-lookup"><span data-stu-id="f570f-145">[beep](#beep), [newGuid](#newguid), [sleep](#sleep)</span></span>                                                                                                                                                                        |

## <a name="business"></a><span data-ttu-id="f570f-146">勤務先</span><span class="sxs-lookup"><span data-stu-id="f570f-146">Business</span></span>
<span data-ttu-id="f570f-147">詳細については、[X++ ビジネス ランタイム関数](xpp-business-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-147">For more information, see [X++ Business Run-Time Functions](xpp-business-run-time-functions.md).</span></span>

|          |         |          |        |
|----------|---------|----------|--------|
| <span data-ttu-id="f570f-148">cTerm</span><span class="sxs-lookup"><span data-stu-id="f570f-148">cTerm</span></span>    | <span data-ttu-id="f570f-149">ddb</span><span class="sxs-lookup"><span data-stu-id="f570f-149">ddb</span></span>     | <span data-ttu-id="f570f-150">dg</span><span class="sxs-lookup"><span data-stu-id="f570f-150">dg</span></span>       | <span data-ttu-id="f570f-151">fV</span><span class="sxs-lookup"><span data-stu-id="f570f-151">fV</span></span>     |
| <span data-ttu-id="f570f-152">idg</span><span class="sxs-lookup"><span data-stu-id="f570f-152">idg</span></span>      | <span data-ttu-id="f570f-153">intvMax</span><span class="sxs-lookup"><span data-stu-id="f570f-153">intvMax</span></span> | <span data-ttu-id="f570f-154">intvName</span><span class="sxs-lookup"><span data-stu-id="f570f-154">intvName</span></span> | <span data-ttu-id="f570f-155">intvNo</span><span class="sxs-lookup"><span data-stu-id="f570f-155">intvNo</span></span> |
| <span data-ttu-id="f570f-156">intvNorm</span><span class="sxs-lookup"><span data-stu-id="f570f-156">intvNorm</span></span> | <span data-ttu-id="f570f-157">pmt</span><span class="sxs-lookup"><span data-stu-id="f570f-157">pmt</span></span>     | <span data-ttu-id="f570f-158">pt</span><span class="sxs-lookup"><span data-stu-id="f570f-158">pt</span></span>       | <span data-ttu-id="f570f-159">pv</span><span class="sxs-lookup"><span data-stu-id="f570f-159">pv</span></span>     |
| <span data-ttu-id="f570f-160">レート</span><span class="sxs-lookup"><span data-stu-id="f570f-160">rate</span></span>     | <span data-ttu-id="f570f-161">sln</span><span class="sxs-lookup"><span data-stu-id="f570f-161">sln</span></span>     | <span data-ttu-id="f570f-162">syd</span><span class="sxs-lookup"><span data-stu-id="f570f-162">syd</span></span>      | <span data-ttu-id="f570f-163">term</span><span class="sxs-lookup"><span data-stu-id="f570f-163">term</span></span>   |

## <a name="container"></a><span data-ttu-id="f570f-164">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f570f-164">Container</span></span>
<span data-ttu-id="f570f-165">詳細については、[X++ コンテナー ランタイム関数](xpp-container-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-165">For more information, see [X++ Container Run-Time Functions](xpp-container-run-time-functions.md).</span></span>

- <span data-ttu-id="f570f-166">conDel</span><span class="sxs-lookup"><span data-stu-id="f570f-166">conDel</span></span>
- <span data-ttu-id="f570f-167">conFind</span><span class="sxs-lookup"><span data-stu-id="f570f-167">conFind</span></span>
- <span data-ttu-id="f570f-168">conIns</span><span class="sxs-lookup"><span data-stu-id="f570f-168">conIns</span></span>
- <span data-ttu-id="f570f-169">conLen</span><span class="sxs-lookup"><span data-stu-id="f570f-169">conLen</span></span>
- <span data-ttu-id="f570f-170">conNull</span><span class="sxs-lookup"><span data-stu-id="f570f-170">conNull</span></span>
- <span data-ttu-id="f570f-171">conPeek</span><span class="sxs-lookup"><span data-stu-id="f570f-171">conPeek</span></span>
- <span data-ttu-id="f570f-172">conPoke</span><span class="sxs-lookup"><span data-stu-id="f570f-172">conPoke</span></span>

## <a name="conversion"></a><span data-ttu-id="f570f-173">換算</span><span class="sxs-lookup"><span data-stu-id="f570f-173">Conversion</span></span>
<span data-ttu-id="f570f-174">詳細については、[X++ 換算ランタイム関数](xpp-conversion-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-174">For more information, see [X++ Conversion Run-Time Functions](xpp-conversion-run-time-functions.md).</span></span>

|           |              |              |            |
|-----------|--------------|--------------|------------|
| <span data-ttu-id="f570f-175">any2Date</span><span class="sxs-lookup"><span data-stu-id="f570f-175">any2Date</span></span>  | <span data-ttu-id="f570f-176">any2Enum</span><span class="sxs-lookup"><span data-stu-id="f570f-176">any2Enum</span></span>     | <span data-ttu-id="f570f-177">any2Guid</span><span class="sxs-lookup"><span data-stu-id="f570f-177">any2Guid</span></span>     | <span data-ttu-id="f570f-178">any2Int</span><span class="sxs-lookup"><span data-stu-id="f570f-178">any2Int</span></span>    |
| <span data-ttu-id="f570f-179">any2Int64</span><span class="sxs-lookup"><span data-stu-id="f570f-179">any2Int64</span></span> | <span data-ttu-id="f570f-180">any2Real</span><span class="sxs-lookup"><span data-stu-id="f570f-180">any2Real</span></span>     | <span data-ttu-id="f570f-181">any2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-181">any2Str</span></span>      | <span data-ttu-id="f570f-182">anytodate</span><span class="sxs-lookup"><span data-stu-id="f570f-182">anytodate</span></span>  |
| <span data-ttu-id="f570f-183">anytoenum</span><span class="sxs-lookup"><span data-stu-id="f570f-183">anytoenum</span></span> | <span data-ttu-id="f570f-184">anytoguid</span><span class="sxs-lookup"><span data-stu-id="f570f-184">anytoguid</span></span>    | <span data-ttu-id="f570f-185">anytoint</span><span class="sxs-lookup"><span data-stu-id="f570f-185">anytoint</span></span>     | <span data-ttu-id="f570f-186">anytoint64</span><span class="sxs-lookup"><span data-stu-id="f570f-186">anytoint64</span></span> |
| <span data-ttu-id="f570f-187">anytoreal</span><span class="sxs-lookup"><span data-stu-id="f570f-187">anytoreal</span></span> | <span data-ttu-id="f570f-188">anytostr</span><span class="sxs-lookup"><span data-stu-id="f570f-188">anytostr</span></span>     | <span data-ttu-id="f570f-189">char2Num</span><span class="sxs-lookup"><span data-stu-id="f570f-189">char2Num</span></span>     | <span data-ttu-id="f570f-190">date2Num</span><span class="sxs-lookup"><span data-stu-id="f570f-190">date2Num</span></span>   |
| <span data-ttu-id="f570f-191">date2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-191">date2Str</span></span>  | <span data-ttu-id="f570f-192">datetime2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-192">datetime2Str</span></span> | <span data-ttu-id="f570f-193">enum2str</span><span class="sxs-lookup"><span data-stu-id="f570f-193">enum2str</span></span>     | <span data-ttu-id="f570f-194">guid2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-194">guid2Str</span></span>   |
| <span data-ttu-id="f570f-195">int2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-195">int2Str</span></span>   | <span data-ttu-id="f570f-196">int642Str</span><span class="sxs-lookup"><span data-stu-id="f570f-196">int642Str</span></span>    | <span data-ttu-id="f570f-197">num2Char</span><span class="sxs-lookup"><span data-stu-id="f570f-197">num2Char</span></span>     | <span data-ttu-id="f570f-198">num2Date</span><span class="sxs-lookup"><span data-stu-id="f570f-198">num2Date</span></span>   |
| <span data-ttu-id="f570f-199">num2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-199">num2Str</span></span>   | <span data-ttu-id="f570f-200">str2Date</span><span class="sxs-lookup"><span data-stu-id="f570f-200">str2Date</span></span>     | <span data-ttu-id="f570f-201">str2Datetime</span><span class="sxs-lookup"><span data-stu-id="f570f-201">str2Datetime</span></span> | <span data-ttu-id="f570f-202">str2Enum</span><span class="sxs-lookup"><span data-stu-id="f570f-202">str2Enum</span></span>   |
| <span data-ttu-id="f570f-203">str2Guid</span><span class="sxs-lookup"><span data-stu-id="f570f-203">str2Guid</span></span>  | <span data-ttu-id="f570f-204">str2Int</span><span class="sxs-lookup"><span data-stu-id="f570f-204">str2Int</span></span>      | <span data-ttu-id="f570f-205">str2Int64</span><span class="sxs-lookup"><span data-stu-id="f570f-205">str2Int64</span></span>    | <span data-ttu-id="f570f-206">str2Num</span><span class="sxs-lookup"><span data-stu-id="f570f-206">str2Num</span></span>    |
| <span data-ttu-id="f570f-207">str2Time</span><span class="sxs-lookup"><span data-stu-id="f570f-207">str2Time</span></span>  | <span data-ttu-id="f570f-208">time2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-208">time2Str</span></span>     | <span data-ttu-id="f570f-209">uint2Str</span><span class="sxs-lookup"><span data-stu-id="f570f-209">uint2Str</span></span>     |            |

## <a name="date"></a><span data-ttu-id="f570f-210">日</span><span class="sxs-lookup"><span data-stu-id="f570f-210">Date</span></span>
<span data-ttu-id="f570f-211">詳細については、[X++ 日付ランタイム関数](xpp-date-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-211">For more information, see [X++ Date Run-Time Functions](xpp-date-run-time-functions.md).</span></span>

|         |          |               |               |
|---------|----------|---------------|---------------|
| <span data-ttu-id="f570f-212">dayName</span><span class="sxs-lookup"><span data-stu-id="f570f-212">dayName</span></span> | <span data-ttu-id="f570f-213">dayOfMth</span><span class="sxs-lookup"><span data-stu-id="f570f-213">dayOfMth</span></span> | <span data-ttu-id="f570f-214">dayOfWk</span><span class="sxs-lookup"><span data-stu-id="f570f-214">dayOfWk</span></span>       | <span data-ttu-id="f570f-215">dayOfYr</span><span class="sxs-lookup"><span data-stu-id="f570f-215">dayOfYr</span></span>       |
| <span data-ttu-id="f570f-216">endMth</span><span class="sxs-lookup"><span data-stu-id="f570f-216">endMth</span></span>  | <span data-ttu-id="f570f-217">mkDate</span><span class="sxs-lookup"><span data-stu-id="f570f-217">mkDate</span></span>   | <span data-ttu-id="f570f-218">mthName</span><span class="sxs-lookup"><span data-stu-id="f570f-218">mthName</span></span>       | <span data-ttu-id="f570f-219">mthOfYr</span><span class="sxs-lookup"><span data-stu-id="f570f-219">mthOfYr</span></span>       |
| <span data-ttu-id="f570f-220">nextMth</span><span class="sxs-lookup"><span data-stu-id="f570f-220">nextMth</span></span> | <span data-ttu-id="f570f-221">nextQtr</span><span class="sxs-lookup"><span data-stu-id="f570f-221">nextQtr</span></span>  | <span data-ttu-id="f570f-222">nextYr</span><span class="sxs-lookup"><span data-stu-id="f570f-222">nextYr</span></span>        | <span data-ttu-id="f570f-223">prevMth</span><span class="sxs-lookup"><span data-stu-id="f570f-223">prevMth</span></span>       |
| <span data-ttu-id="f570f-224">prevQtr</span><span class="sxs-lookup"><span data-stu-id="f570f-224">prevQtr</span></span> | <span data-ttu-id="f570f-225">prevYr</span><span class="sxs-lookup"><span data-stu-id="f570f-225">prevYr</span></span>   | <span data-ttu-id="f570f-226">systemDateGet</span><span class="sxs-lookup"><span data-stu-id="f570f-226">systemDateGet</span></span> | <span data-ttu-id="f570f-227">systemDateSet</span><span class="sxs-lookup"><span data-stu-id="f570f-227">systemDateSet</span></span> |
| <span data-ttu-id="f570f-228">timeNow</span><span class="sxs-lookup"><span data-stu-id="f570f-228">timeNow</span></span> | <span data-ttu-id="f570f-229">今日</span><span class="sxs-lookup"><span data-stu-id="f570f-229">today</span></span>    | <span data-ttu-id="f570f-230">wkOfYr</span><span class="sxs-lookup"><span data-stu-id="f570f-230">wkOfYr</span></span>        | <span data-ttu-id="f570f-231">年</span><span class="sxs-lookup"><span data-stu-id="f570f-231">year</span></span>          |

## <a name="math"></a><span data-ttu-id="f570f-232">計算</span><span class="sxs-lookup"><span data-stu-id="f570f-232">Math</span></span>
<span data-ttu-id="f570f-233">詳細については、[X++ 数学ランタイム関数](xpp-math-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-233">For more information, see [X++ Math Run-Time Functions](xpp-math-run-time-functions.md).</span></span>

|         |          |               |               |
|---------|----------|---------------|---------------|
|<span data-ttu-id="f570f-234">abs</span><span class="sxs-lookup"><span data-stu-id="f570f-234">abs</span></span>|<span data-ttu-id="f570f-235">acos</span><span class="sxs-lookup"><span data-stu-id="f570f-235">acos</span></span>|<span data-ttu-id="f570f-236">asin</span><span class="sxs-lookup"><span data-stu-id="f570f-236">asin</span></span>|<span data-ttu-id="f570f-237">atan</span><span class="sxs-lookup"><span data-stu-id="f570f-237">atan</span></span>|
|<span data-ttu-id="f570f-238">corrFlagGet</span><span class="sxs-lookup"><span data-stu-id="f570f-238">corrFlagGet</span></span>|<span data-ttu-id="f570f-239">corrFlagSet</span><span class="sxs-lookup"><span data-stu-id="f570f-239">corrFlagSet</span></span>|<span data-ttu-id="f570f-240">cos</span><span class="sxs-lookup"><span data-stu-id="f570f-240">cos</span></span>|<span data-ttu-id="f570f-241">cosh</span><span class="sxs-lookup"><span data-stu-id="f570f-241">cosh</span></span>|
|<span data-ttu-id="f570f-242">decRound</span><span class="sxs-lookup"><span data-stu-id="f570f-242">decRound</span></span>|<span data-ttu-id="f570f-243">exp</span><span class="sxs-lookup"><span data-stu-id="f570f-243">exp</span></span>|<span data-ttu-id="f570f-244">exp10</span><span class="sxs-lookup"><span data-stu-id="f570f-244">exp10</span></span>|<span data-ttu-id="f570f-245">frac</span><span class="sxs-lookup"><span data-stu-id="f570f-245">frac</span></span>|
|<span data-ttu-id="f570f-246">log10</span><span class="sxs-lookup"><span data-stu-id="f570f-246">log10</span></span>|<span data-ttu-id="f570f-247">logN</span><span class="sxs-lookup"><span data-stu-id="f570f-247">logN</span></span>|<span data-ttu-id="f570f-248">最大</span><span class="sxs-lookup"><span data-stu-id="f570f-248">max</span></span>|<span data-ttu-id="f570f-249">最小</span><span class="sxs-lookup"><span data-stu-id="f570f-249">min</span></span>|
|<span data-ttu-id="f570f-250">power</span><span class="sxs-lookup"><span data-stu-id="f570f-250">power</span></span>|<span data-ttu-id="f570f-251">round</span><span class="sxs-lookup"><span data-stu-id="f570f-251">round</span></span>|<span data-ttu-id="f570f-252">sin</span><span class="sxs-lookup"><span data-stu-id="f570f-252">sin</span></span>|<span data-ttu-id="f570f-253">sinh</span><span class="sxs-lookup"><span data-stu-id="f570f-253">sinh</span></span>|
|<span data-ttu-id="f570f-254">tan</span><span class="sxs-lookup"><span data-stu-id="f570f-254">tan</span></span>|<span data-ttu-id="f570f-255">tanh</span><span class="sxs-lookup"><span data-stu-id="f570f-255">tanh</span></span>|<span data-ttu-id="f570f-256">trunc</span><span class="sxs-lookup"><span data-stu-id="f570f-256">trunc</span></span>||

## <a name="reflection"></a><span data-ttu-id="f570f-257">反映</span><span class="sxs-lookup"><span data-stu-id="f570f-257">Reflection</span></span>
<span data-ttu-id="f570f-258">詳細については、[X++ リフレクションランタイム関数](xpp-reflection-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-258">For more information, see [X++ Reflection Run-Time Functions](xpp-reflection-run-time-functions.md).</span></span>

|              |               |              |               |
|--------------|---------------|--------------|---------------|
| <span data-ttu-id="f570f-259">classIdGet</span><span class="sxs-lookup"><span data-stu-id="f570f-259">classIdGet</span></span>   | <span data-ttu-id="f570f-260">dimOf</span><span class="sxs-lookup"><span data-stu-id="f570f-260">dimOf</span></span>         | <span data-ttu-id="f570f-261">fieldId2Name</span><span class="sxs-lookup"><span data-stu-id="f570f-261">fieldId2Name</span></span> | <span data-ttu-id="f570f-262">fieldId2PName</span><span class="sxs-lookup"><span data-stu-id="f570f-262">fieldId2PName</span></span> |
| <span data-ttu-id="f570f-263">fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="f570f-263">fieldName2Id</span></span> | <span data-ttu-id="f570f-264">indexId2Name</span><span class="sxs-lookup"><span data-stu-id="f570f-264">indexId2Name</span></span>  | <span data-ttu-id="f570f-265">indexName2Id</span><span class="sxs-lookup"><span data-stu-id="f570f-265">indexName2Id</span></span> | <span data-ttu-id="f570f-266">refPrintAll</span><span class="sxs-lookup"><span data-stu-id="f570f-266">refPrintAll</span></span>   |
| <span data-ttu-id="f570f-267">tableId2Name</span><span class="sxs-lookup"><span data-stu-id="f570f-267">tableId2Name</span></span> | <span data-ttu-id="f570f-268">tableId2PName</span><span class="sxs-lookup"><span data-stu-id="f570f-268">tableId2PName</span></span> | <span data-ttu-id="f570f-269">tableName2Id</span><span class="sxs-lookup"><span data-stu-id="f570f-269">tableName2Id</span></span> | <span data-ttu-id="f570f-270">typeOf</span><span class="sxs-lookup"><span data-stu-id="f570f-270">typeOf</span></span>        |

## <a name="session"></a><span data-ttu-id="f570f-271">セッション</span><span class="sxs-lookup"><span data-stu-id="f570f-271">Session</span></span>
<span data-ttu-id="f570f-272">詳細については、[X++ セッション ランタイム関数](xpp-session-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-272">For more information, see [X++ Session Run-Time Functions](xpp-session-run-time-functions.md).</span></span>

|                          |           |           |                     |
|--------------------------|-----------|-----------|---------------------|
| <span data-ttu-id="f570f-273">curExt</span><span class="sxs-lookup"><span data-stu-id="f570f-273">curExt</span></span>                   | <span data-ttu-id="f570f-274">curUserId</span><span class="sxs-lookup"><span data-stu-id="f570f-274">curUserId</span></span> | <span data-ttu-id="f570f-275">funcName</span><span class="sxs-lookup"><span data-stu-id="f570f-275">funcName</span></span>  | <span data-ttu-id="f570f-276">getCurrentPartition</span><span class="sxs-lookup"><span data-stu-id="f570f-276">getCurrentPartition</span></span> |
| <span data-ttu-id="f570f-277">getCurrentPartitionRecId</span><span class="sxs-lookup"><span data-stu-id="f570f-277">getCurrentPartitionRecId</span></span> | <span data-ttu-id="f570f-278">getPrefix</span><span class="sxs-lookup"><span data-stu-id="f570f-278">getPrefix</span></span> | <span data-ttu-id="f570f-279">sessionId</span><span class="sxs-lookup"><span data-stu-id="f570f-279">sessionId</span></span> | <span data-ttu-id="f570f-280">prmIsDefault</span><span class="sxs-lookup"><span data-stu-id="f570f-280">prmIsDefault</span></span>        |
| <span data-ttu-id="f570f-281">runAs</span><span class="sxs-lookup"><span data-stu-id="f570f-281">runAs</span></span>                    | <span data-ttu-id="f570f-282">setPrefix</span><span class="sxs-lookup"><span data-stu-id="f570f-282">setPrefix</span></span> |           |                     |

## <a name="string"></a><span data-ttu-id="f570f-283">文字列</span><span class="sxs-lookup"><span data-stu-id="f570f-283">String</span></span>
<span data-ttu-id="f570f-284">詳細については、[X++ 文字列ランタイム関数](xpp-string-run-time-functions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f570f-284">For more information, see [X++ String Run-Time Functions](xpp-string-run-time-functions.md).</span></span>

|         |          |          |           |
|---------|----------|----------|-----------|
| <span data-ttu-id="f570f-285">照合</span><span class="sxs-lookup"><span data-stu-id="f570f-285">match</span></span>   | <span data-ttu-id="f570f-286">strAlpha</span><span class="sxs-lookup"><span data-stu-id="f570f-286">strAlpha</span></span> | <span data-ttu-id="f570f-287">strCmp</span><span class="sxs-lookup"><span data-stu-id="f570f-287">strCmp</span></span>   | <span data-ttu-id="f570f-288">strColSeq</span><span class="sxs-lookup"><span data-stu-id="f570f-288">strColSeq</span></span> |
| <span data-ttu-id="f570f-289">strDel</span><span class="sxs-lookup"><span data-stu-id="f570f-289">strDel</span></span>  | <span data-ttu-id="f570f-290">strFind</span><span class="sxs-lookup"><span data-stu-id="f570f-290">strFind</span></span>  | <span data-ttu-id="f570f-291">strFmt</span><span class="sxs-lookup"><span data-stu-id="f570f-291">strFmt</span></span>   | <span data-ttu-id="f570f-292">strIns</span><span class="sxs-lookup"><span data-stu-id="f570f-292">strIns</span></span>    |
| <span data-ttu-id="f570f-293">strKeep</span><span class="sxs-lookup"><span data-stu-id="f570f-293">strKeep</span></span> | <span data-ttu-id="f570f-294">strLen</span><span class="sxs-lookup"><span data-stu-id="f570f-294">strLen</span></span>   | <span data-ttu-id="f570f-295">strLine</span><span class="sxs-lookup"><span data-stu-id="f570f-295">strLine</span></span>  | <span data-ttu-id="f570f-296">strLTrim</span><span class="sxs-lookup"><span data-stu-id="f570f-296">strLTrim</span></span>  |
| <span data-ttu-id="f570f-297">strLwr</span><span class="sxs-lookup"><span data-stu-id="f570f-297">strLwr</span></span>  | <span data-ttu-id="f570f-298">strNFind</span><span class="sxs-lookup"><span data-stu-id="f570f-298">strNFind</span></span> | <span data-ttu-id="f570f-299">strPoke</span><span class="sxs-lookup"><span data-stu-id="f570f-299">strPoke</span></span>  | <span data-ttu-id="f570f-300">strPrompt</span><span class="sxs-lookup"><span data-stu-id="f570f-300">strPrompt</span></span> |
| <span data-ttu-id="f570f-301">strRem</span><span class="sxs-lookup"><span data-stu-id="f570f-301">strRem</span></span>  | <span data-ttu-id="f570f-302">strRep</span><span class="sxs-lookup"><span data-stu-id="f570f-302">strRep</span></span>   | <span data-ttu-id="f570f-303">strRTrim</span><span class="sxs-lookup"><span data-stu-id="f570f-303">strRTrim</span></span> | <span data-ttu-id="f570f-304">strScan</span><span class="sxs-lookup"><span data-stu-id="f570f-304">strScan</span></span>   |
| <span data-ttu-id="f570f-305">strUpr</span><span class="sxs-lookup"><span data-stu-id="f570f-305">strUpr</span></span>  | <span data-ttu-id="f570f-306">subStr</span><span class="sxs-lookup"><span data-stu-id="f570f-306">subStr</span></span>   |          |           |

## <a name="beep"></a><span data-ttu-id="f570f-307">beep</span><span class="sxs-lookup"><span data-stu-id="f570f-307">beep</span></span>
<span data-ttu-id="f570f-308">コンピューターのスピーカーから短いサウンドを出力します。</span><span class="sxs-lookup"><span data-stu-id="f570f-308">Emits a short sound from the speakers on the computer.</span></span>

    void beep()

### <a name="example"></a><span data-ttu-id="f570f-309">例</span><span class="sxs-lookup"><span data-stu-id="f570f-309">Example</span></span>

    static void beepExample(Args _args)
    {
            beep();
    }

## <a name="newguid"></a><span data-ttu-id="f570f-310">newGuid</span><span class="sxs-lookup"><span data-stu-id="f570f-310">newGuid</span></span>
<span data-ttu-id="f570f-311">グローバル一意識別子 (GUID) を作成します。</span><span class="sxs-lookup"><span data-stu-id="f570f-311">Creates a globally unique identifier (GUID).</span></span>

    guid newGuid()

### <a name="return-value"></a><span data-ttu-id="f570f-312">戻り値</span><span class="sxs-lookup"><span data-stu-id="f570f-312">Return value</span></span>

<span data-ttu-id="f570f-313">GUID。</span><span class="sxs-lookup"><span data-stu-id="f570f-313">A GUID.</span></span>

### <a name="example"></a><span data-ttu-id="f570f-314">例</span><span class="sxs-lookup"><span data-stu-id="f570f-314">Example</span></span>

<span data-ttu-id="f570f-315">次の例では、GUID を作成します。</span><span class="sxs-lookup"><span data-stu-id="f570f-315">The following example creates a GUID.</span></span>

    static void newGuidExample(Args _arg)
    {
            guid myGuid;

            myGuid = newguid();
            print strfmt("The GUID is: %1", myGuid);
    }

## <a name="sleep"></a><span data-ttu-id="f570f-316">sleep</span><span class="sxs-lookup"><span data-stu-id="f570f-316">sleep</span></span>
<span data-ttu-id="f570f-317">指定されたミリ秒間、現在のスレッドの実行を一時停止します。</span><span class="sxs-lookup"><span data-stu-id="f570f-317">Pauses the execution of the current thread for the specified number of milliseconds.</span></span>

    int sleep(int _duration)

### <a name="parameters"></a><span data-ttu-id="f570f-318">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f570f-318">Parameters</span></span>

| <span data-ttu-id="f570f-319">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f570f-319">Parameter</span></span>  | <span data-ttu-id="f570f-320">説明</span><span class="sxs-lookup"><span data-stu-id="f570f-320">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="f570f-321">\_期間</span><span class="sxs-lookup"><span data-stu-id="f570f-321">\_duration</span></span> | <span data-ttu-id="f570f-322">一時停止するミリ秒数。</span><span class="sxs-lookup"><span data-stu-id="f570f-322">The number of milliseconds to pause.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f570f-323">戻り値</span><span class="sxs-lookup"><span data-stu-id="f570f-323">Return value</span></span>

<span data-ttu-id="f570f-324">スレッドが実際に一時停止した時間 (ミリ秒)。</span><span class="sxs-lookup"><span data-stu-id="f570f-324">The number of milliseconds that the thread actually paused.</span></span>

### <a name="example"></a><span data-ttu-id="f570f-325">例</span><span class="sxs-lookup"><span data-stu-id="f570f-325">Example</span></span>

    static void sleepExample(Args _arg)
    {
            int seconds = 10;
            int i;

            i = sleep(seconds*1000);
            print "job slept for " + int2str(i/1000) + " seconds";
    }





