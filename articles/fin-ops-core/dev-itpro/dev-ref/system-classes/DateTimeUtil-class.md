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
# <a name="class-datetimeutil"></a>クラス DateTimeUtil

[!include [banner](../../includes/banner.md)]

```xpp
class DateTimeUtil extends Object
```

DateTimeUtil クラスは、utcdatetime および Timezone 値を変換または変更するために使用できます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>方法

| 方法                                                                                                                                                                            | 説明                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ::public static DateTime addDays(DateTime t, int value)                                                                                                                           | utcdatetime 値に指定された日数を追加します。                                                                                                      |
| ::public static DateTime addHours(DateTime t, int value)                                                                                                                          | utcdatetime 値に指定された時間数を追加します。                                                                                                     |
| ::public static DateTime addMinutes(DateTime t, int value)                                                                                                                        | utcdatetime 値に指定された分数を追加します。                                                                                                   |
| ::public static DateTime addMonths(DateTime t, int value)                                                                                                                         | utcdatetime 値に指定された月数を追加します。                                                                                                    |
| ::public static DateTime addSeconds(DateTime t, Int64 value)                                                                                                                      | utcdatetime 値に指定された秒数を追加します。                                                                                                   |
| ::public static DateTime addYears(DateTime t, int value)                                                                                                                          | utcdatetime 値に指定された年数を追加します。                                                                                                     |
| ::public static DateTime anyToDateTime(AnyType value)                                                                                                                             | 任意のオブジェクトを utcdatetime 値に変換します。                                                                                                             |
| ::public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)                                                                                                             | 指定された utcdatetime 値から、指定された Timezone 列挙値により示された量オフセットされる utcdatetime 値を取得します。 |
| ::public static str applyTimeZoneOffsetFilter(QueryFilter filter)                                                                                                                 | フィルターにタイム ゾーン オフセットを適用します。                                                                                                                    |
| ::public static str applyTimeZoneOffsetRange(QueryBuildRange range)                                                                                                               | 範囲にタイム ゾーン オフセットを適用します。                                                                                                                     |
| ::public static Date date(DateTime t)                                                                                                                                             | 指定された utcdatetime 値をデータ タイプに変換します。                                                                                                       |
| ::public static int day(DateTime t)                                                                                                                                               | utcdatetime 値によって指定されている月の日を取得します。                                                                                       |
| ::public static Timezone getClientMachineTimeZone()                                                                                                                               | クライアント コンピューターのタイム ゾーン列挙値を取得します。                                                                                                    |
| ::public static Timezone getCompanyTimeZone()                                                                                                                                     | 現在の法人に設定されているタイム ゾーンを取得します。                                                                                              |
| ::public static Int64 getDifference(DateTime t1, DateTime t2)                                                                                                                     | 2 つの指定された utcdatetime 値間の秒数を取得します。                                                                                           |
| ::public static Timezone getOriginatingTimeZone(DateTime t)                                                                                                                       | 指定した utcdatetime 値の元のタイム ゾーン列挙値を取得します。                                                                            |
| ::public static Date getSystemDate(Timezone tz)                                                                                                                                   |                                                                                                                                                                |
| ::public static DateTime getSystemDateTime()                                                                                                                                      | utcdatetime 値としての現在のシステム時刻を取得します。                                                                                                           |
| ::public static TimeOfDay getTimeNow(Timezone tz)                                                                                                                                 |                                                                                                                                                                |
| ::public static TimeZoneId getTimeZoneId(Timezone tz)                                                                                                                             |                                                                                                                                                                |
| ::public static int getTimeZoneOffset(DateTime t, Timezone tz)                                                                                                                    | タイム ゾーン列挙値の情報を使用して UTC に指定された utcdatetime 値のオフセットを取得します。                                            |
| ::public static int getTimeZoneRule(DateTime t)                                                                                                                                   | 指定した日に影響を与えるタイム ゾーン ルールを返します。                                                                                                |
| ::public static Date getToday(Timezone tz)                                                                                                                                        |                                                                                                                                                                |
| ::public static PreferredCalendar getUserPreferredCalendar()                                                                                                                      | 現在のユーザーの PreferredCalendar 列挙値を取得します。                                                                                             |
| ::public static Timezone getUserPreferredTimeZone()                                                                                                                               | 現在のユーザーの PreferredTimezone 列挙値を取得します。                                                                                             |
| ::public static int hour(DateTime t)                                                                                                                                              | utcdatetime 値によって指定されている日の時間を取得します。                                                                                        |
| ::public static DateTime maxValue()                                                                                                                                               | utcdatetime タイプの変数に許可される最大値を取得します。                                                                            |
| ::public static int minute(DateTime t)                                                                                                                                            | utcdatetime 値によって指定されている時間の分を取得します。                                                                                     |
| ::public static DateTime minValue()                                                                                                                                               | utcdatetime タイプの変数に許可される最小値を取得します。                                                                            |
| ::public static int month(DateTime t)                                                                                                                                             | utcdatetime 値によって指定されている年の月を取得します。                                                                                      |
| ::public static DateTime newDateTime(Date date, TimeOfDay time, \[Timezone tzOffsetToRemove\])                                                                                    | 指定されたデータおよび timeOfDay 値を使用して、新しい utcdatetime 値を作成します。                                                                              |
| ::public static DateTime parse(str s)                                                                                                                                             | 指定された文字列から新しい utcdatetime 値を作成します。                                                                                                     |
| ::public static container populateTimeZoneInfo(int year, Timezone tz)                                                                                                             | 開始日と終了日と時間バイアスを取得します。                                                                                                                   |
| ::public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)                                                                                                            | 指定した utcdatetime 値からタイムゾーンの列挙値によって示されるオフセットを削除します。                                                     |
| ::public static str removeTimeZoneOffsetFilter(QueryFilter filter)                                                                                                                | フィルターからタイム ゾーン オフセットを削除します。                                                                                                                  |
| ::public static str removeTimeZoneOffsetRange(QueryBuildRange range)                                                                                                              | 範囲からタイム ゾーン オフセットを削除します。                                                                                                                   |
| ::public static int second(DateTime t)                                                                                                                                            | utcdatetime 値によって指定されている分の秒を取得します。                                                                                    |
| ::public static TimeOfDay time(DateTime t)                                                                                                                                        | 指定した utcdatetime 値から timeOfDay 値として午前 0 時からの経過秒数を取得します。                                    |
| ::public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, \[int flags\]) |                                                                                                                                                                |
| ::public static str toStr(DateTime t)                                                                                                                                             | utcdatetime 値を次の形式の文字列に変換します。YYYY-MM-DDThh:mm:ss。T は文字リテラルです。                                         |
| ::public static DateTime utcNow()                                                                                                                                                 | 現在のシステム時刻を示す utcdatetime 値を取得します。                                                                                          |
| ::public static int year(DateTime t)                                                                                                                                              | utcdatetime 値によって指定されている年を取得します。                                                                                                   |
| ::public static void setSystemDateTime(DateTime t)                                                                                                                                | 指定した utcdatetime 値に、システムの日時を設定します。                                                                                       |
| ::public static void setCompanyTimeZone(Timezone tz, \[boolean persist\])                                                                                                         | 現在の会社によって使用されているタイムゾーン列挙値を設定します。                                                                                       |
| ::public static void setUserPreferredCalendar(PreferredCalendar calendar)                                                                                                         | 現在のセッションの現在のユーザーの PreferredCalendar 列挙型の値を設定します。                                                          |
| ::public static void setUserPreferredTimeZone(Timezone tz, \[boolean persist\])                                                                                                   | 指定したタイムゾーンの列挙値に、ユーザーの優先タイム ゾーンを設定します。                                                                          |
| private void new()                                                                                                                                                                | DateTimeUtil クラスの新しいインスタンスを初期化します。                                                                                                          |

## <a name="method-adddays"></a>メソッド addDays

utcdatetime 値に指定された日数を追加します。

```xpp
public static DateTime addDays(DateTime t, int value)
```

### <a name="parameters---adddays"></a>パラメーター - addDays

t  
追加する日数。

<!-- -->

値  
追加する日数。

### <a name="return-value---adddays"></a>戻り値 - addDays

新しい utcdatetime 値。

### <a name="remarks---adddays"></a>備考 - addDays

値パラメーターの値が負の場合は、日数が差し引かれます。

## <a name="method-addhours"></a>メソッド addHours

utcdatetime 値に指定された時間数を追加します。

```xpp
public static DateTime addHours(DateTime t, int value)
```

### <a name="parameters---addhours"></a>パラメーター - addHours

t  
追加する時間数。

<!-- -->

値  
追加する時間数。

### <a name="return-value---addhours"></a>戻り値 - addHours

新しい utcdatetime 値。

### <a name="remarks---addhours"></a>備考 - addHours

値パラメーターの値が負の場合は、時間数が差し引かれます。

## <a name="method-addminutes"></a>メソッド addMinutes

utcdatetime 値に指定された分数を追加します。

```xpp
public static DateTime addMinutes(DateTime t, int value)
```

### <a name="parameters---addminutes"></a>パラメーター - addMinutes

t  
追加する分数。

<!-- -->

値  
追加する分数。

### <a name="return-value---addminutes"></a>戻り値 - addMinutes

新しい utcdatetime 値。

### <a name="remarks---addminutes"></a>備考 - addMinutes

値パラメーターの値が負の場合は、分数が差し引かれます。

## <a name="method-addmonths"></a>メソッド addMonths

utcdatetime 値に指定された月数を追加します。

```xpp
public static DateTime addMonths(DateTime t, int value)
```

### <a name="parameters---addmonths"></a>パラメーター - addMonths

t  
追加する月数。

<!-- -->

値  
追加する月数。

### <a name="return-value---addmonths"></a>戻り値 - addMonths

新しい utcdatetime 値。

### <a name="remarks---addmonths"></a>備考 - addMonths

値パラメーターの値が負の場合は、月数が差し引かれます。

## <a name="method-addseconds"></a>メソッド addSeconds

utcdatetime 値に指定された秒数を追加します。

```xpp
public static DateTime addSeconds(DateTime t, Int64 value)
```

### <a name="parameters---addseconds"></a>パラメーター - addSeconds

t  
追加する秒数。

<!-- -->

値  
追加する秒数。

### <a name="return-value---addseconds"></a>戻り値 - addSeconds

新しい utcdatetime 値。

### <a name="remarks---addseconds"></a>備考 - addSeconds

値パラメーターの値が負の場合は、秒数が差し引かれます。

## <a name="method-addyears"></a>メソッド addYears

utcdatetime 値に指定された年数を追加します。

```xpp
public static DateTime addYears(DateTime t, int value)
```

### <a name="parameters---addyears"></a>パラメーター - addYears

t  
追加する年数。

<!-- -->

値  
追加する年数。

### <a name="return-value---addyears"></a>戻り値 - addYears

新しい utcdatetime 値。

### <a name="remarks---addyears"></a>備考 - addYears

値パラメーターの値が負の場合は、年数が差し引かれます。

## <a name="method-anytodatetime"></a>メソッド anyToDateTime

任意のオブジェクトを utcdatetime 値に変換します。

```xpp
public static DateTime anyToDateTime(AnyType value)
```

### <a name="parameters---anytodatetime"></a>パラメーター - anyToDateTime

値  
変換するオブジェクト。

### <a name="return-value---anytodatetime"></a>戻り値 - anyToDateTime

新しい utcdatetime 値。

### <a name="remarks---anytodatetime"></a>備考 - anyToDateTime

次の例の文字列は、この anyToDateTime メソッドが正しく変換できる日付/時刻文字列の形式を示しています ("2009-01-28T13：44：55")。 DateTimeUtil::utcNow メソッドの出力は anyToDateTime メソッドへの有効な入力です。

## <a name="method-applytimezoneoffset"></a>メソッド applyTimeZoneOffset

指定された utcdatetime 値から、指定された Timezone 列挙値により示された量オフセットされる utcdatetime 値を取得します。

```xpp
public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)
```

### <a name="parameters---applytimezoneoffset"></a>パラメーター - applyTimeZoneOffset

t  
使用する新しいオフセットを示すタイム ゾーン列挙値。

<!-- -->

tz  
使用する新しいオフセットを示すタイム ゾーン列挙値。

### <a name="return-value---applytimezoneoffset"></a>戻り値 - applyTimeZoneOffset

新しい utcdatetime 値。

## <a name="method-applytimezoneoffsetfilter"></a>メソッド applyTimeZoneOffsetFilter

フィルターにタイム ゾーン オフセットを適用します。

```xpp
public static str applyTimeZoneOffsetFilter(QueryFilter filter)
```

### <a name="parameters---applytimezoneoffsetfilter"></a>パラメーター - applyTimeZoneOffsetFilter

フィルター  

### <a name="return-value---applytimezoneoffsetfilter"></a>戻り値 - applyTimeZoneOffsetFilter

新しい日付/時間範囲の値。

## <a name="method-applytimezoneoffsetrange"></a>メソッド applyTimeZoneOffsetRange

範囲にタイム ゾーン オフセットを適用します。

```xpp
public static str applyTimeZoneOffsetRange(QueryBuildRange range)
```

### <a name="parameters---applytimezoneoffsetrange"></a>パラメーター - applyTimeZoneOffsetRange

範囲  

### <a name="return-value---applytimezoneoffsetrange"></a>戻り値 - applyTimeZoneOffsetRange

新しい日付/時間範囲の値。

## <a name="method-date"></a>メソッド date

指定された utcdatetime 値をデータ タイプに変換します。

```xpp
public static Date date(DateTime t)
```

### <a name="parameters---date"></a>パラメーター - date

t  
変換する utcdatetime 値。

### <a name="return-value---date"></a>戻り値 - date

日付の値です。

## <a name="method-day"></a>メソッド day

utcdatetime 値によって指定されている月の日を取得します。

```xpp
public static int day(DateTime t)
```

### <a name="parameters---day"></a>パラメーター - day

t  
日付のコンポーネントの値を取得するための utcdatetime 値。

### <a name="return-value---day"></a>戻り値 - day

指定した utcdatetime 値の月の日。

## <a name="method-getclientmachinetimezone"></a>メソッド getClientMachineTimeZone

クライアント コンピューターのタイム ゾーン列挙値を取得します。

```xpp
public static Timezone getClientMachineTimeZone()
```

### <a name="return-value---getclientmachinetimezone"></a>戻り値 - getClientMachineTimeZone

クライアント コンピューターのタイム ゾーン列挙値。

## <a name="method-getcompanytimezone"></a>メソッド getCompanyTimeZone

現在の法人に設定されているタイム ゾーンを取得します。

```xpp
public static Timezone getCompanyTimeZone()
```

### <a name="return-value---getcompanytimezone"></a>戻り値 - getCompanyTimeZone

現在の法人に設定されているタイム ゾーン

## <a name="method-getdifference"></a>メソッド getDifference

2 つの指定された utcdatetime 値間の秒数を取得します。

```xpp
public static Int64 getDifference(DateTime t1, DateTime t2)
```

### <a name="parameters---getdifference"></a>パラメーター - getDifference

t1  
2 番目の utcdatetime 値。

<!-- -->

t2  
2 番目の utcdatetime 値。

### <a name="return-value---getdifference"></a>戻り値 - getDifference

2 つの指定された utcdatetime 値間の秒数。

## <a name="method-getoriginatingtimezone"></a>メソッド getOriginatingTimeZone

指定した utcdatetime 値の元のタイム ゾーン列挙値を取得します。

```xpp
public static Timezone getOriginatingTimeZone(DateTime t)
```

### <a name="parameters---getoriginatingtimezone"></a>パラメーター - getOriginatingTimeZone

t  
タイム ゾーンを取得するための utcdatetime 値。

### <a name="return-value---getoriginatingtimezone"></a>戻り値 - getOriginatingTimeZone

指定した utcdatetime 値のタイム ゾーン列挙値。

## <a name="method-getsystemdate"></a>メソッド getSystemDate

```xpp
public static Date getSystemDate(Timezone tz)
```

### <a name="parameters---getsystemdate"></a>パラメーター - getSystemDate

tz  

### <a name="return-value---getsystemdate"></a>戻り値 - getSystemDate

## <a name="method-getsystemdatetime"></a>メソッド getSystemDateTime

utcdatetime 値としての現在のシステム時刻を取得します。

```xpp
public static DateTime getSystemDateTime()
```

### <a name="return-value---getsystemdatetime"></a>戻り値 - getSystemDateTime

utcdatetime 値としての現在のシステム時刻。

### <a name="remarks---getsystemdatetime"></a>備考 - getSystemDateTime

システム時刻に固定値がない場合は、それが返されます。 それ以外の場合、現在の日付と時刻がローカル コンピューターから返されます。

## <a name="method-gettimenow"></a>メソッド getTimeNow

```xpp
public static TimeOfDay getTimeNow(Timezone tz)
```

### <a name="parameters---gettimenow"></a>パラメーター - getTimeNow

tz  

### <a name="return-value---gettimenow"></a>戻り値 - getTimeNow

## <a name="method-gettimezoneid"></a>メソッド getTimeZoneId

```xpp
public static TimeZoneId getTimeZoneId(Timezone tz)
```

### <a name="parameters---gettimezoneid"></a>パラメーター - getTimeZoneId

tz  

### <a name="return-value---gettimezoneid"></a>戻り値 - getTimeZoneId

## <a name="method-gettimezoneoffset"></a>メソッド getTimeZoneOffset

タイム ゾーン列挙値の情報を使用して UTC に指定された utcdatetime 値のオフセットを取得します。

```xpp
public static int getTimeZoneOffset(DateTime t, Timezone tz)
```

### <a name="parameters---gettimezoneoffset"></a>パラメーター - getTimeZoneOffset

t  
T パラメーターのタイム ゾーンを示すタイム ゾーン列挙値。

<!-- -->

tz  
T パラメーターのタイム ゾーンを示すタイム ゾーン列挙値。

### <a name="return-value---gettimezoneoffset"></a>戻り値 - getTimeZoneOffset

UTC に指定された utcdatetime 値のオフセットを示す整数。

## <a name="method-gettimezonerule"></a>メソッド getTimeZoneRule

指定した日に影響を与えるタイム ゾーン ルールを返します。

```xpp
public static int getTimeZoneRule(DateTime t)
```

### <a name="parameters---gettimezonerule"></a>パラメーター - getTimeZoneRule

t  

### <a name="return-value---gettimezonerule"></a>戻り値 - getTimeZoneRule

指定された日付のタイム ゾーン ルール。

## <a name="method-gettoday"></a>メソッド getToday

```xpp
public static Date getToday(Timezone tz)
```

### <a name="parameters---gettoday"></a>パラメーター - getToday

tz  

### <a name="return-value---gettoday"></a>戻り値 - getToday

## <a name="method-getuserpreferredcalendar"></a>メソッド getUserPreferredCalendar

現在のユーザーの PreferredCalendar 列挙値を取得します。

```xpp
public static PreferredCalendar getUserPreferredCalendar()
```

### <a name="return-value---getuserpreferredcalendar"></a>戻り値 - getUserPreferredCalendar

現在のユーザーの PreferredCalendar 列挙値。

## <a name="method-getuserpreferredtimezone"></a>メソッド getUserPreferredTimeZone

現在のユーザーの PreferredTimezone 列挙値を取得します。

```xpp
public static Timezone getUserPreferredTimeZone()
```

### <a name="return-value---getuserpreferredtimezone"></a>戻り値 - getUserPreferredTimeZone

現在のユーザーの PreferredTimezone 列挙値。

## <a name="method-hour"></a>メソッド hour

utcdatetime 値によって指定されている日の時間を取得します。

```xpp
public static int hour(DateTime t)
```

### <a name="parameters---hour"></a>パラメーター - hour

t  
時間のコンポーネントの値を取得するための utcdatetime 値。

### <a name="return-value---hour"></a>戻り値 - hour

指定した utcdatetime 値の日の時間。

## <a name="method-maxvalue"></a>メソッド maxValue

utcdatetime タイプの変数に許可される最大値を取得します。

```xpp
public static DateTime maxValue()
```

### <a name="return-value---maxvalue"></a>戻り値 - maxValue

utcdatetime タイプの変数に許可される最大値。

## <a name="method-minute"></a>メソッド minute

utcdatetime 値によって指定されている時間の分を取得します。

```xpp
public static int minute(DateTime t)
```

### <a name="parameters---minute"></a>パラメーター - minute

t  
分のコンポーネントの値を取得するための utcdatetime 値。

### <a name="return-value---minute"></a>戻り値 - minute

指定した utcdatetime 値の時間の分。

## <a name="method-minvalue"></a>メソッド minValue

utcdatetime タイプの変数に許可される最小値を取得します。

```xpp
public static DateTime minValue()
```

### <a name="return-value---minvalue"></a>戻り値 - minValue

utcdatetime タイプの変数に許可される最小値。

## <a name="method-month"></a>メソッド month

utcdatetime 値によって指定されている年の月を取得します。

```xpp
public static int month(DateTime t)
```

### <a name="parameters---month"></a>パラメーター - month

t  
月のコンポーネントの値を取得するための utcdatetime 値。

### <a name="return-value---month"></a>戻り値 - month

指定された utcdatetime 値の年の月。

## <a name="method-newdatetime"></a>メソッド newDateTime

指定されたデータおよび timeOfDay 値を使用して、新しい utcdatetime 値を作成します。

```xpp
public static DateTime newDateTime(Date date, TimeOfDay time, [Timezone tzOffsetToRemove])
```

### <a name="parameters---newdatetime"></a>パラメーター - newDateTime

日付  
新しい utcdatetime 値を作成するタイム ゾーン (オプション)。

<!-- -->

タイム  
新しい utcdatetime 値を作成するタイム ゾーン (オプション)。

<!-- -->

tzOffsetToRemove  
新しい utcdatetime 値を作成するタイム ゾーン (オプション)。

### <a name="return-value---newdatetime"></a>戻り値 - newDateTime

新しい utcdatetime 値。

### <a name="remarks---newdatetime"></a>備考 - newDateTime

TzOffsetToRemove パラメーターの値が指定されていない場合は、UTC タイム ゾーンで utcdatetime 値が作成されます。

## <a name="method-parse"></a>メソッド parse

指定された文字列から新しい utcdatetime 値を作成します。

```xpp
public static DateTime parse(str s)
```

### <a name="parameters---parse"></a>パラメーター - parse

秒  
次の形式の文字列: yyyy-mm-ddThh:mm:ss。

### <a name="return-value---parse"></a>戻り値 - parse

指定した文字列からの新しい utcdatetime 値。

## <a name="method-populatetimezoneinfo"></a>メソッド populateTimeZoneInfo

開始日と終了日と時間バイアスを取得します。

```xpp
public static container populateTimeZoneInfo(int year, Timezone tz)
```

### <a name="parameters---populatetimezoneinfo"></a>パラメーター - populateTimeZoneInfo

年  
タイム ゾーン。

<!-- -->

tz  
タイム ゾーン。

### <a name="return-value---populatetimezoneinfo"></a>戻り値 - populateTimeZoneInfo

開始日と終了日と時間バイアス。

## <a name="method-removetimezoneoffset"></a>メソッド removeTimeZoneOffset

指定した utcdatetime 値からタイムゾーンの列挙値によって示されるオフセットを削除します。

```xpp
public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)
```

### <a name="parameters---removetimezoneoffset"></a>パラメーター - removeTimeZoneOffset

t  
削除するタイム ゾーン列挙値。

<!-- -->

tz  
削除するタイム ゾーン列挙値。

### <a name="return-value---removetimezoneoffset"></a>戻り値 - removeTimeZoneOffset

タイム ゾーン オフセットなしの utcdatetime 値。

## <a name="method-removetimezoneoffsetfilter"></a>メソッド removeTimeZoneOffsetFilter

フィルターからタイム ゾーン オフセットを削除します。

```xpp
public static str removeTimeZoneOffsetFilter(QueryFilter filter)
```

### <a name="parameters---removetimezoneoffsetfilter"></a>パラメーター - removeTimeZoneOffsetFilter

フィルター  

### <a name="return-value---removetimezoneoffsetfilter"></a>戻り値 - removeTimeZoneOffsetFilter

新しい日付/時間範囲の値。

## <a name="method-removetimezoneoffsetrange"></a>メソッド removeTimeZoneOffsetRange

範囲からタイム ゾーン オフセットを削除します。

```xpp
public static str removeTimeZoneOffsetRange(QueryBuildRange range)
```

### <a name="parameters---removetimezoneoffsetrange"></a>パラメーター - removeTimeZoneOffsetRange

範囲  

### <a name="return-value---removetimezoneoffsetrange"></a>戻り値 - removeTimeZoneOffsetRange

新しい日付/時間範囲の値。

## <a name="method-second"></a>メソッド second

utcdatetime 値によって指定されている分の秒を取得します。

```xpp
public static int second(DateTime t)
```

### <a name="parameters---second"></a>パラメーター - second

t  
秒のコンポーネントの値を取得するための utcdatetime 値。

### <a name="return-value---second"></a>戻り値 - second

指定された utcdatetime 値の分の秒です。

## <a name="method-time"></a>メソッド time

指定した utcdatetime 値から timeOfDay 値として午前 0 時からの経過秒数を取得します。

```xpp
public static TimeOfDay time(DateTime t)
```

### <a name="parameters---time"></a>パラメーター - time

t  
時刻を取得するための utcdatetime 値。

### <a name="return-value---time"></a>戻り値 - time

午前 0 時から経過した秒数を示す timeOfDay 値。

## <a name="method-toformattedstr"></a>メソッド toFormattedStr

```xpp
public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, [int flags])
```

### <a name="parameters---toformattedstr"></a>パラメーター - toFormattedStr

t  

<!-- -->

順序  

<!-- -->

曜日  

<!-- -->

separator1  

<!-- -->

か月  

<!-- -->

separator2  

<!-- -->

年  

<!-- -->

timeSeparator1  

<!-- -->

timeSeparator2  

<!-- -->

flags  

### <a name="return-value---toformattedstr"></a>戻り値 - toFormattedStr

## <a name="method-tostr"></a>メソッド toStr

utcdatetime 値を次の形式の文字列に変換します。YYYY-MM-DDThh:mm:ss。T は文字リテラルです。

```xpp
public static str toStr(DateTime t)
```

### <a name="parameters---tostr"></a>パラメーター - toStr

t  
変換する utcdatetime 値。

### <a name="return-value---tostr"></a>戻り値 - toStr

指定された utcdatetime 値の文字列表現。

## <a name="method-utcnow"></a>メソッド utcNow

現在のシステム時刻を示す utcdatetime 値を取得します。

```xpp
public static DateTime utcNow()
```

### <a name="return-value---utcnow"></a>戻り値 - utcNow

utcdatetime 値としての現在のシステム時刻。

### <a name="remarks---utcnow"></a>備考 - utcNow

このメソッドはサーバー上で実行されるため、返される時刻はサーバーのシステム時刻です。

## <a name="method-year"></a>メソッド year

utcdatetime 値によって指定されている年を取得します。

```xpp
public static int year(DateTime t)
```

### <a name="parameters---year"></a>パラメータ - year

t  
年のコンポーネントの値を取得するための utcdatetime 値。

### <a name="return-value---year"></a>戻り値 - year

指定された utcdatetime 値の年。

## <a name="method-setsystemdatetime"></a>メソッド setSystemDateTime

指定した utcdatetime 値に、システムの日時を設定します。

```xpp
public static void setSystemDateTime(DateTime t)
```

### <a name="parameters---setsystemdatetime"></a>パラメーター - setSystemDateTime

t  
システム日時を設定する utcdatetime 値。

## <a name="method-setcompanytimezone"></a>メソッド setCompanyTimeZone

現在の会社によって使用されているタイムゾーン列挙値を設定します。

```xpp
public static void setCompanyTimeZone(Timezone tz, [boolean persist])
```

### <a name="parameters---setcompanytimezone"></a>パラメーター - setCompanyTimeZone

tz  
新しい値を保持する必要があるかどうかを示すブール値。

<!-- -->

persist  
新しい値を保持する必要があるかどうかを示すブール値。

## <a name="method-setuserpreferredcalendar"></a>メソッド setUserPreferredCalendar

現在のセッションの現在のユーザーの PreferredCalendar 列挙型の値を設定します。

```xpp
public static void setUserPreferredCalendar(PreferredCalendar calendar)
```

### <a name="parameters---setuserpreferredcalendar"></a>パラメーター - setUserPreferredCalendar

カレンダー  
設定する PreferredCalendar 列挙値。

## <a name="method-setuserpreferredtimezone"></a>メソッド setUserPreferredTimeZone

指定したタイムゾーンの列挙値に、ユーザーの優先タイム ゾーンを設定します。

```xpp
public static void setUserPreferredTimeZone(Timezone tz, [boolean persist])
```

### <a name="parameters---setuserpreferredtimezone"></a>パラメーター - setUserPreferredTimeZone

tz  
新しい値を保持する必要があるかどうかを示すブール値。

<!-- -->

persist  
新しい値を保持する必要があるかどうかを示すブール値。

## <a name="method-new"></a>メソッド new

DateTimeUtil クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

