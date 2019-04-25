---
title: X++ と C# の比較
description: このトピックでは、X++ と C# の構文とプログラミングを比較します。
author: RobinARH
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 72424
ms.assetid: 9e0b3126-aa04-4b76-a254-bfbd3fcd6552
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b022b94742adef2fe9a23f92b642e7df226818
ms.sourcegitcommit: 0b9d7d4c163992a9949bd8c8fffa18eb4ad9fa64
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/15/2019
ms.locfileid: "845113"
---
# <a name="x-and-c-comparison"></a><span data-ttu-id="4902a-103">X++ と C# の比較</span><span class="sxs-lookup"><span data-stu-id="4902a-103">X++ and C# comparison</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4902a-104">このトピックでは、X++ と C# の構文とプログラミングを比較します。</span><span class="sxs-lookup"><span data-stu-id="4902a-104">This topic compares X++ and C# syntax and programming.</span></span>

## <a name="x-c-comparison-hello-world"></a><span data-ttu-id="4902a-105">X++、C# の比較: Hello World</span><span class="sxs-lookup"><span data-stu-id="4902a-105">X++, C# Comparison: Hello World</span></span>

<span data-ttu-id="4902a-106">このセクションでは、最も単純な X++ プログラムを C# の対応するものと比較します。</span><span class="sxs-lookup"><span data-stu-id="4902a-106">This section compares the simplest X++ program to its counterpart in C#.</span></span>

### <a name="x-to-c-comparisons"></a><span data-ttu-id="4902a-107">X++ と C# の比較</span><span class="sxs-lookup"><span data-stu-id="4902a-107">X++ to C# Comparisons</span></span>

<span data-ttu-id="4902a-108">次のセクションでは、X++ と C\# の基本的な類似点と相違点について説明します。</span><span class="sxs-lookup"><span data-stu-id="4902a-108">The following sections describe some basic similarities and differences between X++ and C\#.</span></span>

### <a name="similarities"></a><span data-ttu-id="4902a-109">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-109">Similarities</span></span>

<span data-ttu-id="4902a-110">次の X++ 機能は C# の機能と同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-110">The following X++ features are the same for C#:</span></span>
-   <span data-ttu-id="4902a-111">1 つの明細行 (`//`) と複数行 (/\*\*/) のコメント。</span><span class="sxs-lookup"><span data-stu-id="4902a-111">Single line (`//`) and multi-line (/\* \*/) comments.</span></span>
-   <span data-ttu-id="4902a-112">`==` 2 つの値が等しいかどうかを判定するための (等しい) 演算子。</span><span class="sxs-lookup"><span data-stu-id="4902a-112">`==` (equal) operator for determining whether two values are equal.</span></span>
-   <span data-ttu-id="4902a-113">`!=` (等しくない) 2 つの値が等しくないかどうかを決定するための演算子。</span><span class="sxs-lookup"><span data-stu-id="4902a-113">`!=` (not equal to) operator for determining whether two values are not equivalent.</span></span>
-   <span data-ttu-id="4902a-114">`+` (プラス記号) 文字列連結の演算子です。</span><span class="sxs-lookup"><span data-stu-id="4902a-114">`+` (plus sign) operator for string concatenation.</span></span>

### <a name="differences"></a><span data-ttu-id="4902a-115">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-115">Differences</span></span>

<span data-ttu-id="4902a-116">次のテーブルは、C# では異なる X++ の機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-116">The following table lists X++ features that are different in C#.</span></span>

| <span data-ttu-id="4902a-117">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-117">Feature</span></span> | <span data-ttu-id="4902a-118">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-118">X++</span></span> | <span data-ttu-id="4902a-119">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-119">C#</span></span> | <span data-ttu-id="4902a-120">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-120">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-121">`if` および `else` の条件付きステートメント</span><span class="sxs-lookup"><span data-stu-id="4902a-121">`if` and `else` conditional statements</span></span> | <span data-ttu-id="4902a-122">`if` ステートメントは、ブール値に自動的に変換できる式のあらゆる型を受け付けます。</span><span class="sxs-lookup"><span data-stu-id="4902a-122">The `if` statement accepts any type of expression that it can automatically convert to a Boolean.</span></span> <span data-ttu-id="4902a-123">一般的な例は、0 が false を意味する `int`、または Null が false を意味するオブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="4902a-123">Common examples include an `int` for which 0 means false, or an object for which null means false.</span></span> | <span data-ttu-id="4902a-124">`if` ステートメントには、ブール式が必要です。</span><span class="sxs-lookup"><span data-stu-id="4902a-124">The `if` statement requires a Boolean expression.</span></span> | <span data-ttu-id="4902a-125">中括弧と括弧に関する構文構造は、X++ と C# でまったく同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-125">The syntax structure regarding curly braces and parentheses is exactly the same between X++ and C#.</span></span> |
| <span data-ttu-id="4902a-126">リテラル文字列</span><span class="sxs-lookup"><span data-stu-id="4902a-126">Literal string</span></span> | <span data-ttu-id="4902a-127">リテラル文字列は、次のいずれかの方法で区切ることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-127">A literal string can be delimited by either of the following:</span></span><ul><li><span data-ttu-id="4902a-128">二重引用符 (") 文字のペア。</span><span class="sxs-lookup"><span data-stu-id="4902a-128">A pair of double quotation mark (") characters.</span></span></li><li><span data-ttu-id="4902a-129">単一引用符 (') 文字のペア。</span><span class="sxs-lookup"><span data-stu-id="4902a-129">A pair of single quotation mark (') characters.</span></span></li></ul> | <span data-ttu-id="4902a-130">リテラル文字列は、二重引用符 (") のペアで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-130">A literal string must be delimited by a pair of double quotation mark (") characters.</span></span> | <span data-ttu-id="4902a-131">X++ で、二重引用符文字は通常、文字列を区切るために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-131">For X++, the double quotation mark characters are usually used to delimit strings.</span></span> <span data-ttu-id="4902a-132">ただし、文字列に二重引用符文字を含める必要がある場合、単一引用符文字で文字列を区切るのが便利です。</span><span class="sxs-lookup"><span data-stu-id="4902a-132">However, it is convenient delimit a string with single quotation mark characters when your string must contain a double quotation mark character.</span></span>|
| <span data-ttu-id="4902a-133">char `type`</span><span class="sxs-lookup"><span data-stu-id="4902a-133">char `type`</span></span> | <span data-ttu-id="4902a-134">X++ には `char` または文字タイプがありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-134">There is no `char` or character type in X++.</span></span> <span data-ttu-id="4902a-135">長さ 1 の `str` を宣言することができますが、文字列のままです。</span><span class="sxs-lookup"><span data-stu-id="4902a-135">You can declare a `str` of length one, but it is still a string:</span></span><br> `str 1 myString = "a";` | <span data-ttu-id="4902a-136">C# には `char` があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-136">There is a `char` in C#.</span></span> <span data-ttu-id="4902a-137">最初に `char` を `string` に明示的に変換できますが、パラメーターとして `char` を `string` パラメーターを入力するメソッドに渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-137">You cannot pass a `char` as the parameter to a method that inputs a `string` parameter, although you can first explicitly convert the `char` to a `string`.</span></span>| <span data-ttu-id="4902a-138">X++ データ型の詳細については、プリミティブ データ型を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-138">For more information about X++ data types, see Primitive Data Types.</span></span>|
| <span data-ttu-id="4902a-139">メッセージの出力</span><span class="sxs-lookup"><span data-stu-id="4902a-139">Output of messages</span></span>| <span data-ttu-id="4902a-140">X++ は情報ログ ウィンドウ内でユーザーにメッセージを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-140">X++ delivers messages to the user in the Infolog window.</span></span> <span data-ttu-id="4902a-141">一般的なメソッドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-141">Common methods include the following:</span></span><ul><li><span data-ttu-id="4902a-142"><strong>print</strong> ステートメント:</span><span class="sxs-lookup"><span data-stu-id="4902a-142">The <strong>print</strong> statement:</span></span></li><li><span data-ttu-id="4902a-143">`Global` クラスの静的メソッド:</span><span class="sxs-lookup"><span data-stu-id="4902a-143">static methods on the `Global` class:</span></span><ul><li><span data-ttu-id="4902a-144">Global::info</span><span class="sxs-lookup"><span data-stu-id="4902a-144">Global::info</span></span></li><li><span data-ttu-id="4902a-145">Global::warning</span><span class="sxs-lookup"><span data-stu-id="4902a-145">Global::warning</span></span></li><li><span data-ttu-id="4902a-146">Global::error</span><span class="sxs-lookup"><span data-stu-id="4902a-146">Global::error</span></span></li></ul></li></ul>| <span data-ttu-id="4902a-147">コマンド ライン プログラムで、コンソールにメッセージを配信することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-147">For a command line program, messages can be delivered to the console.</span></span> <span data-ttu-id="4902a-148">一般的なメソッドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-148">Common methods include the following:</span></span><ul><li>`Console.Out.WriteLine`</li><li>`Console.Error.WriteLine`</li></ul>|  |

### <a name="x-and-c-samples"></a><span data-ttu-id="4902a-149">X++ および C++ のサンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-149">X++ and C++ Samples</span></span>

<span data-ttu-id="4902a-150">このセクションには、2 つの簡単なコード サンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4902a-150">This section contains two simple code samples.</span></span> <span data-ttu-id="4902a-151">1 つの例は X++、もう一方は C\# で記述されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-151">One sample is written in X++, and the other is in C\#.</span></span> <span data-ttu-id="4902a-152">両方のサンプルで同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="4902a-152">Both samples achieve the same result.</span></span> <span data-ttu-id="4902a-153">次の X++ 機能が示されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-153">The following X++ features are demonstrated:</span></span>
-   <span data-ttu-id="4902a-154">`//` 単一行のコメント</span><span class="sxs-lookup"><span data-stu-id="4902a-154">`//` single line comment</span></span>
-   <span data-ttu-id="4902a-155">/\* \*/ 複数行コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-155">/\* \*/ multi-line comment</span></span>
-   <span data-ttu-id="4902a-156">`if` ステートメント</span><span class="sxs-lookup"><span data-stu-id="4902a-156">`if` statement</span></span>
-   <span data-ttu-id="4902a-157">`==` 演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-157">`==` operator</span></span>
-   <span data-ttu-id="4902a-158">`!=` 演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-158">`!=` operator</span></span>
-   <span data-ttu-id="4902a-159">`+` 文字列を連結する演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-159">`+` operator to concatenate strings</span></span>
-   <span data-ttu-id="4902a-160">Global:: 接頭語を使用する場合と使用しない場合の、メッセージ出力の Global::info</span><span class="sxs-lookup"><span data-stu-id="4902a-160">Global::info for message output, with and without the Global:: prefix</span></span>
-   <span data-ttu-id="4902a-161">メッセージ出力の Global::error</span><span class="sxs-lookup"><span data-stu-id="4902a-161">Global::error for message output</span></span>
-   <span data-ttu-id="4902a-162">文字列区切り文字としての一重引用符および二重引用符 (' および ") の使用。</span><span class="sxs-lookup"><span data-stu-id="4902a-162">The use of single and double quotation characters (' and ") as string delimiters.</span></span>

<span data-ttu-id="4902a-163">**注記**: ユーザーに表示される可能性のあるすべての文字列に二重引用符を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4902a-163">**Note**: The best practice is to use double quotation marks for any string that might be displayed to the user.</span></span>

#### <a name="x-sample"></a><span data-ttu-id="4902a-164">X++ サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-164">X++ Sample</span></span>

<span data-ttu-id="4902a-165">この X++ コード サンプルでは、ジョブの形式です。</span><span class="sxs-lookup"><span data-stu-id="4902a-165">This X++ code sample is in the form of a job.</span></span> <span data-ttu-id="4902a-166">アプリケーション オブジェクト ツリー (AOT) にジョブというノードがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-166">There is a node titled Jobs in the Application Object Tree (AOT).</span></span> <span data-ttu-id="4902a-167">この例を [ジョブ] ノードの下に追加して、ジョブを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-167">This sample can be added under the Jobs node, and then the job can be run.</span></span>

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
            warning("This is like info," + " but is for warnings, 3.");
            error("This is like info," + " but is for errors, 4.");
        }
    }

##### <a name="output"></a><span data-ttu-id="4902a-168">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-168">Output</span></span>

<span data-ttu-id="4902a-169">情報ログ ウィンドウからの出力を次に示します: メッセージ (09:49:48) Hello World、1。</span><span class="sxs-lookup"><span data-stu-id="4902a-169">Here is the output from the Infolog window: Message (09:49:48) Hello World, 1.</span></span>
<span data-ttu-id="4902a-170">Hello World、2。</span><span class="sxs-lookup"><span data-stu-id="4902a-170">Hello World, 2.</span></span>
<span data-ttu-id="4902a-171">これは、情報のようなものですが、警告、3 です。</span><span class="sxs-lookup"><span data-stu-id="4902a-171">This is like info, but is for warnings, 3.</span></span>
<span data-ttu-id="4902a-172">これは、情報のようなものですが、エラー、4 です。</span><span class="sxs-lookup"><span data-stu-id="4902a-172">This is like info, but is for errors, 4.</span></span>

#### <a name="c-sample"></a><span data-ttu-id="4902a-173">C# サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-173">C# Sample</span></span>

<span data-ttu-id="4902a-174">次の C# プログラムは、以前の X++ プログラムを書き直したものです。</span><span class="sxs-lookup"><span data-stu-id="4902a-174">The following C# program is a rewrite of the previous X++ program.</span></span> <span data-ttu-id="4902a-175">X++ と C# の違いは、X++ の行をコメントアウトして C# の構文に置き換えることで強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-175">The differences between X++ and C# are highlighted by commenting out the X++ lines, and replacing them with the C# syntax.</span></span>

<span data-ttu-id="4902a-176">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-176">C#</span></span>

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
                Console .Out .WriteLine(
                    "Hello World, Explicit .Out , 1.");
                Console .WriteLine(
                    "Hello World, Implicit default to .Out , 2.");
            }
            if (1 != 1)
            {
                Console .Error .WriteLine(
                    "This message will not appear.");
            }
            else
            {
                Console .Error .WriteLine(".Error is like .Out,"
                    + " but can be for warnings, 3.");
                Console .Error .WriteLine(".Error is like .Out,"
                    + " but is for errors, 4.");
            }
        }
    }

##### <a name="output"></a><span data-ttu-id="4902a-177">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-177">Output</span></span>

<span data-ttu-id="4902a-178">C# コンソールへの実際の出力を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-178">Here is the actual output to the C# console:</span></span>

    Hello World, Explicit .Out, 1. 
    Hello World, Implicit default to .Out, 2. 
    .Error is like .Out, but can be for warnings, 3. 
    .Error is like .Out, but is for errors, 4.

## <a name="x-c-comparison-loops"></a><span data-ttu-id="4902a-179">X++、C# の比較: ループ</span><span class="sxs-lookup"><span data-stu-id="4902a-179">X++, C# Comparison: Loops</span></span>
<span data-ttu-id="4902a-180">このセクションでは、X++ と C\# の間のループの特徴を比較します。</span><span class="sxs-lookup"><span data-stu-id="4902a-180">This section compares the loop features between X++ and C\#.</span></span>

###  <a name="similarities"></a><span data-ttu-id="4902a-181">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-181">Similarities</span></span>

<span data-ttu-id="4902a-182">次の機能は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-182">The following features are the same in X++ and C\#:</span></span>
-   <span data-ttu-id="4902a-183">int プリミティブ データ型の変数の宣言。</span><span class="sxs-lookup"><span data-stu-id="4902a-183">Declarations for variables of the int primitive data type.</span></span> <span data-ttu-id="4902a-184">他のプリミティブ型の宣言はほとんど同じですが、型の名前が異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-184">Declarations for other primitive types are almost the same, but the types might have different names.</span></span>
-   <span data-ttu-id="4902a-185">ループ用 while ステートメント。</span><span class="sxs-lookup"><span data-stu-id="4902a-185">while statement for loops.</span></span>
-   <span data-ttu-id="4902a-186">ループを終了する break ステートメント。</span><span class="sxs-lookup"><span data-stu-id="4902a-186">break statement to exit a loop.</span></span>
-   <span data-ttu-id="4902a-187">ループの先頭に移動するための continue ステートメント。</span><span class="sxs-lookup"><span data-stu-id="4902a-187">continue statement to jump up to the top of a loop.</span></span>
-   <span data-ttu-id="4902a-188"><= (以下) 比較演算子です。</span><span class="sxs-lookup"><span data-stu-id="4902a-188"><= (less than or equal) comparison operator.</span></span>

###  <a name="differences"></a><span data-ttu-id="4902a-189">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-189">Differences</span></span>

<span data-ttu-id="4902a-190">次のテーブルは、C# では異なる X++ の機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-190">The following table lists X++ features that are different in C#.</span></span>

| <span data-ttu-id="4902a-191">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-191">Features</span></span> | <span data-ttu-id="4902a-192">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-192">X++</span></span> | <span data-ttu-id="4902a-193">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-193">C#</span></span> | <span data-ttu-id="4902a-194">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-194">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-195">`for` ステートメント。</span><span class="sxs-lookup"><span data-stu-id="4902a-195">The `for` statement.</span></span>| <span data-ttu-id="4902a-196">for 明細書はループで使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-196">The for statement is available for loops.</span></span>| <span data-ttu-id="4902a-197">C# `for` ステートメントは、X++ の `for` と少し異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-197">The C# `for` statement is slightly different from `for` in X++.</span></span>| <span data-ttu-id="4902a-198">C# では、`for` ステートメントでカウンター整数を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-198">In C# you can declare the counter integer in the `for` statement.</span></span> <span data-ttu-id="4902a-199">ただし X++ では、カウンターは `for` ステートメントの外側で宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-199">But in X++ the counter must be declared outside the `for` statement.</span></span>|
|<span data-ttu-id="4902a-200">++ 増分の演算子。</span><span class="sxs-lookup"><span data-stu-id="4902a-200">++ increment operator.</span></span>|<span data-ttu-id="4902a-201">++ 増分の演算子は X++ で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="4902a-201">An ++ increment operator is available in X++.</span></span> <span data-ttu-id="4902a-202">ただし、++ で修飾された <strong>int</strong> 変数は式としてではなく、ステートメントとしてのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-202">But an <strong>int</strong> variable that is decorated with ++ can only be used as a statement, not as an expression.</span></span> <span data-ttu-id="4902a-203">たとえば、次の X++ コードの行はコンパイルしません。</span><span class="sxs-lookup"><span data-stu-id="4902a-203">For example, the following lines of X++ code would not compile:</span></span><br>`int age=42;`<br> `print age++;`<br> <span data-ttu-id="4902a-204">ただし、次の X++ コードの行はコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="4902a-204">However, the following lines of X++ code would compile:</span></span><br>`int age=42;`<br>`age++; print age;`|<span data-ttu-id="4902a-205">C# 演算子は、X++ での方が柔軟です。</span><span class="sxs-lookup"><span data-stu-id="4902a-205">The C# ++ operator is more flexible than in X++.</span></span>|<span data-ttu-id="4902a-206">次のコード行は、両方の言語で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-206">The following lines of code are the same in both languages:</span></span><ul><li><span data-ttu-id="4902a-207">++ myInteger;</span><span class="sxs-lookup"><span data-stu-id="4902a-207">++ myInteger;</span></span></li><li><span data-ttu-id="4902a-208">myInteger++;</span><span class="sxs-lookup"><span data-stu-id="4902a-208">myInteger++;</span></span></li></ul><span data-ttu-id="4902a-209">ただし、次のコード行は互いに異なる効果を持ち、C# でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="4902a-209">But the following lines of code have a different effect from each other, and are valid only in C#:</span></span><ul><li><span data-ttu-id="4902a-210">yourInt = ++myInt;</span><span class="sxs-lookup"><span data-stu-id="4902a-210">yourInt = ++myInt;</span></span></li><li><span data-ttu-id="4902a-211">yourInt = myInt++;</span><span class="sxs-lookup"><span data-stu-id="4902a-211">yourInt = myInt++;</span></span></li></ul>|
| <span data-ttu-id="4902a-212">剰余演算子。</span><span class="sxs-lookup"><span data-stu-id="4902a-212">modulo operator.</span></span>| <span data-ttu-id="4902a-213">X++ では、剰余演算子は mod です。</span><span class="sxs-lookup"><span data-stu-id="4902a-213">In X++ the modulo operator is mod.</span></span>| <span data-ttu-id="4902a-214">C# では、剰余演算子は % です。</span><span class="sxs-lookup"><span data-stu-id="4902a-214">In C# the modulo operator is %.</span></span>| <span data-ttu-id="4902a-215">モジュロ演算子のシンボルは異なりますが、その動作は両方の言語で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-215">The symbols for the modulo operator are different, but their behavior is the same in both languages.</span></span>|
| <span data-ttu-id="4902a-216">既に開始されているコンソール プログラムを一時的に中断します。</span><span class="sxs-lookup"><span data-stu-id="4902a-216">Temporarily suspend a console program that has already begun.</span></span>| <span data-ttu-id="4902a-217">`pause` ステートメント。</span><span class="sxs-lookup"><span data-stu-id="4902a-217">The `pause` statement.</span></span>| <span data-ttu-id="4902a-218">C# では、コマンド ライン プログラムを次のコード行で一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-218">In C#, a command line program can be paused by the following line of code:</span></span><br>`Console.In.Read();`| <span data-ttu-id="4902a-219">X++ では、モーダル ダイアログ ボックスで OK ボタンをクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="4902a-219">In X++ you continue by clicking an OK button on a modal dialog box.</span></span> <span data-ttu-id="4902a-220">C# では、キーボードの任意のキーボードを押して続行します。</span><span class="sxs-lookup"><span data-stu-id="4902a-220">In C# you continue by pressing any keyboard on the keyboard.</span></span>|
| <span data-ttu-id="4902a-221">メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-221">Display a message.</span></span>| <span data-ttu-id="4902a-222">X++ では、`print` ステートメントは印刷ウィンドウにメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-222">In X++, the `print` statement displays a message in the Print window.</span></span>| <span data-ttu-id="4902a-223">C# では、次のコード行でメッセージをコンソールに表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-223">In C# a message can be displayed on the console by the following line of code:</span></span><br>`Console.WriteLine();`| <span data-ttu-id="4902a-224">X++ `print` 関数は、テスト時にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-224">The X++ `print` function is used only when you test.</span></span> <span data-ttu-id="4902a-225">`print` を使用する X++ プログラムは、ほとんどの場合コード内のどこか後で `pause` 明細書を使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-225">An X++ program that uses `print` almost always uses the `pause` statement somewhere later in the code.</span></span> <span data-ttu-id="4902a-226">生産 X++ コードについては、`print` の代わりに Global::info メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-226">For production X++ code, use the Global::info Method instead of `print`.</span></span> <span data-ttu-id="4902a-227">`strfmt` 関数はしばしば `info` と一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-227">The `strfmt` function is often used together with `info`.</span></span> <span data-ttu-id="4902a-228">`info` の後に `pause` を使用する理由はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-228">There is no reason to use `pause` after `info`.</span></span>|
| <span data-ttu-id="4902a-229">音を作成します。</span><span class="sxs-lookup"><span data-stu-id="4902a-229">Make a sound.</span></span>| <span data-ttu-id="4902a-230">ビープ音機能は、人間に聞こえる音を鳴らします。</span><span class="sxs-lookup"><span data-stu-id="4902a-230">The beep function makes a sound that you can hear.</span></span> | <span data-ttu-id="4902a-231">C# では、聞こえるサウンドが次のコード行で発行されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-231">In C# a sound that you can hear is issued by the following line of code:</span></span><br>`Console.Beep();`| <span data-ttu-id="4902a-232">ステートメントはそれぞれ短いトーンを作ります。</span><span class="sxs-lookup"><span data-stu-id="4902a-232">The statements each produce a short tone.</span></span>|


### <a name="print-and-globalinfo"></a><span data-ttu-id="4902a-233">Print および Global::info</span><span class="sxs-lookup"><span data-stu-id="4902a-233">Print and Global::info</span></span>

<span data-ttu-id="4902a-234">ループ用の X++ コード サンプルは、`print` 関数を使用して結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-234">The X++ code samples for loops use the `print` function to display results.</span></span> <span data-ttu-id="4902a-235">X++ では、`print` ステートメントを使用して、まず文字列に変換する関数を呼び出すことなく、任意のプリミティブ データ型を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-235">In X++ you can use the `print` statement can display any primitive data type without having to call functions that convert it to a string first.</span></span> <span data-ttu-id="4902a-236">これにより、簡単なテスト環境では `print` が便利になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-236">This makes `print` useful in quick test situations.</span></span> <span data-ttu-id="4902a-237">一般に、Global::info メソッドは `print` より頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-237">Generally the Global::info method is used more often than `print`.</span></span> <span data-ttu-id="4902a-238">`info` メソッドは文字列のみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-238">The `info` method can only display strings.</span></span> <span data-ttu-id="4902a-239">したがって、strfmt 関数はしばしば `info` と一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-239">Therefore the strfmt function is often used together with `info`.</span></span> <span data-ttu-id="4902a-240">印刷ウィンドウの内容をクリップボードにコピー (Ctrl+C などで) できない `print` の制限。</span><span class="sxs-lookup"><span data-stu-id="4902a-240">A limitation of `print` is that you cannot copy the contents of the Print window to the clipboard (such as with Ctrl+C).</span></span> <span data-ttu-id="4902a-241">Global::info は情報ログ ウィンドウに書き込みをし、クリップボードへのコピーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4902a-241">Global::info writes to the Infolog window which does support copy to the clipboard.</span></span>

### <a name="example-1-the-while-loop"></a><span data-ttu-id="4902a-242">例 1: While Loop</span><span class="sxs-lookup"><span data-stu-id="4902a-242">Example 1: The while Loop</span></span>

<span data-ttu-id="4902a-243">**while** キーワードは、X++ と C# 両方でのループをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4902a-243">The **while** keyword supports looping in both X++ and C#.</span></span>

#### <a name="x-sample-of-while"></a><span data-ttu-id="4902a-244">X++ while のサンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-244">X++ Sample of while</span></span>

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
<span data-ttu-id="4902a-245">}</span><span class="sxs-lookup"><span data-stu-id="4902a-245">}</span></span> 

##### <a name="output"></a><span data-ttu-id="4902a-246">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-246">Output</span></span>

<span data-ttu-id="4902a-247">X++ 印刷ウィンドウの出力は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4902a-247">The output in the X++ Print window is as follows:</span></span>

    1
    2
    3
    4

#### <a name="c-sample-of-while"></a><span data-ttu-id="4902a-248">C# 中のサンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-248">C# Sample of while</span></span>

<span data-ttu-id="4902a-249">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-249">C#</span></span>

    using System;
    public class Pgm_CSharp
    {
        static void Main( string[] args )
        {
            new Pgm_CSharp().Rs002a_CSharp_ControlOFlowWhile();
        }
        void Rs002a_CSharp_ControlOFlowWhile()
        {
            int nLoops = 1;
            while (nLoops <= 88)
            {
                Console.Out.WriteLine( nLoops.ToString() );
                Console.Out.WriteLine( "(Press any key to resume.)" );
                // Paused until user presses a key.
                Console.In.Read();
                if ((nLoops % 4) == 0) break;
                ++ nLoops;
            }
            Console.Beep();
            Console.In.Read();
        }
    }


 
##### <a name="output"></a><span data-ttu-id="4902a-250">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-250">Output</span></span>

<span data-ttu-id="4902a-251">C# プログラムのコンソール出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-251">The console output from the C# program is as follows:</span></span>

    [C:\MyDirectory\]
    >> Rosetta_CSharp_1.exe
    1
    (Press any key to resume.)
    2
    (Press any key to resume.)
    3
    (Press any key to resume.)
    4
    (Press any key to resume.)

### <a name="example-2-the-for-loop"></a><span data-ttu-id="4902a-252">例 2: For Loop</span><span class="sxs-lookup"><span data-stu-id="4902a-252">Example 2: The for Loop</span></span>

<span data-ttu-id="4902a-253">**for** キーワードは、X++ と C# 両方でのループをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4902a-253">The **for** keyword supports looping in both X++ and C#.</span></span>

#### <a name="x-sample-of-for"></a><span data-ttu-id="4902a-254">X++ for のサンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-254">X++ Sample of for</span></span>

<span data-ttu-id="4902a-255">X++ では、カウンター変数は **for** ステートメントの一部として宣言できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-255">In X++ the counter variable cannot be declared as part of the **for** statement.</span></span>

    static void JobRs002a_LoopsWhileFor(Args _args)
    {
        int ii; // The counter.
        for (ii=1; ii < 5; ii++)
        {
            print ii;
            pause;
            // You must click the OK button to proceed
            // beyond a pause statement.
            // ii is always less than 99.
            if (ii < 99)
            {
                continue;
            }
            print "This message never appears.";
        }
        pause;
<span data-ttu-id="4902a-256">}</span><span class="sxs-lookup"><span data-stu-id="4902a-256">}</span></span>


 
##### <a name="output"></a><span data-ttu-id="4902a-257">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-257">Output</span></span>

<span data-ttu-id="4902a-258">X++ 印刷ウィンドウの出力は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4902a-258">The output in the X++ Print window is as follows:</span></span>

    1
    2
    3
    4

#### <a name="c-sample-of-for"></a><span data-ttu-id="4902a-259">C# のサンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-259">C# Sample of for</span></span>

<span data-ttu-id="4902a-260">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-260">C#</span></span>

    using System;
    public class Pgm_CSharp
    {
        static void Main( string[] args )
        {
            new Pgm_CSharp().Rs002a_CSharp_ControlOFlowFor();
        }
        void Rs002a_CSharp_ControlOFlowFor()
        {
            int nLoops = 1,
                ii;
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


 
##### <a name="output"></a><span data-ttu-id="4902a-261">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-261">Output</span></span>

<span data-ttu-id="4902a-262">C# プログラムのコンソール出力は次のとおりです。1 (任意のキーを押して再開します。) 2 (任意のキーを押して再開します。) 3 (任意のキーを押して再開します。) 4 (任意のキーを押して再開します。) (任意のキーを押して再開します。)</span><span class="sxs-lookup"><span data-stu-id="4902a-262">The console output from the C# program is as follows: 1 (Press any key to resume.) 2 (Press any key to resume.) 3 (Press any key to resume.) 4 (Press any key to resume.) (Press any key to resume.)</span></span>

### <a name="x-c-comparison-switch"></a><span data-ttu-id="4902a-263">X++、C# の比較: Switch</span><span class="sxs-lookup"><span data-stu-id="4902a-263">X++, C# Comparison: Switch</span></span>

<span data-ttu-id="4902a-264">X++ と C# の両方では、**switch** ステートメントに、キーワード **case**、**break**、および **default** があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-264">In both X++ and C#, the **switch** statement involves the keywords **case**, **break**, and **default**.</span></span> <span data-ttu-id="4902a-265">次のテーブルは、X++ および C\# の間の **switch** ステートメントの相違点を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-265">The following table lists the differences in the **switch** statement between X++ and C\#.</span></span>

| <span data-ttu-id="4902a-266">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-266">Feature</span></span>  | <span data-ttu-id="4902a-267">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-267">X++</span></span> | <span data-ttu-id="4902a-268">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-268">C#</span></span> | <span data-ttu-id="4902a-269">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-269">Comments</span></span> |
|--------|-----------|------------|-----|
| <span data-ttu-id="4902a-270">各 case ブロックの末尾の `break;`</span><span class="sxs-lookup"><span data-stu-id="4902a-270">`break;` at the end of each case block</span></span>       | <span data-ttu-id="4902a-271">X++ では、いずれかの **case** ブロックが **switch** 句の式の値と一致する場合、`break;` ステートメントに達するまで他のすべての **case** および **default** ブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-271">In X++, when any **case** block matches the expression value on the **switch** clause, all other **case** and **default** blocks are executed until a `break;` statement is reached.</span></span> <span data-ttu-id="4902a-272">`break;` ステートメントは、X++ の **switch** ステートメントでは必要ありませんが、`break;` ステートメントはほとんどすべての実践的な状況において重要です。</span><span class="sxs-lookup"><span data-stu-id="4902a-272">No `break;` statement is ever required in an X++ **switch** statement, but `break;` statements are important in almost all practical situations.</span></span> | <span data-ttu-id="4902a-273">C\# では、`break;` ステートメントが **case** または **default** ブロックのステートメントの後に常に必要になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-273">In C\#, a `break;` statement is always needed after the statements in a **case** or **default** block.</span></span> <span data-ttu-id="4902a-274">**ケース**句に次の**ケース**句との間のステートメントがない場合、2 つの**ケース**節の間に `break;` ステートメントは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-274">If a **case** clause has no statements between itself and the next **case** clause, a `break;` statement is not required between the two **case** clauses.</span></span> | <span data-ttu-id="4902a-275">コードを編集する次のプログラマが混乱する可能性があるので、case **ブロック** の後の `break;` ステートメントを省略することをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="4902a-275">We recommend against omitting the `break;` statement after any case **block**, because it can confuse the next programmer who edits the code.</span></span> |
| <span data-ttu-id="4902a-276">**既定**ブロックの末尾の `break;`</span><span class="sxs-lookup"><span data-stu-id="4902a-276">`break;` at the end of the **default** block</span></span> | <span data-ttu-id="4902a-277">X++ では、`break;` ステートメントを **default** ブロックの最後に追加する効果はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-277">In X++ there is no effect of adding a `break;` statement at the end of the **default** block.</span></span>   | <span data-ttu-id="4902a-278">C\# では、コンパイラは **default** ブロックの最後に `break;` ステートメントを必要とします。</span><span class="sxs-lookup"><span data-stu-id="4902a-278">In C\# the compiler requires a `break;` statement at the end of the **default** block.</span></span> | <span data-ttu-id="4902a-279">詳細については、「明細書の切り替え」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-279">For more information, see Switch Statements.</span></span> |
| <span data-ttu-id="4902a-280">**case** ブロックの定数値のみ</span><span class="sxs-lookup"><span data-stu-id="4902a-280">Only constant values on a **case** block</span></span>     | <span data-ttu-id="4902a-281">X++ では、case ブロックでリテラル値または変数のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-281">In X++ you can specify either a literal value or a variable on a case block.</span></span> <span data-ttu-id="4902a-282">たとえば、ケース myInteger: を書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-282">For example, you can write case myInteger:.</span></span>  | <span data-ttu-id="4902a-283">C\# では、**case** ブロックごとに正確に 1 つのリテラル値を指定する必要があり、変数は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="4902a-283">In C\# you must specify exactly one literal value on each **case** block, and no variables are allowed.</span></span> | <span data-ttu-id="4902a-284">コメントはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-284">No comments.</span></span>  |
| <span data-ttu-id="4902a-285">1 つの **case** ブロックにある複数の値</span><span class="sxs-lookup"><span data-stu-id="4902a-285">Multiple values on one **case** block</span></span>        | <span data-ttu-id="4902a-286">X++ では、case ブロックごとに複数の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-286">In X++ you can specify multiple values on each case block.</span></span> <span data-ttu-id="4902a-287">値は、コンマで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-287">The values must be separated by a comma.</span></span> <span data-ttu-id="4902a-288">たとえば、`case 4,5,myInteger:` を書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-288">For example, you can write `case 4,5,myInteger:`.</span></span>    | <span data-ttu-id="4902a-289">C\# では、**case** ブロックごとに正確に 1 つの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-289">In C\# you must specify exactly one value on each **case** block.</span></span> | <span data-ttu-id="4902a-290">X++ では、1 つまたは複数の case ブロックの最後にある `break;` ステートメントを省略するよりも、**case** ブロックに複数の値を書き込む方が適切です。</span><span class="sxs-lookup"><span data-stu-id="4902a-290">In X++ it is better to write multiple values on one **case** block than to omit the `break;` statement at the end of one or more case blocks.</span></span> |

### <a name="code-examples-for-switch"></a><span data-ttu-id="4902a-291">切り替えのコードの例</span><span class="sxs-lookup"><span data-stu-id="4902a-291">Code Examples for switch</span></span>

<span data-ttu-id="4902a-292">次のセクションでは、X++ と C\# での比較可能な switch ステートメントを示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-292">The following sections show comparable switch statements in X++ and C\#.</span></span>

#### <a name="x-switch-example"></a><span data-ttu-id="4902a-293">X++ 切り替えの例</span><span class="sxs-lookup"><span data-stu-id="4902a-293">X++ switch Example</span></span>

<span data-ttu-id="4902a-294">以下に、X++ スイッチの例を示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-294">The X++ switch example shows the following:</span></span>
-   <span data-ttu-id="4902a-295">case iTemp: および case (93-90): は、**case** 式は、C\# とは異なり、定数に限定されないことを示すため。</span><span class="sxs-lookup"><span data-stu-id="4902a-295">case iTemp: and case (93-90): to show that **case** expressions are not limited to constants, as they are in C\#.</span></span>
-   <span data-ttu-id="4902a-296">`//break;` は、 X++ では `break;` ステートメントが必須ではないことを示していますが、ほとんどの場合望ましいです。</span><span class="sxs-lookup"><span data-stu-id="4902a-296">`//break;` to show that `break;` statements are not required in X++, although they are almost always desirable.</span></span>
-   <span data-ttu-id="4902a-297">case 2, (93-90), 5: は、X++ でが、1 つの **case** 句に複数の式をリストできることを示すため。</span><span class="sxs-lookup"><span data-stu-id="4902a-297">case 2, (93-90), 5: to show that multiple expressions can be listed on one **case** clause in X++.</span></span>

<span data-ttu-id="4902a-298">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-298">X++</span></span>

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


#### <a name="c-switch-example"></a><span data-ttu-id="4902a-299">C# 切り替えの例</span><span class="sxs-lookup"><span data-stu-id="4902a-299">C# switch Example</span></span>

<span data-ttu-id="4902a-300">以下に、C\# スイッチの例を示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-300">The C\# switch example shows the following:</span></span>
-   <span data-ttu-id="4902a-301">case 1: には、**case** 句では定数式のみを指定できることを説明したコメントがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-301">case 1: has a comment explaining that only constant expressions can be given on a **case** clause.</span></span>
-   <span data-ttu-id="4902a-302">`break;` ステートメントは、 C\# で必要とされるステートメントを持つ各 **case** ブロックの最後のステートメントの後に発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-302">`break;` statements occur after the last statement in each **case** block that has statements, as is required by C\#.</span></span>

<span data-ttu-id="4902a-303">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-303">C#</span></span>

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


 
## <a name="x-c-comparison-string-case-and-delimiters"></a><span data-ttu-id="4902a-304">X++、C# の比較: 文字列の大文字小文字の区別および区切り記号</span><span class="sxs-lookup"><span data-stu-id="4902a-304">X++, C# Comparison: String Case and Delimiters</span></span>
<span data-ttu-id="4902a-305">このセクションでは、X++ と C\# の混合ケーシングによる文字列の処理を比較します。</span><span class="sxs-lookup"><span data-stu-id="4902a-305">This section compares the treatment of strings with mixed casing in X++ and C\#.</span></span> <span data-ttu-id="4902a-306">また、X++ で使用できる文字列の区切り記号についても説明します。</span><span class="sxs-lookup"><span data-stu-id="4902a-306">It also explains the string delimiters that are available in X++.</span></span>

### <a name="similarities"></a><span data-ttu-id="4902a-307">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-307">Similarities</span></span>

<span data-ttu-id="4902a-308">次の X++ 機能は C\# の機能と同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-308">The following X++ features are the same as in C\#:</span></span>
-   <span data-ttu-id="4902a-309">バックスラッシュ (\\) は、文字列の区切り記号のエスケープ演算子です。</span><span class="sxs-lookup"><span data-stu-id="4902a-309">The backslash (\\) is the escape operator for string delimiters.</span></span>
-   <span data-ttu-id="4902a-310">アット マーク (@) は、文字列の開始引用符の直前に書かれていると、バックスラッシュのエスケープ効果を無効にします。</span><span class="sxs-lookup"><span data-stu-id="4902a-310">The at sign (@) nullifies the escape effect of the backslash when the at sign is written immediately before the open quotation mark of a string.</span></span>
-   <span data-ttu-id="4902a-311">プラス記号 (+) は文字列連結演算子です。</span><span class="sxs-lookup"><span data-stu-id="4902a-311">The plus sign (+) is the string concatenation operator.</span></span>

### <a name="differences"></a><span data-ttu-id="4902a-312">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-312">Differences</span></span>

<span data-ttu-id="4902a-313">C\# では異なる X++ 機能を以下の表に一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-313">X++ features that are different in C\# are listed in the following table.</span></span>

| <span data-ttu-id="4902a-314">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-314">Feature</span></span> | <span data-ttu-id="4902a-315">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-315">X++</span></span> | <span data-ttu-id="4902a-316">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-316">C#</span></span> | <span data-ttu-id="4902a-317">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-317">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-318">`== `比較演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-318">`== `comparison operator</span></span>| <span data-ttu-id="4902a-319">区別しない: `==` 演算子は文字列の大文字と小文字の差異を区別しません。</span><span class="sxs-lookup"><span data-stu-id="4902a-319">Insensitive: the `==` operator is insensitive to differences in string casing.</span></span>| <span data-ttu-id="4902a-320">C# では、`==` 演算子は文字列の大文字と小文字の差異を区別します。</span><span class="sxs-lookup"><span data-stu-id="4902a-320">In C#, the `==` operator is sensitive to differences in string casing.</span></span>| <span data-ttu-id="4902a-321">X++ では、文字列間の大文字と小文字の比較には strCmp 関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-321">In X++ you can use the strCmp Function for case sensitive comparisons between strings.</span></span>|
| <span data-ttu-id="4902a-322">文字列の区切り記号</span><span class="sxs-lookup"><span data-stu-id="4902a-322">String delimiters</span></span>| <span data-ttu-id="4902a-323">X++ では、文字列の区切り記号として単一引用符 (') または二重引用符 (`"`) のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-323">In X++ you can use either the single (') or double (`"`) quotation mark as the string delimiter.</span></span> <span data-ttu-id="4902a-324">**注記**: 通常、ユーザーに表示される可能性のある文字列に二重引用符を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4902a-324">**Note**: Usually the best practice is to use double quotation marks for strings that might be displayed to the user.</span></span> <span data-ttu-id="4902a-325">ただし、二重引用符文字が文字列の文字のいずれかである場合、単一引用符で文字列を区切るのが便利です。</span><span class="sxs-lookup"><span data-stu-id="4902a-325">However, it is convenient to delimit a string with single quotation marks when a double quotation mark is one of the characters in the string.</span></span>| <span data-ttu-id="4902a-326">C# では、文字列の区切り記号として二重引用符を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-326">In C# you must use the double quotation mark as the string delimiter.</span></span> <span data-ttu-id="4902a-327">これは、タイプ `System.String` を指します。</span><span class="sxs-lookup"><span data-stu-id="4902a-327">This refers to the type `System.String`.</span></span>| <span data-ttu-id="4902a-328">X++ および C# では、リテラル文字列の区切り記号を埋め込み、\ でエスケープするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-328">In X++ and C# you have the option of embedding a delimiter in a literal string and escaping it with \.</span></span> <br><span data-ttu-id="4902a-329">X++ では、エスケープを使用しなくても、二重引用符で区切られた文字列に単一引用符 (または逆) を埋め込むことで代用することもできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-329">In X++ you also have the alternative of embedding single quotation marks in a string that is delimited by double quotation marks (or the reverse), without having to use the escape.</span></span>|
| <span data-ttu-id="4902a-330">文字区切り文字</span><span class="sxs-lookup"><span data-stu-id="4902a-330">Character delimiters</span></span>| <span data-ttu-id="4902a-331">X++ には文字列データ型 (`str`) がありますが、文字の種類はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-331">X++ has a string data type (`str`), but no character type.</span></span>| <span data-ttu-id="4902a-332">C# では、文字の区切り記号として単一引用符を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-332">In C# you must use the single quotation mark as the character delimiter.</span></span> <span data-ttu-id="4902a-333">これは、タイプ `System.Char` を指します。</span><span class="sxs-lookup"><span data-stu-id="4902a-333">This refers to the type `System.Char`.</span></span>| <span data-ttu-id="4902a-334">.NET Framework では、長さが 1 の `System.String` は `System.Char` 文字とは異なるデータ型です。</span><span class="sxs-lookup"><span data-stu-id="4902a-334">In the .NET Framework, a `System.String` of length one is a different data type than a `System.Char` character.</span></span>|

### <a name="example-1-case-sensitivity-of-the--operator"></a><span data-ttu-id="4902a-335">例 1: Case Sensitivity of the == オペレーター</span><span class="sxs-lookup"><span data-stu-id="4902a-335">Example 1: Case Sensitivity of the == Operator</span></span>

<span data-ttu-id="4902a-336">次の例に示すように、`==` と != 演算子は、X++ では大文字と小文字が区別されませんが、C\# では区別されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-336">The `==` and != operators are case insensitive in X++, but are case sensitive in C\#, as is illustrated by the following example.</span></span>

| <span data-ttu-id="4902a-337">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-337">X++</span></span>    | <span data-ttu-id="4902a-338">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-338">C#</span></span>  | <span data-ttu-id="4902a-339">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-339">Comments</span></span>       |
|----------------|---------|-----------|
| `"HELLO" == "hello"` <br><span data-ttu-id="4902a-340">X++ の場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="4902a-340">True in X++.</span></span> | `"HELLO" == "hello"` <br><span data-ttu-id="4902a-341">C# の False。</span><span class="sxs-lookup"><span data-stu-id="4902a-341">False in C#.</span></span> | <span data-ttu-id="4902a-342">X++ と C# の間の異なるケース比較。</span><span class="sxs-lookup"><span data-stu-id="4902a-342">Different case comparisons between X++ and C#.</span></span> |

### <a name="example-2-the--string-concatenation-operator"></a><span data-ttu-id="4902a-343">例 2: The + 文字列連結オペレーター</span><span class="sxs-lookup"><span data-stu-id="4902a-343">Example 2: The + String Concatenation Operator</span></span>

<span data-ttu-id="4902a-344">+ および = 演算子は、次の表の例に示すように、X++ と C\# の両方で文字列を連結するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-344">The + and += operators are used to concatenate strings in both X++ and C\#, as is shown by the examples in the following table.</span></span>

| <span data-ttu-id="4902a-345">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-345">X++</span></span>  | <span data-ttu-id="4902a-346">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-346">C#</span></span>   | <span data-ttu-id="4902a-347">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-347">Comments</span></span> |
|---------|--------------------|----------------------------|
| `myString1 = "Hello" + " world";` <br><span data-ttu-id="4902a-348">結果は等しくなります:</span><span class="sxs-lookup"><span data-stu-id="4902a-348">Result is equality:</span></span> <br>`myString1 == "Hello world"`  | <span data-ttu-id="4902a-349">(X++ と同じです。)</span><span class="sxs-lookup"><span data-stu-id="4902a-349">(Same as for X++.)</span></span> | <span data-ttu-id="4902a-350">X++ と C# の両方では、+ 演算子の動作はオペランドのデータ型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-350">In both X++ and C#, the behavior of the + operator depends on the data type of its operands.</span></span> <span data-ttu-id="4902a-351">演算子は、文字列を連結したり、数値を追加します。</span><span class="sxs-lookup"><span data-stu-id="4902a-351">The operator concatenates strings, or adds numbers.</span></span> |
| `mystring2 = "Hello";` <br>`myString2 += " world";` <br><span data-ttu-id="4902a-352">結果は等しくなります: `myString2 == "Hello world"`</span><span class="sxs-lookup"><span data-stu-id="4902a-352">Result is equality: `myString2 == "Hello world"`</span></span> | <span data-ttu-id="4902a-353">(X++ と同じです。)</span><span class="sxs-lookup"><span data-stu-id="4902a-353">(Same as for X++.)</span></span> | <span data-ttu-id="4902a-354">X++ と C# の両方では、次のステートメントは同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-354">In both X++ and C#, the following statements are equivalent:</span></span> <br>`a = a + b;` <br>`a += b;`  |

### <a name="example-3-embedding-and-escaping-string-delimiters"></a><span data-ttu-id="4902a-355">例 3: 文字列の区切り記号を埋め込みおよび分離</span><span class="sxs-lookup"><span data-stu-id="4902a-355">Example 3: Embedding and Escaping String Delimiters</span></span>

<span data-ttu-id="4902a-356">X++ の文字列を区切るには、単一または二重引用符を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-356">Either single or double quotation marks can be used to delimit strings in X++.</span></span> <span data-ttu-id="4902a-357">エスケープ文字 (\\) は、区切り記号を文字列に埋め込むために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-357">The escape character (\\) can be used to embed delimiters in a string.</span></span> <span data-ttu-id="4902a-358">この点については、次のテーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-358">These are illustrated in the following table.</span></span>

| <span data-ttu-id="4902a-359">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-359">X++</span></span> | <span data-ttu-id="4902a-360">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-360">C#</span></span>         | <span data-ttu-id="4902a-361">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-361">Comments</span></span>   |
|---------|-----|--------------------------------------|
| `myString1 = "He said \"yes\".";` <br><span data-ttu-id="4902a-362">結果:</span><span class="sxs-lookup"><span data-stu-id="4902a-362">Result:</span></span> <br>`He said "yes".`  | <span data-ttu-id="4902a-363">(X++ と同じです。)</span><span class="sxs-lookup"><span data-stu-id="4902a-363">(Same as for X++.)</span></span>  | <span data-ttu-id="4902a-364">エスケープ文字を使用すると、文字列の区切り記号を文字列に埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-364">The escape character enables you to embed string delimiters inside strings.</span></span>   |
| `myString2 = 'He said "yes".';` <br><span data-ttu-id="4902a-365">結果:</span><span class="sxs-lookup"><span data-stu-id="4902a-365">Result:</span></span> <br>`He said "yes".`  | <span data-ttu-id="4902a-366">C# 構文では、文字列を区切るための単一引用符は使用できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-366">C# syntax does not allow for single quotation marks to delimit strings.</span></span>    | <span data-ttu-id="4902a-367">ユーザーにより表示される場合のある文字列については、次の例で示すように、単一引用符ではなくエスケープ文字を使用するためのベスト プラクティスと見なされます。</span><span class="sxs-lookup"><span data-stu-id="4902a-367">For strings that may be seen by the user, it is considered a best practice to use the escape character instead of the single quotation marks as shown in the example.</span></span>   |
| `myString3 = "He said 'yes'.";` <br><span data-ttu-id="4902a-368">結果:</span><span class="sxs-lookup"><span data-stu-id="4902a-368">Result:</span></span> <br>`He said 'yes'.` | <span data-ttu-id="4902a-369">(X++ と同じです。)</span><span class="sxs-lookup"><span data-stu-id="4902a-369">(Same as for X++.)</span></span> | <span data-ttu-id="4902a-370">X++ では、文字列が単一引用符の区切り記号で始まらない限り、単一引用符は区切り記号として扱われません。</span><span class="sxs-lookup"><span data-stu-id="4902a-370">In X++, the single quotation marks are not treated as delimiters unless the string starts with a single quotation mark delimiter.</span></span> <span data-ttu-id="4902a-371">C# では、単一引用符に文字列の特別な意味はなく、文字列を区切るために使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-371">In C# the single quotation mark has no special meaning for strings, and it cannot be used to delimit strings.</span></span> <span data-ttu-id="4902a-372">C# では、単一引用符は型 `System.Char` のリテラルに必要な区切り記号です。</span><span class="sxs-lookup"><span data-stu-id="4902a-372">In C# the single quotation mark is the required delimiter for literals of type `System.Char`.</span></span> <span data-ttu-id="4902a-373">X++ には文字データ型がありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-373">X++ has no character data type.</span></span> |
| `str myString4 = 'C';` <br><span data-ttu-id="4902a-374">ここで、単一引用符は文字列の区切り記号です。</span><span class="sxs-lookup"><span data-stu-id="4902a-374">Here the single quotation is a string delimiter.</span></span> | `char myChar4 = 'C';` <br><span data-ttu-id="4902a-375">ここで、単一引用符は `System.String` 区切り記号ではなく、`System.Char` 区切り記号です。</span><span class="sxs-lookup"><span data-stu-id="4902a-375">Here the single quotation mark is a `System.Char` delimiter, not a `System.String` delimiter.</span></span> | <span data-ttu-id="4902a-376">X++ には .NET Framework の `System.Char` に対応するデータ型はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-376">X++ has no data type that corresponds to `System.Char` in the .NET Framework.</span></span> <span data-ttu-id="4902a-377">長さが 1 に制限されている X++ 文字列は、まだ文字列であり、文字データ型ではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-377">An X++ string that is limited to a length of one is still a string, not a character data type.</span></span> |

### <a name="example-4-single-escape-character"></a><span data-ttu-id="4902a-378">例 4: 単一のエスケープ文字</span><span class="sxs-lookup"><span data-stu-id="4902a-378">Example 4: Single Escape Character</span></span>

<span data-ttu-id="4902a-379">入力または出力の単一のエスケープ文字を示す例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-379">Examples that illustrate the single escape character in either the input or the output are shown in the following table.</span></span>

| <span data-ttu-id="4902a-380">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-380">X++</span></span>    | <span data-ttu-id="4902a-381">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-381">C#</span></span> | <span data-ttu-id="4902a-382">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-382">Comments</span></span>     |
|-----------------------|--------|------------------|
| `myString1 = "Red\ shoe";` <br><span data-ttu-id="4902a-383">結果:</span><span class="sxs-lookup"><span data-stu-id="4902a-383">Result:</span></span> <br>`Red shoe`     | <span data-ttu-id="4902a-384">C# のリテラル文字列には、"\ " のようにエスケープの後にスペースが続く 2 つの文字シーケンスを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-384">A literal string in C# cannot contain the two character sequence of escape followed by a space, such as "\ ".</span></span> <span data-ttu-id="4902a-385">コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-385">A compiler error occurs.</span></span> | <span data-ttu-id="4902a-386">X++ コンパイラは、連続した 2 文字の "\" を検出すると、その 1 つのエスケープ文字は切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="4902a-386">When the X++ compiler encounters the two character sequence of "\ ", it discards the single escape character.</span></span> |
| `myString2 = "Red\\ shoe";` <br><span data-ttu-id="4902a-387">結果:</span><span class="sxs-lookup"><span data-stu-id="4902a-387">Result:</span></span> <br>`Red\ shoe` | <span data-ttu-id="4902a-388">(X++ と同じです。)</span><span class="sxs-lookup"><span data-stu-id="4902a-388">(Same as for X++.)</span></span>  | <span data-ttu-id="4902a-389">エスケープ文字のペアにおいて、1 文字目は 2 文字目の特別な意味をなくします。</span><span class="sxs-lookup"><span data-stu-id="4902a-389">In a pair of escape characters, the first negates the special meaning of the second.</span></span>     |

## <a name="comparison-array-syntax"></a><span data-ttu-id="4902a-390">比較: 配列の構文</span><span class="sxs-lookup"><span data-stu-id="4902a-390">Comparison: Array Syntax</span></span>

<span data-ttu-id="4902a-391">X++ と C\# の配列の機能と構文には類似点と相違点があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-391">There are similarities and differences in the features and syntax for arrays in X++ versus C\#.</span></span>

### <a name="similarities"></a><span data-ttu-id="4902a-392">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-392">Similarities</span></span>

<span data-ttu-id="4902a-393">X++ と C# の配列の構文と処理は、全体的にかなり似ています。</span><span class="sxs-lookup"><span data-stu-id="4902a-393">Overall there is much similarity in the syntax and treatment of arrays in X++ and C#.</span></span> <span data-ttu-id="4902a-394">ただし、多くの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-394">However there are many differences.</span></span>

### <a name="differences"></a><span data-ttu-id="4902a-395">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-395">Differences</span></span>

<span data-ttu-id="4902a-396">次のテーブルは、X++ と C#で異なる配列の [] 構文の領域を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-396">The following table lists areas in the [] syntax for arrays that are different for X++ and C#.</span></span>

| <span data-ttu-id="4902a-397">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="4902a-397">Category</span></span> | <span data-ttu-id="4902a-398">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-398">X++</span></span> | <span data-ttu-id="4902a-399">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-399">C#</span></span> | <span data-ttu-id="4902a-400">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-400">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-401">申告</span><span class="sxs-lookup"><span data-stu-id="4902a-401">Declaration</span></span>| <span data-ttu-id="4902a-402">配列は変数名に追加され角カッコ付きで宣言されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-402">An array is declared with square brackets appended to the variable name.</span></span>| <span data-ttu-id="4902a-403">配列はデータ型に追加され角カッコ付きで宣言されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-403">An array is declared with square brackets appended to the data type.</span></span>| `int myInts[]; // X++` <br><span data-ttu-id="4902a-404">**注記**: X++ 配列は、メソッド内のパラメーターにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-404">**Note**: An X++ array cannot be a parameter in a method.</span></span><br>`int[] myInts; // C#`|
| <span data-ttu-id="4902a-405">申告</span><span class="sxs-lookup"><span data-stu-id="4902a-405">Declaration</span></span>| <span data-ttu-id="4902a-406">配列の構文は、`int` や `str` などのプリミティブ データ型のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4902a-406">The array syntax supports only primitive data types, such as `int` and `str`.</span></span> <span data-ttu-id="4902a-407">構文はクラスまたはテーブルをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4902a-407">The syntax does not support classes or tables.</span></span>|<span data-ttu-id="4902a-408">配列の構文は、プリミティブ データ型およびプリミティブ クラスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4902a-408">The array syntax supports primitive data types and classes.</span></span>| <span data-ttu-id="4902a-409">X++ では、配列のオブジェクトに `Array` 配列を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-409">In X++ you can use the `Array` Array for an array of objects.</span></span>|
| <span data-ttu-id="4902a-410">申告</span><span class="sxs-lookup"><span data-stu-id="4902a-410">Declaration</span></span>| <span data-ttu-id="4902a-411">X++ は一次元配列に制限されます (myStrings[8])。</span><span class="sxs-lookup"><span data-stu-id="4902a-411">X++ is limited to single dimension arrays (myStrings[8]).</span></span>| <span data-ttu-id="4902a-412">C# は多次元配列 (myStrings[8,3]) およびジャグ配列 (myStrings[8][3]) のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="4902a-412">C# adds support for multi-dimensional arrays (myStrings[8,3]) and for jagged arrays (myStrings[8][3]).</span></span>| <span data-ttu-id="4902a-413">X++ では、配列の配列を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-413">In X++ you cannot have an array of arrays.</span></span> <span data-ttu-id="4902a-414">ただし、大規模な配列が消費できる有効なメモリの量を制限する高度な構文があり、それは C#: int intArray[1024,16]; で多次元構文のように見えます。</span><span class="sxs-lookup"><span data-stu-id="4902a-414">However, there is advanced syntax for limiting the amount of active memory that a large array can consume, which looks like the multi-dimensional syntax in C#: int intArray[1024,16];.</span></span> <span data-ttu-id="4902a-415">詳細については、「ベスト プラクティス パフォーマンスの最適化: ディスクへの配列スワッピング」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-415">For more information, see Best Practice Performance Optimizations: Swapping Arrays to Disk.</span></span>|
| <span data-ttu-id="4902a-416">申告</span><span class="sxs-lookup"><span data-stu-id="4902a-416">Declaration</span></span>| <span data-ttu-id="4902a-417">X++ では、配列は特別なコンストラクトですが、オブジェクトではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-417">In X++ an array is a special construct but it is not an object.</span></span>| <span data-ttu-id="4902a-418">C# では、すべての配列が構文の違いに関係なくオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="4902a-418">In C# all arrays are objects regardless of syntax variations.</span></span>| <span data-ttu-id="4902a-419">X++ には配列クラスがありますが、その基本的なメカニズムは [] 構文を使用して作成された配列とは異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-419">X++ does have an Array class, but its underlying mechanism differs from arrays created by using the [] syntax.</span></span> <span data-ttu-id="4902a-420">C# では、すべての配列が `System.Array` クラスの [] 構文がコード内で使用されているかに関係なく、同じ基本的なメカニズムを使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-420">In C# all arrays use the same underlying mechanism, regardless of whether [] syntax of the `System.Array` class is used in your code.</span></span>|
| <span data-ttu-id="4902a-421">期間</span><span class="sxs-lookup"><span data-stu-id="4902a-421">Length</span></span>| <span data-ttu-id="4902a-422">X++ では、静的サイズの配列の長さは宣言構文で決定されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-422">In X++ the length of a static sized array is determined in the declaration syntax.</span></span>| <span data-ttu-id="4902a-423">C# では、配列のサイズは配列オブジェクトが構築されたときに決定されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-423">In C# the size of an array is determined when the array object is constructed.</span></span>| <span data-ttu-id="4902a-424">X++ で [] 宣言構文を使用するときは、配列に値を割り当てるとき、その前にこれ以上の準備は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-424">When you use the [] declaration syntax in X++, no more preparation is needed before you assign values to the array.</span></span> <br><span data-ttu-id="4902a-425">C# では、配列を宣言して作成してから代入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-425">In C# you must declare and then construct the array before assigning to it.</span></span>|
| <span data-ttu-id="4902a-426">期間</span><span class="sxs-lookup"><span data-stu-id="4902a-426">Length</span></span>| <span data-ttu-id="4902a-427">X++ 配列は、開始した後でも増加できる動的長さを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-427">An X++ array can have a dynamic length that can be increased even after population has begun.</span></span> <span data-ttu-id="4902a-428">これは配列が [] 内に数字なしで宣言されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-428">This applies only when the array is declared without a number inside the [].</span></span> <span data-ttu-id="4902a-429">動的配列の長さが何回も増加した場合、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-429">Performance might be slowed if the length of the dynamic array is increased many times.</span></span>| <span data-ttu-id="4902a-430">C# では、長さの設定後に配列の長さを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-430">In C# the length of an array cannot be changed after the length is set.</span></span>| <span data-ttu-id="4902a-431">X++ コードの次のフラグメントでは、`myInts` 配列のみが動的にサイズを大きくできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-431">In the following fragment of X++ code, only the `myInts` array is dynamic and can increase in size.</span></span> <br>`int myInts[];` <br>`int myBools[5];` <br>`myInts[2] = 12;` <br>`myInts[3] = 13;` <br>`myBools[6] = 26; //Error`|
| <span data-ttu-id="4902a-432">期間</span><span class="sxs-lookup"><span data-stu-id="4902a-432">Length</span></span>| <span data-ttu-id="4902a-433">`dimOf` 機能を使用することにより、一部の配列の長さを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-433">You can get the length of some arrays by using the `dimOf` function.</span></span>| <span data-ttu-id="4902a-434">C# の配列は `Length` プロパティを持つオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="4902a-434">C# arrays are objects that have a `Length` property.</span></span>| <span data-ttu-id="4902a-435">コメントはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-435">No comments.</span></span>|
| <span data-ttu-id="4902a-436">インデックスの作成中</span><span class="sxs-lookup"><span data-stu-id="4902a-436">Indexing</span></span>| <span data-ttu-id="4902a-437">配列インデックスは 1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="4902a-437">Array indexing is 1 based.</span></span>| <span data-ttu-id="4902a-438">配列インデックスは 0 ベースです。</span><span class="sxs-lookup"><span data-stu-id="4902a-438">Array indexing is 0 based.</span></span>
| <span data-ttu-id="4902a-439">mtIntArray[0] は X++ ではエラーとなります。</span><span class="sxs-lookup"><span data-stu-id="4902a-439">mtIntArray[0] would cause an error in X++.</span></span>|
| <span data-ttu-id="4902a-440">定数</span><span class="sxs-lookup"><span data-stu-id="4902a-440">Constant</span></span>| <span data-ttu-id="4902a-441">X++ で、定数値は <strong>#define</strong> プリコンパイラ ディレクティブを使用することで最適に実現されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-441">In X++ a constant value is best achieved by using the <strong>#define</strong> precompiler directive.</span></span>| <span data-ttu-id="4902a-442">C# では、キーワード <strong>const</strong> を使用して変数の宣言を修飾して定数値を実現できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-442">In C# you can decorate your variable declaration with the keyword <strong>const</strong>, to achieve a constant value.</span></span>| <span data-ttu-id="4902a-443">X++ には <strong>const</strong> キーワードがありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-443">X++ has no <strong>const</strong> keyword.</span></span> <span data-ttu-id="4902a-444">C# は、#define プリコンパイラ ディレクティブによって作成される変数に値を割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="4902a-444">C# cannot assign values to variables that are created by its #define precompiler directive.</span></span>|

### <a name="x-and-c-samples"></a><span data-ttu-id="4902a-445">X++ および C\# のサンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-445">X++ and C\# Samples</span></span>

<span data-ttu-id="4902a-446">次のコード例は、プリミティブ データ型の配列の処理方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-446">The following code samples show how arrays of primitive data types are handled.</span></span> <span data-ttu-id="4902a-447">最初のサンプルは X++ で、2 番目のサンプルは C\# にあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-447">The first sample is in X++, and the second sample is in C\#.</span></span> <span data-ttu-id="4902a-448">両方のサンプルで同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="4902a-448">Both samples achieve the same results.</span></span>

#### <a name="x-sample"></a><span data-ttu-id="4902a-449">X++ サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-449">X++ Sample</span></span>

<pre>
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
</pre>

##### <a name="output"></a><span data-ttu-id="4902a-450">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-450">Output</span></span>

<span data-ttu-id="4902a-451">情報ログへの出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-451">The output to the Infolog is as follows:</span></span>
<pre>
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
</pre>

#### <a name="c-sample"></a><span data-ttu-id="4902a-452">C\# サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-452">C\# Sample</span></span>

<span data-ttu-id="4902a-453">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-453">C#</span></span>

    using System;
    public class Pgm_CSharp
    {
        static public void Main( string[] args )
        {
            new Pgm_CSharp().Rs005a_CSharp_ArraySimple();
        }
        private void Rs005a_CSharp_ArraySimple()
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
                Console.WriteLine( xx.ToString()
                    + " , [" + sSports[xx] + "]" );
            }
            Console.WriteLine("-------- YEARS --------");
            // In C# you must construct the array before assigning to it.
            years = new int[10];
            years[ 4] = 2008;
            years[10 - 1] = 1930;
            for (xx=0; xx < 10; xx++)
            {
                Console.WriteLine( xx.ToString()
                    + " , [" + years[xx].ToString() + "]" );
            }
        }
    } // EOClass

##### <a name="output"></a><span data-ttu-id="4902a-454">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-454">Output</span></span>

<span data-ttu-id="4902a-455">C# プログラムからコマンド ライン コンソールへの出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-455">The output from the C# program to the command line console is as follows:</span></span>
<pre>
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
</pre>

## <a name="additional-array-like-x-features"></a><span data-ttu-id="4902a-456">追加の配列のような X++ 機能</span><span class="sxs-lookup"><span data-stu-id="4902a-456">Additional array-like X++ features</span></span>

<span data-ttu-id="4902a-457">**コンテナー**は、X++ で利用できる特別なデータ型です。</span><span class="sxs-lookup"><span data-stu-id="4902a-457">The **container** is a special data type that is available in X++.</span></span> <span data-ttu-id="4902a-458">配列と類似したもの、または `List` コレクションと類似したものとみなすことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-458">It can be considered as similar to an array, or similar to a `List` collection.</span></span>

## <a name="comparison-collections"></a><span data-ttu-id="4902a-459">比較: コレクション</span><span class="sxs-lookup"><span data-stu-id="4902a-459">Comparison: Collections</span></span>
<span data-ttu-id="4902a-460">Finance and Operations は X++ `List` コレクション クラスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-460">Finance and Operations provides the X++ `List` collection class.</span></span> <span data-ttu-id="4902a-461">C# で使用されている .NET Framework には、`System.Collections.Generic.List` と似た名前のクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-461">The .NET Framework that is used in C# has a similar class named `System.Collections.Generic.List`.</span></span>

### <a name="comparing-the-use-of-the-list-classes"></a><span data-ttu-id="4902a-462">リスト クラスの使用の比較</span><span class="sxs-lookup"><span data-stu-id="4902a-462">Comparing the Use of the List Classes</span></span>

<span data-ttu-id="4902a-463">次のテーブルは、X++ `List` クラスのメソッドと .NET Framework および C\# の `System.Collections.Generic.List` のメソッドを比較しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-463">The following table compares methods on the X++ `List` class to the methods on `System.Collections.Generic.List` from the .NET Framework and C\#.</span></span>

| <span data-ttu-id="4902a-464">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-464">Feature</span></span> | <span data-ttu-id="4902a-465">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-465">X++</span></span> | <span data-ttu-id="4902a-466">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-466">C#</span></span> | <span data-ttu-id="4902a-467">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-467">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-468">コレクションの宣言</span><span class="sxs-lookup"><span data-stu-id="4902a-468">Declaration of collection</span></span>| `List myList;`| `List<string> myList;`| <span data-ttu-id="4902a-469">X++ 宣言には、格納する要素のタイプは含まれません。</span><span class="sxs-lookup"><span data-stu-id="4902a-469">The X++ declaration does not include the type of elements to be stored.</span></span>|
| <span data-ttu-id="4902a-470">反復子の宣言</span><span class="sxs-lookup"><span data-stu-id="4902a-470">Declaration of iterator</span></span>|`ListIterator iter`<br>`ListEnumerator enumer;`| <span data-ttu-id="4902a-471">IEnumerator&lt;文字列&gt; iter;</span><span class="sxs-lookup"><span data-stu-id="4902a-471">IEnumerator&lt;string&gt; iter;</span></span>| <span data-ttu-id="4902a-472">X++ では、`ListIterator` オブジェクトに `List` の項目を `insert` および `delete` できるメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-472">In X++ the `ListIterator` object has methods that can `insert` and `delete` items from the `List`.</span></span> <span data-ttu-id="4902a-473">X++ `ListEnumerator` は、`List` の内容を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-473">The X++ `ListEnumerator` cannot modify the contents of the `List`.</span></span> <span data-ttu-id="4902a-474">X++ では、`ListEnumerator` オブジェクトは常に `List` と同じ層で作成されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-474">In X++ the `ListEnumerator` object is always created on the same tier as the `List`.</span></span> <span data-ttu-id="4902a-475">これは、必ずしも `ListIterator` に当てはまるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-475">This is not always true for `ListIterator`.</span></span>|
| <span data-ttu-id="4902a-476">反復子の取得</span><span class="sxs-lookup"><span data-stu-id="4902a-476">Obtaining an iterator</span></span>|`new ListIterator (myList)`<br>`myList.getEnumerator()`| `myList.GetEnumerator()`| <span data-ttu-id="4902a-477">X++ と C# の両方では、リスト オブジェクトに、関連付けられている列挙子の getter メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-477">In both X++ and C#, the List object has a getter method for an associated enumerator.</span></span>|
| <span data-ttu-id="4902a-478">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="4902a-478">Constructor</span></span>| `new List(Types::String)`| `new List<string>()`|<span data-ttu-id="4902a-479">`List` クラス内に格納するオブジェクトのタイプに関する情報は、X++ と C# の両方でコントラクターに付与されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-479">Information about the type of objects to be stored inside the `List` classes is given to the constructor in both X++ and C#.</span></span>|
| <span data-ttu-id="4902a-480">データの更新</span><span class="sxs-lookup"><span data-stu-id="4902a-480">Updating data</span></span>|<span data-ttu-id="4902a-481">列挙子 – `List` 内の品目が追加または削除された場合、列挙子は無効になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-481">Enumerator – the enumerator becomes invalid if any items in the `List` are added or removed.</span></span><br><span data-ttu-id="4902a-482">反復子 – 反復子には `List` の項目を挿入および削除するメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-482">Iterator – the iterator has methods that insert and delete items from the `List`.</span></span> <span data-ttu-id="4902a-483">反復子は有効なままです。</span><span class="sxs-lookup"><span data-stu-id="4902a-483">The iterator remains valid.</span></span>| <span data-ttu-id="4902a-484">列挙子 – `List` 内の品目が追加または削除された場合、列挙子は無効になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-484">Enumerator – the enumerator becomes invalid if any items in the `List` are added or removed.</span></span>| <span data-ttu-id="4902a-485">X++ と C# の両方で、項目が `List` から追加または削除された後、列挙子は無効になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-485">Enumerators become invalid after items are added or deleted from the `List`, in both X++ and C#.</span></span>|
| <span data-ttu-id="4902a-486">データの更新</span><span class="sxs-lookup"><span data-stu-id="4902a-486">Updating data</span></span>| <span data-ttu-id="4902a-487">X++ では、`List` クラスにリストの開始または最後に項目を追加するメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-487">In X++ the `List` class has methods for adding items at the start or end of the list.</span></span>| <span data-ttu-id="4902a-488">C# では、`List` クラスにリスト内の任意の位置にメンバーを追加するためのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-488">In C# the `List` class has methods for adding members at any position in the list.</span></span> <span data-ttu-id="4902a-489">また、任意の場所から項目を削除するメソッドもあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-489">It also has methods for removing items from any position.</span></span>| <span data-ttu-id="4902a-490">X++ では、反復子でのみ項目を `List` から削除できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-490">In X++ items can be removed from the `List` only by an iterator.</span></span>|

### <a name="example-1-declaration-of-a-list"></a><span data-ttu-id="4902a-491">例 1: リストの宣言</span><span class="sxs-lookup"><span data-stu-id="4902a-491">Example 1: Declaration of a List</span></span>

<span data-ttu-id="4902a-492">次のテーブルは、`List` コレクションを宣言する X++ および C# のコード例を示しています.</span><span class="sxs-lookup"><span data-stu-id="4902a-492">The following table displays code examples in X++ and C# that declare `List` collections.</span></span>

    // X++
    List listStrings ,list2 ,listMerged;
    ListIterator literator;

    // C#
    using System;
    using SysCollGen = System.Collections.Generic;
    SysCollGen.List<string> listStrings ,list2 ,listMerged; SysCollGen.IEnumerator<string> literator;

### <a name="example-2-construction-of-a-list"></a><span data-ttu-id="4902a-493">例 2: リストの作成</span><span class="sxs-lookup"><span data-stu-id="4902a-493">Example 2: Construction of a List</span></span>

<span data-ttu-id="4902a-494">どちらの言語でも、構築の時点でコレクションが格納する項目のタイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-494">In both languages, the type of items that the collection stores must be specified at the time of construction.</span></span> <span data-ttu-id="4902a-495">クラス タイプでは、X++ はタイプがクラス (Types::Class) であるかどうかよりも具体的でないものを取得します。</span><span class="sxs-lookup"><span data-stu-id="4902a-495">For class types, X++ can get no more specific than whether the type is a class (Types::Class).</span></span> <span data-ttu-id="4902a-496">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-496">Code examples are in the following table.</span></span>

    // X++
    listStrings = new List( Types::String );

    // C#
    listStrings = new SysCollGen.List<string>;

### <a name="example-3-add-items-to-a-list"></a><span data-ttu-id="4902a-497">例 3: リストに品目を追加</span><span class="sxs-lookup"><span data-stu-id="4902a-497">Example 3: Add Items to a List</span></span>

<span data-ttu-id="4902a-498">X++ と C# 両方では、コレクションはコレクションの末尾に項目を追加するメソッドと、最初に項目を挿入するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-498">In both X++ and C#, the collection provides a method for appending an item to the end of the collection, and for inserting an item the start.</span></span> <span data-ttu-id="4902a-499">C# では、コレクションは指数値に基づいてコレクション内の任意の時点で挿入するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-499">In C# the collection provides a method for inserting at any point in the collection based on an index value.</span></span> <span data-ttu-id="4902a-500">X++ では、コレクションの反復子によって現在の位置に項目を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-500">In X++ a collection iterator can insert an item at its current position.</span></span> <span data-ttu-id="4902a-501">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-501">Code examples are in the following table.</span></span>

    // X++
    listStrings.addEnd ("String\_BB."); 
    listStrings.addStart ("String\_AA.");
    // Iterator performs a midpoint insert at current position. 
    listIterator.insert ("dog");

    // C#
    listStrings.Add ("String\_BB."); 
    listStrings.Insert (0 ,"String\_AA.");
    // Index 7 determines the insertion point.
    listStrings.Insert (7 ,"dog");

### <a name="example-4-iterate-through-a-list"></a><span data-ttu-id="4902a-502">例 4: リストを繰り返す</span><span class="sxs-lookup"><span data-stu-id="4902a-502">Example 4: Iterate Through a List</span></span>

<span data-ttu-id="4902a-503">X++ と C\# には反復子のクラスがあり、コレクション内の項目をステップ実行するのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-503">Both X++ and C\# have iterator classes that you can use to step through the items in a collection.</span></span> <span data-ttu-id="4902a-504">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-504">Code examples are in the following table.</span></span>

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

    // C#
    literator = listStrings .GetEnumerator(); 
    // Now enumerator points before the first item, not at the first item.

    // The MoveNext method both advances the item pointer, and 
    // answers whether the pointer is pointing at an item. 
    while (literator.MoveNext()) 
    { 
        Console.WriteLine (literator.Current); 
    }


### <a name="example-4b-foreach-in-c"></a><span data-ttu-id="4902a-505">例 4b: C\# の foreach</span><span class="sxs-lookup"><span data-stu-id="4902a-505">Example 4b: foreach in C\#</span></span>

<span data-ttu-id="4902a-506">C\# では、よく **foreach** キーワードを使用して、一覧の反復のタスクを簡略化します。</span><span class="sxs-lookup"><span data-stu-id="4902a-506">In C\# the **foreach** keyword is often used to simplify the task of iterating through a list.</span></span> <span data-ttu-id="4902a-507">次のコード例は、以前の C\# の例と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="4902a-507">The following code example behaves the same as the previous C\# example.</span></span> 

    foreach (string currentString in listStrings)
    { 
        Console.WriteLine(currentString);
    }

###  <a name="example-5-delete-the-second-item"></a><span data-ttu-id="4902a-508">例 5: 2 番目の項目を削除</span><span class="sxs-lookup"><span data-stu-id="4902a-508">Example 5: Delete the Second Item</span></span>

<span data-ttu-id="4902a-509">次のテーブルに、コレクションから 2 番目のアイテムを削除するコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-509">The following table contains code examples that delete the second item from the collection.</span></span> <span data-ttu-id="4902a-510">X++ では、これに反復子が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-510">In X++ this requires an iterator.</span></span> <span data-ttu-id="4902a-511">C\# では、コレクション自体が項目を削除するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-511">In C\# the collection itself provides the method for removing an item.</span></span>

    // X++
    literator.begin(); 
    literator.next(); 
    literator.delete();

    // C#
    listStrings.RemoveAt(1);

###  <a name="example-6-combine-two-collections"></a><span data-ttu-id="4902a-512">例 6: 2 つのコレクションを結合</span><span class="sxs-lookup"><span data-stu-id="4902a-512">Example 6: Combine Two Collections</span></span>

<span data-ttu-id="4902a-513">次のテーブルには、2 つのコレクションの内容を 1 つにまとめたコード例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4902a-513">The following table contains code examples that combine the contents of two collections into one.</span></span>

    // X++
    listStrings = List::merge(listStrings ,listStr3);
    // Or use the .appendList method:
    listStrings.appendList (listStr3);

    // C#
    listStrings.InsertRange(listStrings.Count ,listStr3);

## <a name="comparison-collections-of-keys-with-values"></a><span data-ttu-id="4902a-514">比較: 値を持つキーのコレクション</span><span class="sxs-lookup"><span data-stu-id="4902a-514">Comparison: Collections of keys with values</span></span>

<span data-ttu-id="4902a-515">Finance and Operations は `Map` コレクション クラスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-515">Finance and Operations provides the `Map` collection class.</span></span> <span data-ttu-id="4902a-516">`Map` コレクションには、値のペア (キー値とデータ値の組み合わせ) が保持されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-516">The `Map` collection holds pairs of values, the key value plus a data value.</span></span> <span data-ttu-id="4902a-517">これは、`System.Collections.Generic.Dictionary` という名前の .NET Framework クラスに似ています。</span><span class="sxs-lookup"><span data-stu-id="4902a-517">This resembles the .NET Framework class named `System.Collections.Generic.Dictionary`.</span></span>

### <a name="similarities"></a><span data-ttu-id="4902a-518">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-518">Similarities</span></span>

<span data-ttu-id="4902a-519">次のリストは、キーと値のペアを格納するコレクションに関する X++ と C\# の類似点について説明します。</span><span class="sxs-lookup"><span data-stu-id="4902a-519">The following list describes similarities between X++ and C\# regarding their collections that store key-value pairs:</span></span>
-   <span data-ttu-id="4902a-520">どちらも重複するキーを防止します。</span><span class="sxs-lookup"><span data-stu-id="4902a-520">Both prevent duplicate keys.</span></span>
-   <span data-ttu-id="4902a-521">どちらも列挙子 (または反復子) を使用して項目をループします。</span><span class="sxs-lookup"><span data-stu-id="4902a-521">Both use an enumerator (or iterator) to loop through the items.</span></span>
-   <span data-ttu-id="4902a-522">両方のキー値コレクション オブジェクトは、キーと値として格納されているタイプの指定で作成されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-522">Both key-value collection objects are constructed with designations of the types that are stored as key and value.</span></span>
-   <span data-ttu-id="4902a-523">どちらもクラス オブジェクトを格納でき、**int** のようなプリミティブの格納に限定されません。</span><span class="sxs-lookup"><span data-stu-id="4902a-523">Both can store class objects, and are not limited to storing primitives like **int**.</span></span>

### <a name="differences"></a><span data-ttu-id="4902a-524">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-524">Differences</span></span>

<span data-ttu-id="4902a-525">次のテーブルは、キーと値のペアを格納するコレクション クラスに関する X++ と C\# の違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-525">The following table describes differences between X++ and C\# regarding their collections classes that store key-value pairs:</span></span>

| <span data-ttu-id="4902a-526">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-526">Feature</span></span>        | <span data-ttu-id="4902a-527">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-527">X++</span></span>     | <span data-ttu-id="4902a-528">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-528">C#</span></span>  | <span data-ttu-id="4902a-529">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-529">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-530">キーの重複</span><span class="sxs-lookup"><span data-stu-id="4902a-530">Duplicate keys</span></span> | <span data-ttu-id="4902a-531">X++ では、`Map` クラスが `insert` メソッドに対する呼び出しを、キーに関連付けられている値のみを更新する操作として暗黙的に扱うことにより、重複キーを防止します。</span><span class="sxs-lookup"><span data-stu-id="4902a-531">In X++ the `Map` class prevents duplicate keys by implicitly treating your call to its `insert` method as an operation to update only the value associated with the key.</span></span> | <span data-ttu-id="4902a-532">C\# では、重複キーを追加しようとすると `Dictionary` クラスが例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="4902a-532">In C\# the `Dictionary` class throws an exception when you try to add a duplicate key.</span></span> | <span data-ttu-id="4902a-533">異なる技術ではあるが、両方の言語で重複するキーが防止されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-533">Duplicate keys are prevented in both languages, although by different techniques.</span></span>               |
| <span data-ttu-id="4902a-534">品目の削除</span><span class="sxs-lookup"><span data-stu-id="4902a-534">Delete items</span></span>   | <span data-ttu-id="4902a-535">X++ では、反復子オブジェクトで `delete` メソッドを使用して、不要なキーと値のペアを `Map` から削除します。</span><span class="sxs-lookup"><span data-stu-id="4902a-535">In X++ the `delete` method on an iterator object is used to remove an unwanted key-value pair from a `Map`.</span></span>    | <span data-ttu-id="4902a-536">C\# では、`Dictionary` クラスに `remove` メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-536">In C\# the `Dictionary` class has a `remove` method.</span></span>      | <span data-ttu-id="4902a-537">どちらの言語でも、列挙子は列挙子の有効期間中にコレクション項目数が変更された場合は無効になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-537">In both languages, an enumerator is made invalid if the collection item count is modified during the life of the enumerator.</span></span> |

### <a name="example-1-declaration-of-a-key-value-collection"></a><span data-ttu-id="4902a-538">例 1: キー値のコレクションの宣言</span><span class="sxs-lookup"><span data-stu-id="4902a-538">Example 1: Declaration of a Key-Value Collection</span></span>

<span data-ttu-id="4902a-539">どちらの言語でも、キー値コレクションが格納する項目のタイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-539">In both languages, the type of items that the key-value collection stores must be specified.</span></span> <span data-ttu-id="4902a-540">X++ では、型は構築時に指定されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-540">In X++ the type is specified at time of construction.</span></span> <span data-ttu-id="4902a-541">C\# では、宣言時と構築時の両方で型が指定されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-541">In C\# the type is specified at both the time of declaration and the time of construction.</span></span> <span data-ttu-id="4902a-542">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-542">Code examples are in the following table.</span></span>

    // X++
    Map mapKeyValue;
    MapEnumerator enumer;
    MapIterator mapIter;

    // C#
    SysCollGen.Dictionary<int,string> dictKeyValue;
    SysCollGen.IEnumerator<SysCollGen.KeyValuePair<int,string>> enumer;
    SysCollGen.KeyValuePair<int,string> kvpCurrentKeyValuePair;

### <a name="example-2-construction-of-the-collection"></a><span data-ttu-id="4902a-543">例 2: コレクションの作成</span><span class="sxs-lookup"><span data-stu-id="4902a-543">Example 2: Construction of the Collection</span></span>

<span data-ttu-id="4902a-544">どちらの言語でも、構築中にキー値コレクションが格納する項目のタイプが指定されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-544">In both languages, the type of items that the key-value collection stores specified during construction.</span></span> <span data-ttu-id="4902a-545">クラス タイプでは、X++ はタイプがクラス (Types::Class) であるかどうかよりも具体的でないものを取得します。</span><span class="sxs-lookup"><span data-stu-id="4902a-545">For class types, X++ can get no more specific than whether the type is a class (Types::Class).</span></span> <span data-ttu-id="4902a-546">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-546">Code examples are in the following table.</span></span>

    // X++
    mapKeyValue = new Map(Types::Integer, Types::String);

    // C#
    dictKeyValue = new SysCollGen.Dictionary<int,string>();

### <a name="example-3-add-an-item-to-the-collection"></a><span data-ttu-id="4902a-547">例 3: 品目をコレクションに追加</span><span class="sxs-lookup"><span data-stu-id="4902a-547">Example 3: Add an Item to the Collection</span></span>

<span data-ttu-id="4902a-548">X++ と C\# では、キー値コレクションにアイテムを追加する方法にほとんど違いはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-548">There is almost no difference in how an item is added to a key-value collection, in X++ and C\#.</span></span> <span data-ttu-id="4902a-549">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-549">Code examples are in the following table.</span></span>

    // X++
    mapKeyValue.insert(xx ,int2str(xx) + “_Value”);

    // C#
    dictKeyValue.Add(xx ,xx.ToString() + “_Value”);

### <a name="example-4-iterate-through-a-key-value-collection"></a><span data-ttu-id="4902a-550">例 4: キー値のコレクションを反復</span><span class="sxs-lookup"><span data-stu-id="4902a-550">Example 4: Iterate Through a Key-Value Collection</span></span>

<span data-ttu-id="4902a-551">列挙子は、X++ と C\# の両方のキー値コレクションをループするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-551">Enumerators are used to loop through the key-value collections in both X++ and C\#.</span></span> <span data-ttu-id="4902a-552">コードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-552">Code examples are in the following table.</span></span>

    // X++ 
    enumer = mapKeyValue.getEnumerator();
    while (enumer.moveNext())
    {
        iCurrentKey = enumer.currentKey();
        sCurrentValue = enumer.currentValue();
        // Display key and value here.
    }

    // C#
    enumer = dictKeyValue.GetEnumerator();
    while (enumer.MoveNext())
    {
        kvpCurrentKeyValuePair = enumer.Current;
        // Display .Key and .Value properties=
        // of kvpCurrentKeyValuePair here.
    }

### <a name="example-5-update-the-value-associated-with-a-key"></a><span data-ttu-id="4902a-553">例 5: キーに関連付けられている値を更新</span><span class="sxs-lookup"><span data-stu-id="4902a-553">Example 5: Update the Value Associated with a Key</span></span>

<span data-ttu-id="4902a-554">構文は、指定されたキーに関連付けられた値を更新するために 2 つの言語で全く異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-554">The syntax is very different between the two languages for an update of the value associated to a given key.</span></span> <span data-ttu-id="4902a-555">キー 102 のコードの例を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-555">Code examples for the key 102 are in the following table.</span></span>

    // X++
    mapKeyValue.insert(
        102 ,
        ”.insert(), Re-inserted” + ” key 102 with a different value.”);

    // C#
    dictKeyValue[102] = 
        “The semi-hidden .item property” 
        + ” in C#, Updated the value for key 102.”;

### <a name="example-6-delete-one-item"></a><span data-ttu-id="4902a-556">例 6: 1つの品目を削除</span><span class="sxs-lookup"><span data-stu-id="4902a-556">Example 6: Delete One Item</span></span>

<span data-ttu-id="4902a-557">構文は、2 つの言語間でコレクション メンバーを反復しながら、コレクションから 1 つのキーと値のペアを削除する方法が全く異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-557">The syntax is very different between the two languages to delete one key-value pair from a collection, while iterating through the collection members.</span></span> <span data-ttu-id="4902a-558">キー 102 のコードの例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-558">Code examples for the key 102 are shown below.</span></span>

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

    // C#
    dictKeyValue.Remove(104);


## <a name="comparison-exceptions"></a><span data-ttu-id="4902a-559">比較: 例外</span><span class="sxs-lookup"><span data-stu-id="4902a-559">Comparison: Exceptions</span></span>
<span data-ttu-id="4902a-560">いくつかの類似点がありますが、X++ と C\# の間の例外関連の動作を比較すると、多くの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-560">There are some similarities but many differences when we compare exception related behavior between X++ and C\#.</span></span> <span data-ttu-id="4902a-561">**try**、**catch**、**throw** キーワードは、X++ と C# で同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="4902a-561">The **try**, **catch**, and **throw** keywords behave the same in X++ and C#.</span></span> <span data-ttu-id="4902a-562">ただし、スローされキャッチされる例外のタイプは 2 つの言語で異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-562">But the types of exceptions thrown and caught are different for the two languages.</span></span>

### <a name="similarities"></a><span data-ttu-id="4902a-563">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-563">Similarities</span></span>

<span data-ttu-id="4902a-564">例外機能に関する X++ と C\# の類似点には、次が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4902a-564">Similarities between X++ and C\# regarding their exception features include the following:</span></span>
-   <span data-ttu-id="4902a-565">どちらの言語も同じ **try** キーワードを持っています。</span><span class="sxs-lookup"><span data-stu-id="4902a-565">Both languages have the same **try** keyword.</span></span>
-   <span data-ttu-id="4902a-566">どちらも同じ **catch** キーワードを持っています。</span><span class="sxs-lookup"><span data-stu-id="4902a-566">Both have the same **catch** keyword.</span></span>
-   <span data-ttu-id="4902a-567">両方とも特定の例外を指定しない **catch** ステートメントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4902a-567">Both enable for a **catch** statement that does not specify any particular exception.</span></span> <span data-ttu-id="4902a-568">このような **catch** ステートメントは、それに到達するすべての例外を検出します。</span><span class="sxs-lookup"><span data-stu-id="4902a-568">Such a **catch** statement catches all exceptions that reach it.</span></span>
-   <span data-ttu-id="4902a-569">どちらも同じ **throw** キーワードを持っています。</span><span class="sxs-lookup"><span data-stu-id="4902a-569">Both have the same **throw** keyword.</span></span>

### <a name="differences"></a><span data-ttu-id="4902a-570">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-570">Differences</span></span>

<span data-ttu-id="4902a-571">X++ と C\# 間の例外関連の違いは、次のテーブルで説明します。</span><span class="sxs-lookup"><span data-stu-id="4902a-571">Exception-related differences between X++ and C\# are described in the following table.</span></span>

| <span data-ttu-id="4902a-572">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-572">Feature</span></span> | <span data-ttu-id="4902a-573">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-573">X++</span></span> | <span data-ttu-id="4902a-574">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-574">C#</span></span> | <span data-ttu-id="4902a-575">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-575">Comments</span></span> |
|---|---|---|---|
| <span data-ttu-id="4902a-576"><strong>再試行</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-576"><strong>retry</strong></span></span>| <span data-ttu-id="4902a-577">関連付けられた <strong>try</strong> ブロックの最初の命令にジャンプします。</span><span class="sxs-lookup"><span data-stu-id="4902a-577">Jumps to the first instruction in the associated <strong>try</strong> block.</span></span> <span data-ttu-id="4902a-578">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-578">For more information, see Exception Handling with try and catch Keywords.</span></span>| <span data-ttu-id="4902a-579"><strong>再試行</strong> キーワードの機能は C# コードでは真似できますが、対応するキーワードはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-579">The functionality of the <strong>retry</strong> keyword can be mimicked in C# code, but there is no corresponding keyword.</span></span>| <span data-ttu-id="4902a-580">X++ のみ、<strong>再試行</strong>キーワードがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-580">Only X++ has a <strong>retry</strong> keyword.</span></span> <span data-ttu-id="4902a-581">C# には対応がありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-581">C# has no counterpart.</span></span> <span data-ttu-id="4902a-582">詳細については、X++、C# の比較: 例外後の再試行の自動化を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-582">For more information, see X++, C# Comparison: Automated Retry After an Exception.</span></span>|
| <span data-ttu-id="4902a-583"><strong>最終的に</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-583"><strong>finally</strong></span></span>| <span data-ttu-id="4902a-584">`finally` キーワードは、`try` および `catch` キーワードの後に使用することがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4902a-584">The `finally` keyword is supported to follow the `try` and `catch` keywords.</span></span>| <span data-ttu-id="4902a-585"><strong>finally</strong> キーワードは、<strong>try</strong> および <strong>catch</strong> ブロックに従うコードのブロックをマークします。</span><span class="sxs-lookup"><span data-stu-id="4902a-585">The <strong>finally</strong> keyword marks a block of code that follows the <strong>try</strong> and <strong>catch</strong> blocks.</span></span> <span data-ttu-id="4902a-586">例外がスローされたかキャッチされたかどうかに関係なく、確定が実行されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-586">The finally will be executed regardless of whether any exception is thrown or caught.</span></span>| <span data-ttu-id="4902a-587">セマンティクスは C# のセマンティクスと同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-587">The semantics are identical to the semantics in C#.</span></span>|
| <span data-ttu-id="4902a-588">特定の固有</span><span class="sxs-lookup"><span data-stu-id="4902a-588">Specific exceptions</span></span>| <span data-ttu-id="4902a-589">X++ では、例外は、**エラー**、**デッドロック**、または **CodeAccessSecurity** など `Exception` 列挙型の要素です。</span><span class="sxs-lookup"><span data-stu-id="4902a-589">In X++ an exception is an element of the `Exception` enum, such as **Error**, **Deadlock**, or **CodeAccessSecurity**.</span></span> <span data-ttu-id="4902a-590">別のものを含めることができる例外はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-590">No exception can contain another.</span></span>| <span data-ttu-id="4902a-591">C# では、例外は `System.Exception` 基本クラスまたは継承された任意のクラスのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="4902a-591">In C# an exception is an instance of the `System.Exception` base class, or any class that inherits from it.</span></span> <span data-ttu-id="4902a-592">スローされた例外の `InnerException` プロパティに例外を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-592">An exception can be contained in the `InnerException` property of the thrown exception.</span></span>| <span data-ttu-id="4902a-593">X++ では、スローされた各例外は Exception 列挙型の値です。</span><span class="sxs-lookup"><span data-stu-id="4902a-593">In X++ each thrown exception is a value of the Exception enum.</span></span> <span data-ttu-id="4902a-594">詳細については、「例外列挙」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-594">For more information, see Exception Enumeration.</span></span>|
| <span data-ttu-id="4902a-595">例外メッセージ</span><span class="sxs-lookup"><span data-stu-id="4902a-595">Exception message</span></span>| <span data-ttu-id="4902a-596">X++ では、例外が発生したときに作成されるメッセージは情報ログでのみ使用でき、そのメッセージは例外に直接関連付けられません。</span><span class="sxs-lookup"><span data-stu-id="4902a-596">In X++ the message that is created when an exception is raised is available only in the Infolog, and the message is not directly tied to the exception.</span></span>| <span data-ttu-id="4902a-597">C# では、メッセージは `System.Exception` オブジェクトの `Message` のメンバーです。</span><span class="sxs-lookup"><span data-stu-id="4902a-597">In C# the message is the `Message` member of the `System.Exception` object.</span></span>| <span data-ttu-id="4902a-598">X++ では、Global::error メソッドは情報ログで例外メッセージを表示するメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="4902a-598">In X++ the Global::error method is the mechanism that display exception messages in the Infolog.</span></span> <span data-ttu-id="4902a-599">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-599">For more information, see Exception Handling with try and catch Keywords.</span></span>|
| <span data-ttu-id="4902a-600">例外条件</span><span class="sxs-lookup"><span data-stu-id="4902a-600">Exception conditions</span></span>| <span data-ttu-id="4902a-601">X++ では、まだ何も代入されていないオブジェクト変数でインスタンス メソッドを呼び出すとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-601">In X++ an error occurs when you call an instance method on an object variable that has not yet had anything assigned to it.</span></span> <span data-ttu-id="4902a-602">ただし、このエラーと共に例外は発生しません。</span><span class="sxs-lookup"><span data-stu-id="4902a-602">However, no exception is raised along with this error.</span></span> <span data-ttu-id="4902a-603">したがって、割り当てられていない変数が `try` ブロックで誤用されても、`catch` ブロックは制御を獲得できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-603">Therefore no `catch` block can gain control even if the unassigned variable is misused in a `try` block.</span></span> <span data-ttu-id="4902a-604">次のコード例では、コード `box4.toString();` で発生したエラーにより、コントロールは任意の `catch` ブロックに移行しません。`DialogBox box4;` `try` { ` box4.toString();` ` info("toString did not error, but expected an error.");` } catch (Exception::Error) // これを検出する例外値はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-604">In the following code example, the error caused by the code `box4.toString();` does not cause control to transfer to any `catch` block: `DialogBox box4;` `try` { ` box4.toString();` ` info("toString did not error, but expected an error.");` } catch (Exception::Error) // No Exception value catches this.</span></span> <span data-ttu-id="4902a-605">{ ` info("Invalid use of box4 gave control to catch, unexpected.");` }</span><span class="sxs-lookup"><span data-stu-id="4902a-605">{ ` info("Invalid use of box4 gave control to catch, unexpected.");` }</span></span>| <span data-ttu-id="4902a-606">C# では、初期化されていない変数がオブジェクト参照として扱われる場合、`System.NullReferenceException` が発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-606">In C# a `System.NullReferenceException` is raised when an uninitialized variable is treated as an object reference.</span></span>
| <span data-ttu-id="4902a-607">例外を発生させる条件にはいくつかの相違点があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-607">There might be several other differences in the conditions that raise exceptions.</span></span>|
| <span data-ttu-id="4902a-608">SQL トランザクション</span><span class="sxs-lookup"><span data-stu-id="4902a-608">SQL transactions</span></span>| <span data-ttu-id="4902a-609">X++ で、SQL 例外が <strong>ttsBegin</strong> - <strong>ttsCommit</strong> トランザクションで発生する場合、そのトランザクション ブロック内の <strong>catch</strong> ステートメントは例外を処理できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-609">In X++ when an SQL exception occurs in a <strong>ttsBegin</strong> - <strong>ttsCommit</strong> transaction, no <strong>catch</strong> statement inside the transaction block can process the exception.</span></span>| <span data-ttu-id="4902a-610">C# では、SQL トランザクション内部の catch ブロックは例外を検出できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-610">In C# a catch block inside an SQL transaction can catch the exception.</span></span>| |

### <a name="examples"></a><span data-ttu-id="4902a-611">例</span><span class="sxs-lookup"><span data-stu-id="4902a-611">Examples</span></span>

<span data-ttu-id="4902a-612">次の X++ 機能が示されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-612">The following X++ features are demonstrated:</span></span>
-   <span data-ttu-id="4902a-613">**試行**キーワード。</span><span class="sxs-lookup"><span data-stu-id="4902a-613">**try** keyword.</span></span>
-   <span data-ttu-id="4902a-614">**catch** キーワード。</span><span class="sxs-lookup"><span data-stu-id="4902a-614">**catch** keyword.</span></span>
-   <span data-ttu-id="4902a-615">Exception::Error 例外が発生した後の動作。</span><span class="sxs-lookup"><span data-stu-id="4902a-615">The behavior after an Exception::Error exception occurs.</span></span>

#### <a name="x-example"></a><span data-ttu-id="4902a-616">X++ 例</span><span class="sxs-lookup"><span data-stu-id="4902a-616">X++ Example</span></span>

<pre>
// X++
static void JobRs008a_Exceptions(Args _args)
{
    str sStrings[4];
    int iIndex = 77;
    try
    {
        info("On purpose, this uses an invalid index for this array: "
            + sStrings[iIndex]);
        warning("This message does not appear in the Infolog,"
            + " it is unreached code.");
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
}</pre>

 
##### <a name="output"></a><span data-ttu-id="4902a-617">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-617">Output</span></span>

<span data-ttu-id="4902a-618">情報ログ ウィンドウからの出力を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-618">Here is the output from the Infolog window:</span></span>

<pre>Message (18:07:24)
Error executing code: Array index 77 is out of bounds.
Stack trace
(C)\Jobs\JobRs008a_Exceptions - line 8
In catch block for -- Exception::Error
End of program.
</pre>

#### <a name="c-sample"></a><span data-ttu-id="4902a-619">C# サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-619">C# Sample</span></span>

<span data-ttu-id="4902a-620">次の C\# プログラムは、以前の X++ プログラムを書き直したものです。</span><span class="sxs-lookup"><span data-stu-id="4902a-620">The following C\# program is a rewrite of the previous X++ program.</span></span>

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
                Console.WriteLine
                    ("On purpose, this uses an invalid index"
                    + " for this array: " + sStrings[77]);
                Console.Error.WriteLine
                    ("This message does not appear in the Infolog,"
                    + " it is unreached code.");
            }
            catch (NullReferenceException exc)
            {
                Console.WriteLine("(e1) In catch block for -- "
                    + exc.GetType().ToString() );
            }
            catch (IndexOutOfRangeException exc)
            {
                Console.WriteLine("(e2) In catch block for -- "
                    + exc.GetType().ToString() );
            }
            // In C#, System.Exception is the base of all
            // .NET Framework exception classes.
            // No as yet uncaught exception can get beyond
            // this next catch.
            catch (Exception exc)
            {
                Console.WriteLine
                    ("This last 'catch' is of the abstract"
                    + " base type Exception: "
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
                Console.WriteLine
                    ("'finally' is not an X++ keyword,"
                    + " although it is in C#.");
            }
            Console.WriteLine("End of program.");
        }
    } // EOClass


 
##### <a name="output"></a><span data-ttu-id="4902a-621">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-621">Output</span></span>

<span data-ttu-id="4902a-622">C\# コンソールへの実際の出力を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-622">Here is the actual output to the C\# console:</span></span>

<pre>

(e2) In catch block for -- System.IndexOutOfRangeException
'finally' is not an X++ keyword, although it is in C#.
End of program.
</pre>

## <a name="comparison-automated-retry-after-an-exception"></a><span data-ttu-id="4902a-623">比較: 例外後の自動再試行</span><span class="sxs-lookup"><span data-stu-id="4902a-623">Comparison: Automated Retry After an Exception</span></span>
<span data-ttu-id="4902a-624">場合によっては、実行時に発生する例外の原因を修正する catch ブロックでコードを記述できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-624">Sometimes you can write code in a catch block that fixes the cause of an exception that occurs during run time.</span></span> <span data-ttu-id="4902a-625">X++ には **catch** ブロック内でのみ使用することができる **retry** キーワードが用意されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-625">X++ provides a **retry** keyword that can be used only inside a **catch** block.</span></span> <span data-ttu-id="4902a-626">**retry** キーワードを使用すると、問題が **catch** ブロック内のコードにより修正されるとプログラムが **try** ブロックの先頭に戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-626">The **retry** keyword enables a program to jump back to the start of the **try** block after the problem has been corrected by code in the **catch** block.</span></span> <span data-ttu-id="4902a-627">C# には**再試行**キーワードがありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-627">C# does not have a **retry** keyword.</span></span> <span data-ttu-id="4902a-628">ただし、同等の動作を提供するよう C# コードを書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-628">However, C# code can be written to provide equivalent behavior.</span></span>

### <a name="code-samples-for-retry"></a><span data-ttu-id="4902a-629">再試行のためのコード サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-629">Code Samples for Retry</span></span>

<span data-ttu-id="4902a-630">次の X++ サンプル プログラムは、Exception::Error を発生させます。</span><span class="sxs-lookup"><span data-stu-id="4902a-630">The following X++ sample program causes an Exception::Error to be raised.</span></span> <span data-ttu-id="4902a-631">これは、最初に無効なインデックス値を使用して `sStrings` 配列から要素を読み取ろうとするときに発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-631">This occurs when it first tries to read an element from the `sStrings` array by using an invalid index value.</span></span> <span data-ttu-id="4902a-632">例外がキャッチされると、**catch** ブロック内で、実行時に是正措置が行われます。</span><span class="sxs-lookup"><span data-stu-id="4902a-632">When the exception is caught, corrective action is taken during run time inside the **catch** block.</span></span> <span data-ttu-id="4902a-633">その後再試行ステートメントは、**try** ブロックの最初のステートメントに戻ります。</span><span class="sxs-lookup"><span data-stu-id="4902a-633">The retry statement then jumps back to the first statement in the **try** block.</span></span> <span data-ttu-id="4902a-634">この 2 回目の繰り返しは、例外が発生することなく動作します。</span><span class="sxs-lookup"><span data-stu-id="4902a-634">This second iteration works without encountering any exception.</span></span>

<pre>
static void JobRs008b_ExceptionsAndRetry(Args _args)
{
    str sStrings[4];
    str sTemp;
    int iIndex = 0;
    ;
    sStrings[1] = "First array element.";
    try
    {
        print("At top of try block: " + int2str(iIndex));
        sTemp = sStrings[iIndex];
        print( "The array element is: " + sTemp );
    }
    catch (Exception::Error)
    {
        print("In catch of -- Exception::Error (will retry)."
            + " Entering catch.");
        ++iIndex;
        print("In catch of -- Exception::Error (will retry).
            + " Leaving catch.");
        // Here is the retry statement.
        retry;
    }
    print("End of X++ retry program.");
    pause;
}
</pre>

#### <a name="output"></a><span data-ttu-id="4902a-635">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-635">Output</span></span>

<span data-ttu-id="4902a-636">印刷ウィンドウへの出力を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-636">Here is the output to the Print window:</span></span>

<pre>
At top of try block: 0
In catch of -- Exception::Error (will retry). Entering catch.
In catch of -- Exception::Error (will retry). Leaving catch.
At top of try block: 1
The array element is: First array element.
End of X++ retry program.
</pre>

### <a name="c-sample"></a><span data-ttu-id="4902a-637">C# サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-637">C# Sample</span></span>

<span data-ttu-id="4902a-638">次の C\# サンプルは、以前の X++ サンプルからの行ごとの変換ではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-638">The following C\# sample is not a line-by-line translation from the previous X++ sample.</span></span> <span data-ttu-id="4902a-639">代わりに、C\# プログラムには X++ プログラムが依存している **retry** のキーワードの動作に似た別の構造体があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-639">Instead the C\# program has a different structure so that it mimics the behavior of the **retry** keyword that the X++ program relies on.</span></span> <span data-ttu-id="4902a-640">**try** および **catch** ブロックは、呼び出されたメソッドにあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-640">The **try** and **catch** blocks are in a called method.</span></span> <span data-ttu-id="4902a-641">**try** ブロックで使用される変数は、caller 側メソッドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-641">The variables that are used in the **try** block are stored in the caller method.</span></span> <span data-ttu-id="4902a-642">呼び出し元メソッドは、変数を **ref** キーワードで修飾されたパラメーターとして渡し、呼び出されたメソッドの **catch** ブロック内で値を修正できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-642">The caller method passes the variables as parameters that are decorated with the **ref** keyword, so that their values can be corrected inside the **catch** block of the called method.</span></span> <span data-ttu-id="4902a-643">呼び出されたメソッドはすべての例外を取得し、**ブール値** を返して、2 番目の呼び出しが必要かどうかを呼び出し元に返信します。</span><span class="sxs-lookup"><span data-stu-id="4902a-643">The called method captures all exceptions, and returns a **boolean** to communicate back to the caller whether a second call is required.</span></span>

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
                    bReturnCode = this
     .Rs008b_CSharp_ExceptionsAndRetry_Callee
    (ref iIndex);
                }
                else
                {
                    break;
                }
            }
            Console.WriteLine("End of C# caller method.");
        }
        private bool Rs008b_CSharp_ExceptionsAndRetry_Callee
                (ref int iIndex)
        {
            bool bReturnCode = true; // Means call this method again.
            string[] sStrings = new string[4];
            string sTemp;
            sStrings[0] = "First array element.";
            try
            {
                Console.WriteLine("At top of try block: "
                    + iIndex.ToString());
                sTemp = sStrings[iIndex];
                Console.WriteLine( "The array element is: " + sTemp );
                bReturnCode = false; // Means do not call this method again.
            }
            catch (Exception)
            {
                Console.WriteLine
                    ("In catch of -- Exception. Entering catch.");
                ++iIndex; // The 'ref' parameter in C#.
                Console.WriteLine
                    ("In catch of -- Exception. Leaving catch.");
                //retry;
                // In C# we let the caller method do the work
                // that the retry keyword does in X++.
            }
            Console.WriteLine("End of C# callee method.");
            return bReturnCode;
        }
    }


 
#### <a name="output"></a><span data-ttu-id="4902a-644">出力</span><span class="sxs-lookup"><span data-stu-id="4902a-644">Output</span></span>

<span data-ttu-id="4902a-645">コンソールへの出力を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-645">Here is the output to the console:</span></span>

<pre>
At top of try block: -1
In catch of -- Exception. Entering catch.
In catch of -- Exception. Leaving catch.
End of C# callee method.
At top of try block: 0
The array element is: First array element.
End of C# callee method.
End of C# caller method.
</pre>

## <a name="comparison-operators"></a><span data-ttu-id="4902a-646">比較: 演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-646">Comparison: Operators</span></span>
<span data-ttu-id="4902a-647">このセクションでは、X++ と C\# の間のループの演算子を比較します。</span><span class="sxs-lookup"><span data-stu-id="4902a-647">This section compares the operators between X++ and C\#.</span></span>

### <a name="assignment-operators"></a><span data-ttu-id="4902a-648">代入演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-648">Assignment Operators</span></span>

<span data-ttu-id="4902a-649">次のテーブルは、X++ と C\# の代入演算子の違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-649">The following table displays the differences between the assignment operators in X++ and C\#.</span></span>

| <span data-ttu-id="4902a-650">X++ および C#</span><span class="sxs-lookup"><span data-stu-id="4902a-650">X++ and C#</span></span> | <span data-ttu-id="4902a-651">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-651">Differences</span></span> |
|---|---|
| `=`| <span data-ttu-id="4902a-652">X++ では、この演算子によって、<strong>int64</strong> から <strong>int</strong> に代入する場合など、精度が損なわれる可能性がある場合は必ず暗黙的な変換が発生します。ただし、C# では、この代入により、コンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-652">In X++ this operator causes an implicit conversion whenever a loss of precision might occur, such for an assignment from an <strong>int64</strong> to an <strong>int</strong>. But in C# the assignment causes a compile error.</span></span>|
| <span data-ttu-id="4902a-653">`+=` および `-=`</span><span class="sxs-lookup"><span data-stu-id="4902a-653">`+=` and `-=`</span></span>| <span data-ttu-id="4902a-654">唯一の違いは、C# ではこれらの演算子もデリゲート操作で使用されることです。</span><span class="sxs-lookup"><span data-stu-id="4902a-654">The only difference is that in C# these operators are also used in delegate manipulation.</span></span>|
| <span data-ttu-id="4902a-655">++ および --</span><span class="sxs-lookup"><span data-stu-id="4902a-655">++ and --</span></span>| <span data-ttu-id="4902a-656">これらは、両方の言語のインクリメント演算子およびデクリメント演算子です。</span><span class="sxs-lookup"><span data-stu-id="4902a-656">These are the increment and decrement operators in both languages.</span></span> <span data-ttu-id="4902a-657">次の行は、両方の言語で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-657">The following line is identical in both languages:</span></span><br>`++myInteger;`<br><span data-ttu-id="4902a-658">ただし X++ では、これら 2 つの演算子は式ではなくステートメントに対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-658">But in X++ these two operators are for statements, not for expressions.</span></span> <span data-ttu-id="4902a-659">したがって、次の行は X++ でコンパイル エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="4902a-659">Therefore the following lines generate compile errors in X++:</span></span><br>`myStr = int2str(++myInteger);`<br>`myIntA = myIntBB++;`|

### <a name="arithmetic-operators"></a><span data-ttu-id="4902a-660">算術演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-660">Arithmetic Operators</span></span>

<span data-ttu-id="4902a-661">次のテーブルに、算術演算子の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-661">The following table lists the arithmetic operators.</span></span>

|<span data-ttu-id="4902a-662">X++ および C#</span><span class="sxs-lookup"><span data-stu-id="4902a-662">X++ and C#</span></span> | <span data-ttu-id="4902a-663">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-663">Differences</span></span> |
|---|---|
| *| <span data-ttu-id="4902a-664">乗算演算子との違いはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-664">As the multiplication operator, there are no differences.</span></span><br><span data-ttu-id="4902a-665">**注記**: アスタリスクは、X++ 言語の一部である SQL ステートメントにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-665">**Note**: The asterisk is also used in the SQL statements that are part of the X++ language.</span></span> <span data-ttu-id="4902a-666">これらの SQL ステートメントでは、アスタリスクを次のいずれかに設定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-666">In these SQL statements the asterisk can also be one of the following:</span></span><ul><li><span data-ttu-id="4902a-667">すべての列を返す必要があることを示すワイルドカード。</span><span class="sxs-lookup"><span data-stu-id="4902a-667">A wildcard indicating that all the columns should be returned.</span></span></li><li><span data-ttu-id="4902a-668"><strong>LIKE</strong> 句で使用される文字列の文字のワイルドカード。</span><span class="sxs-lookup"><span data-stu-id="4902a-668">A wildcard for characters in a string that is used on a <strong>like</strong> clause.</span></span></li></ul>|
| `/`| <span data-ttu-id="4902a-669">除算演算子は、X++ と C# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-669">The division operator is the same in X++ and C#.</span></span>|
| `MOD`| <span data-ttu-id="4902a-670">剰余工程については、唯一の違いは % 記号が C# で使用されることです。</span><span class="sxs-lookup"><span data-stu-id="4902a-670">For modulo operations, the only difference is that the % symbol is used in C#.</span></span>|
| +| <span data-ttu-id="4902a-671">加算演算子は、X++ と C# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-671">The addition operator is the same in X++ and C#.</span></span> <span data-ttu-id="4902a-672">プラス記号は文字列の連結にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-672">The plus sign is also used for string concatenation.</span></span> <span data-ttu-id="4902a-673">この演算子は、数値を追加し、両方の言語で文字列を連結します。 </span><span class="sxs-lookup"><span data-stu-id="4902a-673">This operator adds numbers and concatenates strings in both languages.</span></span>|
| -| <span data-ttu-id="4902a-674">減算演算子は、X++ と C# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-674">The subtraction operator is the same in X++ and C#.</span></span>|


### <a name="bitwise-operators"></a><span data-ttu-id="4902a-675">ビット演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-675">Bitwise Operators</span></span>

<span data-ttu-id="4902a-676">次のテーブルは X++ と C\# の間のビット演算子を比較しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-676">The following table compares the bitwise operators between X++ and C\#.</span></span>


| <span data-ttu-id="4902a-677">X++ および C\#</span><span class="sxs-lookup"><span data-stu-id="4902a-677">X++ and C\#</span></span> |                     <span data-ttu-id="4902a-678">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-678">Differences</span></span>                      |
|-------------|------------------------------------------------------|
|  &lt;&lt;   | <span data-ttu-id="4902a-679">左シフト演算子は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-679">The left shift operator is the same in X++ and C\#.</span></span>  |
|  &gt;&gt;   | <span data-ttu-id="4902a-680">右シフト演算子は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-680">The right shift operator is the same in X++ and C\#.</span></span> |
|      ~      | <span data-ttu-id="4902a-681">ビットの NOT 演算子は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-681">The bitwise NOT operator is the same in X++ and C\#.</span></span> |
|      &      | <span data-ttu-id="4902a-682">バイナリの AND 演算子は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-682">The binary AND operator is the same in X++ and C\#.</span></span>  |
|      ^      | <span data-ttu-id="4902a-683">バイナリの XOR 演算子は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-683">The binary XOR operator is the same in X++ and C\#.</span></span>  |
|             |                                                      |

### <a name="relational-operators"></a><span data-ttu-id="4902a-684">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-684">Relational Operators</span></span>

<span data-ttu-id="4902a-685">次のリレーショナル演算子は、X++ と C\# で同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-685">The following relational operators are the same in X++ and C\#:</span></span>
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

## <a name="comparison-events"></a><span data-ttu-id="4902a-686">比較: イベント</span><span class="sxs-lookup"><span data-stu-id="4902a-686">Comparison: Events</span></span>

<span data-ttu-id="4902a-687">X++ と C# がイベントデザインパターンを実装する方法にはいくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-687">There are some differences in how X++ and C# implement the event design pattern.</span></span> <span data-ttu-id="4902a-688">詳細については、「イベント用語とキーワード」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-688">For more information, see Event Terminology and Keywords.</span></span>

### <a name="comparison-of-events-between-x-and-c"></a><span data-ttu-id="4902a-689">X++ と C\# 間のイベントの比較</span><span class="sxs-lookup"><span data-stu-id="4902a-689">Comparison of Events between X++ and C\#</span></span>

<span data-ttu-id="4902a-690">委任が X++ と C# の各イベントに使用される方法には違いがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-690">There are differences in the way delegates are used for events in X++ versus C#.</span></span>

| <span data-ttu-id="4902a-691">概念</span><span class="sxs-lookup"><span data-stu-id="4902a-691">Concept</span></span> | <span data-ttu-id="4902a-692">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-692">X++</span></span> | <span data-ttu-id="4902a-693">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-693">C#</span></span> | <span data-ttu-id="4902a-694">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-694">Comments</span></span>|
|---|---|---|---|
| <span data-ttu-id="4902a-695"><strong>デリゲート</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-695"><strong>delegate</strong></span></span>| <span data-ttu-id="4902a-696">X++ では、デリゲートはクラスのメンバーとしてのみ宣言できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-696">In X++, a delegate can be declared only as a member on a class.</span></span> <span data-ttu-id="4902a-697">デリゲートは、テーブルのメンバーであることはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-697">A delegate cannot be a member on a table.</span></span> <span data-ttu-id="4902a-698">すべてのデリゲートはそのクラスのインスタンス メンバーであり、<strong>静的</strong>メンバーではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-698">All delegates are instance members of their class, not <strong>static</strong> members.</span></span> <span data-ttu-id="4902a-699">すべてのデリゲートは<strong>保護された</strong>メンバーであるため、デリゲートの宣言で使用できるアクセス修飾子はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-699">No access modifier can be used on a delegate declaration, because all delegates are <strong>protected</strong> members.</span></span> <span data-ttu-id="4902a-700">したがって、イベントは、デリゲートがメンバーである同じクラス内のコードによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-700">Therefore, the event can be raised only by code within the same class where the delegate is a member.</span></span> <span data-ttu-id="4902a-701">ただし、デリゲートのプライベート性質の 1 つの例外は、そのクラス以外のコードが、+= および -= 演算子を使用してデリゲートで操作できることです。</span><span class="sxs-lookup"><span data-stu-id="4902a-701">However, the one exception to the private nature of a delegate is that code outside their class can operate on the delegates by using the += and -= operators.</span></span>| <span data-ttu-id="4902a-702">C# では、各<strong>デリゲート</strong>は、すべて<strong>クラス</strong>が 1 つの型であるように 1 つの型です。</span><span class="sxs-lookup"><span data-stu-id="4902a-702">In C#, each <strong>delegate</strong> is a type, just as every <strong>class</strong> is a type.</span></span> <span data-ttu-id="4902a-703">デリゲートは、任意のクラスとは別に宣言されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-703">A delegate is declared independently of any class.</span></span> <span data-ttu-id="4902a-704"><strong>イベント</strong> キーワードがない場合、パラメーター タイプとしてクラスを設定することができるように、メソッドのパラメーター タイプとしてデリゲートを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-704">Without the <strong>event</strong> keyword, you can have a delegate as a parameter type on a method, just as you can have a class as a parameter type.</span></span> <span data-ttu-id="4902a-705">デリゲートのインスタンスを構築して、パラメーター値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-705">You can construct an instance of a delegate to pass in for the parameter value.</span></span>| <span data-ttu-id="4902a-706">X++ では、各クラスは型ですが、デリゲートは型ではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-706">In X++, each class is a type, but no delegate is a type.</span></span> <span data-ttu-id="4902a-707">デリゲートのインスタンスをコンストラクトすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-707">You cannot construct an instance of a delegate.</span></span> <span data-ttu-id="4902a-708">メソッドのパラメーターに設定できるデリゲートはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-708">No delegate can be a parameter for a method.</span></span> <span data-ttu-id="4902a-709">ただし、デリゲート メンバーを持つクラスを作成し、クラスのインスタンスをパラメーター値として渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-709">But you can create a class that has a delegate member, and you can pass instances of the class as parameter values.</span></span> <span data-ttu-id="4902a-710">詳細については、「X++ キーワード」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-710">For more information, see X++ Keywords.</span></span>|
| <span data-ttu-id="4902a-711"><strong>イベント</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-711"><strong>event</strong></span></span>| <span data-ttu-id="4902a-712">X++ コードでは、イベントは次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4902a-712">In X++ code, an event is one of the following:</span></span><ul><li><span data-ttu-id="4902a-713">デリゲートを明示的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4902a-713">An explicit call to a delegate.</span></span></li><li><span data-ttu-id="4902a-714">メソッドの開始または終了。</span><span class="sxs-lookup"><span data-stu-id="4902a-714">The start or end of a method.</span></span></li></ul><span data-ttu-id="4902a-715">X++ には <strong>event</strong> キーワードがありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-715">There is no <strong>event</strong> keyword in X++.</span></span>| <span data-ttu-id="4902a-716">C# では、<strong>event</strong> キーワードを使用して<strong>デリゲート</strong>型をクラスのメンバーとして宣言します。</span><span class="sxs-lookup"><span data-stu-id="4902a-716">In C#, the <strong>event</strong> keyword is used to declare a <strong>delegate</strong> type as a member of a class.</span></span> <span data-ttu-id="4902a-717"><strong>イベント</strong> キーワードの結果は、委任を確認する<strong>protected</strong> を委任することですが、+= および -= 演算子にはアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-717">The effect of the <strong>event</strong> keyword is to make the delegate <strong>protected</strong>, yet still accessible for the += and -= operators.</span></span> <span data-ttu-id="4902a-718">+= 演算子を使用して、<strong>イベント</strong> に対するイベント ハンドラー メソッドを申し込むことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-718">You can subscribe event handler methods to an <strong>event</strong> by using the += operator.</span></span> <span data-ttu-id="4902a-719">メソッドに関数ポインターをパラメータとして渡す手法として<strong>デリゲート</strong>は、<strong>イベント</strong>キーワードなしで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4902a-719">A <strong>delegate</strong> can be useful without the <strong>event</strong> keyword, as a technique for passing a function pointer as a parameter into a method.</span></span>| <span data-ttu-id="4902a-720">メソッドの開始前およびメソッドの終了後に発生する自動イベントは、AOT の使用によってのみサブスクライブできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-720">The automatic events that occur before the start of a method, and after the end of a method, can be subscribed to only by using the AOT.</span></span>|
| <span data-ttu-id="4902a-721">+= および -= 演算子</span><span class="sxs-lookup"><span data-stu-id="4902a-721">+= and -= operators</span></span>| <span data-ttu-id="4902a-722">X++ では、+= 演算子を使用して<strong>デリゲート</strong>に対するメソッドをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="4902a-722">In X++, you use the += operator to subscribe methods to a <strong>delegate</strong>.</span></span> <span data-ttu-id="4902a-723">-= 演算子は、デリゲートからメソッドのサブスクライブを解除します。</span><span class="sxs-lookup"><span data-stu-id="4902a-723">The -= operator unsubscribes a method from a delegate.</span></span>| <span data-ttu-id="4902a-724">C# では、+= 演算子を使用して、<strong>event</strong> キーワードとともに使用されていない<strong>イベント</strong>、または<strong>デリゲート</strong>にメソッドをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="4902a-724">In C#, you use the += operator to subscribe methods to an <strong>event</strong>, or to a <strong>delegate</strong> that is not used with the <strong>event</strong> keyword.</span></span>| <span data-ttu-id="4902a-725">デリゲートには、デリゲートにサブスクライブされたメソッドを持つすべてのオブジェクトへの照会が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4902a-725">The delegate contains a reference to all the objects that have methods subscribed to the delegate.</span></span> <span data-ttu-id="4902a-726">これらのオブジェクトはガベージ コレクションの対象外ですが、デリゲートはそれらの参照を保持します。</span><span class="sxs-lookup"><span data-stu-id="4902a-726">Those objects are not eligible for garbage collection while delegate holds those references.</span></span>|
| `eventHandler`| <span data-ttu-id="4902a-727">X++ で、+= や -= の演算子を使用してデリゲートからメソッドをサブスクライブまたはサブスクライブ解除を行う場合、<strong>eventHandler</strong> キーワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="4902a-727">In X++, the <strong>eventHandler</strong> keyword is required when you use either the += or -= operator to subscribe or unsubscribe a method from a delegate.</span></span>| <span data-ttu-id="4902a-728">`System.EventHandler` は、.NET Framework のデリゲート タイプです。</span><span class="sxs-lookup"><span data-stu-id="4902a-728">`System.EventHandler` is a delegate type in the .NET Framework.</span></span>| <span data-ttu-id="4902a-729">この用語は、C# または .NET Framework の場合とは異なる方法で、X++ で使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-729">This term is used differently in X++ than it is in C# or the .NET Framework.</span></span> <span data-ttu-id="4902a-730">詳細については、「X++ キーワード」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-730">For more information, see X++ Keywords.</span></span>|

### <a name="x-example"></a><span data-ttu-id="4902a-731">X++ 例</span><span class="sxs-lookup"><span data-stu-id="4902a-731">X++ Example</span></span>

<span data-ttu-id="4902a-732">X++ の例で注目すべき重要なことは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-732">The important things to notice in the X++ example are the following:</span></span>

-   <span data-ttu-id="4902a-733">`XppClass` には、`myDelegate` という名前のデリゲート メンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4902a-733">The `XppClass` has a delegate member that is named `myDelegate`.</span></span> <span data-ttu-id="4902a-734">**注記**: AOT には委任のノードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4902a-734">**Note**: The AOT contains a node for the delegate.</span></span> <span data-ttu-id="4902a-735">このノードは、[AOT] > [クラス] > [XppClass] > [myDelegate] にあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-735">The node is located at AOT > Classes > XppClass > myDelegate.</span></span> <span data-ttu-id="4902a-736">いくつかのイベント ハンドラー ノードは、myDelegate ノードの下に配置できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-736">Several event handler nodes can be located under the myDelegate node.</span></span> <span data-ttu-id="4902a-737">AOT ノードによって表されるイベント ハンドラーは、実行時に -= オペレーターによって削除できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-737">Event handlers that are represented by nodes in the AOT cannot be removed by the -= operator during run time.</span></span> 
-   <span data-ttu-id="4902a-738">デリゲート宣言の末尾の {} カッコは必要ですが、カッコにコードを所持することはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-738">The {} braces at the end of the delegate declaration are required, but they cannot have any code in them.</span></span>
-   <span data-ttu-id="4902a-739">`XppClass` には、パラメーター シグネチャがデリゲートと互換性を持つ 2 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-739">The `XppClass` has two methods whose parameter signatures are compatible with the delegate.</span></span> <span data-ttu-id="4902a-740">１ つの方法は静的です。</span><span class="sxs-lookup"><span data-stu-id="4902a-740">One method is static.</span></span>
-   <span data-ttu-id="4902a-741">2 つの互換メソッドは、+= 演算子と **eventHandler** キーワードを使用してデリゲートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-741">The two compatible methods are added to the delegate with the += operator and the **eventHandler** keyword.</span></span> <span data-ttu-id="4902a-742">これらのステートメントはイベント ハンドラー メソッドを呼び出さず、ステートメントはデリゲートにメソッドを追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="4902a-742">These statements do not call the event handler methods, the statements only add the methods to the delegate.</span></span>
-   <span data-ttu-id="4902a-743">デリゲートへの 1 回の呼び出しでイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="4902a-743">The event is raised by one call to the delegate.</span></span>
-   <span data-ttu-id="4902a-744">デリゲートに渡されたパラメーター値は、各イベント ハンドラー メソッドによって受け取られます。</span><span class="sxs-lookup"><span data-stu-id="4902a-744">The parameter value that passed in to the delegate is received by each event handler method.</span></span>
-   <span data-ttu-id="4902a-745">サンプルの一番上にある短い X++ ジョブがテストを開始します。</span><span class="sxs-lookup"><span data-stu-id="4902a-745">The short X++ job at the top of the example starts the test.</span></span>

<pre>
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
            myXppClass.myDelegate += eventHandler
                    (myXppClass.myEventSubscriberMethod2);
            myXppClass.myDelegate += eventHandler
                    (XppClass::myEventSubscriberMethod3);
            // Raise the event by calling the delegate one time,
            // which calls all the subscribed event handler methods.
            myXppClass.myDelegate(_stringFromJob);
        }
    }
</pre> 

<span data-ttu-id="4902a-746">以前の X++ ジョブの出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-746">The output from the previous X++ job is as follows:</span></span>

    X++, hello from static event handler 
    3: The information from the X++ job. X++, hello from instance event handler 
    2: The information from the X++ job.

### <a name="c-sample"></a><span data-ttu-id="4902a-747">C# サンプル</span><span class="sxs-lookup"><span data-stu-id="4902a-747">C# Sample</span></span>

<span data-ttu-id="4902a-748">このセクションには、以前の X++ サンプルのイベント設計パターンの C\# コード サンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4902a-748">This section contains a C\# code sample for the event design pattern of the previous X++ sample.</span></span>

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
            myCsClass.MyEvent += new MyDelegate
                    (myCsClass.MyEventSubscriberMethod2);
            myCsClass.MyEvent += new MyDelegate
                    (CsClass.MyEventSubscriberMethod3);
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

<span data-ttu-id="4902a-749">以前の C\# サンプルの出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4902a-749">The output from the previous C\# sample is as follows:</span></span>

    CsClass.exe C#, hello from instance event handler 
    2: The information from the C\# Main. C\#, hello from static event handler 
    3: The information from the C\# Main. |

### <a name="events-and-the-aot"></a><span data-ttu-id="4902a-750">イベントおよび AOT</span><span class="sxs-lookup"><span data-stu-id="4902a-750">Events and the AOT</span></span>

<span data-ttu-id="4902a-751">Finance and Operations には、AOT 内の品目のみに適用する他のイベント システムがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-751">Finance and Operations has other event systems that apply only to items in the AOT.</span></span> <span data-ttu-id="4902a-752">詳細については、「AOT でのイベント ハンドラー ノード」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-752">For more information, see Event Handler Nodes in the AOT.</span></span>

## <a name="comparison-precompiler-directives"></a><span data-ttu-id="4902a-753">比較: プリコンパイラのディレクティブ</span><span class="sxs-lookup"><span data-stu-id="4902a-753">Comparison: Precompiler Directives</span></span>

<span data-ttu-id="4902a-754">X++ および C# はプリコンパイラー ディレクティブ構文の一部のキーワードを共有しますが、意味は常に同じではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-754">X++ and C# share some keywords for their precompiler directive syntax, but the meanings are not always the same.</span></span>

### <a name="similarities"></a><span data-ttu-id="4902a-755">類似点</span><span class="sxs-lookup"><span data-stu-id="4902a-755">Similarities</span></span>

<span data-ttu-id="4902a-756">X++ および C\# コンパイラは、同じキーワードの多くを認識します。</span><span class="sxs-lookup"><span data-stu-id="4902a-756">The X++ and C\# compilers recognize many of the same keywords.</span></span> <span data-ttu-id="4902a-757">ほとんどの場合、キーワードは両言語のコンパイラに対して同じ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="4902a-757">In most cases, the keywords mean the same for both language compilers.</span></span>

### <a name="differences"></a><span data-ttu-id="4902a-758">違い</span><span class="sxs-lookup"><span data-stu-id="4902a-758">Differences</span></span>

<span data-ttu-id="4902a-759">X++ と C\# でのプリコンパイラ ディレクティブの基本的な違いは、両方の言語プリコンパイラが認識できる\#定義キーワードです。</span><span class="sxs-lookup"><span data-stu-id="4902a-759">A fundamental difference between the precompiler directives in X++ versus C\# is the \#define keyword that both language precompilers recognize.</span></span> <span data-ttu-id="4902a-760">C\# とは異なり、X++ では \#define ディレクティブではその構文にドットを必要とします。</span><span class="sxs-lookup"><span data-stu-id="4902a-760">Unlike C\#, in X++ the \#define directive requires a dot in its syntax.</span></span> <span data-ttu-id="4902a-761">X++ では、定義済の記号に値を指定するために丸かっこを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-761">In X++, parentheses can be used to give the defined symbol a value.</span></span> <span data-ttu-id="4902a-762">これらの違いを次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-762">These differences are shown in the following examples:</span></span>
-   <span data-ttu-id="4902a-763">X++: \#define.InitialYear(2003)</span><span class="sxs-lookup"><span data-stu-id="4902a-763">In X++: \#define.InitialYear(2003)</span></span>
-   <span data-ttu-id="4902a-764">C\#: \#define InitialYear</span><span class="sxs-lookup"><span data-stu-id="4902a-764">In C\#: \#define InitialYear</span></span>

<span data-ttu-id="4902a-765">小さな差異は、C\# では、\# 文字とディレクティブ キーワード (\# テストの定義など) の間にスペースとタブ文字があることです。</span><span class="sxs-lookup"><span data-stu-id="4902a-765">A minor difference is that in C\# there can be spaces and tab characters between the \# character and the directive keyword, such as \# define Testing.</span></span>

### <a name="identical-keywords"></a><span data-ttu-id="4902a-766">同一であるキーワード</span><span class="sxs-lookup"><span data-stu-id="4902a-766">Identical Keywords</span></span>

<span data-ttu-id="4902a-767">次のテーブルは、X++ および C\# で同様のプリコンパイラ ディレクティブを示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-767">The following table lists precompiler directives that are similar in X++ and C\#.</span></span>

| <span data-ttu-id="4902a-768">キーワード</span><span class="sxs-lookup"><span data-stu-id="4902a-768">Keyword</span></span> | <span data-ttu-id="4902a-769">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-769">X++</span></span> | <span data-ttu-id="4902a-770">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-770">C#</span></span> | <span data-ttu-id="4902a-771">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-771">Comments</span></span> |
|---|---|---|---|
| `#define` | <span data-ttu-id="4902a-772">X++ では、プリコンパイラ変数名を定義でき、その変数に値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-772">In X++, a precompiler variable name can be defined, and a value can be given to that variable.</span></span>                | <span data-ttu-id="4902a-773">C\# では、プリコンパイラ変数名を定義できますが、その変数に値を指定できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-773">In C\#, a precompiler variable name can be defined, but no value can be given to that variable.</span></span> <span data-ttu-id="4902a-774">また、\#C での定義\#はファイルの先頭になければならず、using ステートメントやクラス宣言などのコードの後には出現できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-774">Also, any \#define in C\# must occur at the top of the file, and cannot occur after any code such as a using statement or a class declaration.</span></span> | <span data-ttu-id="4902a-775">C\# コンパイラは、C\# コード ファイルで変数を定義しなくても、`/define` のコマンドライン パラメーターを入力し、プリコンパイラ変数名を定義できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-775">The C\# compiler can input a command line parameter of `/define` to define a precompiler variable name without defining the variable in any C\# code file.</span></span> <span data-ttu-id="4902a-776">X++ コンパイラには、`/define` に相当するものはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-776">The X++ compiler has no counterpart to `/define`.</span></span> |
|`#if`     | <span data-ttu-id="4902a-777">X++ では、\#if がプリコンパイラ変数が存在するかどうかと、変数に指定された値があるかどうかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-777">In X++, \#if can determine whether a precompiler variable exists, and whether the variable has a given value.</span></span> | <span data-ttu-id="4902a-778">C\# では、\#if はプリコンパイラ変数が存在するかどうかのみ特定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-778">In C\#, \#if can only determine whether a precompiler variable exists.</span></span> <span data-ttu-id="4902a-779">値が割り当てられないため、任意の値のテストはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-779">It cannot test for any value because no value can be assigned.</span></span> |      |
| `#endif`  | <span data-ttu-id="4902a-780">X++ では、\#endif が \#if ブロックの終了を示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-780">In X++, \#endif marks the end of an \#if block.</span></span> <span data-ttu-id="4902a-781">また、\#ifnot ブロックも終了します。</span><span class="sxs-lookup"><span data-stu-id="4902a-781">It also ends an \#ifnot block.</span></span>   | <span data-ttu-id="4902a-782">C\# では、ブロックに \#else が含まれるかに関係なく、\#endif を \#if ブロックの最後に記述します。</span><span class="sxs-lookup"><span data-stu-id="4902a-782">In C\#, \#endif marks the end of an \#if block, regardless of whether the block includes a \#else.</span></span>       |   |

### <a name="different-keywords-with-the-same-processing-result"></a><span data-ttu-id="4902a-783">同じ処理結果を持つ異なるキーワード</span><span class="sxs-lookup"><span data-stu-id="4902a-783">Different Keywords with the Same Processing Result</span></span>

<span data-ttu-id="4902a-784">次のテーブルは、X++ および C\# で異なる名前が付けられているが、処理時に同じ結果を与えるプリコンパイラ ディレクティブを示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-784">The following table lists precompiler directives that are named differently in X++ and C\#, but that give the same results when processed.</span></span>

| <span data-ttu-id="4902a-785">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-785">X++</span></span> | <span data-ttu-id="4902a-786">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-786">C#</span></span> | <span data-ttu-id="4902a-787">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-787">Comments</span></span> |
|---|---|---|
| <span data-ttu-id="4902a-788">\#ifnot</span><span class="sxs-lookup"><span data-stu-id="4902a-788">\#ifnot</span></span>                     | <span data-ttu-id="4902a-789">\#if \#else</span><span class="sxs-lookup"><span data-stu-id="4902a-789">\#if \#else</span></span>      | <span data-ttu-id="4902a-790">X++ には \#else ディレクティブはありませんが、\#ifnot は同様の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-790">There is no \#else directive in X++, but the \#ifnot provides similar functionality.</span></span> <span data-ttu-id="4902a-791">X++ では、\#ifnot がプリコンパイラ変数が存在するかどうかと、変数に指定された値がないかどうかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-791">In X++, \#ifnot can determine whether a precompiler variable exists, and whether the variable does not have a specific given value.</span></span> <span data-ttu-id="4902a-792">C\# では、\#if は ‘!’ の場合にプリコンパイラ変数が存在するかどうかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-792">In C\#, \#if can determine whether a precompiler variable exists when the ‘!’</span></span> <span data-ttu-id="4902a-793">symbol は変数名に対する接頭語になります。</span><span class="sxs-lookup"><span data-stu-id="4902a-793">symbol is prefixed to the variable name.</span></span> |
| `//BP Deviation documented` | <span data-ttu-id="4902a-794">\#pragma 警告</span><span class="sxs-lookup"><span data-stu-id="4902a-794">\#pragma warning</span></span> | <span data-ttu-id="4902a-795">これら X++ エントリと C\# エントリは等価ではありませんが、部分的な類似性があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-795">These X++ and C\# entries are not equivalent, but there is a partial similarity.</span></span> <span data-ttu-id="4902a-796">どちらもコンパイラの警告メッセージを抑制します。</span><span class="sxs-lookup"><span data-stu-id="4902a-796">Both suppress compiler warning messages.</span></span>                    |
| <span data-ttu-id="4902a-797">\#macrolib</span><span class="sxs-lookup"><span data-stu-id="4902a-797">\#macrolib</span></span>                  | <span data-ttu-id="4902a-798">C++ 内の .HPP ファイル</span><span class="sxs-lookup"><span data-stu-id="4902a-798">.HPP file in C++</span></span> | <span data-ttu-id="4902a-799">X++ ディレクティブ \#macrolib と C++ の .HPP ファイルの間には部分的な類似点があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-799">There is a partial similarity between the X++ directive \#macrolib versus an .HPP file in C++.</span></span> <span data-ttu-id="4902a-800">両方とも複数の\#定義ステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-800">Both can contain several \#define statements.</span></span>            |

### <a name="precompiler-directives-exclusive-to-x"></a><span data-ttu-id="4902a-801">X++ 限定のプリコンパイラ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="4902a-801">Precompiler Directives Exclusive to X++</span></span>

<span data-ttu-id="4902a-802">次のテーブルは、C\# に直接対応するものがない X++ プリコンパイラ ディレクティブを示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-802">The following table lists X++ precompiler directives that have no direct counterpart in C\#.</span></span>

| <span data-ttu-id="4902a-803">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-803">X++</span></span>                  | <span data-ttu-id="4902a-804">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-804">Comments</span></span>    |
|---|---|
| <span data-ttu-id="4902a-805">\#linenumber</span><span class="sxs-lookup"><span data-stu-id="4902a-805">\#linenumber</span></span>         | <span data-ttu-id="4902a-806">\# 行番号ディレクティブは、情報ログに出力できるように、行番号を取得するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-806">The \#linenumber directive is for obtaining the line number, so that it can be output to the Infolog.</span></span> <br><span data-ttu-id="4902a-807">C\# ディレクティブ \# 行は、その目的が行番号を設定することであるため異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-807">The C\# directive \#line is different because its purpose is for setting the line number.</span></span> |
| <span data-ttu-id="4902a-808">\#defdec \#definc</span><span class="sxs-lookup"><span data-stu-id="4902a-808">\#defdec \#definc</span></span>    |         |
| <span data-ttu-id="4902a-809">\#globaldefine</span><span class="sxs-lookup"><span data-stu-id="4902a-809">\#globaldefine</span></span>       | <span data-ttu-id="4902a-810">X++ では、\#globaldefine と \#define はわずかに違います。</span><span class="sxs-lookup"><span data-stu-id="4902a-810">In X++, there is a small difference between \#globaldefine versus \#define.</span></span> <span data-ttu-id="4902a-811">違いは、\#globaldefine は、\#define によってプリコンパイラ変数に割り当てられた現在の非 null 値を上書きしないことです。</span><span class="sxs-lookup"><span data-stu-id="4902a-811">The difference is that \#globaldefine never overwrites a current nonnull value that was assigned to a precompiler variable by \#define.</span></span> <br><span data-ttu-id="4902a-812">C\# ではプリコンパイラの変数名は値を指定することができないため、C\# はこの違いと大きく異なっています。</span><span class="sxs-lookup"><span data-stu-id="4902a-812">C\# has nothing similar to this difference, because in C\#, a precompiler variable name cannot be given a value.</span></span> |
| <span data-ttu-id="4902a-813">\#localmacro \#マクロ</span><span class="sxs-lookup"><span data-stu-id="4902a-813">\#localmacro \#macro</span></span> | <span data-ttu-id="4902a-814">X++ では、\#localmacro を使用すると、プリコンパイラ変数に複数行の値を代入できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-814">In X++, \#localmacro enables you to assign a multiline value to a precompiler variable.</span></span> <span data-ttu-id="4902a-815">\#マクロは同義語ですが、 \#localmacro をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4902a-815">\#macro is a synonym, but \#localmacro is recommended.</span></span> <br><span data-ttu-id="4902a-816">C\# では、\#define ディレクティブにこの機能の一部がありますが、プリコンパイラ変数に値を代入できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-816">In C\#, the \#define directive has part of this functionality, but it cannot assign a value to a precompiler variable.</span></span>      |
| <span data-ttu-id="4902a-817">\#globalmacro</span><span class="sxs-lookup"><span data-stu-id="4902a-817">\#globalmacro</span></span>        | <span data-ttu-id="4902a-818">X++ では、\#globalmacro は優先 \#localmacro とほぼ同じです。</span><span class="sxs-lookup"><span data-stu-id="4902a-818">In X++, \#globalmacro is almost the same as the preferred \#localmacro.</span></span>          |

## <a name="comparison-object-oriented-programming"></a><span data-ttu-id="4902a-819">比較: オブジェクト指向プログラミング</span><span class="sxs-lookup"><span data-stu-id="4902a-819">Comparison: Object Oriented Programming</span></span>
<span data-ttu-id="4902a-820">X++ のオブジェクト指向プログラミング (OOP) の原則は、C\# と異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-820">The object oriented programming (OOP) principles of X++ differ from C\#.</span></span>

### <a name="conceptual-comparisons"></a><span data-ttu-id="4902a-821">概念の比較</span><span class="sxs-lookup"><span data-stu-id="4902a-821">Conceptual Comparisons</span></span>

<span data-ttu-id="4902a-822">次のテーブルは、X++ と C\# の間の OOP の原則の実装を比較しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-822">The following table compares the implementation of OOP principles between X++ and C\#.</span></span>

|<span data-ttu-id="4902a-823">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-823">Feature</span></span>|<span data-ttu-id="4902a-824">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-824">X++</span></span>|<span data-ttu-id="4902a-825">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-825">C#</span></span>|<span data-ttu-id="4902a-826">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-826">Comments</span></span>|
|---|---|---|---|
| <span data-ttu-id="4902a-827">キャスティング</span><span class="sxs-lookup"><span data-stu-id="4902a-827">Casting</span></span> | <span data-ttu-id="4902a-828">X++ 言語には、キーワード <strong>is</strong> および <strong>as</strong> があり、ダウンキャストを安全かつ明示的にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-828">The X++ language has the keywords <strong>is</strong> and <strong>as</strong>, which are used to make downcasts safe and explicit.</span></span> <span data-ttu-id="4902a-829">**ヒント**: X++ では、基本クラス変数を派生クラス変数にダウンキャストするときに、<strong>as</strong> キーワードを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-829">**Tip**: X++ does not require the use of the <strong>as</strong> keyword when you downcast a base class variable to a derived class variable.</span></span> <span data-ttu-id="4902a-830">ただし、すべてのダウンキャスト ステートメントで <strong>as</strong> キーワードを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4902a-830">However, we recommend that all downcast statements use the <strong>as</strong> keyword.</span></span>| <span data-ttu-id="4902a-831">オブジェクトは継承パスを上または下にキャストすることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-831">An object can be cast either up or down the inheritance path.</span></span> <span data-ttu-id="4902a-832">ダウンキャストは <strong>as</strong> キーワードを必要とします。</span><span class="sxs-lookup"><span data-stu-id="4902a-832">Downcasts require the <strong>as</strong> keyword.</span></span>| <span data-ttu-id="4902a-833">X++ キーワード <strong>is</strong> および <strong>as</strong> の詳細については、式の演算子: 継承の Is および As を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-833">For more information about the X++ keywords <strong>is</strong> and <strong>as</strong>, see Expression Operators: Is and As for Inheritance.</span></span>|
| <span data-ttu-id="4902a-834">ローカル関数</span><span class="sxs-lookup"><span data-stu-id="4902a-834">Local functions</span></span>| <span data-ttu-id="4902a-835">メソッドには、ゼロ以上のローカル関数用の宣言およびコードの本文を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-835">A method can contain a declaration and code body for zero or more local functions.</span></span> <span data-ttu-id="4902a-836">そのメソッドのみローカル関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-836">Only that method can have calls to the local function.</span></span>| <span data-ttu-id="4902a-837">C# 3.0 では、匿名関数およびローカル関数といくつかの類似点を持つラムダ式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4902a-837">C# 3.0 supports lambda expressions, which have some similarity to anonymous functions and local functions.</span></span> <span data-ttu-id="4902a-838">ラムダ式は、デリゲートでよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-838">Lambda expressions are often used with delegates.</span></span>| |
| <span data-ttu-id="4902a-839">メソッドのオーバーロード</span><span class="sxs-lookup"><span data-stu-id="4902a-839">Method overloading</span></span> | <span data-ttu-id="4902a-840">メソッドのオーバーロードはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4902a-840">Method overloading is not supported.</span></span> <span data-ttu-id="4902a-841">メソッド名は、クラスごとに 1 回のみ発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-841">A method name can occur only one time per class.</span></span>| <span data-ttu-id="4902a-842">メソッドのオーバーロードはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4902a-842">Method overloading is supported.</span></span> <span data-ttu-id="4902a-843">メソッド名は、それぞれのケースで異なるパラメーターシグネチャを使用して、1 つのクラスで複数回発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-843">A method name can occur multiple times in one class, with different parameter signatures in each case.</span></span>| <span data-ttu-id="4902a-844">X++ はメソッドでの省略可能パラメーターをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4902a-844">X++ does support optional parameters on methods.</span></span> <span data-ttu-id="4902a-845">省略可能なパラメーターは、メソッドのオーバーロードを部分的に反映できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-845">Optional parameters can partially mimic method overloading.</span></span> <span data-ttu-id="4902a-846">詳細については、この表の、「オプション パラメーターの行」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-846">For more information, see the row for optional parameters in this table.</span></span>|
| <span data-ttu-id="4902a-847">メソッドのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="4902a-847">Method overriding</span></span> | <span data-ttu-id="4902a-848">メソッドのオーバーライドはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4902a-848">Method overriding is supported.</span></span> <span data-ttu-id="4902a-849">派生クラスは、パラメータの署名がどちらの場合も同じ限り、基本クラスと同じ名前のメソッドを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-849">A derived class can have a method by the same name as in the base class, as long as the parameter signature is the same in both cases.</span></span> <span data-ttu-id="4902a-850">唯一の例外は、オーバーライドするメソッドがパラメーターに既定値を追加できることです。</span><span class="sxs-lookup"><span data-stu-id="4902a-850">The only exception is that the overriding method can add a default value to a parameter.</span></span>| <span data-ttu-id="4902a-851">メソッドのオーバーライドはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4902a-851">Method overriding is supported.</span></span> <span data-ttu-id="4902a-852">派生クラスでメソッドを上書きするには、<strong>virtual</strong> キーワードをメソッドに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-852">The <strong>virtual</strong> keyword must be applied to a method before the method can be overridden in a derived class.</span></span>| <span data-ttu-id="4902a-853">上書きするメソッドの概念には、メソッド名、そのパラメーター署名および戻り値の型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4902a-853">The concept of overriding a method includes the method name, its parameter signature, and its return type.</span></span> <span data-ttu-id="4902a-854">メソッドのオーバーライドの概念は、基準メソッドとオーバーライド メソッドがこれらの側面のいずれかで異なる場合は適用されません。</span><span class="sxs-lookup"><span data-stu-id="4902a-854">The concept of method overriding does not apply if the base method and the overriding method differ in any of these aspects.</span></span>|
| <span data-ttu-id="4902a-855">オプションのパラメーター</span><span class="sxs-lookup"><span data-stu-id="4902a-855">Optional parameters</span></span>| <span data-ttu-id="4902a-856">パラメーター宣言の後に既定値の割り当てを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-856">A parameter declaration can be followed by a default value assignment.</span></span> <span data-ttu-id="4902a-857">メソッド呼び出し元には、そのパラメーターの値を渡すか、既定値を受け入れるようにパラメーターを無視するかの選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-857">The method caller has the option of passing a value for that parameter, or ignoring the parameter to accept the default value.</span></span> <span data-ttu-id="4902a-858">このメソッドは、同じメソッド名への 2 回の呼び出しが異なる数のパラメーターを渡すことができるため、メソッドのオーバーロードに似ています。</span><span class="sxs-lookup"><span data-stu-id="4902a-858">This feature mimics method overloading because two calls to the same method name can pass different numbers of parameters.</span></span> <span data-ttu-id="4902a-859">既定値を持つ各パラメーターは、既定値を持たない最後のパラメーターに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-859">Each parameter that has a default value must follow the last parameter that does not have a default value.</span></span>| <span data-ttu-id="4902a-860">オプションのパラメーターは、<strong>params</strong> キーワードによりサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4902a-860">Optional parameters are supported by the <strong>params</strong> keyword.</span></span> <span data-ttu-id="4902a-861">呼び出しの表示ポイントから<strong>パラメーター</strong>キーワードが無くても、メソッドのオーバーロードは、部分的に同様の機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-861">Even without the <strong>params</strong> keyword, from the point of view of the caller, method overloading can provide partially similar functionality.</span></span>| <span data-ttu-id="4902a-862">詳細については、「パラメーターとスコープおよびオプションのパラメーターの使用」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-862">For more information, see Parameters and Scoping and Using Optional Parameters.</span></span>|
| <span data-ttu-id="4902a-863">単一の継承</span><span class="sxs-lookup"><span data-stu-id="4902a-863">Single inheritance</span></span>| <span data-ttu-id="4902a-864">AOT では、クラスの classDeclaration ノード内で <strong>extends</strong> キーワードを使用することにより、X++ クラスを他の X++ クラスから派生させることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-864">You can derive your X++ class from another X++ class by using the <strong>extends</strong> keyword in the classDeclaration node of your class, in the AOT.</span></span> <span data-ttu-id="4902a-865">別のクラスから暗黙的に直接派生するクラスはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-865">No class implicitly derives directly from another class.</span></span> <span data-ttu-id="4902a-866">クラスを `Object` クラスから直接派生させる場合は、<strong>拡張</strong>キーワードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-866">If you want your class to directly derive from the `Object` class, you must use the <strong>extends</strong> keyword.</span></span> <span data-ttu-id="4902a-867"><strong>extends</strong> キーワード上では 1 つのクラスのみを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-867">You can specify only one class on the <strong>extends</strong> keyword.</span></span><br><br><span data-ttu-id="4902a-868">**注意**: 他のクラスが派生する X++ 基本クラスを変更する場合は、コンパイル フォワードを使用してその基本クラスを再コンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-868">**Caution**: When you modify an X++ base class that other classes derive from, you must recompile that base class using the Compile forward.</span></span> <span data-ttu-id="4902a-869">このオプションを使用すると、派生クラスも再コンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="4902a-869">This option ensures that the derived classes are also recompiled.</span></span> <span data-ttu-id="4902a-870">派生クラスも再コンパイルされるようにするには、基本クラス ノードを右クリックし、[アドイン] > [コンパイル フォワード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4902a-870">To ensure the derived classes are also recompiled, right-click the base class node, and then click Add-Ins > Compile forward.</span></span> <span data-ttu-id="4902a-871">[ビルド] > [コンパイル] のクリック (または F7 キーを押すこと) という代わりの方法では、基底クラスを変更できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-871">The alternative of clicking Build > Compile (or pressing the F7 key) is sometimes insufficient for a base class change.</span></span><br><br><span data-ttu-id="4902a-872">クラスは、ゼロから多くのインターフェイスを実装できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-872">A class can implement zero to many interfaces.</span></span> <br><br><span data-ttu-id="4902a-873">X++ テーブルは `Common` テーブル、および `xRecord` クラスから暗黙的に継承します。</span><span class="sxs-lookup"><span data-stu-id="4902a-873">An X++ table implicitly inherits from the `Common` table, and from the `xRecord` class.</span></span>| <span data-ttu-id="4902a-874">別のクラスから派生するために C# は<strong>拡張</strong>キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-874">C# uses the <strong>extends</strong> keyword to derive from another class.</span></span> <span data-ttu-id="4902a-875">すべての .NET Framework クラスは明示的に別のクラスから派生しない限り、`System.Object` クラスから暗黙的に派生しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-875">All .NET Framework classes implicitly derive from the `System.Object` class, unless they explicitly derive from another class.</span></span>| |

### <a name="keyword-comparisons"></a><span data-ttu-id="4902a-876">キーワードの比較</span><span class="sxs-lookup"><span data-stu-id="4902a-876">Keyword Comparisons</span></span>

<span data-ttu-id="4902a-877">次のテーブルは、X++ および C＃ の OOP 関連のキーワードを示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-877">The following table lists the OOP-related keywords in X++ and C#.</span></span>

|<span data-ttu-id="4902a-878">キーワード</span><span class="sxs-lookup"><span data-stu-id="4902a-878">Keyword</span></span>|<span data-ttu-id="4902a-879">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-879">X++</span></span>|<span data-ttu-id="4902a-880">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-880">C#</span></span>|<span data-ttu-id="4902a-881">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-881">Comments</span></span>|
|---|---|---|---|
| <span data-ttu-id="4902a-882"><strong>抽象</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-882"><strong>abstract</strong></span></span>| | | <span data-ttu-id="4902a-883">差異はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-883">No difference.</span></span>|
| <span data-ttu-id="4902a-884"><strong>クラス</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-884"><strong>class</strong></span></span>| <span data-ttu-id="4902a-885">修飾子 <strong>パブリック</strong> と <strong>プライベート</strong> はクラス宣言で無視されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-885">The modifiers <strong>public</strong> and <strong>private</strong> are ignored on class declarations.</span></span> <span data-ttu-id="4902a-886">クラスの名前空間グループ化の概念はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-886">There is no concept of a namespace grouping of classes.</span></span> <span data-ttu-id="4902a-887">どのクラス名にもピリオド (.) はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-887">There are no dots (.) in any class names.</span></span>| <span data-ttu-id="4902a-888">修飾子 <strong>パブリック</strong> と <strong>プライベート</strong> を使用してクラス宣言を変更できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-888">The modifiers <strong>public</strong> and <strong>private</strong> can be used to modify class declarations.</span></span> <span data-ttu-id="4902a-889">C＃にはキーワード<strong>内部</strong>があります。このキーワードは、クラスがアセンブリ ファイル内でグループ化されている方法が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="4902a-889">C# also has the keyword <strong>internal</strong>, which relates to how classes are grouped together in assembly files.</span></span>| <span data-ttu-id="4902a-890"><strong>protected</strong> クラスの概念はなく、クラスの <strong>protected</strong> メンバーのみあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-890">There is no concept of a <strong>protected</strong> class, only <strong>protected</strong> members of a class.</span></span>|
| <span data-ttu-id="4902a-891"><strong>拡張</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-891"><strong>extends</strong></span></span>| <span data-ttu-id="4902a-892">クラス宣言は、<strong>拡張</strong>キーワードを利用して、別のクラスから継承できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-892">A class declaration can inherit from another class by using the <strong>extends</strong> keyword.</span></span>| <span data-ttu-id="4902a-893"><strong>拡張</strong>および<strong>実装</strong>などのキーワードが X++ で使用される場合、コロン (:) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-893">A colon (:) is used where the keywords <strong>extends</strong> and <strong>implements</strong> are used in X++.</span></span>| |
| <span data-ttu-id="4902a-894"><strong>最終</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-894"><strong>final</strong></span></span>| <span data-ttu-id="4902a-895"><strong>最終</strong>メソッドは、派生クラスで上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-895">A <strong>final</strong> method cannot be overridden in a derived class.</span></span> <span data-ttu-id="4902a-896"><strong>最終</strong>クラスは拡張できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-896">A <strong>final</strong> class cannot be extended.</span></span>| <span data-ttu-id="4902a-897">クラスのキーワード <strong>シールド</strong> は、<strong>最終</strong> が X++クラスで意味するのと同じことを意味します。</span><span class="sxs-lookup"><span data-stu-id="4902a-897">The keyword <strong>sealed</strong> on a class means the same thing that <strong>final</strong> means on an X++ class.</span></span>| |
| <span data-ttu-id="4902a-898"><strong>実装</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-898"><strong>implements</strong></span></span>| <span data-ttu-id="4902a-899">クラス宣言では、<strong>実装</strong>キーワードを利用して、<strong>インターフェイス</strong>を実装することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-899">A class declaration can implement an <strong>interface</strong> by using the <strong>implements</strong> keyword.</span></span>| | |
| <span data-ttu-id="4902a-900"><strong>インターフェイス</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-900"><strong>interface</strong></span></span>| <span data-ttu-id="4902a-901"><strong>インターフェイス</strong>はクラスで実装する必要があるメソッドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-901">An <strong>interface</strong> can specify methods that the class must implement.</span></span>| <span data-ttu-id="4902a-902"><strong>インターフェイス</strong>はクラスで実装する必要があるメソッドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-902">An <strong>interface</strong> can specify methods that the class must implement.</span></span>| |
| <span data-ttu-id="4902a-903"><strong>新規</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-903"><strong>new</strong></span></span>| <span data-ttu-id="4902a-904"><strong>new</strong> キーワードは、クラスの新しいインスタンスを割り当てるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-904">The <strong>new</strong> keyword is used to allocate a new instance of a class.</span></span> <span data-ttu-id="4902a-905">コンストラクターは自動で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-905">Then the constructor is automatically called.</span></span> <span data-ttu-id="4902a-906">各クラスには、厳密に 1 つのコンストラクターがあり、コンストラクターの名前は `new` です。</span><span class="sxs-lookup"><span data-stu-id="4902a-906">Each class has exactly one constructor, and the constructor is named `new`.</span></span> <span data-ttu-id="4902a-907">コンストラクターが入力するパラメーターを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-907">You can decide what parameters the constructor should input.</span></span>| <span data-ttu-id="4902a-908"><strong>new</strong> キーワードは、クラスの新しいインスタンスを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-908">The <strong>new</strong> keyword is used to create a new instance of a class.</span></span> <span data-ttu-id="4902a-909">コンストラクターは自動で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-909">Then the constructor is automatically called.</span></span> <span data-ttu-id="4902a-910">コンストラクターのメソッド自体は `new` という名前ではなく、クラスと同じ名前です。</span><span class="sxs-lookup"><span data-stu-id="4902a-910">Constructor methods themselves are not named `new`, they have the same name as the class.</span></span><br><span data-ttu-id="4902a-911">**注記**: <strong>新しい</strong>キーワードをメソッドに使用して、メソッドが基本クラスの同じメソッドを上書きする方法を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-911">**Note**: The <strong>new</strong> keyword can also be used on a method, to modify the way in which the method overrides the same method in the base class.</span></span>| <span data-ttu-id="4902a-912">X++ と C# はどちらもコードで明示的に記述されたコンストラクターを持たないクラスの既定のコンストラクターであると想定します。</span><span class="sxs-lookup"><span data-stu-id="4902a-912">Both X++ and C# assume a default constructor for classes that have no constructor explicitly written in their code.</span></span>|
| <span data-ttu-id="4902a-913"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-913"><strong>null</strong></span></span>| | | <span data-ttu-id="4902a-914">差異はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-914">No difference.</span></span>|
| <span data-ttu-id="4902a-915"><strong>プライベート</strong>および<strong>保護</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-915"><strong>private</strong> and <strong>protected</strong></span></span>| <span data-ttu-id="4902a-916"><strong>private</strong> および <strong>protected</strong> キーワードは、クラス メンバーの申告を変更するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-916">The <strong>private</strong> and <strong>protected</strong> keywords can be used to modify the declaration of a class member.</span></span>| <span data-ttu-id="4902a-917"><strong>private</strong> および <strong>protected</strong> キーワードは、クラス メンバーの申告を変更するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-917">The <strong>private</strong> and <strong>protected</strong> keywords can be used to modify the declaration of a class member.</span></span>||
| <span data-ttu-id="4902a-918"><strong>パブリック</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-918"><strong>public</strong></span></span>| <span data-ttu-id="4902a-919"><strong>パブリック</strong>の既定のアクセス レベルを持つ<strong>パブリック</strong>、<strong>保護</strong>、または<strong>プライベート</strong>で変更されないメソッド。</span><span class="sxs-lookup"><span data-stu-id="4902a-919">A method that is not modified with <strong>public</strong>, <strong>protected</strong>, or <strong>private</strong> has the default access level of <strong>public</strong>.</span></span>| <span data-ttu-id="4902a-920"><strong>プライベート</strong>の既定のアクセス レベルを持つ<strong>パブリック</strong>、<strong>保護</strong>、または<strong>プライベート</strong>で変更されないメソッド。</span><span class="sxs-lookup"><span data-stu-id="4902a-920">A method that is not modified with <strong>public</strong>, <strong>protected</strong>, or <strong>private</strong> has the default access level of <strong>private</strong>.</span></span>||
| <span data-ttu-id="4902a-921"><strong>静的</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-921"><strong>static</strong></span></span>| <span data-ttu-id="4902a-922">メソッドは<strong>静的</strong>にできますが、フィールドはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-922">A method can be <strong>static</strong>, but a field cannot.</span></span>| <span data-ttu-id="4902a-923">メソッドとフィールドの両方を<strong>静的</strong>にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-923">Both methods and fields can be <strong>static</strong>.</span></span>| |
| <span data-ttu-id="4902a-924"><strong>スーパー</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-924"><strong>super</strong></span></span>| <span data-ttu-id="4902a-925"><strong>super</strong> キーワードは、基本クラスで同じメソッドにアクセスするために派生クラスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-925">The <strong>super</strong> keyword is used in a derived class to access the same method on its base class.</span></span> `void method2()`<br>`{`<br>`    // Call method2 method`<br> `    // on the base class.`<br> `    super();` <br>`}`<br>| <span data-ttu-id="4902a-926"><strong>base</strong> キーワードは、基本クラスのさまざまなメソッドにアクセスするために派生クラスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-926">The <strong>base</strong> keyword is used in a derived class to access various methods in its base class.</span></span> <br>`void method2()` <br>`{`<br> `    // Call methods on`<br> `    // the base class.`<br> `    base.method2();`<br> `    base.method3();` <br>`}`| <span data-ttu-id="4902a-927">C# では、<strong>ベース</strong>を使用して基本コンストラクターを呼び出すための特別な構文があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-927">In C#, there is special syntax for using <strong>base</strong> to call the base constructor.</span></span>|
| <span data-ttu-id="4902a-928"><strong>この</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-928"><strong>this</strong></span></span>| <span data-ttu-id="4902a-929">同じオブジェクトで 1 つのインスタンス メソッドから別への呼び出しで、呼び出されたメソッドの修飾子が必要です。</span><span class="sxs-lookup"><span data-stu-id="4902a-929">For a call from one instance method to another on the same object, a qualifier for the called method is required.</span></span> <span data-ttu-id="4902a-930">キーワード <strong>これ</strong> は現在のオブジェクトの修飾子として使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-930">The keyword <strong>this</strong> is available as a qualifier for the current object.</span></span>| <span data-ttu-id="4902a-931">同じオブジェクトで 1 つのインスタンス メソッドから別への呼び出しで、呼び出されたメソッドの修飾子は必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-931">For a call from one instance method to another on the same object, a qualifier for the called method is not required.</span></span> <span data-ttu-id="4902a-932">ただし、<strong>この</strong>キーワードは現在のオブジェクトの修飾子として使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-932">However, the <strong>this</strong> keyword is available as a qualifier for the current object.</span></span> <span data-ttu-id="4902a-933">実際、キーワード <strong>this</strong> は IntelliSense の情報を表示することで役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="4902a-933">In practice, the keyword <strong>this</strong> can be helpful by displaying IntelliSense information.</span></span>| |
| `finalize`| <span data-ttu-id="4902a-934">`Object` クラスには、`finalize` メソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4902a-934">The `Object` class contains the `finalize` method.</span></span> <span data-ttu-id="4902a-935">`finalize` メソッドは<strong>最終</strong>でないため、オーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-935">The `finalize` method is not <strong>final</strong>, and it can be overridden.</span></span> <span data-ttu-id="4902a-936">`finalize` メソッドは、C# では `System.Object.Finalize` メソッドと似ているように見えますが、X++ では `finalize` メソッドにはどのような特別な意味もありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-936">The `finalize` method appears to resemble the `System.Object.Finalize` method in C#, but in X++ the `finalize` method has no special meaning of any kind.</span></span> <span data-ttu-id="4902a-937">オブジェクへの最後の参照がオブジェクトの参照を停止した場合、オブジェクトはメモリから自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-937">An object is automatically removed from memory when the last reference to the object stops referencing the object.</span></span> <span data-ttu-id="4902a-938">たとえば、これは、最後の参照がスコープ外になるまたは参照する他のオブジェクトが割り当てられる場合に、発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-938">For example, this can happen when the last reference goes out of scope or is assigned another object to reference.</span></span>| <span data-ttu-id="4902a-939">`Finalize` と `Dispose` メソッドはいくつかのタイプのクラスで共通です。</span><span class="sxs-lookup"><span data-stu-id="4902a-939">The methods `Finalize` and `Dispose` are common on some types of classes.</span></span> <span data-ttu-id="4902a-940">ガベージ コレクターは、破棄して処理するときに、`Finalize` メソッドと `Dispose` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4902a-940">The garbage collector calls the `Finalize` and `Dispose` methods when it destroys and object.</span></span>| <span data-ttu-id="4902a-941">C# では、.NET Framework の `System.GC.Collect` メソッドを呼び出してガベージ コレクターを開始できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-941">In C#, the `System.GC.Collect` method in the .NET Framework can be called to start the garbage collector.</span></span> <span data-ttu-id="4902a-942">X++ には確定的なガベージ コレクターが使用されているため、X++ には似たような機能はありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-942">There is no similar function in X++ because X++ uses a deterministic garbage collector.</span></span>|
| `main`| <span data-ttu-id="4902a-943">メニューから呼び出されるクラスには、システムによって呼び出される `main` メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-943">Classes that are invoked from a menu have their `main` method called by the system.</span></span>| <span data-ttu-id="4902a-944">コマンド ライン コンソールから呼び出されるクラスには、システムによって呼び出される `Main` メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-944">Classes that are invoked from a command line console have their `Main` method called by the system.</span></span>| |

## <a name="comparison-classes"></a><span data-ttu-id="4902a-945">比較: クラス</span><span class="sxs-lookup"><span data-stu-id="4902a-945">Comparison: Classes</span></span>
<span data-ttu-id="4902a-946">.NET frameworkで C\# を使用すると、クラスは名前空間にグループ分けされます。</span><span class="sxs-lookup"><span data-stu-id="4902a-946">When you use C\# in the .NET Framework, classes are grouped into namespaces.</span></span> <span data-ttu-id="4902a-947">各名前空間では、ファイル操作やリフレクションなどの機能区分に焦点を当てます。</span><span class="sxs-lookup"><span data-stu-id="4902a-947">Each namespace focuses on a functional area such as file operations or reflection.</span></span> <span data-ttu-id="4902a-948">ただし、X++ のクラスを使用する場合、名前空間のようなグループ分けは表示されません。</span><span class="sxs-lookup"><span data-stu-id="4902a-948">However, when you use the classes in X++, there are no visible groupings like a namespace.</span></span>

### <a name="comparison-classes-about-reflection"></a><span data-ttu-id="4902a-949">比較: リフレクションに関するクラス</span><span class="sxs-lookup"><span data-stu-id="4902a-949">Comparison: Classes about Reflection</span></span>
<span data-ttu-id="4902a-950">X++ では、`TreeNode` クラスがアプリケーション オブジェクト ツリー (AOT) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-950">In X++ the `TreeNode` class provides access to the Application Object Tree (AOT).</span></span> <span data-ttu-id="4902a-951">`TreeNode` クラスは、X++ におけるリフレクション機能の中心です。</span><span class="sxs-lookup"><span data-stu-id="4902a-951">The `TreeNode` class is the center of reflection functionality in X++.</span></span> <span data-ttu-id="4902a-952">`TreeNode` クラスとそのメソッドは、C\# が使用する .NET Framework において `System.Reflection` 名前空間と比較できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-952">The `TreeNode` class and its methods can be compared to the `System.Reflection` namespace in the .NET Framework that C\# uses.</span></span>

<span data-ttu-id="4902a-953">次のテーブルに、C\# コードを書くときに利用できるいくつかのクラスを示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-953">The following table lists several classes that are available to you when you write C\# code.</span></span> <span data-ttu-id="4902a-954">これらは、.NET Framework クラスです。</span><span class="sxs-lookup"><span data-stu-id="4902a-954">These are .NET Framework classes.</span></span> <span data-ttu-id="4902a-955">このテーブルでは、すべての C\# クラスは、特に指定のない限り `System.Reflection` 名前空間にあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-955">For this table, all C\# classes are in the `System.Reflection` namespace unless otherwise specified.</span></span> <span data-ttu-id="4902a-956">各行では、対応するクラスまたはクラス メンバーを示し、X++ コードを記述する際に利用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-956">Each row shows the corresponding class, or class member, that is available to you when your write X++ code.</span></span>

|<span data-ttu-id="4902a-957">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-957">X++</span></span>|<span data-ttu-id="4902a-958">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-958">C#</span></span>|<span data-ttu-id="4902a-959">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-959">Comments</span></span>|
|---|---|---|
| `TreeNode` | `System .Assembly`   | <span data-ttu-id="4902a-960">アセンブリは C\# プログラムがリフレクション情報を収集する必要がある場合に使用する最初のクラスです。</span><span class="sxs-lookup"><span data-stu-id="4902a-960">Assembly is the first class to use when a C\# program must gather reflection information.</span></span> <span data-ttu-id="4902a-961">X++ クラスの静的メソッド `TreeNode` は、X++ におけるリフレクションの開始点です。</span><span class="sxs-lookup"><span data-stu-id="4902a-961">Static methods on the X++ class `TreeNode` are the starting point for reflection in X++.</span></span>    |
| `TreeNode` | `System .Type`       | <span data-ttu-id="4902a-962">`TreeNode` のインスタンス メソッドは、`System.Type` のインスタンス メソッドに対応します。</span><span class="sxs-lookup"><span data-stu-id="4902a-962">Instance methods on `TreeNode` correspond to instance methods on `System.Type`.</span></span>                |
| `TreeNode .AOTgetSource`         | `MethodInfo`         | <span data-ttu-id="4902a-963">`AOTgetSource` メソッドは、いくつかの情報を 1 つの文字列でまとめて返します。</span><span class="sxs-lookup"><span data-stu-id="4902a-963">The `AOTgetSource` method returns several pieces of information together in one string.</span></span> <span data-ttu-id="4902a-964">これには、メソッドの X++ ソース コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4902a-964">This includes the X++ source code in the method.</span></span> <span data-ttu-id="4902a-965">対照的に、`MethodInfo` には各情報に対する個別のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-965">In contrast, `MethodInfo` has a separate member for each piece of information.</span></span>                  |
| <span data-ttu-id="4902a-966">`TreeNode .AOTfirstChild` `TreeNode .AOTnextSibling` `TreeNode .AOTiterator` `AOTiterator`</span><span class="sxs-lookup"><span data-stu-id="4902a-966">`TreeNode .AOTfirstChild` `TreeNode .AOTnextSibling` `TreeNode .AOTiterator` `AOTiterator`</span></span> | <span data-ttu-id="4902a-967">MethodInfo\[\] (配列)</span><span class="sxs-lookup"><span data-stu-id="4902a-967">MethodInfo\[\] (an array)</span></span>   | <span data-ttu-id="4902a-968">C\# では、`System.Type` の `GetMethods` メソッドは MethodInfo オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="4902a-968">In C\#, the `GetMethods` method on `System.Type` returns an array of MethodInfo objects.</span></span> <span data-ttu-id="4902a-969">インデクサーをインクリメントする一般的な手法により、配列の間をループことができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-969">You can loop through the array by the common technique of incrementing an indexer.</span></span> <span data-ttu-id="4902a-970">対照的に、X++ モデルは、AOT のツリー コントロールを移動するためのものです。</span><span class="sxs-lookup"><span data-stu-id="4902a-970">In contrast, the X++ model is to navigate the tree control of the AOT.</span></span> <span data-ttu-id="4902a-971">`AOTfirstChild` および `AOTnextSibling` の `TreeNode` メソッドは、ナビゲーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="4902a-971">The `TreeNode` methods of `AOTfirstChild` and `AOTnextSibling` accomplish the navigation.</span></span> <span data-ttu-id="4902a-972">同等の代替として X++ `AOTiterator` クラスは、AOT のツリー コントロールをナビゲートするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-972">As an equivalent alternative, the X++ `AOTiterator` class is designed to navigate the tree control of the AOT.</span></span> <span data-ttu-id="4902a-973">クラス ノードは、いくつかのメソッド ノードの親です。</span><span class="sxs-lookup"><span data-stu-id="4902a-973">A class node is the parent over several method nodes.</span></span> <span data-ttu-id="4902a-974">`AOTiterator` は、子ノードを順番に進み、それぞれ別の `TreeNode` インスタンスとして返します。</span><span class="sxs-lookup"><span data-stu-id="4902a-974">The `AOTiterator` steps through child nodes, returning each as another `TreeNode` instance.</span></span> <span data-ttu-id="4902a-975">`AOTparent` および `AOTprevious` という名前の追加のリソース `TreeNode` メソッド。</span><span class="sxs-lookup"><span data-stu-id="4902a-975">Additional resources the `TreeNode` methods that are named `AOTparent` and `AOTprevious`.</span></span> |
| <span data-ttu-id="4902a-976">`TreeNode .AOTgetProperty` `TreeNode .AOTgetProperties` `TreeNode .AOTname`</span><span class="sxs-lookup"><span data-stu-id="4902a-976">`TreeNode .AOTgetProperty` `TreeNode .AOTgetProperties` `TreeNode .AOTname`</span></span>                | `PropertyInfo`       | <span data-ttu-id="4902a-977">X++ では、`AOTgetProperties` メソッドは `TreeNode` のすべてのプロパティの名前と値のペアを含む長い文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4902a-977">In X++, the `AOTgetProperties` method returns a long string that contains name-value pairs for all the properties of the `TreeNode`.</span></span> <span data-ttu-id="4902a-978">`AOTname` メソッドは、名プロパティの値のみを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4902a-978">The `AOTname` method returns a string that contains only the value for the name property.</span></span>                  |
| <span data-ttu-id="4902a-979">`TreeNode .AOTsave` `TreeNode .AOTinsert`</span><span class="sxs-lookup"><span data-stu-id="4902a-979">`TreeNode .AOTsave` `TreeNode .AOTinsert`</span></span>                     | <span data-ttu-id="4902a-980">`System .Reflection .Emit` (クラスの名前空間)</span><span class="sxs-lookup"><span data-stu-id="4902a-980">`System .Reflection .Emit` (namespace of classes)</span></span> | <span data-ttu-id="4902a-981">`AOTsave` メソッドは、X++ コード内の `TreeNode` オブジェクトからの変更を AOT に適用し、変更は維持されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-981">The `AOTsave` method applies changes from a `TreeNode` object in your X++ code to the AOT, and the changes are persisted.</span></span> <span data-ttu-id="4902a-982">大規模なコード サンプルについては、TreeNode.AOTsave メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-982">For a large code sample, see TreeNode.AOTsave Method.</span></span>       |

### <a name="comparison-classes-about-file-io"></a><span data-ttu-id="4902a-983">比較: ファイル IO に関するクラス</span><span class="sxs-lookup"><span data-stu-id="4902a-983">Comparison: Classes about File IO</span></span>
<span data-ttu-id="4902a-984">ファイル入出力 (IO) 操作を実行するクラスはいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-984">There are several classes that perform file input and output (IO) operations.</span></span> <span data-ttu-id="4902a-985">C\# で使用されている .NET Framework では、これらのクラスに対応するものが `System.IO` 名前空間に配置されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-985">In the .NET Framework that is used in C\#, the counterparts to these classes reside in the `System.IO` namespace.</span></span>

<span data-ttu-id="4902a-986">次のテーブルは、`System.IO` 名前空間にある C\# のいくつかの .NET Framework クラスをリストしたものです。</span><span class="sxs-lookup"><span data-stu-id="4902a-986">The following table lists several .NET Framework classes for C\# that are in the `System.IO` namespace.</span></span> <span data-ttu-id="4902a-987">テーブルの各行は、.NET Framework クラスに最も対応する方法または X++ クラスを示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-987">Each row in the table shows the X++ class or method that best corresponds to the .NET Framework class.</span></span>

|<span data-ttu-id="4902a-988">X++</span><span class="sxs-lookup"><span data-stu-id="4902a-988">X++</span></span>|<span data-ttu-id="4902a-989">C#</span><span class="sxs-lookup"><span data-stu-id="4902a-989">C#</span></span>|<span data-ttu-id="4902a-990">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-990">Comments</span></span>|
|---|---|---|
| `BinaryIo`| <span data-ttu-id="4902a-991">`FileStream` `BinaryReader` `BinaryWriter`</span><span class="sxs-lookup"><span data-stu-id="4902a-991">`FileStream` `BinaryReader` `BinaryWriter`</span></span>
| <span data-ttu-id="4902a-992">抽象クラス `Io` から拡張された `BinaryIo` 等の X++ クラスはストリームとして機能し、そのストリームのリーダーおよびライターとしても機能します。</span><span class="sxs-lookup"><span data-stu-id="4902a-992">X++ classes such as `BinaryIo` that extend from the abstract class `Io` serve as a stream, and they also serve as a reader and writer for that stream.</span></span> <span data-ttu-id="4902a-993">C# では、ストリームはより具体的な読み取りおよび書き込みメソッドがあるクラスからの別のクラスです。</span><span class="sxs-lookup"><span data-stu-id="4902a-993">In C# the stream is a separate class the from the class that has the more specific read and write methods.</span></span>|
| `TextBuffer`| `MemoryStream`| <span data-ttu-id="4902a-994">これらのクラスにはメモリ内バッファがあり、メソッドの中には、バッファをハードディスク上のファイルであるかのように扱うものがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-994">These classes contain an in-memory buffer, and some of the methods treat the buffer as if it were a file on the hard disk.</span></span>|
| <span data-ttu-id="4902a-995">WINAPI::createDirectory WINAPI::folderExists WINAPI::removeDirectory</span><span class="sxs-lookup"><span data-stu-id="4902a-995">WINAPI::createDirectory WINAPI::folderExists WINAPI::removeDirectory</span></span>| <span data-ttu-id="4902a-996">`Directory` `DirectoryInfo` `Path`</span><span class="sxs-lookup"><span data-stu-id="4902a-996">`Directory` `DirectoryInfo` `Path`</span></span>| <span data-ttu-id="4902a-997">X++ はディレクトリを含む多くの基本オペレーティング システム関数の `WINAPI` クラス内で静的メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-997">X++ can use static methods in the `WINAPI` class for many basic operating system functions that involve directories.</span></span>|
| <span data-ttu-id="4902a-998">WINAPI::getDriveType</span><span class="sxs-lookup"><span data-stu-id="4902a-998">WINAPI::getDriveType</span></span>| <span data-ttu-id="4902a-999">`DriveInfo` `DriveType`</span><span class="sxs-lookup"><span data-stu-id="4902a-999">`DriveInfo` `DriveType`</span></span>| <span data-ttu-id="4902a-1000">これらのクラスとメソッドは、ドライブ関連の情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1000">These classes and methods are used to obtain drive related information.</span></span>|
| <span data-ttu-id="4902a-1001">WINAPI::copyFile WINAPI::createFile WINAPI::deleteFile WINAPI::fileExists</span><span class="sxs-lookup"><span data-stu-id="4902a-1001">WINAPI::copyFile WINAPI::createFile WINAPI::deleteFile WINAPI::fileExists</span></span>| <span data-ttu-id="4902a-1002">`File` `FileAttributes` `FileInfo`</span><span class="sxs-lookup"><span data-stu-id="4902a-1002">`File` `FileAttributes` `FileInfo`</span></span>| <span data-ttu-id="4902a-1003">X++ はファイルを含む多くの基本オペレーティング システム関数の `WINAPI` クラスで内で静的メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1003">X++ can use static methods in the `WINAPI` class for many basic operating system functions that involve files.</span></span>|
| <span data-ttu-id="4902a-1004">`CommaIo` `Comma7Io`</span><span class="sxs-lookup"><span data-stu-id="4902a-1004">`CommaIo` `Comma7Io`</span></span>| <span data-ttu-id="4902a-1005">(対応するクラスはありません。)</span><span class="sxs-lookup"><span data-stu-id="4902a-1005">(No corresponding class.)</span></span>| <span data-ttu-id="4902a-1006">これらの X++ クラスは、Microsoft Excel がインポートできるファイルを生成できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1006">These X++ classes can generate files that Microsoft Excel can import.</span></span> <span data-ttu-id="4902a-1007">X++ で、Excel との追加のインタラクションに <a href="http://epplus.codeplex.com/">EPPlus</a>ライブラリ リファレンスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1007">In X++ an <a href="http://epplus.codeplex.com/">EPPlus</a> library reference is available for additional interaction with Excel.</span></span>|
| <span data-ttu-id="4902a-1008">`AsciiIo` `TextIo`</span><span class="sxs-lookup"><span data-stu-id="4902a-1008">`AsciiIo` `TextIo`</span></span>| <span data-ttu-id="4902a-1009">`FileStream` `TextReader` `TextWriter`</span><span class="sxs-lookup"><span data-stu-id="4902a-1009">`FileStream` `TextReader` `TextWriter`</span></span>| <span data-ttu-id="4902a-1010">これらのクラスはさまざまなコード ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1010">These classes use different code pages.</span></span>|
| `Io`| <span data-ttu-id="4902a-1011">`Stream` `StreamReader` `StreamWriter` `FileStream`</span><span class="sxs-lookup"><span data-stu-id="4902a-1011">`Stream` `StreamReader` `StreamWriter` `FileStream`</span></span>| <span data-ttu-id="4902a-1012">これらは、他のクラスが拡張する基本クラスとしてよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1012">These are often used as base classes that other classes extend.</span></span>|
| <span data-ttu-id="4902a-1013">`CodeAccessPermission` `FileIoPermission`</span><span class="sxs-lookup"><span data-stu-id="4902a-1013">`CodeAccessPermission` `FileIoPermission`</span></span>| <span data-ttu-id="4902a-1014">`System.Security` `.CodeAccessPermission` 名前空間 `System.Security.Permissions` には、次のクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1014">`System.Security` `.CodeAccessPermission` The namespace `System.Security.Permissions` includes the following classes:</span></span><ul><li>`CodeAccessSecurityAttribute`</li><li>`FileIOPermissionAttribute`</li><li>`FileIOPermission`</li><li>`FileIOPermissionAccess`</li></ul>| <span data-ttu-id="4902a-1015">`assert`、`demand`、および `revertAssert` の概念とメソッドは両方の言語に適用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1015">The concepts and methods of `assert`, `demand`, and `revertAssert` apply to both languages.</span></span> <span data-ttu-id="4902a-1016">ただし、C# で利用可能な `deny` および `revertDeny` メソッドは、X++ では使用できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1016">However, the `deny` and `revertDeny` methods that are available in C# are not available in X++.</span></span>|

## <a name="x-ansi-sql-comparison-sql-select"></a><span data-ttu-id="4902a-1017">X++、ANSI SQL 比較: SQL の選択</span><span class="sxs-lookup"><span data-stu-id="4902a-1017">X++, ANSI SQL Comparison: SQL Select</span></span>
<span data-ttu-id="4902a-1018">X++ では、SQL **select** ステートメントの構文は、米国規格協会 (ANSI) の仕様とは異なります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1018">In X++, the SQL **select** statement syntax differs from the American National Standards Institute (ANSI) specification.</span></span>

### <a name="single-table-select"></a><span data-ttu-id="4902a-1019">1 つのテーブル選択</span><span class="sxs-lookup"><span data-stu-id="4902a-1019">Single Table Select</span></span>

<span data-ttu-id="4902a-1020">次のテーブルで、X++ SQL および ANSI SQLの select ステートメントの相違点について説明します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1020">The following table lists differences between the select statements of X++ SQL and ANSI SQL.</span></span>

|<span data-ttu-id="4902a-1021">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-1021">Feature</span></span>|<span data-ttu-id="4902a-1022">X++ SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1022">X++ SQL</span></span>|<span data-ttu-id="4902a-1023">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1023">ANSI SQL</span></span>|<span data-ttu-id="4902a-1024">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-1024">Comments</span></span>|
|---|---|---|---|
| <span data-ttu-id="4902a-1025"><strong>from</strong> 句のテーブル名。</span><span class="sxs-lookup"><span data-stu-id="4902a-1025">Table name on the <strong>from</strong> clause.</span></span>| <span data-ttu-id="4902a-1026"><strong>from</strong> 句は、`CustTable` テーブルからなど、テーブルから宣言されているレコード バッファー インスタンスを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1026">The <strong>from</strong> clause lists a record buffer instance that is declared from a table, such as from the `CustTable` table.</span></span>| <span data-ttu-id="4902a-1027"><strong>from</strong> 句は、バッファーの名前ではなく、テーブル名を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1027">The <strong>from</strong> clause lists a table name, not the name of a buffer.</span></span>| <span data-ttu-id="4902a-1028">レコード バッファには、`xRecord`class が X++ のすべてのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1028">The record buffer has all the methods that the `xRecord`class has in X++.</span></span>|
| <span data-ttu-id="4902a-1029">order by 句と <strong>where</strong> 句の構文の順序。</span><span class="sxs-lookup"><span data-stu-id="4902a-1029">Syntax sequence of the order by versus <strong>where</strong> clauses.</span></span>| <span data-ttu-id="4902a-1030">order by 句は、<strong>where</strong> 句の前に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1030">The order by clause must appear before the <strong>where</strong> clause.</span></span> <span data-ttu-id="4902a-1031">order by 句は、<strong>from</strong> 句または <strong>join</strong> 句の後に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1031">The order by clause must appear after the <strong>from</strong> or <strong>join</strong> clause.</span></span> <span data-ttu-id="4902a-1032">group by 句は、次の順序で同じ構文位置決めルールに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1032">The group by clause must follow the same syntax positioning rules that the order by follows.</span></span>| <span data-ttu-id="4902a-1033">order by 句は、<strong>where</strong> 句の後に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1033">The order by clause must appear after the <strong>where</strong> clause.</span></span> <span data-ttu-id="4902a-1034"><strong>where</strong> 句は、<strong>from</strong> 句または <strong>join</strong> 句の後に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1034">The <strong>where</strong> clause must appear after the <strong>from</strong> or <strong>join</strong> clause.</span></span>| <span data-ttu-id="4902a-1035">X++ と ANSI SQL の両方では、<strong>from</strong> および <strong>join</strong> 句が order by および <strong>where</strong> 句の前に表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1035">In both X++ and ANSI SQL, the <strong>from</strong> and <strong>join</strong> clauses must appear before the order by and <strong>where</strong> clauses.</span></span>|
| <span data-ttu-id="4902a-1036">条件の否定。</span><span class="sxs-lookup"><span data-stu-id="4902a-1036">Condition negation.</span></span>| <span data-ttu-id="4902a-1037">感嘆符 ('!') は 否定を示すために使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1037">The exclamation mark ('!') is used for negation.</span></span>| <span data-ttu-id="4902a-1038"><strong>not</strong> キーワードは、否定を示すために使用します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1038">The <strong>not</strong> keyword is used for negation.</span></span>| <span data-ttu-id="4902a-1039">X++ は構文 !like はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1039">X++ does not support the syntax !like.</span></span> <span data-ttu-id="4902a-1040">代わりに、! を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1040">Instead, you must apply the !</span></span> <span data-ttu-id="4902a-1041">演算子を句に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1041">operator to a clause.</span></span>|
| <span data-ttu-id="4902a-1042"><strong>like</strong> 演算子用ワイルドカード文字。</span><span class="sxs-lookup"><span data-stu-id="4902a-1042">Wildcard characters for the <strong>like</strong> operator.</span></span>|<span data-ttu-id="4902a-1043">0 から多数 - アスタリスク (「\*」)</span><span class="sxs-lookup"><span data-stu-id="4902a-1043">0 to many – Asterisk ('\*')</span></span><br><span data-ttu-id="4902a-1044">1 のみ – 疑問符 ('?')</span><span class="sxs-lookup"><span data-stu-id="4902a-1044">Exactly 1 – Question mark ('?')</span></span>|<span data-ttu-id="4902a-1045">0 から多数 - パーセントを記号 (「%」)</span><span class="sxs-lookup"><span data-stu-id="4902a-1045">0 to many – Percent sign ('%')</span></span><br><span data-ttu-id="4902a-1046">1 のみ – アンダーバー ('_')</span><span class="sxs-lookup"><span data-stu-id="4902a-1046">Exactly 1 – Underbar ('_')</span></span>| |
| <span data-ttu-id="4902a-1047"><strong>where</strong> 句における論理演算子。</span><span class="sxs-lookup"><span data-stu-id="4902a-1047">Logical operators in the <strong>where</strong> clause.</span></span>|<span data-ttu-id="4902a-1048">および – &&</span><span class="sxs-lookup"><span data-stu-id="4902a-1048">And – &&</span></span><br><span data-ttu-id="4902a-1049">または – \|\|</span><span class="sxs-lookup"><span data-stu-id="4902a-1049">Or – \|\|</span></span> |<span data-ttu-id="4902a-1050">および – <strong>および</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-1050">And – <strong>and</strong></span></span><br><span data-ttu-id="4902a-1051">または – <strong>や</strong></span><span class="sxs-lookup"><span data-stu-id="4902a-1051">Or – <strong>or</strong></span></span>| |

### <a name="code-example"></a><span data-ttu-id="4902a-1052">コードの例</span><span class="sxs-lookup"><span data-stu-id="4902a-1052">Code Example</span></span>

<span data-ttu-id="4902a-1053">次のコード例は、前のテーブルの機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-1053">The following code example illustrates features in the previous table.</span></span>
<pre>
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
</pre>
 
### <span data-ttu-id="4902a-1054">X++ SQL キーワード</span><span class="sxs-lookup"><span data-stu-id="4902a-1054">X++ SQL Keywords</span></span>

<span data-ttu-id="4902a-1055">次の X++ SQL キーワードは、ANSI SQL に含まれていないものです。</span><span class="sxs-lookup"><span data-stu-id="4902a-1055">The following X++ SQL keywords are among those that are not part of ANSI SQL:</span></span>
-   <span data-ttu-id="4902a-1056">crosscompany</span><span class="sxs-lookup"><span data-stu-id="4902a-1056">crosscompany</span></span>
-   <span data-ttu-id="4902a-1057">firstonly100</span><span class="sxs-lookup"><span data-stu-id="4902a-1057">firstonly100</span></span>
-   <span data-ttu-id="4902a-1058">forceliterals</span><span class="sxs-lookup"><span data-stu-id="4902a-1058">forceliterals</span></span>
-   <span data-ttu-id="4902a-1059">forcenestedloop</span><span class="sxs-lookup"><span data-stu-id="4902a-1059">forcenestedloop</span></span>
-   <span data-ttu-id="4902a-1060">forceplaceholders</span><span class="sxs-lookup"><span data-stu-id="4902a-1060">forceplaceholders</span></span>
-   <span data-ttu-id="4902a-1061">forceselectorder</span><span class="sxs-lookup"><span data-stu-id="4902a-1061">forceselectorder</span></span>
-   <span data-ttu-id="4902a-1062">validtimestate</span><span class="sxs-lookup"><span data-stu-id="4902a-1062">validtimestate</span></span>

#### <a name="join-clause"></a><span data-ttu-id="4902a-1063">句の結合</span><span class="sxs-lookup"><span data-stu-id="4902a-1063">Join Clause</span></span>

<span data-ttu-id="4902a-1064">次のテーブルで、X++ SQL および ANSI SQLの **結合** キーワードの相違点について説明します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1064">The following table lists differences about the **join** keyword of X++ SQL and ANSI SQL.</span></span>

|<span data-ttu-id="4902a-1065">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-1065">Feature</span></span>|<span data-ttu-id="4902a-1066">X++ SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1066">X++ SQL</span></span>|<span data-ttu-id="4902a-1067">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1067">ANSI SQL</span></span>|<span data-ttu-id="4902a-1068">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-1068">Comments</span></span>|
|---|---|---|---|
| <span data-ttu-id="4902a-1069">列リスト。</span><span class="sxs-lookup"><span data-stu-id="4902a-1069">Columns list.</span></span>                    | <span data-ttu-id="4902a-1070">列リストの列は、**from** 句にリストされているテーブルから取得し、**join** 句のテーブルからは取得しないでください。</span><span class="sxs-lookup"><span data-stu-id="4902a-1070">The columns in the columns list must all come from the table listed in the **from** clause, and not from any table in a **join** clause.</span></span> <span data-ttu-id="4902a-1071">リスト内の列は、テーブル名で修飾することはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1071">Columns in the list cannot be qualified by their table name.</span></span> | <span data-ttu-id="4902a-1072">列リストの列は、**from** または **join** 句の任意のテーブルから取得できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1072">The columns in the columns list can come from any table in the **from** or **join** clauses.</span></span> <span data-ttu-id="4902a-1073">これにより、他のユーザーはそのテーブル名のあるリスト内の列を修飾するときに、コードを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1073">It helps others to maintain your code when you qualify the columns in the list with their table name.</span></span> | <span data-ttu-id="4902a-1074">詳細については、「フィールドでの明細書の選択」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4902a-1074">For more information, see Select Statements on Fields.</span></span>    |
| <span data-ttu-id="4902a-1075">**Join** 句の構文。</span><span class="sxs-lookup"><span data-stu-id="4902a-1075">**Join** clause syntax.</span></span>          | <span data-ttu-id="4902a-1076">**join** 句は **where** 句に従います。</span><span class="sxs-lookup"><span data-stu-id="4902a-1076">The **join** clause follows the **where** clause.</span></span>           | <span data-ttu-id="4902a-1077">**join** 句は、**from** 句のテーブルに従います。</span><span class="sxs-lookup"><span data-stu-id="4902a-1077">The **join** clause follows a table in the **from** clause.</span></span>                    | <span data-ttu-id="4902a-1078">X++ コードの例で、**join** の条件は `SalesPoolId` 値と一致します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1078">In the X++ code example, the **join** criteria is an equality of `SalesPoolId` values.</span></span> |
| <span data-ttu-id="4902a-1079">**内部**キーワード。</span><span class="sxs-lookup"><span data-stu-id="4902a-1079">**Inner** keyword.</span></span>               | <span data-ttu-id="4902a-1080">既定の **結合** モードは内部結合です。</span><span class="sxs-lookup"><span data-stu-id="4902a-1080">The default **join** mode is inner join.</span></span> <span data-ttu-id="4902a-1081">**inner** キーワードがありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1081">There is no **inner** keyword.</span></span>           | <span data-ttu-id="4902a-1082">既定の **結合** モードは内部結合です。</span><span class="sxs-lookup"><span data-stu-id="4902a-1082">The default **join** mode is inner join.</span></span> <span data-ttu-id="4902a-1083">**inner** キーワードは、コードを明確にするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1083">The **inner** keyword is available to make the code explicit.</span></span>      | <span data-ttu-id="4902a-1084">**outer** キーワードは、X++ SQL と ANSI SQL の両方に存在します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1084">The **outer** keyword exists in both X++ SQL and ANSI SQL.</span></span>       |
| <span data-ttu-id="4902a-1085">**左**および**右**キーワード。</span><span class="sxs-lookup"><span data-stu-id="4902a-1085">**Left** and **right** keywords.</span></span> | <span data-ttu-id="4902a-1086">**left** および **right** キーワードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1086">The **left** and **right** keywords are not available.</span></span> <span data-ttu-id="4902a-1087">すべての結合が残されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1087">All joins are left.</span></span>        | <span data-ttu-id="4902a-1088">**left** および **right** キーワードは、**join** キーワードを変更するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1088">The **left** and **right** keywords are available to modify the **join** keyword.</span></span>     | <span data-ttu-id="4902a-1089">コメントはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1089">No comments.</span></span>                 |
| <span data-ttu-id="4902a-1090">等式演算子。</span><span class="sxs-lookup"><span data-stu-id="4902a-1090">Equality operator.</span></span>               | <span data-ttu-id="4902a-1091">二重等号演算子 ('`==`') は、2 つの値の等価性をテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1091">The double equal sign operator ('`==`') is used to test for the equality of two values.</span></span>  | <span data-ttu-id="4902a-1092">一重等号演算子 ('`=`') は、2 つの値の等価性をテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1092">The single equal sign operator ('`=`') is used to test for the equality of two values.</span></span>                      | <span data-ttu-id="4902a-1093">コメントはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1093">No comments.</span></span>                 |

### <a name="code-example"></a><span data-ttu-id="4902a-1094">コードの例</span><span class="sxs-lookup"><span data-stu-id="4902a-1094">Code Example</span></span>

<span data-ttu-id="4902a-1095">次のコード例は、X++ SQL の **join** 構文を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-1095">The following code example illustrates the **join** syntax in X++ SQL.</span></span>
<pre>
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
</pre>
 
### <span data-ttu-id="4902a-1096">集計フィールド</span><span class="sxs-lookup"><span data-stu-id="4902a-1096">Aggregate Fields</span></span>

<span data-ttu-id="4902a-1097">次のテーブルは、**選択** 列リストの集計フィールドが X++ SQL と ANSI SQL の間でどのように参照されるかの相違点を示しています。</span><span class="sxs-lookup"><span data-stu-id="4902a-1097">The following table lists some differences in how aggregate fields in the **select** column list are referenced between X++ SQL and ANSI SQL.</span></span> <span data-ttu-id="4902a-1098">集計フィールドとは、**合計**または**平均**などの機能によって派生したものです。</span><span class="sxs-lookup"><span data-stu-id="4902a-1098">Aggregate fields are those that are derived by functions such as **sum** or **avg**.</span></span>

|<span data-ttu-id="4902a-1099">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-1099">Feature</span></span>|<span data-ttu-id="4902a-1100">X++ SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1100">X++ SQL</span></span>|<span data-ttu-id="4902a-1101">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1101">ANSI SQL</span></span>|<span data-ttu-id="4902a-1102">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-1102">Comments</span></span>|
|---|---|---|---|
| <span data-ttu-id="4902a-1103">集計フィールド名エイリアス。</span><span class="sxs-lookup"><span data-stu-id="4902a-1103">Aggregate field name alias.</span></span> | <span data-ttu-id="4902a-1104">集計値は、集計されたフィールドにあります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1104">The aggregate value is in the field that was aggregated.</span></span> | <span data-ttu-id="4902a-1105">**as** キーワードを使用すると、名前エイリアス内の集計フィールドをタグ付けすることができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1105">You can use the **as** keyword to tag an aggregate field with a name alias.</span></span> <span data-ttu-id="4902a-1106">エイリアスは、以降のコードで参照される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4902a-1106">The alias can be referenced in subsequent code.</span></span> | <span data-ttu-id="4902a-1107">詳細については、「集計関数: X++ および SQL の差異」を参照してください</span><span class="sxs-lookup"><span data-stu-id="4902a-1107">For more information, see Aggregate Functions: Differences Between X++ and SQL</span></span> |

### <a name="code-example"></a><span data-ttu-id="4902a-1108">コードの例</span><span class="sxs-lookup"><span data-stu-id="4902a-1108">Code Example</span></span>

<span data-ttu-id="4902a-1109">次のコード例では、情報メソッドの呼び出しが集計フィールドを参照する方法を示しています (`tPurchLine.QtyOrdered` を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="4902a-1109">In the following code example, the call to the info method illustrates the way to reference aggregate fields (see `tPurchLine.QtyOrdered`).</span></span>

<pre>
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
</pre>

### <a name="other-differences"></a><span data-ttu-id="4902a-1110">その他の違い</span><span class="sxs-lookup"><span data-stu-id="4902a-1110">Other Differences</span></span>

<span data-ttu-id="4902a-1111">次のテーブルに、X++ SQL および ANSI SQLの **select** ステートメントの相違点を示します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1111">The following table lists other differences of the **select** statement between the X++ SQL and ANSI SQL.</span></span>

|<span data-ttu-id="4902a-1112">機能</span><span class="sxs-lookup"><span data-stu-id="4902a-1112">Feature</span></span>|<span data-ttu-id="4902a-1113">X++ SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1113">X++ SQL</span></span>|<span data-ttu-id="4902a-1114">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="4902a-1114">ANSI SQL</span></span>|<span data-ttu-id="4902a-1115">コメント</span><span class="sxs-lookup"><span data-stu-id="4902a-1115">Comments</span></span>|
|---|---|---|---|
|<span data-ttu-id="4902a-1116">**having** キーワード。</span><span class="sxs-lookup"><span data-stu-id="4902a-1116">The **having** keyword.</span></span>|<span data-ttu-id="4902a-1117">**having** キーワードがありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1117">There is no **having** keyword.</span></span>|<span data-ttu-id="4902a-1118">**having** キーワードを使用すると、group by 句によって生成された行のフィルター条件を指できます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1118">The **having** keyword enables you to specify filter criteria for rows that are generated by the group by clause.</span></span>|<span data-ttu-id="4902a-1119">コメントはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1119">No comments.</span></span>|
|<span data-ttu-id="4902a-1120">null の結果。</span><span class="sxs-lookup"><span data-stu-id="4902a-1120">Null results.</span></span>|<span data-ttu-id="4902a-1121">**while** select ステートメントで、**where** 句がすべての行を除外する場合、それをレポートする特別なカウント行は返されません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1121">In a **while** select statement, if the **where** clause filters out all rows, no special count row is returned to report that.</span></span>|<span data-ttu-id="4902a-1122">**select** で、**where** 句がすべての行を除外する場合、特別なカウント行が返されます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1122">In a **select**, if the **where** clause filters out all rows, a special count row is returned.</span></span> <span data-ttu-id="4902a-1123">カウント値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="4902a-1123">The count value is 0.</span></span>|<span data-ttu-id="4902a-1124">コメントはありません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1124">No comments.</span></span>|
|<span data-ttu-id="4902a-1125">戻された行を移動するためのカーソル。</span><span class="sxs-lookup"><span data-stu-id="4902a-1125">Cursors for navigating returned rows.</span></span>|<span data-ttu-id="4902a-1126">while select 文は、カーソル機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1126">The while select statement provides cursor functionality.</span></span> <span data-ttu-id="4902a-1127">代わりに、**next** キーワードを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1127">The alternative is to use the **next** keyword.</span></span>|<span data-ttu-id="4902a-1128">**select** ステートメントから戻される行間ループのために、**cursor** を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="4902a-1128">You can declare a **cursor** for looping through the rows that are returned from a **select** statement.</span></span>||
|<span data-ttu-id="4902a-1129">**From** 句。</span><span class="sxs-lookup"><span data-stu-id="4902a-1129">**From** clause.</span></span>|<span data-ttu-id="4902a-1130">列がリストされず、1 つのテーブルだけが参照される場合、**from** キーワードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="4902a-1130">The **from** keyword is optional when no columns are listed and only one table is referenced.</span></span> <span data-ttu-id="4902a-1131">次の 2 つの構文オプションは同等です。</span><span class="sxs-lookup"><span data-stu-id="4902a-1131">The following two syntax options are equivalent:</span></span> <br>`select \* from tCustTable;` <br>`select tCustTable;`|<span data-ttu-id="4902a-1132">**選択**ステートメントは、**from** 句が使用されていない限り、テーブルから読み取ることはできません。</span><span class="sxs-lookup"><span data-stu-id="4902a-1132">A **select** statement cannot read from a table unless the **from** clause is used.</span></span>|<span data-ttu-id="4902a-1133">X++ SQL では、シンプルな**選択**ステートメントが返された最初の行でテーブル バッファ変数を入力します。</span><span class="sxs-lookup"><span data-stu-id="4902a-1133">In X++ SQL, the simple **select** statement fills the table buffer variable with the first row that was returned.</span></span> <span data-ttu-id="4902a-1134">これは、次のコード フラグメントによって示されています。</span><span class="sxs-lookup"><span data-stu-id="4902a-1134">This is illustrated by the following code fragment:</span></span> <br>`select \* from tCustTable;` <br>`info(tCustTable.Name);`|


