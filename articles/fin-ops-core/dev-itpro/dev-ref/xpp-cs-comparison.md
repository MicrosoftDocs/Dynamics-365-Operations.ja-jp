---
title: X++ と C# の比較
description: このトピックでは、X++ と C# の構文とプログラミングを比較します。
author: RobinARH
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 72424
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7b04ec44037a9479d831fbb67757cdb5e4e7941
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753030"
---
# <a name="x-and-c-comparison"></a>X++ と C# の比較

[!include [banner](../includes/banner.md)]

このトピックでは、X++ と C# の構文とプログラミングを比較します。

## <a name="x-c-comparison-hello-world"></a>X++、C# の比較: Hello World

このセクションでは、最も単純な X++ プログラムを C# の対応するものと比較します。

### <a name="x-to-c-comparisons"></a>X++ と C# の比較

次のセクションでは、X++ と C\# の基本的な類似点と相違点について説明します。

### <a name="similarities"></a>類似点

次の X++ 機能は C# の機能と同じです。
-   単一ライン (`//`) および複数行 (`/* */`) のコメント。
-   `==` 2 つの値が等しいかどうかを判定するための (等しい) 演算子。
-   `!=` (等しくない) 2 つの値が等しくないかどうかを決定するための演算子。
-   `+` (プラス記号) 文字列連結の演算子です。

### <a name="differences"></a>違い

次のテーブルは、C# では異なる X++ の機能を示しています。

| 機能 | X++ | C# | コメント |
|---|---|---|---|
| `if` および `else` の条件付きステートメント | `if` ステートメントは、ブール値に自動的に変換できる式のあらゆる型を受け付けます。 一般的な例は、0 が false を意味する `int`、または Null が false を意味するオブジェクトを含みます。 | `if` ステートメントには、ブール式が必要です。 | 中括弧と括弧に関する構文構造は、X++ と C# でまったく同じです。 |
| リテラル文字列 | リテラル文字列は、次のいずれかの方法で区切ることができます。<ul><li>二重引用符 (") 文字のペア。</li><li>単一引用符 (') 文字のペア。</li></ul> | リテラル文字列は、二重引用符 (") のペアで区切る必要があります。 | X++ で、二重引用符文字は通常、文字列を区切るために使用されます。 ただし、文字列に二重引用符文字を含める必要がある場合、単一引用符文字で文字列を区切るのが便利です。|
| char `type` | X++ には `char` または文字タイプがありません。 長さ 1 の `str` を宣言することができますが、文字列のままです。<br> `str 1 myString = "a";` | C# には `char` があります。 最初に `char` を `string` に明示的に変換できますが、パラメーターとして `char` を `string` パラメーターを入力するメソッドに渡すことはできません。| X++ データ型の詳細については、プリミティブ データ型を参照してください。|
| メッセージの出力| X++ は情報ログ ウィンドウ内でユーザーにメッセージを提供します。 一般的なメソッドは次のとおりです。<ul><li><strong>print</strong> ステートメント:</li><li>`Global` クラスの静的メソッド:<ul><li>Global::info</li><li>Global::warning</li><li>Global::error</li></ul></li></ul>| コマンド ライン プログラムで、コンソールにメッセージを配信することができます。 一般的なメソッドは次のとおりです。<ul><li>`Console.Out.WriteLine`</li><li>`Console.Error.WriteLine`</li></ul>|  |

### <a name="x-and-c-samples"></a>X++ および C++ のサンプル

このセクションには、2 つの簡単なコード サンプルが含まれています。 1 つの例は X++、もう一方は C\# で記述されています。 両方のサンプルで同じ結果が得られます。 次の X++ 機能が示されています。
-   `//` 単一行のコメント
-   `/\*` `\*/`複数行コメント
-   `if` ステートメント
-   `==` 演算子
-   `!=` 演算子
-   `+` 文字列を連結する演算子
-   Global:: 接頭語を使用する場合と使用しない場合の、メッセージ出力の Global::info
-   メッセージ出力の Global::error
-   文字列区切り文字としての一重引用符および二重引用符 (' および ") の使用。

> [!NOTE]
> ユーザーに公開される可能性のある、すべての文字列に二重引用符を使用することをお勧めします。

#### <a name="x-sample"></a>X++ サンプル

この X++ コード サンプルでは、ジョブの形式です。 アプリケーション オブジェクト ツリー (AOT) にジョブというノードがあります。 この例を [ジョブ] ノードの下に追加して、ジョブを実行することができます。

```xpp
static void JobRs001a_HelloWorld(Args _args)
{
    if (1 == 1) 
    {
        // These two info() calls are identical to the X++ compiler.
        // The second form is the one typically used in X++.
        Global::info("Hello World, 1.");
        info('Hello World, 2.');
    }
    if (1 != 1)
    {
        error("This message will not appear.");
    }
    else
    {
        // These two methods are also from the Global class.
        // The + operator concatenates two strings.
        warning("This is like info, but is for warnings, 3.");
        error("This is like info, but is for errors, 4.");
    }
}
```

##### <a name="output"></a>出力

情報ログ ウィンドウからの出力を次に示します: メッセージ (09:49:48) Hello World、1。
Hello World、2。
これは、情報のようなものですが、警告、3 です。
これは、情報のようなものですが、エラー、4 です。

#### <a name="c-sample"></a>C# サンプル

次の C# プログラムは、以前の X++ プログラムを書き直したものです。 

```csharp
using System;
class Pgm_CSharp
{
    static void Main( string[] args )
    {
        new Pgm_CSharp().Rs001a_CSharp_HelloWorld();
    }
    void Rs001a_CSharp_HelloWorld()
    {
        if (1 == 1) 
        {
            Console .Out .WriteLine("Hello World, Explicit .Out , 1.");
            Console .WriteLine("Hello World, Implicit default to .Out , 2.");
        }
        if (1 != 1)
        {
            Console .Error .WriteLine("This message will not appear.");
        }
        else
        {
            Console .Error .WriteLine(".Error is like .Out, but can be for warnings, 3.");
            Console .Error .WriteLine(".Error is like .Out, but is for errors, 4.");
        }
    }
}
```

##### <a name="output"></a>出力

C# コンソールへの実際の出力を次に示します。

```Console
Hello World, Explicit .Out, 1. 
Hello World, Implicit default to .Out, 2. 
.Error is like .Out, but can be for warnings, 3. 
.Error is like .Out, but is for errors, 4.
```

## <a name="x-c-comparison-loops"></a>X++、C# の比較: ループ
このセクションでは、X++ と C\# の間のループの特徴を比較します。

###  <a name="similarities"></a>類似点

次の機能は、X++ と C\# で同じです。
-   int プリミティブ データ型の変数の宣言。 他のプリミティブ型の宣言はほとんど同じですが、型の名前が異なる可能性があります。
-   ループ用 while ステートメント。
-   ループを終了する break ステートメント。
-   ループの先頭に移動するための continue ステートメント。
-   <= (以下) 比較演算子です。

###  <a name="differences"></a>違い

次のテーブルは、C# では異なる X++ の機能を示しています。

| 機能 | X++ | C# | コメント |
|---|---|---|---|
| `for` ステートメント。| for 明細書はループで使用できます。| C# `for` ステートメントは、X++ の `for` と少し異なります。| C# では、`for` ステートメントでカウンター整数を宣言できます。 ただし X++ では、カウンターは `for` ステートメントの外側で宣言する必要があります。|
|++ 増分の演算子。|++ 増分の演算子は X++ で利用可能です。 ただし、++ で修飾された <strong>int</strong> 変数は式としてではなく、ステートメントとしてのみ使用できます。 たとえば、次の X++ コードの行はコンパイルしません。<br>`int age=42;`<br> `print age++;`<br> ただし、次の X++ コードの行はコンパイルします。<br>`int age=42;`<br>`age++; print age;`|C# 演算子は、X++ での方が柔軟です。|次のコード行は、両方の言語で同じです。<ul><li>++ myInteger;</li><li>myInteger++;</li></ul>ただし、次のコード行は互いに異なる効果を持ち、C# でのみ有効です。<ul><li>yourInt = ++myInt;</li><li>yourInt = myInt++;</li></ul>|
| 剰余演算子。| X++ では、剰余演算子は mod です。| C# では、剰余演算子は % です。| モジュロ演算子のシンボルは異なりますが、その動作は両方の言語で同じです。|
| 既に開始されているコンソール プログラムを一時的に中断します。| `pause` ステートメント。| C# では、コマンド ライン プログラムを次のコード行で一時停止することができます。<br>`Console.In.Read();`| X++ では、モーダル ダイアログ ボックスで OK ボタンをクリックして続行します。 C# では、キーボードの任意のキーボードを押して続行します。|
| メッセージを表示します。| X++ では、`print` ステートメントは印刷ウィンドウにメッセージを表示します。| C# では、次のコード行でメッセージをコンソールに表示することができます。<br>`Console.WriteLine();`| X++ `print` 関数は、テスト時にのみ使用されます。 `print` を使用する X++ プログラムは、ほとんどの場合コード内のどこか後で `pause` 明細書を使用します。 生産 X++ コードについては、`print` の代わりに Global::info メソッドを使用します。 `strfmt` 関数はしばしば `info` と一緒に使用されます。 `info` の後に `pause` を使用する理由はありません。|
| 音を作成します。| ビープ音機能は、人間に聞こえる音を鳴らします。 | C# では、聞こえるサウンドが次のコード行で発行されます。<br>`Console.Beep();`| ステートメントはそれぞれ短いトーンを作ります。|


### <a name="print-and-globalinfo"></a>Print および Global::info

ループ用の X++ コード サンプルは、`print` 関数を使用して結果を表示します。 X++ では、`print` ステートメントを使用して、まず文字列に変換する関数を呼び出すことなく、任意のプリミティブ データ型を表示できます。 これにより、簡単なテスト環境では `print` が便利になります。 一般に、Global::info メソッドは `print` より頻繁に使用されます。 `info` メソッドは文字列のみを表示できます。 したがって、strfmt 関数はしばしば `info` と一緒に使用されます。 印刷ウィンドウの内容をクリップボードにコピー (Ctrl+C などで) できない `print` の制限。 Global::info は情報ログ ウィンドウに書き込みをし、クリップボードへのコピーをサポートします。

### <a name="example-1-the-while-loop"></a>例 1: While Loop

**while** キーワードは、X++ と C# 両方でのループをサポートします。

#### <a name="x-sample-of-while"></a>X++ while のサンプル

```xpp
static void JobRs002a_LoopsWhile(Args _args)
{
    int nLoops = 1;
    while (nLoops <= 88)
    {
        print nLoops;
        pause;
        // The X++ modulo operator is mod.
        if ((nLoops mod 4) == 0)
        {
            break;
        }
        ++ nLoops;
    }
    beep(); // Function.
    pause; // X++ keyword.
} 
```

##### <a name="output"></a>出力

X++ 印刷ウィンドウの出力は次のようになります。

```xpp
1
2
3
4
```

#### <a name="c-sample-of-while"></a>C# 中のサンプル

```csharp
using System;
public class Pgm_CSharp
{
    static void Main( string[] args )
    {
        new Pgm_CSharp().WhileLoops();
    }

    void WhileLoops()
    {
        int nLoops = 1;
        while (nLoops <= 88)
        {
            Console.Out.WriteLine(nLoops.ToString());
            Console.Out.WriteLine("(Press any key to resume.)");
            // Paused until user presses a key.
            Console.In.Read();
            if ((nLoops % 4) == 0) {
                break;
            }
            ++ nLoops;
        }
        Console.Beep();
        Console.In.Read();
    }
}
```
 
##### <a name="output"></a>出力

C# プログラムのコンソール出力は次のとおりです。

```Console
1
(Press any key to resume.)
2
(Press any key to resume.)
3
(Press any key to resume.)
4
(Press any key to resume.)
```

### <a name="example-2-the-for-loop"></a>例 2: For Loop

**for** キーワードは、X++ と C# 両方でのループをサポートします。

#### <a name="x-sample-of-for"></a>X++ for のサンプル

X++ では、カウンター変数は **for** ステートメントの一部として宣言できません。

```xpp
static void JobRs002a_LoopsWhileFor(Args _args)
{
    int ii; // The counter.
    for (ii=1; ii < 5; ii++)
    {
        print ii;
        pause;
        // You must click the OK button to proceed beyond a pause statement.
        // ii is always less than 99.
        if (ii < 99)
        {
            continue;
        }
        print "This message never appears.";
    }
    pause;
}
```
 
##### <a name="output"></a>出力

X++ 印刷ウィンドウの出力は次のようになります。

```xpp
1
2
3
4
```

#### <a name="c-sample-of-for"></a>C# のサンプル

```csharp
using System;
public class Pgm_CSharp
{
    static void Main( string[] args )
    {
        new Pgm_CSharp().ForLoops();
    }
    void ForLoops()
    {
        int nLoops = 1, ii;
        for (ii = 1; ii < 5; ii++)
        {
            Console.Out.WriteLine(ii.ToString());
            Console.Out.WriteLine("(Press any key to resume.)");
            Console.In.Read();
            if (ii < 99)
            {
                continue;
            }
            Console.Out.WriteLine("This message never appears.");
        }
        Console.Out.WriteLine("(Press any key to resume.)");
        Console.In.Read();
    }
}
```
 
##### <a name="output"></a>出力

C# プログラムのコンソール出力は次のとおりです。

```Console
1
(Press any key to resume.)
2
(Press any key to resume.)
3
(Press any key to resume.)
4
(Press any key to resume.)
(Press any key to resume.)
```

### <a name="x-c-comparison-switch"></a>X++、C# の比較: Switch

X++ と C# の両方では、**switch** ステートメントに、キーワード **case**、**break**、および **default** があります。 次のテーブルは、X++ および C\# の間の **switch** ステートメントの相違点を示しています。

| 機能  | X++ | C# | コメント |
|--------|-----------|------------|-----|
| 各 case ブロックの末尾の `break;`       | X++ では、いずれかの **case** ブロックが **switch** 句の式の値と一致する場合、`break;` ステートメントに達するまで他のすべての **case** および **default** ブロックが実行されます。 `break;` ステートメントは、X++ の **switch** ステートメントでは必要ありませんが、`break;` ステートメントはほとんどすべての実践的な状況において重要です。 | C\# では、`break;` ステートメントが **case** または **default** ブロックのステートメントの後に常に必要になります。 **ケース** 句に次の **ケース** 句との間のステートメントがない場合、2 つの **ケース** 節の間に `break;` ステートメントは必要ありません。 | コードを編集する次のプログラマが混乱する可能性があるので、case **ブロック** の後の `break;` ステートメントを省略することをお勧めしません。 |
| **既定** ブロックの末尾の `break;` | X++ では、`break;` ステートメントを **default** ブロックの最後に追加する効果はありません。   | C\# では、コンパイラは **default** ブロックの最後に `break;` ステートメントを必要とします。 | 詳細については、「明細書の切り替え」を参照してください。 |
| **case** ブロックの定数値のみ     | X++ では、case ブロックでリテラル値または変数のいずれかを指定できます。 たとえば、ケース myInteger: を書き込むことができます。  | C\# では、**case** ブロックごとに正確に 1 つのリテラル値を指定する必要があり、変数は許可されていません。 | コメントはありません。  |
| 1 つの **case** ブロックにある複数の値        | X++ では、case ブロックごとに複数の値を指定できます。 値は、コンマで区切る必要があります。 たとえば、`case 4,5,myInteger:` を書き込むことができます。    | C\# では、**case** ブロックごとに正確に 1 つの値を指定する必要があります。 | X++ では、1 つまたは複数の case ブロックの最後にある `break;` ステートメントを省略するよりも、**case** ブロックに複数の値を書き込む方が適切です。 |

### <a name="code-examples-for-switch"></a>切り替えのコードの例

次のセクションでは、X++ と C\# での比較可能な switch ステートメントを示します。

#### <a name="x-switch-example"></a>X++ 切り替えの例

以下に、X++ スイッチの例を示します。
-   `case iTemp:` および `case (93-90):` は、**case** 式が C\# のように、定数に限定されないことを示します。
-   `//break;` は、 X++ では `break;` ステートメントが必須ではないことを示していますが、ほとんどの場合望ましいです。
-   `case 2, (93-90), 5:` は、X++ の 1 つの **case** 句に複数の式をリストできることを示します。

```xpp
static void GXppSwitchJob21(Args _args)  // X++ job in AOT &gt; Jobs.
{
    int iEnum = 3;
    int iTemp = 6;
    switch (iEnum)
    {
        case 1:
        case iTemp:  // 6
            info(strFmt("iEnum is one of these values: 1,6: %1", iEnum));
            break;
        case 2, (93-90), str2Int("5"):  // Equivalent to three 'case' clauses stacked, valid in X++.
            //case 2:
            //case (93-90):  // Value after each 'case' can be a constant, variable, or expression; in X++.
            //case str2Int("5"):
            info(strFmt("iEnum is one of these values: 2,3,5: %1", iEnum));
            //break;  // Not required in X++, but usually wanted.
        case 4:
            info(strFmt("iEnum is one of these values: 4: %1", iEnum));
            break;
        default:
            info(strFmt("iEnum is an unforeseen value: %1", iEnum));
            break;
            // None of these 'break' occurrences in this example are required for X++ compiler.
    }
    return;
}

/*** Copied from the Infolog:
Message (02:32:08 pm)
iEnum is one of these values: 2,3,5: 3
iEnum is one of these values: 4: 3
***
```

#### <a name="c-switch-example"></a>C# 切り替えの例

以下に、C\# スイッチの例を示します。
-   case 1: には、**case** 句では定数式のみを指定できることを説明したコメントがあります。
-   `break;` ステートメントは、 C\# で必要とされるステートメントを持つ各 **case** ブロックの最後のステートメントの後に発生します。

```csharp
using System;
namespace CSharpSwitch2
{
    class Program
    {
        static void Main(string[] args)  // C#
        {
            int iEnum = 3;
            switch (iEnum)
            {
                case 1:  // Value after each 'case' must be a constant.
                case 6:
                    Console.WriteLine("iEnum is one of these values: 1,6: " + iEnum.ToString());
                    break;
                //case 2,3,5:  // In C# this syntax is invalid, and multiple 'case' clauses are needed.
                case 2:
                case 3:
                case 5:
                    Console.WriteLine("iEnum is one of these values: 2,3,5: " + iEnum.ToString());
                    break;
                case 4:
                    Console.WriteLine("iEnum is one of these values: 4: " + iEnum.ToString());
                    break;
                default:
                    Console.WriteLine("iEnum is an unforeseen value: " + iEnum.ToString());
                    break;
                // All 'break' occurrences in this example are required for C# compiler.
            }
          return;
        }
    }
}
/*** Output copied from the console:
>> CSharpSwitch2.exe
iEnum is one of these values: 2,3,5: 3
>>
***/
```
 
## <a name="x-c-comparison-string-case-and-delimiters"></a>X++、C# の比較: 文字列の大文字小文字の区別および区切り記号
このセクションでは、X++ と C\# の混合ケーシングによる文字列の処理を比較します。 また、X++ で使用できる文字列の区切り記号についても説明します。

### <a name="similarities"></a>類似点

次の X++ 機能は C\# の機能と同じです。
-   バックスラッシュ (\\) は、文字列の区切り記号のエスケープ演算子です。
-   アット マーク (@) は、文字列の開始引用符の直前に書かれていると、バックスラッシュのエスケープ効果を無効にします。
-   プラス記号 (+) は文字列連結演算子です。

### <a name="differences"></a>違い

C\# では異なる X++ 機能を以下の表に一覧表示します。

| 機能 | X++ | C# | コメント |
|---|---|---|---|
| `== `比較演算子| 区別しない: `==` 演算子は文字列の大文字と小文字の差異を区別しません。| C# では、`==` 演算子は文字列の大文字と小文字の差異を区別します。| X++ では、文字列間の大文字と小文字の比較には strCmp 関数を使用できます。|
| 文字列の区切り記号| X++ では、文字列の区切り記号として単一引用符 (') または二重引用符 (`"`) のいずれかを使用できます。<p><strong>注記</strong>: ユーザーに公開される可能性のある文字列に、二重引用符を使用することを推奨しています。 ただし、二重引用符文字が文字列の文字のいずれかである場合、単一引用符で文字列を区切るのが便利です。</p>| C# では、文字列の区切り記号として二重引用符を使用する必要があります。 これは、タイプ `System.String` を指します。| X++ および C# では、リテラル文字列の区切り記号を埋め込み、\ でエスケープするオプションがあります。 <br>X++ では、エスケープを使用しなくても、二重引用符で区切られた文字列に単一引用符 (または逆) を埋め込むことで代用することもできます。|
| 文字区切り文字| X++ には文字列データ型 (`str`) がありますが、文字の種類はありません。| C# では、文字の区切り記号として単一引用符を使用する必要があります。 これは、タイプ `System.Char` を指します。| .NET Framework では、長さが 1 の `System.String` は `System.Char` 文字とは異なるデータ型です。|

### <a name="example-1-case-sensitivity-of-the--operator"></a>例 1: Case Sensitivity of the == オペレーター

次の例に示すように、`==` と != 演算子は、X++ では大文字と小文字が区別されませんが、C\# では区別されます。

| X++    | C#  | コメント       |
|----------------|---------|-----------|
| `"HELLO" == "hello"` <br>X++ の場合も同様です。 | `"HELLO" == "hello"` <br>C# の False。 | X++ と C# の間の異なるケース比較。 |

### <a name="example-2-the--string-concatenation-operator"></a>例 2: The + 文字列連結オペレーター

+ および = 演算子は、次の表の例に示すように、X++ と C\# の両方で文字列を連結するために使用されます。

| X++  | C#   | コメント |
|---------|--------------------|----------------------------|
| `myString1 = "Hello" + " world";` <br>結果は等しくなります: <br>`myString1 == "Hello world"`  | (X++ と同じです。) | X++ と C# の両方では、+ 演算子の動作はオペランドのデータ型によって異なります。 演算子は、文字列を連結したり、数値を追加します。 |
| `mystring2 = "Hello";` <br>`myString2 += " world";` <br>結果は等しくなります: `myString2 == "Hello world"` | (X++ と同じです。) | X++ と C# の両方では、次のステートメントは同じです。 <br>`a = a + b;` <br>`a += b;`  |

### <a name="example-3-embedding-and-escaping-string-delimiters"></a>例 3: 文字列の区切り記号を埋め込みおよび分離

X++ の文字列を区切るには、単一または二重引用符を使用できます。 エスケープ文字 (\\) は、区切り記号を文字列に埋め込むために使用できます。 この点については、次のテーブルを参照してください。

| X++ | C#         | コメント   |
|---------|-----|--------------------------------------|
| `myString1 = "He said \"yes\".";` <br>結果: <br>`He said "yes".`  | (X++ と同じです。)  | エスケープ文字を使用すると、文字列の区切り記号を文字列に埋め込むことができます。   |
| `myString2 = 'He said "yes".';` <br>結果: <br>`He said "yes".`  | C# 構文では、文字列を区切るための単一引用符は使用できません。    | ユーザーにより表示される場合のある文字列については、次の例で示すように、単一引用符ではなくエスケープ文字を使用するためのベスト プラクティスと見なされます。   |
| `myString3 = "He said 'yes'.";` <br>結果: <br>`He said 'yes'.` | (X++ と同じです。) | X++ では、文字列が単一引用符の区切り記号で始まらない限り、単一引用符は区切り記号として扱われません。 C# では、単一引用符に文字列の特別な意味はなく、文字列を区切るために使用することはできません。 C# では、単一引用符は型 `System.Char` のリテラルに必要な区切り記号です。 X++ には文字データ型がありません。 |
| `str myString4 = 'C';` <br>ここで、単一引用符は文字列の区切り記号です。 | `char myChar4 = 'C';` <br>ここで、単一引用符は `System.String` 区切り記号ではなく、`System.Char` 区切り記号です。 | X++ には .NET Framework の `System.Char` に対応するデータ型はありません。 長さが 1 に制限されている X++ 文字列は、まだ文字列であり、文字データ型ではありません。 |

### <a name="example-4-single-escape-character"></a>例 4: 単一のエスケープ文字

入力または出力の単一のエスケープ文字を示す例を次の表に示します。

| X++    | C# | コメント     |
|-----------------------|--------|------------------|
| `myString1 = "Red\ shoe";` <br>結果: <br>`Red shoe`     | C# のリテラル文字列には、"\ " のようにエスケープの後にスペースが続く 2 つの文字シーケンスを含めることはできません。 コンパイラ エラーが発生します。 | X++ コンパイラは、連続した 2 文字の "\" を検出すると、その 1 つのエスケープ文字は切り捨てます。 |
| `myString2 = "Red\\ shoe";` <br>結果: <br>`Red\ shoe` | (X++ と同じです。)  | エスケープ文字のペアにおいて、1 文字目は 2 文字目の特別な意味をなくします。     |

## <a name="comparison-array-syntax"></a>比較: 配列の構文

X++ と C\# の配列の機能と構文には類似点と相違点があります。

### <a name="similarities"></a>類似点

X++ と C# の配列の構文と処理は、全体的にかなり似ています。 ただし、多くの違いがあります。

### <a name="differences"></a>違い

次のテーブルは、X++ と C#で異なる配列の [] 構文の領域を示しています。

| カテゴリ | X++ | C# | コメント |
|---|---|---|---|
| 申告| 配列は変数名に追加され角カッコ付きで宣言されています。| 配列はデータ型に追加され角カッコ付きで宣言されています。| `int myInts[]; // X++` <p><strong>注記</strong>: X++ 配列をメソッド内のパラメーターにすることはできません。</p><p>`int[] myInts; // C#`</p>|
| 申告| 配列の構文は、`int` や `str` などのプリミティブ データ型のみをサポートします。 構文はクラスまたはテーブルをサポートしていません。|配列の構文は、プリミティブ データ型およびプリミティブ クラスをサポートします。| X++ では、配列のオブジェクトに `Array` 配列を使用できます。|
| 申告| X++ は一次元配列に制限されます (myStrings[8])。| C# は多次元配列 (myStrings[8,3]) およびジャグ配列 (myStrings[8][3]) のサポートを追加しました。| X++ では、配列の配列を持つことはできません。 ただし、大規模な配列が消費できる有効なメモリの量を制限する高度な構文があり、それは C#: int intArray[1024,16]; で多次元構文のように見えます。 詳細については、「ベスト プラクティス パフォーマンスの最適化: ディスクへの配列スワップ」を参照してください。|
| 申告| X++ では、配列は特別なコンストラクトですが、オブジェクトではありません。| C# では、すべての配列が構文の違いに関係なくオブジェクトです。| X++ には配列クラスがありますが、その基本的なメカニズムは [] 構文を使用して作成された配列とは異なります。 C# では、すべての配列が `System.Array` クラスの [] 構文がコード内で使用されているかに関係なく、同じ基本的なメカニズムを使用します。|
| 期間| X++ では、静的サイズの配列の長さは宣言構文で決定されます。| C# では、配列のサイズは配列オブジェクトが構築されたときに決定されます。| X++ で [] 宣言構文を使用するときは、配列に値を割り当てるとき、その前にこれ以上の準備は必要ありません。 <br>C# では、配列を宣言して作成してから代入する必要があります。|
| 期間| X++ 配列は、開始した後でも増加できる動的長さを持つことができます。 これは配列が [] 内に数字なしで宣言されている場合にのみ適用されます。 動的配列の長さが何回も増加した場合、パフォーマンスが低下する可能性があります。| C# では、長さの設定後に配列の長さを変更することはできません。| X++ コードの次のフラグメントでは、`myInts` 配列のみが動的にサイズを大きくできます。 <br>`int myInts[];` <br>`int myBools[5];` <br>`myInts[2] = 12;` <br>`myInts[3] = 13;` <br>`myBools[6] = 26; //Error`|
| 期間| `dimOf` 機能を使用することにより、一部の配列の長さを取得することができます。| C# の配列は `Length` プロパティを持つオブジェクトです。| コメントはありません。|
| インデックスの作成中| 配列インデックスは 1 ベースです。| 配列インデックスは 0 ベースです。| mtIntArray[0] は X++ ではエラーとなります。|
| 定数| X++ で、定数値は <strong>#define</strong> プリコンパイラ ディレクティブを使用することで最適に実現されます。| C# では、キーワード <strong>const</strong> を使用して変数の宣言を修飾して定数値を実現できます。| X++ には <strong>const</strong> キーワードがありません。 C# は、#define プリコンパイラ ディレクティブによって作成される変数に値を割り当てることができません。|

### <a name="x-and-c-samples"></a>X++ および C\# のサンプル

次のコード例は、プリミティブ データ型の配列の処理方法を示しています。 最初のサンプルは X++ で、2 番目のサンプルは C\# にあります。 両方のサンプルで同じ結果が得られます。

#### <a name="x-sample"></a>X++ サンプル

```xpp
static void JobRs005a_ArraySimple(Args _args)
{
    #define.macroArrayLength(3)
    // Static length.
    str sSports[#macroArrayLength];
    // Dynamic length, changeable during run time.
    int years[];
    int xx;
    Global::warning("-------- SPORTS --------");
    sSports[#macroArrayLength] = "Baseball";
    for (xx=1; xx <= #macroArrayLength; xx++)
    {
        info(int2str(xx) + " , [" + sSports[xx] + "]");
    }
    warning("-------- YEARS --------");
    years[ 4] = 2008;
    years[10] = 1930;
    for (xx=1; xx <= 10; xx++)
    {
        info(int2str(xx) + " , " + int2str(years[xx]));
    }
}
```

##### <a name="output"></a>出力

情報ログへの出力は次のとおりです。

```xpp
Message (14:16:08)
-------- SPORTS --------
1 , []
2 , []
3 , [Baseball]
-------- YEARS --------
1 , 0
2 , 0
3 , 0
4 , 2008
5 , 0
6 , 0
7 , 0
8 , 0
9 , 0
10 , 1930
```

#### <a name="c-sample"></a>C\# サンプル

```csharp
using System;
public class Pgm_CSharp
{
    static public void Main( string[] args )
    {
        new Pgm_CSharp().ArraySimple();
    }
    private void ArraySimple()
    {
        const int const_iMacroArrayLength = 3;
        // In C# the length is set at construction during run.
        string[] sSports;
        int[] years;
        int xx;
        Console.WriteLine("-------- SPORTS --------");
        sSports = new string[const_iMacroArrayLength];
        sSports[const_iMacroArrayLength - 1] = "Baseball";
        for (xx=0; xx < const_iMacroArrayLength; xx++)
        {
            Console.WriteLine(xx.ToString() + " , [" + sSports[xx] + "]");
        }
        Console.WriteLine("-------- YEARS --------");
        // In C# you must construct the array before assigning to it.
        years = new int[10];
        years[ 4] = 2008;
        years[10 - 1] = 1930;
        for (xx=0; xx < 10; xx++)
        {
            Console.WriteLine(xx.ToString() + " , [" + years[xx].ToString() + "]");
        }
    }
} // EOClass
```

##### <a name="output"></a>出力

C# プログラムからコマンド ライン コンソールへの出力は次のとおりです。

```Console
-------- SPORTS --------
0 , []
1 , []
2 , [Baseball]
-------- YEARS --------
0 , [0]
1 , [0]
2 , [0]
3 , [0]
4 , [2008]
5 , [0]
6 , [0]
7 , [0]
8 , [0]
9 , [1930]
```

## <a name="additional-array-like-x-features"></a>追加の配列のような X++ 機能

**コンテナー** は、X++ で利用できる特別なデータ型です。 配列と類似したもの、または `List` コレクションと類似したものとみなすことができます。

## <a name="comparison-collections"></a>比較: コレクション
Finance and Operations アプリケーションでは、X++ `List` コレクション クラスを使用できます。 C# で使用されている .NET Framework には、`System.Collections.Generic.List` と似た名前のクラスがあります。

### <a name="comparing-the-use-of-the-list-classes"></a>リスト クラスの使用の比較

次のテーブルは、X++ `List` クラスのメソッドと .NET Framework および C\# の `System.Collections.Generic.List` のメソッドを比較しています。

| 機能 | X++ | C# | コメント |
|---|---|---|---|
| コレクションの宣言| `List myList;`| `List<string> myList;`| X++ 宣言には、格納する要素のタイプは含まれません。|
| 反復子の宣言|`ListIterator iter`<br>`ListEnumerator enumer;`| IEnumerator&lt;文字列&gt; iter;| X++ では、`ListIterator` オブジェクトに `List` の項目を `insert` および `delete` できるメソッドがあります。 X++ `ListEnumerator` は、`List` の内容を変更することはできません。 X++ では、`ListEnumerator` オブジェクトは常に `List` と同じ層で作成されます。 これは、必ずしも `ListIterator` に当てはまるわけではありません。|
| 反復子の取得|`new ListIterator (myList)`<br>`myList.getEnumerator()`| `myList.GetEnumerator()`| X++ と C# の両方では、リスト オブジェクトに、関連付けられている列挙子の getter メソッドがあります。|
| コンストラクター| `new List(Types::String)`| `new List<string>()`|`List` クラス内に格納するオブジェクトのタイプに関する情報は、X++ と C# の両方でコントラクターに付与されます。|
| データの更新|列挙子 – `List` 内の品目が追加または削除された場合、列挙子は無効になります。<br>反復子 – 反復子には `List` の項目を挿入および削除するメソッドがあります。 反復子は有効なままです。| 列挙子 – `List` 内の品目が追加または削除された場合、列挙子は無効になります。| X++ と C# の両方で、項目が `List` から追加または削除された後、列挙子は無効になります。|
| データの更新| X++ では、`List` クラスにリストの開始または最後に項目を追加するメソッドがあります。| C# では、`List` クラスにリスト内の任意の位置にメンバーを追加するためのメソッドがあります。 また、任意の場所から項目を削除するメソッドもあります。| X++ では、反復子でのみ項目を `List` から削除できます。|

### <a name="example-1-declaration-of-a-list"></a>例 1: リストの宣言

`List` コレクションを宣言する X++ および C# のコード例を次に示します。

```xpp
// X++
List listStrings ,list2 ,listMerged;
ListIterator literator;
```

```csharp
// C#
using System;
using System.Collections.Generic;
List<string> listStrings ,list2 ,listMerged; IEnumerator<string> literator;
```

### <a name="example-2-construction-of-a-list"></a>例 2: リストの作成

どちらの言語でも、構築の時点でコレクションが格納する項目のタイプを指定する必要があります。 クラス タイプでは、X++ はタイプがクラス (Types::Class) であるかどうかよりも具体的でないものを取得します。 次に示すのが X++ および C# のコード例です。

```xpp
// X++
listStrings = new List( Types::String );
```

```csharp
// C#
listStrings = new List<string>;
```

### <a name="example-3-add-items-to-a-list"></a>例 3: リストに品目を追加

X++ と C# 両方では、コレクションはコレクションの末尾に項目を追加するメソッドと、最初に項目を挿入するメソッドを提供します。 C# では、コレクションは指数値に基づいてコレクション内の任意の時点で挿入するためのメソッドを提供します。 X++ では、コレクションの反復子によって現在の位置に項目を挿入できます。 次に示すのが X++ および C# のコード例です。

```xpp
// X++
listStrings.addEnd ("StringBB."); 
listStrings.addStart ("StringAA.");
// Iterator performs a midpoint insert at current position. 
listIterator.insert ("dog");
```

```csharp
// C#
listStrings.Add ("StringBB."); 
listStrings.Insert (0 ,"StringAA.");
// Index 7 determines the insertion point.
listStrings.Insert (7 ,"dog");
```

### <a name="example-4-iterate-through-a-list"></a>例 4: リストを繰り返す

X++ と C\# にはイテレータ クラスがあり、次の例に示すように、コレクション内の項目のステップを活用できます。 

```xpp
// X++
literator = new ListIterator (listStrings); 
// Now the iterator points at the first item.

// The more method answers whether 
// the iterator currently points 
// at an item. 
while (literator.more()) 
{ 
    info(any2str (literator.value())); 
    literator.next(); 
}
```

```csharp
// C#
literator = listStrings .GetEnumerator(); 
// Now enumerator points before the first item, not at the first item.

// The MoveNext method both advances the item pointer, and 
// answers whether the pointer is pointing at an item. 
while (literator.MoveNext()) 
{ 
    Console.WriteLine (literator.Current); 
}
```

### <a name="example-4b-foreach-in-c"></a>例 4b: C\# の foreach

C\# では、よく **foreach** キーワードを使用して、一覧の反復のタスクを簡略化します。 次のコード例は、以前の C\# の例と同じように動作します。 

```csharp
foreach (string currentString in listStrings)
{ 
    Console.WriteLine(currentString);
}
```

###  <a name="example-5-delete-the-second-item"></a>例 5: 2 番目の項目を削除

次のコード例では、コレクションの 2 つ目の項目が削除されます。 X++ では、これに反復子が必要になります。 C\# では、コレクション自体が項目を削除するメソッドを提供します。

```xpp
// X++
literator.begin(); 
literator.next(); 
literator.delete();
```

```csharp
// C#
listStrings.RemoveAt(1);
```

###  <a name="example-6-combine-two-collections"></a>例 6: 2 つのコレクションを結合

次のコード例では、2 つのコレクションの目次を 1 つに結合しています。

```xpp
// X++
listStrings = List::merge(listStrings ,listStr3);
// Or use the .appendList method:
listStrings.appendList (listStr3);
```

```csharp
// C#
listStrings.InsertRange(listStrings.Count ,listStr3);
```

## <a name="comparison-collections-of-keys-with-values"></a>比較: 値を持つキーのコレクション

Finance and Operations アプリケーションでは、`Map` コレクション クラスを使用できます。 `Map` コレクションには、値のペア (キー値とデータ値の組み合わせ) が保持されます。 これは、`System.Collections.Generic.Dictionary` という名前の .NET Framework クラスに似ています。

### <a name="similarities"></a>類似点

次のリストは、キーと値のペアを格納するコレクションに関する X++ と C\# の類似点について説明します。
-   どちらも重複するキーを防止します。
-   どちらも列挙子 (または反復子) を使用して項目をループします。
-   両方のキー値コレクション オブジェクトは、キーと値として格納されているタイプの指定で作成されます。
-   どちらもクラス オブジェクトを格納でき、**int** のようなプリミティブの格納に限定されません。

### <a name="differences"></a>違い

次のテーブルは、キーと値のペアを格納するコレクション クラスに関する X++ と C\# の違いを示しています。

| 機能        | X++     | C#  | コメント |
|---|---|---|---|
| キーの重複 | X++ では、`Map` クラスが `insert` メソッドに対する呼び出しを、キーに関連付けられている値のみを更新する操作として暗黙的に扱うことにより、重複キーを防止します。 | C\# では、重複キーを追加しようとすると `Dictionary` クラスが例外をスローします。 | 異なる技術ではあるが、両方の言語で重複するキーが防止されます。               |
| 品目の削除   | X++ では、反復子オブジェクトで `delete` メソッドを使用して、不要なキーと値のペアを `Map` から削除します。    | C\# では、`Dictionary` クラスに `remove` メソッドがあります。      | どちらの言語でも、列挙子は列挙子の有効期間中にコレクション項目数が変更された場合は無効になります。 |

### <a name="example-1-declaration-of-a-key-value-collection"></a>例 1: キー値のコレクションの宣言

どちらの言語でも、キー値コレクションが格納する項目のタイプを指定する必要があります。 X++ では、型は構築時に指定されます。 C\# では、宣言時と構築時の両方で型が指定されています。 次に示すのが X++ および C# のコード例です。

```xpp
// X++
Map mapKeyValue;
MapEnumerator enumer;
MapIterator mapIter;
```

```csharp
// C#
Dictionary<int,string> dictKeyValue;
IEnumerator<SysCollGen.KeyValuePair<int,string>> enumer;
KeyValuePair<int,string> kvpCurrentKeyValuePair;
```

### <a name="example-2-construction-of-the-collection"></a>例 2: コレクションの作成

どちらの言語でも、構築中にキー値コレクションが格納する項目のタイプが指定されます。 クラス タイプでは、X++ はタイプがクラス (Types::Class) であるかどうかよりも具体的でないものを取得します。 次に示すのが X++ および C# のコード例です。

```xpp
// X++
mapKeyValue = new Map(Types::Integer, Types::String);
```

```csharp
// C#
dictKeyValue = new Dictionary<int,string>();
```

### <a name="example-3-add-an-item-to-the-collection"></a>例 3: 品目をコレクションに追加

X++ と C\# のキー値コレクションに項目を追加する方法は、次のコード例に示すように、ほとんど違いがありません。

```xpp
// X++
mapKeyValue.insert(xx ,int2str(xx) + “_Value”);
```

```csharp
// C#
dictKeyValue.Add(xx ,xx.ToString() + “_Value”);
```

### <a name="example-4-iterate-through-a-key-value-collection"></a>例 4: キー値のコレクションを反復

列挙子は、次のコード例に示すように、キー値コレクションを X++ と C\# の双方でループ処理するために使用されます。

```xpp
// X++ 
enumer = mapKeyValue.getEnumerator();
while (enumer.moveNext())
{
    iCurrentKey = enumer.currentKey();
    sCurrentValue = enumer.currentValue();
    // Display key and value here.
}
```

```csharp
// C#
enumer = dictKeyValue.GetEnumerator();
while (enumer.MoveNext())
{
    kvpCurrentKeyValuePair = enumer.Current;
    // Display .Key and .Value properties=
    // of kvpCurrentKeyValuePair here.
}
```

### <a name="example-5-update-the-value-associated-with-a-key"></a>例 5: キーに関連付けられている値を更新

構文は、指定されたキーに関連付けられた値を更新するために 2 つの言語で全く異なります。 キー 102 のコード例を次に示します。

```xpp
// X++
mapKeyValue.insert(
    102 ,
    ”.insert(), Re-inserted” + ” key 102 with a different value.”);
```

```csharp
// C#
dictKeyValue[102] = 
    “The semi-hidden .item property in C#, Updated the value for key 102.”;
```

### <a name="example-6-delete-one-item"></a>例 6: 1つの品目を削除

構文は、2 つの言語間でコレクション メンバーを反復しながら、コレクションから 1 つのキーと値のペアを削除する方法が全く異なります。 キー 102 のコードの例は次のとおりです。

```xpp
// X++
mapIter = new MapIterator(mapKeyValue);
//mapIter.begin();
while (mapIter.more())
{
    iCurrentKey = mapIter.key();
    if (104 == iCurrentKey)
    {
        // mapKeyValue.remove would invalidate the iterator.
        mapIter.delete();
        break;
    }
    mapIter.next();
}
```

```csharp
// C#
dictKeyValue.Remove(104);
```

## <a name="comparison-exceptions"></a>比較: 例外
いくつかの類似点がありますが、X++ と C\# の間の例外関連の動作を比較すると、多くの違いがあります。 **try**、**catch**、**throw** キーワードは、X++ と C# で同じように動作します。 ただし、スローされキャッチされる例外のタイプは 2 つの言語で異なります。

### <a name="similarities"></a>類似点

例外機能に関する X++ と C\# の類似点には、次が含まれます。
-   どちらの言語も同じ **try** キーワードを持っています。
-   どちらも同じ **catch** キーワードを持っています。
-   両方とも特定の例外を指定しない **catch** ステートメントを有効にします。 このような **catch** ステートメントは、それに到達するすべての例外を検出します。
-   どちらも同じ **throw** キーワードを持っています。

### <a name="differences"></a>違い

X++ と C\# 間の例外関連の違いは、次のテーブルで説明します。

| 機能 | X++ | C# | コメント |
|---|---|---|---|
| <strong>再試行</strong>| 関連付けられた <strong>try</strong> ブロックの最初の命令にジャンプします。 詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。| <strong>再試行</strong> キーワードの機能は C# コードでは真似できますが、対応するキーワードはありません。| X++ のみ、<strong>再試行</strong>キーワードがあります。 C# には対応がありません。 詳細については、X++、C# の比較: 例外後の再試行の自動化を参照してください。|
| <strong>最終的に</strong>| `finally` キーワードは、`try` および `catch` キーワードの後に使用することがサポートされます。| <strong>finally</strong> キーワードは、<strong>try</strong> および <strong>catch</strong> ブロックに従うコードのブロックをマークします。 例外がスローされたかキャッチされたかどうかに関係なく、確定が実行されます。| セマンティクスは C# のセマンティクスと同じです。|
| 特定の固有| X++ では、例外は、**エラー**、**デッドロック**、または **CodeAccessSecurity** など `Exception` 列挙型の要素です。 別のものを含めることができる例外はありません。| C# では、例外は `System.Exception` 基本クラスまたは継承された任意のクラスのインスタンスです。 スローされた例外の `InnerException` プロパティに例外を含めることができます。| X++ では、スローされた各例外は Exception 列挙型の値です。 詳細については、「例外列挙」を参照してください。|
| 例外メッセージ| X++ では、例外が発生したときに作成されるメッセージは情報ログでのみ使用でき、そのメッセージは例外に直接関連付けられません。| C# では、メッセージは `System.Exception` オブジェクトの `Message` のメンバーです。| X++ では、Global::error メソッドは情報ログで例外メッセージを表示するメカニズムです。 詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。|
| 例外条件| X++ では、まだ何も代入されていないオブジェクト変数でインスタンス メソッドを呼び出すとエラーが発生します。 ただし、このエラーと共に例外は発生しません。 したがって、割り当てられていない変数が `try` ブロックで誤用されても、`catch` ブロックは制御を獲得できません。 次のコード例では、コード `box4.toString();` で発生したエラーにより、コントロールは任意の `catch` ブロックに移行しません。`DialogBox box4;` `try` { ` box4.toString();` ` info("toString did not error, but expected an error.");` } catch (Exception::Error) // これを検出する例外値はありません。 { ` info("Invalid use of box4 gave control to catch, unexpected.");` }| C# では、初期化されていない変数がオブジェクト参照として扱われる場合、`System.NullReferenceException` が発生します。| 例外を発生させる条件にはいくつかの相違点があります。|
| SQL トランザクション| X++ で、SQL 例外が <strong>ttsBegin</strong> - <strong>ttsCommit</strong> トランザクションで発生する場合、そのトランザクション ブロック内の <strong>catch</strong> ステートメントは例外を処理できます。| C# では、SQL トランザクション内部の catch ブロックは例外を検出できます。| |

### <a name="examples"></a>例

次の X++ 機能が示されています。
-   **試行** キーワード。
-   **catch** キーワード。
-   Exception::Error 例外が発生した後の動作。

#### <a name="x-example"></a>X++ 例

```xpp
// X++
static void JobRs008a_Exceptions(Args _args)
{
    str sStrings[4];
    int iIndex = 77;
    try
    {
        info("On purpose, this uses an invalid index for this array: " + sStrings[iIndex]);
        warning("This message does not appear in the Infolog," + " it is unreached code.");
    }
    // Next is a catch for some of the values of
    // the X++ Exception enumeration.
    catch (Exception::CodeAccessSecurity)
    {
        info("In catch block for -- Exception::CodeAccessSecurity");
    }
    catch (Exception::Error)
    {
        info("In catch block for -- Exception::Error");
    }
    catch (Exception::Warning)
    {
        info("In catch block for -- Exception::Warning");
    }
    catch
    {
        info("This last 'catch' is of an unspecified exception.");
    }
    //finally
    //{
    //    //Global::Warning("'finally' is not an X++ keyword, although it is in C#.");
    //}
    info("End of program.");
}
```

 
##### <a name="output"></a>出力

情報ログ ウィンドウからの出力を次に示します。

```xpp
Message (18:07:24)
Error executing code: Array index 77 is out of bounds.
Stack trace
(C)\Jobs\JobRs008a_Exceptions - line 8
In catch block for -- Exception::Error
End of program.
```

#### <a name="c-sample"></a>C# サンプル

次の C\# プログラムは、以前の X++ プログラムを書き直したものです。

```csharp
// C#
using System;
public class Pgm_CSharp
{
    static void Main( string[] args )
    {
        new Pgm_CSharp().Rs008a_CSharp_Exceptions();
    }
    void Rs008a_CSharp_Exceptions()
    {
        //str sStrings[4];
        string[] sStrings = new string[4];
        try
        {
            Console.WriteLine("On purpose, this uses an invalid index for this array: " + sStrings[77]);
            Console.Error.WriteLine("This message does not appear in the Infolog, it is unreached code.");
        }
        catch (NullReferenceException exc)
        {
            Console.WriteLine("(e1) In catch block for -- " + exc.GetType().ToString() );
        }
        catch (IndexOutOfRangeException exc)
        {
            Console.WriteLine("(e2) In catch block for -- " + exc.GetType().ToString() );
        }
        // In C#, System.Exception is the base of all
        // .NET Framework exception classes.
        // No as yet uncaught exception can get beyond
        // this next catch.
        catch (Exception exc)
        {
            Console.WriteLine("This last 'catch' is of the abstract base type Exception: "
                + exc.GetType().ToString());
        }
        // The preceding catch of System.Exception makes this catch of
        // an unspecified exception redundant and unnecessary.
        //catch
        //{
        //    Console.WriteLine("This last 'catch' is"
        //        + " of an unspecified exception.");
        //}
        finally
        {
            Console.WriteLine("'finally' is not an X++ keyword, although it is in C#.");
        }
        Console.WriteLine("End of program.");
    }
} // EOClass
```

 
##### <a name="output"></a>出力

C\# コンソールへの出力を次に示します。

```Console
(e2) In catch block for -- System.IndexOutOfRangeException
'finally' is not an X++ keyword, although it is in C#.
End of program.
```

## <a name="comparison-automated-retry-after-an-exception"></a>比較: 例外後の自動再試行
場合によっては、実行時に発生する例外の原因を修正する catch ブロックでコードを記述できます。 X++ には **catch** ブロック内でのみ使用することができる **retry** キーワードが用意されています。 **retry** キーワードを使用すると、問題が **catch** ブロック内のコードにより修正されるとプログラムが **try** ブロックの先頭に戻ることができます。 C# には **再試行** キーワードがありません。 ただし、同等の動作を提供するよう C# コードを書き込むことができます。

### <a name="code-samples-for-retry"></a>再試行のためのコード サンプル

次の X++ サンプル プログラムは、Exception::Error を発生させます。 これは、最初に無効なインデックス値を使用して `sStrings` 配列から要素を読み取ろうとするときに発生します。 例外がキャッチされると、**catch** ブロック内で、実行時に是正措置が行われます。 その後再試行ステートメントは、**try** ブロックの最初のステートメントに戻ります。 この 2 回目の繰り返しは、例外が発生することなく動作します。

```xpp
static void JobRs008b_ExceptionsAndRetry(Args _args)
{
    str sStrings[4];
    str sTemp;
    int iIndex = 0;

    sStrings[1] = "First array element.";
    try
    {
        print("At top of try block: " + int2str(iIndex));
        sTemp = sStrings[iIndex];
        print( "The array element is: " + sTemp );
    }
    catch (Exception::Error)
    {
        print("In catch of -- Exception::Error (will retry)." + " Entering catch.");
        ++iIndex;
        print("In catch of -- Exception::Error (will retry)." + " Leaving catch.");
        // Here is the retry statement.
        retry;
    }
    print("End of X++ retry program.");
    pause;
}
```

#### <a name="output"></a>出力

印刷ウィンドウへの出力を次に示します。

```xpp
At top of try block: 0
In catch of -- Exception::Error (will retry). Entering catch.
In catch of -- Exception::Error (will retry). Leaving catch.
At top of try block: 1
The array element is: First array element.
End of X++ retry program.
```

### <a name="c-sample"></a>C# サンプル

次の C\# サンプルは、以前の X++ サンプルからの行ごとの変換ではありません。 代わりに、C\# プログラムには X++ プログラムが依存している **retry** のキーワードの動作に似た別の構造体があります。 **try** および **catch** ブロックは、呼び出されたメソッドにあります。 **try** ブロックで使用される変数は、caller 側メソッドに格納されます。 呼び出し元メソッドは、変数を **ref** キーワードで修飾されたパラメーターとして渡し、呼び出されたメソッドの **catch** ブロック内で値を修正できます。 呼び出されたメソッドはすべての例外を取得し、**ブール値** を返して、2 番目の呼び出しが必要かどうかを呼び出し元に返信します。

```csharp
// C#
using System;
public class Pgm_CSharp
{
    static void Main(string[] args)
    {
        new Pgm_CSharp() .Rs008b_CSharp_ExceptionsAndRetry();
    }
    void Rs008b_CSharp_ExceptionsAndRetry() // Caller
    {
        int iIndex = -1
            , iNumRetriesAllowed = 3;
        bool bReturnCode = true; // Means call the callee method.
        for (int xx=0; xx <= iNumRetriesAllowed; xx++)
        {
            if (bReturnCode)
            {
                bReturnCode = this.Rs008b_CSharp_ExceptionsAndRetry_Callee(ref iIndex);
            }
            else
            {
                break;
            }
        }
        Console.WriteLine("End of C# caller method.");
    }
    
    private bool Rs008b_CSharp_ExceptionsAndRetry_Callee(ref int iIndex)
    {
        bool bReturnCode = true; // Means call this method again.
        string[] sStrings = new string[4];
        string sTemp;
        sStrings[0] = "First array element.";
        try
        {
            Console.WriteLine("At top of try block: " + iIndex.ToString());
            sTemp = sStrings[iIndex];
            Console.WriteLine( "The array element is: " + sTemp );
            bReturnCode = false; // Means do not call this method again.
        }
        catch (Exception)
        {
            Console.WriteLine("In catch of -- Exception. Entering catch.");
            ++iIndex; // The 'ref' parameter in C#.
            Console.WriteLine("In catch of -- Exception. Leaving catch.");
            //retry;
            // In C# we let the caller method do the work
            // that the retry keyword does in X++.
        }
        Console.WriteLine("End of C# callee method.");
        return bReturnCode;
    }
}
```

 
#### <a name="output"></a>出力

コンソールへの出力を次に示します。

```Console
At top of try block: -1
In catch of -- Exception. Entering catch.
In catch of -- Exception. Leaving catch.
End of C# callee method.
At top of try block: 0
The array element is: First array element.
End of C# callee method.
End of C# caller method.
```

## <a name="comparison-operators"></a>比較: 演算子
このセクションでは、X++ と C\# の間のループの演算子を比較します。

### <a name="assignment-operators"></a>代入演算子

次のテーブルは、X++ と C\# の代入演算子の違いを示しています。

| X++ および C# | 違い |
|---|---|
| `=`| X++ では、この演算子によって、<strong>int64</strong> から <strong>int</strong> に代入する場合など、精度が損なわれる可能性がある場合は必ず暗黙的な変換が発生します。ただし、C# では、この代入により、コンパイル エラーが発生します。|
| `+=` および `-=`| 唯一の違いは、C# ではこれらの演算子もデリゲート操作で使用されることです。|
| ++ および --| これらは、両方の言語のインクリメント演算子およびデクリメント演算子です。 次の行は、両方の言語で同じです。<br>`++myInteger;`<br>ただし X++ では、これら 2 つの演算子は式ではなくステートメントに対して使用できます。 したがって、次の行は X++ でコンパイル エラーを生成します。<br>`myStr = int2str(++myInteger);`<br>`myIntA = myIntBB++;`|

### <a name="arithmetic-operators"></a>算術演算子

次のテーブルに、算術演算子の一覧を示します。

|X++ および C# | 違い |
|---|---|
| *| 乗算演算子との違いはありません。<p><strong>注記</strong>: アスタリスクは、X++言語の一部である SQL ステートメントにも使用されます。 これらの SQL ステートメントでは、アスタリスクを次のいずれかに設定できます。</p><ul><li>すべての列を返す必要があることを示すワイルドカード。</li><li><strong>LIKE</strong> 句で使用される文字列の文字のワイルドカード。</li></ul>|
| `/`| 除算演算子は、X++ と C# で同じです。|
| `MOD`| 剰余工程については、唯一の違いは % 記号が C# で使用されることです。|
| +| 加算演算子は、X++ と C# で同じです。 プラス記号は文字列の連結にも使用されます。 この演算子は、数値を追加し、両方の言語で文字列を連結します。 |
| -| 減算演算子は、X++ と C# で同じです。|


### <a name="bitwise-operators"></a>ビット演算子

次のテーブルは X++ と C\# の間のビット演算子を比較しています。


| X++ および C\# |                     違い                      |
|-------------|------------------------------------------------------|
|  &lt;&lt;   | 左シフト演算子は、X++ と C\# で同じです。  |
|  &gt;&gt;   | 右シフト演算子は、X++ と C\# で同じです。 |
|      ~      | ビットの NOT 演算子は、X++ と C\# で同じです。 |
|      &      | バイナリの AND 演算子は、X++ と C\# で同じです。  |
|      ^      | バイナリの XOR 演算子は、X++ と C\# で同じです。  |
|             |                                                      |

### <a name="relational-operators"></a>リレーショナル演算子

次のリレーショナル演算子は、X++ と C\# で同じです。
-   `==`
-   `<=`
-   `<=`
-   `>`
-   `<`
-   `!=`
-   `&&`
-   `||`
-   `!`
-   `? :`

## <a name="comparison-events"></a>比較: イベント

X++ と C# がイベントデザインパターンを実装する方法にはいくつかの違いがあります。 詳細については、「イベント用語とキーワード」を参照してください。

### <a name="comparison-of-events-between-x-and-c"></a>X++ と C\# 間のイベントの比較

委任が X++ と C# の各イベントに使用される方法には違いがあります。

| 概念 | X++ | C# | コメント|
|---|---|---|---|
| <strong>デリゲート</strong>| X++ では、デリゲートはクラスのメンバーとしてのみ宣言できます。 デリゲートは、テーブルのメンバーであることはできません。 すべてのデリゲートはそのクラスのインスタンス メンバーであり、<strong>静的</strong>メンバーではありません。 すべてのデリゲートは<strong>保護された</strong>メンバーであるため、デリゲートの宣言で使用できるアクセス修飾子はありません。 したがって、イベントは、デリゲートがメンバーである同じクラス内のコードによってのみ呼び出すことができます。 ただし、デリゲートのプライベート性質の 1 つの例外は、そのクラス以外のコードが、+= および -= 演算子を使用してデリゲートで操作できることです。| C# では、各<strong>デリゲート</strong>は、すべて<strong>クラス</strong>が 1 つの型であるように 1 つの型です。 デリゲートは、任意のクラスとは別に宣言されます。 <strong>イベント</strong> キーワードがない場合、パラメーター タイプとしてクラスを設定することができるように、メソッドのパラメーター タイプとしてデリゲートを設定することができます。 デリゲートのインスタンスを構築して、パラメーター値を渡すことができます。| X++ では、各クラスは型ですが、デリゲートは型ではありません。 デリゲートのインスタンスをコンストラクトすることはできません。 メソッドのパラメーターに設定できるデリゲートはありません。 ただし、デリゲート メンバーを持つクラスを作成し、クラスのインスタンスをパラメーター値として渡すことができます。 詳細については、「X++ キーワード」を参照してください。|
| <strong>イベント</strong>| X++ コードでは、イベントは次のいずれかです。<ul><li>デリゲートを明示的に呼び出します。</li><li>メソッドの開始または終了。</li></ul>X++ には <strong>event</strong> キーワードがありません。| C# では、<strong>event</strong> キーワードを使用して<strong>デリゲート</strong>型をクラスのメンバーとして宣言します。 <strong>イベント</strong> キーワードの結果は、委任を確認する<strong>protected</strong> を委任することですが、+= および -= 演算子にはアクセスできます。 += 演算子を使用して、<strong>イベント</strong> に対するイベント ハンドラー メソッドを申し込むことができます。 メソッドに関数ポインターをパラメータとして渡す手法として<strong>デリゲート</strong>は、<strong>イベント</strong>キーワードなしで役立ちます。| メソッドの開始前およびメソッドの終了後に発生する自動イベントは、AOT の使用によってのみサブスクライブできます。|
| += および -= 演算子| X++ では、+= 演算子を使用して<strong>デリゲート</strong>に対するメソッドをサブスクライブします。 -= 演算子は、デリゲートからメソッドのサブスクライブを解除します。| C# では、+= 演算子を使用して、<strong>event</strong> キーワードとともに使用されていない<strong>イベント</strong>、または<strong>デリゲート</strong>にメソッドをサブスクライブします。| デリゲートには、デリゲートにサブスクライブされたメソッドを持つすべてのオブジェクトへの照会が含まれています。 これらのオブジェクトはガベージ コレクションの対象外ですが、デリゲートはそれらの参照を保持します。|
| `eventHandler`| X++ で、+= や -= の演算子を使用してデリゲートからメソッドをサブスクライブまたはサブスクライブ解除を行う場合、<strong>eventHandler</strong> キーワードが必要です。| `System.EventHandler` は、.NET Framework のデリゲート タイプです。| この用語は、C# または .NET Framework の場合とは異なる方法で、X++ で使用されます。 詳細については、「X++ キーワード」を参照してください。|

### <a name="x-example"></a>X++ 例

X++ の例で注目すべき重要なことは次のとおりです。

-   `XppClass` には、`myDelegate` という名前のデリゲート メンバーが含まれます。

    > [!NOTE]
    > AOT にはデリゲートのノードが含まれています。 このノードは、AOT > クラス > XppClass > myDelegate にあります。 いくつかのイベント ハンドラー ノードは、myDelegate ノードの下に配置できます。 AOT ノードによって表されるイベント ハンドラーは、実行時に -= オペレーターによって削除できません。

-   デリゲート宣言の末尾の {} カッコは必要ですが、カッコにコードを所持することはできません。
-   `XppClass` には、パラメーター シグネチャがデリゲートと互換性を持つ 2 つのメソッドがあります。 １ つの方法は静的です。
-   2 つの互換メソッドは、+= 演算子と **eventHandler** キーワードを使用してデリゲートに追加されます。 これらのステートメントはイベント ハンドラー メソッドを呼び出さず、ステートメントはデリゲートにメソッドを追加するだけです。
-   デリゲートへの 1 回の呼び出しでイベントが発生します。
-   デリゲートに渡されたパラメーター値は、各イベント ハンドラー メソッドによって受け取られます。
-   サンプルの一番上にある短い X++ ジョブがテストを開始します。

```xpp
// X++
// Simple job to start the delegate event test.
static void DelegateEventTestJob()
{
    XppClass::runTheTest("The information from the X++ job.");
}
// The X++ class that contains the delegate and the event handlers.
class XppClass
{
    delegate void myDelegate(str _information)
    {
    }
    public void myEventSubscriberMethod2(str _information)
    {
        info("X++, hello from instance event handler 2: " + _information);
    }
    static public void myEventSubscriberMethod3(str _information)
    {
        info("X++, hello from static event handler 3: " + _information);
    }
    static public void runTheTest(str _stringFromJob)
    {
        XppClass myXppClass = new XppClass();
        // Subscribe two event handler methods to the delegate.
        myXppClass.myDelegate += eventHandler(myXppClass.myEventSubscriberMethod2);
        myXppClass.myDelegate += eventHandler(XppClass::myEventSubscriberMethod3);
        // Raise the event by calling the delegate one time,
        // which calls all the subscribed event handler methods.
        myXppClass.myDelegate(_stringFromJob);
    }
}
```

以前の X++ ジョブの出力は次のとおりです。

```xpp
X++, hello from static event handler 
3: The information from the X++ job. X++, hello from instance event handler 
2: The information from the X++ job.
```

### <a name="c-sample"></a>C# サンプル

このセクションには、以前の X++ サンプルのイベント設計パターンの C\# コード サンプルが含まれています。

```csharp
// C#
using System;
// Define the delegate type named MyDelegate.
public delegate void MyDelegate(string _information);
public class CsClass
{
    protected event MyDelegate MyEvent;
    static public void Main()
    {
        CsClass myCsClass = new CsClass();
        // Subscribe two event handler methods to the delegate.
        myCsClass.MyEvent += new MyDelegate(myCsClass.MyEventSubscriberMethod2);
        myCsClass.MyEvent += new MyDelegate(CsClass.MyEventSubscriberMethod3);
        // Raise the event by calling the event one time, which
        // then calls all the subscribed event handler methods.
        myCsClass.MyEvent("The information from the C# Main.");
    }
    public void MyEventSubscriberMethod2(string _information)
    {
        Console.WriteLine("C#, hello from instance event handler 2: " + _information);
    }
    static public void MyEventSubscriberMethod3(string _information)
    {
        Console.WriteLine("C#, hello from static event handler 3: " + _information);
    }
}
```

以前の C\# サンプルの出力は次のとおりです。

```Console
CsClass.exe C#, hello from instance event handler 
2: The information from the C\# Main. C\#, hello from static event handler 
3: The information from the C\# Main.
```

### <a name="events-and-the-aot"></a>イベントおよび AOT

AOT 内の品目のみに適用する他のイベント システムがあります。 詳細については、「AOT でのイベント ハンドラー ノード」を参照してください。

## <a name="comparison-precompiler-directives"></a>比較: プリコンパイラのディレクティブ

X++ および C# はプリコンパイラー ディレクティブ構文の一部のキーワードを共有しますが、意味は常に同じではありません。

### <a name="similarities"></a>類似点

X++ および C\# コンパイラは、同じキーワードの多くを認識します。 ほとんどの場合、キーワードは両言語のコンパイラに対して同じ意味を持ちます。

### <a name="differences"></a>違い

X++ と C\# でのプリコンパイラ ディレクティブの基本的な違いは、両方の言語プリコンパイラが認識できる\#定義キーワードです。 C\# とは異なり、X++ では \#define ディレクティブではその構文にドットを必要とします。 X++ では、定義済の記号に値を指定するために丸かっこを使用できます。 これらの違いを次の例に示します。
-   X++: \#define.InitialYear(2003)
-   C\#: \#define InitialYear

小さな差異は、C\# では、\# 文字とディレクティブ キーワード (\# テストの定義など) の間にスペースとタブ文字があることです。

### <a name="identical-keywords"></a>同一であるキーワード

次のテーブルは、X++ および C\# で同様のプリコンパイラ ディレクティブを示しています。

| キーワード | X++ | C# | コメント |
|---|---|---|---|
| `#define` | X++ では、プリコンパイラ変数名を定義でき、その変数に値を指定できます。                | C\# では、プリコンパイラ変数名を定義できますが、その変数に値を指定できません。 また、\#C での定義\#はファイルの先頭になければならず、using ステートメントやクラス宣言などのコードの後には出現できません。 | C\# コンパイラは、C\# コード ファイルで変数を定義しなくても、`/define` のコマンドライン パラメーターを入力し、プリコンパイラ変数名を定義できます。 X++ コンパイラには、`/define` に相当するものはありません。 |
|`#if`     | X++ では、\#if がプリコンパイラ変数が存在するかどうかと、変数に指定された値があるかどうかを特定できます。 | C\# では、\#if はプリコンパイラ変数が存在するかどうかのみ特定できます。 値が割り当てられないため、任意の値のテストはできません。 |      |
| `#endif`  | X++ では、\#endif が \#if ブロックの終了を示します。 また、\#ifnot ブロックも終了します。   | C\# では、ブロックに \#else が含まれるかに関係なく、\#endif を \#if ブロックの最後に記述します。       |   |

### <a name="different-keywords-with-the-same-processing-result"></a>同じ処理結果を持つ異なるキーワード

次のテーブルは、X++ および C\# で異なる名前が付けられているが、処理時に同じ結果を与えるプリコンパイラ ディレクティブを示しています。

| X++ | C# | コメント |
|---|---|---|
| \#ifnot                     | \#if \#else      | X++ には \#else ディレクティブはありませんが、\#ifnot は同様の機能を提供します。 X++ では、\#ifnot がプリコンパイラ変数が存在するかどうかと、変数に指定された値がないかどうかを特定できます。 C\# では、\#if は ‘!’ の場合にプリコンパイラ変数が存在するかどうかを特定できます。 symbol は変数名に対する接頭語になります。 |
| `//BP Deviation documented` | \#pragma 警告 | これら X++ エントリと C\# エントリは等価ではありませんが、部分的な類似性があります。 どちらもコンパイラの警告メッセージを抑制します。                    |
| \#macrolib                  | C++ 内の .HPP ファイル | X++ ディレクティブ \#macrolib と C++ の .HPP ファイルの間には部分的な類似点があります。 両方とも複数の\#定義ステートメントを含めることができます。            |

### <a name="precompiler-directives-exclusive-to-x"></a>X++ 限定のプリコンパイラ ディレクティブ

次のテーブルは、C\# に直接対応するものがない X++ プリコンパイラ ディレクティブを示しています。

| X++                  | コメント    |
|---|---|
| \#linenumber         | \# 行番号ディレクティブは、情報ログに出力できるように、行番号を取得するために使用します。 <br>C\# ディレクティブ \# 行は、その目的が行番号を設定することであるため異なります。 |
| \#defdec \#definc    |         |
| \#globaldefine       | X++ では、\#globaldefine と \#define はわずかに違います。 違いは、\#globaldefine は、\#define によってプリコンパイラ変数に割り当てられた現在の非 null 値を上書きしないことです。 <br>C\# ではプリコンパイラの変数名は値を指定することができないため、C\# はこの違いと大きく異なっています。 |
| \#localmacro \#マクロ | X++ では、\#localmacro を使用すると、プリコンパイラ変数に複数行の値を代入できます。 \#マクロは同義語ですが、 \#localmacro をお勧めします。 <br>C\# では、\#define ディレクティブにこの機能の一部がありますが、プリコンパイラ変数に値を代入できません。      |
| \#globalmacro        | X++ では、\#globalmacro は優先 \#localmacro とほぼ同じです。          |

## <a name="comparison-object-oriented-programming"></a>比較: オブジェクト指向プログラミング
X++ のオブジェクト指向プログラミング (OOP) の原則は、C\# と異なります。

### <a name="conceptual-comparisons"></a>概念の比較

次のテーブルは、X++ と C\# の間の OOP の原則の実装を比較しています。

|機能|X++|C#|コメント|
|---|---|---|---|
| キャスティング | X++ 言語には、キーワード <strong>is</strong> および <strong>as</strong> があり、ダウンキャストを安全かつ明示的にするために使用されます。 **ヒント**: X++ では、基本クラス変数を派生クラス変数にダウンキャストするときに、<strong>as</strong> キーワードを使用する必要はありません。 ただし、すべてのダウンキャスト ステートメントで <strong>as</strong> キーワードを使用することをお勧めします。| オブジェクトは継承パスを上または下にキャストすることができます。 ダウンキャストは <strong>as</strong> キーワードを必要とします。| X++ キーワード <strong>is</strong> および <strong>as</strong> の詳細については、式の演算子: 継承の Is および As を参照してください。|
| ローカル関数| メソッドには、ゼロ以上のローカル関数用の宣言およびコードの本文を含めることができます。 そのメソッドのみローカル関数を呼び出すことができます。| C# 3.0 では、匿名関数およびローカル関数といくつかの類似点を持つラムダ式をサポートしています。 ラムダ式は、デリゲートでよく使用されます。| |
| メソッドのオーバーロード | メソッドのオーバーロードはサポートされません。 メソッド名は、クラスごとに 1 回のみ発生する場合があります。| メソッドのオーバーロードはサポートされています。 メソッド名は、それぞれのケースで異なるパラメーターシグネチャを使用して、1 つのクラスで複数回発生する場合があります。| X++ はメソッドでの省略可能パラメーターをサポートしています。 省略可能なパラメーターは、メソッドのオーバーロードを部分的に反映できます。 詳細については、この表の、「オプション パラメーターの行」を参照してください。|
| メソッドのオーバーライド | メソッドのオーバーライドはサポートされています。 派生クラスは、パラメータの署名がどちらの場合も同じ限り、基本クラスと同じ名前のメソッドを持つことができます。 唯一の例外は、オーバーライドするメソッドがパラメーターに既定値を追加できることです。| メソッドのオーバーライドはサポートされています。 派生クラスでメソッドを上書きするには、<strong>virtual</strong> キーワードをメソッドに適用する必要があります。| 上書きするメソッドの概念には、メソッド名、そのパラメーター署名および戻り値の型が含まれています。 メソッドのオーバーライドの概念は、基準メソッドとオーバーライド メソッドがこれらの側面のいずれかで異なる場合は適用されません。|
| オプションのパラメーター| パラメーター宣言の後に既定値の割り当てを実行できます。 メソッド呼び出し元には、そのパラメーターの値を渡すか、既定値を受け入れるようにパラメーターを無視するかの選択肢があります。 このメソッドは、同じメソッド名への 2 回の呼び出しが異なる数のパラメーターを渡すことができるため、メソッドのオーバーロードに似ています。 既定値を持つ各パラメーターは、既定値を持たない最後のパラメーターに従う必要があります。| オプションのパラメーターは、<strong>params</strong> キーワードによりサポートされます。 呼び出しの表示ポイントから<strong>パラメーター</strong>キーワードが無くても、メソッドのオーバーロードは、部分的に同様の機能を提供できます。| 詳細については、「パラメーターとスコープおよびオプションのパラメーターの使用」を参照してください。|
| 単一の継承| AOT では、クラスの classDeclaration ノード内で <strong>extends</strong> キーワードを使用することにより、X++ クラスを他の X++ クラスから派生させることができます。 別のクラスから暗黙的に直接派生するクラスはありません。 クラスを `Object` クラスから直接派生させる場合は、<strong>拡張</strong>キーワードを使用する必要があります。 <strong>extends</strong> キーワード上では 1 つのクラスのみを指定することができます。<br><br>**注意**: 他のクラスが派生する X++ 基本クラスを変更する場合は、コンパイル フォワードを使用してその基本クラスを再コンパイルする必要があります。 このオプションを使用すると、派生クラスも再コンパイルされます。 派生クラスも再コンパイルされるようにするには、基本クラス ノードを右クリックし、[アドイン] > [コンパイル フォワード] をクリックします。 [ビルド] > [コンパイル] のクリック (または F7 キーを押すこと) という代わりの方法では、基底クラスを変更できない場合があります。<br><br>クラスは、ゼロから多くのインターフェイスを実装できます。 <br><br>X++ テーブルは `Common` テーブル、および `xRecord` クラスから暗黙的に継承します。| 別のクラスから派生するために C# は<strong>拡張</strong>キーワードを使用します。 すべての .NET Framework クラスは明示的に別のクラスから派生しない限り、`System.Object` クラスから暗黙的に派生しています。| |

### <a name="keyword-comparisons"></a>キーワードの比較

次のテーブルは、X++ および C＃ の OOP 関連のキーワードを示しています。

|キーワード|X++|C#|コメント|
|---|---|---|---|
| <strong>抽象</strong>| | | 差異はありません。|
| <strong>クラス</strong>| 修飾子 <strong>パブリック</strong> と <strong>プライベート</strong> はクラス宣言で無視されます。 クラスの名前空間グループ化の概念はありません。 どのクラス名にもピリオド (.) はありません。| 修飾子 <strong>パブリック</strong> と <strong>プライベート</strong> を使用してクラス宣言を変更できます。 C＃にはキーワード<strong>内部</strong>があります。このキーワードは、クラスがアセンブリ ファイル内でグループ化されている方法が関連付けられています。| <strong>protected</strong> クラスの概念はなく、クラスの <strong>protected</strong> メンバーのみあります。|
| <strong>拡張</strong>| クラス宣言は、<strong>拡張</strong>キーワードを利用して、別のクラスから継承できます。| <strong>拡張</strong>および<strong>実装</strong>などのキーワードが X++ で使用される場合、コロン (:) が使用されます。| |
| <strong>最終</strong>| <strong>最終</strong>メソッドは、派生クラスで上書きすることはできません。 <strong>最終</strong>クラスは拡張できません。| クラスのキーワード <strong>シールド</strong> は、<strong>最終</strong> が X++クラスで意味するのと同じことを意味します。| |
| <strong>実装</strong>| クラス宣言では、<strong>実装</strong>キーワードを利用して、<strong>インターフェイス</strong>を実装することができます。| | |
| <strong>インターフェイス</strong>| <strong>インターフェイス</strong>はクラスで実装する必要があるメソッドを指定できます。| <strong>インターフェイス</strong>はクラスで実装する必要があるメソッドを指定できます。| |
| <strong>新規</strong>| <strong>new</strong> キーワードは、クラスの新しいインスタンスを割り当てるために使用されます。 コンストラクターは自動で呼び出されます。 各クラスには、厳密に 1 つのコンストラクターがあり、コンストラクターの名前は `new` です。 コンストラクターが入力するパラメーターを決定することができます。| <strong>new</strong> キーワードは、クラスの新しいインスタンスを作成するために使用されます。 コンストラクターは自動で呼び出されます。 コンストラクターのメソッド自体は `new` という名前ではなく、クラスと同じ名前です。<p><strong>注記</strong>: <strong>新しい</strong> キーワードはメソッドに使用することも可能で、メソッドがベースクラスの同じメソッドを上書きする方法を変更します。</p> | X++ と C# はどちらもコードで明示的に記述されたコンストラクターを持たないクラスの既定のコンストラクターであると想定します。|
| <strong>NULL</strong>| | | 差異はありません。|
| <strong>プライベート</strong>および<strong>保護</strong>| <strong>private</strong> および <strong>protected</strong> キーワードは、クラス メンバーの申告を変更するために使用できます。| <strong>private</strong> および <strong>protected</strong> キーワードは、クラス メンバーの申告を変更するために使用できます。||
| <strong>パブリック</strong>| <strong>パブリック</strong>の既定のアクセス レベルを持つ<strong>パブリック</strong>、<strong>保護</strong>、または<strong>プライベート</strong>で変更されないメソッド。| <strong>プライベート</strong>の既定のアクセス レベルを持つ<strong>パブリック</strong>、<strong>保護</strong>、または<strong>プライベート</strong>で変更されないメソッド。||
| <strong>静的</strong>| メソッドは<strong>静的</strong>にできますが、フィールドはできません。| メソッドとフィールドの両方を<strong>静的</strong>にすることができます。| |
| <strong>スーパー</strong>| <strong>super</strong> キーワードは、基本クラスで同じメソッドにアクセスするために派生クラスで使用されます。 `void method2()`<br>`{`<br>`    // Call method2 method`<br> `    // on the base class.`<br> `    super();` <br>`}`<br>| <strong>base</strong> キーワードは、基本クラスのさまざまなメソッドにアクセスするために派生クラスで使用されます。 <br>`void method2()` <br>`{`<br> `    // Call methods on`<br> `    // the base class.`<br> `    base.method2();`<br> `    base.method3();` <br>`}`| C# では、<strong>ベース</strong>を使用して基本コンストラクターを呼び出すための特別な構文があります。|
| <strong>この</strong>| 同じオブジェクトで 1 つのインスタンス メソッドから別への呼び出しで、呼び出されたメソッドの修飾子が必要です。 キーワード <strong>これ</strong> は現在のオブジェクトの修飾子として使用できます。| 同じオブジェクトで 1 つのインスタンス メソッドから別への呼び出しで、呼び出されたメソッドの修飾子は必要ではありません。 ただし、<strong>この</strong>キーワードは現在のオブジェクトの修飾子として使用できます。 実際、キーワード <strong>this</strong> は IntelliSense の情報を表示することで役に立ちます。| |
| `finalize`| `Object` クラスには、`finalize` メソッドが含まれます。 `finalize` メソッドは<strong>最終</strong>でないため、オーバーライドできます。 `finalize` メソッドは、C# では `System.Object.Finalize` メソッドと似ているように見えますが、X++ では `finalize` メソッドにはどのような特別な意味もありません。 オブジェクへの最後の参照がオブジェクトの参照を停止した場合、オブジェクトはメモリから自動的に削除されます。 たとえば、これは、最後の参照がスコープ外になるまたは参照する他のオブジェクトが割り当てられる場合に、発生する可能性があります。| `Finalize` と `Dispose` メソッドはいくつかのタイプのクラスで共通です。 ガベージ コレクターは、破棄して処理するときに、`Finalize` メソッドと `Dispose` メソッドを呼び出します。| C# では、.NET Framework の `System.GC.Collect` メソッドを呼び出してガベージ コレクターを開始できます。 X++ には確定的なガベージ コレクターが使用されているため、X++ には似たような機能はありません。|
| `main`| メニューから呼び出されるクラスには、システムによって呼び出される `main` メソッドがあります。| コマンド ライン コンソールから呼び出されるクラスには、システムによって呼び出される `Main` メソッドがあります。| |

## <a name="comparison-classes"></a>比較: クラス
.NET frameworkで C\# を使用すると、クラスは名前空間にグループ分けされます。 各名前空間では、ファイル操作やリフレクションなどの機能区分に焦点を当てます。 ただし、X++ のクラスを使用する場合、名前空間のようなグループ分けは表示されません。

### <a name="comparison-classes-about-reflection"></a>比較: リフレクションに関するクラス
X++ では、`TreeNode` クラスがアプリケーション オブジェクト ツリー (AOT) へのアクセスを提供します。 `TreeNode` クラスは、X++ におけるリフレクション機能の中心です。 `TreeNode` クラスとそのメソッドは、C\# が使用する .NET Framework において `System.Reflection` 名前空間と比較できます。

次のテーブルに、C\# コードを書くときに利用できるいくつかのクラスを示します。 これらは、.NET Framework クラスです。 このテーブルでは、すべての C\# クラスは、特に指定のない限り `System.Reflection` 名前空間にあります。 各行では、対応するクラスまたはクラス メンバーを示し、X++ コードを記述する際に利用します。

|X++|C#|コメント|
|---|---|---|
| `TreeNode` | `System .Assembly`   | アセンブリは C\# プログラムがリフレクション情報を収集する必要がある場合に使用する最初のクラスです。 X++ クラスの静的メソッド `TreeNode` は、X++ におけるリフレクションの開始点です。    |
| `TreeNode` | `System .Type`       | `TreeNode` のインスタンス メソッドは、`System.Type` のインスタンス メソッドに対応します。                |
| `TreeNode .AOTgetSource`         | `MethodInfo`         | `AOTgetSource` メソッドは、いくつかの情報を 1 つの文字列でまとめて返します。 これには、メソッドの X++ ソース コードが含まれます。 対照的に、`MethodInfo` には各情報に対する個別のメンバーがあります。                  |
| `TreeNode .AOTfirstChild` `TreeNode .AOTnextSibling` `TreeNode .AOTiterator` `AOTiterator` | MethodInfo\[\] (配列)   | C\# では、`System.Type` の `GetMethods` メソッドは MethodInfo オブジェクトの配列を返します。 インデクサーをインクリメントする一般的な手法により、配列の間をループことができます。 対照的に、X++ モデルは、AOT のツリー コントロールを移動するためのものです。 `AOTfirstChild` および `AOTnextSibling` の `TreeNode` メソッドは、ナビゲーションを実行します。 同等の代替として X++ `AOTiterator` クラスは、AOT のツリー コントロールをナビゲートするように設計されています。 クラス ノードは、いくつかのメソッド ノードの親です。 `AOTiterator` は、子ノードを順番に進み、それぞれ別の `TreeNode` インスタンスとして返します。 `AOTparent` および `AOTprevious` という名前の追加のリソース `TreeNode` メソッド。 |
| `TreeNode .AOTgetProperty` `TreeNode .AOTgetProperties` `TreeNode .AOTname`                | `PropertyInfo`       | X++ では、`AOTgetProperties` メソッドは `TreeNode` のすべてのプロパティの名前と値のペアを含む長い文字列を返します。 `AOTname` メソッドは、名プロパティの値のみを含む文字列を返します。                  |
| `TreeNode .AOTsave` `TreeNode .AOTinsert`                     | `System .Reflection .Emit` (クラスの名前空間) | `AOTsave` メソッドは、X++ コード内の `TreeNode` オブジェクトからの変更を AOT に適用し、変更は維持されます。 大規模なコード サンプルについては、TreeNode.AOTsave メソッドを参照してください。       |

### <a name="comparison-classes-about-file-io"></a>比較: ファイル IO に関するクラス
ファイル入出力 (IO) 操作を実行するクラスはいくつかあります。 C\# で使用されている .NET Framework では、これらのクラスに対応するものが `System.IO` 名前空間に配置されています。

次のテーブルは、`System.IO` 名前空間にある C\# のいくつかの .NET Framework クラスをリストしたものです。 テーブルの各行は、.NET Framework クラスに最も対応する方法または X++ クラスを示します。

|X++|C#|コメント|
|---|---|---|
| `BinaryIo`| `FileStream` `BinaryReader` `BinaryWriter` | 抽象クラス `Io` から拡張された `BinaryIo` 等の X++ クラスはストリームとして機能し、そのストリームのリーダーおよびライターとしても機能します。 C# では、ストリームは、より具体的な読み書きメソッドを持つクラスとは別のクラスです。|
| `TextBuffer`| `MemoryStream`| これらのクラスにはメモリ内バッファがあり、メソッドの中には、バッファをハードディスク上のファイルであるかのように扱うものがあります。|
| WINAPI::createDirectory WINAPI::folderExists WINAPI::removeDirectory| `Directory` `DirectoryInfo` `Path`| X++ はディレクトリを含む多くの基本オペレーティング システム関数の `WINAPI` クラス内で静的メソッドを使用することができます。|
| WINAPI::getDriveType| `DriveInfo` `DriveType`| これらのクラスとメソッドは、ドライブ関連の情報を取得するために使用されます。|
| WINAPI::copyFile WINAPI::createFile WINAPI::deleteFile WINAPI::fileExists| `File` `FileAttributes` `FileInfo`| X++ はファイルを含む多くの基本オペレーティング システム関数の `WINAPI` クラスで内で静的メソッドを使用することができます。|
| `CommaIo` `Comma7Io`| (対応するクラスはありません。)| これらの X++ クラスは、Microsoft Excel がインポートできるファイルを生成できます。 X++ で、Excel との追加のインタラクションに <a href="https://epplus.codeplex.com/">EPPlus</a>ライブラリ リファレンスを使用できます。|
| `AsciiIo` `TextIo`| `FileStream` `TextReader` `TextWriter`| これらのクラスはさまざまなコード ページを使用します。|
| `Io`| `Stream` `StreamReader` `StreamWriter` `FileStream`| これらは、他のクラスが拡張する基本クラスとしてよく使用されます。|
| `CodeAccessPermission` `FileIoPermission`| `System.Security` `.CodeAccessPermission` 名前空間 `System.Security.Permissions` には、次のクラスが含まれます。<ul><li>`CodeAccessSecurityAttribute`</li><li>`FileIOPermissionAttribute`</li><li>`FileIOPermission`</li><li>`FileIOPermissionAccess`</li></ul>| `assert`、`demand`、および `revertAssert` の概念とメソッドは両方の言語に適用されます。 ただし、C# で利用可能な `deny` および `revertDeny` メソッドは、X++ では使用できません。|

## <a name="x-ansi-sql-comparison-sql-select"></a>X++、ANSI SQL 比較: SQL の選択
X++ では、SQL **select** ステートメントの構文は、米国規格協会 (ANSI) の仕様とは異なります。

### <a name="single-table-select"></a>1 つのテーブル選択

次のテーブルで、X++ SQL および ANSI SQLの select ステートメントの相違点について説明します。

|機能|X++ SQL|ANSI SQL|コメント|
|---|---|---|---|
| <strong>from</strong> 句のテーブル名。| <strong>from</strong> 句は、`CustTable` テーブルからなど、テーブルから宣言されているレコード バッファー インスタンスを一覧表示します。| <strong>from</strong> 句は、バッファーの名前ではなく、テーブル名を一覧表示します。| レコード バッファには、`xRecord`class が X++ のすべてのメソッドがあります。|
| order by 句と <strong>where</strong> 句の構文の順序。| order by 句は、<strong>where</strong> 句の前に指定する必要があります。 order by 句は、<strong>from</strong> 句または <strong>join</strong> 句の後に指定する必要があります。 group by 句は、次の順序で同じ構文位置決めルールに従う必要があります。| order by 句は、<strong>where</strong> 句の後に指定する必要があります。 <strong>where</strong> 句は、<strong>from</strong> 句または <strong>join</strong> 句の後に指定する必要があります。| X++ と ANSI SQL の両方では、<strong>from</strong> および <strong>join</strong> 句が order by および <strong>where</strong> 句の前に表示されている必要があります。|
| 条件の否定。| 感嘆符 ('!') は 否定を示すために使用します。| <strong>not</strong> キーワードは、否定を示すために使用します。| X++ は構文 !like はサポートしません。 代わりに、! を適用する必要があります。 演算子を句に適用する必要があります。|
| <strong>like</strong> 演算子用ワイルドカード文字。|0 から多数 - アスタリスク (「*」)<br>1 のみ – 疑問符 ('?')|0 から多数 - パーセントを記号 (「%」)<br>1 のみ – アンダーバー ('_')| |
| <strong>where</strong> 句における論理演算子。|および – &&<br>または – \|\| |および – <strong>および</strong><br>または – <strong>や</strong>| |

### <a name="code-example"></a>コードの例

次のコード例は、前のテーブルの機能を示しています。

```xpp
static void OByWhere452Job(Args _args)
{
    // Declare the table buffer variable.
    CustTable tCustTable;
    ;
    while
    SELECT * from tCustTable
        order by tCustTable.AccountNum desc
        where (!(tCustTable.Name like '*i*i*') &amp;&amp; tCustTable.Name like 'T?e *')
    {
        info(tCustTable.AccountNum + " , " + tCustTable.Name);
    }
}
/*** InfoLog output
Message (04:02:29 pm)
4010 , The Lamp Shop
4008 , The Warehouse
4001 , The Bulb
***/
```
 
### <a name="x-sql-keywords"></a>X++ SQL キーワード

次の X++ SQL キーワードは、ANSI SQL に含まれていないものです。
-   crosscompany
-   firstonly100
-   forceliterals
-   forcenestedloop
-   forceplaceholders
-   forceselectorder
-   validtimestate

#### <a name="join-clause"></a>句の結合

次のテーブルで、X++ SQL および ANSI SQLの **結合** キーワードの相違点について説明します。

|機能|X++ SQL|ANSI SQL|コメント|
|---|---|---|---|
| 列リスト。                    | 列リストの列は、**from** 句にリストされているテーブルから取得し、**join** 句のテーブルからは取得しないでください。 リスト内の列は、テーブル名で修飾することはできません。 | 列リストの列は、**from** または **join** 句の任意のテーブルから取得できます。 これにより、他のユーザーはそのテーブル名のあるリスト内の列を修飾するときに、コードを維持することができます。 | 詳細については、「フィールドでの明細書の選択」を参照してください。    |
| **Join** 句の構文。          | **join** 句は **where** 句に従います。           | **join** 句は、**from** 句のテーブルに従います。                    | X++ コードの例で、**join** の条件は `SalesPoolId` 値と一致します。 |
| **内部** キーワード。               | 既定の **結合** モードは内部結合です。 **inner** キーワードがありません。           | 既定の **結合** モードは内部結合です。 **inner** キーワードは、コードを明確にするために使用できます。      | **outer** キーワードは、X++ SQL と ANSI SQL の両方に存在します。       |
| **左** および **右** キーワード。 | **left** および **right** キーワードは使用できません。 すべての結合が残されます。        | **left** および **right** キーワードは、**join** キーワードを変更するために使用できます。     | コメントはありません。                 |
| 等式演算子。               | 二重等号演算子 ('`==`') は、2 つの値の等価性をテストするために使用されます。  | 一重等号演算子 ('`=`') は、2 つの値の等価性をテストするために使用されます。                      | コメントはありません。                 |

### <a name="code-example"></a>コードの例

次のコード例は、X++ SQL の **join** 構文を示しています。

```xpp
static void OByWhere453Job(Args _args)
{
    // Declare table buffer variables.
    CustTable tCustTable;
    SalesPool tSalesPool;
    ;
    while
    SELECT
            // Not allowed to qualify by table buffer.
            // These fields must be from the table
            // in the from clause.
            AccountNum,
            Name
        from tCustTable
            order by tCustTable.AccountNum desc
            where (tCustTable.Name like 'The *')
        join tSalesPool
            where tCustTable.SalesPoolId == tSalesPool.SalesPoolId
    {
        info(tCustTable.AccountNum + " , " + tCustTable.Name);
    }
}
```
 
### <a name="aggregate-fields"></a>集計フィールド

次のテーブルは、**選択** 列リストの集計フィールドが X++ SQL と ANSI SQL の間でどのように参照されるかの相違点を示しています。 集計フィールドとは、**合計** または **平均** などの機能によって派生したものです。

|機能|X++ SQL|ANSI SQL|コメント|
|---|---|---|---|
| 集計フィールド名エイリアス。 | 集計値は、集計されたフィールドにあります。 | **as** キーワードを使用すると、名前エイリアス内の集計フィールドをタグ付けすることができます。 エイリアスは、以降のコードで参照される場合があります。 | 詳細については、「集計関数: X++ および SQL の差異」を参照してください |

### <a name="code-example"></a>コードの例

次のコード例では、情報メソッドの呼び出しが集計フィールドを参照する方法を示しています (`tPurchLine.QtyOrdered` を参照してください)。

```xpp
static void Null673Job(Args _args)
{
    PurchLine tPurchLine;
    ;
    while
    select
        // This aggregate field cannot be assigned an alias name.
        sum(QtyOrdered)
        from tPurchLine
    {
        info(
            // QtyOrdered is used to reference the sum.
            "QtyOrdered:  " + num2str(tPurchLine.QtyOrdered, 
            3,  // Minimum number of output characters.
            2,  // Required number of decimal places in the output.
            1,  // '.'  Separator to mark the start of the decimal places.
            2   // ','  The thousands separator.
            ));
    }
    info("End.");
}
/***
Message (12:23:08 pm)
QtyOrdered:  261,550.00
End.
***/
```

### <a name="other-differences"></a>その他の違い

次のテーブルに、X++ SQL および ANSI SQLの **select** ステートメントの相違点を示します。

|機能|X++ SQL|ANSI SQL|コメント|
|---|---|---|---|
|**having** キーワード。|**having** キーワードがありません。|**having** キーワードを使用すると、group by 句によって生成された行のフィルター条件を指できます。|コメントはありません。|
|null の結果。|**while** select ステートメントで、**where** 句がすべての行を除外する場合、それをレポートする特別なカウント行は返されません。|**select** で、**where** 句がすべての行を除外する場合、特別なカウント行が返されます。 カウント値は 0 です。|コメントはありません。|
|戻された行を移動するためのカーソル。|while select 文は、カーソル機能を提供します。 代わりに、**next** キーワードを使用することもできます。|**select** ステートメントから戻される行間ループのために、**cursor** を宣言することができます。||
|**From** 句。|列がリストされず、1 つのテーブルだけが参照される場合、**from** キーワードはオプションです。 次の 2 つの構文オプションは同等です。 <br>`select \* from tCustTable;` <br>`select tCustTable;`|**選択** ステートメントは、**from** 句が使用されていない限り、テーブルから読み取ることはできません。|X++ SQL では、シンプルな **選択** ステートメントが返された最初の行でテーブル バッファ変数を入力します。 これは、次のコード フラグメントによって示されています。 <br>`select \* from tCustTable;` <br>`info(tCustTable.Name);`|



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]