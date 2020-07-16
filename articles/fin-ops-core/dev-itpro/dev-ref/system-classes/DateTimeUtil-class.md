---
title: DateTimeUtil クラス
description: このトピックでは、DateTimeUtil クラスについて説明します。
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
ms.openlocfilehash: 68dd7eae7879571e6d42c119ee08943b229b8793
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502730"
---
# <a name="class-datetimeutil"></a><span data-ttu-id="0c8b4-103">クラス DateTimeUtil</span><span class="sxs-lookup"><span data-stu-id="0c8b4-103">Class DateTimeUtil</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DateTimeUtil extends Object
```

<span data-ttu-id="0c8b4-104">DateTimeUtil クラスは、utcdatetime および Timezone 値を変換または変更するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-104">The DateTimeUtil class can be used to convert or modify utcdatetime and Timezone values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c8b4-105">備考</span><span class="sxs-lookup"><span data-stu-id="0c8b4-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="0c8b4-106">例</span><span class="sxs-lookup"><span data-stu-id="0c8b4-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0c8b4-107">方法</span><span class="sxs-lookup"><span data-stu-id="0c8b4-107">Methods</span></span>

| <span data-ttu-id="0c8b4-108">方法</span><span class="sxs-lookup"><span data-stu-id="0c8b4-108">Method</span></span>                                                                                                                                                                            | <span data-ttu-id="0c8b4-109">説明</span><span class="sxs-lookup"><span data-stu-id="0c8b4-109">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8b4-110">::public static DateTime addDays(DateTime t, int value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-110">::public static DateTime addDays(DateTime t, int value)</span></span>                                                                                                                           | <span data-ttu-id="0c8b4-111">utcdatetime 値に指定された日数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-111">Adds the specified number of days to a utcdatetime value.</span></span>                                                                                                      |
| <span data-ttu-id="0c8b4-112">::public static DateTime addHours(DateTime t, int value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-112">::public static DateTime addHours(DateTime t, int value)</span></span>                                                                                                                          | <span data-ttu-id="0c8b4-113">utcdatetime 値に指定された時間数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-113">Adds the specified number of hours to a utcdatetime value.</span></span>                                                                                                     |
| <span data-ttu-id="0c8b4-114">::public static DateTime addMinutes(DateTime t, int value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-114">::public static DateTime addMinutes(DateTime t, int value)</span></span>                                                                                                                        | <span data-ttu-id="0c8b4-115">utcdatetime 値に指定された分数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-115">Adds the specified number of minutes to a utcdatetime value.</span></span>                                                                                                   |
| <span data-ttu-id="0c8b4-116">::public static DateTime addMonths(DateTime t, int value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-116">::public static DateTime addMonths(DateTime t, int value)</span></span>                                                                                                                         | <span data-ttu-id="0c8b4-117">utcdatetime 値に指定された月数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-117">Adds the specified number of months to a utcdatetime value.</span></span>                                                                                                    |
| <span data-ttu-id="0c8b4-118">::public static DateTime addSeconds(DateTime t, Int64 value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-118">::public static DateTime addSeconds(DateTime t, Int64 value)</span></span>                                                                                                                      | <span data-ttu-id="0c8b4-119">utcdatetime 値に指定された秒数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-119">Adds the specified number of seconds to a utcdatetime value.</span></span>                                                                                                   |
| <span data-ttu-id="0c8b4-120">::public static DateTime addYears(DateTime t, int value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-120">::public static DateTime addYears(DateTime t, int value)</span></span>                                                                                                                          | <span data-ttu-id="0c8b4-121">utcdatetime 値に指定された年数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-121">Adds the specified number of years to a utcdatetime value.</span></span>                                                                                                     |
| <span data-ttu-id="0c8b4-122">::public static DateTime anyToDateTime(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-122">::public static DateTime anyToDateTime(AnyType value)</span></span>                                                                                                                             | <span data-ttu-id="0c8b4-123">任意のオブジェクトを utcdatetime 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-123">Converts an anytype object to a utcdatetime value.</span></span>                                                                                                             |
| <span data-ttu-id="0c8b4-124">::public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-124">::public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)</span></span>                                                                                                             | <span data-ttu-id="0c8b4-125">指定された utcdatetime 値から、指定された Timezone 列挙値により示された量オフセットされる utcdatetime 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-125">Retrieves a utcdatetime value that is offset from the specified utcdatetime value by the amount that is indicated by the specified Timezone enumeration value.</span></span> |
| <span data-ttu-id="0c8b4-126">::public static str applyTimeZoneOffsetFilter(QueryFilter filter)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-126">::public static str applyTimeZoneOffsetFilter(QueryFilter filter)</span></span>                                                                                                                 | <span data-ttu-id="0c8b4-127">フィルターにタイム ゾーン オフセットを適用します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-127">Applies the time zone offset to the filter.</span></span>                                                                                                                    |
| <span data-ttu-id="0c8b4-128">::public static str applyTimeZoneOffsetRange(QueryBuildRange range)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-128">::public static str applyTimeZoneOffsetRange(QueryBuildRange range)</span></span>                                                                                                               | <span data-ttu-id="0c8b4-129">範囲にタイム ゾーン オフセットを適用します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-129">Applies the time zone offset to the range.</span></span>                                                                                                                     |
| <span data-ttu-id="0c8b4-130">::public static Date date(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-130">::public static Date date(DateTime t)</span></span>                                                                                                                                             | <span data-ttu-id="0c8b4-131">指定された utcdatetime 値をデータ タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-131">Converts the specified utcdatetime value to a date type.</span></span>                                                                                                       |
| <span data-ttu-id="0c8b4-132">::public static int day(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-132">::public static int day(DateTime t)</span></span>                                                                                                                                               | <span data-ttu-id="0c8b4-133">utcdatetime 値によって指定されている月の日を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-133">Retrieves the day of the month that is specified by a utcdatetime value.</span></span>                                                                                       |
| <span data-ttu-id="0c8b4-134">::public static Timezone getClientMachineTimeZone()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-134">::public static Timezone getClientMachineTimeZone()</span></span>                                                                                                                               | <span data-ttu-id="0c8b4-135">クライアント コンピューターのタイム ゾーン列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-135">Gets the Timezone enumeration value on the client computer.</span></span>                                                                                                    |
| <span data-ttu-id="0c8b4-136">::public static Timezone getCompanyTimeZone()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-136">::public static Timezone getCompanyTimeZone()</span></span>                                                                                                                                     | <span data-ttu-id="0c8b4-137">現在の法人に設定されているタイム ゾーンを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-137">Gets the Timezone value that is set for the current legal entity.</span></span>                                                                                              |
| <span data-ttu-id="0c8b4-138">::public static Int64 getDifference(DateTime t1, DateTime t2)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-138">::public static Int64 getDifference(DateTime t1, DateTime t2)</span></span>                                                                                                                     | <span data-ttu-id="0c8b4-139">2 つの指定された utcdatetime 値間の秒数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-139">Gets the number of seconds between two specified utcdatetime values.</span></span>                                                                                           |
| <span data-ttu-id="0c8b4-140">::public static Timezone getOriginatingTimeZone(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-140">::public static Timezone getOriginatingTimeZone(DateTime t)</span></span>                                                                                                                       | <span data-ttu-id="0c8b4-141">指定した utcdatetime 値の元のタイム ゾーン列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-141">Gets the originating Timezone enumeration value of the specified utcdatetime value.</span></span>                                                                            |
| <span data-ttu-id="0c8b4-142">::public static Date getSystemDate(Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-142">::public static Date getSystemDate(Timezone tz)</span></span>                                                                                                                                   |                                                                                                                                                                |
| <span data-ttu-id="0c8b4-143">::public static DateTime getSystemDateTime()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-143">::public static DateTime getSystemDateTime()</span></span>                                                                                                                                      | <span data-ttu-id="0c8b4-144">utcdatetime 値としての現在のシステム時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-144">Gets the current system time as a utcdatetime value.</span></span>                                                                                                           |
| <span data-ttu-id="0c8b4-145">::public static TimeOfDay getTimeNow(Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-145">::public static TimeOfDay getTimeNow(Timezone tz)</span></span>                                                                                                                                 |                                                                                                                                                                |
| <span data-ttu-id="0c8b4-146">::public static TimeZoneId getTimeZoneId(Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-146">::public static TimeZoneId getTimeZoneId(Timezone tz)</span></span>                                                                                                                             |                                                                                                                                                                |
| <span data-ttu-id="0c8b4-147">::public static int getTimeZoneOffset(DateTime t, Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-147">::public static int getTimeZoneOffset(DateTime t, Timezone tz)</span></span>                                                                                                                    | <span data-ttu-id="0c8b4-148">タイム ゾーン列挙値の情報を使用して UTC に指定された utcdatetime 値のオフセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-148">Gets the offset of the specified utcdatetime value to UTC by using the information in a Timezone enumeration value.</span></span>                                            |
| <span data-ttu-id="0c8b4-149">::public static int getTimeZoneRule(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-149">::public static int getTimeZoneRule(DateTime t)</span></span>                                                                                                                                   | <span data-ttu-id="0c8b4-150">指定した日に影響を与えるタイム ゾーン ルールを返します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-150">Returns the time zone rule that takes effect on the given date.</span></span>                                                                                                |
| <span data-ttu-id="0c8b4-151">::public static Date getToday(Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-151">::public static Date getToday(Timezone tz)</span></span>                                                                                                                                        |                                                                                                                                                                |
| <span data-ttu-id="0c8b4-152">::public static PreferredCalendar getUserPreferredCalendar()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-152">::public static PreferredCalendar getUserPreferredCalendar()</span></span>                                                                                                                      | <span data-ttu-id="0c8b4-153">現在のユーザーの PreferredCalendar 列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-153">Gets the PreferredCalendar enumeration value for the current user.</span></span>                                                                                             |
| <span data-ttu-id="0c8b4-154">::public static Timezone getUserPreferredTimeZone()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-154">::public static Timezone getUserPreferredTimeZone()</span></span>                                                                                                                               | <span data-ttu-id="0c8b4-155">現在のユーザーの PreferredTimezone 列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-155">Gets the PreferredTimezone enumeration value for the current user.</span></span>                                                                                             |
| <span data-ttu-id="0c8b4-156">::public static int hour(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-156">::public static int hour(DateTime t)</span></span>                                                                                                                                              | <span data-ttu-id="0c8b4-157">utcdatetime 値によって指定されている日の時間を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-157">Retrieves the hour of the day that is specified by a utcdatetime value.</span></span>                                                                                        |
| <span data-ttu-id="0c8b4-158">::public static DateTime maxValue()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-158">::public static DateTime maxValue()</span></span>                                                                                                                                               | <span data-ttu-id="0c8b4-159">utcdatetime タイプの変数に許可される最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-159">Retrieves the maximum value that is allowed for a variable of the utcdatetime type.</span></span>                                                                            |
| <span data-ttu-id="0c8b4-160">::public static int minute(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-160">::public static int minute(DateTime t)</span></span>                                                                                                                                            | <span data-ttu-id="0c8b4-161">utcdatetime 値によって指定されている時間の分を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-161">Retrieves the minute in the hour that is specified by a utcdatetime value.</span></span>                                                                                     |
| <span data-ttu-id="0c8b4-162">::public static DateTime minValue()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-162">::public static DateTime minValue()</span></span>                                                                                                                                               | <span data-ttu-id="0c8b4-163">utcdatetime タイプの変数に許可される最小値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-163">Retrieves the minimum value that is allowed for a variable of the utcdatetime type.</span></span>                                                                            |
| <span data-ttu-id="0c8b4-164">::public static int month(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-164">::public static int month(DateTime t)</span></span>                                                                                                                                             | <span data-ttu-id="0c8b4-165">utcdatetime 値によって指定されている年の月を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-165">Retrieves the month in the year that is specified by a utcdatetime value.</span></span>                                                                                      |
| <span data-ttu-id="0c8b4-166">::public static DateTime newDateTime(Date date, TimeOfDay time, \[Timezone tzOffsetToRemove\])</span><span class="sxs-lookup"><span data-stu-id="0c8b4-166">::public static DateTime newDateTime(Date date, TimeOfDay time, \[Timezone tzOffsetToRemove\])</span></span>                                                                                    | <span data-ttu-id="0c8b4-167">指定されたデータおよび timeOfDay 値を使用して、新しい utcdatetime 値を作成します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-167">Creates a new utcdatetime value by using the specified date and timeOfDay values.</span></span>                                                                              |
| <span data-ttu-id="0c8b4-168">::public static DateTime parse(str s)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-168">::public static DateTime parse(str s)</span></span>                                                                                                                                             | <span data-ttu-id="0c8b4-169">指定された文字列から新しい utcdatetime 値を作成します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-169">Creates a new utcdatetime value from the specified string.</span></span>                                                                                                     |
| <span data-ttu-id="0c8b4-170">::public static container populateTimeZoneInfo(int year, Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-170">::public static container populateTimeZoneInfo(int year, Timezone tz)</span></span>                                                                                                             | <span data-ttu-id="0c8b4-171">開始日と終了日と時間バイアスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-171">Retrieves start and end dates and time bias.</span></span>                                                                                                                   |
| <span data-ttu-id="0c8b4-172">::public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-172">::public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)</span></span>                                                                                                            | <span data-ttu-id="0c8b4-173">指定した utcdatetime 値からタイムゾーンの列挙値によって示されるオフセットを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-173">Removes the offset that is indicated by a Timezone enumeration value from the specified utcdatetime value.</span></span>                                                     |
| <span data-ttu-id="0c8b4-174">::public static str removeTimeZoneOffsetFilter(QueryFilter filter)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-174">::public static str removeTimeZoneOffsetFilter(QueryFilter filter)</span></span>                                                                                                                | <span data-ttu-id="0c8b4-175">フィルターからタイム ゾーン オフセットを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-175">Removes the time zone offset from the filter.</span></span>                                                                                                                  |
| <span data-ttu-id="0c8b4-176">::public static str removeTimeZoneOffsetRange(QueryBuildRange range)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-176">::public static str removeTimeZoneOffsetRange(QueryBuildRange range)</span></span>                                                                                                              | <span data-ttu-id="0c8b4-177">範囲からタイム ゾーン オフセットを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-177">Removes the time zone offset from the range.</span></span>                                                                                                                   |
| <span data-ttu-id="0c8b4-178">::public static int second(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-178">::public static int second(DateTime t)</span></span>                                                                                                                                            | <span data-ttu-id="0c8b4-179">utcdatetime 値によって指定されている分の秒を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-179">Retrieves the seconds in a minute that is specified by a utcdatetime value.</span></span>                                                                                    |
| <span data-ttu-id="0c8b4-180">::public static TimeOfDay time(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-180">::public static TimeOfDay time(DateTime t)</span></span>                                                                                                                                        | <span data-ttu-id="0c8b4-181">指定した utcdatetime 値から timeOfDay 値として午前 0 時からの経過秒数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-181">Retrieves the number of seconds that have elapsed since midnight as a timeOfDay value from the specified utcdatetime value.</span></span>                                    |
| <span data-ttu-id="0c8b4-182">::public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="0c8b4-182">::public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, \[int flags\])</span></span> |                                                                                                                                                                |
| <span data-ttu-id="0c8b4-183">::public static str toStr(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-183">::public static str toStr(DateTime t)</span></span>                                                                                                                                             | <span data-ttu-id="0c8b4-184">utcdatetime 値を次の形式の文字列に変換します。YYYY-MM-DDThh:mm:ss。T は文字リテラルです。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-184">Converts a utcdatetime value to a string in the following format: YYYY-MM-DDThh:mm:ss, where T is a character literal.</span></span>                                         |
| <span data-ttu-id="0c8b4-185">::public static DateTime utcNow()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-185">::public static DateTime utcNow()</span></span>                                                                                                                                                 | <span data-ttu-id="0c8b4-186">現在のシステム時刻を示す utcdatetime 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-186">Retrieves a utcdatetime value that indicates the current system time.</span></span>                                                                                          |
| <span data-ttu-id="0c8b4-187">::public static int year(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-187">::public static int year(DateTime t)</span></span>                                                                                                                                              | <span data-ttu-id="0c8b4-188">utcdatetime 値によって指定されている年を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-188">Retrieves the year that is specified by a utcdatetime value.</span></span>                                                                                                   |
| <span data-ttu-id="0c8b4-189">::public static void setSystemDateTime(DateTime t)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-189">::public static void setSystemDateTime(DateTime t)</span></span>                                                                                                                                | <span data-ttu-id="0c8b4-190">指定した utcdatetime 値に、システムの日時を設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-190">Sets the date and time of the system to the specified utcdatetime value.</span></span>                                                                                       |
| <span data-ttu-id="0c8b4-191">::public static void setCompanyTimeZone(Timezone tz, \[boolean persist\])</span><span class="sxs-lookup"><span data-stu-id="0c8b4-191">::public static void setCompanyTimeZone(Timezone tz, \[boolean persist\])</span></span>                                                                                                         | <span data-ttu-id="0c8b4-192">現在の会社によって使用されているタイムゾーン列挙値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-192">Sets the Timezone enumeration value that is used by the current company.</span></span>                                                                                       |
| <span data-ttu-id="0c8b4-193">::public static void setUserPreferredCalendar(PreferredCalendar calendar)</span><span class="sxs-lookup"><span data-stu-id="0c8b4-193">::public static void setUserPreferredCalendar(PreferredCalendar calendar)</span></span>                                                                                                         | <span data-ttu-id="0c8b4-194">現在のセッションの現在のユーザーの PreferredCalendar 列挙型の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-194">Sets the value of the PreferredCalendar enumeration type of the current user for the current session.</span></span>                                                          |
| <span data-ttu-id="0c8b4-195">::public static void setUserPreferredTimeZone(Timezone tz, \[boolean persist\])</span><span class="sxs-lookup"><span data-stu-id="0c8b4-195">::public static void setUserPreferredTimeZone(Timezone tz, \[boolean persist\])</span></span>                                                                                                   | <span data-ttu-id="0c8b4-196">指定したタイムゾーンの列挙値に、ユーザーの優先タイム ゾーンを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-196">Sets the preferred time zone of the user to the specified Timezone enumeration value.</span></span>                                                                          |
| <span data-ttu-id="0c8b4-197">private void new()</span><span class="sxs-lookup"><span data-stu-id="0c8b4-197">private void new()</span></span>                                                                                                                                                                | <span data-ttu-id="0c8b4-198">DateTimeUtil クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-198">Initializes a new instance of the DateTimeUtil class.</span></span>                                                                                                          |

## <a name="method-adddays"></a><span data-ttu-id="0c8b4-199">メソッド addDays</span><span class="sxs-lookup"><span data-stu-id="0c8b4-199">Method addDays</span></span>

<span data-ttu-id="0c8b4-200">utcdatetime 値に指定された日数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-200">Adds the specified number of days to a utcdatetime value.</span></span>

```xpp
public static DateTime addDays(DateTime t, int value)
```

### <a name="parameters---adddays"></a><span data-ttu-id="0c8b4-201">パラメーター - addDays</span><span class="sxs-lookup"><span data-stu-id="0c8b4-201">Parameters - addDays</span></span>

<span data-ttu-id="0c8b4-202">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-202">t</span></span>  
<span data-ttu-id="0c8b4-203">追加する日数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-203">The number of days to add.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-204">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-204">value</span></span>  
<span data-ttu-id="0c8b4-205">追加する日数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-205">The number of days to add.</span></span>

### <a name="return-value---adddays"></a><span data-ttu-id="0c8b4-206">戻り値 - addDays</span><span class="sxs-lookup"><span data-stu-id="0c8b4-206">Return Value - addDays</span></span>

<span data-ttu-id="0c8b4-207">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-207">A new utcdatetime value.</span></span>

### <a name="remarks---adddays"></a><span data-ttu-id="0c8b4-208">備考 - addDays</span><span class="sxs-lookup"><span data-stu-id="0c8b4-208">Remarks - addDays</span></span>

<span data-ttu-id="0c8b4-209">値パラメーターの値が負の場合は、日数が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-209">If the value of the value parameter is negative, days will be subtracted.</span></span>

## <a name="method-addhours"></a><span data-ttu-id="0c8b4-210">メソッド addHours</span><span class="sxs-lookup"><span data-stu-id="0c8b4-210">Method addHours</span></span>

<span data-ttu-id="0c8b4-211">utcdatetime 値に指定された時間数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-211">Adds the specified number of hours to a utcdatetime value.</span></span>

```xpp
public static DateTime addHours(DateTime t, int value)
```

### <a name="parameters---addhours"></a><span data-ttu-id="0c8b4-212">パラメーター - addHours</span><span class="sxs-lookup"><span data-stu-id="0c8b4-212">Parameters - addHours</span></span>

<span data-ttu-id="0c8b4-213">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-213">t</span></span>  
<span data-ttu-id="0c8b4-214">追加する時間数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-214">The number of hours to add.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-215">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-215">value</span></span>  
<span data-ttu-id="0c8b4-216">追加する時間数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-216">The number of hours to add.</span></span>

### <a name="return-value---addhours"></a><span data-ttu-id="0c8b4-217">戻り値 - addHours</span><span class="sxs-lookup"><span data-stu-id="0c8b4-217">Return Value - addHours</span></span>

<span data-ttu-id="0c8b4-218">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-218">A new utcdatetime value.</span></span>

### <a name="remarks---addhours"></a><span data-ttu-id="0c8b4-219">備考 - addHours</span><span class="sxs-lookup"><span data-stu-id="0c8b4-219">Remarks - addHours</span></span>

<span data-ttu-id="0c8b4-220">値パラメーターの値が負の場合は、時間数が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-220">If the value of the value parameter is negative, hours will be subtracted.</span></span>

## <a name="method-addminutes"></a><span data-ttu-id="0c8b4-221">メソッド addMinutes</span><span class="sxs-lookup"><span data-stu-id="0c8b4-221">Method addMinutes</span></span>

<span data-ttu-id="0c8b4-222">utcdatetime 値に指定された分数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-222">Adds the specified number of minutes to a utcdatetime value.</span></span>

```xpp
public static DateTime addMinutes(DateTime t, int value)
```

### <a name="parameters---addminutes"></a><span data-ttu-id="0c8b4-223">パラメーター - addMinutes</span><span class="sxs-lookup"><span data-stu-id="0c8b4-223">Parameters - addMinutes</span></span>

<span data-ttu-id="0c8b4-224">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-224">t</span></span>  
<span data-ttu-id="0c8b4-225">追加する分数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-225">The number of minutes to add.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-226">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-226">value</span></span>  
<span data-ttu-id="0c8b4-227">追加する分数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-227">The number of minutes to add.</span></span>

### <a name="return-value---addminutes"></a><span data-ttu-id="0c8b4-228">戻り値 - addMinutes</span><span class="sxs-lookup"><span data-stu-id="0c8b4-228">Return Value - addMinutes</span></span>

<span data-ttu-id="0c8b4-229">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-229">A new utcdatetime value.</span></span>

### <a name="remarks---addminutes"></a><span data-ttu-id="0c8b4-230">備考 - addMinutes</span><span class="sxs-lookup"><span data-stu-id="0c8b4-230">Remarks - addMinutes</span></span>

<span data-ttu-id="0c8b4-231">値パラメーターの値が負の場合は、分数が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-231">If the value of the value parameter is negative, minutes will be subtracted.</span></span>

## <a name="method-addmonths"></a><span data-ttu-id="0c8b4-232">メソッド addMonths</span><span class="sxs-lookup"><span data-stu-id="0c8b4-232">Method addMonths</span></span>

<span data-ttu-id="0c8b4-233">utcdatetime 値に指定された月数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-233">Adds the specified number of months to a utcdatetime value.</span></span>

```xpp
public static DateTime addMonths(DateTime t, int value)
```

### <a name="parameters---addmonths"></a><span data-ttu-id="0c8b4-234">パラメーター - addMonths</span><span class="sxs-lookup"><span data-stu-id="0c8b4-234">Parameters - addMonths</span></span>

<span data-ttu-id="0c8b4-235">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-235">t</span></span>  
<span data-ttu-id="0c8b4-236">追加する月数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-236">The number of months to add.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-237">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-237">value</span></span>  
<span data-ttu-id="0c8b4-238">追加する月数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-238">The number of months to add.</span></span>

### <a name="return-value---addmonths"></a><span data-ttu-id="0c8b4-239">戻り値 - addMonths</span><span class="sxs-lookup"><span data-stu-id="0c8b4-239">Return Value - addMonths</span></span>

<span data-ttu-id="0c8b4-240">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-240">A new utcdatetime value.</span></span>

### <a name="remarks---addmonths"></a><span data-ttu-id="0c8b4-241">備考 - addMonths</span><span class="sxs-lookup"><span data-stu-id="0c8b4-241">Remarks - addMonths</span></span>

<span data-ttu-id="0c8b4-242">値パラメーターの値が負の場合は、月数が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-242">If the value of the value parameter is negative, months will be subtracted.</span></span>

## <a name="method-addseconds"></a><span data-ttu-id="0c8b4-243">メソッド addSeconds</span><span class="sxs-lookup"><span data-stu-id="0c8b4-243">Method addSeconds</span></span>

<span data-ttu-id="0c8b4-244">utcdatetime 値に指定された秒数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-244">Adds the specified number of seconds to a utcdatetime value.</span></span>

```xpp
public static DateTime addSeconds(DateTime t, Int64 value)
```

### <a name="parameters---addseconds"></a><span data-ttu-id="0c8b4-245">パラメーター - addSeconds</span><span class="sxs-lookup"><span data-stu-id="0c8b4-245">Parameters - addSeconds</span></span>

<span data-ttu-id="0c8b4-246">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-246">t</span></span>  
<span data-ttu-id="0c8b4-247">追加する秒数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-247">The number of seconds to add.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-248">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-248">value</span></span>  
<span data-ttu-id="0c8b4-249">追加する秒数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-249">The number of seconds to add.</span></span>

### <a name="return-value---addseconds"></a><span data-ttu-id="0c8b4-250">戻り値 - addSeconds</span><span class="sxs-lookup"><span data-stu-id="0c8b4-250">Return Value - addSeconds</span></span>

<span data-ttu-id="0c8b4-251">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-251">A new utcdatetime value.</span></span>

### <a name="remarks---addseconds"></a><span data-ttu-id="0c8b4-252">備考 - addSeconds</span><span class="sxs-lookup"><span data-stu-id="0c8b4-252">Remarks - addSeconds</span></span>

<span data-ttu-id="0c8b4-253">値パラメーターの値が負の場合は、秒数が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-253">If the value of the value parameter is negative, seconds will be subtracted.</span></span>

## <a name="method-addyears"></a><span data-ttu-id="0c8b4-254">メソッド addYears</span><span class="sxs-lookup"><span data-stu-id="0c8b4-254">Method addYears</span></span>

<span data-ttu-id="0c8b4-255">utcdatetime 値に指定された年数を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-255">Adds the specified number of years to a utcdatetime value.</span></span>

```xpp
public static DateTime addYears(DateTime t, int value)
```

### <a name="parameters---addyears"></a><span data-ttu-id="0c8b4-256">パラメーター - addYears</span><span class="sxs-lookup"><span data-stu-id="0c8b4-256">Parameters - addYears</span></span>

<span data-ttu-id="0c8b4-257">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-257">t</span></span>  
<span data-ttu-id="0c8b4-258">追加する年数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-258">The number of years to add.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-259">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-259">value</span></span>  
<span data-ttu-id="0c8b4-260">追加する年数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-260">The number of years to add.</span></span>

### <a name="return-value---addyears"></a><span data-ttu-id="0c8b4-261">戻り値 - addYears</span><span class="sxs-lookup"><span data-stu-id="0c8b4-261">Return Value - addYears</span></span>

<span data-ttu-id="0c8b4-262">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-262">A new utcdatetime value.</span></span>

### <a name="remarks---addyears"></a><span data-ttu-id="0c8b4-263">備考 - addYears</span><span class="sxs-lookup"><span data-stu-id="0c8b4-263">Remarks - addYears</span></span>

<span data-ttu-id="0c8b4-264">値パラメーターの値が負の場合は、年数が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-264">If the value of the value parameter is negative, years will be subtracted.</span></span>

## <a name="method-anytodatetime"></a><span data-ttu-id="0c8b4-265">メソッド anyToDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-265">Method anyToDateTime</span></span>

<span data-ttu-id="0c8b4-266">任意のオブジェクトを utcdatetime 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-266">Converts an anytype object to a utcdatetime value.</span></span>

```xpp
public static DateTime anyToDateTime(AnyType value)
```

### <a name="parameters---anytodatetime"></a><span data-ttu-id="0c8b4-267">パラメーター - anyToDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-267">Parameters - anyToDateTime</span></span>

<span data-ttu-id="0c8b4-268">値</span><span class="sxs-lookup"><span data-stu-id="0c8b4-268">value</span></span>  
<span data-ttu-id="0c8b4-269">変換するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-269">The object to convert.</span></span>

### <a name="return-value---anytodatetime"></a><span data-ttu-id="0c8b4-270">戻り値 - anyToDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-270">Return Value - anyToDateTime</span></span>

<span data-ttu-id="0c8b4-271">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-271">A new utcdatetime value.</span></span>

### <a name="remarks---anytodatetime"></a><span data-ttu-id="0c8b4-272">備考 - anyToDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-272">Remarks - anyToDateTime</span></span>

<span data-ttu-id="0c8b4-273">次の例の文字列は、この anyToDateTime メソッドが正しく変換できる日付/時刻文字列の形式を示しています ("2009-01-28T13：44：55")。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-273">The following example string shows the format of a date-time string that this anyToDateTime method can correctly convert: "2009-01-28T13:44:55".</span></span> <span data-ttu-id="0c8b4-274">DateTimeUtil::utcNow メソッドの出力は anyToDateTime メソッドへの有効な入力です。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-274">The output of the DateTimeUtil::utcNow method is valid input into the anyToDateTime method.</span></span>

## <a name="method-applytimezoneoffset"></a><span data-ttu-id="0c8b4-275">メソッド applyTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-275">Method applyTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-276">指定された utcdatetime 値から、指定された Timezone 列挙値により示された量オフセットされる utcdatetime 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-276">Retrieves a utcdatetime value that is offset from the specified utcdatetime value by the amount that is indicated by the specified Timezone enumeration value.</span></span>

```xpp
public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)
```

### <a name="parameters---applytimezoneoffset"></a><span data-ttu-id="0c8b4-277">パラメーター - applyTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-277">Parameters - applyTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-278">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-278">t</span></span>  
<span data-ttu-id="0c8b4-279">使用する新しいオフセットを示すタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-279">A Timezone enumeration value that indicates the new offset to use.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-280">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-280">tz</span></span>  
<span data-ttu-id="0c8b4-281">使用する新しいオフセットを示すタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-281">A Timezone enumeration value that indicates the new offset to use.</span></span>

### <a name="return-value---applytimezoneoffset"></a><span data-ttu-id="0c8b4-282">戻り値 - applyTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-282">Return Value - applyTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-283">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-283">A new utcdatetime value.</span></span>

## <a name="method-applytimezoneoffsetfilter"></a><span data-ttu-id="0c8b4-284">メソッド applyTimeZoneOffsetFilter</span><span class="sxs-lookup"><span data-stu-id="0c8b4-284">Method applyTimeZoneOffsetFilter</span></span>

<span data-ttu-id="0c8b4-285">フィルターにタイム ゾーン オフセットを適用します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-285">Applies the time zone offset to the filter.</span></span>

```xpp
public static str applyTimeZoneOffsetFilter(QueryFilter filter)
```

### <a name="parameters---applytimezoneoffsetfilter"></a><span data-ttu-id="0c8b4-286">パラメーター - applyTimeZoneOffsetFilter</span><span class="sxs-lookup"><span data-stu-id="0c8b4-286">Parameters - applyTimeZoneOffsetFilter</span></span>

<span data-ttu-id="0c8b4-287">フィルター</span><span class="sxs-lookup"><span data-stu-id="0c8b4-287">filter</span></span>  

### <a name="return-value---applytimezoneoffsetfilter"></a><span data-ttu-id="0c8b4-288">戻り値 - applyTimeZoneOffsetFilter</span><span class="sxs-lookup"><span data-stu-id="0c8b4-288">Return Value - applyTimeZoneOffsetFilter</span></span>

<span data-ttu-id="0c8b4-289">新しい日付/時間範囲の値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-289">The new date/time range value.</span></span>

## <a name="method-applytimezoneoffsetrange"></a><span data-ttu-id="0c8b4-290">メソッド applyTimeZoneOffsetRange</span><span class="sxs-lookup"><span data-stu-id="0c8b4-290">Method applyTimeZoneOffsetRange</span></span>

<span data-ttu-id="0c8b4-291">範囲にタイム ゾーン オフセットを適用します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-291">Applies the time zone offset to the range.</span></span>

```xpp
public static str applyTimeZoneOffsetRange(QueryBuildRange range)
```

### <a name="parameters---applytimezoneoffsetrange"></a><span data-ttu-id="0c8b4-292">パラメーター - applyTimeZoneOffsetRange</span><span class="sxs-lookup"><span data-stu-id="0c8b4-292">Parameters - applyTimeZoneOffsetRange</span></span>

<span data-ttu-id="0c8b4-293">範囲</span><span class="sxs-lookup"><span data-stu-id="0c8b4-293">range</span></span>  

### <a name="return-value---applytimezoneoffsetrange"></a><span data-ttu-id="0c8b4-294">戻り値 - applyTimeZoneOffsetRange</span><span class="sxs-lookup"><span data-stu-id="0c8b4-294">Return Value - applyTimeZoneOffsetRange</span></span>

<span data-ttu-id="0c8b4-295">新しい日付/時間範囲の値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-295">The new date/time range value.</span></span>

## <a name="method-date"></a><span data-ttu-id="0c8b4-296">メソッド date</span><span class="sxs-lookup"><span data-stu-id="0c8b4-296">Method date</span></span>

<span data-ttu-id="0c8b4-297">指定された utcdatetime 値をデータ タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-297">Converts the specified utcdatetime value to a date type.</span></span>

```xpp
public static Date date(DateTime t)
```

### <a name="parameters---date"></a><span data-ttu-id="0c8b4-298">パラメーター - date</span><span class="sxs-lookup"><span data-stu-id="0c8b4-298">Parameters - date</span></span>

<span data-ttu-id="0c8b4-299">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-299">t</span></span>  
<span data-ttu-id="0c8b4-300">変換する utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-300">The utcdatetime value to convert.</span></span>

### <a name="return-value---date"></a><span data-ttu-id="0c8b4-301">戻り値 - date</span><span class="sxs-lookup"><span data-stu-id="0c8b4-301">Return Value - date</span></span>

<span data-ttu-id="0c8b4-302">日付の値です。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-302">A date value.</span></span>

## <a name="method-day"></a><span data-ttu-id="0c8b4-303">メソッド day</span><span class="sxs-lookup"><span data-stu-id="0c8b4-303">Method day</span></span>

<span data-ttu-id="0c8b4-304">utcdatetime 値によって指定されている月の日を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-304">Retrieves the day of the month that is specified by a utcdatetime value.</span></span>

```xpp
public static int day(DateTime t)
```

### <a name="parameters---day"></a><span data-ttu-id="0c8b4-305">パラメーター - day</span><span class="sxs-lookup"><span data-stu-id="0c8b4-305">Parameters - day</span></span>

<span data-ttu-id="0c8b4-306">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-306">t</span></span>  
<span data-ttu-id="0c8b4-307">日付のコンポーネントの値を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-307">A utcdatetime value for which to retrieve the value of the day component.</span></span>

### <a name="return-value---day"></a><span data-ttu-id="0c8b4-308">戻り値 - day</span><span class="sxs-lookup"><span data-stu-id="0c8b4-308">Return Value - day</span></span>

<span data-ttu-id="0c8b4-309">指定した utcdatetime 値の月の日。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-309">The day of the month of the specified utcdatetime value.</span></span>

## <a name="method-getclientmachinetimezone"></a><span data-ttu-id="0c8b4-310">メソッド getClientMachineTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-310">Method getClientMachineTimeZone</span></span>

<span data-ttu-id="0c8b4-311">クライアント コンピューターのタイム ゾーン列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-311">Gets the Timezone enumeration value on the client computer.</span></span>

```xpp
public static Timezone getClientMachineTimeZone()
```

### <a name="return-value---getclientmachinetimezone"></a><span data-ttu-id="0c8b4-312">戻り値 - getClientMachineTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-312">Return Value - getClientMachineTimeZone</span></span>

<span data-ttu-id="0c8b4-313">クライアント コンピューターのタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-313">The Timezone enumeration value on the client computer.</span></span>

## <a name="method-getcompanytimezone"></a><span data-ttu-id="0c8b4-314">メソッド getCompanyTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-314">Method getCompanyTimeZone</span></span>

<span data-ttu-id="0c8b4-315">現在の法人に設定されているタイム ゾーンを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-315">Gets the Timezone value that is set for the current legal entity.</span></span>

```xpp
public static Timezone getCompanyTimeZone()
```

### <a name="return-value---getcompanytimezone"></a><span data-ttu-id="0c8b4-316">戻り値 - getCompanyTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-316">Return Value - getCompanyTimeZone</span></span>

<span data-ttu-id="0c8b4-317">現在の法人に設定されているタイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="0c8b4-317">The Timezone value that is set for the current legal entity.</span></span>

## <a name="method-getdifference"></a><span data-ttu-id="0c8b4-318">メソッド getDifference</span><span class="sxs-lookup"><span data-stu-id="0c8b4-318">Method getDifference</span></span>

<span data-ttu-id="0c8b4-319">2 つの指定された utcdatetime 値間の秒数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-319">Gets the number of seconds between two specified utcdatetime values.</span></span>

```xpp
public static Int64 getDifference(DateTime t1, DateTime t2)
```

### <a name="parameters---getdifference"></a><span data-ttu-id="0c8b4-320">パラメーター - getDifference</span><span class="sxs-lookup"><span data-stu-id="0c8b4-320">Parameters - getDifference</span></span>

<span data-ttu-id="0c8b4-321">t1</span><span class="sxs-lookup"><span data-stu-id="0c8b4-321">t1</span></span>  
<span data-ttu-id="0c8b4-322">2 番目の utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-322">The second utcdatetime value.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-323">t2</span><span class="sxs-lookup"><span data-stu-id="0c8b4-323">t2</span></span>  
<span data-ttu-id="0c8b4-324">2 番目の utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-324">The second utcdatetime value.</span></span>

### <a name="return-value---getdifference"></a><span data-ttu-id="0c8b4-325">戻り値 - getDifference</span><span class="sxs-lookup"><span data-stu-id="0c8b4-325">Return Value - getDifference</span></span>

<span data-ttu-id="0c8b4-326">2 つの指定された utcdatetime 値間の秒数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-326">The number of seconds between the two specified utcdatetime values.</span></span>

## <a name="method-getoriginatingtimezone"></a><span data-ttu-id="0c8b4-327">メソッド getOriginatingTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-327">Method getOriginatingTimeZone</span></span>

<span data-ttu-id="0c8b4-328">指定した utcdatetime 値の元のタイム ゾーン列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-328">Gets the originating Timezone enumeration value of the specified utcdatetime value.</span></span>

```xpp
public static Timezone getOriginatingTimeZone(DateTime t)
```

### <a name="parameters---getoriginatingtimezone"></a><span data-ttu-id="0c8b4-329">パラメーター - getOriginatingTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-329">Parameters - getOriginatingTimeZone</span></span>

<span data-ttu-id="0c8b4-330">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-330">t</span></span>  
<span data-ttu-id="0c8b4-331">タイム ゾーンを取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-331">The utcdatetime value for which to retrieve the time zone.</span></span>

### <a name="return-value---getoriginatingtimezone"></a><span data-ttu-id="0c8b4-332">戻り値 - getOriginatingTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-332">Return Value - getOriginatingTimeZone</span></span>

<span data-ttu-id="0c8b4-333">指定した utcdatetime 値のタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-333">The Timezone enumeration value of the specified utcdatetime value.</span></span>

## <a name="method-getsystemdate"></a><span data-ttu-id="0c8b4-334">メソッド getSystemDate</span><span class="sxs-lookup"><span data-stu-id="0c8b4-334">Method getSystemDate</span></span>

```xpp
public static Date getSystemDate(Timezone tz)
```

### <a name="parameters---getsystemdate"></a><span data-ttu-id="0c8b4-335">パラメーター - getSystemDate</span><span class="sxs-lookup"><span data-stu-id="0c8b4-335">Parameters - getSystemDate</span></span>

<span data-ttu-id="0c8b4-336">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-336">tz</span></span>  

### <a name="return-value---getsystemdate"></a><span data-ttu-id="0c8b4-337">戻り値 - getSystemDate</span><span class="sxs-lookup"><span data-stu-id="0c8b4-337">Return Value - getSystemDate</span></span>

## <a name="method-getsystemdatetime"></a><span data-ttu-id="0c8b4-338">メソッド getSystemDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-338">Method getSystemDateTime</span></span>

<span data-ttu-id="0c8b4-339">utcdatetime 値としての現在のシステム時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-339">Gets the current system time as a utcdatetime value.</span></span>

```xpp
public static DateTime getSystemDateTime()
```

### <a name="return-value---getsystemdatetime"></a><span data-ttu-id="0c8b4-340">戻り値 - getSystemDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-340">Return Value - getSystemDateTime</span></span>

<span data-ttu-id="0c8b4-341">utcdatetime 値としての現在のシステム時刻。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-341">The current system time as a utcdatetime value.</span></span>

### <a name="remarks---getsystemdatetime"></a><span data-ttu-id="0c8b4-342">備考 - getSystemDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-342">Remarks - getSystemDateTime</span></span>

<span data-ttu-id="0c8b4-343">システム時刻に固定値がない場合は、それが返されます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-343">If the system time has a fixed value, it will be returned.</span></span> <span data-ttu-id="0c8b4-344">それ以外の場合、現在の日付と時刻がローカル コンピューターから返されます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-344">Otherwise, the current date and time from the local computer will be returned.</span></span>

## <a name="method-gettimenow"></a><span data-ttu-id="0c8b4-345">メソッド getTimeNow</span><span class="sxs-lookup"><span data-stu-id="0c8b4-345">Method getTimeNow</span></span>

```xpp
public static TimeOfDay getTimeNow(Timezone tz)
```

### <a name="parameters---gettimenow"></a><span data-ttu-id="0c8b4-346">パラメーター - getTimeNow</span><span class="sxs-lookup"><span data-stu-id="0c8b4-346">Parameters - getTimeNow</span></span>

<span data-ttu-id="0c8b4-347">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-347">tz</span></span>  

### <a name="return-value---gettimenow"></a><span data-ttu-id="0c8b4-348">戻り値 - getTimeNow</span><span class="sxs-lookup"><span data-stu-id="0c8b4-348">Return Value - getTimeNow</span></span>

## <a name="method-gettimezoneid"></a><span data-ttu-id="0c8b4-349">メソッド getTimeZoneId</span><span class="sxs-lookup"><span data-stu-id="0c8b4-349">Method getTimeZoneId</span></span>

```xpp
public static TimeZoneId getTimeZoneId(Timezone tz)
```

### <a name="parameters---gettimezoneid"></a><span data-ttu-id="0c8b4-350">パラメーター - getTimeZoneId</span><span class="sxs-lookup"><span data-stu-id="0c8b4-350">Parameters - getTimeZoneId</span></span>

<span data-ttu-id="0c8b4-351">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-351">tz</span></span>  

### <a name="return-value---gettimezoneid"></a><span data-ttu-id="0c8b4-352">戻り値 - getTimeZoneId</span><span class="sxs-lookup"><span data-stu-id="0c8b4-352">Return Value - getTimeZoneId</span></span>

## <a name="method-gettimezoneoffset"></a><span data-ttu-id="0c8b4-353">メソッド getTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-353">Method getTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-354">タイム ゾーン列挙値の情報を使用して UTC に指定された utcdatetime 値のオフセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-354">Gets the offset of the specified utcdatetime value to UTC by using the information in a Timezone enumeration value.</span></span>

```xpp
public static int getTimeZoneOffset(DateTime t, Timezone tz)
```

### <a name="parameters---gettimezoneoffset"></a><span data-ttu-id="0c8b4-355">パラメーター - getTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-355">Parameters - getTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-356">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-356">t</span></span>  
<span data-ttu-id="0c8b4-357">T パラメーターのタイム ゾーンを示すタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-357">A Timezone enumeration value that indicates the time zone of the t parameter.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-358">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-358">tz</span></span>  
<span data-ttu-id="0c8b4-359">T パラメーターのタイム ゾーンを示すタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-359">A Timezone enumeration value that indicates the time zone of the t parameter.</span></span>

### <a name="return-value---gettimezoneoffset"></a><span data-ttu-id="0c8b4-360">戻り値 - getTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-360">Return Value - getTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-361">UTC に指定された utcdatetime 値のオフセットを示す整数。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-361">An integer that indicates the offset of the specified utcdatetime value to UTC.</span></span>

## <a name="method-gettimezonerule"></a><span data-ttu-id="0c8b4-362">メソッド getTimeZoneRule</span><span class="sxs-lookup"><span data-stu-id="0c8b4-362">Method getTimeZoneRule</span></span>

<span data-ttu-id="0c8b4-363">指定した日に影響を与えるタイム ゾーン ルールを返します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-363">Returns the time zone rule that takes effect on the given date.</span></span>

```xpp
public static int getTimeZoneRule(DateTime t)
```

### <a name="parameters---gettimezonerule"></a><span data-ttu-id="0c8b4-364">パラメーター - getTimeZoneRule</span><span class="sxs-lookup"><span data-stu-id="0c8b4-364">Parameters - getTimeZoneRule</span></span>

<span data-ttu-id="0c8b4-365">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-365">t</span></span>  

### <a name="return-value---gettimezonerule"></a><span data-ttu-id="0c8b4-366">戻り値 - getTimeZoneRule</span><span class="sxs-lookup"><span data-stu-id="0c8b4-366">Return Value - getTimeZoneRule</span></span>

<span data-ttu-id="0c8b4-367">指定された日付のタイム ゾーン ルール。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-367">The time zone rule for the given date.</span></span>

## <a name="method-gettoday"></a><span data-ttu-id="0c8b4-368">メソッド getToday</span><span class="sxs-lookup"><span data-stu-id="0c8b4-368">Method getToday</span></span>

```xpp
public static Date getToday(Timezone tz)
```

### <a name="parameters---gettoday"></a><span data-ttu-id="0c8b4-369">パラメーター - getToday</span><span class="sxs-lookup"><span data-stu-id="0c8b4-369">Parameters - getToday</span></span>

<span data-ttu-id="0c8b4-370">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-370">tz</span></span>  

### <a name="return-value---gettoday"></a><span data-ttu-id="0c8b4-371">戻り値 - getToday</span><span class="sxs-lookup"><span data-stu-id="0c8b4-371">Return Value - getToday</span></span>

## <a name="method-getuserpreferredcalendar"></a><span data-ttu-id="0c8b4-372">メソッド getUserPreferredCalendar</span><span class="sxs-lookup"><span data-stu-id="0c8b4-372">Method getUserPreferredCalendar</span></span>

<span data-ttu-id="0c8b4-373">現在のユーザーの PreferredCalendar 列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-373">Gets the PreferredCalendar enumeration value for the current user.</span></span>

```xpp
public static PreferredCalendar getUserPreferredCalendar()
```

### <a name="return-value---getuserpreferredcalendar"></a><span data-ttu-id="0c8b4-374">戻り値 - getUserPreferredCalendar</span><span class="sxs-lookup"><span data-stu-id="0c8b4-374">Return Value - getUserPreferredCalendar</span></span>

<span data-ttu-id="0c8b4-375">現在のユーザーの PreferredCalendar 列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-375">The PreferredCalendar enumeration value for the current user.</span></span>

## <a name="method-getuserpreferredtimezone"></a><span data-ttu-id="0c8b4-376">メソッド getUserPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-376">Method getUserPreferredTimeZone</span></span>

<span data-ttu-id="0c8b4-377">現在のユーザーの PreferredTimezone 列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-377">Gets the PreferredTimezone enumeration value for the current user.</span></span>

```xpp
public static Timezone getUserPreferredTimeZone()
```

### <a name="return-value---getuserpreferredtimezone"></a><span data-ttu-id="0c8b4-378">戻り値 - getUserPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-378">Return Value - getUserPreferredTimeZone</span></span>

<span data-ttu-id="0c8b4-379">現在のユーザーの PreferredTimezone 列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-379">The PreferredTimezone enumeration value for the current user.</span></span>

## <a name="method-hour"></a><span data-ttu-id="0c8b4-380">メソッド hour</span><span class="sxs-lookup"><span data-stu-id="0c8b4-380">Method hour</span></span>

<span data-ttu-id="0c8b4-381">utcdatetime 値によって指定されている日の時間を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-381">Retrieves the hour of the day that is specified by a utcdatetime value.</span></span>

```xpp
public static int hour(DateTime t)
```

### <a name="parameters---hour"></a><span data-ttu-id="0c8b4-382">パラメーター - hour</span><span class="sxs-lookup"><span data-stu-id="0c8b4-382">Parameters - hour</span></span>

<span data-ttu-id="0c8b4-383">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-383">t</span></span>  
<span data-ttu-id="0c8b4-384">時間のコンポーネントの値を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-384">A utcdatetime value for which to retrieve the value of the hour component.</span></span>

### <a name="return-value---hour"></a><span data-ttu-id="0c8b4-385">戻り値 - hour</span><span class="sxs-lookup"><span data-stu-id="0c8b4-385">Return Value - hour</span></span>

<span data-ttu-id="0c8b4-386">指定した utcdatetime 値の日の時間。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-386">The hour in the day of the specified utcdatetime value.</span></span>

## <a name="method-maxvalue"></a><span data-ttu-id="0c8b4-387">メソッド maxValue</span><span class="sxs-lookup"><span data-stu-id="0c8b4-387">Method maxValue</span></span>

<span data-ttu-id="0c8b4-388">utcdatetime タイプの変数に許可される最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-388">Retrieves the maximum value that is allowed for a variable of the utcdatetime type.</span></span>

```xpp
public static DateTime maxValue()
```

### <a name="return-value---maxvalue"></a><span data-ttu-id="0c8b4-389">戻り値 - maxValue</span><span class="sxs-lookup"><span data-stu-id="0c8b4-389">Return Value - maxValue</span></span>

<span data-ttu-id="0c8b4-390">utcdatetime タイプの変数に許可される最大値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-390">The maximum value that is allowed for a variable of the utcdatetime type.</span></span>

## <a name="method-minute"></a><span data-ttu-id="0c8b4-391">メソッド minute</span><span class="sxs-lookup"><span data-stu-id="0c8b4-391">Method minute</span></span>

<span data-ttu-id="0c8b4-392">utcdatetime 値によって指定されている時間の分を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-392">Retrieves the minute in the hour that is specified by a utcdatetime value.</span></span>

```xpp
public static int minute(DateTime t)
```

### <a name="parameters---minute"></a><span data-ttu-id="0c8b4-393">パラメーター - minute</span><span class="sxs-lookup"><span data-stu-id="0c8b4-393">Parameters - minute</span></span>

<span data-ttu-id="0c8b4-394">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-394">t</span></span>  
<span data-ttu-id="0c8b4-395">分のコンポーネントの値を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-395">A utcdatetime value for which to retrieve the value of the minute component.</span></span>

### <a name="return-value---minute"></a><span data-ttu-id="0c8b4-396">戻り値 - minute</span><span class="sxs-lookup"><span data-stu-id="0c8b4-396">Return Value - minute</span></span>

<span data-ttu-id="0c8b4-397">指定した utcdatetime 値の時間の分。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-397">The minute in the hour of the specified utcdatetime value.</span></span>

## <a name="method-minvalue"></a><span data-ttu-id="0c8b4-398">メソッド minValue</span><span class="sxs-lookup"><span data-stu-id="0c8b4-398">Method minValue</span></span>

<span data-ttu-id="0c8b4-399">utcdatetime タイプの変数に許可される最小値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-399">Retrieves the minimum value that is allowed for a variable of the utcdatetime type.</span></span>

```xpp
public static DateTime minValue()
```

### <a name="return-value---minvalue"></a><span data-ttu-id="0c8b4-400">戻り値 - minValue</span><span class="sxs-lookup"><span data-stu-id="0c8b4-400">Return Value - minValue</span></span>

<span data-ttu-id="0c8b4-401">utcdatetime タイプの変数に許可される最小値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-401">The minimum value that is allowed for a variable of the utcdatetime type.</span></span>

## <a name="method-month"></a><span data-ttu-id="0c8b4-402">メソッド month</span><span class="sxs-lookup"><span data-stu-id="0c8b4-402">Method month</span></span>

<span data-ttu-id="0c8b4-403">utcdatetime 値によって指定されている年の月を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-403">Retrieves the month in the year that is specified by a utcdatetime value.</span></span>

```xpp
public static int month(DateTime t)
```

### <a name="parameters---month"></a><span data-ttu-id="0c8b4-404">パラメーター - month</span><span class="sxs-lookup"><span data-stu-id="0c8b4-404">Parameters - month</span></span>

<span data-ttu-id="0c8b4-405">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-405">t</span></span>  
<span data-ttu-id="0c8b4-406">月のコンポーネントの値を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-406">A utcdatetime value for which to retrieve the value of the month component.</span></span>

### <a name="return-value---month"></a><span data-ttu-id="0c8b4-407">戻り値 - month</span><span class="sxs-lookup"><span data-stu-id="0c8b4-407">Return Value - month</span></span>

<span data-ttu-id="0c8b4-408">指定された utcdatetime 値の年の月。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-408">The month in the year of the specified utcdatetime value.</span></span>

## <a name="method-newdatetime"></a><span data-ttu-id="0c8b4-409">メソッド newDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-409">Method newDateTime</span></span>

<span data-ttu-id="0c8b4-410">指定されたデータおよび timeOfDay 値を使用して、新しい utcdatetime 値を作成します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-410">Creates a new utcdatetime value by using the specified date and timeOfDay values.</span></span>

```xpp
public static DateTime newDateTime(Date date, TimeOfDay time, [Timezone tzOffsetToRemove])
```

### <a name="parameters---newdatetime"></a><span data-ttu-id="0c8b4-411">パラメーター - newDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-411">Parameters - newDateTime</span></span>

<span data-ttu-id="0c8b4-412">日付</span><span class="sxs-lookup"><span data-stu-id="0c8b4-412">date</span></span>  
<span data-ttu-id="0c8b4-413">新しい utcdatetime 値を作成するタイム ゾーン (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-413">The time zone in which to create the new utcdatetime value; optional.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-414">タイム</span><span class="sxs-lookup"><span data-stu-id="0c8b4-414">time</span></span>  
<span data-ttu-id="0c8b4-415">新しい utcdatetime 値を作成するタイム ゾーン (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-415">The time zone in which to create the new utcdatetime value; optional.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-416">tzOffsetToRemove</span><span class="sxs-lookup"><span data-stu-id="0c8b4-416">tzOffsetToRemove</span></span>  
<span data-ttu-id="0c8b4-417">新しい utcdatetime 値を作成するタイム ゾーン (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-417">The time zone in which to create the new utcdatetime value; optional.</span></span>

### <a name="return-value---newdatetime"></a><span data-ttu-id="0c8b4-418">戻り値 - newDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-418">Return Value - newDateTime</span></span>

<span data-ttu-id="0c8b4-419">新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-419">A new utcdatetime value.</span></span>

### <a name="remarks---newdatetime"></a><span data-ttu-id="0c8b4-420">備考 - newDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-420">Remarks - newDateTime</span></span>

<span data-ttu-id="0c8b4-421">TzOffsetToRemove パラメーターの値が指定されていない場合は、UTC タイム ゾーンで utcdatetime 値が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-421">If no value is specified for the tzOffsetToRemove parameter, the utcdatetime value will be created in the UTC time zone.</span></span>

## <a name="method-parse"></a><span data-ttu-id="0c8b4-422">メソッド parse</span><span class="sxs-lookup"><span data-stu-id="0c8b4-422">Method parse</span></span>

<span data-ttu-id="0c8b4-423">指定された文字列から新しい utcdatetime 値を作成します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-423">Creates a new utcdatetime value from the specified string.</span></span>

```xpp
public static DateTime parse(str s)
```

### <a name="parameters---parse"></a><span data-ttu-id="0c8b4-424">パラメーター - parse</span><span class="sxs-lookup"><span data-stu-id="0c8b4-424">Parameters - parse</span></span>

<span data-ttu-id="0c8b4-425">秒</span><span class="sxs-lookup"><span data-stu-id="0c8b4-425">s</span></span>  
<span data-ttu-id="0c8b4-426">次の形式の文字列: yyyy-mm-ddThh:mm:ss。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-426">A string in the following format: yyyy-mm-ddThh:mm:ss.</span></span>

### <a name="return-value---parse"></a><span data-ttu-id="0c8b4-427">戻り値 - parse</span><span class="sxs-lookup"><span data-stu-id="0c8b4-427">Return Value - parse</span></span>

<span data-ttu-id="0c8b4-428">指定した文字列からの新しい utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-428">A new utcdatetime value from the specified string.</span></span>

## <a name="method-populatetimezoneinfo"></a><span data-ttu-id="0c8b4-429">メソッド populateTimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="0c8b4-429">Method populateTimeZoneInfo</span></span>

<span data-ttu-id="0c8b4-430">開始日と終了日と時間バイアスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-430">Retrieves start and end dates and time bias.</span></span>

```xpp
public static container populateTimeZoneInfo(int year, Timezone tz)
```

### <a name="parameters---populatetimezoneinfo"></a><span data-ttu-id="0c8b4-431">パラメーター - populateTimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="0c8b4-431">Parameters - populateTimeZoneInfo</span></span>

<span data-ttu-id="0c8b4-432">年</span><span class="sxs-lookup"><span data-stu-id="0c8b4-432">year</span></span>  
<span data-ttu-id="0c8b4-433">タイム ゾーン。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-433">The time zone.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-434">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-434">tz</span></span>  
<span data-ttu-id="0c8b4-435">タイム ゾーン。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-435">The time zone.</span></span>

### <a name="return-value---populatetimezoneinfo"></a><span data-ttu-id="0c8b4-436">戻り値 - populateTimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="0c8b4-436">Return Value - populateTimeZoneInfo</span></span>

<span data-ttu-id="0c8b4-437">開始日と終了日と時間バイアス。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-437">The start and end dates and time bias.</span></span>

## <a name="method-removetimezoneoffset"></a><span data-ttu-id="0c8b4-438">メソッド removeTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-438">Method removeTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-439">指定した utcdatetime 値からタイムゾーンの列挙値によって示されるオフセットを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-439">Removes the offset that is indicated by a Timezone enumeration value from the specified utcdatetime value.</span></span>

```xpp
public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)
```

### <a name="parameters---removetimezoneoffset"></a><span data-ttu-id="0c8b4-440">パラメーター - removeTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-440">Parameters - removeTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-441">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-441">t</span></span>  
<span data-ttu-id="0c8b4-442">削除するタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-442">The Timezone enumeration value to remove.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-443">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-443">tz</span></span>  
<span data-ttu-id="0c8b4-444">削除するタイム ゾーン列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-444">The Timezone enumeration value to remove.</span></span>

### <a name="return-value---removetimezoneoffset"></a><span data-ttu-id="0c8b4-445">戻り値 - removeTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0c8b4-445">Return Value - removeTimeZoneOffset</span></span>

<span data-ttu-id="0c8b4-446">タイム ゾーン オフセットなしの utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-446">A utcdatetime value without a time zone offset.</span></span>

## <a name="method-removetimezoneoffsetfilter"></a><span data-ttu-id="0c8b4-447">メソッド removeTimeZoneOffsetFilter</span><span class="sxs-lookup"><span data-stu-id="0c8b4-447">Method removeTimeZoneOffsetFilter</span></span>

<span data-ttu-id="0c8b4-448">フィルターからタイム ゾーン オフセットを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-448">Removes the time zone offset from the filter.</span></span>

```xpp
public static str removeTimeZoneOffsetFilter(QueryFilter filter)
```

### <a name="parameters---removetimezoneoffsetfilter"></a><span data-ttu-id="0c8b4-449">パラメーター - removeTimeZoneOffsetFilter</span><span class="sxs-lookup"><span data-stu-id="0c8b4-449">Parameters - removeTimeZoneOffsetFilter</span></span>

<span data-ttu-id="0c8b4-450">フィルター</span><span class="sxs-lookup"><span data-stu-id="0c8b4-450">filter</span></span>  

### <a name="return-value---removetimezoneoffsetfilter"></a><span data-ttu-id="0c8b4-451">戻り値 - removeTimeZoneOffsetFilter</span><span class="sxs-lookup"><span data-stu-id="0c8b4-451">Return Value - removeTimeZoneOffsetFilter</span></span>

<span data-ttu-id="0c8b4-452">新しい日付/時間範囲の値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-452">The new date/time range value.</span></span>

## <a name="method-removetimezoneoffsetrange"></a><span data-ttu-id="0c8b4-453">メソッド removeTimeZoneOffsetRange</span><span class="sxs-lookup"><span data-stu-id="0c8b4-453">Method removeTimeZoneOffsetRange</span></span>

<span data-ttu-id="0c8b4-454">範囲からタイム ゾーン オフセットを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-454">Removes the time zone offset from the range.</span></span>

```xpp
public static str removeTimeZoneOffsetRange(QueryBuildRange range)
```

### <a name="parameters---removetimezoneoffsetrange"></a><span data-ttu-id="0c8b4-455">パラメーター - removeTimeZoneOffsetRange</span><span class="sxs-lookup"><span data-stu-id="0c8b4-455">Parameters - removeTimeZoneOffsetRange</span></span>

<span data-ttu-id="0c8b4-456">範囲</span><span class="sxs-lookup"><span data-stu-id="0c8b4-456">range</span></span>  

### <a name="return-value---removetimezoneoffsetrange"></a><span data-ttu-id="0c8b4-457">戻り値 - removeTimeZoneOffsetRange</span><span class="sxs-lookup"><span data-stu-id="0c8b4-457">Return Value - removeTimeZoneOffsetRange</span></span>

<span data-ttu-id="0c8b4-458">新しい日付/時間範囲の値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-458">The new date/time range value.</span></span>

## <a name="method-second"></a><span data-ttu-id="0c8b4-459">メソッド second</span><span class="sxs-lookup"><span data-stu-id="0c8b4-459">Method second</span></span>

<span data-ttu-id="0c8b4-460">utcdatetime 値によって指定されている分の秒を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-460">Retrieves the seconds in a minute that is specified by a utcdatetime value.</span></span>

```xpp
public static int second(DateTime t)
```

### <a name="parameters---second"></a><span data-ttu-id="0c8b4-461">パラメーター - second</span><span class="sxs-lookup"><span data-stu-id="0c8b4-461">Parameters - second</span></span>

<span data-ttu-id="0c8b4-462">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-462">t</span></span>  
<span data-ttu-id="0c8b4-463">秒のコンポーネントの値を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-463">A utcdatetime value for which to retrieve the value of the second component.</span></span>

### <a name="return-value---second"></a><span data-ttu-id="0c8b4-464">戻り値 - second</span><span class="sxs-lookup"><span data-stu-id="0c8b4-464">Return Value - second</span></span>

<span data-ttu-id="0c8b4-465">指定された utcdatetime 値の分の秒です。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-465">The second in the minute of the specified utcdatetime value.</span></span>

## <a name="method-time"></a><span data-ttu-id="0c8b4-466">メソッド time</span><span class="sxs-lookup"><span data-stu-id="0c8b4-466">Method time</span></span>

<span data-ttu-id="0c8b4-467">指定した utcdatetime 値から timeOfDay 値として午前 0 時からの経過秒数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-467">Retrieves the number of seconds that have elapsed since midnight as a timeOfDay value from the specified utcdatetime value.</span></span>

```xpp
public static TimeOfDay time(DateTime t)
```

### <a name="parameters---time"></a><span data-ttu-id="0c8b4-468">パラメーター - time</span><span class="sxs-lookup"><span data-stu-id="0c8b4-468">Parameters - time</span></span>

<span data-ttu-id="0c8b4-469">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-469">t</span></span>  
<span data-ttu-id="0c8b4-470">時刻を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-470">A utcdatetime value for which to retrieve the time.</span></span>

### <a name="return-value---time"></a><span data-ttu-id="0c8b4-471">戻り値 - time</span><span class="sxs-lookup"><span data-stu-id="0c8b4-471">Return Value - time</span></span>

<span data-ttu-id="0c8b4-472">午前 0 時から経過した秒数を示す timeOfDay 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-472">A timeOfDay value that indicates the number of seconds that have elapsed since midnight.</span></span>

## <a name="method-toformattedstr"></a><span data-ttu-id="0c8b4-473">メソッド toFormattedStr</span><span class="sxs-lookup"><span data-stu-id="0c8b4-473">Method toFormattedStr</span></span>

```xpp
public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, [int flags])
```

### <a name="parameters---toformattedstr"></a><span data-ttu-id="0c8b4-474">パラメーター - toFormattedStr</span><span class="sxs-lookup"><span data-stu-id="0c8b4-474">Parameters - toFormattedStr</span></span>

<span data-ttu-id="0c8b4-475">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-475">t</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-476">順序</span><span class="sxs-lookup"><span data-stu-id="0c8b4-476">sequence</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-477">曜日</span><span class="sxs-lookup"><span data-stu-id="0c8b4-477">day</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-478">separator1</span><span class="sxs-lookup"><span data-stu-id="0c8b4-478">separator1</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-479">か月</span><span class="sxs-lookup"><span data-stu-id="0c8b4-479">month</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-480">separator2</span><span class="sxs-lookup"><span data-stu-id="0c8b4-480">separator2</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-481">年</span><span class="sxs-lookup"><span data-stu-id="0c8b4-481">year</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-482">timeSeparator1</span><span class="sxs-lookup"><span data-stu-id="0c8b4-482">timeSeparator1</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-483">timeSeparator2</span><span class="sxs-lookup"><span data-stu-id="0c8b4-483">timeSeparator2</span></span>  

<!-- -->

<span data-ttu-id="0c8b4-484">flags</span><span class="sxs-lookup"><span data-stu-id="0c8b4-484">flags</span></span>  

### <a name="return-value---toformattedstr"></a><span data-ttu-id="0c8b4-485">戻り値 - toFormattedStr</span><span class="sxs-lookup"><span data-stu-id="0c8b4-485">Return Value - toFormattedStr</span></span>

## <a name="method-tostr"></a><span data-ttu-id="0c8b4-486">メソッド toStr</span><span class="sxs-lookup"><span data-stu-id="0c8b4-486">Method toStr</span></span>

<span data-ttu-id="0c8b4-487">utcdatetime 値を次の形式の文字列に変換します。YYYY-MM-DDThh:mm:ss。T は文字リテラルです。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-487">Converts a utcdatetime value to a string in the following format: YYYY-MM-DDThh:mm:ss, where T is a character literal.</span></span>

```xpp
public static str toStr(DateTime t)
```

### <a name="parameters---tostr"></a><span data-ttu-id="0c8b4-488">パラメーター - toStr</span><span class="sxs-lookup"><span data-stu-id="0c8b4-488">Parameters - toStr</span></span>

<span data-ttu-id="0c8b4-489">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-489">t</span></span>  
<span data-ttu-id="0c8b4-490">変換する utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-490">The utcdatetime value to convert.</span></span>

### <a name="return-value---tostr"></a><span data-ttu-id="0c8b4-491">戻り値 - toStr</span><span class="sxs-lookup"><span data-stu-id="0c8b4-491">Return Value - toStr</span></span>

<span data-ttu-id="0c8b4-492">指定された utcdatetime 値の文字列表現。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-492">The string representation of the specified utcdatetime value.</span></span>

## <a name="method-utcnow"></a><span data-ttu-id="0c8b4-493">メソッド utcNow</span><span class="sxs-lookup"><span data-stu-id="0c8b4-493">Method utcNow</span></span>

<span data-ttu-id="0c8b4-494">現在のシステム時刻を示す utcdatetime 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-494">Retrieves a utcdatetime value that indicates the current system time.</span></span>

```xpp
public static DateTime utcNow()
```

### <a name="return-value---utcnow"></a><span data-ttu-id="0c8b4-495">戻り値 - utcNow</span><span class="sxs-lookup"><span data-stu-id="0c8b4-495">Return Value - utcNow</span></span>

<span data-ttu-id="0c8b4-496">utcdatetime 値としての現在のシステム時刻。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-496">The current system time as a utcdatetime value.</span></span>

### <a name="remarks---utcnow"></a><span data-ttu-id="0c8b4-497">備考 - utcNow</span><span class="sxs-lookup"><span data-stu-id="0c8b4-497">Remarks - utcNow</span></span>

<span data-ttu-id="0c8b4-498">このメソッドはサーバー上で実行されるため、返される時刻はサーバーのシステム時刻です。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-498">This method is run on the server, so that the time that is returned is the system time of the server.</span></span>

## <a name="method-year"></a><span data-ttu-id="0c8b4-499">メソッド year</span><span class="sxs-lookup"><span data-stu-id="0c8b4-499">Method year</span></span>

<span data-ttu-id="0c8b4-500">utcdatetime 値によって指定されている年を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-500">Retrieves the year that is specified by a utcdatetime value.</span></span>

```xpp
public static int year(DateTime t)
```

### <a name="parameters---year"></a><span data-ttu-id="0c8b4-501">パラメータ - year</span><span class="sxs-lookup"><span data-stu-id="0c8b4-501">Parameters - year</span></span>

<span data-ttu-id="0c8b4-502">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-502">t</span></span>  
<span data-ttu-id="0c8b4-503">年のコンポーネントの値を取得するための utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-503">A utcdatetime value for which to retrieve the value of the year component.</span></span>

### <a name="return-value---year"></a><span data-ttu-id="0c8b4-504">戻り値 - year</span><span class="sxs-lookup"><span data-stu-id="0c8b4-504">Return Value - year</span></span>

<span data-ttu-id="0c8b4-505">指定された utcdatetime 値の年。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-505">The year of the specified utcdatetime value.</span></span>

## <a name="method-setsystemdatetime"></a><span data-ttu-id="0c8b4-506">メソッド setSystemDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-506">Method setSystemDateTime</span></span>

<span data-ttu-id="0c8b4-507">指定した utcdatetime 値に、システムの日時を設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-507">Sets the date and time of the system to the specified utcdatetime value.</span></span>

```xpp
public static void setSystemDateTime(DateTime t)
```

### <a name="parameters---setsystemdatetime"></a><span data-ttu-id="0c8b4-508">パラメーター - setSystemDateTime</span><span class="sxs-lookup"><span data-stu-id="0c8b4-508">Parameters - setSystemDateTime</span></span>

<span data-ttu-id="0c8b4-509">t</span><span class="sxs-lookup"><span data-stu-id="0c8b4-509">t</span></span>  
<span data-ttu-id="0c8b4-510">システム日時を設定する utcdatetime 値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-510">A utcdatetime value to which to set the system date and time.</span></span>

## <a name="method-setcompanytimezone"></a><span data-ttu-id="0c8b4-511">メソッド setCompanyTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-511">Method setCompanyTimeZone</span></span>

<span data-ttu-id="0c8b4-512">現在の会社によって使用されているタイムゾーン列挙値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-512">Sets the Timezone enumeration value that is used by the current company.</span></span>

```xpp
public static void setCompanyTimeZone(Timezone tz, [boolean persist])
```

### <a name="parameters---setcompanytimezone"></a><span data-ttu-id="0c8b4-513">パラメーター - setCompanyTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-513">Parameters - setCompanyTimeZone</span></span>

<span data-ttu-id="0c8b4-514">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-514">tz</span></span>  
<span data-ttu-id="0c8b4-515">新しい値を保持する必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-515">A Boolean value that indicates whether the new value should be persisted.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-516">persist</span><span class="sxs-lookup"><span data-stu-id="0c8b4-516">persist</span></span>  
<span data-ttu-id="0c8b4-517">新しい値を保持する必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-517">A Boolean value that indicates whether the new value should be persisted.</span></span>

## <a name="method-setuserpreferredcalendar"></a><span data-ttu-id="0c8b4-518">メソッド setUserPreferredCalendar</span><span class="sxs-lookup"><span data-stu-id="0c8b4-518">Method setUserPreferredCalendar</span></span>

<span data-ttu-id="0c8b4-519">現在のセッションの現在のユーザーの PreferredCalendar 列挙型の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-519">Sets the value of the PreferredCalendar enumeration type of the current user for the current session.</span></span>

```xpp
public static void setUserPreferredCalendar(PreferredCalendar calendar)
```

### <a name="parameters---setuserpreferredcalendar"></a><span data-ttu-id="0c8b4-520">パラメーター - setUserPreferredCalendar</span><span class="sxs-lookup"><span data-stu-id="0c8b4-520">Parameters - setUserPreferredCalendar</span></span>

<span data-ttu-id="0c8b4-521">カレンダー</span><span class="sxs-lookup"><span data-stu-id="0c8b4-521">calendar</span></span>  
<span data-ttu-id="0c8b4-522">設定する PreferredCalendar 列挙値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-522">The PreferredCalendar enumeration value to set.</span></span>

## <a name="method-setuserpreferredtimezone"></a><span data-ttu-id="0c8b4-523">メソッド setUserPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-523">Method setUserPreferredTimeZone</span></span>

<span data-ttu-id="0c8b4-524">指定したタイムゾーンの列挙値に、ユーザーの優先タイム ゾーンを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-524">Sets the preferred time zone of the user to the specified Timezone enumeration value.</span></span>

```xpp
public static void setUserPreferredTimeZone(Timezone tz, [boolean persist])
```

### <a name="parameters---setuserpreferredtimezone"></a><span data-ttu-id="0c8b4-525">パラメーター - setUserPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="0c8b4-525">Parameters - setUserPreferredTimeZone</span></span>

<span data-ttu-id="0c8b4-526">tz</span><span class="sxs-lookup"><span data-stu-id="0c8b4-526">tz</span></span>  
<span data-ttu-id="0c8b4-527">新しい値を保持する必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-527">A Boolean value that indicates whether the new value should be persisted.</span></span>

<!-- -->

<span data-ttu-id="0c8b4-528">persist</span><span class="sxs-lookup"><span data-stu-id="0c8b4-528">persist</span></span>  
<span data-ttu-id="0c8b4-529">新しい値を保持する必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-529">A Boolean value that indicates whether the new value should be persisted.</span></span>

## <a name="method-new"></a><span data-ttu-id="0c8b4-530">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0c8b4-530">Method new</span></span>

<span data-ttu-id="0c8b4-531">DateTimeUtil クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0c8b4-531">Initializes a new instance of the DateTimeUtil class.</span></span>

```xpp
private void new()
```

