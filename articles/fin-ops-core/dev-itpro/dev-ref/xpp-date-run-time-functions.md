---
title: X++ 日付ランタイム関数
description: このトピックでは、日付ランタイム関数について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31341
ms.assetid: fbaf07ef-63d0-40aa-bef5-e44d6c6a4643
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc4c26f116eb45aabe2505877af907dfe60bf74a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408691"
---
# <a name="x-date-runtime-functions"></a>X++ 日付ランタイム関数

[!include [banner](../includes/banner.md)]

このトピックでは、日付ランタイム関数について説明します。

<a name="dayname"></a>dayName
-------

番号で指定されている曜日の名前を取得します。

```xpp
str dayName(int number)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                    |
|-----------|--------------------------------|
| 数値    | 週内の日付の数。 |

### <a name="return-value"></a>戻り値

番号パラメーターで指定された曜日。

### <a name="remarks"></a>備考

番号のパラメーターの有効値は **1** ～ **7** です。 月曜日は **1**、火曜日は **2**、日曜日は **7** として表されます。

### <a name="example"></a>例

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

## <a name="dayofmth"></a>dayOfMth
指定された日付の月内の日数を計算します。

```xpp
int dayOfMth(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明       |
|-----------|-------------------|
| 日付      | テストする日付。 |

### <a name="return-value"></a>戻り値

指定された日付の月の日を示す 1 から 31 までの整数。

### <a name="remarks"></a>備考

```xpp
dayOfMth(31122001) //returns 31.
```

### <a name="example"></a>例

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

## <a name="dayofwk"></a>dayOfWk
指定された日付の週内の日数を計算します。 **注記:** 月曜日は **1**、火曜日は **2**、日曜日は **7** として表されます。

```xpp
int dayOfWk(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                               |
|-----------|-----------------------------------------------------------|
| 日付      | 年、月、日を示す **日付** 値。 |

### <a name="return-value"></a>戻り値

指定された曜日の数。

### <a name="example"></a>例

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

## <a name="dayofyr"></a>dayOfYr
1 月 1 日から指定された日までの日数を計算します。

```xpp
int dayOfYr(date _date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                     |
|-----------|-------------------------------------------------|
| \_ 日付    | 年、月、日を指定する日付です。 |

### <a name="return-value"></a>戻り値

1 月 1 日から指定された日付までの日数。

### <a name="remarks"></a>備考

1 月 1 日は **1**、12 月 31 日は **365** または **366** です。

### <a name="example"></a>例

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

## <a name="endmth"></a>endMth
指定した日付の月の最後の日付を計算します。

```xpp
date endMth(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                             |
|-----------|---------------------------------------------------------|
| 日付      | 年、月、日を示す **日付** 値。 |

### <a name="return-value"></a>戻り値

指定した月の最後の日付の **date** 値。

### <a name="remarks"></a>備考

```xpp
endMth(0221988); //Returns the date 2921988 because 1988 is a leap year.
endMth(0221989); //Returns the date 2821989.
```

## <a name="mkdate"></a>mkDate
日、月、および年を示す 3 つの整数に基づいて日付を作成します。

```xpp
date mkDate(int day, int month, int year)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                               |
|-----------|---------------------------------------------------------------------------|
| 日       | 月の日を表す整数。                          |
| 月     | 年の月を表す整数。                         |
| 年      | 1900 年から 2154 年の間で必要とする年を表す整数。 |

### <a name="return-value"></a>戻り値

*日*、*月*、および *年* のパラメーター値に基づく **日付** 値。

### <a name="remarks"></a>備考

データが無効である場合は、このメソッドは **0** (zero, 1/1/1900) 日付を返します。 Dynamics AX 7.0 (2016 年 2 月) から、1975 年の 75 のような、その年のショートカット値はサポートされていません。 その年のショートカット値を指定すると、1900 年 1 月 1 日の日付が返されます。

### <a name="example"></a>例

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

## <a name="mthname"></a>mthName
指定された月の名前を取得します

```xpp
str monthName(int number)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明              |
|-----------|--------------------------|
| 数値    | 月の番号。 |

### <a name="return-value"></a>戻り値

指定された月の名前。

### <a name="remarks"></a>備考

*番号* のパラメーターの有効値は **1** ～ **12** です。 1 月は **1** で、12 月は **12** で表されます。

### <a name="example"></a>例

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

## <a name="mthofyr"></a>mthOfYr
指定された日付の年内の月数を取得します。 **注記:** 1 月は **1**、2 月は **2**、12 月は **12** となります。

```xpp
int mthOfYr(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| 日付      | 年月日を指定する日付です。 |

### <a name="return-value"></a>戻り値

*日付* パラメーターで表される月の年の月の数字。

### <a name="example"></a>例

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

## <a name="nextmth"></a>nextMth
指定した日付に最も近い、対応する次の月の日付を取得します。

```xpp
date nextMth(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| 日付      | 翌月に一致する日付。 |

### <a name="return-value"></a>戻り値

翌月に指定された日付に最も近い一致。

### <a name="remarks"></a>備考

```xpp
nextMth(2921996); //returns 29/03/1996.
nextMth(3111996); //returns 2921996, because 1996 is a leap year.
```

### <a name="example"></a>例

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

## <a name="nextqtr"></a>nextQtr
指定した日付に最も近い、対応する次の四半期の日付を取得します。

```xpp
date nextQtr(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                 |
|-----------|---------------------------------------------|
| 日付      | 翌四半期に一致する日付。 |

### <a name="return-value"></a>戻り値

次の四半期に指定された日付に最も近い一致。

### <a name="remarks"></a>備考

たとえば、**nextQtr(3111998)** は **3041998** を返します。

### <a name="example"></a>例

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

## <a name="nextyr"></a>nextYr
指定した日付に最も近い、対応する次の年の日付を取得します。

```xpp
date nextYr(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                              |
|-----------|------------------------------------------|
| 日付      | 翌年に一致する日付。 |

### <a name="return-value"></a>戻り値

翌年に指定された日付に最も近い一致。

### <a name="remarks"></a>備考

たとえば、**nextyr(2921998)** は **2821999** を返します。

### <a name="example"></a>例

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

## <a name="prevmth"></a>prevMth
指定した日付に最も近い、対応する前の月の日付を取得します。

```xpp
date prevMth(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                              |
|-----------|------------------------------------------|
| 日付      | 前月に一致する日付。 |

### <a name="return-value"></a>戻り値

前月に指定された日付に最も近い一致。

### <a name="remarks"></a>備考

```xpp
prevMth(3131996); //Returns the date 29/02/1996 because 1996 is a leap year.
prevMth(2821998); //Returns the date 28/01/1998.
```

## <a name="prevqtr"></a>prevQtr
指定した日付に最も近い、対応する前の四半期の日付を取得します。

```xpp
date prevQtr(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                |
|-----------|--------------------------------------------|
| 日付      | 前四半期に一致する日付。 |

### <a name="return-value"></a>戻り値

前の四半期に指定された日付に最も近い一致。

### <a name="remarks"></a>備考

```xpp
prevQtr(3041998); //Returns the date 30/01/1998.
prevQtr(2951996); //Returns the date 29/02/1996, because 1996 is a leap year.
```

## <a name="prevyr"></a>prevYr
指定した日付に最も近い、対応する前の年の日付を取得します。

```xpp
date prevYr(date date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| 日付      | 前年に一致する日付。 |

### <a name="return-value"></a>戻り値

前年に指定された日付に最も近い一致。

### <a name="remarks"></a>備考

```xpp
prevYr(2921996); //Returns the date 28/02/1995 because 1996 is a leap year.
prevYr(2821998); //Returns the date 28/02/1997.
```

## <a name="systemdateget"></a>systemDateGet
設定されている場合は、セッションの日付を取得します。

```xpp
date systemDateGet()
```

### <a name="return-value"></a>戻り値

セッションの日付が設定されている場合はそれを返します。それ以外の場合はシステムの日付を返します。

### <a name="remarks"></a>備考

**セッション日時** ページを開くには、**ツール** メニューの **セッション日時** を使用してください。 このページを使用して、セッションの日付を有効に設定できます。 システムによってこの設定されたアクションが検出されると、その後の **systemDateGet** 関数の呼び出しによってセッションの日付が返されます。 **today** 関数は、システム日付を返します。 この関数は、タイム ゾーンをサポートしていません。

### <a name="example"></a>例

次の例は、Infolog ウィンドウの日付を示しています。

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

## <a name="systemdateset"></a>systemDateSet
システム日付を変更します。

```xpp
date systemDateSet(date _date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                  |
|-----------|------------------------------|
| \_ 日付    | システムの新しい日付。 |

### <a name="return-value"></a>戻り値

新しいシステム日付。

### <a name="remarks"></a>備考

この関数は、セッションの日付には影響しません。 このメソッドは日付を変更しますが、時刻は **0** (ゼロ) に設定されます。

### <a name="example"></a>例

次の例では、システムの日付を今日の日付に設定します。

```xpp
static void systemDateSetExample(Args _arg)
{
    date d = today();
    d = systemDateSet(d);
    print d;
}
```

## <a name="timenow"></a>timeNow
現在のシステム時刻を取得します。

```xpp
int timeNow()
```

### <a name="return-value"></a>戻り値

午前0時から経過した秒数。

### <a name="example"></a>例

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

## <a name="today"></a>今日
システムの現在の日付を取得します。

```xpp
date today()
```

### <a name="return-value"></a>戻り値

現在の日付。

### <a name="example"></a>例

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

## <a name="wkofyr"></a>wkOfYr
ISO 8601 仕様に従って、日付に該当する年の週を計算します。

```xpp
int wkOfYr(date _date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                     |
|-----------|-------------------------------------------------|
| \_ 日付    | その年の週を計算する日付。 |

### <a name="return-value"></a>戻り値

*\_date* パラメーターが発生する週のシーケンス番号。

### <a name="example"></a>例

次のコード例は、**wkOfYr** 関数と **Global::weekOfYear** メソッドを比較します。 関数とメソッドは異なる結果を生成します。

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

上記の例は、次の情報を表示のために情報ログに送信します。 出力は、**wkOfYr** と **Global::weekOfYear** の間に違いがあることを示しています。 

```xpp
Message (01:59:13 pm) ----- 
#1. For Sunday, January 5, 2003 ----- 1 = wkOfYr function 2 = Global::weekOfYear method ----- 
#2. For Wednesday, August 20, 2003 ----- 34 = wkOfYr function 34 = Global::weekOfYear method ----- 
#3. For Sunday, December 28, 2003 ----- 52 = wkOfYr function 1 = Global::weekOfYear method
```

## <a name="year"></a>年
**date** 値から年を取得します。

```xpp
int year(date _date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                       |
|-----------|-----------------------------------|
| \_ 日付    | 年を返す日付。 |

### <a name="return-value"></a>戻り値

指定した日付の年。

### <a name="remarks"></a>備考

```xpp
year(0221998); //Returns the value 1998.
```


