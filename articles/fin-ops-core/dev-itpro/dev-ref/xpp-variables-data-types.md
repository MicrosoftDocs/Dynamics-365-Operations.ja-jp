---
title: X++ 変数
description: このトピックでは、X++の変数について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150183
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1380640d6dc028828e0615900b0488b21f130051
ms.sourcegitcommit: 7eae20185944ff7394531173490a286a61092323
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872640"
---
# <a name="x-variables"></a>X++ 変数

[!include [banner](../includes/banner.md)]

このトピックでは、X++の変数について説明します。

- *変数*は、特定のデータ型の情報が格納されているメモリ位置を示す識別子です。 サイズ、精度、既定値、暗黙的および明示的[変換](xpp-conversion-run-time-functions.md)関数、範囲は、変数のデータ型によって異なります。 
- 変数の*スコープ*は、項目にアクセスできるコード内の領域を定義します。 
- *インスタンス変数*はクラス宣言で宣言され、クラス内の任意のメソッドからまたは拡張クラスのメソッドからアクセスできます。 
- *ローカル変数*は定義されたブロック内でのみアクセスできます。 
- 変数が宣言されると、メモリが割り当てられ、その変数が既定値に初期化されます。 
- 静的フィールドおよびインスタンス フィールドの両方に、値を declaration ステートメントの一部として割り当てることができます。 
- 変数は、メソッドのコード ブロック内の任意の場所で宣言できます。 これらは、メソッドの先頭で宣言される必要はありません。 
- *定数*は、変数が宣言されたときに値を変更できない変数です。 **const** キーワードまたは **readonly** キーワードを使用します。 
- 定数は 1 つの方法で*読み取り専用のフィールド*とは異なります。 読み取り専用フィールドには値を 1 回だけ割り当てることができ、その値は変わりません。 フィールドには、フィールドが宣言されている場所、またはコンストラクターのいずれかでインラインで値を割り当てることができます。 

X++ で作成されていないマネージ型の変数を宣言するときは、2 つのオプションがあります。 完全な名前空間を含めることにより宣言内のタイプ名を完全に修飾、または **using** ステートメントをファイルに追加してから名前空間をタイプ名から省略することができます。

## <a name="variable-examples"></a>変数の例

```xpp
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
```

## <a name="var"></a>var

コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができます。 変数は、まだ厳密に型指定されている明確な型です。 

**var** は初期化式が提供されている宣言でのみ使用することができます。 (コンパイラは、初期化式から種類を推定します。) 場合によっては、この方法によって、コードが読みやすくなります。 

こうした状況でローカル変数を宣言するには、**var** を使用してください。

- 変数の型が右側の割り当てから明らかなとき
- 正確な型が重要でないとき
- ループ カウンター**用**の申告について
- **using** ステートメント内での破棄可能なオブジェクト対象

種類が初期化式からクリアされていない際は、**var** を使用しないでください。

## <a name="var-examples"></a>var の例

```xpp
// When the type of a variable is clear from
// the context, use var in the declaration.
var var1 = "This is clearly a string.";
var var2 = 27; // This is an integer (not a real).
var i = System.Convert::ToInt32(3.4);

// Don't use var when the type of the variable is not clear
// from the context. Use an explicit type instead.
int var4 = myObject.ResultSoFar();
```

## <a name="declare-anywhere"></a>任意の場所で宣言

ステートメントを提供できる場所に宣言を提供できるようになりました。 宣言は、構文的にはステートメントで、*宣言ステートメント*です。 

変数は使用される直前に宣言することができます。すべての変数を 1 つの場所で宣言する必要はありません。 したがって、変数のスコープを正確に制御できます。 

変数を参照することができない場所で、変数に小さなスコープを付与することができます。 変数の有効期間は宣言されているスコープです。 スコープは、**for** ステートメントおよび **using** ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。 

スコープを小さくすることにはいくつかの利点があります。

- 読みやすさが向上しました。
- コードの長期保守中に変数が不適切な方法で再利用されるリスクを軽減します。
- コードをリファクターすることがより簡単です。 再使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。

次の例では、使用される **for** ステートメント内のループ カウンターを宣言します。

```xpp
void MyMethod()
{
    for (int i = 0; i < 10; i++)
    {
        info(strfmt("i is %1", i));
    }
}
```

変数のスコープは **for** ステートメントそのものであり、条件式とループ更新部分を含みます。 この範囲外で値を使用することはできません。 

次の例では、コンパイラが **info** ステートメントに達すると、「'i' が宣言されていません」というエラー メッセージを発行します。

```xpp
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
```

また、以下の例に示されるように、変数を **using** ステートメントにスコープすることができます。

```xpp
static void AnotherMethod()
{
    str textFromFile;
    using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
    {
        textFromFile = sr.ReadToEnd();
    }
}
```

**IDisposable** を実装するオブジェクトを使用するときは、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。 **using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。 オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。 実際、コンパイラはこの方法だけで **using** ステートメントを変換します。 

次の例は、説明してきた機能のいくつかを示しています。

```xpp
// loop variable declared within the loop: It will
// not be misused outside the loop
for(int i = 1; i < 10; i++)
{
    // Because this value is not used from outside the loop,
    // its declaration belongs in this smaller scope.
    str s = int2str(i);
    info(s);
}
```

混乱を避けるために、コンパイラは囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラー メッセージを発行します。 たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります: 「i と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している i が別の意味になってしまうためです。」

```xpp
{
    int i;
    {
        int i;
    }
}
```

## <a name="constants-read-only-variables-and-macros"></a>定数、読み取り専用変数、およびマクロ

マクロの概念は完全にサポートされています。 ただし、定数にはマクロに比べて次のような利点があります。

- ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。 最終的に、言語サービスはこのコメントを受け取り、ユーザーに有用な情報を提供します。
- 定数は、IntelliSense で知られています。
- 定数は、相互参照です。 したがって、マクロではなく、特定の定数のすべての参照を見つけることができます。
- 定数は、アクセス修飾子が適用されます。 **private**、**protected**、および **public** モディファイアを使用することができます。 マクロのアクセシビリティが厳密に定義されていません。
- 定数変数にはスコープがありますが、マクロにはスコープがありません。
- デバッガーには定数の値または読み取り専用変数を表示することができます。

クラス スコープ (つまりクラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。 この機能は元はレガシ コンパイラ マクロの実装におけるバグしたが、ただし、多くのアプリケーション プログラマが多くの場合それを活用できるようになりました。 X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。 この機能は、コンパイラのパフォーマンスにも大きな影響を与えます。 

次の例に示すように、定数はクラス レベルで宣言できます。

```xpp
private const str MyConstant = 'SomeValue';
```

次に、定数を二重コロン (::) 構文を使用して参照することができます。

```xpp
str value = MyClass::MyConstant;
```

定数 (**const**) が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では **MyClass**) を省略できます。 したがって、マクロ ライブラリの概念を簡単に実装することができます。 マクロ シンボルのリストは、パブリック **const** の定義を持つクラスになります。 

また、定数を変数のみとして定義することができます。 コンパイラはインバリアントを維持して、値を変更できないようにします。

```xpp
{
    const int Blue = 0x0000FF;
    const int Green = 0x00FF00;
    const int Red = 0xFF0000;
}
```

## <a name="null-values-for-data-types"></a>データ型の null 値
その他の数多くのデータベース管理システム (DBMS) で使用できる **null** 値の概念がサポートされていません。 X++ の変数は、常にタイプと値を持ちます。ただし、各データ タイプでは、1 つの値が **null** と見なされます (たとえば、**validateField** テーブル メソッドの実行時)。

| 種類 | null として扱われる値 |
|------|-------------------------------|
| 日        | 1900-01-01                                              |
| 列挙        | その値が **0** に設定されている要素              |
| 整数     | 0                                                       |
| 実数        | 0.0                                                     |
| 文字列      | 空の文字列                                         |
| 時刻        | 00:00:00                                                |
| Utcdatetime | 時間部分の値に関係なく、日付部が**1900-01-01**に設定されている値。 たとえば、値 **1900-01-01T22:33:44** は **null** として扱われます。 日付部分が **1900-01-01** に設定されている **utcDateTime** 値は X++ **print** ステートメントでは空白で表示されることに注意してください。 **1900-01-01T00:00:00** 値のみ空白として **Global::info** メソッドにより表示されます。 値は、**DateTimeUtil::MinValue** メソッドの値です。 |

したがって、**validateField** メソッドによりユーザーが必須項目に入力したかどうかがチェックされる際、たとえば、**0** は **integer** タイプ フィールドで許容されず、最初のエントリは **enum** タイプ フィールドで許容されません。 また、SQL X++ ステートメントで、前のテーブルにリストされている値は、ブール値比較で **false** になります。 ただし、非 SQL X++ ステートメントでは、同等演算子およびリレーショナル演算子は他の値に対して動作するのと同じように、これらの値に対して動作します。 従来の DBMS の意味では、**コンテナー**型と**テーブル**型のクラスおよび変数は **null** とすることができます。 **テーブル**タイプは、すべてのフィールドに **null** 値がある場合は **null** です。

