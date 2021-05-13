---
title: X++ 日付ランタイム関数
description: このトピックでは、日付ランタイム関数について説明します。
author: RobinARH
ms.date: 11/03/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31341
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 928eeb52a0f8a14c7b97544e29cb23cefb5fda38
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865904"
---
# <a name="x-date-runtime-functions"></a><span data-ttu-id="5e360-103">X++ 日付ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="5e360-103">X++ date runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e360-104">このトピックでは、日付ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e360-104">This topic describes the date run-time functions.</span></span>

<a name="dayname"></a><span data-ttu-id="5e360-105">dayName</span><span class="sxs-lookup"><span data-stu-id="5e360-105">dayName</span></span>
-------

<span data-ttu-id="5e360-106">番号で指定されている曜日の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-106">Retrieves the name of the day of the week that is specified by a number.</span></span>

```xpp
str dayName(int number)
```

### <a name="parameters"></a><span data-ttu-id="5e360-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-107">Parameters</span></span>

| <span data-ttu-id="5e360-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-108">Parameter</span></span> | <span data-ttu-id="5e360-109">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-109">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="5e360-110">数値</span><span class="sxs-lookup"><span data-stu-id="5e360-110">number</span></span>    | <span data-ttu-id="5e360-111">週内の日付の数。</span><span class="sxs-lookup"><span data-stu-id="5e360-111">The number of a day in a week.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-112">Return value</span></span>

<span data-ttu-id="5e360-113">番号パラメーターで指定された曜日。</span><span class="sxs-lookup"><span data-stu-id="5e360-113">The day of the week specified by the number parameter.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-114">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-114">Remarks</span></span>

<span data-ttu-id="5e360-115">番号のパラメーターの有効値は **1** ～ **7** です。</span><span class="sxs-lookup"><span data-stu-id="5e360-115">The valid values for the number parameter are **1** through **7**.</span></span> <span data-ttu-id="5e360-116">月曜日は **1**、火曜日は **2**、日曜日は **7** として表されます。</span><span class="sxs-lookup"><span data-stu-id="5e360-116">Monday is represented by **1**, Tuesday by **2**, and Sunday by **7**.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-117">例</span><span class="sxs-lookup"><span data-stu-id="5e360-117">Example</span></span>

```xpp
static void dayNameExample(Args _arg)
{
    str s;
    ;
    s = dayName(01);
    print "First day of the week's name is " + s;
    pause;
}
```

## <a name="dayofmth"></a><span data-ttu-id="5e360-118">dayOfMth</span><span class="sxs-lookup"><span data-stu-id="5e360-118">dayOfMth</span></span>
<span data-ttu-id="5e360-119">指定された日付の月内の日数を計算します。</span><span class="sxs-lookup"><span data-stu-id="5e360-119">Calculates the number of the day in the month for the specified date.</span></span>

```xpp
int dayOfMth(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-120">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-120">Parameters</span></span>

| <span data-ttu-id="5e360-121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-121">Parameter</span></span> | <span data-ttu-id="5e360-122">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-122">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="5e360-123">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-123">date</span></span>      | <span data-ttu-id="5e360-124">テストする日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-124">The date to test.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-125">Return value</span></span>

<span data-ttu-id="5e360-126">指定された日付の月の日を示す 1 から 31 までの整数。</span><span class="sxs-lookup"><span data-stu-id="5e360-126">An integer between 1 and 31 that indicates the day of the month for the specified date.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-127">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-127">Remarks</span></span>

```xpp
dayOfMth(31122001) //returns 31.
```

### <a name="example"></a><span data-ttu-id="5e360-128">例</span><span class="sxs-lookup"><span data-stu-id="5e360-128">Example</span></span>

```xpp
static void dayOfMthExample(Args _arg)
{
    date d = today();
    int i;
    ;
    i = dayOfMth(d);
    print "Today's day of the month is " + int2Str(i);
    pause;
}
```

## <a name="dayofwk"></a><span data-ttu-id="5e360-129">dayOfWk</span><span class="sxs-lookup"><span data-stu-id="5e360-129">dayOfWk</span></span>
<span data-ttu-id="5e360-130">指定された日付の週内の日数を計算します。</span><span class="sxs-lookup"><span data-stu-id="5e360-130">Calculates the number of day in the week for the specified date.</span></span> <span data-ttu-id="5e360-131">**注記:** 月曜日は **1**、火曜日は **2**、日曜日は **7** として表されます。</span><span class="sxs-lookup"><span data-stu-id="5e360-131">**Note:** Monday is represented by **1**, Tuesday by **2**, and Sunday by **7**.</span></span>

```xpp
int dayOfWk(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-132">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-132">Parameters</span></span>

| <span data-ttu-id="5e360-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-133">Parameter</span></span> | <span data-ttu-id="5e360-134">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-134">Description</span></span>                                               |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="5e360-135">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-135">date</span></span>      | <span data-ttu-id="5e360-136">年、月、日を示す **日付** 値。</span><span class="sxs-lookup"><span data-stu-id="5e360-136">A **date** value that indicates the year, month, and day.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-137">Return value</span></span>

<span data-ttu-id="5e360-138">指定された曜日の数。</span><span class="sxs-lookup"><span data-stu-id="5e360-138">The number of the specified day in the week.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-139">例</span><span class="sxs-lookup"><span data-stu-id="5e360-139">Example</span></span>

```xpp
static void dayOfWkExample(Args _arg)
{
    date d = today();
    int i;
    ;
    i = dayOfWk(d);
    print "Today's day of the week is " + int2Str(i);
    pause;
}
```

## <a name="dayofyr"></a><span data-ttu-id="5e360-140">dayOfYr</span><span class="sxs-lookup"><span data-stu-id="5e360-140">dayOfYr</span></span>
<span data-ttu-id="5e360-141">1 月 1 日から指定された日までの日数を計算します。</span><span class="sxs-lookup"><span data-stu-id="5e360-141">Calculates the number of days between January 1 and the specified date.</span></span>

```xpp
int dayOfYr(date _date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-142">Parameters</span></span>

| <span data-ttu-id="5e360-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-143">Parameter</span></span> | <span data-ttu-id="5e360-144">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-144">Description</span></span>                                     |
|-----------|-------------------------------------------------|
| <span data-ttu-id="5e360-145">\_ 日付</span><span class="sxs-lookup"><span data-stu-id="5e360-145">\_date</span></span>    | <span data-ttu-id="5e360-146">年、月、日を指定する日付です。</span><span class="sxs-lookup"><span data-stu-id="5e360-146">A date that specifies the year, month, and day.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-147">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-147">Return value</span></span>

<span data-ttu-id="5e360-148">1 月 1 日から指定された日付までの日数。</span><span class="sxs-lookup"><span data-stu-id="5e360-148">The number of days between January 1 and the specified date, inclusive.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-149">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-149">Remarks</span></span>

<span data-ttu-id="5e360-150">1 月 1 日は **1**、12 月 31 日は **365** または **366** です。</span><span class="sxs-lookup"><span data-stu-id="5e360-150">January 1 is **1**, and December 31 is either **365** or **366**.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-151">例</span><span class="sxs-lookup"><span data-stu-id="5e360-151">Example</span></span>

```xpp
static void dayOfYrExample(Args _arg)
{
    date d = today();
    int i;
    ;
    i = dayOfYr(d);
    print "Today's day of the year is " + int2Str(i);
    pause;
}
```

## <a name="endmth"></a><span data-ttu-id="5e360-152">endMth</span><span class="sxs-lookup"><span data-stu-id="5e360-152">endMth</span></span>
<span data-ttu-id="5e360-153">指定した日付の月の最後の日付を計算します。</span><span class="sxs-lookup"><span data-stu-id="5e360-153">Calculates the last date in the month of the specified date.</span></span>

```xpp
date endMth(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-154">Parameters</span></span>

| <span data-ttu-id="5e360-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-155">Parameter</span></span> | <span data-ttu-id="5e360-156">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-156">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="5e360-157">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-157">date</span></span>      | <span data-ttu-id="5e360-158">年、月、日を示す **日付** 値。</span><span class="sxs-lookup"><span data-stu-id="5e360-158">A **date** value that indicates a year, month, and day.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-159">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-159">Return value</span></span>

<span data-ttu-id="5e360-160">指定した月の最後の日付の **date** 値。</span><span class="sxs-lookup"><span data-stu-id="5e360-160">The **date** value of the last day in the specified month.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-161">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-161">Remarks</span></span>

```xpp
endMth(0221988); //Returns the date 2921988 because 1988 is a leap year.
endMth(0221989); //Returns the date 2821989.
```

## <a name="mkdate"></a><span data-ttu-id="5e360-162">mkDate</span><span class="sxs-lookup"><span data-stu-id="5e360-162">mkDate</span></span>
<span data-ttu-id="5e360-163">日、月、および年を示す 3 つの整数に基づいて日付を作成します。</span><span class="sxs-lookup"><span data-stu-id="5e360-163">Creates a date, based on three integers that indicate the day, month, and year, respectively.</span></span>

```xpp
date mkDate(int day, int month, int year)
```

### <a name="parameters"></a><span data-ttu-id="5e360-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-164">Parameters</span></span>

| <span data-ttu-id="5e360-165">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-165">Parameter</span></span> | <span data-ttu-id="5e360-166">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-166">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="5e360-167">日</span><span class="sxs-lookup"><span data-stu-id="5e360-167">day</span></span>       | <span data-ttu-id="5e360-168">月の日を表す整数。</span><span class="sxs-lookup"><span data-stu-id="5e360-168">An integer that represents the day of the month.</span></span>                          |
| <span data-ttu-id="5e360-169">月</span><span class="sxs-lookup"><span data-stu-id="5e360-169">month</span></span>     | <span data-ttu-id="5e360-170">年の月を表す整数。</span><span class="sxs-lookup"><span data-stu-id="5e360-170">An integer that represents the month of the year.</span></span>                         |
| <span data-ttu-id="5e360-171">年</span><span class="sxs-lookup"><span data-stu-id="5e360-171">year</span></span>      | <span data-ttu-id="5e360-172">1900 年から 2154 年の間で必要とする年を表す整数。</span><span class="sxs-lookup"><span data-stu-id="5e360-172">An integer that represents the year, which must be between 1900 and 2154.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-173">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-173">Return value</span></span>

<span data-ttu-id="5e360-174">*日*、*月*、および *年* のパラメーター値に基づく **日付** 値。</span><span class="sxs-lookup"><span data-stu-id="5e360-174">A **date** value that is based on the values of the *day*, *month*, and *year* parameters.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-175">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-175">Remarks</span></span>

<span data-ttu-id="5e360-176">データが無効である場合は、このメソッドは **0** (zero, 1/1/1900) 日付を返します。</span><span class="sxs-lookup"><span data-stu-id="5e360-176">If the date isn't valid, this method returns a **0** (zero, 1/1/1900) date.</span></span> <span data-ttu-id="5e360-177">Dynamics AX 7.0 (2016 年 2 月) から、1975 年の 75 のような、その年のショートカット値はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5e360-177">Beginning with Dynamics AX 7.0(February 2016), shortcut values for the year, e.g. 75 for 1975, are not supported.</span></span> <span data-ttu-id="5e360-178">その年のショートカット値を指定すると、1900 年 1 月 1 日の日付が返されます。</span><span class="sxs-lookup"><span data-stu-id="5e360-178">If you provide a shortcut value for the year, a date of 1/1/1900 is returned.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-179">例</span><span class="sxs-lookup"><span data-stu-id="5e360-179">Example</span></span>

```xpp
static void mkDateExample(Args _arg)
{
    date d;
    ;
    // Returns the date 0112005.
    d = mkDate(1, 1, 2005);
    print d;
    pause;
}
```

## <a name="mthname"></a><span data-ttu-id="5e360-180">mthName</span><span class="sxs-lookup"><span data-stu-id="5e360-180">mthName</span></span>
<span data-ttu-id="5e360-181">指定された月の名前を取得します</span><span class="sxs-lookup"><span data-stu-id="5e360-181">Retrieves the name of the specified month</span></span>

```xpp
str monthName(int number)
```

### <a name="parameters"></a><span data-ttu-id="5e360-182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-182">Parameters</span></span>

| <span data-ttu-id="5e360-183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-183">Parameter</span></span> | <span data-ttu-id="5e360-184">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-184">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="5e360-185">数値</span><span class="sxs-lookup"><span data-stu-id="5e360-185">number</span></span>    | <span data-ttu-id="5e360-186">月の番号。</span><span class="sxs-lookup"><span data-stu-id="5e360-186">The number of the month.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-187">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-187">Return value</span></span>

<span data-ttu-id="5e360-188">指定された月の名前。</span><span class="sxs-lookup"><span data-stu-id="5e360-188">The name of the specified month.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-189">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-189">Remarks</span></span>

<span data-ttu-id="5e360-190">*番号* のパラメーターの有効値は **1** ～ **12** です。</span><span class="sxs-lookup"><span data-stu-id="5e360-190">The valid values of the *number* parameter are **1** through **12**.</span></span> <span data-ttu-id="5e360-191">1 月は **1** で、12 月は **12** で表されます。</span><span class="sxs-lookup"><span data-stu-id="5e360-191">January is represented by **1** and December by **12**.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-192">例</span><span class="sxs-lookup"><span data-stu-id="5e360-192">Example</span></span>

```xpp
static void mthNameExample(Args _arg)
{
    str s;
    ;
    // MthName(6) returns the text string "June".
    s = mthName(6);
    print "Month name is " + s;
    pause;
}
```

## <a name="mthofyr"></a><span data-ttu-id="5e360-193">mthOfYr</span><span class="sxs-lookup"><span data-stu-id="5e360-193">mthOfYr</span></span>
<span data-ttu-id="5e360-194">指定された日付の年内の月数を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-194">Retrieves the number of the month in the year for the specified date.</span></span> <span data-ttu-id="5e360-195">**注記:** 1 月は **1**、2 月は **2**、12 月は **12** となります。</span><span class="sxs-lookup"><span data-stu-id="5e360-195">**Note:** January is **1**, February is **2**, and December is **12**.</span></span>

```xpp
int mthOfYr(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-196">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-196">Parameters</span></span>

| <span data-ttu-id="5e360-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-197">Parameter</span></span> | <span data-ttu-id="5e360-198">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-198">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="5e360-199">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-199">date</span></span>      | <span data-ttu-id="5e360-200">年月日を指定する日付です。</span><span class="sxs-lookup"><span data-stu-id="5e360-200">A date that specifies a year, month, and day.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-201">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-201">Return value</span></span>

<span data-ttu-id="5e360-202">*日付* パラメーターで表される月の年の月の数字。</span><span class="sxs-lookup"><span data-stu-id="5e360-202">The number of the month in the year, for the month that is represented by the *date* parameter.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-203">例</span><span class="sxs-lookup"><span data-stu-id="5e360-203">Example</span></span>

```xpp
static void mthOfYrExample(Args _arg)
{
    int i;
    ;
    i = mthOfYr(today());
    print "The number of the month in today's date is " + int2Str(i);
    pause;
}
```

## <a name="nextmth"></a><span data-ttu-id="5e360-204">nextMth</span><span class="sxs-lookup"><span data-stu-id="5e360-204">nextMth</span></span>
<span data-ttu-id="5e360-205">指定した日付に最も近い、対応する次の月の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-205">Retrieves the date in the following month that corresponds most closely to the specified date.</span></span>

```xpp
date nextMth(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-206">Parameters</span></span>

| <span data-ttu-id="5e360-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-207">Parameter</span></span> | <span data-ttu-id="5e360-208">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-208">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="5e360-209">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-209">date</span></span>      | <span data-ttu-id="5e360-210">翌月に一致する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-210">The date to match in the following month.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-211">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-211">Return value</span></span>

<span data-ttu-id="5e360-212">翌月に指定された日付に最も近い一致。</span><span class="sxs-lookup"><span data-stu-id="5e360-212">The closest match to the specified date that is found in the next month.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-213">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-213">Remarks</span></span>

```xpp
nextMth(2921996); //returns 29/03/1996.
nextMth(3111996); //returns 2921996, because 1996 is a leap year.
```

### <a name="example"></a><span data-ttu-id="5e360-214">例</span><span class="sxs-lookup"><span data-stu-id="5e360-214">Example</span></span>

```xpp
static void nextMthExample(Args _arg)
{
    date d;
    ;
    d = nextMth(today());
    print "Closest date next month is "
    + date2Str(d, 2, 2, -1, 2, -1, 4);
    pause;
}
```

## <a name="nextqtr"></a><span data-ttu-id="5e360-215">nextQtr</span><span class="sxs-lookup"><span data-stu-id="5e360-215">nextQtr</span></span>
<span data-ttu-id="5e360-216">指定した日付に最も近い、対応する次の四半期の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-216">Retrieves the date in the following quarter that corresponds most closely to the specified date.</span></span>

```xpp
date nextQtr(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-217">Parameters</span></span>

| <span data-ttu-id="5e360-218">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-218">Parameter</span></span> | <span data-ttu-id="5e360-219">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-219">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="5e360-220">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-220">date</span></span>      | <span data-ttu-id="5e360-221">翌四半期に一致する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-221">The date to match in the following quarter.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-222">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-222">Return value</span></span>

<span data-ttu-id="5e360-223">次の四半期に指定された日付に最も近い一致。</span><span class="sxs-lookup"><span data-stu-id="5e360-223">The closest match to specified date that is found in the next quarter.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-224">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-224">Remarks</span></span>

<span data-ttu-id="5e360-225">たとえば、**nextQtr(3111998)** は **3041998** を返します。</span><span class="sxs-lookup"><span data-stu-id="5e360-225">For example, **nextQtr(3111998)** returns **3041998**.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-226">例</span><span class="sxs-lookup"><span data-stu-id="5e360-226">Example</span></span>

```xpp
static void nextQtrExample(Args _arg)
{
    date d;
    ;
    d = nextQtr(today());
    print "Closest date next quarter is "
        + date2Str(d, 2, 2, -1, 2, -1, 4);
    pause;
}
```

## <a name="nextyr"></a><span data-ttu-id="5e360-227">nextYr</span><span class="sxs-lookup"><span data-stu-id="5e360-227">nextYr</span></span>
<span data-ttu-id="5e360-228">指定した日付に最も近い、対応する次の年の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-228">Retrieves the date in the following year that corresponds most closely to the specified date.</span></span>

```xpp
date nextYr(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-229">Parameters</span></span>

| <span data-ttu-id="5e360-230">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-230">Parameter</span></span> | <span data-ttu-id="5e360-231">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-231">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="5e360-232">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-232">date</span></span>      | <span data-ttu-id="5e360-233">翌年に一致する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-233">The date to match in the following year.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-234">Return value</span></span>

<span data-ttu-id="5e360-235">翌年に指定された日付に最も近い一致。</span><span class="sxs-lookup"><span data-stu-id="5e360-235">The closest match to the specified date that is found in the following year.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-236">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-236">Remarks</span></span>

<span data-ttu-id="5e360-237">たとえば、**nextyr(2921998)** は **2821999** を返します。</span><span class="sxs-lookup"><span data-stu-id="5e360-237">For example, **nextyr(2921998)** returns **2821999**.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-238">例</span><span class="sxs-lookup"><span data-stu-id="5e360-238">Example</span></span>

```xpp
static void nextYrExample(Args _arg)
{
    date d;
    ;
    d = nextYr(today());
    print "Closest date next year is "
        + date2Str(d, 2, 2, -1, 2, -1, 4);
    pause;
}
```

## <a name="prevmth"></a><span data-ttu-id="5e360-239">prevMth</span><span class="sxs-lookup"><span data-stu-id="5e360-239">prevMth</span></span>
<span data-ttu-id="5e360-240">指定した日付に最も近い、対応する前の月の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-240">Retrieves the date in the previous month that corresponds most closely to the specified date.</span></span>

```xpp
date prevMth(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-241">Parameters</span></span>

| <span data-ttu-id="5e360-242">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-242">Parameter</span></span> | <span data-ttu-id="5e360-243">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-243">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="5e360-244">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-244">date</span></span>      | <span data-ttu-id="5e360-245">前月に一致する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-245">The date to match in the previous month.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-246">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-246">Return value</span></span>

<span data-ttu-id="5e360-247">前月に指定された日付に最も近い一致。</span><span class="sxs-lookup"><span data-stu-id="5e360-247">The closest match to the specified date that is found in the previous month.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-248">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-248">Remarks</span></span>

```xpp
prevMth(3131996); //Returns the date 29/02/1996 because 1996 is a leap year.
prevMth(2821998); //Returns the date 28/01/1998.
```

## <a name="prevqtr"></a><span data-ttu-id="5e360-249">prevQtr</span><span class="sxs-lookup"><span data-stu-id="5e360-249">prevQtr</span></span>
<span data-ttu-id="5e360-250">指定した日付に最も近い、対応する前の四半期の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-250">Retrieves the date in the previous quarter that corresponds most closely to the specified date.</span></span>

```xpp
date prevQtr(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-251">Parameters</span></span>

| <span data-ttu-id="5e360-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-252">Parameter</span></span> | <span data-ttu-id="5e360-253">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-253">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="5e360-254">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-254">date</span></span>      | <span data-ttu-id="5e360-255">前四半期に一致する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-255">The date to match in the previous quarter.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-256">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-256">Return value</span></span>

<span data-ttu-id="5e360-257">前の四半期に指定された日付に最も近い一致。</span><span class="sxs-lookup"><span data-stu-id="5e360-257">The closest match to the specified date that is found in the previous quarter.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-258">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-258">Remarks</span></span>

```xpp
prevQtr(3041998); //Returns the date 30/01/1998.
prevQtr(2951996); //Returns the date 29/02/1996, because 1996 is a leap year.
```

## <a name="prevyr"></a><span data-ttu-id="5e360-259">prevYr</span><span class="sxs-lookup"><span data-stu-id="5e360-259">prevYr</span></span>
<span data-ttu-id="5e360-260">指定した日付に最も近い、対応する前の年の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-260">Retrieves the date in the previous year that corresponds most closely to the specified date.</span></span>

```xpp
date prevYr(date date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-261">Parameters</span></span>

| <span data-ttu-id="5e360-262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-262">Parameter</span></span> | <span data-ttu-id="5e360-263">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-263">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="5e360-264">日付</span><span class="sxs-lookup"><span data-stu-id="5e360-264">date</span></span>      | <span data-ttu-id="5e360-265">前年に一致する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-265">The date to match in the previous year.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-266">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-266">Return value</span></span>

<span data-ttu-id="5e360-267">前年に指定された日付に最も近い一致。</span><span class="sxs-lookup"><span data-stu-id="5e360-267">The closest match to the specified date that is found in the previous year.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-268">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-268">Remarks</span></span>

```xpp
prevYr(2921996); //Returns the date 28/02/1995 because 1996 is a leap year.
prevYr(2821998); //Returns the date 28/02/1997.
```

## <a name="systemdateget"></a><span data-ttu-id="5e360-269">systemDateGet</span><span class="sxs-lookup"><span data-stu-id="5e360-269">systemDateGet</span></span>
<span data-ttu-id="5e360-270">設定されている場合は、セッションの日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-270">Retrieves the session date, if it has been set.</span></span>

```xpp
date systemDateGet()
```

### <a name="return-value"></a><span data-ttu-id="5e360-271">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-271">Return value</span></span>

<span data-ttu-id="5e360-272">セッションの日付が設定されている場合はそれを返します。それ以外の場合はシステムの日付を返します。</span><span class="sxs-lookup"><span data-stu-id="5e360-272">The session date if it has been set; otherwise, the system date.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-273">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-273">Remarks</span></span>

<span data-ttu-id="5e360-274">**セッション日時** ページを開くには、**ツール** メニューの **セッション日時** を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5e360-274">Consider using **Session date and time** on the **Tools** menu to open the **Session date and time** page.</span></span> <span data-ttu-id="5e360-275">このページを使用して、セッションの日付を有効に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5e360-275">This page can be used to actively set the session date.</span></span> <span data-ttu-id="5e360-276">システムによってこの設定されたアクションが検出されると、その後の **systemDateGet** 関数の呼び出しによってセッションの日付が返されます。</span><span class="sxs-lookup"><span data-stu-id="5e360-276">After this set action is detected by the system, subsequent calls to the **systemDateGet** function return the session date.</span></span> <span data-ttu-id="5e360-277">**today** 関数は、システム日付を返します。</span><span class="sxs-lookup"><span data-stu-id="5e360-277">The **today** function returns the system date.</span></span> <span data-ttu-id="5e360-278">この関数は、タイム ゾーンをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5e360-278">This function doesn't support time zones.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-279">例</span><span class="sxs-lookup"><span data-stu-id="5e360-279">Example</span></span>

<span data-ttu-id="5e360-280">次の例は、Infolog ウィンドウの日付を示しています。</span><span class="sxs-lookup"><span data-stu-id="5e360-280">The following example shows the date in the Infolog window.</span></span>

```xpp
static void Job_systemDateGet(Args _arg)
{
    info( date2Str(
        systemDateGet(),        // X++ language function.
        321,                    // 321 = ymd
        DateDay::Digits2,
        DateSeparator::Hyphen,  // separator1
        DateMonth::Digits2,
        DateSeparator::Hyphen,  // separator2
        DateYear::Digits4
    )
);
/*********** Actual Infolog output
Message (03:46:00 pm)
2012-04-16
***********/
}
```

## <a name="systemdateset"></a><span data-ttu-id="5e360-281">systemDateSet</span><span class="sxs-lookup"><span data-stu-id="5e360-281">systemDateSet</span></span>
<span data-ttu-id="5e360-282">システム日付を変更します。</span><span class="sxs-lookup"><span data-stu-id="5e360-282">Changes the system date.</span></span>

```xpp
date systemDateSet(date _date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-283">Parameters</span></span>

| <span data-ttu-id="5e360-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-284">Parameter</span></span> | <span data-ttu-id="5e360-285">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-285">Description</span></span>                  |
|-----------|------------------------------|
| <span data-ttu-id="5e360-286">\_ 日付</span><span class="sxs-lookup"><span data-stu-id="5e360-286">\_date</span></span>    | <span data-ttu-id="5e360-287">システムの新しい日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-287">The new date for the system.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-288">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-288">Return value</span></span>

<span data-ttu-id="5e360-289">新しいシステム日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-289">The new system date.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-290">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-290">Remarks</span></span>

<span data-ttu-id="5e360-291">この関数は、セッションの日付には影響しません。</span><span class="sxs-lookup"><span data-stu-id="5e360-291">This function doesn't affect the session date.</span></span> <span data-ttu-id="5e360-292">このメソッドは日付を変更しますが、時刻は **0** (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5e360-292">This method changes the date, but the time will be set to **0** (zero).</span></span>

### <a name="example"></a><span data-ttu-id="5e360-293">例</span><span class="sxs-lookup"><span data-stu-id="5e360-293">Example</span></span>

<span data-ttu-id="5e360-294">次の例では、システムの日付を今日の日付に設定します。</span><span class="sxs-lookup"><span data-stu-id="5e360-294">The following example sets the system date to today's date.</span></span>

```xpp
static void systemDateSetExample(Args _arg)
{
    date d = today();
    d = systemDateSet(d);
    print d;
}
```

## <a name="timenow"></a><span data-ttu-id="5e360-295">timeNow</span><span class="sxs-lookup"><span data-stu-id="5e360-295">timeNow</span></span>
<span data-ttu-id="5e360-296">現在のシステム時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-296">Retrieves the current system time.</span></span>

```xpp
int timeNow()
```

### <a name="return-value"></a><span data-ttu-id="5e360-297">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-297">Return value</span></span>

<span data-ttu-id="5e360-298">午前0時から経過した秒数。</span><span class="sxs-lookup"><span data-stu-id="5e360-298">The number of seconds that have passed since midnight.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-299">例</span><span class="sxs-lookup"><span data-stu-id="5e360-299">Example</span></span>

```xpp
static void timeNowExample(Args _arg)
{
    int i;
    ;
    i = timeNow();
    print "The number of seconds since midnight is " + int2Str(i);
    pause;
}
```

## <a name="today"></a><span data-ttu-id="5e360-300">今日</span><span class="sxs-lookup"><span data-stu-id="5e360-300">today</span></span>
<span data-ttu-id="5e360-301">システムの現在の日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-301">Retrieves the current date on the system.</span></span>

```xpp
date today()
```

### <a name="return-value"></a><span data-ttu-id="5e360-302">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-302">Return value</span></span>

<span data-ttu-id="5e360-303">現在の日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-303">The current date.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-304">例</span><span class="sxs-lookup"><span data-stu-id="5e360-304">Example</span></span>

```xpp
static void todayExample(Args _arg)
{
    date d;
    ;
    d = today();
    print "Today's date is " + date2Str(d, 0, 2, -1, 2, -1, 4);
    pause;
}
```

## <a name="wkofyr"></a><span data-ttu-id="5e360-305">wkOfYr</span><span class="sxs-lookup"><span data-stu-id="5e360-305">wkOfYr</span></span>
<span data-ttu-id="5e360-306">ISO 8601 仕様に従って、日付に該当する年の週を計算します。</span><span class="sxs-lookup"><span data-stu-id="5e360-306">Calculates the week of the year that a date falls in, according to the ISO 8601 specification.</span></span>

```xpp
int wkOfYr(date _date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-307">Parameters</span></span>

| <span data-ttu-id="5e360-308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-308">Parameter</span></span> | <span data-ttu-id="5e360-309">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-309">Description</span></span>                                     |
|-----------|-------------------------------------------------|
| <span data-ttu-id="5e360-310">\_ 日付</span><span class="sxs-lookup"><span data-stu-id="5e360-310">\_date</span></span>    | <span data-ttu-id="5e360-311">その年の週を計算する日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-311">The date to calculate the week of the year for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-312">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-312">Return value</span></span>

<span data-ttu-id="5e360-313">*\_date* パラメーターが発生する週のシーケンス番号。</span><span class="sxs-lookup"><span data-stu-id="5e360-313">The sequence number of the week that the *\_date* parameter occurs in.</span></span>

### <a name="example"></a><span data-ttu-id="5e360-314">例</span><span class="sxs-lookup"><span data-stu-id="5e360-314">Example</span></span>

<span data-ttu-id="5e360-315">次のコード例は、**wkOfYr** 関数と **Global::weekOfYear** メソッドを比較します。</span><span class="sxs-lookup"><span data-stu-id="5e360-315">The following code example compares the **wkOfYr** function with the **Global::weekOfYear** method.</span></span> <span data-ttu-id="5e360-316">関数とメソッドは異なる結果を生成します。</span><span class="sxs-lookup"><span data-stu-id="5e360-316">The function and the method produce different results.</span></span>

```xpp
// X++ job, under AOT > Jobs.
static void WeekTests3Job(Args _args)
{
int weekNum, i;
date dateTest;
str sMessages[];
//---------------------------------------------
sMessages[1] = "----- #1.  For Sunday, January 5, 2003 -----";
dateTest = 512003; // DayMonthYear  format.
weekNum = wkOfYr(dateTest);
sMessages[2] = int2str(weekNum) + " = wkOfYr funtion";
weekNum = Global::weekOfYear(dateTest);
sMessages[3] = int2str(weekNum) + " = Global::weekOfYear method";
//---------------------------------------------
sMessages[4] = " ";
sMessages[5] = "----- #2.  For Wednesday, August 20, 2003 -----";
dateTest = 2082003;
weekNum = wkOfYr(dateTest);
sMessages[6] = int2str(weekNum) + " = wkOfYr funtion";
weekNum = Global::weekOfYear(dateTest);
sMessages[7] = int2str(weekNum) + " = Global::weekOfYear method";
//---------------------------------------------
sMessages[8] = " ";
sMessages[9] = "----- #3.  For Sunday, December 28, 2003 -----";
dateTest = 28122003;
weekNum = wkOfYr(dateTest);
sMessages[10] = int2str(weekNum) + " = wkOfYr funtion";
weekNum = Global::weekOfYear(dateTest);
sMessages[11] = int2str(weekNum) + " = Global::weekOfYear method";
for (i=1; i<= 11; i++)
{
Global::info(sMessages[i]);
}
}
```

<span data-ttu-id="5e360-317">上記の例は、次の情報を表示のために情報ログに送信します。</span><span class="sxs-lookup"><span data-stu-id="5e360-317">The previous example sent the following information to the Infolog for display.</span></span> <span data-ttu-id="5e360-318">出力は、**wkOfYr** と **Global::weekOfYear** の間に違いがあることを示しています。</span><span class="sxs-lookup"><span data-stu-id="5e360-318">The output shows that there are differences between **wkOfYr** and **Global::weekOfYear**.</span></span> 

```xpp
Message (01:59:13 pm) ----- 
#1. For Sunday, January 5, 2003 ----- 1 = wkOfYr function 2 = Global::weekOfYear method ----- 
#2. For Wednesday, August 20, 2003 ----- 34 = wkOfYr function 34 = Global::weekOfYear method ----- 
#3. For Sunday, December 28, 2003 ----- 52 = wkOfYr function 1 = Global::weekOfYear method
```

## <a name="year"></a><span data-ttu-id="5e360-319">年</span><span class="sxs-lookup"><span data-stu-id="5e360-319">year</span></span>
<span data-ttu-id="5e360-320">**date** 値から年を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e360-320">Retrieves the year from a **date** value.</span></span>

```xpp
int year(date _date)
```

### <a name="parameters"></a><span data-ttu-id="5e360-321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-321">Parameters</span></span>

| <span data-ttu-id="5e360-322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e360-322">Parameter</span></span> | <span data-ttu-id="5e360-323">説明</span><span class="sxs-lookup"><span data-stu-id="5e360-323">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="5e360-324">\_ 日付</span><span class="sxs-lookup"><span data-stu-id="5e360-324">\_date</span></span>    | <span data-ttu-id="5e360-325">年を返す日付。</span><span class="sxs-lookup"><span data-stu-id="5e360-325">The date to return the year from.</span></span> |

### <a name="return-value"></a><span data-ttu-id="5e360-326">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e360-326">Return value</span></span>

<span data-ttu-id="5e360-327">指定した日付の年。</span><span class="sxs-lookup"><span data-stu-id="5e360-327">The year of the specified date.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e360-328">備考</span><span class="sxs-lookup"><span data-stu-id="5e360-328">Remarks</span></span>

```xpp
year(0221998); //Returns the value 1998.
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]