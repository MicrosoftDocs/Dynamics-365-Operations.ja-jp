---
title: X++ ビジネス ランタイム関数
description: この記事では、ビジネス ランタイム関数について説明します。
author: RobinARH
ms.date: 06/20/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57235edc67ecf929d0342d3e826b28d54297c312
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867237"
---
# <a name="x-business-runtime-functions"></a>X++ ビジネス ランタイム関数

[!include [banner](../includes/banner.md)]

この記事では、ビジネス ランタイム関数について説明します。

これらの関数は財務データを入力し、式を計算します。

## <a name="cterm"></a>cTerm
現在の投資価値がターゲット値に達するために必要な期間の数を計算します。

### <a name="syntax"></a>構文

```xpp
real cTerm(real interest, real future_value, real current_value)
```
### <a name="parameters"></a>パラメーター

| パラメーター      | 説明                   |
|----------------|-------------------------------|
| 利息       | 利率。            |
| future\_value  | ターゲット値。             |
| current\_value | 現在の投資価値。 |

### <a name="return-value"></a>戻り値

*future\_value* に達するために必要な期間の数。

### <a name="remarks"></a>備考

*current\_value* および *future\_value* パラメーターには、同じ接頭辞記号 (プラスまたはマイナス) が付いています。

### <a name="example"></a>例

```xpp
static void cTermExample(Args _arg)
{
    real r;
    ;
    r = cTerm(10.0, 500.00, 100.00);
    print "The cTerm is " + num2Str(r, 2, 2, 1, 1);
    pause;
}
```

## <a name="ddb"></a>ddb

資産の増加償却を計算します。

### <a name="syntax"></a>構文

```xpp
real ddb(real price, real scrap, real life, int period)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                |
|-----------|------------------------------------------------------------|
| 価格     | アセットの購買価格。                           |
| 仕損     | 損金処理された資産の残存価値。 |
| life      | 資産の予想有効期間。                        |
| 期間    | 減価償却を計算する期間。                 |

### <a name="return-value"></a>戻り値

資産の減価償却。

### <a name="remarks"></a>備考

特定期間の簿価額は、購入価格から前期間の減価償却累計額を差し引いた額に等しい。

-   期間 1 の簿価額 = 価格
-   期間 2 の簿価額 = 期間 1 の簿価額 – 期間の減価償却 1
-   期間 n の簿価額 = 期間 (n–1) の簿価額 – 期間の減価償却 (n–1)

減価償却費の計算には 3 つのバリエーションがあります。期間タイプ &gt; 耐用年数:

-   減価償却 = 0

If (期間 n の簿価額) – ((期間 n の簿価額) × 2 ÷ ライフ) &lt; 残存価額:

-   減価償却 = (期間 n の簿価額) – 残存価額

その他の場合: 減価償却 = (期間 n の簿価額) × 2 ÷ 耐用年数、**syd** および **sln** 関数も、資産の減価償却を計算します。 **syd** および **ddb** 関数を使用すると、早い年の減価償却を高くできますが、**sln** は直線的な減価償却を計算します。

```xpp
ddb(12000,2000,10,1); //Returns the value 2400.
ddb(12000,2000,10,3); //Returns the value 1536.
```

## <a name="dg"></a>dg

販売価格および購買価格に基づいて利益率を計算します。 *売上* パラメーターの値が **0.0** である場合、計算を実行することはできません。

### <a name="syntax"></a>構文

```xpp
real dg(real sale, real purchase)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明         |
|-----------|---------------------|
| 販売      | 販売価格。     |
| 購買  | 購買価格。 |

### <a name="return-value"></a>戻り値

利益率。

### <a name="remarks"></a>備考

```xpp
dg(1000,300); //Returns the value 0.7.
dg(100,30); //Returns the value 0.7.
dg(20000, 11000); //Returns the value 0.45.
```

## <a name="fv"></a>fV

投資の未来価値を計算します。

### <a name="syntax"></a>構文

```xpp
real fV(real amount, real interest, real life)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                     |
|-----------|-------------------------------------------------|
| 金額    | 各期間中に支払われた金額。 |
| 利息  | 利率。                              |
| life      | 投資期間の数。               |

### <a name="return-value"></a>戻り値

投資の将来の値。

### <a name="remarks"></a>備考

```xpp
fV(100,0.14,10); //Returns the value 1933.73.
fV(400,0.10,5); //Returns the value 2442.04.
```

## <a name="idg"></a>idg

利益率および購買価格に基づいて販売価格を計算します。

```xpp
real idg(real purchase, real contribution_ratio)
```

### <a name="parameters"></a>パラメーター

| パラメーター           | 説明             |
|---------------------|-------------------------|
| 購買            | 購買価格。     |
| contribution\_ratio | 利益率。 |

### <a name="return-value"></a>戻り値

販売価格。

### <a name="remarks"></a>備考

利益率が **1.0** と等しい場合は、計算を実行することはできません。 **idg** 関数は、**dg** 関数の逆です。

```xpp
idg(300,0.7); //Returns the value 1000.
idg(11000,0.45); //Returns the value 20000.
```

## <a name="intvmax"></a>intvMax
期間が *func* パラメーターによって指定された部分に分割されているとき、指定された期間の間隔の数を取得します。

```xpp
int intvMax(date input_date, date ref_date, int func)
```

### <a name="parameters"></a>パラメーター

| パラメーター   | 説明                                                                |
|-------------|----------------------------------------------------------------------------|
| input\_date | 期間の終了日は、*ref\_date* パラメーターよりも後でなければなりません。 |
| ref\_date   | 期間の開始日。                                                   |
| func        | **IntvScale** は、部門単位を示すシステム列挙値です。 |

### <a name="remarks"></a>備考

*func* パラメータの使用可能な値を次に示します。

-   None
-   YearMonthDay
-   YearMonth
-   年
-   MonthDay
-   月
-   曜日
-   YearQuarter
-   四半期
-   YearWeek
-   週
-   WeekDay

### <a name="example"></a>例

```xpp
static void intvMaxExample()
{
    date refDate = str2Date("4/9/2007", 213);
    date inputDate = str2Date("10/5/2007", 213);
    int numberOfIntervals;
    ;
    numberOfIntervals = intvMax(inputDate, refDate, intvScale::YearMonth);
    print numberOfIntervals;
    pause;
}
```

## <a name="intvname"></a>intvName
指定した日付から指定した間隔数先の間隔の名前を返します。

```xpp
str intvName(date input_date, int col, enum func)
```

### <a name="parameters"></a>パラメーター

| パラメーター   | 説明                                                                                 |
|-------------|---------------------------------------------------------------------------------------------|
| input\_date | 最初の間隔の日付です。                                                               |
| col         | *input\_date* パラメーターで指定された日付より前の間隔の数。 |
| func        | **intvScale** 列挙値です。                                                         |

### <a name="return-value"></a>戻り値

間隔の名前。

### <a name="remarks"></a>備考

たとえば、*func* パラメーターが、**IntvScale::WeekDay** 列挙値である場合、このメソッドは平日の名前を返します。 *func* パラメーターが、**IntvScale::Week** 列挙値である場合、このメソッドは週の数が含まれている文字列を返します。

### <a name="example"></a>例

```xpp
static void intvNameExample(Args _args)
{
    date refDate = 2672010;
    str name;
    ;
    name = intvName(refDate, 3,  intvScale::WeekDay);
    Global::info(strfmt("%1 is the output, which indicates the day of the week 3 days after 26\7\2010.", name));
}
/**** Infolog display.
Message (09:56:55 am)
Thu is the output, which indicates the day of the week 3 days after 2672010.
****/
```

## <a name="intvno"></a>intvNo
指定した間隔に時間を分割するとき、2 つの日付間の間隔の数を計算します。

### <a name="syntax"></a>構文

```xpp
int intvNo(date input_date, date ref_date, int func)
```

### <a name="parameters"></a>パラメーター

| パラメーター   | 説明                                    |
|-------------|------------------------------------------------|
| input\_date | 期間の終了を示す日付    |
| ref\_date   | 期間の開始を示す日付です。 |
| func        | **intvScale** 列挙値です。            |

### <a name="return-value"></a>戻り値

*ref\_date* および *input\_date* パラメーターで指定された日付間の間隔の数。

### <a name="example"></a>例

```xpp
static void intvNoExample(Args _args)
{
    date inputDate = str2Date("1/1/2007", 213);
    date refDate = str2Date("3/1/2007", 213);
    int noOfIntervals;
    ;
    noOfIntervals = intvNo(refDate, inputDate, intvScale::Month);
    print noOfIntervals;
    pause;
    //noOfIntervals now holds the difference in months between March and January (2).
}
```

## <a name="intvnorm"></a>intvNorm
期間の正規化日を返します。

### <a name="syntax"></a>構文

```xpp
date intvNorm(date input_date, date ref_date, int func)
```

### <a name="parameters"></a>パラメーター

| パラメーター   | 説明                                                                                              |
|-------------|----------------------------------------------------------------------------------------------------------|
| input\_date | 期間の終了日は、*ref\_date* パラメーターが指定した日付よりも後でなければなりません。 |
| ref\_date   | 期間の開始日。                                                                                 |
| func        | **intvScale** は、間隔区分単位を示す列挙値です。                            |

### <a name="return-value"></a>戻り値

期間の正規化日

### <a name="remarks"></a>備考

返される日付は、*ref\_date* パラメーターで指定された日付が存在する区間の、最初の日の日付になります。

### <a name="example"></a>例

```xpp
static void example()
{
    print intvNorm(today(), today()-1, IntVScale::WeekDay);
    pause;
}
```

## <a name="pmt"></a>pmt

ローンを返済するために毎回支払われなければならない金額を計算します。

### <a name="syntax"></a>構文

```xpp
real pmt(real principal, real interest, real life)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                               |
|-----------|---------------------------------------------------------------------------|
| principal | 最初に借り入れた金額。                                  |
| 利息  | 各期間に借用した金額に適用される利息。 |
| life      | ローンが返済される期間の数。                       |

### <a name="return-value"></a>戻り値

期間ごとに支払われる必要のある金額。

### <a name="remarks"></a>備考

*life* および *interest* パラメーターは、同じ時間単位で表される必要があります。 *life* パラメーターの値は、**0.0** を超える必要があります。

### <a name="example"></a>例

```xpp
pmt(4000,0.14,4); //Returns the value 1372.82.
pmt(10000,0.10,20); //Returns the value 1174.60.
```

## <a name="pt"></a>pt

その番号の指定された割合と数値の合計を取得します。

### <a name="syntax"></a>構文

```xpp
real pt(real amount, real percentage)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                |
|------------|----------------------------|
| 金額     | 元の番号。       |
| パーセント | パーセント補足。 |

### <a name="return-value"></a>戻り値

((<em>amount *× *percentage</em>) + <em>amount</em>) に等しい数。

### <a name="remarks"></a>備考

```xpp
pt(2000.0,0.10); //Returns the value 2200.0.
pt(20.0,0.10); //Returns the value 22.0.
```

## <a name="pv"></a>pv

年金の現在価値を計算します。金額は複数の期間にわたり支払われ、利息は期間ごとに控除されます。

### <a name="syntax"></a>構文

```xpp
real pv(real amount, real interest, real life)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                             |
|-----------|-----------------------------------------------------------------------------------------|
| 金額    | 各期間中に支払われる金額。                                             |
| 利息  | 利率。                                                                      |
| life      | *amount* パラメーターで指定された値が支払われた回数。 |

### <a name="return-value"></a>戻り値

年金の現在の値。

### <a name="remarks"></a>備考

```xpp
pv(300,0.14,4); //Returns the value 874.11.
```

## <a name="rate"></a>レート
現在の投資価値が指定された期間の数にわたって未来価値を達成するために必要な利子を計算します。

### <a name="syntax"></a>構文

```xpp
real rate(real _future_value, real _current_value, real _terms)
```

### <a name="parameters"></a>パラメーター

| パラメーター        | 説明                                      |
|------------------|--------------------------------------------------|
| \_将来\_値  | 投資の将来の値。              |
| \_現在\_値 | 投資の現在の値。             |
| \_使用条件          | 投資がわたる期間の数。 |

### <a name="return-value"></a>戻り値

計算済利率。

### <a name="remarks"></a>備考

```xpp
rate(10000,1000,20); //Returns the value 0.12.
```

## <a name="sln"></a>sln

減価償却期間ごとに指定された資産の固定の減価償却金額を取得します。

### <a name="syntax"></a>構文

```xpp
real sln(real price, real scrap, real life)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                              |
|-----------|----------------------------------------------------------|
| 価格     | アセットの購買価格。                         |
| 仕損     | 資産の仕損価格。                            |
| life      | 資産の予想期限における期間の数。 |

### <a name="return-value"></a>戻り値

減価償却金額。

### <a name="example"></a>例

```xpp
static void slnExample(Args _arg)
{
    real r;
    ;
    r = sln(100.00, 50.00, 50.00);
    print r;
    pause;
}
```

## <a name="syd"></a>syd

指定した期間にわたる資産の減価償却を計算します。

### <a name="syntax"></a>構文

```xpp
real syd(real _price, real _scrap, real _life, int _period)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                             |
|-----------|---------------------------------------------------------|
| \_価格   | アセットの購買価格。                        |
| \_仕損   | 資産の仕損価格。                           |
| \_期限    | 資産の予想期限 (期間数)。 |
| \_期間  | 減価償却を計算する期間。               |

### <a name="return-value"></a>戻り値

指定した期間での減価償却の金額。

### <a name="remarks"></a>備考

**sln** 関数とは対照的に、**syd** 関数は資産の増加償却を可能にします。 **ddb** 関数と同様に、資産の耐用年数の初期段階におけるよりも高い減価償却が可能になります。

### <a name="example"></a>例

次の例では、定期的な減価償却が 10,000 の購買価格、2,000 の仕損価格、および 5 の耐用年数の資産に対して計算されます。 比較では、**sln(10000,2000,5)** は各期間ごとに 1600.00 を算出します。

```xpp
// Returns the value 2666.67 (for the 1st period).
syd(10000,2000,5,1);
// Returns the value 2133.33 (for the 2nd period).
syd(10000,2000,5,2);
// Returns the value 1600.00 (for the 3rd period).
syd(10000,2000,5,3);
// Returns the value 1066.67 (for the 4th period).
syd(10000,2000,5,4);
// Returns the value 533.33 (for 5th - and final- period).
syd(10000,2000,5,5);
```

## <a name="term"></a>term
投資が実行されなければならない期間の数を計算します。

### <a name="syntax"></a>構文

```xpp
real term(real amount, real interest, real future_value)
```

### <a name="parameters"></a>パラメーター

| パラメーター     | 説明                                             |
|---------------|---------------------------------------------------------|
| 金額        | 定期的な投資の金額。                  |
| 利息      | 各期間の利率。                      |
| future\_value | 投資に予想される将来の価値 |

### <a name="return-value"></a>戻り値

投資が実行されなければならない期間の数。

### <a name="example"></a>例

```xpp
static void termExample(Args _args)
{
    print term(400,0.08,5000);  //returns the value '9.01'.
    print term(100,0.14,3000);  //returns the value '12.58'.
    pause;
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]