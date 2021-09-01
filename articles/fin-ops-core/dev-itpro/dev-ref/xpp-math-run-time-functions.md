---
title: X++ 数学ランタイム関数
description: このトピックでは、数学ランタイム関数について説明します。
author: RobinARH
ms.date: 06/20/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6447ae98fcbafdf6a9bdd2f11bd152b94e85126cf3e39a50a72772bae2fc1d1b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748356"
---
# <a name="x-math-runtime-functions"></a>X++ 数学ランタイム関数

[!include [banner](../includes/banner.md)]

このトピックでは、数学ランタイム関数について説明します。

これらの関数は数学的な計算を実行します。

## <a name="abs"></a>abs

実数の絶対値を取得します。 例

-   **abs(-100.0)** は、値 **100.0** を返します。
-   **abs(30.56)** は、値 **30.56** を返します。

### <a name="syntax"></a>構文

```xpp
real abs(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                              |
|-----------|------------------------------------------|
| arg       | 絶対値を取得する数。 |

### <a name="return-value"></a>戻り値

*arg* の絶対値。

### <a name="example"></a>例

```xpp
static void absExample(Args _args)
{
    real r1;
    real r2;
    ;
    r1 = abs(-3.14);
    r2 = abs(3.14);
    if (r1 == r2)
    {
        print "abs of values are the same";
        pause;
    }
}
```

## <a name="acos"></a>acos
実数の逆余弦を取得します。

> [!NOTE]
> 注記: 引数が -1 から 1 の範囲外である場合、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。

### <a name="syntax"></a>構文

```xpp
real acos(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| arg       | 逆余弦を取得するための数。 |

### <a name="return-value"></a>戻り値

*arg* の逆余弦。

### <a name="example"></a>例

```xpp
static void acosExample(Args _args)
{
    real r;
    str  s;
    ;
    r = acos(0.0);
    s = strFmt("The arc cosine of 0.0 is %1 ", r);
    print s;
    pause;
}
```

## <a name="asin"></a>asin
実数の逆正弦を取得します。

> [!NOTE]
> 注記: 引数が -1 から 1 の範囲外である場合、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。

### <a name="syntax"></a>構文

```xpp
real asin(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| arg       | 逆正弦を計算する数。 |

### <a name="return-value"></a>戻り値

指定した数の逆正弦。

### <a name="remarks"></a>備考

**aSin(0.36)** は **0.37** を返します。

## <a name="atan"></a>atan
実数の逆正接を取得します。

### <a name="syntax"></a>構文

```xpp
real atan(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                  |
|-----------|----------------------------------------------|
| arg       | 逆正接を計算する数。 |

### <a name="return-value"></a>戻り値

指定した数の逆正接。

### <a name="remarks"></a>備考

**aTan(0.36)** は **0.35** を返します。

### <a name="example"></a>例

```xpp
static void atanExample(Args _args)
{
    real r;
    ;
    r = atan(1.0);
    print strFmt("The Arc Tangent of 1.0 is %1", r);
    pause;
}
```

## <a name="corrflagget"></a>corrFlagGet
実数の修正フラグの状態を取得します。

### <a name="syntax"></a>構文

```xpp
int corrFlagGet(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| arg       | 状態を取得するためのフラグ。 |

### <a name="return-value"></a>戻り値

フラグが **0** (ゼロ) に設定された場合、フラグがクリアされた場合はゼロ以外の値。

### <a name="example"></a>例

次の例は、**1** を表示します。

```xpp
static void corrFlagGetExample(Args _args)
{
    real rr;
    rr = corrFlagSet(0.36,2);
    print(corrFlagGet(rr));
}
```

## <a name="corrflagset"></a>corrFlagSet
実数の補正フラグをコントロールします。

### <a name="syntax"></a>構文

```xpp
real corrFlagSet(real real, int arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                       |
|-----------|-------------------------------------------------------------------|
| real      | 補正フラグをオンまたはオフにする番号。        |
| arg       | フラグを無効にするには **0**、フラグを有効にする場合は、0 以外の値。 |

### <a name="return-value"></a>戻り値

**0** フラグが現在オフの場合。フラグがオンの場合はゼロ以外の値。

## <a name="cos"></a>cos


実数の余弦を取得します。

### <a name="syntax"></a>構文

```xpp
real cos(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                        |
|-----------|------------------------------------|
| arg       | 余弦を計算する数。 |

### <a name="return-value"></a>戻り値

指定した数のコサイン。

### <a name="remarks"></a>備考

パラメーター *arg* の値はラジアンにする必要があります。

### <a name="example"></a>例

次のコード例は、**0.76** を表示します。

```xpp
static void cosExample(Args _arg)
{
    real r;
    ;
    r = cos(15);
    print strFmt("Cos of 15 is %1", r);
    pause;
}
```

## <a name="cosh"></a>cosh
実数の双曲線余弦を取得します。

> [!NOTE]
> 注記: 引数が -250 から 250 の範囲外である場合、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。

### <a name="syntax"></a>構文

```xpp
real cosh(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                        |
|-----------|----------------------------------------------------|
| arg       | 余弦を計算する双曲線余弦。 |

### <a name="return-value"></a>戻り値

指定した数の双曲線余弦。

### <a name="remarks"></a>備考

パラメーター *arg* の値はラジアンにする必要があります。

### <a name="example"></a>例

```xpp
static void coshExample(Args _arg)
{
    real r;
    ;
    r = cosh(0.1);
    print "The hyperbolic cosine of 0.1 is " + num2Str(r, 2, 2, 1, 1);
    pause;
}
```

## <a name="decround"></a>decRound
指定された小数点以下の桁数となるように数値の端数を丸めます。

### <a name="syntax"></a>構文

```xpp
real decRound(real figure, int decimals)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| figure    | 切り上げ後の数。                      |
| decimals  | 丸められる小数点以下の桁数。 |

### <a name="return-value"></a>戻り値

指定された数値の小数点以下の桁数を丸めた値。

### <a name="remarks"></a>備考

*decimals* パラメーターの値は、正の値、0 (ゼロ)、負の値のいずれかになります。

-   **decRound(1234.6574,2)** は、値 **1234.66** を返します。
-   **decRound(1234.6574,0)** は、値 **1235** を返します。
-   **decRound(1234.6574,-2)** は、値 **1200** を返します。
-   **decRound(12345.6789,1)** は、値 **12345.70** を返します。
-   **decRound(12345.6789,-1)** は、値 **12350.00** を返します。

## <a name="exp"></a>exp

指定した実数の値の自然逆対数を取得します。

### <a name="syntax"></a>構文

```xpp
real exp(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                 |
|-----------|-------------------------------------------------------------|
| arg       | ナチュラル逆対数を計算する実数。 |

### <a name="return-value"></a>戻り値

指定した実数の値の自然逆対数を取得します。

### <a name="remarks"></a>備考

計算されたナチュラル逆対数は、*引数* パラメーターによって示されるべき乗した自然対数 e です。

### <a name="example"></a>例

```xpp
static void expExample(Args _arg)
{
    real r1;
    real r2;
    ;
    r1 = exp(2.302585093);
    r2 = exp10(2.302585093);
    print strFmt("exp of 2.302585093 is %1", r1);
    print strFmt("exp10 of 230258 is %1", r2);
    pause;
}
```

## <a name="exp10"></a>exp10
指定した実数の値の常用逆対数を取得します。

### <a name="syntax"></a>構文

```xpp
real exp10(real decimal)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                 |
|-----------|-------------------------------------------------------------|
| decimal   | 10 進数の逆数を計算する実数。 |

### <a name="return-value"></a>戻り値

*decimal* パラメーターの値の 10 から始まる逆対数。

### <a name="example"></a>例

```xpp
static void exp10Example(Args _arg)
{
    real r1;
    real r2;
    ;
    r1 = exp(2.302585093);
    r2 = exp10(2.302585093);
    print strFmt("exp of 2.302585093 is %1", r1);
    print strFmt("exp10 of 230258 is %1", r2);
    pause;
}
```

## <a name="frac"></a>frac
実数の小数部を取得します。

### <a name="syntax"></a>構文

```xpp
real frac(real decimal)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                       |
|-----------|---------------------------------------------------|
| decimal   | 小数部を取得する実数。 |

### <a name="return-value"></a>戻り値

指定した数の小数部分。

### <a name="remarks"></a>備考

**frac(12.345)** は、値 **0.345** を返します。

## <a name="log10"></a>log10
実数の 10 桁の対数を取得します。

### <a name="syntax"></a>構文

```xpp
real log10(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                |
|-----------|--------------------------------------------|
| arg       | 対数を計算する数。 |

### <a name="return-value"></a>戻り値

指定した数の常用対数。

### <a name="remarks"></a>備考

**log10(200)** は、値 **2.30** を返します。

## <a name="logn"></a>logN
指定した実数の値の自然対数を取得します。

### <a name="syntax"></a>構文

```xpp
real logN(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                        |
|-----------|----------------------------------------------------|
| arg       | 自然対数を計算する数。 |

### <a name="return-value"></a>戻り値

指定した数の自然対数。

### <a name="remarks"></a>備考

**logN(45)** は、値 **3.81** を返します。

## <a name="max"></a>最大

2 つの指定した値の大きい方を取得します。

```xpp
anytype max(anytype object1, anytype object2)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明       |
|-----------|-------------------|
| object1   | 最初の値。  |
| object2   | 2 番目の値。 |

### <a name="return-value"></a>戻り値

*object1* および *object2* パラメーターで指定される 2 つの値のうちの大きい方。

### <a name="remarks"></a>備考

-   **最大 (12.0,12.1)** は、値 **12.1** を返します。
-   **最大 (2,33)** は、値 **33** を返します。

## <a name="min"></a>最小

2 つの指定した値の小さい方を取得します。

```xpp
anytype min(anytype object1, anytype object2)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明       |
|-----------|-------------------|
| object1   | 最初の値。  |
| object2   | 2 番目の値。 |

### <a name="return-value"></a>戻り値

*object1* パラメーターおよび *object2* パラメーターで指定される 2 つの値のうちの小さい方。

### <a name="remarks"></a>備考

**最小 (2,33**) は、値 **2** を返します。

### <a name="example"></a>例

```xpp
static void minExample(Args _arg)
{
    anytype a;
    real r = 3.0;
    real s = 2.0;

    a = min(r, s);
    print num2Str(a, 1, 2, 1, 1) + " is less than the other number.";
}
```

## <a name="power"></a>power
実数を別の実数でべき乗します。

### <a name="syntax"></a>構文

```xpp
real power(real arg, real exponent)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                 |
|-----------|-----------------------------------------------------------------------------|
| arg       | 力を計算する数。                                       |
| exponent  | *arg* パラメーターで指定された数値を増やすための数。 |

### <a name="return-value"></a>戻り値

*arg* パラメーターで指定された数の実数は、*exponent* パラメーターで指定された数の累乗になります。

### <a name="remarks"></a>備考

-   **パワー (5.0,2.0)** は、値 **25.0** を返します。
-   **パワー (4.0,0.5)** は、値 **2.0** を返します。

## <a name="round"></a>round
実数は別の実数の最も近い倍数に切り上げられます。

### <a name="syntax"></a>構文

```xpp
real round(real _arg, real _decimals)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                          |
|------------|--------------------------------------------------------------------------------------|
| \_arg      | 元の番号。                                                                 |
| \_小数点以下 | *\_arg* パラメーターの値を倍数に丸める必要がある数。 |

### <a name="return-value"></a>戻り値

*\_decimals* パラメーターで指定された値の倍数で *\_arg* パラメーターで指定された値に最も近い数。

### <a name="remarks"></a>備考

指定した小数点以下の桁数に実数を丸めるには、[decround 関数](/previous-versions/dynamics/ax-2012/reference/aa499511(v=ax.60))を使用します。

### <a name="remarks"></a>備考

-   **丸め (123.45,5.00)** は、値 **125.00** を返します。
-   **丸め (7.45,1.05)** は、値 **7.35** を返します。
-   **丸め (23.9,5.0)** は、値 **25.00** を返します。
-   **丸め (26.1,5.0)** は、値 **25.00** を返します。

## <a name="sin"></a>sin

実数の正弦を取得します。

### <a name="syntax"></a>構文

```xpp
real sin(real _arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                           |
|-----------|---------------------------------------|
| \_arg     | 正弦を計算する数。 |

### <a name="return-value"></a>戻り値

指定した実数のサイン。

### <a name="remarks"></a>備考

パラメーター *\_arg* の値はラジアンにする必要があります。

### <a name="example"></a>例

```xpp
static void sinExample(Args _arg)
{
    real angleDegrees = 15.0;
    real angleRadians;
    real pi = 3.14;
    real r;
    ;
    angleRadians = pi * angleDegrees / 180;
    r = sin(angleRadians);
    print "sin of a "
        + num2Str(angleDegrees, 2, 2, 1, 1)
        + " degree angle is "
        + num2Str(r, 2, 10, 1, 1);
    pause;
}
```

## <a name="sinh"></a>sinh
実数の双曲線正弦を取得します。

### <a name="syntax"></a>構文

```xpp
real sinh(real _arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                      |
|-----------|--------------------------------------------------|
| \_arg     | 双曲線正弦を計算する数。 |

### <a name="return-value"></a>戻り値

指定された実数の双曲線正弦。

### <a name="remarks"></a>備考

-250 から 250 の範囲外の *\_arg* パラメーターの値では、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。

### <a name="example"></a>例

次の例は、**sinh** 関数を示しています。

```xpp
static void sinhExample(Args _arg)
{
    real angleDegrees = 45.0;
    real angleRadians;
    real pi = 3.14;
    real r;
    ;
    angleRadians = pi * angleDegrees / 180;
    r = sinh(angleRadians);
    print "sinh of a "
    + num2Str(angleDegrees, 2, 2, 1, 1)
    + " degree angle is "
    + num2Str(r, 2, 15, 1, 1);
    pause;
}
```

## <a name="tan"></a>tan

実数の正接を取得します。

### <a name="syntax"></a>構文

```xpp
real tan(real arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| arg       | 正接を計算する実数。 |

### <a name="return-value"></a>戻り値

指定した実数の正接。

### <a name="remarks"></a>備考

-250 から 250 の範囲外の *arg* パラメーターの値では、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。

### <a name="example"></a>例

次の例は、**tan** 関数を示しています。

```xpp
static void tanExample(Args _arg)
{
    real r;
    ;
    r = tan(250);
    print strFmt("Tan of 250 is %1", r);
    pause;
}
```

## <a name="tanh"></a>tanh
実数の双曲線正接を取得します。

### <a name="syntax"></a>構文

```xpp
real tanh(real _arg)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                         |
|-----------|-----------------------------------------------------|
| \_arg     | 双曲線正接を計算する数。 |

### <a name="return-value"></a>戻り値

指定された実数の双曲線正接。

### <a name="example"></a>例

次の例は、**tanh** 関数を示しています。

```xpp
static void tanhExample(Args _arg)
{
    real r;
    ;
    r = tanh(0.1);
    print "The hyperbolic tangent of angle 0.1 is "
    + num2Str(r, 2, 10, 1, 1);
    pause;
}
```

## <a name="trunc"></a>trunc
小数点以下を削除して実数を切り捨てます。

### <a name="syntax"></a>構文

```xpp
real trunc(real _decimal)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明             |
|-----------|-------------------------|
| \_小数点以下 | 切り捨て後の数。 |

### <a name="return-value"></a>戻り値

小数点以下桁数が削除された後の *\_decimal* パラメーターの値に等しい番号。

### <a name="remarks"></a>備考

この関数は、常に数値を完全な整数に四捨五入します。

### <a name="example"></a>例

次の例では、2.7147 を 2.00 に切り捨てます。

```xpp
static void truncExample(Args _arg)
{
    real r;
    ;
    r = trunc(2.7147);
    print strFmt("r = %1",  r);
    pause;
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]