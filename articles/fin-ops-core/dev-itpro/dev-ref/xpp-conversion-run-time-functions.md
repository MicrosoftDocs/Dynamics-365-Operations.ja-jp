---
title: X++ 変換ランタイム関数
description: このトピックでは、変換ランタイム関数について説明します。
author: RobinARH
ms.date: 06/26/2018
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85c8deb332dcd25b8e767aac4fa5d91e663c305f663734c551e63b0bd8927aef
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763474"
---
# <a name="x-conversion-runtime-functions"></a>X++ 変換ランタイム関数

[!include [banner](../includes/banner.md)]

このトピックでは、変換ランタイム関数について説明します。

## <a name="any2date"></a>any2Date

**anytype** 値を **日付** 値に変換します。

```xpp
date any2Date(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                     |
|-----------|---------------------------------|
| オブジェクト    | 日付に変換する値。 |

### <a name="return-value"></a>戻り値

**日付** 値。

### <a name="remarks"></a>備考

*object* パラメーターはほとんどのデータ型にすることができますが、**str** または **int** 型である場合に役に立つ出力が取得されます。 不適切なコンテンツでは、ランタイム エラーが生成されます。

### <a name="example"></a>例

```xpp
static void any2DateExample(Args _args)
{
    date myDate;
    str s;
    int i;
    s = "2010 6 17"; // A string object, of yyyy mm dd.
    myDate = any2Date(s);
    Global::info(strFmt("%1  is output, from input of "2010 6 17"", myDate));
    i = 40361; // An int object, which represents the number of days from 1900/01/01.
    myDate = any2Date(i);
    Global::info(strFmt("%1  is output, from input of 40361", myDate));
}
/**** Infolog display.
Message (04:44:15 pm)
6/17/2010 is output, from input of "2010 6 17"
7/4/2010 is output, from input of 40361
****/
```

## <a name="any2enum"></a>any2Enum
**anytype** 値を、ターゲット列挙の要素の **名前** プロパティ値に変換します。

```xpp
enum any2Enum(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                 |
|-----------|-----------------------------------------------------------------------------|
| オブジェクト    | ターゲット列挙の要素の **Value** プロパティに一致する値。 |

### <a name="return-value"></a>戻り値

ターゲット列挙に、入力パラメーターに一致する **Value** がある方の、**Name** プロパティの値

### <a name="remarks"></a>備考

*object* パラメーターはほとんどのデータ型にすることができますが、**str** または **int** 型のパラメーターを使用した場合のみ役に立つデータが取得されます。 この入力 *オブジェクト* パラメーターは、ターゲット列挙型の個々の要素の **値** プロパティを参照します。

### <a name="example"></a>例

```xpp
static void any2EnumExample(Args _args)
{
    NoYes myNoYes;  // NoYes is an enum.
    int i;
    str s;
    i = 0;  // An int that will be converted.
    myNoYes = any2Enum(i);
    Global::info(strfmt("'%1' - is the output, from input of the %2 as int.", myNoYes, i));
    s = "1";  // A str that will be converted.
    myNoYes = any2Enum(s);
    Global::info(strfmt("'%1' - is the output, from input of the %2 as str.", myNoYes, s));
    /**** Infolog display.
    Message (01:05:32 pm)
    'No' - is the output, from input of the 0 as int.
    'Yes' - is the output, from input of the 1 as str.
    ****/
}
```

## <a name="any2guid"></a>any2Guid
指定された **anytype** オブジェクトを GUID オブジェクトに変換します。

```xpp
guid any2Guid(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                            |
|-----------|----------------------------------------|
| オブジェクト    | GUID オブジェクトに変換する値。 |

### <a name="return-value"></a>戻り値

GUID オブジェクト。

## <a name="any2int"></a>any2Int
**anytype** 値を **int** 値に変換します。

```xpp
int any2Int(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明           |
|-----------|-----------------------|
| オブジェクト    | 変換する値。 |

### <a name="return-value"></a>戻り値

**int** 値です。

### <a name="remarks"></a>備考

*object* パラメーターはほとんどのデータ型にすることができますが、**enum**、**real**、または **str** 型のパラメーターを使用した場合のみ役に立つデータが取得されます。

### <a name="example"></a>例

```xpp
static void any2IntExample(Args _args)
{
    int myInt;
    str s;
    NoYes a;
    real r;
    s = "31";
    myInt = any2Int(s);
    Global::info(strfmt("%1 is the output, from input of 31 as a str value.", myInt));
    a = NoYes::No;
    myInt = any2Int(a);
    Global::info(strfmt("%1 is the output, from input of NoYes::No as an enum value.", myInt));
    r = 5.34e2;
    myInt = any2Int(r);
    Global::info(strfmt("%1 is the output, from the input of 5.34e2 as a real value.", myInt));
}
/**** Infolog display.
Message (02:23:59 pm)
31 is the output, from input of 31 as a str value.
0 is the output, from input of NoYes::No as an enum value.
534 is the output, from the input of 5.34e2 as a real value.
****/
```

## <a name="any2int64"></a>any2Int64
**anytype** オブジェクトを **int64** オブジェクトに変換します。

```xpp
int64 any2Int64(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                        |
|-----------|------------------------------------|
| オブジェクト    | 変換する **anytype** オブジェクト。 |

### <a name="return-value"></a>戻り値

**int64** オブジェクトです。

## <a name="any2real"></a>any2Real
**anytype** 値を **実際の** 値に変換します。

```xpp
real any2Real(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明           |
|-----------|-----------------------|
| オブジェクト    | 変換する値。 |

### <a name="return-value"></a>戻り値

**実数** 値。

### <a name="remarks"></a>備考

*object* パラメーターはほとんどのデータ型にすることができますが、**date**、**int**、**enum**、および **str** 型の入力要素で役に立つ出力が取得されます。

### <a name="example"></a>例

```xpp
static void any2RealExample(Args _args)
{
    real myReal;
    str s;
    int i;
    NoYes a;
    s = "5.12";
    myReal = any2Real(s);
    Global::info(strfmt("%1 is the output from the input of 5.12 as a str object", myReal));
    i = 64;
    myReal = any2Real(i);
    Global::info(strfmt("%1 is the output from the input of 64 as an int object", myReal));
    a = NoYes::Yes;
    myReal = any2Real(a);
    Global::info(strfmt("%1 is the output from the input of NoYes::Yes as an enum object", myReal));
}
/****Infolog display.
Message (02:43:57 pm)
5.12 is the output from the input of 5.12 as a str object
64.00 is the output from the input of 64 as an int object
1.00 is the output from the input of NoYes::Yes as an enum object
****/
```

## <a name="any2str"></a>any2Str
**anytype** 値を **str** 値に変換します。

```xpp
str any2Str(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明           |
|-----------|-----------------------|
| オブジェクト    | 変換する値。 |

### <a name="return-value"></a>戻り値

**str** 値。

### <a name="remarks"></a>備考

*object* パラメーターはほとんどのデータ型にすることができますが、**date**、**int**、および **enum** 型の入力要素から役に立つ出力が取得されます。

### <a name="example"></a>例

```xpp
static void any2StrExample(Args _args)
{
    str myStr;
    anytype a;
    a = "Any to string";
    myStr = any2Str(a);
    Global::info(strFmt("%1 is output, from input of Any to string as a str value", myStr));
    a = NoYes::Yes;
    myStr = any2Str(a);
    Global::info(strFmt("%1 is output, from input of NoYes::Yes as an enumeration", myStr));
}
/****Infolog Display
Message (09:08:46 am)
Any to string is output, from input of Any to string as a str value
1 is output, from input of NoYes::Yes as an enumeration
****/
```

## <a name="anytodate"></a>anytodate
[any2Date](#any2date) を参照してください。

## <a name="anytoenum"></a>anytoenum
[any2Enum](#any2enum) を参照してください。

## <a name="anytoguid"></a>anytoguid
[any2Guid](#any2guid) を参照してください。

## <a name="anytoint"></a>anytoint
[any2Int](#any2int) を参照してください。

## <a name="anytoint64"></a>anytoint64
[any2Int64](#any2int64) を参照してください。

## <a name="anytoreal"></a>anytoreal
[any2Real](#any2real) を参照してください。

## <a name="anytostr"></a>anytostr
[any2Str](#any2str) を参照してください。

## <a name="char2num"></a>char2Num

文字列内の文字を、その文字の ASCII 値に変換します。

```xpp
int char2Num(str text, int position)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                  |
|-----------|----------------------------------------------|
| テキスト      | 文字を含む文字列。      |
| 職位  | 文字列内の文字の位置。 |

### <a name="return-value"></a>戻り値

**int** オブジェクトとしての文字の ASCII 値。

### <a name="remarks"></a>備考

```xpp
char2Num("ABCDEFG",3); //Returns the numeric value of C, which is 67.
char2Num("ABCDEFG",1); //Returns the numeric value of A, which is 65.
```

## <a name="date2num"></a>date2Num
日付を、1900 年 1 月 1 日以降の日数に対応する整数に変換します。

```xpp
int date2Num(date _date)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明          |
|-----------|----------------------|
| \_ 日付    | 変換する日付。 |

### <a name="return-value"></a>戻り値

1900 年 1 月 1 日から指定された日付までの日数。

### <a name="example"></a>例

```xpp
//Returns the value377.
date2Num(1311901);
static void date2NumExample(Args _arg)
{
    date d = today();
    int i;
    i = date2Num(d);
    print i;
}
```

## <a name="date2str"></a>date2Str
指定されたデータを文字列に変換します。

```xpp
str date2Str(date date, int sequence, int day, int separator1, int month, int separator2, int year [, int flags = DateFlags::None])
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 日付       | 変換する日付。                                                                                                                                                                                        |
| 順序   | 日付のコンポーネントの順序を示す 3 桁の番号: 日は **1**、月は **2**、年は **3**。                                                                        |
| 日        | 日付に関する、日付コンポーネントの形式を示す列挙値です。                                                                                                                            |
| separator1 | 日付の最初の 2 つのコンポーネント間で使用する区切り記号を示す列挙値です。                                                                                                       |
| 月      | 日付に関する月のコンポーネントの形式を示す列挙値です。                                                                                                                          |
| separator2 | 日付の最後の 2 つのコンポーネント間で使用する区切り記号を示す列挙値です。                                                                                                        |
| 年       | 日付に関する、年のコンポーネントの形式を示す列挙値です。                                                                                                                           |
| flags      | **DateFlags** は、ローカル コンピューター上の言語設定を使用して、返された文字列内の、左から右または右から左の順序が適切か計算する必要があるかどうかを示す列挙値です。 |

### <a name="return-value"></a>戻り値

指定日を表す文字列。

### <a name="remarks"></a>備考

MorphX は、指定された値が有効でない場合、書式設定パラメーターに有効な値を割り当てます。 地域設定で指定した日付形式を使用するには、**strFmt** または **date2Str** 関数を使用し、すべての書式設定パラメーターで **-1** を指定します。 地域の設定が日付形式を制御するときは、その設定はユーザーごとに変更できます。 **-1** がいずれかの *区切り* パラメーターに使用されている場合、両方の区切りはデフォルトで地域設定になります。 *sequence* パラメーターの値は、桁 1、2、および 3 をそれぞれちょうど 1 回含む任意の 3 桁の数値にする必要があります。 数字 1、2、および 3 は、日、月、および年をそれぞれ表します。 たとえば、**321** は連続する年、月、および日を生成します。 または、値は地域の設定を使う **-1** にすることができます。 321 などの数字は、0 ～ 250 を含む列挙値の有効な値の範囲を超えているため、このパラメーターに使用する必要がある列挙型はありません。 *フラグ* パラメーターの既定値は、**DateFlags::None** 列挙値で、左から右または右から左へのシーケンス処理は行われないことを意味します。

### <a name="example"></a>例

次の例では、現在の日付を年、月、日の順に表示します。

```xpp
static void Job2(Args _args)
{
    date currentDate = today();
    str s;
    int iEnum;
    s = date2Str
    (currentDate, 
        321,
        DateDay::Digits2,
        DateSeparator::Hyphen, // separator1
        DateMonth::Digits2,
        DateSeparator::Hyphen, // separator2
        DateYear::Digits4
    );
    info("Today is:  " + s);
}
/** Example Infolog output
Message (12:36:21 pm)
Today is:  2009-01-13
**/
```

## <a name="datetime2str"></a>datetime2Str
**utcdatetime** 値を文字列に変換します。

```xpp
str datetime2Str(utcdatetime datetime [, int flags = DateFlags::None])
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| datetime  | 変換する **utcdatetime** 値。                                                                    |
| flags     | **DateFlags** は、右から左への出力にローカル設定を使用するかどうかを示す列挙値です。 |

### <a name="return-value"></a>戻り値

*datetime* パラメーターとして指定された **utcdatetime** 値を表す文字列。

### <a name="remarks"></a>備考

#### <a name="null-date-time-input"></a>null の日付と時刻の入力

**utcdatetime** 値の最小値が *datetime* パラメーターに対して指定されている場合、**datetime2Str** 関数は null 入力値として扱われます。 これにより、関数は空の文字列を返します。 日時 **1900-01-01T00:00:00** は、**DateTimeUtil::minValue** メソッドによって返されます。 この最小値は null として扱われます。

#### <a name="right-to-left-local-settings"></a>右から左 (ローカル設定)

この関数の規定の動作では、左から右への順序で文字列を生成します。年の部分が一番左になります。 ただし、**DateFlags::FormatAll** 列挙値の *フラグ* パラメーター値は、ローカル設定が右から左に構成されている場合は、右から左の順序で文字列を生成するよう機能に指示します。 **DateTimeUtil** クラスの **toStr** メソッドの形式は、地域設定の影響を受けません。

### <a name="example"></a>例

```xpp
static void jobTestDatetime2str( Args _args )
{
    utcdatetime utc2 = 1959-06-17T15:44:33;
    str s3;
    s3 = datetime2Str( utc2 );
    info( s3 );
}
```

## <a name="enum2str"></a>enum2Str
指定された、列挙されたテキストを文字表現に変換します。

```xpp
str enum2Str(enum enum)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                     |
|-----------|---------------------------------|
| 列挙型      | 変換する列挙されたテキスト。 |

### <a name="return-value"></a>戻り値

文字列形式での列挙値。

### <a name="example"></a>例

次の例では、文字列 "含まない" を返します。 これは、**ListCode** 列挙型の **IncludeNot** 値のラベルです。

```xpp
static void enum2StrExample(Args _arg)
{
    ListCode l;
    l =  ListCode::IncludeNot;
    print enum2Str(l);
}
```

## <a name="guid2str"></a>guid2Str
指定した GUID オブジェクトを等価の文字列に変換します。

```xpp
str guid2String(guid _uuid)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                 |
|-----------|-----------------------------|
| \_uuid    | 変換する GUID オブジェクト。 |

### <a name="return-value"></a>戻り値

指定された GUID オブジェクトに等価の文字列。

### <a name="example"></a>例

```xpp
static void guid2StrExample()
{
    guid _guid;
    str stringGuid;
    _guid = Global::guidFromString("{12345678-1234-1234-1234-123456789abc}");
    print strfmt("GUID is %1", _guid);
    stringGuid = guid2str(_guid);
    info("String GUID is " + stringGuid);
}
/**** Output to Infolog
String GUID is {12345678-1234-1234-1234-123456789ABC}
****/
```

## <a name="int2str"></a>int2Str
整数を等価の文字列に変換します。

```xpp
str int2Str(int integer)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明             |
|-----------|-------------------------|
| integer   | 変換する整数。 |

### <a name="return-value"></a>戻り値

整数の文字列表現。

### <a name="example"></a>例

```xpp
static void int2StrExample(Args _arg)
{
    print "This is int2Str, value is " + int2Str(intMax());
    print "This is int642Str, value is " + int642Str(int64Max());
}
```

## <a name="int642str"></a>int642Str
指定された *整数* パラメーターを等価のテキスト文字列に変換します。

```xpp
str int642Str(int64 integer)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                       |
|-----------|-----------------------------------|
| integer   | 文字列に変換する int64。 |

### <a name="return-value"></a>戻り値

*整数* パラメーターの等価テキスト文字列。

### <a name="example"></a>例

```xpp
static void example()
{
    print "This is int2Str, value is " + int2Str(intMax());
    print "This is int642Str, value is " + int642Str(int64Max());
}
```

## <a name="num2char"></a>num2Char
整数を対応する ASCII 文字に変換します。

```xpp
str num2Char(int figure)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                            |
|-----------|----------------------------------------|
| figure    | 文字に変換する整数。 |

### <a name="return-value"></a>戻り値

指定した整数で表される文字。

### <a name="example"></a>例

```xpp
static void num2CharExample(Args _arg)
{
    str s;
    s = num2Char(42);
    // Prints an asterisk * -the character represented by 42.
    print s;
}
```

## <a name="num2date"></a>num2Date
1900 年 1 月 1 日から指定した日数に対応する日付を取得します。

```xpp
date num2Date(int _days)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                                                                                                                                                |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_日    | 1900 年 1 月 1 日以降の日数を返します。 **注記:** 最初の有効日は 1901 年 1 月 1 日です。 したがって、**num2Date** 関数は、*\_days* が **365** を超えない限り、有効な日付を返しません。 |

### <a name="return-value"></a>戻り値

1900 年 1 月 1 日以降に、*\_days* パラメーターで指定された日数の日付。

### <a name="remarks"></a>備考

```xpp
num2Date(366); //Returns the date 01/01/1901 (1 January 1901).
```

## <a name="num2str"></a>num2Str
実数を文字列に変換します。

```xpp
str num2Str(real number, int character, int decimals, int separator1, int separator2)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                     |
|------------|-----------------------------------------------------------------|
| 数値     | 文字列に変換する実数。                         |
| 文字  | テキストに必要な最小文字数。 |
| decimals   | 小数点以下の必要な桁数。                          |
| separator1 | **DecimalSeparator** 列挙値。                       |
| separator2 | **ThousandSeparator** 列挙値。                      |

### <a name="return-value"></a>戻り値

番号を表す文字列。

### <a name="remarks"></a>備考

*小数点以下* パラメーターについては、最大値は **16** です。 より大きい数値が使用された場合、このメソッドは *小数点以下* のパラメーターの値をローカル コンピューターから取得します。 どちらの場合も、丸めが発生します。 *separator1* パラメータの使用可能な列挙値を次に示します。

-   **99** – 自動 (ユーザーの書式設定によって使用される小数点区切り記号を決定)、列挙値 DecimalSeparator::Auto 
-   **1** – ドット (.)、列挙値 DecimalSeparator::Dot
-   **2** – コンマ (,)、列挙値 DecimalSeparator::Comma

*separator2* パラメータの使用可能な値を次に示します。

-   **99** – 自動 (ユーザーの書式設定によって使用される 3 桁の区切り文字を決定)
-   **0** – なし (3 桁の区切り文字なし)、列挙値 ThousandSeparator::None
-   **1** – ドット (.)、列挙値 ThousandSeparator::Dot
-   **2** – コンマ (,)、列挙値 ThousandSeparator::Comma
-   **3** – アポストロフィ (')、列挙値 ThousandSeparator::Apostrophe
-   **4** – スペース ( )、列挙値 ThousandSeparator::Space

### <a name="example"></a>例

次のコード例では、**num2str** メソッドの最初の呼び出しでは **16** が *小数点以下* のパラメーターに渡され、2 番目の呼び出しでは **17** が渡されます。

```xpp
static void Job_Num2Str(Args _args)
{
    real realNum = 0.1294567890123456777; // 19 decimals places.
    info(Num2Str(realNum, 0, 16, DecimalSeparator::Dot, ThousandSeparator::Space)); // 16 decimal places
    info(Num2Str(realNum, 0, 17, DecimalSeparator::Dot, ThousandSeparator::Space)); // 17 decimal places
}
```

### <a name="output"></a>出力

メッセージは次の Infolog 出力にあります。 出力の最初の数字には 16 桁の小数が含まれ、2 番目の数字には小数点以下 2 桁の小数のみが含まれます。

```xpp
Message (10:18:12)
0.1294567890123457
0.13
```

## <a name="str2date"></a>str2Date
指定された文字列を **データ** 値に変換します。

```xpp
date str2Date(str _text, str _sequence)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| \_テキスト     | **date** 値に変換する文字列。                                                               |
| \_順序 | 変換する文字列の日、月、年の位置を表す 3 桁の整数。 |

### <a name="return-value"></a>戻り値

**日付** 値。

### <a name="remarks"></a>備考

*\_sequence* パラメーターで日、月、年の位置を指定するには、次の値を使用します。

-   **日付:** 1
-   **月:** 2
-   **年:** 3

たとえば、文字列の順序が月、年、さらに日である場合、*\_順序* パラメーターは **231** である必要があります。 入力パラメーターが無効な日付を指定した場合、日付 **0**(ゼロ) が返されます。 次の 2 つの例では無効な日付を指定しています。

```xpp
str2Date("31/12/44", 123) // Year must be four digits to reach the minimum of January 1 1901.
str2Date("31/12/2044", 213) // 213 means the month occurs first in the string, but 31 cannot be a month.
```

### <a name="example"></a>例

```xpp
static void str2DateExample(Args _arg)
{
    date d;
    d = str2Date("22/11/2007", 123);
    print d;
}
```

## <a name="str2datetime"></a>str2Datetime
日付と時刻情報の指定した文字列から **utcdatetime** 値を生成します。

```xpp
utcdatetime str2datetime( str text, int sequence )
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------|
| テキスト      | **utcdatetime** 値に変換する文字列。                                                |
| 順序  | *テキスト* パラメーターの日付コンポーネントの順序を示す 3 桁の番号。 |

### <a name="return-value"></a>戻り値

**utcdatetime** 値は、指定された日付と時刻を表します。

### <a name="remarks"></a>備考

*text* パラメーターの日付部分の構文要件は柔軟性があります。 有効な形式のバリエーションは、**date2str** 関数と同じです。 **str2datetime** への以下の呼び出しはそれぞれ有効です。またそれらすべての出力は同じです。

```xpp
utc3 = str2datetime( "1985/02/25 23:04:59" ,321 );
utc3 = str2datetime( "Feb-1985-25 11:04:59 pm" ,231 );
utc3 = str2datetime( "2 25 1985 11:04:59 pm" ,123 );
```

各コンポーネントの日時は、*シーケンス* パラメーター内の数字で表されます。

-   **1** - 日
-   **2** - 月
-   **3** - 年

たとえば、年、月、日の順序は **321** です。 すべての有効な値には、これらの 3 桁の数字がそれぞれ正確に 1 回含まれます。 *順序* パラメーターの値が無効である場合、入力 *テキスト* パラメーターを解釈するために地域の設定が使用されます。 入力パラメーターに無効な日付と時刻が表示されている場合は、空の文字列が返されます。

### <a name="example"></a>例

```xpp
static void JobTestStr2datetime( Args _args )
{
    utcdatetime utc3;
    str sTemp;
    utc3 = str2datetime( "1985/02/25 23:04:59" ,321 );
    sTemp = datetime2str( utc3 );
    print( "sTemp == " + sTemp );
}
```

## <a name="str2enum"></a>str2Enum
ローカライズされた **Label** プロパティ値が入力文字列に一致する列挙要素を取得します。

```xpp
enum str2Enum(enum _type, str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                              |
|-----------|--------------------------------------------------------------------------|
| \_タイプ    | **列挙** 型の宣言された変数。                        |
| \_テキスト    | 列挙型内のターゲット要素のローカライズ **ラベル** プロパティのテキスト。 |

### <a name="return-value"></a>戻り値

ターゲット列挙の要素で、int も表します。

### <a name="remarks"></a>備考

関連関数 **enum2str** は列挙型の 1 要素から **Label** プロパティの値を返します。 **enum2str** 関数により返された値は、**str2enum** 関数の *\_type* パラメーターの入力となります。 *\_テキスト* パラメータは、**enum2Str(BankAccountType::SavingsAccount)** の適切な値です。 各列挙型要素には、**名前** プロパティおよび **ラベル** プロパティがあります。 新規インストールでは、**名前** の値はほぼ必ず英語です。 英語版では、**ラベル** のプロパティ値がほとんどの場合、**名前** の値と同じです。 ただし、英語以外のエディションでは、**ラベル** 値はローカライズされるため **名前** 値とは一致しません。

### <a name="example"></a>例

他の言語にローカライズされたために発生する文字列の不一致を避けるために、**str2enum** 関数への入力を生成するには **enum2str** 関数を使用することをお勧めします。 次の例は、**str2enum** 関数と **enum2str** 関数を併用する適切な方法を示しています。

```xpp
static void str2Enum_AcrossLangs(Args _arg)
{
    BankAccountType bat;
    str sEnumValueLabelLocalized;
    int nInt;
    // enum2str.
    sEnumValueLabelLocalized = enum2str(BankAccountType::SavingsAccount);
    info("Localized friendly string: "
        + sEnumValueLabelLocalized);
    // str2enum.
    bat = str2Enum(bat, sEnumValueLabelLocalized);
    nInt = bat;
    info("nInt = " + int2str(nInt));
    /********** Actual output:
    Message (04:32:12 pm)
    Localized friendly string: Savings account
    nInt = 1
    **********/
}
```

## <a name="str2guid"></a>str2Guid
文字列を GUID オブジェクトに変換します。

```xpp
Guid str2Guid(str text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                      |
|-----------|----------------------------------|
| guid      | GUID を表す文字列。 |

### <a name="return-value"></a>戻り値

入力文字列で表される GUID。

### <a name="remarks"></a>備考

たとえば、*GUID* パラメータの有効な値は **{12345678-1234-abCD-3456-123456789012}** で、かっこ付きまたはかっこなしのいずれかです。

## <a name="str2int"></a>str2Int
文字列を等価の整数に変換します。

```xpp
int str2Int(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                          |
|-----------|--------------------------------------|
| \_テキスト    | 整数に変換する文字列。 |

### <a name="return-value"></a>戻り値

指定された文字列の等価整数。

### <a name="example"></a>例

```xpp
static void str2IntExample(Args _arg)
{
    int i;
    i = str2Int("1234567890");
    print "i = " + int2Str(i);
}
```

## <a name="str2int64"></a>str2Int64
文字列を **Int64** 値に変換します。

```xpp
int str2Int64(str text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明            |
|-----------|------------------------|
| テキスト      | 変換する文字列。 |

### <a name="return-value"></a>戻り値

指定された文字列の **Int64** 値。

### <a name="example"></a>例

```xpp
static void str2Int64Example(Args _args)
{
    str myStr;
    str tooBig;
    Int64 myInt64;
    myStr = "1234567890";
    tooBig = int642str(int64Max()+1);
    myInt64 = str2Int64(mystr);
    print strfmt ("int64: %1",myInt64);
    myInt64 = str2Int64(tooBig);
    print strfmt ("Too big int64: %1",myInt64);
}
```

## <a name="str2num"></a>str2Num
文字列を実数に変換します。

```xpp
real str2Num(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| \_テキスト    | 実数に変換する文字列。 |

### <a name="return-value"></a>戻り値

指定された文字列に有効な数値が含まれている場合の実数。それ以外の場合は **0** (ゼロ) です。

### <a name="remarks"></a>備考

次の例では、この関数の使用方法を示しています。

```xpp
str2Num("123.45") returns the value 123.45.
str2Num("a123") returns the value 0.0.
str2Num("123a") returns the value 123.00.
```

スキャンは左から右に行われ、文字を実数の一部に変換できなくなると終了します。

### <a name="example"></a>例

```xpp
static void str2NumToReal(Args _arg)
{
    real r;
    str s;
    r = str2Num("3.15");
    s = strFmt("r = %1", r);
    info(s);
}
/*** Infolog output.
Message_@SYS14327 (02:36:12 pm)
r = 3.15
***/

static void str2NumExponentialSyntax(Args _args)
{
    Qty qty1, qty2, qty3;
    qty1 = str2num('1e-3'); // Bad syntax by the user.
    qty2 = str2num('1.e-3');
    qty3 = str2num('1.0e-3');
    info(strfmt('Result: %1; Expected: %2', num2str(qty1, 0,3,2,0), '0.001'));
    info(strfmt('Result: %1; Expected: %2', num2str(qty2, 0,3,2,0), '0.001'));
    info(strfmt('Result: %1; Expected: %2', num2str(qty3, 0,3,2,0), '0.001'));
}
/*** Infolog output. The first result differs from expectations.
Message_@SYS14327 (02:20:55 pm)
Result: 1,000; Expected: 0.001
Result: 0,001; Expected: 0.001
Result: 0,001; Expected: 0.001
***/
```

## <a name="str2time"></a>str2Time
文字列を **timeOfDay** 値に変換します。

```xpp
int str2Time(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                        |
|-----------|--------------------------------------------------------------------|
| \_テキスト    | 深夜からの秒数を計算するために使用する時間。 |

### <a name="return-value"></a>戻り値

真夜中と *\_text* パラメーターの間の秒数。 そうでなければ、**-1**。

### <a name="remarks"></a>備考

```xpp
str2Time("05:01:37") //Returns the value 18097.
str2Time("7 o'clock") //Returns the value -1.
```

### <a name="example"></a>例

```xpp
static void str2TimeExample(Args _arg)
{
    int i;
    i = str2Time("11:30");
    print i;
}
```

## <a name="time2str"></a>time2Str
**timeOfDay** 値を時、分、秒を含む文字列に変換します。

```xpp
str time2Str(int _time, int _separator, int _timeFormat)
```

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                                                                                                                       |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| \_タイム       | **timeOfDay** 値。                                                                                                            |
| \_区切り記号  | **TimeSeparator** は、出力文字列の時、分、秒の間の文字を示す列挙値です。 |
| \_timeFormat | **TimeFormat** は、12時間制または24時間制のどちらを使用するかを示す列挙値です。                             |

### <a name="return-value"></a>戻り値

指定された時間を表す文字列。

### <a name="remarks"></a>備考

*\_time* パラメーターの値は、深夜 0 時からの秒数です。

### <a name="example"></a>例

```xpp
static void TimeJob4(Args _args)
{
    timeOfDay theTime = timeNow();
    info( time2Str(theTime, TimeSeparator::Colon, TimeFormat::AMPM) );
}
/**
Message (04:33:56 pm)
04:33:56 pm
**/
```

## <a name="uint2str"></a>uint2Str
整数を文字列に変換します。 整数が符号なしであることを前提としています。

```xpp
str uint2Str(int integer)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明             |
|-----------|-------------------------|
| integer   | 変換する整数。 |

### <a name="return-value"></a>戻り値

指定された符号なし整数に同等の文字列。

### <a name="remarks"></a>備考

レコード ID などの非常に大きな整数の場合は、**int2str** 関数の代わりにこの関数を使用します。

```xpp
info(int2str(3123456789)); //returns -1171510507 as a string.
info(uint2str(3123456789)); //returns 3123456789 as a string.
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]