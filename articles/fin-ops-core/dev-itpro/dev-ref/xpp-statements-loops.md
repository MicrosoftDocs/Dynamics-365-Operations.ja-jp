---
title: コメント、使用、および印刷ステートメント
description: この記事では、X++ のステートメントについて説明します。
author: josaw1
ms.date: 08/27/2021
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.devlang: xpp
ms.openlocfilehash: 31ec127057ced34fc2c855f4c1aaf525827a2b0e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271275"
---
# <a name="comments-using-and-print-statements"></a>コメント、使用、および印刷ステートメント

[!include [banner](../includes/banner.md)]

この記事では、X++ のステートメントについて説明します。

## <a name="comments"></a>コメント

コードにコメントを追加することをお勧めします。 コメントは、プログラムを読みやすく、またわかりやすくします。 コメントは、プログラムをコンパイルする際には無視されます。 コメントには、**//** スタイルまたは **/\**_ スタイルを使用できます。ただし、ベスト プラクティスは、コメントおよび複数行のコメントの _*//** スタイルを使用することです。

```xpp
// This is an example of a comment.
/* Here is another example of a comment. */
```

## <a name="print-statements"></a>print ステートメント

**印刷** 明細書を使用して、**System.Diagnostics.WriteLine** 経由でテキストを Visual Studio **出力** ウィンドウに出力します。 テスト中は、**印刷** 明細書は **Globa::linfo** メソッドの代替になり、**情報ログ** ウィンドウのテキストを表示してくれます。 次のテーブルは、 **print** ステートメントと **info** メソッドを比較しています。

| 機能   | print ステートメント    | 情報メソッド  |
|-----------|--------------------|--------------|
| 呼び出し易さ                        | **print** ステートメントは、さまざまなデータ型を自動的に文字列に変換します。 1 つの呼び出しで複数のデータ型を変換できます。       | **info** メソッドでは、入力パラメーターを文字列にする必要があります。     |
| クリップボードにコンテンツをコピーする機能 | テキストは、**出力** ウィンドウからクリップボードに簡単にコピーできます。            | テキストは **情報ログ** ウィンドウからクリップボードに容易にコピーされます。 |
| 一般的な使用                             | **print** ステートメントは、テスト時に使用すると便利です。 正式なデバッガーを実行する必要なく、小さな問題をデバッグすることができます。 | **info** メソッドは、生産での使用に適しています。     |

### <a name="example-of-a-print-statement"></a>印刷明細書の例

次のコード例は、任意の日付型を文字列に自動的に変換する Print ステートメントを示します。 呼び出し時に、 **info** の前に **Global::** を付ける必要はありません。

```xpp
str hello = "Hello";
int fortytwo = 42;
utcDateTime now = DateTimeUtil::utcNow();
Dialog dialog = new Dialog();

print "The print statement automatically converts data types to strings.";
print hello, " -- ", fortytwo, " -- ", now, " -- ", dialog;
// Output to the Print window:
// The print statement automatically converts data types to strings.
// Hello -- 42 -- 10/3/2011 09:18:10 pm -- 1

// int2Str converter is needed when using info().
info("Hello");
info(int2Str(fortytwo));

// Output to Infolog window:
// Hello
// 42
```

## <a name="todo-comments"></a>TODO コメント

コンパイラは、コメントの先頭に **仕事** という文字列があると認識します。 **TODO** 文字列は、Microsoft Visual Studio の **タスク一覧** ウィンドウでコメント テキストの残りの部分を報告するようにコンパイラに求めます。 **タスク一覧** ウィンドウを開くには、**表示** を選択し、**タスク ウィンドウ** を選択します。 **タスク ウィンドウ** は、明細行番号を報告します。**TODO** コメントがコード内にあります。

コメントで **TODO** を使用するためのルールを次に示します。

- **TODO** 文字列は、 **//** スタイル、または **/\*** スタイルを使うコメントに表示されます。
- **"TODO"** 文字列は、コメント内の最初の空白文字以外の文字列にする必要があります。 キャリッジ リターン、改行、タブ、およびスペース、すべて空白と見なされます。
- コメントの開始と **"仕事"** の間に空白は必要ありません。
- **TODO** 文字列では大文字と小文字が区別されません。 ただし、規則では **ToDo** またはその他のバリエーションの代わりに、全大文字で **TODO** が入力されます。
- **TODO** 文字列には任意の文字を追加できます。 ただし、規則は、コロンを **TODO** 文字列に追加するかまたは空白で続けるかのいずれかです。
- **TODO** 文字列の後のコメントの残りは、タスク記述として報告されます。 コメントが 200 文字よりも長い場合は、**タスク** タブで切り詰められるとうに表示されることがあります。
- **/\*** コメント スタイルが使用されている場合、**TODO** タスクの説明は複数行にまたがることができます。

### <a name="examples-of-todo-comments"></a>TODO コメントの例

次の例は、 **TODO** コメントを示します。

```xpp
// An example of using TODO in the // style of comment.
public boolean isLate()
{
    // TODO: Finish this stub.
    return true;
}

// An example of using TODO in the /* */ style of comment.
public boolean isLate()
{
    /* TODO Finish this stub */
    return true;
}
```

## <a name="unsupported-statements-changesite-pause-and-window"></a>構文はサポートされていません: changeSite、一時停止、およびウィンドウ

**changeSite**、**pause**、**window** キーワードは、X++ 言語の一部ではなくなりました。 これらのキーワードを使用すると、コンパイル エラーが発生します。

## <a name="ignored-statements-server-and-client"></a>無視されたステートメント: サーバーおよびクライアント

以前のバージョン (AX2012 以前) では、クライアントまたはサーバーのいずれかで実行するメソッドを指定することができました。 すべての X++ コードは、サーバー上で .NET CIL として実行されるため、これは使用できなくなりました。 `client` および `server` キーワードは無視されます。 コンパイル エラーは発生しませんが、新しい X++ コードのいずれでも使用しないでください。

## <a name="using-clauses"></a>句の使用

タイプの完全修飾名を指定する必要がないように、**using** 句を使用します。 **using** 句は、適用されるクラスの前に配置する必要があり、適用先のすべてのソース ファイルに必要です。 すべての **using** 句は通常、ソース ファイルの先頭に配置します。 完全修飾名の短縮名を導入するエイリアスを提供することもできます。 エイリアスは名前空間またはクラスを示すことができます。

次の例では、**using** 句、名前空間エイリアス、およびクラス エイリアスを示しています。

```xpp
using System;
using IONS=System.IO; // Namespace alias
using Alist=System.Collections.ArrayList; // Class alias

class UsingClass
{
    public static void test()
    {
        Int32 I;                  // Alternative to System.Int32
        Alist al = new Alist();   // Using a class alias
        al.Add(1);
        str s = IONS.Path::ChangeExtension(@"c:\tmp\test.xml", ".txt"); // Using a namespace alias
    }
}
```

## <a name="using-statements"></a>ステートメントの使用

**using** ステートメントは、**IDisposable** を実行するオブジェクトが正しく破棄されることを保証するのに役立ちます。 原則として、**IDisposable** オブジェクトを使用する場合は、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。 **using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。 オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。 **using** ステートメントは構文を簡素化し、オブジェクトを正しく破棄します。 **using** ステートメントの構文を次に示します。

**(** *式* **) を使用して {** *ステートメント* **}**

この構文では、*ステートメント* はステートメントのブロックとすることができ、*式* は **IDisposable** を実装するオブジェクトを宣言してインスタンス化します。 次の例では､**StreamReader** オブジェクトを作成して使用します。

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

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
