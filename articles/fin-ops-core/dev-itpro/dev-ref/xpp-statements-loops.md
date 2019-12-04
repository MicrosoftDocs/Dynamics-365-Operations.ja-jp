---
title: X++ ステートメント
description: このトピックでは、X++のステートメントについて説明します。
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150213
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 390e9218cc4522972751fcf5094df9e1fa3fa5e6
ms.sourcegitcommit: 260a820038c29f712e8f1483cca9315b6dd3df55
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778684"
---
# <a name="x-statements"></a><span data-ttu-id="1cc45-103">X++ ステートメント</span><span class="sxs-lookup"><span data-stu-id="1cc45-103">X++ statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cc45-104">このトピックでは、X++のステートメントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-104">This topic describes statements in X++.</span></span>

## <a name="comments"></a><span data-ttu-id="1cc45-105">備考</span><span class="sxs-lookup"><span data-stu-id="1cc45-105">Comments</span></span>

<span data-ttu-id="1cc45-106">コードにコメントを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1cc45-106">It's a good practice to add comments to your code.</span></span> <span data-ttu-id="1cc45-107">コメントは、プログラムを読みやすく、またわかりやすくします。</span><span class="sxs-lookup"><span data-stu-id="1cc45-107">Comments make a program easier to read and understand.</span></span> <span data-ttu-id="1cc45-108">コメントは、プログラムをコンパイルする際には無視されます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-108">Comments are ignored when the program is compiled.</span></span> <span data-ttu-id="1cc45-109">コメントには **//** スタイルまたは **/\*** スタイルのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-109">Your comments can use either the **//** style or the **/\*** style.</span></span> <span data-ttu-id="1cc45-110">ただし、ベスト プラクティスは、コメント、および複数行コメントの**//** スタイルを使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="1cc45-110">However, a best practice is to use the **//** style for comments, and even for multiline comments.</span></span>

```X++
    // This is an example of a comment.
    /* Here is another example of a comment. */
```

## <a name="print-statements"></a><span data-ttu-id="1cc45-111">print ステートメント</span><span class="sxs-lookup"><span data-stu-id="1cc45-111">print statements</span></span>

<span data-ttu-id="1cc45-112">**印刷** 明細書を使用して、**System.Diagnostics.WriteLine** 経由でテキストを Visual Studio **出力** ウィンドウに出力します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-112">You use the **print** statement to output text through **System.Diagnostics.WriteLine** to the Visual Studio **Output** window.</span></span> <span data-ttu-id="1cc45-113">テスト中は、**印刷** 明細書は **Globa::linfo** メソッドの代替になり、**情報ログ** ウィンドウのテキストを表示してくれます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-113">During testing, the **print** statement is an alternative to the **Global::info** method, which shows text in the **Infolog** window.</span></span> <span data-ttu-id="1cc45-114">次のテーブルは、 **print** ステートメントと **info** メソッドを比較しています。</span><span class="sxs-lookup"><span data-stu-id="1cc45-114">The following table compares the **print** statement and the **info** method.</span></span>

| <span data-ttu-id="1cc45-115">機能</span><span class="sxs-lookup"><span data-stu-id="1cc45-115">Feature</span></span>   | <span data-ttu-id="1cc45-116">print ステートメント</span><span class="sxs-lookup"><span data-stu-id="1cc45-116">print statement</span></span>    | <span data-ttu-id="1cc45-117">情報メソッド</span><span class="sxs-lookup"><span data-stu-id="1cc45-117">info method</span></span>  |
|-----------|--------------------|--------------|
| <span data-ttu-id="1cc45-118">呼び出し易さ</span><span class="sxs-lookup"><span data-stu-id="1cc45-118">Ease of invocation</span></span>                        | <span data-ttu-id="1cc45-119">**print** ステートメントは、さまざまなデータ型を自動的に文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-119">The **print** statement automatically converts various data types into strings.</span></span> <span data-ttu-id="1cc45-120">1 つの呼び出しで複数のデータ型を変換できます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-120">It can convert multiple data types in one invocation.</span></span>       | <span data-ttu-id="1cc45-121">**info** メソッドでは、入力パラメーターを文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc45-121">The **info** method requires that the input parameter be a string.</span></span>     |
| <span data-ttu-id="1cc45-122">クリップボードにコンテンツをコピーする機能</span><span class="sxs-lookup"><span data-stu-id="1cc45-122">Ability to copy contents to the clipboard</span></span> | <span data-ttu-id="1cc45-123">テキストは、**出力** ウィンドウからクリップボードに簡単にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-123">Text is easily copied from the **Output** window to the clipboard.</span></span>            | <span data-ttu-id="1cc45-124">テキストは、**情報ログ** ウィンドウからクリップボードに簡単にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-124">Text is easily easily copied from the **Infolog** window to the clipboard.</span></span> |
| <span data-ttu-id="1cc45-125">一般的な使用</span><span class="sxs-lookup"><span data-stu-id="1cc45-125">Typical usage</span></span>                             | <span data-ttu-id="1cc45-126">**print** ステートメントは、テスト時に使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="1cc45-126">The **print** statement is used for convenience during testing.</span></span> <span data-ttu-id="1cc45-127">正式なデバッガーを実行する必要なく、小さな問題をデバッグすることができます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-127">It can help you debug small issues without having to run a formal debugger.</span></span> | <span data-ttu-id="1cc45-128">**info** メソッドは、生産での使用に適しています。</span><span class="sxs-lookup"><span data-stu-id="1cc45-128">The **info** method is appropriate for use in production.</span></span>     |

### <a name="example-of-a-print-statement"></a><span data-ttu-id="1cc45-129">印刷明細書の例</span><span class="sxs-lookup"><span data-stu-id="1cc45-129">Example of a print statement</span></span>

<span data-ttu-id="1cc45-130">次のコード例は、任意の日付型を文字列に自動的に変換する Print ステートメントを示します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-130">The following code example demonstrates the print statement automatically converting any date type to a string.</span></span> <span data-ttu-id="1cc45-131">呼び出し時に、 **info** の前に **Global::** を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1cc45-131">You do not need to prefix **info** with **Global::** when you call it.</span></span>

```X++

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

## <a name="todo-comments"></a><span data-ttu-id="1cc45-132">TODO コメント</span><span class="sxs-lookup"><span data-stu-id="1cc45-132">TODO comments</span></span>
<span data-ttu-id="1cc45-133">コンパイラは、コメントの先頭に**仕事**という文字列があると認識します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-133">The compiler recognizes the string **TODO** when it occurs at the start of a comment.</span></span> <span data-ttu-id="1cc45-134">**TODO** 文字列は、Microsoft Visual Studio の**タスク一覧**ウィンドウでコメント テキストの残りの部分を報告するようにコンパイラに求めます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-134">The **TODO** string prompts the compiler to report the rest of the comment text in the **Task List** window in Microsoft Visual Studio.</span></span> <span data-ttu-id="1cc45-135">**タスク一覧** ウィンドウを開くには、**表示** を選択し、**タスク ウィンドウ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-135">To open the **Task List** window, select **View**, and then select **Task Window**.</span></span> <span data-ttu-id="1cc45-136">**タスク ウィンドウ**は、明細行番号を報告します。**TODO** コメントがコード内にあります。</span><span class="sxs-lookup"><span data-stu-id="1cc45-136">The **Task Window** reports the line number where the **TODO** comment can be found in the code.</span></span> 

<span data-ttu-id="1cc45-137">コメントで **TODO** を使用するためのルールを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-137">Here are the rules for using **TODO** in comments:</span></span>

- <span data-ttu-id="1cc45-138">**TODO** 文字列は、 **//** スタイル、または **/\*** スタイルを使うコメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-138">The **TODO** string can appear in a comment that uses either the **//** style or the **/\*** style.</span></span>
- <span data-ttu-id="1cc45-139">**"TODO"** 文字列は、コメント内の最初の空白文字以外の文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc45-139">The **TODO** string must be the very first non–white space string in the comment.</span></span> <span data-ttu-id="1cc45-140">キャリッジ リターン、改行、タブ、およびスペース、すべて空白と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-140">A carriage return, a line feed, a tab, and a space are all considered white space.</span></span>
- <span data-ttu-id="1cc45-141">コメントの開始と **"仕事"** の間に空白は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1cc45-141">No white space is required between the start of the comment and the **TODO**.</span></span>
- <span data-ttu-id="1cc45-142">**TODO** 文字列では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="1cc45-142">The **TODO** string is case-insensitive.</span></span> <span data-ttu-id="1cc45-143">ただし、規則では **ToDo** またはその他のバリエーションの代わりに、全大文字で **TODO** が入力されます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-143">However, the convention is to type **TODO** in all uppercase letters, instead of **ToDo** or another variation.</span></span>
- <span data-ttu-id="1cc45-144">**TODO** 文字列には任意の文字を追加できます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-144">The **TODO** string can have any characters appended to it.</span></span> <span data-ttu-id="1cc45-145">ただし、規則は、コロンを **TODO** 文字列に追加するかまたは空白で続けるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="1cc45-145">However, the convention is either to append a colon to the **TODO** string or to follow it with a white space.</span></span>
- <span data-ttu-id="1cc45-146">**TODO** 文字列の後のコメントの残りは、タスク記述として報告されます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-146">The rest of the comment after the **TODO** string is reported as the task description.</span></span> <span data-ttu-id="1cc45-147">コメントが 200 文字よりも長い場合は、**タスク** タブで切り詰められるとうに表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1cc45-147">If the comment is longer than 200 characters, it might appear truncated on the **Tasks** tab.</span></span>
- <span data-ttu-id="1cc45-148">**/\*** コメント スタイルが使用されている場合、**TODO** タスクの説明は複数行にまたがることができます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-148">The **TODO** task description can be spread over multiple lines when the **/\*** comment style is used.</span></span>

### <a name="examples-of-todo-comments"></a><span data-ttu-id="1cc45-149">TODO コメントの例</span><span class="sxs-lookup"><span data-stu-id="1cc45-149">Examples of TODO comments</span></span>

<span data-ttu-id="1cc45-150">次の例は、 **TODO** コメントを示します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-150">The following examples show **TODO** comments.</span></span>

```X++
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

## <a name="unsupported-statements-changesite-pause-and-window"></a><span data-ttu-id="1cc45-151">構文はサポートされていません: changeSite、一時停止、およびウィンドウ</span><span class="sxs-lookup"><span data-stu-id="1cc45-151">Unsupported statements: changeSite, pause, and window</span></span>

<span data-ttu-id="1cc45-152">**changeSite**、**pause**、**window** キーワードは、X++ 言語の一部ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="1cc45-152">The **changeSite**, **pause**, and **window** keywords are no longer a part of the X++ language.</span></span> <span data-ttu-id="1cc45-153">これらのキーワードを使用すると、コンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-153">These keywords will cause compilation errors if you use them.</span></span>

## <a name="using-clauses"></a><span data-ttu-id="1cc45-154">句の使用</span><span class="sxs-lookup"><span data-stu-id="1cc45-154">using clauses</span></span>
<span data-ttu-id="1cc45-155">タイプの完全修飾名を指定する必要がないように、**using** 句を使用します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-155">You use **using** clauses so that you don't have to provide the fully qualified name of a type.</span></span> <span data-ttu-id="1cc45-156">**using** 句は、適用されるクラスの前に配置する必要があり、適用先のすべてのソース ファイルに必要です。</span><span class="sxs-lookup"><span data-stu-id="1cc45-156">The **using** clause must precede the class that it applies, and it's required in every source file that you want it to apply to.</span></span> <span data-ttu-id="1cc45-157">すべての **using** 句は通常、ソース ファイルの先頭に配置します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-157">Typically, all **using** clauses are put at the beginning of the source file.</span></span> <span data-ttu-id="1cc45-158">完全修飾名の短縮名を導入するエイリアスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-158">You can also provide aliases that introduce a short name for a fully qualified name.</span></span> <span data-ttu-id="1cc45-159">エイリアスは名前空間またはクラスを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-159">Aliases can denote namespaces or classes.</span></span> 

<span data-ttu-id="1cc45-160">次の例では、**using** 句、名前空間エイリアス、およびクラス エイリアスを示しています。</span><span class="sxs-lookup"><span data-stu-id="1cc45-160">The following example shows a **using** clause, a namespace alias, and a class alias.</span></span>

```X++
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

## <a name="using-statements"></a><span data-ttu-id="1cc45-161">ステートメントの使用</span><span class="sxs-lookup"><span data-stu-id="1cc45-161">using statements</span></span>
<span data-ttu-id="1cc45-162">**using** ステートメントは、**IDisposable** を実行するオブジェクトが正しく破棄されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-162">The **using** statement helps guarantee that objects that implement **IDisposable** are disposed of correctly.</span></span> <span data-ttu-id="1cc45-163">原則として、**IDisposable** オブジェクトを使用する場合は、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc45-163">When you use an **IDisposable** object, you should declare and instantiate it in a **using** statement.</span></span> <span data-ttu-id="1cc45-164">**using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-164">The **using** statement calls the **Dispose** method on the object in the correct way, even if an exception occurs while you're calling methods on the object.</span></span> <span data-ttu-id="1cc45-165">オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="1cc45-165">You can achieve the same result by putting the object inside a **try** block and then explicitly calling **Dispose** in a **finally** block.</span></span> <span data-ttu-id="1cc45-166">**using** ステートメントは構文を簡素化し、オブジェクトを正しく破棄します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-166">The **using** statement simplifies the syntax and disposes of the object correctly.</span></span> <span data-ttu-id="1cc45-167">**using** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-167">Here is the syntax for a **using** statement:</span></span>

<span data-ttu-id="1cc45-168">**(** *式* **) を使用して {** *ステートメント* **}**</span><span class="sxs-lookup"><span data-stu-id="1cc45-168">**using (** *expression* **) {** *statement* **}**</span></span>

<span data-ttu-id="1cc45-169">この構文では、*ステートメント*はステートメントのブロックとすることができ、*式*は **IDisposable** を実装するオブジェクトを宣言してインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-169">In this syntax, *statement* can be a block of statements, and *expression* declares and instantiates an object that implements **IDisposable**.</span></span> <span data-ttu-id="1cc45-170">次の例では､**StreamReader** オブジェクトを作成して使用します。</span><span class="sxs-lookup"><span data-stu-id="1cc45-170">The following example creates and uses a **StreamReader** object.</span></span>

```X++
static void AnotherMethod()
{
    str textFromFile;
    using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
    {
        textFromFile = sr.ReadToEnd();
    }
}
```
