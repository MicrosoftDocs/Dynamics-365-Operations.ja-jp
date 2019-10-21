---
title: X++ プリミティブ データ型
description: このトピックでは、X++のプリミティブ データ型について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150183
ms.assetid: 0ff4e759-851d-4b53-aa67-6f03eee53f02
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a12e14ebb7627a3cce29b8f68353ed6d5424af55
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550148"
---
# <a name="x-primitive-data-types"></a>X++ プリミティブ データ型

[!include [banner](../includes/banner.md)]

このトピックでは、X++のプリミティブ データ型について説明します。 X++ のプリミティブ データ型は、**anytype**、**boolean**、**date**、**enum**、**guid**、**int**、**int64**、**real**、**str**、**timeOfDay**、および **utcdatetime** です。

## <a name="anytype"></a>anytype

**anytype** データ型は任意のデータ型のプレースホルダーです。 このタイプの変数は、引数および戻り値としてのみ使用する必要があります。 **anytype** を変数として使用するには、最初に変数に値を割り当てる必要があります。 それ以外の場合、実行時エラーが発生します。 **anytype** 値に割り当てた後、別のデータ型に変換することはできません。 式に **anytype** の変数を使用できますが、通常は引数および戻り値の型として使用されます。 サイズ、精度、有効範囲、既定値、**anytype** の範囲は、割り当てた変換タイプによって異なります。 変換対象のデータ タイプを使用するように、**anytype** を使用することができます。 たとえば、整数を割り当てる場合、変数にリレーショナル演算子と算術演算子を適用できます。 **anytype** 変数は値をタイプに割り当てるとき、日付、列挙 (enum)、整数、実数、文字列、拡張データ型 (EDT) (レコード)、クラス、またはコンテナーを自動的に変換します。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **any2date**、**any2enum**、**any2int**、**any2real**、**any2str**。 **anytype** に変換した後は、変数を別のデータ型に変更することはできません。

### <a name="anytype-examples"></a>anytype 例

    // An example of using anytype variables.
    public static str range(anytype _from, anytype _to)
    {
        return queryValue(_from) + '..' + queryValue(_to);
    }

    // Another example of using anytype variables.
    void put(int position, anytype data)
    {
        record = conPoke (record, position, data);
    }

    public void AnytypeMethod()
    {
        // An example of automatic conversion for anytype.
        anytype a;
        a = "text"; // Automatically assigns a string literal.
    }

## <a name="boolean"></a>ブール値

**ブール** データ型には、**true** または **false** のいずれかとして評価される値が含まれます。 **ブール** 式が予期される場所では、引当済のリテラル キーワード **true** および **false** を使用することができます。 **boolean** のサイズは 1 byte です。 既定値は、**false** で、内部表示は、短い番号です。 **ブール**は、自動的に **int**、**date**、または **real** に変更されます。 明示的な変換関数はありません。 **ブール** の内部テーブル現は整数です。 **ブール値** タイプとして宣言された変数には任意の整数値を割り当てることができます。 整数値 **0** (ゼロ) は **false** と評価され、他のすべての整数値は **true** と評価されます。 **ブール**の内部表示は整数なので、**ブール**値は自動的に整数と実数に変換されます。

### <a name="boolean-examples"></a>ブール値の例

    public void BooleanMethod()
    {
        // Simple declaration of a boolean variable, b.
        boolean b;

        // Multiple declarations of booleans.
        boolean b1, b2;

        // Boolean variable is initialized to true.
        boolean b3 = true;

        // Declares a dynamic array of booleans.
        boolean b4[];

        // This example shows the most common usage of a boolean: a boolean in
        // a conditional statement and as a result of a logical expression.
        void main()
        {
            // Declares a boolean called exprValue.
            boolean exprValue;

            // Assigns ExprValue the value of (7*6 == 42), which equates to true.
            exprValue = (7*6 == 42);

            // If the conditional statement is true, print "OK".
            if (exprValue)
            {
                print "OK";  //"OK" is printed because the expression is true.
            }
        }
    }

## <a name="date"></a>日付

**date** データ型は、年、月、日を格納します。 日付は、次の構文を使用してリテラルとして記述できます。**日付リテラル = 日 \\ 月 \\ 年**。 その年の 4 桁の数字を使用する必要があります。 **日付**データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。 **date** のサイズは 32 ビットです。 既定値は、**null** で、内部表示は、日付です。 **日付**に暗黙的な変換はありません。 ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2date**、 **date2str**、 **date2num**、 **int2date**。 日付に対し、整数を加算または減算することができます。これにより将来の日付または、過去の日付に移動します。 それぞれの日付を減算することにより、差異が日数で計算されます。 ただし、2つの日付を一緒に加算することはできず、コンパイラ エラーの原因になります。

### <a name="date-examples"></a>date の例

    public void DateMethod()
    {
        // Simple declaration of a date variable, d.
       date d;

        // Multiple declaration of two date variables.
        date d1, d2;

        // A date variable, d3, is initialized to the 21st of November 1998.
        date d3 = 21\11\1998;

        // Declaration of a dynamic array of dates.
        date d4[];

        // Using arithmetic operators with integer variables and dates.
        void myMethod()
        {
            int anInteger;
            date aDate;
            // Sets the date variable aDate to January 1, 1998.
            aDate = 1\1\1998;
            // Sets the integer variable anInteger to 30.
            anInteger = 30;
            // Uses an integer value in the computation of dates.
            // This sets aDate to aDate + 30; that is the 31st of January 1998.
            aDate = aDate + anInteger;

            // Create 2 variables, set bDate, and then subtract from that date.
            date bDate;
            int dateDifference;
            bDate = 2\10\1998; 
            dateDifference = bDate - aDate; // dateDifference will equal 244.
        }
    }

## <a name="enum"></a>列挙型

**列挙**はリテラルのリストです。 **列挙**を使用する前に、アプリケーション エクスプローラーで宣言する必要があります。 リテラルの値は、内部的に整数で表されます。 最初のリテラルは数字 0、次のリテラルは 1、次のリテラルは 2 というように続きます。 式の中では **列挙型** の値を整数として使用することができます。 最初のエントリの既定値は、**0** で、内部表示は、短い番号です。 **列挙**値は自動的に**ブール**、**int**、または **real** に変換されます。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **enum2str** および **str2enum**。 百種類の列挙型が標準アプリケーションに組み込まれています。 たとえば、**NoYes** 列挙には関連付けられている 2 つのリテラルがあります: **No** は **0** の値を、および**Yes**は **1** の値です。 必要なだけ列挙型を作成して、最大で 251 (0 ~ 250) のリテラルを単一列挙型で宣言することができます。 **列挙型**の値を参照するには、列挙型の名前、2 つのコロン、およびリテラルの名前を入力します。 たとえば、**NoYes** 列挙でリテラルの **No** を使用するには、**NoYes::No** を入力します。

### <a name="create-an-enum"></a>列挙型を作成する

1.  ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。
2.  **アーティファクト** で、**データ型** を選択します。
3.  **基本列挙**をクリックし、を新しい項目の種類を選択します。
4.  **名前**フィールドに、列挙型の名前を入力してから **OK** をクリックします。 新しい列挙型がプロジェクトに追加され、新しい要素の列挙型デザイナーが開きます。
5.  列挙型デザイナーで、列挙名を右クリックしてから**新しい要素**をクリックします。
6.  **プロパティ** ウィンドウで、列挙要素の名前を入力します。

### <a name="enum-examples"></a>列挙型の例

    public void EnumMethod()
    {
        // Declare the enum (a NoYes enum) in the Application Explorer.
        NoYes done;

        // An array of Criteria enums.
        Criteria crit[100];
    }

## <a name="guid"></a>guid

**guid** データ型は、*グローバルに一意の識別子* (GUID) 値を保持します。 GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる整数です。 数字が重複することはあまりありません。 有効な GUID は、次のすべての仕様を満たします。

-   32 桁の 16 進数が必要です。
-   次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。
-   文字列の先頭と末尾の中かっこ ({}) はオプションです。 たとえば、「12345678-BBBb-cCCCC-0000-123456789012」および「{12345678-BBBb-cCCCC-0000-123456789012}」両方共有効な GUID 文字列です。
-   かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。
-   a 〜 f (または A 〜 F) の 16 進数は、大文字、小文字、または混在することができます。

**guid** のサイズは 16 byte または 128 ビットです。 次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**any2guid**、**guid2str**、**newGuid**、**str2guid**、**Global::guidFromString**、および **Global::stringFromGuid** も使用できます。

### <a name="guid-examples"></a>guid の例

次の例は、**guid** 関数の使い方を示しています。 これらの例のコード出力は次のとおりです。

    // An example of how to use the GUID functions.
    static void GuidRoundTripJob(Args _args)
    {
        guid guid2;
        str string3;

        // Convert a guid to a string, and back to a guid.
        guid2 = newGuid();
        info(strFmt("Info_a1:  guid2 == %1", guid2));
        string3 = guid2str(guid2);
        info(strFmt("Info_a2:  string3 == %1", string3));
        guid2 = str2guid(string3);
        info(strFmt("Info_a3:  guid2 == %1", guid2));

        // Test string representations of a guid. Mixing upper and lower case letters does not affect the guid.
        guid2 = str2guid("BB345678-abcd-ABCD-0000-bbbbffff9012");
        string3 = guid2str(guid2);
        info(strFmt("Info_b1:  8-4-4-4-12 format for dashes works (%1)", string3));
        info(strFmt("Info_b2:  Mixed upper and lower case works."));

        // Test invalid dash locations, see output is all zeros. Dash locations must be exact.
        guid2 = str2guid("CC2345678abcd-ABCD-0000-cccc9012");
        string3 = guid2str(guid2);
        info(strFmt("Info_c1:  These embedded dash locations are required.  %1", string3));

        // Braces {} are optional.
        guid2 = str2guid("{DD345678-abcd-ABCD-0000-ddddaaaa9012}");
        string3 = guid2str(guid2);
        info(strFmt("Info_d1:  Braces {} are optional (%1)", string3));
    }

### <a name="guid-code-output"></a>guid コード出力

次の出力は、情報ログに表示されます。 文字列にはオプションの中かっこが含まれることに注意してください。

    Message (02:26:46 pm)
    Info_a1:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a2:  string3 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a3:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_b1:  8-4-4-4-12 format for dashes works ({BB345678-ABCD-ABCD-0000-BBBBFFFF9012})
    Info_b2:  Mixed upper and lower case works.
    Info_c1:  These embedded dash locations are required.  {00000000-0000-0000-0000-000000000000}
    Info_d1:  Braces {} are optional ({DD345678-ABCD-ABCD-0000-DDDDAAAA9012})

## <a name="int-and-int64"></a>int および int64

*整数*は小数点以下の桁数のない数字です。 **int** および **int64** の、2 つの整数タイプがあります。 整数は、繰り返しのステートメントの制御変数または配列のインデックスとして使用されます。 また、整数式が必要で、リレーショナル演算子と算術演算子の両方を適用することができる任意の場所で *整数リテラル* を使用することができます。 整数リテラルは **32768** のように、コードに直接入力された整数。 **Int** は 32 ビット幅で、**int64** は 64 ビット幅です。 既定値は、**0** で、内部表示は、長い番号です。 整数は自動的に **boolean**、**enum** または **real** に変換されます。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2int**、**int2str**、**str2int64**、**int642str**。 **int** の範囲は \[-2,147,483,647 : 2,147,483,647\]、**int64** の範囲は \[-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808\] です。 全整数はこれらの範囲のいずれかでリテラルとして使用することができます。

### <a name="int-and-int64-examples"></a>int および int64 の例

次の例は、整数を宣言して式で使用する方法を示しています。 **int64** に最大整数プラス 1 を代入しようとすると、数値は 32 ビット数として解釈されるため、間違った結果になります。 したがって、番号は折り返され、代わりに -2,147,483,647 として格納されます。 この問題を防ぐためには、番号の最後に "u" を追加します。 たとえば、**int64 I = 0x8000 0000u** (0x8000 0000 は 2,147,483,648 です) を入力します。

    public void IntegerMethod()
    {
        // Declaration of an integer variable, i.
        int i;

        // Declaration of two int64 variables.
        int64 i1, i2;

        // An integer variable is initialized to the value 100.
        int i3 = 100;

        // Declaration of a dynamic array of integers.
        int i4[];
        void element()
        {
            // Two integer variables are declared and initialized.
            int k = 1, j = 2;

            // j is assigned the result of j + ((i + i) DIV 2).
            j +=(i + i) div 2;

            // This results in: j=3.

            if (j > 2 )
            {
                print "J is greater than 2";
            }
            else
            {
                print "J is NOT greater than 2";
            }
        }
    }

## <a name="real"></a>real

**実数**変数は、整数に加えて小数値を保持できます。 *10 進リテラル* は **実数** が予期される場所ではどこでも使用することができます。 10 進数リテラルは、**2.123876** のように、コードで直接入力された 10 進数です。 実数リテラルは、**1.0e3** などの指数の表記を使用して記述することもできます。 Reals は、すべての式で使用することができ、リレーショナル演算子と算術演算子の両方と共に使用できます。 **実数**は、16桁の有効な数値の精度があります。 **real** の既定値は **0.0** で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。 BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。 **実数** 変数の範囲は、-(10)¹²⁷ から (10)¹²⁷ です。 この範囲内のすべての実数は X++ でリテラルとして使用できます。 **実数**変数は、自動的に**ブール**、**enum**、または **int** に変換されます。結果が整数の場合、または演算子が整数演算子の場合には、**実数**は整数に変換されます。 結果が**ブール値**である場合、**実数**が**ブール値**に変換されたりします。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2num**、**num2str**。 X++ **実数** と Microsoft .NET Framework **System.Decimal** 間の直接割り当てによって、値が正しく変換されます。 換算関数を呼び出す必要はありません。 *10 進数*は、符号、0 から 9 の範囲内の数値、および数値の整数と小数点以下を区切る浮動小数点の位置を表すスケーリング係数で構成される浮動小数点値です。 **実数**値のバイナリ表現は、1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。 拡大縮小係数は、96 ビット整数を分割し、小数部の部分を指定するのに使用されます。 拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。 したがって、10 進数のバイナリ表現は (\[-2⁹⁶ ～ 2⁹⁶\] ÷ 10(0\\ ～\\ 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値になります。 **注記:** Finance and Operations アプリケーションで**実数**値を表すために使用されるタイプは、変換された Microsoft Dynamics AX 2012 の X++ から変更されています。 ただし、新しいタイプは、古いタイプが表すことができるすべての値を表すことができるので、コードを書き直す必要はありません。 完全な開示のためにこの材料を提供します。 **実数**タイプのすべてのインスタンスが .NET 小数タイプ (**System.Decimal**) のインスタンスとして実装されます。 以前のバージョンでの **real** 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は丸め誤差に対する対応力があります。 以前のバージョンと異なる 10 進型の範囲と解像度。 元の X++ **実数** 型は 16 桁と小数点の位置を定義した指数をサポートしていました。 ただし、Finance and Operations アプリケーションの**実数**タイプは 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から -79,228,162,514,264,337,593,543,950,335 (-\[2⁹⁶-1\]) の範囲の 10 進数を表します。 新しい**実数**タイプにはさらに丸めが必要です。 たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。 1/3 の値を正確に表せる小数点以下の桁数はありません。 ここで得られる不一致は、有限数の小数しか提供されないことによるものです。 必要な小数点以下の桁数まで丸めるには、**round** 関数を使用します。

    // An example of using the debugger to show the value of the variables.
    public static void UseTheDebugger(Args a)
    {
        real dividend = 1.0;
        real divisor = 3.0;
        str stringvalue;
        System.Decimal valueAsDecimal;
        real value = dividend/divisor * divisor; 
        valueAsDecimal = value;
        info(valueAsDecimal.ToString("G28"));
        // An example of using the Round function to round to the number of decimals required.
        value  = round(value, 2);
    }

### <a name="real-examples"></a>real の例

    public void RealMethod()
    {
        // Simple declaration of a real variable, r.
        real r;

        // Multiple declaration of two real variables.
        real r1, r2;

        // A real variable is initialized to the approximate value of pi.
        real r3 = 3.1415;

        // Declaration of a dynamic array of reals.
        real r4[];

        // An example of a real literal written using exponential notation.
        real r;
        r = 1.000e3;
        r = 1.2345e+3;
        r = 1.2345e+03;
        r = 1234.5e4;
        r = 1.0e1; // Means 1.0E1 
    }

    // An example of automatic conversions.
    void main()
    {
        // Declares a variable of type integer with the name exprValue.
        int exprValue;

        // Declares a real variable with the name area.
        real area = 3.141528;
        exprValue = Area/3;

        // The expression Area/3 is a real expression because
        // division is a real operator, and the result is 1.047176. This result is
        // automatically converted (actually truncated) to an integer with the value 1,
        // because exprValue is an integer.
    }

    // An example of a real being converted to .NET System.Decimal.
    void AnotherMain(Args _args)
    {
        real real9;
        System.Decimal sysdec1;

        // Direct assignments supported between these types.
        sysdec1 = 2.3456;
        real9 = sysdec1;
        info(strFmt("strFmt says real9 == %1", real9));
    }

    /***
    Message (05:48:43 pm)
    strFmt says real9 == 2.35
    ***/

    // An example of using reals in expressions.
    void myMethod()
    {
        // Two real variables are declared and initialized.
        real i = 2.5, j = 2.5;

        // j is assigned the result of j * i, so j=6.25.
        j = j * i;
        if (j > (i * 2)) // If j > 5 
        {
            print "Great"; // "Great" is printed.
        }
        else
        {
           print "Oops"; // else "Oops" is printed.
        }
    }

## <a name="str"></a>str

**str** 変数 (*文字列*) は、テキスト、ヘルプ行、住所、電話番号などとして使用される文字の並びです。 文字列を宣言するには、**str** キーワードを使用します。 *文字列リテラル*引用符 ("") で囲まれた文字です。 文字列式が必要な場合はいつでも、文字列リテラルを使用することができます。 文字列リテラルの例には、「StringLit」および「Hello World」が含まれます。 文字列を複数の行にまたがるようにするには、その前にアットマーク (@) を付けます。 比較などの論理式では文字列を使用することができます。 また、+ 演算子を使用することで文字列を連結することができます。 文字列の既定値は **空**で、内部表示は文字のリストです。 文字列の自動変換はありません。 ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2int**、**str2int64**、**int2str**、**str2num**、**num2str**、**str2date**、および **date2str**。 文字列は、無制限の文字数を保持できます。 ただし、変数の宣言で文字列の最大の長さを指定できます。 文字列はその最大長に切り捨てられます。 例として次のセクションに表示します。

### <a name="str-examples"></a>str の例

    void StringMethod()
    {
        // Declare a dynamic string of unlimited length.
        str unlimitedString;

        // Declare a string with a maximum of 64 characters
        // in order to force a truncation, initialized to "A".
        str 64 maxLengthString = "A";

        // Declare an array of 100 strings.
       str 30 hundredStrings[100];

        // Using strings in expressions.
        void myMethod()
        {
            // Two strings are declared and initialized.
            str a="Hello", b="World";

            // The concatenation of a, " " and b is printed in a window.
            print a+" "+b;
        }
    }

## <a name="timeofday"></a>timeOfDay

**timeOfDay** (時間) データ型は、午前 0 時から経過した秒数を表す整数値です。 整数と同様に、**timeOfDay** 変数はリテラルとして使用することができます。 リレーショナルおよび算術演算子は、**timeOfDay** 変数に適用できます。 **timeOfDay** 変数も式で使用できます。 **timeOfDay** データ型の範囲は \[0;86,400\] のクローズ区間にあります。 86,400 (23: 59:59) を超える値は解釈できません。 **timeOfDay** 変数は、自動的に**ブール**、**enum**、または**実数**に変換されます。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2time**、**time2str**。

### <a name="timeofday-examples"></a>timeOfDay の例

    public void TimeofdayMethod()
    {
        // Declaration of a timeOfDay variable, time1.
        timeOfDay time1;

        // Declaration and initialization of a timeOfDay variable to 00:21:35.
        timeOfDay time2 = 1295;
    }

## <a name="utcdatetime"></a>utcdatetime

**utcdatetime** データ型は、**date** 型と **timeOfDay** 型を結合します。 **utcdatetime** 変数には、タイム ゾーンに関する情報も含まれています。 ただし、この情報はコードではアクセスできません。 **utcdatetime** リテラルの形式は、**yyyy-mm-ddThh:mm:ss** です。 大文字「T」が必要です。 この形式は引用符を使用せずに記述できます。 最小値は、**1900-01-01T00:00:00** で、最大値は **1900-01-01T00:00:00** です。 この最大値は、**date** と **timeOfDay** の上位範囲に一致します。 **utcdatetime** の最小単位は 1 秒です。 宣言されているもののまた初期化されていない **utcdatetime** 変数の規定値は、 **1900-01-01T00:00:00** です。 この値は、**DateTimeUtil::minValue()** によって返される値です。 一部の機能は、この最小値の入力パラメーターを **null** として扱います。 たとえば、**DateTimeUtil::toStr** メソッドは、空の文字列を返します。 ただし、**DateTimeUtil::addSeconds** メソッドは使用可能な **utcdatetime** 値を返します。 **utcdatetime** データ型の暗黙的な変換はありません。 **DateTimeUtil** クラスは、**utcdatetime** 値を操作するために使用できるさまざまなメソッドを提供します。 次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**str2datetime** および **datetime2str** も使用できます。 また、**グローバル** クラスは、**utcDateTime2SystemDateTime** と **CLRSystemDateTime2UtcDateTime** 変換メソッドを提供して、共通言語ランタイム (CLR) 相互運用をサポートします。 比較演算子は、**utcdatetime** データ型で使用できる唯一の演算子です。 次の演算子を使用して、2つの **utcdatetime** 値を比較することができます: !=、&lt;、&lt;=、==、&gt;、および &gt;=。 テーブルに **utcdatetime** フィールドを追加するときは、そのフィールドを EDT にもとづいて決めることをお勧めします。

### <a name="utcdatetime-examples"></a>utcdatetime の例

    public void UtcdatetimeMethod()
    {
        // Declaring a utcdatetime literal.
        utcdatetime myUtc2 = 1988-07-20T13:34:45;

        // Another example of declaring a utcdatetime literal.
        int iDay = DateTimeUtil::day(1988-07-20T13:34:45);

        // utcdatetime using a quoted string parameter into the DateTimeUtil::parse method.
        utcdatetime myUtc4 = DateTimeUtil::parse("1988-07-20T13:34:45");
    }
