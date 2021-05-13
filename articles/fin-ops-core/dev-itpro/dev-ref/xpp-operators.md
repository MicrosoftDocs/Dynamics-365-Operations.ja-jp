---
title: X++ 演算子
description: このトピックでは、X++ でサポートされている演算子について説明します。
author: RobinARH
ms.date: 12/02/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150373
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2e8fde8fae0a41446c00717611de2be6f5fc019
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866110"
---
# <a name="x-operators"></a>X++ 演算子

[!include [banner](../includes/banner.md)]

このトピックでは、X++ でサポートされている演算子について説明します。

## <a name="assignment-operators"></a>代入演算子

割り当ては、変数やフィールドの値を変更します。 次のテーブルは、X++ の代入演算子を示しています。 接頭辞と接尾辞の演算子には違いはありません。

| オペレーター   | 説明                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| `=`        | 等号の右側の式を左側の変数に割り当てます。                |
| `+=`       | 現在の変数の値に右側の式を足したものを左側の変数に割り当てます。  |
| `++`       | 変数を 1 ずつ増加します。                                                                     |
| `-=`       | 現在の変数の値から右側の式を差し引いたものを左側の変数に割り当てます。 |
| `--`       | 変数を 1 ずつ減分します。                                                                     |

### <a name="code-examples-for-assignment-operators"></a>代入演算子のコード例

```xpp
// An example of assignment operators and their output. 
static void Example1()
{
    int i = 1;
    // Using the = operator. i is assigned the value of i, plus 1. i = 2.
    i = i + 1;
    info(strFmt("Example 1: The result is "), i); // The result is 2.
}

static void Example2()
{
    int i = 1;
    // Using the += operator. i is assigned the value of i, plus 1. 
    // i = 2 (i = i + 1).
    i += 1;
    info(strFmt("Example 2: The result is "), i); // The result is 2. 
}

static void Example3()
{
    int i = 1;
    // Using the ++ operator. i is incremented by 1, and then 
    // by 1 again in the second statement. The final value of i is 3.
    i++;
    ++i;
    info(strFmt("Example 3: The result is "), i); // The result is 3. 
}

static void Example4()
{
    int i = 1;
    // Using the -= operator. i is assigned the value of i minus 1. 
    // i = 0 (i = i - 1).
    i -= 1;
    info(strFmt("Example 4: The result is "), i); // The result is 0. 
}

static void Example5()
{
    int i = 1;
    // Using the -- operator. i is decremented by 1, and then by 
    // 1 again in the second statement. The final value of i is -1.
    i--;
    --i;
    info(strFmt("Example 5: The result is "), i); // The result is -1. 
}
```

## <a name="arithmetic-operators"></a>算術演算子
算術演算子を使用して、数値計算を実行します。 演算子のほとんどはバイナリであり、2 つのオペランドを取ります。 ただし、**not** (`~`) 演算子は単項であり、オペランドを 1 つだけ受け取ります。 バイナリ演算子の構文: *expression1* *ArithmeticOperator* *expression2* 単項演算子の構文: *ArithmeticOperator* *expression1*

| オペレーター   | 説明      |
|------------|------------------|
| `<<`       | **left shift** 演算子は、*expression1* で *expression2* の左シフト (2 により乗算) を実行します。              |
| `>>`       | **right shift** 演算子は、*expression1* で *expression2* の右シフト (2 で除算) を実行します。                  |
| `\*`       | **multiply** 演算子は、*expression1* を *expression2* で乗算します。                                               |
| `/`        | **divide** 演算子は、*expression1* を *expression2* で除算します。                                                    |
| `DIV`      | **integer division** 演算子は、*expression1* の整数除算を *expression2* で実行します。                  |
| `MOD`      | **integer remainder** 演算子は、*expression2* による *expression1* の整数除算の余りを返します。 |
| `~`        | **not** 演算子、つまり単項演算子は、操作ではなくバイナリを実行します。                                          |
| `&`        | **binary AND** 演算子は、*expression1* および *expression2* でバイナリおよび演算を実行します。                    |
| `^`        | **binary XOR** 演算子は、*expression1* および *expression2* でバイナリ XOR 演算を実行します。                    |
| `|`        | **binary OR** 演算子は、*expression1* および *expression2* でバイナリまたは演算を実行します。                      |
| `+`        | **plus** 演算子は *expression1* を *expression2* に追加します。                                                         |
| `-`        | **minus** 演算子は、*expression1* から *expression2* を減算します。                                                 |
| `?`        | **ternary** 演算子は、3 つの式を取ります: *expression1* ? *式2* : *式3*。 *expression1* が true の場合、*expression2* が返されます。 それ以外の場合、*expression3* が返されます。 |

### <a name="code-examples-for-arithmetic-operators"></a>算術演算子のコード例

```xpp
int a = 1 << 4;      // Perform four left shifts on 1 (1*2*2*2*2). a=16.
int b = 16 >> 4;     // Perform four right shifts on 16 (16/2/2/2/2). b=1.
int c = 4 * 5;       // Multiply 4 by 5. c=20.
int d = 20 / 5;      // Divide 20 by 5. d=4.
int e = 100 div 21;  // Return the integer division of 100 by 21. e=4 (4*21 = 84, remainder 16).
int f = 100 mod 21;  // Return the remainder of the integer division of 100 by 21. f=16.
int g = ~1;          // Binary negate 1 (all bits are reversed). g=-2.
int h = 1 & 3;       // Binary AND. Return the bits that are in common in the two integers. h=1.
int i = 1 | 3;       // Binary OR. Return the bits that are set in either 1 or 3. i=3.
int j = 1 ^ 3;       // Binary XOR. Return the bits that are set in 1 and NOT set in 3, and vice versa. j=2.
int k = 1 + 3;       // Add 1 and 3. k=4.
int l = 3 - 1;       // Subtract 1 from 3. l=2.
int m = (400 > 4) ? 1 : 5;  // If 400>4, 1 is returned. Otherwise, 5 is returned. Because 400>4, 1 is returned. m=1.
```

## <a name="expression-operators"></a>式の演算子
`as` および `is` 式演算子は、ダウンキャストの割り当てを制御します。 ダウン キャストの割り当てには、クラスまたはテーブルの継承が含まれています。 暗黙的にダウンキャストされた代入ステートメントは、予測および診断が困難なエラーを引き起こす可能性があります。 `as` キーワードを使用するとダウンキャストを明示的にすることができます。 `is` キーワードを使用して、実行時にダウンキャストが有効かどうかをテストできます。

### <a name="the-as-keyword"></a>as キーワード

基本クラス変数から派生クラス変数にダウンキャストする割り当てキーワードには、`as` を使用します。 `as` キーワードは、他のプログラマやコンパイラに対して、ダウンキャストが実行時に有効であると考えられることを通知します。

-   コンパイラは、`as` キーワードを持たないダウンキャスト割り当てステートメントのエラーを報告します。
-   実行時に `as` キーワードを指定すると、ダウンキャストが有効でない場合に、ダウンキャスト割り当てステートメントに `null` が割り当てられます。
-   この `is` キーワードは、多くの場合、`as` キーワードが機能するかどうかのテストを問題なく行うために使用されます。

#### <a name="code-example-for-the-as-keyword"></a>キーワードとしてのコード例

次のコード例では、**DerivedClass** クラスが **BaseClass** クラスを拡張します。 このコード例には、**basec** と **derivedc** 変数の間に 2 つの有効な割り当てが含まれています。 **basec** へのアップキャスト割り当てには `as` キーワードは必要ありませんが、**derivedc** へのダウンキャストの割り当てには `as` キーワードが必要です。 次のコードはエラーなしでコンパイルして実行します。

```xpp
static void AsKeywordExample()
{
    // DerivedClass extends BaseClass.
    BaseClass basec;
    DerivedClass derivedc;
    // BottomClass extends DerivedClass.
    BottomClass bottomc;
    derivedc = new DerivedClass();
    // AS is not required for an upcast assignment like this.
    basec = derivedc;
    // AS is required for a downcast assignment like this.
    derivedc = basec as DerivedClass;
    bottomc = new BottomClass();
    // AS causes this invalid downcast to assign null.
    bottomc = basec as DerivedClass;
}
```

### <a name="the-is-keyword"></a>is キーワード

`is` キーワードは、オブジェクトが指定されたクラスのサブタイプであるかどうかを確認します。 `is` 式は、オブジェクトがクラスのサブタイプである場合、またはオブジェクトがクラスと同じ型である場合に **true** を返します。 `is` キーワード式が 2 つの型を比較するが、どちらの型も他方のサブタイプではなく、同じ型でない場合、コンパイラはエラーを報告します。 コンパイラは、2 つの型の間の任意の明示的な代入ステートメントについて同様のエラーを報告します。どちらの型も一方の型のサブタイプではなく、同じ型ではありません。 実行時に、基になるオブジェクトを参照する変数の型は `is` キーワードとは無関係です。 `is` キーワードを指定すると、システムは、オブジェクトを参照する変数の宣言された型ではなく、変数が参照するオブジェクトを検証します。

#### <a name="code-examples-for-the-is-keyword"></a>のコード例はキーワードです

次のコード例は、`is`式が **true** または **false** を返すかどうかを制御する条件を示しています。 このコード例は、**Form** クラスと **Query** クラスの両方が **TreeNode** クラスを拡張しているという事実に依存しています。

```xpp
// The compiler issues an error for the following code. 
// The compiler ascertains that the Form class and the Query class are not 
// part of the same inheritance hierarchy. Both the Form class and the Query class
// extend the TreeNode class, but neither Form nor Query is a subtype of the other.
Form myForm = new Form();
info(strFmt("%1", (myForm is Query)));

// The Infolog displays 0 during run time, where 0 means false. No supertype 
// object can be considered to also be of its subtype class.
TreeNode myTreeNode = new TreeNode();
info(strFmt("%1", (myTreeNode is Form)));

// The Infolog displays 0 during run time, where 0 means false. A null 
// reference causes the is expression to return false.
Form myForm;
info(strFmt("%1", (myForm is Form)));

// The Infolog displays 1 during run time, where 1 means true. 
// An object is an instance of its own class type.
Form myForm = new Form();
info(strFmt("%1", (myForm is Form)));

// The Infolog displays 1 during run time, where 1 means true. 
// Every subtype is also of its supertype.
Form myForm = new Form();
info(strFmt("%1", (myForm is TreeNode)));

// The Infolog displays 1 during run time, where 1 means true. 
// The type of the underlying object matters in the is expression,
// not the type of the variable that references the object.
Form myForm = new Form();
TreeNode myTreeNode;
myTreeNode = myForm; // Upcast.
info(strFmt("%1", (myTreeNode is Form)));
```

#### <a name="code-example-for-the-is-and-as-keywords"></a>と キーワードとしてのコード例

次のコード例には、`is` キーワードの一般的な使用方法が含まれています。 `as` キーワードは `is` キーワードが `as` キーワードが成功することを確認した後に使用されます。 この例では、`is` キーワードと `as` キーワードは大文字で表示され、見やすくなっています。

```xpp
static void IsKeywordExample() 
{
    DerivedClass derivedc;
    BaseClass basec;
    basec = new DerivedClass();  // An upcast.
    if (basec IS DerivedClass)
    {
        info("Test 1: (basec IS DerivedClass) is true. Good.");
        derivedc = basec AS DerivedClass;
    }
    basec = new BaseClass();
    if (!(basec IS DerivedClass))
    {
        info("Test 2: !(basec IS DerivedClass) is true. Good.");
    }
}

//Output to the Infolog
Test 1: (basec IS DerivedClass) is true. Good.
Test 2: (!(basec IS DerivedClass)) is true. Good.
```

### <a name="object-class-as-a-special-case"></a>特殊なケースとしてのオブジェクト クラス

**Object** クラスは、継承機能に特別なケースとして表示できます。 コンパイラは、**オブジェクト** 型であると宣言された変数との間の割り当ての型チェックをバイパスします。 **オブジェクト** クラスから継承されるクラス、別のクラスから継承されるクラス、どのクラスからも継承されないクラスがあります。 **ダイアログ** クラスはどのクラスからも継承しませんが、次のコード例の割り当ておよび呼び出しステートメントからの処理はおこなわれます。 ただし、割り当てが `bank4 = dlog3;` の場合、**銀行** クラスと **ダイアログ** クラスは互いに継承関係を持たないため、コンパイル時に失敗します。 コンパイラは、**オブジェクト** クラスであると宣言された変数への割り当てに対して、1 つの小さな検証しか実行しません。 コンパイラは、**オブジェクト** 変数に割り当てられている項目がクラスのインスタンスであることを確認します。 コンパイラでは、テーブル バッファーのインスタンスを **オブジェクト** 変数に割り当てることはできません。 また、コンパイラは、`int` または `str`のようなプリミティブ データ型を **オブジェクトt** 変数に割り当てることはできません。

```xpp
static void ObjectExample()
{
    Bank bank4;
    Object obj2;
    Dialog dlog3 = new Dialog("Test 4.");
    obj2 = dlog3;  // The assignment does work.
    obj2.run(false);  // The call causes the dialog to appear.
    info("Test 4a is finished.");
}
```

### <a name="tables"></a>テーブル

すべての表は、異なる表から明示的に継承しない限り、共通システム表から直接継承します。 共通テーブルをインスタンス化することはできません。 基になる物理データベースに存在しません。 共通テーブルは **xRecord** クラスから継承されますが、`is` キーワードまたは `as` キーワードに適切でない特別な方法で継承されます。 テーブル間の無効なダウンキャストの実行に`as` キーワードが使用されるとき、ターゲット変数は使用不可能な null エンティティを参照します。 ターゲット変数の参照を解除しようとすると、プログラムを停止させるエラーが発生します。

### <a name="the-is-and-as-keywords-and-extended-data-types"></a>is キーワードと as キーワードと拡張データ型

各拡張データ タイプには、**拡張** プロパティがあります。 このプロパティが制御する継承のスタイルは、`is` で、`as` のキーワードが設計されている継承のスタイルと異なります。

## <a name="relational-operators"></a>リレーショナル演算子
次のテーブルは、X++ で使用できるリレーショナル演算子の一覧です。 演算子のほとんどはバイナリであり、2 つのオペランドを取ります。 ただし、**not** (`!`) 演算子は単項であり、オペランドを 1 つだけ受け取ります。 バイナリ演算子の構文: *expression1* *relationalOperator* *expression2* 単項演算子の構文: *relationalOperator* *expression1*

| オペレーター | 説明     |
|----------|--------------------------------|
| `like`   | **like** 関係演算子は、*expression1* が *expression2* と似ている場合に **true** を返します。  |
| `==`     | **equal** 関係演算子は、両方の式が等しい場合に **true** を返します。  |
| `>=`     | **greater than or equal to** 関係演算子は、*expression1* が *expression2* 以上の場合に **true** を返します。   |
| `<=`     | **less than or equal to** 関係演算子は、*expression1* が *expression2* 以下の場合に **true** を返します。|
| `>`      | **greater than** 関係演算子は、*expression1* が *expression2* より大きい場合に **true** を返します。 |
| `<`      | **less than** 関係演算子は、*expression1* が *expression2* より小さい場合に **true** を返します。  |
| `!=`     | **not equal** 関係演算子は、*expression1* が *expression2* と異なる (つまり等しくない) 場合に **true** を返します。                          |
| `&&`     | **and** 関係演算子は、*expression1* と *expression2* の両方が true の場合に、**true** を返します。  |
| `||`     | **or** 関係演算子は、*expression1* または *expression2* が true の場合、または両方が true の場合に **true** を返します。 |
| `!`      | **not** または **unary** 関係演算子、式を無効にします。 式が false の場合は **true**、式が true の場合は **false** を返します。 |

### <a name="the-like-operator"></a>like 演算子

`like`演算子は、`*` を 0 文字以上のワイルドカード文字として、さらに、 `?` を 1 つの文字に対する 1 つのワイルドカード文字として使用できます。 オペランドは 1,000 文字を超えることはできません。 `like` 演算子は、基になる SQL により評価されるため、インストールごとに結果が異なる可能性があります。 比較している式にファイルのパスが含まれている場合は、次の例で示すように、各要素の間で次の 4 つのバックスラッシュを含める必要があります。

```xpp
select * from xRefpaths
where xRefPaths.Path like "\\\\Classes\\\\AddressSelectForm"
```

### <a name="the-equal--operator"></a>等号 (==) 演算子

**等号** (`==`) 演算子を使用してオブジェクトを比較するとき、オブジェクト自体ではなく、オブジェクト参照が比較されます。  この動作は、2 つのオブジェクト (そのうちの 1 つはサーバー上にあり、もう 1 つはクライアント上にあるオブジェクト) を比較すると問題が発生する可能性があります。 そのような場合、**equal** メソッドを **オブジェクト** クラスで使用する必要があります。 このメソッドをオーバーライドして、2つのオブジェクトが等しいことが何を意味するかを指定することができます。 **等号** メソッドを上書きしない場合、比較は **等号** (`==`) 演算子によって行われる比較と同じになります。

### <a name="code-examples-for-relational-operators"></a>リレーショナル演算子のコード例

```xpp
"Jones" like "Jo?es"  // Returns true, because the ? is equal to any single character.
"Fabrikam, Inc." like "Fa*"  // Returns true, because the * is equal to zero or more characters.
(( 42 * 2) == 84)  // Returns true, because 42*2 is equal to 84.
today() >= 1\1\1980  // Returns true, because today is later than January 1, 1980.
((11 div 10) >= 1)  // Returns true, because 11 div 10 is 1 (therefore, >= 1 is true).
(11<= 12)  // Returns true, because 11 is less than 12.
((11 div 10) > 1)  // Returns false, because 11 div 10 is 1.
(11 div 10) < 1)  // Returns false, because 11 div 10 is 1.
(11 != 12)  // Returns true, because 11 is not equal to 12.
(1 == 1) && (3 > 1)  // Returns true, because both expressions are true.
```

## <a name="operator-precedence"></a>演算子の優先順位
複合式が評価される順序は重要です。 たとえば `(x + y / 100)` は、追加または区分を最初に実行するかどうかによって、結果が異なります。 かっこ (`()`) を使用すると、式の評価方法を明示的にコンパイラに指示することができます。 たとえば、 `(x + y) / 100`を指定できます。 オペレーションを実行する順序をコンパイラーに明示的に伝えていない場合、順序はオペレーターに割り当てられた優先順位に基づきます。 たとえば、除算演算子には、加算演算子より高い優先順位があります。 したがって、`x + y / 100`の式では、コンパイラはまず `y / 100` を評価します。 つまり、 `x + y / 100` は `x + (y / 100)` と等しくなります。 コードを読みやすく管理しやすくするために、明示的に記述します。 最初に評価する演算子を示すには、かっこを使用します。 次のテーブルは、優先順位の順に演算子を示します。 テーブルの演算子は高いほど、優先順位が高くなります。 高い優先順位がある演算子は、低い優先順位がある演算子より前に評価されます。 X++ の演算子の優先順位は、C\# および Java などの他の言語の演算子の優先順位と同じではないことに注意してください。


| 演算子グループ (優先順位順)                          |                 演算子    |
|------------------------------------------------------------------|------------------------------|
| 単項                                                            | `- ~ !`                      |
| 乗算、シフト、ビット演算 **AND**、ビット演算排他的 **OR** | `* / % DIV << >> & ^ `       |
| 加法、ビット演算包括的 **OR**                               | `+ –`                        |
| リレーショナル、同等                                             | `< <= == != > >= like as is` |
| 論理 (**AND**、**OR**)                                        | `&&` `||`                    |
| 条件付                                                      | `? :`                        |

同じ行の演算子には、同等な優先順位があります。 式にこれらの演算子のうち 1 つ以上が含まれる場合、代入演算子が使用されない限り、式は左から右に評価されます。 (代入演算子は、右から左に評価されます)。たとえば、`&&` (論理 `AND`) および `||` (論理 `OR`) には、同じ優先順位で、左から右に評価されます。 したがって、 
+ `0 && 0 || 1` == `1`
+ `1 || 0 && 0` == `0` です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]