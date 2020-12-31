---
title: コメント、使用、および印刷ステートメント
description: このトピックでは、X++のステートメントについて説明します。
author: robinarh
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.devlang: xpp
ms.reviewer: rhaertle
ms.custom: 150213
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a692579a331f9e58810f6ae2d50d30c68ae3e3bc
ms.sourcegitcommit: 71a19a55ae84df917c19a11c065d0d8a6140e669
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2020
ms.locfileid: "4409581"
---
# <a name="comments-using-and-print-statements"></a><span data-ttu-id="70d10-103">コメント、使用、および印刷ステートメント</span><span class="sxs-lookup"><span data-stu-id="70d10-103">Comments, using, and print statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70d10-104">このトピックでは、X++のステートメントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="70d10-104">This topic describes statements in X++.</span></span>

## <a name="comments"></a><span data-ttu-id="70d10-105">備考</span><span class="sxs-lookup"><span data-stu-id="70d10-105">Comments</span></span>

<span data-ttu-id="70d10-106">コードにコメントを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="70d10-106">It's a good practice to add comments to your code.</span></span> <span data-ttu-id="70d10-107">コメントは、プログラムを読みやすく、またわかりやすくします。</span><span class="sxs-lookup"><span data-stu-id="70d10-107">Comments make a program easier to read and understand.</span></span> <span data-ttu-id="70d10-108">コメントは、プログラムをコンパイルする際には無視されます。</span><span class="sxs-lookup"><span data-stu-id="70d10-108">Comments are ignored when the program is compiled.</span></span> <span data-ttu-id="70d10-109">コメントには、**//** スタイルまたは **/\**_ スタイルを使用できます。ただし、ベスト プラクティスは、コメントおよび複数行のコメントの _*//** スタイルを使用することです。</span><span class="sxs-lookup"><span data-stu-id="70d10-109">Your comments can use either the **//** style or the **/\**_ style. However, a best practice is to use the _*//** style for comments, and even for multiline comments.</span></span>

```xpp
// This is an example of a comment.
/* Here is another example of a comment. */
```

## <a name="print-statements"></a><span data-ttu-id="70d10-110">print ステートメント</span><span class="sxs-lookup"><span data-stu-id="70d10-110">print statements</span></span>

<span data-ttu-id="70d10-111">**印刷** 明細書を使用して、**System.Diagnostics.WriteLine** 経由でテキストを Visual Studio **出力** ウィンドウに出力します。</span><span class="sxs-lookup"><span data-stu-id="70d10-111">You use the **print** statement to output text through **System.Diagnostics.WriteLine** to the Visual Studio **Output** window.</span></span> <span data-ttu-id="70d10-112">テスト中は、**印刷** 明細書は **Globa::linfo** メソッドの代替になり、**情報ログ** ウィンドウのテキストを表示してくれます。</span><span class="sxs-lookup"><span data-stu-id="70d10-112">During testing, the **print** statement is an alternative to the **Global::info** method, which shows text in the **Infolog** window.</span></span> <span data-ttu-id="70d10-113">次のテーブルは、 **print** ステートメントと **info** メソッドを比較しています。</span><span class="sxs-lookup"><span data-stu-id="70d10-113">The following table compares the **print** statement and the **info** method.</span></span>

| <span data-ttu-id="70d10-114">機能</span><span class="sxs-lookup"><span data-stu-id="70d10-114">Feature</span></span>   | <span data-ttu-id="70d10-115">print ステートメント</span><span class="sxs-lookup"><span data-stu-id="70d10-115">print statement</span></span>    | <span data-ttu-id="70d10-116">情報メソッド</span><span class="sxs-lookup"><span data-stu-id="70d10-116">info method</span></span>  |
|-----------|--------------------|--------------|
| <span data-ttu-id="70d10-117">呼び出し易さ</span><span class="sxs-lookup"><span data-stu-id="70d10-117">Ease of invocation</span></span>                        | <span data-ttu-id="70d10-118">**print** ステートメントは、さまざまなデータ型を自動的に文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="70d10-118">The **print** statement automatically converts various data types into strings.</span></span> <span data-ttu-id="70d10-119">1 つの呼び出しで複数のデータ型を変換できます。</span><span class="sxs-lookup"><span data-stu-id="70d10-119">It can convert multiple data types in one invocation.</span></span>       | <span data-ttu-id="70d10-120">**info** メソッドでは、入力パラメーターを文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70d10-120">The **info** method requires that the input parameter be a string.</span></span>     |
| <span data-ttu-id="70d10-121">クリップボードにコンテンツをコピーする機能</span><span class="sxs-lookup"><span data-stu-id="70d10-121">Ability to copy contents to the clipboard</span></span> | <span data-ttu-id="70d10-122">テキストは、**出力** ウィンドウからクリップボードに簡単にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="70d10-122">Text is easily copied from the **Output** window to the clipboard.</span></span>            | <span data-ttu-id="70d10-123">テキストは、**情報ログ** ウィンドウからクリップボードに簡単にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="70d10-123">Text is easily easily copied from the **Infolog** window to the clipboard.</span></span> |
| <span data-ttu-id="70d10-124">一般的な使用</span><span class="sxs-lookup"><span data-stu-id="70d10-124">Typical usage</span></span>                             | <span data-ttu-id="70d10-125">**print** ステートメントは、テスト時に使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="70d10-125">The **print** statement is used for convenience during testing.</span></span> <span data-ttu-id="70d10-126">正式なデバッガーを実行する必要なく、小さな問題をデバッグすることができます。</span><span class="sxs-lookup"><span data-stu-id="70d10-126">It can help you debug small issues without having to run a formal debugger.</span></span> | <span data-ttu-id="70d10-127">**info** メソッドは、生産での使用に適しています。</span><span class="sxs-lookup"><span data-stu-id="70d10-127">The **info** method is appropriate for use in production.</span></span>     |

### <a name="example-of-a-print-statement"></a><span data-ttu-id="70d10-128">印刷明細書の例</span><span class="sxs-lookup"><span data-stu-id="70d10-128">Example of a print statement</span></span>

<span data-ttu-id="70d10-129">次のコード例は、任意の日付型を文字列に自動的に変換する Print ステートメントを示します。</span><span class="sxs-lookup"><span data-stu-id="70d10-129">The following code example demonstrates the print statement automatically converting any date type to a string.</span></span> <span data-ttu-id="70d10-130">呼び出し時に、 **info** の前に **Global::** を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="70d10-130">You do not need to prefix **info** with **Global::** when you call it.</span></span>

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

## <a name="todo-comments"></a><span data-ttu-id="70d10-131">TODO コメント</span><span class="sxs-lookup"><span data-stu-id="70d10-131">TODO comments</span></span>
<span data-ttu-id="70d10-132">コンパイラは、コメントの先頭に **仕事** という文字列があると認識します。</span><span class="sxs-lookup"><span data-stu-id="70d10-132">The compiler recognizes the string **TODO** when it occurs at the start of a comment.</span></span> <span data-ttu-id="70d10-133">**TODO** 文字列は、Microsoft Visual Studio の **タスク一覧** ウィンドウでコメント テキストの残りの部分を報告するようにコンパイラに求めます。</span><span class="sxs-lookup"><span data-stu-id="70d10-133">The **TODO** string prompts the compiler to report the rest of the comment text in the **Task List** window in Microsoft Visual Studio.</span></span> <span data-ttu-id="70d10-134">**タスク一覧** ウィンドウを開くには、**表示** を選択し、**タスク ウィンドウ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70d10-134">To open the **Task List** window, select **View**, and then select **Task Window**.</span></span> <span data-ttu-id="70d10-135">**タスク ウィンドウ** は、明細行番号を報告します。**TODO** コメントがコード内にあります。</span><span class="sxs-lookup"><span data-stu-id="70d10-135">The **Task Window** reports the line number where the **TODO** comment can be found in the code.</span></span> 

<span data-ttu-id="70d10-136">コメントで **TODO** を使用するためのルールを次に示します。</span><span class="sxs-lookup"><span data-stu-id="70d10-136">Here are the rules for using **TODO** in comments:</span></span>

- <span data-ttu-id="70d10-137">**TODO** 文字列は、**//** スタイル、または \**/\** _ スタイルを使うコメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="70d10-137">The **TODO** string can appear in a comment that uses either the **//** style or the \**/\** _ style.</span></span>
- <span data-ttu-id="70d10-138">_ *TODO*\* 文字列は、コメント内の最初の空白文字以外の文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70d10-138">The _ *TODO*\* string must be the very first non–white space string in the comment.</span></span> <span data-ttu-id="70d10-139">キャリッジ リターン、改行、タブ、およびスペース、すべて空白と見なされます。</span><span class="sxs-lookup"><span data-stu-id="70d10-139">A carriage return, a line feed, a tab, and a space are all considered white space.</span></span>
- <span data-ttu-id="70d10-140">コメントの開始と **"仕事"** の間に空白は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="70d10-140">No white space is required between the start of the comment and the **TODO**.</span></span>
- <span data-ttu-id="70d10-141">**TODO** 文字列では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="70d10-141">The **TODO** string is case-insensitive.</span></span> <span data-ttu-id="70d10-142">ただし、規則では **ToDo** またはその他のバリエーションの代わりに、全大文字で **TODO** が入力されます。</span><span class="sxs-lookup"><span data-stu-id="70d10-142">However, the convention is to type **TODO** in all uppercase letters, instead of **ToDo** or another variation.</span></span>
- <span data-ttu-id="70d10-143">**TODO** 文字列には任意の文字を追加できます。</span><span class="sxs-lookup"><span data-stu-id="70d10-143">The **TODO** string can have any characters appended to it.</span></span> <span data-ttu-id="70d10-144">ただし、規則は、コロンを **TODO** 文字列に追加するかまたは空白で続けるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="70d10-144">However, the convention is either to append a colon to the **TODO** string or to follow it with a white space.</span></span>
- <span data-ttu-id="70d10-145">**TODO** 文字列の後のコメントの残りは、タスク記述として報告されます。</span><span class="sxs-lookup"><span data-stu-id="70d10-145">The rest of the comment after the **TODO** string is reported as the task description.</span></span> <span data-ttu-id="70d10-146">コメントが 200 文字よりも長い場合は、**タスク** タブで切り詰められるとうに表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="70d10-146">If the comment is longer than 200 characters, it might appear truncated on the **Tasks** tab.</span></span>
- <span data-ttu-id="70d10-147">**/\** _ コメント スタイルが使用されている場合、\*\*TODO*\* タスクの説明は複数行にまたがることができます。</span><span class="sxs-lookup"><span data-stu-id="70d10-147">The **TODO** task description can be spread over multiple lines when the \**/\** _ comment style is used.</span></span>

### <a name="examples-of-todo-comments"></a><span data-ttu-id="70d10-148">TODO コメントの例</span><span class="sxs-lookup"><span data-stu-id="70d10-148">Examples of TODO comments</span></span>

<span data-ttu-id="70d10-149">次の例は、_ *TODO*\* コメントを示します。</span><span class="sxs-lookup"><span data-stu-id="70d10-149">The following examples show _ *TODO*\* comments.</span></span>

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

## <a name="unsupported-statements-changesite-pause-and-window"></a><span data-ttu-id="70d10-150">構文はサポートされていません: changeSite、一時停止、およびウィンドウ</span><span class="sxs-lookup"><span data-stu-id="70d10-150">Unsupported statements: changeSite, pause, and window</span></span>

<span data-ttu-id="70d10-151">**changeSite**、**pause**、**window** キーワードは、X++ 言語の一部ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="70d10-151">The **changeSite**, **pause**, and **window** keywords are no longer a part of the X++ language.</span></span> <span data-ttu-id="70d10-152">これらのキーワードを使用すると、コンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="70d10-152">These keywords will cause compilation errors if you use them.</span></span>

## <a name="using-clauses"></a><span data-ttu-id="70d10-153">句の使用</span><span class="sxs-lookup"><span data-stu-id="70d10-153">using clauses</span></span>
<span data-ttu-id="70d10-154">タイプの完全修飾名を指定する必要がないように、**using** 句を使用します。</span><span class="sxs-lookup"><span data-stu-id="70d10-154">You use **using** clauses so that you don't have to provide the fully qualified name of a type.</span></span> <span data-ttu-id="70d10-155">**using** 句は、適用されるクラスの前に配置する必要があり、適用先のすべてのソース ファイルに必要です。</span><span class="sxs-lookup"><span data-stu-id="70d10-155">The **using** clause must precede the class that it applies, and it's required in every source file that you want it to apply to.</span></span> <span data-ttu-id="70d10-156">すべての **using** 句は通常、ソース ファイルの先頭に配置します。</span><span class="sxs-lookup"><span data-stu-id="70d10-156">Typically, all **using** clauses are put at the beginning of the source file.</span></span> <span data-ttu-id="70d10-157">完全修飾名の短縮名を導入するエイリアスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="70d10-157">You can also provide aliases that introduce a short name for a fully qualified name.</span></span> <span data-ttu-id="70d10-158">エイリアスは名前空間またはクラスを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="70d10-158">Aliases can denote namespaces or classes.</span></span> 

<span data-ttu-id="70d10-159">次の例では、**using** 句、名前空間エイリアス、およびクラス エイリアスを示しています。</span><span class="sxs-lookup"><span data-stu-id="70d10-159">The following example shows a **using** clause, a namespace alias, and a class alias.</span></span>

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

## <a name="using-statements"></a><span data-ttu-id="70d10-160">ステートメントの使用</span><span class="sxs-lookup"><span data-stu-id="70d10-160">using statements</span></span>
<span data-ttu-id="70d10-161">**using** ステートメントは、**IDisposable** を実行するオブジェクトが正しく破棄されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="70d10-161">The **using** statement helps guarantee that objects that implement **IDisposable** are disposed of correctly.</span></span> <span data-ttu-id="70d10-162">原則として、**IDisposable** オブジェクトを使用する場合は、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70d10-162">When you use an **IDisposable** object, you should declare and instantiate it in a **using** statement.</span></span> <span data-ttu-id="70d10-163">**using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="70d10-163">The **using** statement calls the **Dispose** method on the object in the correct way, even if an exception occurs while you're calling methods on the object.</span></span> <span data-ttu-id="70d10-164">オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="70d10-164">You can achieve the same result by putting the object inside a **try** block and then explicitly calling **Dispose** in a **finally** block.</span></span> <span data-ttu-id="70d10-165">**using** ステートメントは構文を簡素化し、オブジェクトを正しく破棄します。</span><span class="sxs-lookup"><span data-stu-id="70d10-165">The **using** statement simplifies the syntax and disposes of the object correctly.</span></span> <span data-ttu-id="70d10-166">**using** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="70d10-166">Here is the syntax for a **using** statement:</span></span>

<span data-ttu-id="70d10-167">**(** *式* **) を使用して {** *ステートメント* **}**</span><span class="sxs-lookup"><span data-stu-id="70d10-167">**using (** *expression* **) {** *statement* **}**</span></span>

<span data-ttu-id="70d10-168">この構文では、*ステートメント* はステートメントのブロックとすることができ、*式* は **IDisposable** を実装するオブジェクトを宣言してインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="70d10-168">In this syntax, *statement* can be a block of statements, and *expression* declares and instantiates an object that implements **IDisposable**.</span></span> <span data-ttu-id="70d10-169">次の例では､**StreamReader** オブジェクトを作成して使用します。</span><span class="sxs-lookup"><span data-stu-id="70d10-169">The following example creates and uses a **StreamReader** object.</span></span>

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
