---
title: X++ の変数とデータ型
description: このトピックでは、X++ の変数とデータ型について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150183
ms.assetid: 0ff4e759-851d-4b53-aa67-6f03eee53f02
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e85c80b92b160fc07beee0609659a3291eff7ce
ms.sourcegitcommit: 3be8d2be6474264f0a530a052d19ea2635e269cf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/08/2019
ms.locfileid: "1729892"
---
# <a name="x-variables-and-data-types"></a>X++ の変数とデータ型

[!include [banner](../includes/banner.md)]

このトピックでは、X++ の変数とデータ型について説明します。

<a name="variables"></a>変数
---------

*変数*は、特定のデータ型の情報が格納されているメモリ位置を示す識別子です。 サイズ、精度、既定値、暗黙的および明示的[変換](xpp-conversion-run-time-functions.md)関数、範囲は、変数のデータ型によって異なります。 変数の*スコープ*は、項目にアクセスできるコード内の領域を定義します。 *インスタンス変数*はクラス宣言で宣言され、クラス内の任意のメソッドからまたは拡張クラスのメソッドからアクセスできます。 *ローカル変数*は定義されたブロック内でのみアクセスできます。 変数が宣言されると、メモリが割り当てられ、その変数が既定値に初期化されます。 静的フィールドおよびインスタンス フィールドの両方に、値を declaration ステートメントの一部として割り当てることができます。 変数は、メソッドのコード ブロック内の任意の場所で宣言できます。 これらは、メソッドの先頭で宣言される必要はありません。 *定数*は、変数が宣言されたときに値を変更できない変数です。 **const** キーワードまたは **readonly** キーワードを使用します。 定数は 1 つの方法で*読み取り専用のフィールド*とは異なります。 読み取り専用フィールドには値を 1 回だけ割り当てることができ、その値は変わりません。 フィールドには、フィールドが宣言されている場所、またはコンストラクターのいずれかでインラインで値を割り当てることができます。 X++ で作成されていないマネージ型の変数を宣言するときは、2 つのオプションがあります。 完全な名前空間を含めることにより宣言内のタイプ名を完全に修飾、または **using** ステートメントをファイルに追加してから名前空間をタイプ名から省略することができます。

### <a name="variable-examples"></a>変数の例

    // An example of two valid variable names.
    str variableName;
    CustInfo custNumber;

    // An example of simultaneously declaring and initializing a variable.
    real pi = 3.14159265359; // Assigns value of pi to 12 significant digits.

    // An example of initializing an object by using the new method on the class.
    Access accessObject = new Access(); // Simple call to the new method in the Access class.

    // An example of multiple declarations using integers.
    int i,j; // Declares 2 integers, i and j.

    // An example of multiple declarations using an array.
    int a[100,5], b=1; // Declares array with 100 integers with 5 in memory and b as an integer with value 1.

    // An example of how variable scopes work.
    class ScopeExample
    {
        // The variable a is declared within the class.
        int a;

        // Because the method below is declared within the class,
        // it can access all the variables defined within the class.
        void aNewMethod()
        {
            // The variable b is declared within the method.
            // It can only be accessed by this method.
            int b;
        }
    }

    // An example of an assignment of field members inline.
    public class FieldAssignmentExample
    {
        int field1 = 1;
        str field2 = "Banana";
        void new()
        {
            // ...
        }
    }

    class ConstantExample
    {
        // An example of a constant being declared at the class level.
        public const str MyContent = 'SomeValue';
        public int ResultSoFar()
        {
            return 1;
        }
    }

    // The constants can then be referenced by using the double-colon syntax.
    str value = ConstantExample::MyContent;
    // If you're in the scope of the class where the const is defined, 
    // you can omit the type name prefix (ConstantExample in this example).

    // An example of the using clause where the alias can denote
    // namespaces and classes.
    using System;
    using IONS=System.IO; // Namespace alias.
    using Alist=System.Collections.ArrayList; // Class alias.
    public class NamespaceExample
    {
        public static void Main(Args a)
        {
            Int32 I; // Alternative to System.Int32.
            Alist al; // Using a class alias.
            al = new Alist();
            str s;
            al.Add(1);
            IONS.Path::ChangeExtension(@"c:\tmp\test.xml", ".txt");
        }
    }

### <a name="var"></a>var

コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができます。 変数は、まだ厳密に型指定されている明確な型です。 **var** は初期化式が提供されている宣言でのみ使用することができます。 (コンパイラは、初期化式から種類を推定します。) 場合によっては、この方法によって、コードが読みやすくなります。 こうした状況でローカル変数を宣言するには、**var** を使用してください。

-   変数の型が右側の割り当てから明らかなとき
-   正確な型が重要でないとき
-   ループ カウンター**用**の申告について
-   **using** ステートメント内での破棄可能なオブジェクト対象

種類が初期化式からクリアされていない際は、**var** を使用しないでください。

### <a name="var-examples"></a>var の例

    // When the type of a variable is clear from
    // the context, use var in the declaration.
    var var1 = "This is clearly a string.";
    var var2 = 27; // This is an integer (not a real).
    var i = System.Convert::ToInt32(3.4);

    // Don't use var when the type of the variable is not clear
    // from the context. Use an explicit type instead.
    int var4 = myObject.ResultSoFar();

### <a name="declare-anywhere"></a>任意の場所で宣言

ステートメントを提供できる場所に宣言を提供できるようになりました。 宣言は、構文的にはステートメントで、*宣言ステートメント*です。 変数は使用される直前に宣言することができます。すべての変数を 1 つの場所で宣言する必要はありません。 したがって、変数のスコープを正確に制御できます。 変数を参照することができない場所で、変数に小さなスコープを付与することができます。 変数の有効期間は宣言されているスコープです。 スコープは、**for** ステートメントおよび **using** ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。 スコープを小さくすることにはいくつかの利点があります。

-   読みやすさが向上しました。
-   コードの長期保守中に変数が不適切な方法で再利用されるリスクを軽減します。
-   コードをリファクターすることがより簡単です。 再使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。

次の例では、使用される **for** ステートメント内のループ カウンターを宣言します。

    void MyMethod()
    {
        for (int i = 0; i < 10; i++)
        {
            info(strfmt("i is %1", i));
        }
    }

変数のスコープは **for** ステートメントそのものであり、条件式とループ更新部分を含みます。 この範囲外で値を使用することはできません。 次の例では、コンパイラが **info** ステートメントに達すると、「'i' が宣言されていません」というエラー メッセージを発行します。

    void MyMethod()
    {
        for (int i = 0; i < 10; i++)
        {
            if (i == 7)
            {
                break;
            }
        }
        // The next statement causes a compiler error.
        info(strfmt("Found: %1", i));
    }

また、以下の例に示されるように、変数を **using** ステートメントにスコープすることができます。

    static void AnotherMethod()
    {
        str textFromFile;
        using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
        {
            textFromFile = sr.ReadToEnd();
        }
    }

**IDisposable** を実装するオブジェクトを使用するときは、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。 **using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。 オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。 実際、コンパイラはこの方法だけで **using** ステートメントを変換します。 次の例は、説明してきた機能のいくつかを示しています。

    // loop variable declared within the loop: It will
    // not be misused outside the loop
    for(int i = 1; i < 10; i++)
    {
        // Because this value is not used from outside the loop,
        // its declaration belongs in this smaller scope.
        str s = int2str(i);
        info(s);
    }

混乱を避けるために、コンパイラは囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラー メッセージを発行します。 たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります: 「i と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している i が別の意味になってしまうためです。」

    {
        int i;
        {
            int i;
        }
    }

### <a name="constants-read-only-variables-and-macros"></a>定数、読み取り専用変数、およびマクロ

マクロの概念は完全にサポートされています。 ただし、定数にはマクロに比べて次のような利点があります。

-   ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。 最終的に、言語サービスはこのコメントを受け取り、ユーザーに有用な情報を提供します。
-   定数は、IntelliSense で知られています。
-   定数は、相互参照です。 したがって、マクロではなく、特定の定数のすべての参照を見つけることができます。
-   定数は、アクセス修飾子が適用されます。 **private**、**protected**、および **public** モディファイアを使用することができます。 マクロのアクセシビリティが厳密に定義されていません。
-   定数変数にはスコープがありますが、マクロにはスコープがありません。
-   デバッガーには定数の値または読み取り専用変数を表示することができます。

クラス スコープ (つまりクラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。 この機能は元はレガシ コンパイラ マクロの実装におけるバグでした。 ただし、多くのアプリケーション プログラマが多くの場合それを活用できるようになりました。 X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。 この機能は、コンパイラのパフォーマンスにも大きな影響を与えます。 次の例に示すように、定数はクラス レベルで宣言できます。

    private const str MyConstant = 'SomeValue';

次に、定数を二重コロン (::) 構文を使用して参照することができます。

    str value = MyClass::MyConstant;

定数 (**const**) が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では **MyClass**) を省略できます。 したがって、マクロ ライブラリの概念を簡単に実装することができます。 マクロ シンボルのリストは、パブリック **const** の定義を持つクラスになります。 また、定数を変数のみとして定義することができます。 コンパイラはインバリアントを維持して、値を変更できないようにします。

    {
        const int Blue = 0x0000FF;
        const int Green = 0x00FF00;
        const int Red = 0xFF0000;
    }

## <a name="primitive-data-types"></a>プリミティブ データ型
X++ のプリミティブ データ型は、**anytype**、**boolean**、**date**、**enum**、**guid**、**int**、**int64**、**real**、**str**、**timeOfDay**、および **utcdatetime** です。

### <a name="anytype"></a>anytype

**anytype** データ型は任意のデータ型のプレースホルダーです。 このタイプの変数は、引数および戻り値としてのみ使用する必要があります。 **anytype** を変数として使用するには、最初に変数に値を割り当てる必要があります。 それ以外の場合、実行時エラーが発生します。 **anytype** 値に割り当てた後、別のデータ型に変換することはできません。 式に **anytype** の変数を使用できますが、通常は引数および戻り値の型として使用されます。 サイズ、精度、有効範囲、既定値、**anytype** の範囲は、割り当てた変換タイプによって異なります。 変換対象のデータ タイプを使用するように、**anytype** を使用することができます。 たとえば、整数を割り当てる場合、変数にリレーショナル演算子と算術演算子を適用できます。 **anytype** 変数は値をタイプに割り当てるとき、日付、列挙 (enum)、整数、実数、文字列、拡張データ型 (EDT) (レコード)、クラス、またはコンテナーを自動的に変換します。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **any2date**、**any2enum**、**any2int**、**any2real**、**any2str**。 **anytype** に変換した後は、変数を別のデータ型に変更することはできません。

#### <a name="anytype-examples"></a>anytype 例

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

### <a name="boolean"></a>ブール値

**ブール** データ型には、**true** または **false** のいずれかとして評価される値が含まれます。 **ブール** 式が予期される場所では、引当済のリテラル キーワード **true** および **false** を使用することができます。 **boolean** のサイズは 1 byte です。 既定値は、**false** で、内部表示は、短い番号です。 **ブール**は、自動的に **int**、**date**、または **real** に変更されます。 明示的な変換関数はありません。 **ブール** の内部テーブル現は整数です。 **ブール値** タイプとして宣言された変数には任意の整数値を割り当てることができます。 整数値 **0** (ゼロ) は **false** と評価され、他のすべての整数値は **true** と評価されます。 **ブール**の内部表示は整数なので、**ブール**値は自動的に整数と実数に変換されます。

#### <a name="boolean-examples"></a>ブール値の例

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

### <a name="date"></a>日付

**date** データ型は、年、月、日を格納します。 日付は、次の構文を使用してリテラルとして記述できます。**日付リテラル = 日 \\ 月 \\ 年**。 その年の 4 桁の数字を使用する必要があります。 **日付**データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。 **date** のサイズは 32 ビットです。 既定値は、**null** で、内部表示は、日付です。 **日付**に暗黙的な変換はありません。 ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2date**、 **date2str**、 **date2num**、 **int2date**。 日付に対し、整数を加算または減算することができます。これにより将来の日付または、過去の日付に移動します。 それぞれの日付を減算することにより、差異が日数で計算されます。 ただし、2つの日付を一緒に加算することはできず、コンパイラ エラーの原因になります。

#### <a name="date-examples"></a>date の例

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

### <a name="enum"></a>列挙型

**列挙**はリテラルのリストです。 **列挙**を使用する前に、アプリケーション エクスプローラーで宣言する必要があります。 リテラルの値は、内部的に整数で表されます。 最初のリテラルは数字 0、次のリテラルは 1、次のリテラルは 2 というように続きます。 式の中では **列挙型** の値を整数として使用することができます。 最初のエントリの既定値は、**0** で、内部表示は、短い番号です。 **列挙**値は自動的に**ブール**、**int**、または **real** に変換されます。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **enum2str** および **str2enum**。 百種類の列挙型が標準アプリケーションに組み込まれています。 たとえば、**NoYes** 列挙には関連付けられている 2 つのリテラルがあります: **No** は **0** の値を、および**Yes**は **1** の値です。 必要なだけ列挙型を作成して、最大で 251 (0 ~ 250) のリテラルを単一列挙型で宣言することができます。 **列挙型**の値を参照するには、列挙型の名前、2 つのコロン、およびリテラルの名前を入力します。 たとえば、**NoYes** 列挙でリテラルの **No** を使用するには、**NoYes::No** を入力します。

#### <a name="create-an-enum"></a>列挙型を作成する

1.  ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。
2.  **アーティファクト** で、**データ型** を選択します。
3.  **基本列挙**をクリックし、を新しい項目の種類を選択します。
4.  **名前**フィールドに、列挙型の名前を入力してから **OK** をクリックします。 新しい列挙型がプロジェクトに追加され、新しい要素の列挙型デザイナーが開きます。
5.  列挙型デザイナーで、列挙名を右クリックしてから**新しい要素**をクリックします。
6.  **プロパティ** ウィンドウで、列挙要素の名前を入力します。

#### <a name="enum-examples"></a>列挙型の例

    public void EnumMethod()
    {
        // Declare the enum (a NoYes enum) in the Application Explorer.
        NoYes done;

        // An array of Criteria enums.
        Criteria crit[100];
    }

### <a name="guid"></a>guid

**guid** データ型は、*グローバルに一意の識別子* (GUID) 値を保持します。 GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる整数です。 数字が重複することはあまりありません。 有効な GUID は、次のすべての仕様を満たします。

-   32 桁の 16 進数が必要です。
-   次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。
-   文字列の先頭と末尾の中かっこ ({}) はオプションです。 たとえば、「12345678-BBBb-cCCCC-0000-123456789012」および「{12345678-BBBb-cCCCC-0000-123456789012}」両方共有効な GUID 文字列です。
-   かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。
-   a 〜 f (または A 〜 F) の 16 進数は、大文字、小文字、または混在することができます。

**guid** のサイズは 16 byte または 128 ビットです。 次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**any2guid**、**guid2str**、**newGuid**、**str2guid**、**Global::guidFromString**、および **Global::stringFromGuid** も使用できます。

#### <a name="guid-examples"></a>guid の例

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

#### <a name="guid-code-output"></a>guid コード出力

次の出力は、情報ログに表示されます。 文字列にはオプションの中かっこが含まれることに注意してください。

    Message (02:26:46 pm)
    Info_a1:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a2:  string3 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a3:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_b1:  8-4-4-4-12 format for dashes works ({BB345678-ABCD-ABCD-0000-BBBBFFFF9012})
    Info_b2:  Mixed upper and lower case works.
    Info_c1:  These embedded dash locations are required.  {00000000-0000-0000-0000-000000000000}
    Info_d1:  Braces {} are optional ({DD345678-ABCD-ABCD-0000-DDDDAAAA9012})

### <a name="int-and-int64"></a>int および int64

*整数*は小数点以下の桁数のない数字です。 **int** および **int64** の、2 つの整数タイプがあります。 整数は、繰り返しのステートメントの制御変数または配列のインデックスとして使用されます。 また、整数式が必要で、リレーショナル演算子と算術演算子の両方を適用することができる任意の場所で *整数リテラル* を使用することができます。 整数リテラルは **32768** のように、コードに直接入力された整数。 **Int** は 32 ビット幅で、**int64** は 64 ビット幅です。 既定値は、**0** で、内部表示は、長い番号です。 整数は自動的に **boolean**、**enum** または **real** に変換されます。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2int**、**int2str**、**str2int64**、**int642str**。 **int** の範囲は \[-2,147,483,647 : 2,147,483,647\]、**int64** の範囲は \[-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808\] です。 全整数はこれらの範囲のいずれかでリテラルとして使用することができます。

#### <a name="int-and-int64-examples"></a>int および int64 の例

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

### <a name="real"></a>real

**実数**変数は、整数に加えて小数値を保持できます。 *10 進リテラル* は **実数** が予期される場所ではどこでも使用することができます。 10 進数リテラルは、**2.123876** のように、コードで直接入力された 10 進数です。 実数リテラルは、**1.0e3** などの指数の表記を使用して記述することもできます。 Reals は、すべての式で使用することができ、リレーショナル演算子と算術演算子の両方と共に使用できます。 **実数**は、16桁の有効な数値の精度があります。 **real** の既定値は **0.0** で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。 BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。 **実数** 変数の範囲は、-(10)¹²⁷ から (10)¹²⁷ です。 この範囲内のすべての実数は X++ でリテラルとして使用できます。 **実数**変数は、自動的に**ブール**、**enum**、または **int** に変換されます。結果が整数の場合、または演算子が整数演算子の場合には、**実数**は整数に変換されます。 結果が**ブール値**である場合、**実数**が**ブール値**に変換されたりします。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2num**、**num2str**。 X++ **実数** と Microsoft .NET Framework **System.Decimal** 間の直接割り当てによって、値が正しく変換されます。 換算関数を呼び出す必要はありません。 *10 進数*は、符号、0 から 9 の範囲内の数値、および数値の整数と小数点以下を区切る浮動小数点の位置を表すスケーリング係数で構成される浮動小数点値です。 **実数**値のバイナリ表現は、1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。 拡大縮小係数は、96 ビット整数を分割し、小数部の部分を指定するのに使用されます。 拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。 したがって、10 進数のバイナリ表現は (\[-2⁹⁶ ～ 2⁹⁶\] ÷ 10(0\\ ～\\ 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値になります。 **注記:** Microsoft Dynamics 365 for Finance and Operations で**実数**値を表すために使用されるタイプは、変換された Microsoft Dynamics AX 2012 の X++ から変更されています。 ただし、新しいタイプは、古いタイプが表すことができるすべての値を表すことができるので、コードを書き直す必要はありません。 完全な開示のためにこの材料を提供します。 **実数**タイプのすべてのインスタンスが .NET 小数タイプ (**System.Decimal**) のインスタンスとして実装されます。 以前のバージョンでの **real** 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は丸め誤差に対する対応力があります。 以前のバージョンと異なる 10 進型の範囲と解像度。 元の X++ **実数** 型は 16 桁と小数点の位置を定義した指数をサポートしていました。 ただし、Microsoft Dynamics 365 for Finance and Operations 以降の X++ **実数**タイプは 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から -79,228,162,514,264,337,593,543,950,335 (-\[2⁹⁶-1\]) の範囲の 10 進数を表します。 新しい**実数**タイプにはさらに丸めが必要です。 たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。 1/3 の値を正確に表せる小数点以下の桁数はありません。 ここで得られる不一致は、有限数の小数しか提供されないことによるものです。 必要な小数点以下の桁数まで丸めるには、**round** 関数を使用します。

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

#### <a name="real-examples"></a>real の例

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

### <a name="str"></a>str

**str** 変数 (*文字列*) は、テキスト、ヘルプ行、住所、電話番号などとして使用される文字の並びです。 文字列を宣言するには、**str** キーワードを使用します。 *文字列リテラル*引用符 ("") で囲まれた文字です。 文字列式が必要な場合はいつでも、文字列リテラルを使用することができます。 文字列リテラルの例には、「StringLit」および「Hello World」が含まれます。 文字列を複数の行にまたがるようにするには、その前にアットマーク (@) を付けます。 比較などの論理式では文字列を使用することができます。 また、+ 演算子を使用することで文字列を連結することができます。 文字列の既定値は **空**で、内部表示は文字のリストです。 文字列の自動変換はありません。 ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2int**、**str2int64**、**int2str**、**str2num**、**num2str**、**str2date**、および **date2str**。 文字列は、無制限の文字数を保持できます。 ただし、変数の宣言で文字列の最大の長さを指定できます。 文字列はその最大長に切り捨てられます。 例として次のセクションに表示します。

#### <a name="str-examples"></a>str の例

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

### <a name="timeofday"></a>timeOfDay

**timeOfDay** (時間) データ型は、午前 0 時から経過した秒数を表す整数値です。 整数と同様に、**timeOfDay** 変数はリテラルとして使用することができます。 リレーショナルおよび算術演算子は、**timeOfDay** 変数に適用できます。 **timeOfDay** 変数も式で使用できます。 **timeOfDay** データ型の範囲は \[0;86,400\] のクローズ区間にあります。 86,400 (23: 59:59) を超える値は解釈できません。 **timeOfDay** 変数は、自動的に**ブール**、**enum**、または**実数**に変換されます。 また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2time**、**time2str**。

#### <a name="timeofday-examples"></a>timeOfDay の例

    public void TimeofdayMethod()
    {
        // Declaration of a timeOfDay variable, time1.
        timeOfDay time1;

        // Declaration and initialization of a timeOfDay variable to 00:21:35.
        timeOfDay time2 = 1295;
    }

### <a name="utcdatetime"></a>utcdatetime

**utcdatetime** データ型は、**date** 型と **timeOfDay** 型を結合します。 **utcdatetime** 変数には、タイム ゾーンに関する情報も含まれています。 ただし、この情報はコードではアクセスできません。 **utcdatetime** リテラルの形式は、**yyyy-mm-ddThh:mm:ss** です。 大文字「T」が必要です。 この形式は引用符を使用せずに記述できます。 最小値は、**1900-01-01T00:00:00** で、最大値は **2154-12-31T23:59:59** です。 この最大値は、**date** と **timeOfDay** の上位範囲に一致します。 **utcdatetime** の最小単位は 1 秒です。 宣言されているもののまた初期化されていない **utcdatetime** 変数の規定値は、 **1900-01-01T00:00:00** です。 この値は、**DateTimeUtil::minValue()** によって返される値です。 一部の機能は、この最小値の入力パラメーターを **null** として扱います。 たとえば、**DateTimeUtil::toStr** メソッドは、空の文字列を返します。 ただし、**DateTimeUtil::addSeconds** メソッドは使用可能な **utcdatetime** 値を返します。 **utcdatetime** データ型の暗黙的な変換はありません。 **DateTimeUtil** クラスは、**utcdatetime** 値を操作するために使用できるさまざまなメソッドを提供します。 次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**str2datetime** および **datetime2str** も使用できます。 また、**グローバル** クラスは、**utcDateTime2SystemDateTime** と **CLRSystemDateTime2UtcDateTime** 変換メソッドを提供して、共通言語ランタイム (CLR) 相互運用をサポートします。 比較演算子は、**utcdatetime** データ型で使用できる唯一の演算子です。 次の演算子を使用して、2つの **utcdatetime** 値を比較することができます: !=、&lt;、&lt;=、==、&gt;、および &gt;=。 テーブルに **utcdatetime** フィールドを追加するときは、そのフィールドを EDT にもとづいて決めることをお勧めします。

#### <a name="utcdatetime-examples"></a>utcdatetime の例

    public void UtcdatetimeMethod()
    {
        // Declaring a utcdatetime literal.
        utcdatetime myUtc2 = 1988-07-20T13:34:45;

        // Another example of declaring a utcdatetime literal.
        int iDay = DateTimeUtil::day(1988-07-20T13:34:45);

        // utcdatetime using a quoted string parameter into the DateTimeUtil::parse method.
        utcdatetime myUtc4 = DateTimeUtil::parse("1988-07-20T13:34:45");
    }

## <a name="composite-data-types"></a>複合データ型
X++ の複合データ型は、配列、コンテナー、データ型としてのクラス、データ型としてのデリゲート、データ型としてのテーブルです。

### <a name="array"></a>配列

*配列*は同じデータ型を持つ項目のリストを含む変数です。 配列の要素は、整数インデックスを使用してアクセスされます。 配列内の各要素を初期化するには、別のステートメントを使用します。 コンテナー データ型または配列オブジェクトを使用してコレクションを作成するとき、1 つのステートメントを使用して複数の要素を初期化できます。 既定では、配列内のすべての項目は配列のデータ型の既定値を持ちます。 *動的配列*、*固定長配列*、*ディスク配列の一部*の 3 種類の配列があります。

-   **動的配列** - これらの配列は、空の配列オプションを使用して宣言されます。 つまり、かっこ (\[\]) だけがあります。
-   **固定長の配列** – これらの配列は、宣言で指定されている品目の数を保持できます。 固定長の配列は動的配列と宣言されますが、かっこ内に長さのオプションが含まれます。
-   **ディスク配列の一部** – これらの配列は、動的配列または固定長の配列として宣言され、メモリに保持する品目の数を宣言するオプションが追加されています。 他の項目はディスクに保存され、参照されると自動的に読み込まれます。

X++ は1次元配列のみをサポートしています。 ただし、複数の配列インデックスの動作を再現することができます。 (詳細については、「複数の配列インデックス」セクションを参照してください)。 オブジェクトとテーブル内の変数は配列として宣言することができます。 たとえば、この機能は、標準アプリケーションの住所明細行で使用されます。 配列コレクション クラスを配列内のオブジェクトに格納できます。 配列インデックスは 1 から開始されます。 配列の最初の項目は \[1\] で参照され、2番目の項目は、 \[2\] などで参照されます。 次の構文は、配列要素にアクセスするために使用されます: **ArrayItemReference = ArrayVariable \[ Index \]**。 この構文では、**ArrayVariable** は配列の識別子であり、**Index** は配列要素の数です。 **インデックス**には整数式を指定できます。 項目ゼロ \[0\] は配列をクリアするために使用します。 値が配列のインデックス 0 に割り当てられている場合は、配列内のすべての要素が既定値にリセットされます。

#### <a name="array-examples"></a>配列の例

    public void ArrayMethod()
    {
        int myArray[10]; // Fixed-length array with 10 integers.
        myArray[4] = 1; // Accessing the 4th element in the array.
        myArray[0] = 0; // Resets all elements in intArray. 

        // Dynamic array of integers.
        int intArray[];

        // Dynamic array of variables of type Datatype.
        //Datatype arrayVariable[];

        // Fixed-length arrays.
        boolean boolArray[100]; // Fixed-length array of booleans with 100 items.

        // Two examples of Partly On Disk Arrays.
        // Dynamic integer array with only 100 elements in memory.
        int arrayVariable [ ,100];
        // Fixed-length string array with 1000 elements, and only 200 in memory.
        str arrayVariable2 [1000,200];

            // A dynamic array of integers.
            int i[];
            // A fixed-length real array with 100 elements.
            real r[100];
            // A dynamic array of dates with only 10 elements in memory.
            date d[,10];
            // A fixed length array of NoYes variables with 100 elements and 10 in memory.
            NoYes ny[100,10];
    }

#### <a name="multiple-array-indexes"></a>複数の配列インデックス

C++ および C\# などの一部の言語を使用すると、1 つ以上のインデックスを持つ配列を宣言できます。 つまり、「配列の配列」を定義することができます。 X++ では、1 次元配列のみサポートされているため、複数の配列インデックスを直接作成できません。 ただし、このセクションに記載されているメソッドを使用して、複数のインデックスを実装することができます。 たとえば、国別分析コードにより獲得される量を保持するため、2 つの分析コードを持つ配列を宣言します。 10 の国と 3 つの分析コードがあります。 C++ および C\# では、次の配列を宣言します。

    // This is C# or C++ code, not X++ code.
    real earning[10, 3];

ただし、X++ はこの申告をサポートしていません。 代わりに、要素の数が各分析コード内の要素の製品である 1 次元配列を定義することができます。 次に例を示します。

    public void MultipleArrayMethod()
    {
        // Step 1: define a one-dimensional array with the number
        // of elements that is the product of the elements in each dimension.
        real earnings[10*3];

        // Step 2: to refer to a specific element, such as earnings[i,j], write the following:
        // declare i and j (maybe) and assign the value to something
        int i = 1;
        int j = 2;
        real element = earnings[(i-1)*3 + j];
    }

    // This can be written into a macro like this:
    #localmacro.earningIndex
    (%1-1)*3+%2
    #endmacro

    public void CallTheMacro()
    {
        // Next, call the specific element within the macro like this:
        int i = 1;
        int j = 2;
        real element = earnings[#earningIndex(i,j)];

        // The previous scheme can be extended to any number of dimensions.
        // The element a[i1, i2, ..., ik] can be accessed by computing the
        // offset into an array containing (d1*d2*...*dk) elements.
        //(i1 - 1)*d2*d3*..*dk +
        //(i2 - 1)*d3*d4*...*dk + .... +
        //(ik-1 -1)*dk +
        //(ik-1)
    }

### <a name="container"></a>コンテナー

*コンテナー*オブジェクトは、プリミティブ データ型または複合データ型が含まれる項目の動的リストです。 コンテナーは、クライアント層とサーバー層の間でさまざまな種類の値を渡す必要がある場合に便利です。 ただし、ループ内でのリストに繰り返し追加する予定がある場合、コンテナーは適切な選択肢ではありません。 コンテナーは、コンテナーのサイズまたは内容を過度に変更することがないプロセスに最も適しています。 コンテナーに過剰にデータが追加されると、コンテナーのデータを繰り返しコピーする必要があり、また新しい領域を繰り返し割り当てる必要があるため、システム全体のパフォーマンスが低下する可能性があります。 コンテナーはクラスではありません。 コンテナーには、プリミティブ値またはその他のコンテナーの注文済のシーケンスが含まれています。 **anytype** の柔軟性のために、コンテナーは異なるタイプの値を一緒に保存する良い方法を提供します。 コンテナーは、データベースに保管できます。 コンテナーとは、アプリケーション エクスプローラーを使用して、テーブルに列を追加する場合に選択可能な列タイプの 1 つです。 配列に少し似た、または **List** や **Stack** クラスのようなコレクションのコンテナーです。 ただし、コンテナーを作成した後にコンテナーのサイズまたはコンテンツを変更できません。 コンテナを変更するために表示される X++ ステートメントは、内部で新しいコンテナを構築して必要に応じ値をコピーします。 コンテナーを別のコンテナー変数に割り当てても、コンテナーの新しいコピーは作成されます。 これらすべての工程はパフォーマンスに影響を与えることがあります。 コンテナーへのアクセスを提供する関数 (**conPeek** など) では、コンテナーは 0 ベースではなく、1 ベースです。 インデックスは配列に対して 1 ベースです。 コンテナーの既定値は **空** です。 コンテナーには値が含まれていません。 コンテナーを使用するいくつかのステートメントは、コンテナーを変更するように見えることがあります。 ただし、システム内部では、コンテナーは決して変更されません。 代わりに、元のコンテナーからのデータは、新しいコンテナーを構築するためにコマンドからのデータと結合されます。 **conDel**、**conIns**、または **conPoke** のいずれかの関数を使用して、新しいコンテナを作成することができます。 また、**グローバル** クラスには、コンテナーを処理するための静的メソッドがあります。 これらのメソッドには、**con2ArraySource**、**con2Buf**、**con2List**、**con2Str**、**containerFromXmlNode**、**conView**、**str2Con** が含まれます。 **conIns** や **conPeek** のような、コンテナーを扱うためのいくつかの固有の関数があります。 X++ **conPeek** 関数は **anytype** タイプを返します。 したがって、各値の型がわからない場合は、コンテナーから値を読み取る方が簡単です。 **anytype** は値を変換することができればすべての X++ 値タイプに割り当てることができます。 明示的なデータ型の変換を回避すると、コードは読みやすくなります。 したがって、値をコンテナーに配置するために使用されたのと同じデータ型にコンテナーから値を割り当てます。 コンテナーを **エニタイプ** に割り当てることはできません。適切な変換を決定できない可能性があるためです。 そのような場合、予期しない動作やエラーが発生する可能性があります。

#### <a name="comparing-container-to-other-options"></a>コンテナーと他のオプションの比較

**コンテナー**型は、**List** や **Stack** などの配列およびコレクション クラスなど、他の構成要素と似ています。 コンテナーと **リスト** の違いは、**リスト** クラスのインスタンスが不変であるという点です。 **リスト**オブジェクトは、最初にそのデータが消費するよりも多くの領域を割り当てます。 その後、データが追加されると、スペースが埋められます。 この動作は、要素が追加されるたびに多くの領域を割り当てる場合よりも効率的です。 **リスト**の更新はコンテナーの同様の操作よりも高速に実行します。 **リスト** オブジェクトを作成するときは、**リスト** オブジェクトが格納できるデータの 1 つのタイプを決定します。 この制限は、コンテナの場合よりも**リスト**の柔軟性が低くなります。 ただし、**リスト**のオブジェクトを格納できますが、コンテナーでは値の型しか格納できません。 コンテナーと配列の違いは、配列は宣言された型の項目だけを保持できるという点です。 配列にメモリ容量を割り当て、後からその容量に値を入力することができます。 たとえば、ループに値を入力することができます。 この動作は効率的であり、適正に動作します。 新しいデータを追加して新しいコンテナーを作成するときは、**+=** 演算子かまたは **conIns** 機能のいずれかを使用します。 **+=** 演算子は高速の代替です。 **conIns** 関数は、元のデータの最後のインデックスの前に新しいデータを追加する場合にのみ使用します。 Dynamics AX 2012 では、コンテナーのオブジェクト参照を格納するために X++ コンパイラを使用できましたが、結果は実行時に失敗していました。 ただし、Microsoft Dynamics 365 for Finance and Operations で、コンパイラがコンテナー内のオブジェクト参照を格納しようとする試みを確認すると、エラー メッセージを出します。 コンテナーに追加される要素のタイプが **anytype** である場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。 この場合、コンパイラはその試行を認めます。 ユーザーは何をしているかを把握しているとみなされます。 コンパイラはコードを誤っていると診断しませんが、エラーは実行時間にスローされます。

#### <a name="container-examples"></a>コンテナーの例

    public void ContainerExample() 
    {
        // First, declare the variables you are using.  
        container myContainer;
        container myContainer4;
        container myContainer5; 
        // Three ways to declare a container.
        myContainer = [1];
        myContainer += [2];
        myContainer4 = myContainer5;

        // Declare a container.
        container cr3;

        // Assign a literal container to a container variable.
        cr3 = [22, "blue"];

        // Declare and assign a container.
        container cr2 = [1, "blue", true];

        // Mimic container modification (implicitly creates a copy).
        cr3 += [16, strMyColorString];
        cr3 = conIns(cr3, 1, 3.14);
        cr3 = conPoke(cr3, 2, "violet");

        // Assignment of a container (implicitly creates a copy).
        cr2 = cr3;

        // Read a value from the container.
        str  myStr = conPeek(cr2, 1);

        // One statement that does multiple assignments from a container.
        str myStr;
        int myInt;
        container cr4 = ["Hello", 22, 20\07\1988];
        [myStr, myInt] = cr4; // "Hello", 22

        // Example of applying the = operator to a container. The example
        // initializes myContainer2 and myContainer33.
        myContainer2 = [2, "apple"];

        // Next, you make a copy of myContainer33 and assign the copy to myContainer2.
        myContainer33 = [33, "grape"];
        myContainer2 = myContainer33;  // The container that myContainer2 had been holding is no longer available and cannot be recovered.
        // An example of building a new container by
        // assigning a new value to myContainer33 through the += operator.
        myContainer33 += [34, "banana"];
    }

    // Container example. The variable2 and variable3 hold different containers.
    static void JobC(Args _args)
    {
        container variable2, variable3;
        variable2 += [98];
        variable3 = variable2;
        variable2 += [97];
    }

    // List class example. In this example, variable2 and variable3 refer to the same List object.
    static void JobL(Args _args)
    {
        List variable2,variable3;
        variable2 = new List(Types::Integer);
        variable2.addEnd(98);
        variable3 = variable2;
        variable2.addEnd(97);
    }

    // The automatic type conversion by anytype also applies to the special syntax for making multiple
    // assignments from a container in one statement. This is shown in the following code example,
    // which assigns a str to an int, and an int to a str.
    static void JobContainerMultiAssignmentUsesAnytype(Args _args)
    {
        container con2;
        int int4;
        str str7;
        con2 = ["11", 222];
        [int4, str7] = con2;
        info(strfmt("int4==11==(%1), str7==222==(%2)", int4, str7));
    }

    /***  Output:
    Message (10:36:22 am)
    int4==11==(11), str7==222==(222)
    ***/

    static void UseQuery()
    {
        // An example of how the compiler diagnoses attempts to store object in containers
        container c = [new Query()];   // This statement will cause the error message shown below.
        /*** Instance of type 'Query' cannot be added to a container. ***/

        // An example of a code that won't cause an error message, but will
        // cause an error message to be thrown at runtime.
        anytype a = new Query();
        container d = [a];
    }

### <a name="classes-as-data-types"></a>データ型としてのクラス

*クラス*は、クラスのインスタンスの変数とメソッドの両方を説明するタイプ定義です。 (クラスのインスタンスは*オブジェクト*ともよばれます。) クラスはオブジェクトの定義に過ぎず、すべてのオブジェクトは宣言されると **null** です。 アプリケーション エクスプローラーでは、**クラス** ノードの各アプリケーション クラスはデータ型です。 これらの種類の変数をコード内で宣言することができます。 クラスのインスタンスを構築してインスタンスを変数に割り当てることができます。 クラスはソース コードに入れ子にできます。 入れ子になったクラスはフォーム内 (**FormRun** を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表すために使用します。 属性の修飾で接尾語に**属性**がある場合、属性の修飾などのクラスまたはメソッドで、属性名の接尾語を省略できます。 したがって、X++ は **\[MyFavoriteAttribute\]** を必要とするのではなく、**\[MyFavorite\]** を許可します。 また、属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらのターゲットにマップします。 AX 2012 およびそれ以前のバージョンでは、クライアントまたはサーバーのいずれかで実行するメソッドを指定することができました。 ただし、Microsoft Dynamics 365 for Finance and Operations およびそれ以降のバージョンでは、コンパイルされたすべての X++ コードがサーバーの .NET 共通中間言語 (CIL) として実行されます。 クライアント サイトまたはブラウザーで評価されるコードはなくなりました。 したがって、**client** キーワードと **server** キーワードは無視されるようになりました。 これらのキーワードが使用される場合コンパイル エラーは発生しませんが、新しいコードを使用することはできません。

#### <a name="private-and-protected-member-variables"></a>プライベートおよび保護されたメンバー変数

以前は、クラスで定義されていたすべてのメンバー変数が保護されていました。 **private**、**protected**、および **public** キーワードを加えることにより、メンバー変数の表示を明示的にすることができるようになりました。 これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。

-   **プライベート** – メンバー変数は、定義されているクラス内でのみ使用できます。
-   **保護されている** – メンバー変数は、それが定義されているクラスおよびクラスのすべてのサブクラスで使用できます。
-   **パブリック** – メンバー変数を任意の場所に使用することができます。 これは、定義されているクラス階層の範囲外に表示されます。

既定では、明示的なモディファイアーで実装されていないメンバー変数は引き続き保護されています。 ただし、ベスト プラクティスとしては、可視性を明示的に指定する必要があります。 先に説明したように、メンバー変数が**パブリック**として定義されている場合、メンバー変数は定義されているクラス外でアクセスできます。 この場合、変数をホストしているオブジェクトを指定する修飾子を指定する必要があります。 修飾子を指定するには、メソッド呼び出しの場合と同様にドット表記法を使用します。 次の例では、**field1** に明示的な **this** 修飾子を使用することでアクセスします。 この場合、そのアプローチは消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることをお勧めできない場合があります。 常に、実装ではなくコントラクトにのみ依存させる必要があります。

    public class AnotherClass3
    {
        int field1;
        str field2;
        void new()
        {
            this.field1 = 1;   // Explicit object designated.
            field2 = "Banana";  // 'this' assumed, as usual.
        }
    }

#### <a name="static-constructors-and-static-fields"></a>静的コンストラクターおよび静的フィールド

*静的フィールド*は**静的**キーワードを使用して宣言されているフィールドです。 概念的には、クラスのインスタンスではなく静的フィールドに適用されます。 静的コンストラクターは、静的呼び出しまたはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。 静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。 静的コンストラクターは明示的に呼び出さないでください。 代わりに、コンパイラはコンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。 静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のあるアクションを実行するために使用されます。 静的コンストラクターのパラメーターを指定することはできず、**静的** キーワードでマークされる必要があります。

    // An example of how a singleton (call instance in the example below)
    // can be created using the static constructor.
    public class Singleton
    {
        private static Singleton instance;
        private void new()
        {
        }
        static void TypeNew()    // This is the static constructor.
        {
            instance = new Singleton();
        }

        public static Singleton Instance()
        {
            return Singleton::instance;
        }
    }

    // The singleton ensures that only one instance of the class
    // will be called, which is consumed by the following. 
    {
        // Your code here.
        Singleton i = Singleton::Instance();
    }

#### <a name="class-elements-in-application-explorer"></a>アプリケーション エクスプローラーのクラス要素

アプリケーション エクスプ ローラーのほとんどのクラス・ノードの下には、**classDeclaration** ノードと **new** ノードという 2 つの特殊ノードがあります。 **classDeclaration** は、常に X++ **クラス**キーワードになります。 追加のキーワードは、**拡張**のように、クラスを変更するために含めることができます。 このノードには、メンバー変数の宣言も含めることができます。 メンバー変数は、**classDeclaration** の値に初期化することはできません。また静的にすることはできません。 次の例では、変数 **m\_priority** および **m\_rectangle** はクラスのメンバーです。

    // An example of a classDeclaration.
    public class YourDerivedClass extends YourBaseClass
    {
        int m_priority;
        Rectangle m_rectangle;
        void new(int _length, int _width)
        {
            this.m_rectangle = new Rectangle(_length, _width);
        }
    }

**新しい**演算子には、**新しい**演算子を使用して、クラスのインスタンスを作成するときに実行されるロジックが含まれます。 **新規** メソッドのロジックは、オブジェクトを作成し、そのオブジェクトを **classDeclaration** で宣言された変数に割り当てることができます。 各クラスは、**新しい**方法を 1 つだけ持つことが可能です。 ただし、**新しい**メソッドでは、多くの場合基本クラスの**新しい**メソッドを呼び出す必要があります。 基本クラスの<**新規**メソッドを呼び出すには、**super()** を呼び出します。 次の例は、前の **classDeclaration** の例の **YourDerivedClass** クラスの **new** メソッドを示しています。 この**新しい**メソッドで、コードは**長方形**クラスのインスタンスを構築します。 インスタンスは、**m\_rectangle** 変数に割り当てられます。 例で使用される **this** キーワードはオプションです。 ただし、それを含める場合、IntelliSense が役立つ可能性があります。

    // An example of the new method from the previous classDeclaration example.
    void new(int _length, int _width)
    {
        this.m_rectangle = new Rectangle(_length, _width);
    }

#### <a name="garbage-collection"></a>ガベージ コレクション

最終的に実行中では、ほとんどのオブジェクトがそれらを指す変数はなくなります。 システムはこれらのオブジェクトをスキャンし、それらをメモリから消去します。 その後、メモリ空間は他の用途に利用できるようになります。 **Object** クラスには、**finalize** というメソッドがあります。 ただし、**確定**メソッドはデストラクタではありません。 ランタイムは、オブジェクトがガベージとして収集された場合でも、**finalize** メソッドを呼び出すことはありません。

#### <a name="system-classes"></a>システム クラス

アプリケーション エクスプローラーの**システムのドキュメント** &gt; **クラス**には、カーネル クラスまたはシステム クラスの一覧があります。 システム クラスは、X++ で記述されておらず、ソース コードを表示することはできません。 システム クラスを追加することはできません。 システム クラには通常、**new** メソッドがありますが、**classDeclaration** ノードはありません。 すべてのアプリケーション クラスは**オブジェクト**システム クラスを暗黙的に拡張します。 一部のシステム クラスは、類似した名前を持つアプリケーション クラスで拡張されます。 たとえば、**xClassFactory** が **ClassFactory** ごとに延期されます。 そのような場合、システム クラスは使用しないでください。 詳細については、[X++ クラスおよびメソッド](xpp-classes-methods.md) で「システム クラスの代替アプリケーション クラス」を参照してください。

#### <a name="extension-methods"></a>拡張メソッド

拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。 次のルールが適用されます。

-   拡張クラスは静的でなければなりません。
-   拡張クラスの名前は、10 文字の接尾語 **\_Extension** で終了する必要があります。 ただし、接尾辞に先行する名前の部分には制限はありません。
-   拡張子クラス内のすべての拡張子メソッドは、**パブリック静的**として宣言する必要があります。
-   すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。 ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。 代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。
-   拡張メソッドのターゲットは、クラス、テーブル、ビュー、またはマップ アプリケーション オブジェクト タイプである必要があります。

拡張クラスはプライベートまたは保護された静的メソッドを含めることができます。 これらのメソッドは通常、実装の詳細に使用され、拡張として公開されません。 拡張メソッドの手法は、拡張するクラスのソース コードには影響しません。 したがって、クラスへの追加はオーバーレイを必要なく行うことができます。 ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。 ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。 拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。 拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトには何もアクセスできません。 したがって、拡張メソッドは構文砂糖の一種と考えることができます。 目標タイプに関係なく、拡張機能クラスはタイプに拡張メソッドを追加するために使用されます。 たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されていませんし、拡張テーブルというものは存在しません。

    // An example of an extension class holding a few extension methods.
    public static class AtlInventLocation_Extension
    {
        public static InventLocation refillEnabled(
           InventLocation _warehouse,
           boolean _isRefillEnabled = true)
        {
           _warehouse.ReqRefill = _isRefillEnabled;
           return _warehouse;
        }

        public static InventLocation save(InventLocation _warehouse)
        {
           _warehouse.write();
           return _warehouse;
        }
    }

### <a name="delegates-as-data-types"></a>データ型としてのデリゲート

*デリゲート*は、それをサブスクライブするメソッドを収集します。 デリゲートは、すべてのサブスクライバ メソッドが共有する必要があるパラメーター署名を指定します。 デリゲートが呼び出されると、デリゲートはその各サブスクライバを呼び出します。 デリゲートは値を返しませんし、**既定値を持つことはできません**。 最初に、すべてのデリゲートにはサブスクライブされたメソッドがありません。 デリゲートが宣言できるパラメーターの数に制限はなく、これらのパラメーターの種類に制限はありません。 デリゲートの唯一の目的は、サブスクライバが従わなければならない契約を定義することであるため、デリゲート本文は常に空です。 デリゲートは、クラスで定義をしなくてもかまいません。 デリゲートは、テーブル、フォーム、またはクエリで定義することもできます。

#### <a name="delegate-examples"></a>デリゲートの例

    abstract class VarDatClass
    {
        // delegatemethod examples
        // An example of declaring a delegate.
        delegate void notifyChange(utcdatetime _dateTime, str _changeDescription)
        {
        }

        // An example of subscribing an event handler to a delegate.
        public static void notifyStatic(utcDateTime _dateTime, str _changeDescription)
        {
            info("A notification has occurred calling static handler:" +
                DateTimeUtil::toStr(_dateTime) +
                " Message:" +
                _changeDescription);
        }
    }

### <a name="tables-as-data-types"></a>データ型としてのテーブル

すべてのテーブルはクラス定義として扱うことができます。 テーブル変数は、テーブル (class) の定義のインスタンス (オブジェクト) と見なすことができます。 テーブル変数の各フィールドでは、既定値は**空**です。 フィールドに注意を向けてテーブル上でメソッドを作成することができます。 これらのメソッドは、テーブルのインスタンス上で呼び出すことができます。 テーブル内のレコードを操作 (つまり、読み取り、更新、挿入、削除) するには、レコードを保持しておくための少なくとも 1 つのテーブル変数を宣言する必要があります。 ベスト プラクティスは、変数の名前としてテーブルの名前を使用する必要がありますが、最初の小文字を使用します。 テーブルとオブジェクト間のいくつかの重要な違いを次に示します。

-   テーブル変数の容量を割り当てることはできません。 配賦は暗黙的に行われます。
-   テーブル変数のフィールドは、パブリックです。 任意の場所でそれを参照することができます。
-   テーブル変数のフィールドは、式を使用して参照できます。

自動変換はありませんが、**共通**として宣言されているテーブル変数は、どのテーブルからでもデータを保持できます。

#### <a name="scope-of-table-variables"></a>テーブル変数の範囲

ほとんどの点で、テーブル変数をオブジェクトとみなすことができます。 ただし、オブジェクトとは異なり、それらは明示的に割り当てられません。 変数の宣言のみ必要です。 すべてのテーブルには共通のテーブルと互換性があるように、すべてのオブジェクトにも**オブジェクト**クラスの互換性があります。 テーブル変数は、一般的なバッファーとして宣言され、任意のテーブルからデータを保持するために使用できます。 テーブル変数を持たないテーブルにはアクセスできません。 テーブルの変数およびオブジェクトの宣言の原則は、領域の割り当てに関する点を除いて同じです。

#### <a name="table-examples"></a>テーブルの例

構文は、レコード内のフィールドを参照するさまざまな可能性を高めます。 たとえば、**TableName.(FieldId)** 構文を使用できます。 次の例では、顧客テーブルの現在のレコードにあるフィールドの内容を出力します。

    // Declares and allocates space for one CustTable record.
    public void myMethod()
    {
        CustomerTable custTable;
    }

    // An example of referencing table variables.
    public void printAccountNo()
    {
        CustomerTable custTable;
        print custTable.AccountNo;  // Prints the field reference.
    }

次の例では、**fieldCnt** および **fieldCnt2Id** メソッドを使用しています。 **fieldCnt** メソッドは、テーブル内のフィールドの数をカウントしますが、**fieldCnt2Id** はフィールド番号の ID を返します。 たとえば、**fieldCnt2Id** メソッドを使用して、テーブルでそのフィールド番号 6 が ID 54 を持っていることを確認します。 この変換は、表内のフィールドの ID が連続しているという保証がないため、この変換が必要です。

    // An example of the various possibilities for referencing fields in records.
    public void printCust()
    {
        int i, n, k;
        CustomerTable custTable;
        DictTable dictTable;
        dictTable = new DictTable(custTable.TableId);
        n = dictTable.fieldCnt();
        print "Number of fields in table: ", n;
        for(i=1; i<=n; i++)
        {
            k = dictTable.fieldCnt2Id(i);
            print "The ", dictTable.fieldName(k),
            " field with Id=",k, " contains '",
            custTable.(k), "'";
        }
    }

## <a name="collection-classes"></a>コレクション クラス
X++ 言語の構文には、配列とコンテナーという 2 種類の複合が用意されています。 これらの複合型は、プリミティブ型の値を集約するのに便利です。 ただし、配列またはコンテナーのクラス オブジェクトを格納することはできません。 *コレクション クラス*はオブジェクトの格納に使用されます。 これらは、配列、リスト、セット、マップ、任意のデータ型を保持できる構造、オブジェクトさえも作成できます。 最大パフォーマンスについては、C++ (システム クラス) で、クラスが実装されます。 *ファンデーション クラス*と呼ばれていたコレクション クラス。 コレクション クラスは、**配列**、**リスト**、**マップ**、**設定**、および**構造体**です。

-   **配列** - このクラスは、X++ 言語の**配列**タイプに似ていますが、単一タイプ、オブジェクトおよびレコードの値を保持できます。 オブジェクトは、特定の順序でアクセスされます。
-   **リスト** – このクラスには、順にアクセスされる要素が含まれます。 配列とは異なり、**List** クラスは **addStart** メソッドを提供します。 **Set** クラスと同様に、**List** クラスは **getEnumerator** メソッドと **getIterator** メソッドを提供します。 反復子を使用して、**リスト** オブジェクトから項目を挿入および削除することができます。
-   **マップ** – このクラスはキー値を別の値に関連付けます。
-   **設定** – このクラスは、1 つのタイプの値を保持します。 値は、追加された順序で格納されません。 代わりに、**Set** オブジェクトは **in** メソッドのパフォーマンスを最適化するように値を格納します。 **セット**オブジェクトは、**セット**オブジェクトが既に格納している値を追加しようとする試みをすべて無視します。 **Set** クラスは、**Array** クラスとは異なり、**in** メソッドと **remove** メソッドを提供します。
-   **構造体** – このクラスは、1 つ以上のタイプの値を含めることができます。 これは、特定のエンティティに関する情報をグループ化するために使用されます。

**構造体**を除くすべてのコレクション クラスのコンストラクターは、**型**システム列挙型の要素である型パラメーターをとります。 コレクション インスタンスは、その型のアイテムのみを格納できます。 **Types::AnyType** 列挙要素は、**Set** オブジェクトなどのコレクション オブジェクトを作成するために使用できない特殊なケースです。 **null** 値は、**Set** オブジェクトに要素として格納できません。 また、**マップ** オブジェクトで **null** はキーになることはできません。 反復子または列挙子を使用して、コレクション オブジェクトを介して反復することができます。 反復子を取得する方法を示す一般的な例を次に示します。

    new MapIterator(myMap)
    myMap.getEnumerator()

**設定**オブジェクトで、任意の要素が追加または反復子が作成された後に削除される場合、反復子インスタンスは読み取りまたはコレクションによるステップで使用されることはなくなります。 **マップ**オブジェクトで、**設定**オブジェクトと同じように、任意の要素が削除されると、反復子が有効ではなくなります。 ただし、キーが新しいか、またはキーが既に存在していてその値のみが**マップ**要素で更新されているかどうかに関係なく、**Map.insert** メソッドへの呼び出し後も、**MapIterator** オブジェクトは有効です。 **Map.insert** を呼び出し、反復子オブジェクトが有効であることに依存するコードは、.NET Framework CIL として実行されると失敗する可能性があります。 コレクション クラスを使用するとより複雑なクラスを作成することができます。 たとえば、リストの先頭に要素が常に追加されるリストを使用して、スタックを簡単に実装できます。 最新の要素がスタックの先頭を占めます。 コレクション クラスを拡張することもできます。 たとえば、**リスト**クラスを拡張して、操作がタイプ セーフである顧客レコードの一覧を作成します。 この場合、派生したコレクション クラスは顧客レコードのみを受け入れます。

## <a name="extended-data-types"></a>拡張データ型
*拡張データ型*は**ブール**、**int**、**int64**、**実数**、**str**、および**日付**プリミティブ データ型、および**コンテナー**複合型に基づくユーザー定義型です。 EDT はプリミティブ データ型または補助名および追加のプロパティを持つコンテナーです。 たとえば、文字列を基準にして、**名前**という新しい EDT を作成することができます。 新しい EDT は、開発環境の変数とフィールド宣言で使用することができます。 また、EDT を他の EDT の基準にすることができます。 EDTs は、標準的なデータ型ですが、特定の名前および追加のプロパティがあります。 EDTs は、それらが基づいている標準データ型と同じ値とタイプ[換算](xpp-conversion-run-time-functions.md)を適用します。 EDT の利点を次に示します。

-   変数は意味のあるデータ型を持つため、コードは読みやすくなります。 たとえば、データ型は **str** の代わりに**名前**です。
-   EDT に設定するプロパティは、そのタイプのすべてのインスタンスで使用されます。 したがって、EDT は作業を減らし、一貫性を促進するのに役立ちます。 たとえば、勘定番号 (**AccountNum** データ型) には、システム全体で同じプロパティがあります。
-   EDT の階層を作成することができます。 EDT は、親から適切なプロパティを継承でき、その他のプロパティを変更することができます。 たとえば、**ItemCode** データ型が、**MarkupItemCode** および **PriceDiscItemCode** データ型の基準として使用されます。

### <a name="create-an-edt"></a>EDT の作成

この機能は、言語コンストラクトとして実装されていません。 EDT を作成するには、次の手順を実行します。

1.  ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。
2.  **新しい項目の追加**ダイアログ ボックスで、**インストール済み**を選択してから左ウィンドウの**アーティファクト**を選択します。
3.  中央ウィンドウで、作成する EDT タイプを選択します。
4.  名前を入力し、次に**追加**をクリックします。

### <a name="edt-example"></a>EDT 例

    public void EdtMethod()
    {
        // Example of declaring EDT variables where
        // a UserGroupID (integer) variable is declared and initialized to 1.
        UserGroupID groupID = 1;

        // An Amount (real) variable is declared.
        Amount currency;
    }

## <a name="null-values-for-data-types"></a>データ型の null 値
Microsoft Dynamics 365 for Finance and Operations は、その他の数多くのデータベース管理システム (DBMS) で使用できる **null** 値の概念をサポートしていません。 X++ の変数は、常にタイプと値を持ちます。 ただし、各データ タイプでは、1 つの値が **null** と見なされます (たとえば、**validateField** テーブル メソッドの実行時)。

| 種類        | null として扱われる値                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 日        | 1900-01-01                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 列挙        | その値が **0** に設定されている要素                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 整数     | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 実数        | 0.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 文字列      | 空の文字列                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 時刻        | 00:00:00                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Utcdatetime | 時間部分の値に関係なく、日付部分が **1900-01-01** に設定されている値たとえば、値 **1900-01-01T22:33:44** は **null** として扱われます。 日付部分が **1900-01-01** に設定されている **utcDateTime** 値は X++ **print** ステートメントでは空白で表示されることに注意してください。 **1900-01-01T00:00:00** 値のみ空白として **Global::info** メソッドにより表示されます。 値は、**DateTimeUtil::MinValue** メソッドの値です。 |

したがって、**validateField** メソッドによりユーザーが必須項目に入力したかどうかがチェックされる際、たとえば、**0** は **integer** タイプ フィールドで許容されず、最初のエントリは **enum** タイプ フィールドで許容されません。 また、SQL X++ ステートメントで、前のテーブルにリストされている値は、ブール値比較で **false** になります。 ただし、非 SQL X++ ステートメントでは、同等演算子およびリレーショナル演算子は他の値に対して動作するのと同じように、これらの値に対して動作します。 従来の DBMS の意味では、**コンテナー**型と**テーブル**型のクラスおよび変数は **null** とすることができます。 **テーブル**タイプは、すべてのフィールドに **null** 値がある場合は **null** です。



