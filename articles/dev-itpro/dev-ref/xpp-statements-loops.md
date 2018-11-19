---
title: "X++ ステートメント、ループ、および例外処理"
description: "このトピックでは、X++ の構文、ループ、および例外処理について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 10/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150213
ms.assetid: 16b30ff1-bb31-4f9d-8105-c73abd2455f6
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 0eb1645c0f17456aec645420516f7bd25263eba8
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="x-statements-loops-and-exception-handling"></a><span data-ttu-id="a9e0a-103">X++ ステートメント、ループ、および例外処理</span><span class="sxs-lookup"><span data-stu-id="a9e0a-103">X++ statements, loops, and exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9e0a-104">このトピックでは、X++ の構文、ループ、および例外処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-104">This topic describes statements, loops, and exception handling in X++.</span></span>

<a name="comments"></a><span data-ttu-id="a9e0a-105">コメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-105">Comments</span></span>
--------

<span data-ttu-id="a9e0a-106">コードにコメントを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-106">It's a good practice to add comments to your code.</span></span> <span data-ttu-id="a9e0a-107">コメントは、プログラムを読みやすく、またわかりやすくします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-107">Comments make a program easier to read and understand.</span></span> <span data-ttu-id="a9e0a-108">コメントは、プログラムをコンパイルする際には無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-108">Comments are ignored when the program is compiled.</span></span> <span data-ttu-id="a9e0a-109">コメントには、**//** スタイルまたは **/** スタイルのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-109">Your comments can use either the **//** style or the **/** style.</span></span> <span data-ttu-id="a9e0a-110">ただし、ベスト プラクティスは、コメント、および複数行コメントの**//** スタイルを使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-110">However, a best practice is to use the **//** style for comments, and even for multiline comments.</span></span>

    // This is an example of a comment.
    /* Here is another example of a comment. */

## <a name="conditional-statements-if-ifelse-switch-and-ternary-operator-"></a><span data-ttu-id="a9e0a-111">条件付きステートメント: if、if...else、switch、および 3 項演算子 (?) です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-111">Conditional statements: if, if...else, switch, and ternary operator (?)</span></span>
<span data-ttu-id="a9e0a-112">条件付きステートメントは、**if**、**if**...**else**、**switch**、および 3 項演算子 (**?**) です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-112">The conditional statements are **if**, **if**...**else**, **switch**, and the ternary operator (**?**).</span></span> <span data-ttu-id="a9e0a-113">条件付きステートメントを使用して、コードのブロックを実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-113">You use conditional statements to specify whether a block of code is executed.</span></span> <span data-ttu-id="a9e0a-114">異なる条件文は、異なる状況において利点を提供する。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-114">Different conditional statements offer advantages in different situations.</span></span>

### <a name="if-and-ifelse-statements"></a><span data-ttu-id="a9e0a-115">if および if...else ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-115">if and if...else statements</span></span>

<span data-ttu-id="a9e0a-116">**if** ステートメントは、条件式を評価した後、条件式が **true** として評価された場合にステートメントまたは一連のステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-116">The **if** statement evaluates a conditional expression, and then executes a statement or a set of statements if the conditional expression is evaluated as **true**.</span></span> <span data-ttu-id="a9e0a-117">**else** 句を使用すると、条件が **false** と評価される場合に実行される代替ステートメントまたは一連のステートメントを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-117">You can use the **else** clause to provide an alternative statement or set of statements that is executed if the condition is evaluated as **false**.</span></span> <span data-ttu-id="a9e0a-118">**if**...**else** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-118">Here is the syntax for an **if**...**else** statement:</span></span>

<span data-ttu-id="a9e0a-119">**(** *式* **)** の場合、*明細書* **\[ 他の** *明細書* **\]**</span><span class="sxs-lookup"><span data-stu-id="a9e0a-119">**if (** *expression* **)** *statement* **\[ else** *statement* **\]**</span></span>

<span data-ttu-id="a9e0a-120">この構文では、*ステートメント*の回数は両方とも複合ステートメントとすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-120">In this syntax, both occurrences of *statement* can be compound statements.</span></span> <span data-ttu-id="a9e0a-121">かっこで囲まれた*式* (条件式) は、**true** または **false** として評価される有効な式にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-121">The *expression* in the parentheses (the conditional expression) can be any valid expression that is evaluated as **true** or **false**.</span></span> <span data-ttu-id="a9e0a-122">0 (ゼロ) を除くすべての番号は **true** です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-122">All numbers except 0 (zero) are **true**.</span></span> <span data-ttu-id="a9e0a-123">すべての空でない文字列も **true** です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-123">All non-empty strings are also **true**.</span></span> <span data-ttu-id="a9e0a-124">**if** ステートメントは入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-124">You can nest **if** statements.</span></span> <span data-ttu-id="a9e0a-125">ただし、**if** ステートメントの入れ子が深すぎる場合、**switch** ステートメントを代わりに使用することを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-125">However, if the nesting of **if** statements becomes too deep, you should consider using a **switch** statement instead.</span></span>

#### <a name="examples-of-if-and-ifelse-statements"></a><span data-ttu-id="a9e0a-126">if および if...else ステートメントの例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-126">Examples of if and if...else statements</span></span>

    // if statement
    if(a > 4)
    {
       print a;
    }

    // if... else statement 
    if(a > 4)
    {
       print a;
    }
    else
    {
       print "a is less than or equal to 4";
    }

### <a name="switch-statements"></a><span data-ttu-id="a9e0a-127">switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-127">switch statements</span></span>

<span data-ttu-id="a9e0a-128">**switch** ステートメントは、同じ効果を生み出すために **if** ステートメントを入れ子にする必要がある **if** ステートメントとは異なり、マルチブランチ言語コンストラクトです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-128">The **switch** statement is a multibranch language construct, unlike the **if** statement, where you must nest **if** statements to create the same effect.</span></span> <span data-ttu-id="a9e0a-129">**SWITCH** ステートメントの条件式が評価され、それぞれの Case の値に対してチェックされます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-129">The conditional expression of the **switch** statement is evaluated and checked against each case value.</span></span> <span data-ttu-id="a9e0a-130">大文字と小文字の値は、コンパイラが評価できる定数でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-130">The case values must be constants that the compiler can evaluate.</span></span> <span data-ttu-id="a9e0a-131">ケース定数が**切り替え**式と一致する場合、**case** ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-131">If a case constant matches the **switch** expression, the **case** statement is executed.</span></span> <span data-ttu-id="a9e0a-132">そのケースに**休憩**ステートメントが含まれている場合、プログラムはスイッチからジャンプ アウトします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-132">If the case also contains a **break** statement, the program then jumps out of the switch.</span></span> <span data-ttu-id="a9e0a-133">ケースに**休憩**ステートメントが含まれていない場合、プログラムは継続し、**ケース** ステートメントの次のセットを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-133">If the case doesn't contain a **break** statement, the program continues and executes the next set of **case** statements.</span></span> <span data-ttu-id="a9e0a-134">一致が見つからない場合、**既定**ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-134">If no matches are found, the **default** statement is executed.</span></span> <span data-ttu-id="a9e0a-135">一致するものがなく、**default** ステートメントがない場合、**switch** ステートメント内のステートメントは実行されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-135">If there are no matches and no **default** statement, none of the statements inside the **switch** statement are executed.</span></span> <span data-ttu-id="a9e0a-136">**switch** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-136">Here is the syntax for a **switch** statement:</span></span>

<span data-ttu-id="a9e0a-137">**切り替え (** *式* **) { { ケース } \[ 既定:** *明細書* **\] }**</span><span class="sxs-lookup"><span data-stu-id="a9e0a-137">**switch (** *expression* **) { { case } \[ default:** *statement* **\] }**</span></span>

<span data-ttu-id="a9e0a-138">**case** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-138">Here is the syntax for a **case** statement:</span></span>

<span data-ttu-id="a9e0a-139">**ケース** *式* **{ 、** *式* **} :** *明細書*</span><span class="sxs-lookup"><span data-stu-id="a9e0a-139">**case** *expression* **{ ,** *expression* **} :** *statement*</span></span>

<span data-ttu-id="a9e0a-140">**switch** ステートメントおよび **case** ステートメントの両方の構文で、*ステートメント*があるごとに、かっこ ({}) でブロックを囲むことでステートメントのブロックを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-140">In the syntax for both a **switch** statement and a **case** statement, every occurrence of s*tatement* can be replaced with a block of statements by enclosing the block in braces ({}).</span></span>

#### <a name="examples-of-switch-statements"></a><span data-ttu-id="a9e0a-141">切り替え明細書の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-141">Examples of switch statements</span></span>

    // When the break keyword is used within a switch statement, the execution of 
    // the case branch terminates, and the statement following the 
    // switch is executed as shown in the following example.
    // If the Debtor account number is 1000, the program executes 
    // "do something", and then continues execution after the switch statement.
    switch (Debtor.AccountNo)
    {
        case "1000":
            // do something
            break;
        case "2000":
            // do something else
            break;
        default:
            // default statement
            break;
    }

    // Switch statement example to make the execution drop 
    // through case branches by omitting a break statement. 
    // If x is 10, b is assigned to a, and d is assigned to c, the break 
    // statement is omitted after the case 10: statement. If x is 11, d 
    // is assigned to c. If x is 12, f is assigned to e.
    switch (x)
    {
        case 10:
            a = b;
        case 11:
            c = d;
            break;
        case 12:
            e = f;
            break;
    }

    // If you do not use the break statement, the program flow in the switch
    // statement continues into the next case. Code segments A and B
    // have the same behavior. 
    // Code segment A (break omitted)
    case 13:
    case 17:
    case 21:
    case 500:
        print "g";
        break;
    // Code segment B (the values are comma-delimited)
    case 13, 17, 21, 500;
        print "g";
        break;

    // Break statement example within a while loop. When used within
    // a loop, the loop is terminated and execution continues
    // from the statement following the loop. This works for do... while
    // and for loops as well. 
    var mainMenu = SysDictMenu::newMainMenu();
    var enum = mainMenu.getEnumerator();
    var found = false;
    while (enum.moveNext())
    {
        var menuItem = enum.current();
        if (menuItem.label() == "StringOfInterest")
        {
            found = true;
            break;
        }
    }
    if (found) 
    {
        // do something
    }

### <a name="ternary-operator-"></a><span data-ttu-id="a9e0a-142">三項演算子 (?)</span><span class="sxs-lookup"><span data-stu-id="a9e0a-142">Ternary operator (?)</span></span>

<span data-ttu-id="a9e0a-143">三項演算子 (**?**) は、2 つの式のうちの 1 つに解決される条件文です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-143">The ternary operator (**?**) is a conditional statement that is resolved to one of two expressions.</span></span> <span data-ttu-id="a9e0a-144">結果は、変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-144">The result can be assigned to a variable.</span></span> <span data-ttu-id="a9e0a-145">対照的に、**if** ステートメントはプログラム フローの条件付き分岐を提供しますが、変数に割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-145">By contrast, an **if** statement provides conditional branching of the program flow but can't be assigned to a variable.</span></span> <span data-ttu-id="a9e0a-146">三項演算子の構文を次に示します:</span><span class="sxs-lookup"><span data-stu-id="a9e0a-146">Here is the syntax for the ternary operator:</span></span>

<span data-ttu-id="a9e0a-147">*式1* **?**</span><span class="sxs-lookup"><span data-stu-id="a9e0a-147">*expression1* **?**</span></span> <span data-ttu-id="a9e0a-148">*式2* **:** *式3*</span><span class="sxs-lookup"><span data-stu-id="a9e0a-148">*expression2* **:** *expression3*</span></span>

<span data-ttu-id="a9e0a-149">この構文では、*expression1* は **true** または **false** の値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-149">In this syntax, *expression1* must return a value of **true** or **false**.</span></span> <span data-ttu-id="a9e0a-150">*expression1* が **true** である場合、三項全体の明細書は*式*を返します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-150">If *expression1* is **true**, the whole ternary statement returns *expression2*.</span></span> <span data-ttu-id="a9e0a-151">それ以外の場合、ステートメントは *expression3* を返します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-151">Otherwise, the statement returns *expression3*.</span></span> <span data-ttu-id="a9e0a-152">*expression2* と *expression3* の両方は同じタイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-152">Both *expression2* and *expression3* must have the same type.</span></span>

#### <a name="examples-of-the-ternary-operator-"></a><span data-ttu-id="a9e0a-153">三項演算子 (?) の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-153">Examples of the ternary operator (?)</span></span>

    // Returns one of two strings based on a Boolean return value from a method call. 
    // The Boolean expression indicated whether the CustTable table has a row
    // with a RecId field value of 1. If this Boolean expression is true 
    // (meaning RecId != 0), found is assigned to result. 
    // Otherwise, the alternative not found is assigned to result.
    result = (custTable::find("1").RecId) ? "found" : "not found";

    // An example of a nested ternary statement. 
    // If z is not greater than 1000, the expression is equal to the third 
    // expression and low is printed. If AccountNum is greater than 1000, the second 
    // expression is evaluated, and this also contains a ternary operator. If AccountNum 
    // is greater than 1000 and less than 2000, In interval is printed. If AccountNum is 
    // greater than 1000 and greater than or equal to 2000, Above 2000 is printed.str z = "5";
    print( (z > "1000") ?
             ( (z < "2000") ? "In interval" : "Above 2000")
             : "low");
    ); 

## <a name="exception-handling-throw-trycatch-finally-and-retry"></a><span data-ttu-id="a9e0a-154">例外処理: スロー、トライ、キャッチ、最後に再トライ</span><span class="sxs-lookup"><span data-stu-id="a9e0a-154">Exception handling: throw, try...catch, finally, and retry</span></span>
<span data-ttu-id="a9e0a-155">使用してエラーを処理するには、**throw**、**try**...**catch**、**finally**、および **retry** ステートメントを使用して例外を生成して処理します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-155">You handle errors by using the **throw**, **try**...**catch**, **finally**, and **retry** statements to generate and handle exceptions.</span></span> <span data-ttu-id="a9e0a-156">*例外*はプログラム実行の順序から離れて規制ジャンプします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-156">An *exception* is a regulated jump away from the sequence of program execution.</span></span> <span data-ttu-id="a9e0a-157">プログラムの実行が再開する指示は、**try**...**catch** ブロックとスローされる例外のタイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-157">The instruction where program execution resumes is determined by **try**...**catch** blocks and the type of exception that is thrown.</span></span> <span data-ttu-id="a9e0a-158">例外は**例外**列挙の値で表されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-158">An exception is represented by a value of the **Exception** enumeration.</span></span> <span data-ttu-id="a9e0a-159">多くの場合スローされる 1 つの例外は、**例外::エラー**列挙値です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-159">One exception that is often thrown is the **Exception::error** enum value.</span></span> <span data-ttu-id="a9e0a-160">一般的には、例外がスローされる前に infolog に診断情報を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-160">A common practice is to write diagnostic information to the Infolog before the exception is thrown.</span></span> <span data-ttu-id="a9e0a-161">**Global::error** メソッドは多くの場合、情報ログに診断情報を書き込む最善の方法です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-161">The **Global::error** method is often the best way to write diagnostic information to the Infolog.</span></span> <span data-ttu-id="a9e0a-162">たとえば、メソッドは無効な入力パラメーター値を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-162">For example, your method might receive an input parameter value that isn't valid.</span></span> <span data-ttu-id="a9e0a-163">この場合、メソッドは例外をスローして、このエラー状況を処理するためのロジックを含む **catch** コード ブロックにすぐにコントロールを転送します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-163">In this case, the method can throw an exception to immediately transfer control to a **catch** code block that contains logic for handling this error situation.</span></span> <span data-ttu-id="a9e0a-164">例外がスローされる場合、コントロールを受け取る **Catch** ブロックの場所を必ずしも知る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-164">You don't necessarily have to know the location of the **catch** block that will receive control when the exception is thrown.</span></span>

### <a name="throw-statements"></a><span data-ttu-id="a9e0a-165">throw ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-165">throw statements</span></span>

<span data-ttu-id="a9e0a-166">**Exception** 列挙値をスローするには、**throw** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-166">You use the **throw** keyword to throw an **Exception** enum value.</span></span> <span data-ttu-id="a9e0a-167">たとえば、次のステートメントは例外エラーをスローします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-167">For example, the following statement throws an error exception.</span></span>

    throw Exception::error;

<span data-ttu-id="a9e0a-168">列挙値をスローするのではなく、**Global::error** メソッドの出力を**スロー**のオペランドとして使用することがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-168">Instead of throwing an enum value, a best practice is to use the output of the **Global::error** method as the operand for **throw**.</span></span>

    throw Global::error("The parameter value is invalid.");

<span data-ttu-id="a9e0a-169">**Global::error** メソッドは、対応するテキストにラベルを自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-169">The **Global::error** method can automatically convert a label into the corresponding text.</span></span> <span data-ttu-id="a9e0a-170">この機能は、ローカライズ可能なコードを書くのに役立ちます。 </span><span class="sxs-lookup"><span data-stu-id="a9e0a-170">This functionality helps you write code that can be localized more easily.</span></span>

    throw Global::error("@SYS98765");

<span data-ttu-id="a9e0a-171">**Global** クラスの静的メソッドは、**Global::** プレフィックスなしで呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-171">The static methods on the **Global** class can be called without the **Global::** prefix.</span></span> <span data-ttu-id="a9e0a-172">たとえば、**Global::error** メソッドは、次のように呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-172">For example, the **Global::error** method can be called like this.</span></span>

    error("My message.");

### <a name="try-catch-finally-and-retry-statements"></a><span data-ttu-id="a9e0a-173">try ステートメント、catch ステートメント、最後に retry ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-173">try, catch, finally, and retry statements</span></span>

<span data-ttu-id="a9e0a-174">例外がスローされると、その例外は、もっとも内側の <strong>try</strong> ブロックの <strong>キャッチ</strong> リストによって最初に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-174">When an exception is thrown, it's first processed through the <strong>catch</strong> list of the innermost <strong>try</strong> block.</span></span> <span data-ttu-id="a9e0a-175">スローされている例外の種類を処理する <strong>catch</strong> ブロックが見つかった場合、プログラム コントロールはその <strong>キャッチ</strong> ブロックにジャンプします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-175">If a <strong>catch</strong> block is found that handles the kind of exception that is being thrown, program control jumps to that <strong>catch</strong> block.</span></span> <span data-ttu-id="a9e0a-176"><strong>catch</strong> リストに例外を指定するブロックがない場合は、システムは、次の一番内側の <strong>try</strong> ブロックの<strong>catch</strong> リストに例外を渡します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-176">If the <strong>catch</strong> list has no block that specifies the exception, the system passes the exception to the <strong>catch</strong> list of the next-innermost <strong>try</strong> block.</span></span> <span data-ttu-id="a9e0a-177"><strong>catch</strong> ステートメントは、コードに表示されているのと同じ順序で処理されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-177">The <strong>catch</strong> statements are processed in the same sequence as they appear in the code.</span></span> <span data-ttu-id="a9e0a-178">最初の <strong>catch</strong> ステートメントで <strong>Exception::Error</strong> 列挙値を処理することが一般的です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-178">It's a common practice to have the first <strong>catch</strong> statement handle the <strong>Exception::Error</strong> enum value.</span></span> <span data-ttu-id="a9e0a-179">1 つの方法は、最後の <strong>catch</strong> ステートメントの例外タイプを未指定のままにすることです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-179">One strategy is to have the last <strong>catch</strong> statement leave the exception type unspecified.</span></span> <span data-ttu-id="a9e0a-180">この場合、前回の <strong>catch</strong> ステートメントは、前のいずれかの <strong>catch</strong> ステートメントで処理されていないすべての例外を処理します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-180">In this case, the last <strong>catch</strong> statement handles all exceptions that aren't handled by any earlier <strong>catch</strong> statement.</span></span> <span data-ttu-id="a9e0a-181">この戦略は、最も外側の <strong>try</strong> ... <strong>catch</strong>ブロックに適しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-181">This strategy is appropriate for the outermost <strong>try</strong>...<strong>catch</strong> blocks.</span></span> <span data-ttu-id="a9e0a-182"><strong>try</strong>...<strong>catch</strong> ステートメントにオプションの *<strong><em>finally</em></strong>* 句を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-182">An optional *<strong><em>finally</em></strong>* clause can be included in <strong>try</strong>...<strong>catch</strong> statements.</span></span> <span data-ttu-id="a9e0a-183"><strong>finally</strong> 節のセマンティクスは、C\# と同じです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-183">The semantics of a <strong>finally</strong> clause are the same as they are in C\#.</span></span> <span data-ttu-id="a9e0a-184"><strong>finally</strong> 句のステートメントは、通常または例外を介してコントロールが <strong>try</strong> ブロックを離れるときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-184">The statements in the <strong>finally</strong> clause are executed when control leaves the <strong>try</strong> block, either normally or through an exception.</span></span> <span data-ttu-id="a9e0a-185"><strong>retry</strong> ステートメントは、<strong>catch</strong> ブロックでのみ書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-185">The <strong>retry</strong> statement can be written only in a <strong>catch</strong> block.</span></span> <span data-ttu-id="a9e0a-186"><strong>retry</strong> ステートメントは、関連付けられている <strong>try</strong> ブロックの最初のコード行までコントロールをジャンプさせます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-186">The <strong>retry</strong> statement causes control to jump up to the first line of code in the associated <strong>try</strong> block.</span></span> <span data-ttu-id="a9e0a-187"><strong>retry</strong> ステートメントは、例外の原因を <strong>catch</strong> ブロック内のコードにより修正できる場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-187">The <strong>retry</strong> statement is used when the cause of the exception can be fixed by the code in the <strong>catch</strong> block.</span></span> <span data-ttu-id="a9e0a-188"><strong>retry</strong> ステートメントは、<strong>try</strong> ブロック内のコードに成功するための別の機会を与えます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-188">The <strong>retry</strong> statement gives the code in the <strong>try</strong> block another opportunity to succeed.</span></span> <span data-ttu-id="a9e0a-189"><strong>retry</strong> ステートメントは、プログラム コントロールが <strong>try</strong> ブロックに入ってから情報ログに書き込まれたすべてのメッセージを消去します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-189">The <strong>retry</strong> statement erases all messages that have been written to the Infolog since program control entered the <strong>try</strong> block.</span></span> <span data-ttu-id="a9e0a-190"><strong>注記:</strong> <strong>再試行</strong>ステートメントにより、無限ループが発生しないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-190"><strong>Note:</strong> You must make sure that your <strong>retry</strong> statements don't cause an infinite loop.</span></span> <span data-ttu-id="a9e0a-191">ベスト プラクティスとして、<strong>試行</strong>ブロックは、ループ中であるかを確認するテストができる変数を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-191">As a best practice, the <strong>try</strong> block should include a variable that you can test to find out whether you're in a loop.</span></span>

    try 
    { 
        // Code here.
    }
    catch (Exception::Numeric) 
    { 
        info("Caught a Numeric exception."); 
    }
    catch 
    { 
        info("Caught an exception."); 
    }
    finally
    {
        // Executed no matter how the try block exits.
    }

#### <a name="the-system-exception-handler"></a><span data-ttu-id="a9e0a-192">システム例外ハンドラー</span><span class="sxs-lookup"><span data-stu-id="a9e0a-192">The system exception handler</span></span>

<span data-ttu-id="a9e0a-193">**catch** ステートメントが例外を処理しない場合、システムの例外ハンドラーによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-193">If no **catch** statement handles the exception, it's handled by the system exception handler.</span></span> <span data-ttu-id="a9e0a-194">システム例外ハンドラーは、情報ログを作成できません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-194">The system exception handler doesn't write to the Infolog.</span></span> <span data-ttu-id="a9e0a-195">したがって、ハンドルされない例外を診断することは難しい可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-195">Therefore, an unhandled exception can be hard to diagnose.</span></span> <span data-ttu-id="a9e0a-196">効率的な例外処理を提供するために、これらすべてのガイドラインに従うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-196">We recommended that you follow all these guidelines to provide effective exception handling:</span></span>

-   <span data-ttu-id="a9e0a-197">呼び出しスタックの最も外側のフレームで、すべての明細書を含む **try** ブロックがあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-197">Have a **try** block that contains all your statements in the outermost frame on the call stack.</span></span>
-   <span data-ttu-id="a9e0a-198">最も外側の **catch** リストの最後に非修飾の **catch** ブロックがあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-198">Have an unqualified **catch** block at the end of your outermost **catch** list.</span></span>
-   <span data-ttu-id="a9e0a-199">**例外**列挙値を直接スローするのは避けてください。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-199">Avoid throwing an **Exception** enum value directly.</span></span>
-   <span data-ttu-id="a9e0a-200">**Global** クラスの **Global::error**、**Global::warning**、または **Global::info** のいずれかのメソッドから返された列挙値をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-200">Throw the enum value that is returned from one of the following methods on the **Global** class: **Global::error**, **Global::warning**, or **Global::info**.</span></span> <span data-ttu-id="a9e0a-201">(暗黙的 **Global::** 接頭語を省略することができます)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-201">(You can omit the implicit **Global::** prefix).</span></span>
-   <span data-ttu-id="a9e0a-202">情報ログに表示されていない例外をキャッチするとき、**Global::info** 関数を呼び出してそれを表示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-202">When you catch an exception that hasn't been shown in the Infolog, call the **Global::info** function to show it.</span></span>

<span data-ttu-id="a9e0a-203">**Exception::CLRError**、**Exception::UpdateConflictNotRecovered**、およびシステム カーネルの例外は、情報ログに自動的に表示されていない例外の例です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-203">**Exception::CLRError**, **Exception::UpdateConflictNotRecovered**, and system kernel exceptions are examples of exceptions that aren't automatically shown in the Infolog.</span></span>

#### <a name="exceptions-and-clr-interop"></a><span data-ttu-id="a9e0a-204">例外および CLR 相互運用</span><span class="sxs-lookup"><span data-stu-id="a9e0a-204">Exceptions and CLR interop</span></span>

<span data-ttu-id="a9e0a-205">共通言語欄タイム (CLR) が管理するアセンブリ内にある、Microsoft .NET Framework クラスおよびメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-205">You can call Microsoft .NET Framework classes and methods that reside in assemblies that are managed by the common language runtime (CLR).</span></span> <span data-ttu-id="a9e0a-206">.NET Framework の **System.Exception** インスタンスがスローされたとき、**Exception::CLRError** を参照することによってコードでそのインスタンスをキャッチできます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-206">When a .NET Framework **System.Exception** instance is thrown, your code can catch it by referencing **Exception::CLRError**.</span></span> <span data-ttu-id="a9e0a-207">コードは、**CLRInterop::getLastException** メソッドを呼び出すことによって、**System.Exception** インスタンスへの参照を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-207">Your code can obtain a reference to the **System.Exception** instance by calling the **CLRInterop::getLastException** method.</span></span>

#### <a name="ensuring-that-exceptions-are-shown"></a><span data-ttu-id="a9e0a-208">例外が表示されるようにする</span><span class="sxs-lookup"><span data-stu-id="a9e0a-208">Ensuring that exceptions are shown</span></span>

<span data-ttu-id="a9e0a-209">**Exception::CLRError** タイプの例外は、**Global::error** などのメソッドの呼び出しでは発行されないため、Infolog には表示されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-209">Exceptions of the **Exception::CLRError** type aren't shown in the Infolog, because these exceptions aren't issued by a call to a method such as **Global::error**.</span></span> <span data-ttu-id="a9e0a-210">**catch** ブロックでは、コードで **Global::error** を呼び出して特定の例外を報告できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-210">In your **catch** block, your code can call **Global::error** to report the specific exception.</span></span>

### <a name="global-class-methods"></a><span data-ttu-id="a9e0a-211">グローバル クラス メソッド</span><span class="sxs-lookup"><span data-stu-id="a9e0a-211">Global class methods</span></span>

<span data-ttu-id="a9e0a-212">このセクションでは、いくつかの**グローバル**クラス メソッドについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-212">This section describes some **Global** class methods in more detail.</span></span> <span data-ttu-id="a9e0a-213">これらのクラスのメソッドには、**Global::error**、**Global::info**、**Global::exceptionTextFallThrough** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-213">These class methods include **Global::error**, **Global::info**, and **Global::exceptionTextFallThrough**.</span></span>

#### <a name="globalerror-method"></a><span data-ttu-id="a9e0a-214">Global::error メソッド</span><span class="sxs-lookup"><span data-stu-id="a9e0a-214">Global::error method</span></span>

<span data-ttu-id="a9e0a-215">次のコードは、**error** メソッドの宣言方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-215">The following code shows how the **error** method is declared.</span></span>

    static Exception error
        (SysInfoLogStr txt,
        URL helpURL = '',
        SysInfoAction _sysInfoAction = null)

<span data-ttu-id="a9e0a-216">戻り値の型は、**Exception::Error** 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-216">The return type is the **Exception::Error** enum value.</span></span> <span data-ttu-id="a9e0a-217">**error** メソッドは例外をスローしません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-217">The **error** method doesn't throw an exception.</span></span> <span data-ttu-id="a9e0a-218">**throw** ステートメントで使用できる列挙値を提供するだけです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-218">It just provides an enum value that can be used in a **throw** statement.</span></span> <span data-ttu-id="a9e0a-219">**throw** ステートメントは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-219">The **throw** statement throws the exception.</span></span> <span data-ttu-id="a9e0a-220">**エラー**メソッドのパラメーターの説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-220">Here are descriptions of the parameters for the **error** method.</span></span> <span data-ttu-id="a9e0a-221">最初のパラメーターのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-221">Only the first parameter is required.</span></span>

- <span data-ttu-id="a9e0a-222"><strong>SysInfoLogStr</strong> txt は、メッセージ テキストの <strong>str</strong> です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-222"><strong>SysInfoLogStr</strong> txt is a <strong>str</strong> of the message text.</span></span> <span data-ttu-id="a9e0a-223">また、<strong>strFmt("@SYS12345", strThingName)</strong> などのラベルの参照にもなります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-223">It can also be a label reference, such as <strong>strFmt("@SYS12345", strThingName)</strong>.</span></span>
- <span data-ttu-id="a9e0a-224">**URL** helpUrl は、アプリケーション エクスプローラーのヘルプ トピックの場所への参照です (**"KernDoc:\\\\\\\\Functions\\\\substr"**)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-224">The **URL** helpUrl is a reference to the location of a Help topic in Application Explorer, such as **"KernDoc:\\\\\\\\Functions\\\\substr"**.</span></span> <span data-ttu-id="a9e0a-225">\_sysInfoAction が提供された場合、このパラメータは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-225">The parameter value is ignored if \_sysInfoAction is supplied.</span></span>
- <span data-ttu-id="a9e0a-226">**SysInfoAction** \_sysInfoAction は、**SysInfoAction** クラスを拡張するクラスのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-226">The **SysInfoAction** \_sysInfoAction is an instance of a class that extends the **SysInfoAction** class.</span></span> <span data-ttu-id="a9e0a-227">**description** メソッド、**run** メソッド、**pack** メソッド、および **unpack** メソッドは、子クラスに対して推奨されるメソッドのオーバーライドです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-227">The method overrides that we recommend for the child class are the **description** method, the **run** method, the **pack** method, and the **unpack** method.</span></span>

#### <a name="globalinfo-method"></a><span data-ttu-id="a9e0a-228">Global::info メソッド</span><span class="sxs-lookup"><span data-stu-id="a9e0a-228">Global::info method</span></span>

<span data-ttu-id="a9e0a-229">**Global::info** メソッドは、情報ログにテキストを表示するために頻繁に使用します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-229">The **Global::info** method is often used to show text in the Infolog.</span></span> <span data-ttu-id="a9e0a-230">プログラムでは、**情報 (「メッセージ。」)** としてよく書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-230">In programs, it's often written as **info("My message.");**.</span></span> <span data-ttu-id="a9e0a-231">**情報**メソッドは **Exception::Info** 列挙値を返しますが、まれに予期しないことが発生するため、**Exception::Info** をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-231">Although the **info** method returns an **Exception::Info** enum value, you will rarely want to throw **Exception::Info**, because nothing unexpected has occurred.</span></span>

#### <a name="globalexceptiontextfallthrough-method"></a><span data-ttu-id="a9e0a-232">Global::exceptionTextFallThrough メソッド</span><span class="sxs-lookup"><span data-stu-id="a9e0a-232">Global::exceptionTextFallThrough method</span></span>

<span data-ttu-id="a9e0a-233">場合によっては、**catch** ブロック内で何もしない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-233">Occasionally, you want to do nothing inside your **catch** block.</span></span> <span data-ttu-id="a9e0a-234">ただし、空の **catch** ブロックがある場合、X++ コンパイラは警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-234">However, the X++ compiler generates a warning if you have an empty **catch** block.</span></span> <span data-ttu-id="a9e0a-235">この警告を避けるためには、**catch** ブロック内の **Global::exceptionTextFallThrough** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-235">To avoid this warning, call the **Global::exceptionTextFallThrough** method in the **catch** block.</span></span> <span data-ttu-id="a9e0a-236">このメソッドは何もしませんが、コンパイラを満たします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-236">The method does nothing, but it satisfies the compiler.</span></span>

### <a name="exceptions-inside-transactions"></a><span data-ttu-id="a9e0a-237">トランザクション内の例外</span><span class="sxs-lookup"><span data-stu-id="a9e0a-237">Exceptions inside transactions</span></span>

<span data-ttu-id="a9e0a-238">例外がトランザクションの内部でスローされる場合は、トランザクションが自動的にキャンセル (つまり、**ttsAbort** 操作が発生) されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-238">If an exception is thrown inside a transaction, the transaction is automatically canceled (that is, a **ttsAbort** operation occurs).</span></span> <span data-ttu-id="a9e0a-239">この動作は、手動でスローされる例外とシステムがスローする例外の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-239">This behavior applies for both exceptions that are thrown manually and exceptions that the system throws.</span></span> <span data-ttu-id="a9e0a-240">**ttsBegin**-**ttsCommit** トランザクション ブロック内で例外がスローされるとき、そのトランザクション ブロック内の **catch** ステートメントは例外を処理できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-240">When an exception is thrown inside a **ttsBegin**-**ttsCommit** transaction block, no **catch** statement inside that transaction block can process the exception.</span></span> <span data-ttu-id="a9e0a-241">代わりに、トランザクション ブロックの外部にある最も内側の **catch** ステートメントが、最初にテストされる **catch** ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-241">Instead, the innermost **catch** statements that are outside the transaction block are the first **catch** statements that are tested.</span></span>

### <a name="examples-of-exception-handling"></a><span data-ttu-id="a9e0a-242">例外処理の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-242">Examples of exception handling</span></span>

#### <a name="showing-exceptions-in-the-infolog"></a><span data-ttu-id="a9e0a-243">情報ログに例外を表示</span><span class="sxs-lookup"><span data-stu-id="a9e0a-243">Showing exceptions in the Infolog</span></span>

<span data-ttu-id="a9e0a-244">次のコード例は、Infolog の例外を示しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-244">The following code example shows exceptions in the Infolog.</span></span>

    // This example shows that a direct throw of Exception::Error does not
    // display a message in the Infolog. This is why we recommend the 
    // Global::error method. 
    static void TryCatchThrowError1Job(Args _args)
    {
    /***
      The 'throw' does not directly add a message to the Infolog.
      The exception is caught.
    ***/    
        try
        {
            info("In the 'try' block. (j1)");
            throw Exception::Error;
        }
        catch (Exception::Error)
        {
            info("Caught 'Exception::Error'.");
        }

    /**********  Actual Infolog output
    Message (03:43:45 pm)
    In the 'try' block. (j1)
    Caught 'Exception::Error'.
    **********/
    }

#### <a name="using-the-error-method-to-write-exception-information-to-the-infolog"></a><span data-ttu-id="a9e0a-245">エラー メソッドを使用して例外情報を情報ログに記述</span><span class="sxs-lookup"><span data-stu-id="a9e0a-245">Using the error method to write exception information to the Infolog</span></span>

<span data-ttu-id="a9e0a-246">次のコード例では、**error** メソッドを使用して例外情報を Infolog に書き出します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-246">The following code example uses the **error** method to write exception information to the Infolog.</span></span>

    // This example shows that the use of the Global::error method 
    // is a reliable way to display exceptions in the Infolog. 
    static void TryCatchGlobalError2Job(Args _args)
    {
        /***
        The 'Global::error()' does directly add a message to the Infolog.
        The exception is caught.
        ***/
        try
        {
            info("In the 'try' block. (j2)");
            throw Global::error("Written to the Infolog.");
        }
        catch (Exception::Error)
        {
            info("Caught 'Exception::Error'.");
        }

    /***  Infolog output
    Message (03:51:44 pm)
    In the 'try' block. (j2)
    Written to the Infolog.
    Caught 'Exception::Error'.
    ***/
    }

#### <a name="handling-a-clrerror"></a><span data-ttu-id="a9e0a-247">CLRError の処理</span><span class="sxs-lookup"><span data-stu-id="a9e0a-247">Handling a CLRError</span></span>

<span data-ttu-id="a9e0a-248">次のコード例は、**CLRError** 例外を処理します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-248">The following code example handles a **CLRError** exception.</span></span>

    // This example shows that a CLRError exception is not displayed 
    // in the Infolog unless you catch the exception and manually
    // call the info method. The use of the CLRInterop::getLastException
    // method is also demonstrated. 
    static void TryCatchCauseCLRError3Job(Args _args)
    {
        /***
        The 'netString.Substring(-2)' causes a CLRError,
        but it does not directly add a message to the Infolog.
        The exception is caught.
        ***/
        System.String netString = "Net string.";
        System.Exception netExcepn;
        try
        {
            info("In the 'try' block. (j3)");
            netString.Substring(-2); // Causes CLR Exception.
        }
        catch (Exception::Error)
        {
            info("Caught 'Exception::Error'.");
        }
        catch (Exception::CLRError)
        {
            info("Caught 'Exception::CLRError'.");
            netExcepn = CLRInterop::getLastException();
            info(netExcepn.ToString());
        }

    /**********  Actual Infolog output (truncated for display)
    Message (03:55:10 pm)
    In the 'try' block. (j3)
    Caught 'Exception::CLRError'.
    System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. ---> 
        System.ArgumentOutOfRangeException: StartIndex cannot be less than zero.
    Parameter name: startIndex
       at System.String.InternalSubStringWithChecks(Int32 startIndex, Int32 length, Boolean fAlwaysCopy)
       at System.String.Substring(Int32 startIndex)
       at ClrBridgeImpl.InvokeClrInstanceMethod(ClrBridgeImpl* , ObjectWrapper* objectWrapper, Char* pszMethodName, 
       Int32 argsLength, ObjectWrapper** arguments, Boolean* argsAreByRef, Boolean* isException)
    **********/
    }

#### <a name="using-a-retry-statement"></a><span data-ttu-id="a9e0a-249">再試行ステートメントの使用</span><span class="sxs-lookup"><span data-stu-id="a9e0a-249">Using a retry statement</span></span>

<span data-ttu-id="a9e0a-250">次のコード例では、**retry** ステートメントを使用しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-250">The following code example uses a **retry** statement.</span></span>

    // This example shows how to use the retry statement. The print
    // statements are included because retry causes earlier Infolog 
    // messages to be erased. 
    static void TryCatchRetry4Job(Args _args)
    {
        /***
        Demonstration of 'retry'. The Infolog output is partially erased
        by 'retry', but the Print window is fully displayed.
        ***/
        Exception excepnEnum;
        int nCounter = 0;
        try
        {
            info("        .");
            print("        .");
            info("In the 'try' block, [" + int2str(nCounter) + "]. (j4)");
            print("In the 'try' block, [" + int2str(nCounter) + "]. (j4)");
            nCounter++;
            if (nCounter >= 3) // Prevent infinite loop.
            {
                info("---- Will now throw a warning, which is not caught.");
                print("---- Will now throw a warning, which is not caught.");
                throw Global::warning("This warning will not be caught. [" + int2str(nCounter) + "]");
            }
            else
            {
                info("Did not throw a warning this loop. [" + int2str(nCounter) + "]");
                print("Did not throw a warning this loop. [" + int2str(nCounter) + "]");
            }
            excepnEnum = Global::error("This error message is written to the Infolog.");
            throw excepnEnum;
        }
        catch (Exception::Error)
        {
            info("Caught 'Exception::Error'.");
            print("Caught 'Exception::Error'.");
            retry;
        }
        info("End of job.");
        print("End of job.");

    /**********  Actual Infolog output
    Message (04:33:56 pm)
            .
    In the 'try' block, [2]. (j4)
    ---- Will now throw a warning, which is not caught.
    This warning will not be caught. [3]
    **********/
    }

#### <a name="throwing-an-exception-inside-a-transaction"></a><span data-ttu-id="a9e0a-251">トランザクション内での例外のスロー</span><span class="sxs-lookup"><span data-stu-id="a9e0a-251">Throwing an exception inside a transaction</span></span>

<span data-ttu-id="a9e0a-252">次のコード例は、トランザクション ブロックに例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-252">The following code example throws an exception in a transaction block.</span></span>

    // This examples uses three levels of try nesting to illustrate
    // where an exception is caught when the exception is thrown inside
    // a ttsBegin-ttsCommit transaction block. 
    static void TryCatchTransaction5Job(Args _args)
    {
        /***
        Shows an exception that is thrown inside a ttsBegin - ttsCommit
        transaction block cannot be caught inside that block.
        ***/
        try
        {
            try
            {
                ttsbegin;
                try
                {
                    throw error("Throwing exception inside transaction.");
                }
                catch (Exception::Error)
                {
                    info("Catch_1: Unexpected, caught in 'catch' inside the transaction block.");
                }
                ttscommit;
            }
            catch (Exception::Error)
            {
                info("Catch_2: Expected, caught in the innermost 'catch' that is outside of the transaction block.");
            }
        }
        catch (Exception::Error)
        {
            info("Catch_3: Unexpected, caught in 'catch' far outside the transaction block.");
        }
        info("End of job.");

    /**********  Actual Infolog output
    Message (04:12:34 pm)
    Throwing exception inside transaction.
    Catch_2: Expected, caught in the innermost 'catch' that is outside of the transaction block.
    End of job.
    **********/
    }

#### <a name="using-globalerror-with-a-sysinfoaction-parameter"></a><span data-ttu-id="a9e0a-253">SysInfoAction パラメーターでの Global::error の使用</span><span class="sxs-lookup"><span data-stu-id="a9e0a-253">Using Global::error with a SysInfoAction parameter</span></span>

<span data-ttu-id="a9e0a-254">コードが例外をスローすると、情報ログにメッセージを書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-254">When your code throws an exception, it can write messages to the Infolog.</span></span> <span data-ttu-id="a9e0a-255">**SysInfoAction** クラスを使用すると、これらの情報ログ メッセージをさらに便利にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-255">You can make those Infolog messages more helpful by using the **SysInfoAction** class.</span></span> <span data-ttu-id="a9e0a-256">次の例では、**SysInfoAction** パラメーターは **Global::error** メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-256">In the following example, a **SysInfoAction** parameter is passed in to the **Global::error** method.</span></span> <span data-ttu-id="a9e0a-257">**error** メソッドは、情報ログにメッセージを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-257">The **error** method writes the message to the Infolog.</span></span> <span data-ttu-id="a9e0a-258">ユーザーが情報ログ メッセージをダブルクリックすると、**SysInfoAction.run** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-258">When the user double-clicks the Infolog message, the **SysInfoAction.run** method is run.</span></span> <span data-ttu-id="a9e0a-259">**run** メソッドでは、診断を支援したり、例外が発生した問題を解決したりするコードを書き込めます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-259">In the **run** method, you can write code that helps diagnose or fix the issue that caused the exception.</span></span> <span data-ttu-id="a9e0a-260">**Global::error** メソッドに渡されるオブジェクトは、**SysInfoAction** を拡張して記述するクラスから構築されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-260">The object that is passed in to the **Global::error** method is constructed from a class that you write that extends **SysInfoAction**.</span></span> <span data-ttu-id="a9e0a-261">次のコード例は 2 つの部分で示されています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-261">The following code sample is shown in two parts.</span></span> <span data-ttu-id="a9e0a-262">最初の部分は、**Global::error** メソッドを呼び出して、返された値をスローするジョブを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-262">The first part shows a job that calls the **Global::error** method and then throws the returned value.</span></span> <span data-ttu-id="a9e0a-263">**SysInfoAction\_PrintWindow\_Demo** クラスのインスタンスが**エラー** メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-263">An instance of the **SysInfoAction\_PrintWindow\_Demo** class is passed in to the **error** method.</span></span> <span data-ttu-id="a9e0a-264">2 番目の部分は、**SysInfoAction\_PrintWindow\_Demo** クラスを示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-264">The second part shows the **SysInfoAction\_PrintWindow\_Demo** class.</span></span>

##### <a name="part-1-calling-globalerror"></a><span data-ttu-id="a9e0a-265">パート 1: Global::error を呼び出す</span><span class="sxs-lookup"><span data-stu-id="a9e0a-265">Part 1: Calling Global::error</span></span>

    static void Job_SysInfoAction(Args _args)
    {
        try
        {
            throw Global::error
                ("Click me to make the Print window display."
                ,""
                ,new SysInfoAction_PrintWindow_Demo()
                );
        }
        catch
        {
            warning("Issuing a warning from the catch block.");
        }
    }

##### <a name="part-2-the-sysinfoactionprintwindowdemo-class"></a><span data-ttu-id="a9e0a-266">パート 2: SysInfoAction\_PrintWindow\_Demo クラス</span><span class="sxs-lookup"><span data-stu-id="a9e0a-266">Part 2: The SysInfoAction\_PrintWindow\_Demo class</span></span>

    public class SysInfoAction_PrintWindow_Demo extends SysInfoAction
    {
        str m_sGreeting; // In classDeclaration.
        public str description()
        {
            return "Starts the Print Window for demonstration.";
        }
        public void run()
        {
            print("This appears in the Print window.");
            print(m_sGreeting);

            /*********** Actual Infolog output
            Message (03:19:28 pm)
            Click me to make the Print window display.
            Issuing a warning from the catch block.
            ***************/
        }
        public container pack()
        {
            return ["Packed greeting."]; // Literal container.
        }
        public boolean unpack(container packedClass, Object object = null)
        {
            [m_sGreeting] = packedClass;
            return true;
        }
    }

### <a name="list-of-exceptions"></a><span data-ttu-id="a9e0a-267">例外のリスト</span><span class="sxs-lookup"><span data-stu-id="a9e0a-267">List of exceptions</span></span>

<span data-ttu-id="a9e0a-268">次のテーブルは、**例外** 列挙型の値である例外リテラルを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-268">The following table shows the exception literals that are the values of the **Exception** enumeration.</span></span>

| <span data-ttu-id="a9e0a-269">リテラルの例外</span><span class="sxs-lookup"><span data-stu-id="a9e0a-269">Exception literal</span></span>                 | <span data-ttu-id="a9e0a-270">説明</span><span class="sxs-lookup"><span data-stu-id="a9e0a-270">Description</span></span>                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e0a-271">分割</span><span class="sxs-lookup"><span data-stu-id="a9e0a-271">Break</span></span>                             | <span data-ttu-id="a9e0a-272">ユーザーは Break または Ctrl+C を押しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-272">The user pressed Break or Ctrl+C.</span></span>                                                                                                                                   |
| <span data-ttu-id="a9e0a-273">CLRError</span><span class="sxs-lookup"><span data-stu-id="a9e0a-273">CLRError</span></span>                          | <span data-ttu-id="a9e0a-274">CLR 機能の使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-274">An error occurred while the CLR functionality was being used.</span></span>                                                                                                       |
| <span data-ttu-id="a9e0a-275">CodeAccessSecurity</span><span class="sxs-lookup"><span data-stu-id="a9e0a-275">CodeAccessSecurity</span></span>                | <span data-ttu-id="a9e0a-276">**CodeAccessPermission.demand** メソッドを使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-276">An error occurred while the **CodeAccessPermission.demand** method was being used.</span></span>                                                                                  |
| <span data-ttu-id="a9e0a-277">DDEerror</span><span class="sxs-lookup"><span data-stu-id="a9e0a-277">DDEerror</span></span>                          | <span data-ttu-id="a9e0a-278">**DDE** システム クラスを使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-278">An error occurred while the **DDE** system class was being used.</span></span>                                                                                                    |
| <span data-ttu-id="a9e0a-279">デッドロック</span><span class="sxs-lookup"><span data-stu-id="a9e0a-279">Deadlock</span></span>                          | <span data-ttu-id="a9e0a-280">複数のトランザクションが相互に待機しているため、データベースのデッドロックが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-280">A database deadlock occurred, because several transactions are waiting for each other.</span></span>                                                                              |
| <span data-ttu-id="a9e0a-281">DuplicateKeyException</span><span class="sxs-lookup"><span data-stu-id="a9e0a-281">DuplicateKeyException</span></span>             | <span data-ttu-id="a9e0a-282">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-282">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9e0a-283">トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-283">The transaction can be retried (use a **retry** statement in the **catch** block).</span></span> |
| <span data-ttu-id="a9e0a-284">DuplicateKeyExceptionNotRecovered</span><span class="sxs-lookup"><span data-stu-id="a9e0a-284">DuplicateKeyExceptionNotRecovered</span></span> | <span data-ttu-id="a9e0a-285">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-285">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9e0a-286">このコードは再試行されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-286">The code won't be retried.</span></span> <span data-ttu-id="a9e0a-287">この例外は、トランザクション内では検出されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-287">This exception can't be caught inside a transaction.</span></span>    |
| <span data-ttu-id="a9e0a-288">エラー</span><span class="sxs-lookup"><span data-stu-id="a9e0a-288">Error</span></span>                             | <span data-ttu-id="a9e0a-289">致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-289">A fatal error occurred.</span></span> <span data-ttu-id="a9e0a-290">トランザクションは停止されました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-290">The transaction has been stopped.</span></span>                                                                                                           |
| <span data-ttu-id="a9e0a-291">情報</span><span class="sxs-lookup"><span data-stu-id="a9e0a-291">Info</span></span>                              | <span data-ttu-id="a9e0a-292">この例外リテラルは、ユーザーのメッセージを保持します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-292">This exception literal holds a message for the user.</span></span> <span data-ttu-id="a9e0a-293">**情報**例外をスローしないでください。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-293">Don't throw an **info** exception.</span></span>                                                                             |
| <span data-ttu-id="a9e0a-294">内部</span><span class="sxs-lookup"><span data-stu-id="a9e0a-294">Internal</span></span>                          | <span data-ttu-id="a9e0a-295">開発システムで内部エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-295">An internal error occurred in the development system.</span></span>                                                                                                               |
| <span data-ttu-id="a9e0a-296">数値</span><span class="sxs-lookup"><span data-stu-id="a9e0a-296">Numeric</span></span>                           | <span data-ttu-id="a9e0a-297">**str2int**、**str2int64**、または **str2num** 機能を使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-297">An error occurred while the **str2int**, **str2int64**, or **str2num** function was being used.</span></span>                                                                     |
| <span data-ttu-id="a9e0a-298">順番</span><span class="sxs-lookup"><span data-stu-id="a9e0a-298">Sequence</span></span>                          |                                                                                                                                                                     |
| <span data-ttu-id="a9e0a-299">UpdateConflict</span><span class="sxs-lookup"><span data-stu-id="a9e0a-299">UpdateConflict</span></span>                    | <span data-ttu-id="a9e0a-300">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-300">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9e0a-301">トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-301">The transaction can be retried (use a **retry** statement in the **catch** block).</span></span> |
| <span data-ttu-id="a9e0a-302">UpdateConflictNotRecovered</span><span class="sxs-lookup"><span data-stu-id="a9e0a-302">UpdateConflictNotRecovered</span></span>        | <span data-ttu-id="a9e0a-303">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-303">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9e0a-304">このコードは再試行されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-304">The code won't be retried.</span></span> <span data-ttu-id="a9e0a-305">この例外は、トランザクション内では検出されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-305">This exception can't be caught within a transaction.</span></span>    |
| <span data-ttu-id="a9e0a-306">警告</span><span class="sxs-lookup"><span data-stu-id="a9e0a-306">Warning</span></span>                           | <span data-ttu-id="a9e0a-307">例外的なイベントが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-307">An exceptional event has occurred.</span></span> <span data-ttu-id="a9e0a-308">ユーザーはアクションの実行をする必要がありますが、イベントは致命的ではありません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-308">Although the user might have to take action, the event isn't fatal.</span></span> <span data-ttu-id="a9e0a-309">**警告**例外をスローしないでください。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-309">Don't throw a **warning** exception.</span></span>                         |
| [<span data-ttu-id="a9e0a-310">TransientSqlConnectionError</span><span class="sxs-lookup"><span data-stu-id="a9e0a-310">TransientSqlConnectionError</span></span>](sql-connection-error.md)       | <span data-ttu-id="a9e0a-311">クエリ実行時にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-311">An error occured when during the query execution.</span></span> <span data-ttu-id="a9e0a-312">トランザクションはキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-312">The transaction will be canceled.</span></span> <span data-ttu-id="a9e0a-313">この例外は、トランザクション内では検出されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-313">This exception can't be caught within a transaction.</span></span> |

## <a name="loop-statements-for-while-and-dowhile"></a><span data-ttu-id="a9e0a-314">ループ ステートメント: for、while、do...while</span><span class="sxs-lookup"><span data-stu-id="a9e0a-314">Loop statements: for, while, and do...while</span></span>
<span data-ttu-id="a9e0a-315">ループ ステートメントは、**for**、**while**、**do**、**while** の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-315">There are three loop statements: **for**, **while**, and **do**...**while**.</span></span> <span data-ttu-id="a9e0a-316">ループでは、ループに設定された条件が **false** になるまで、そのステートメントを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-316">A loop repeats its statement until the condition that is set for the loop is **false**.</span></span> <span data-ttu-id="a9e0a-317">loop ステートメント内では、**break** および **continue** ステートメントを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-317">Within the loop statements, you can use **break** and **continue** statements.</span></span>

### <a name="for-loops"></a><span data-ttu-id="a9e0a-318">for ループ</span><span class="sxs-lookup"><span data-stu-id="a9e0a-318">for loops</span></span>

<span data-ttu-id="a9e0a-319">**for** ループは、条件式が **true** である限り、1 つ以上のステートメントを繰り返し実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-319">The **for** loop repeatedly executes one or more statements for as long as the conditional expression is **true**.</span></span> <span data-ttu-id="a9e0a-320">ステートメントは、条件が満たされた回数だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-320">The statement is executed as many times as the condition is met.</span></span> <span data-ttu-id="a9e0a-321">**for** ループの本文は、条件テストの結果に応じて 0 回以上実行されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-321">The body of the **for** loop might be executed zero or more times, depending on the results of the condition test.</span></span> <span data-ttu-id="a9e0a-322">**for** ループは、制御変数に初期値を割り当て、また変数の増減ステートメントがあるために、他のループとは異なります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-322">A **for** loop differs from other loops because an initial value can be assigned to a control variable, and because there is a statement for incrementing or decrementing the variable.</span></span> <span data-ttu-id="a9e0a-323">これらの追加は **for** ループを作成します。これは、リスト、コンテナー、配列をトラバースする場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-323">These additions make a **for** loop especially useful for traversing lists, containers, and arrays, because they have a fixed number of elements.</span></span> <span data-ttu-id="a9e0a-324">また、明細書を各要素に適用して、要素全体を増分し、最後の要素をテストする条件を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-324">You can also apply a statement to each element and increment your way through the elements, setting the condition to test for the last element.</span></span> <span data-ttu-id="a9e0a-325">**for** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-325">Here is the syntax for a **for** statement:</span></span>

<span data-ttu-id="a9e0a-326">**(** *初期化* **;** *テスト* **;** *増分* **){** *明細書* **}対象**</span><span class="sxs-lookup"><span data-stu-id="a9e0a-326">**for (** *initialization* **;** *test* **;** *increment* **) {** *statement* **}**</span></span>

<span data-ttu-id="a9e0a-327">*tatement* 明細書のブロックにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-327">*tatement* can be a block of statements.</span></span>

#### <a name="example-of-a-for-loop"></a><span data-ttu-id="a9e0a-328">For loop の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-328">Example of a for loop</span></span>

    // An example where all items are printed in 
    // a fixed array called ra with 100 reals. 
    int ra[100];
    int i; // Control variable.
    for (i=1; i<=100; i+=1)
    {
        print ra[i];
    }

### <a name="while-loops"></a><span data-ttu-id="a9e0a-329">while loops</span><span class="sxs-lookup"><span data-stu-id="a9e0a-329">while loops</span></span>

<span data-ttu-id="a9e0a-330">**while** ループは、条件式が **true** である限り、1 つ以上のステートメントを繰り返し実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-330">A **while** loop repeatedly executes one or more statements for as long as the conditional expression is **true**.</span></span> <span data-ttu-id="a9e0a-331">ステートメントは、条件が満たされた回数だけ実行されます (ゼロから多数)。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-331">The statements are executed as many times as the condition is met (zero to many).</span></span> <span data-ttu-id="a9e0a-332">**while** ループの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-332">Here is the syntax for a **while** loop:</span></span>

<span data-ttu-id="a9e0a-333">**(** *式* **)** のとき、*明細書*</span><span class="sxs-lookup"><span data-stu-id="a9e0a-333">**while (** *expression* **)** *statement*</span></span>

<span data-ttu-id="a9e0a-334">この構文では、*ステートメント*はステートメントのブロックで置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-334">In this syntax, *statement* can be replaced by a block of statements.</span></span>

#### <a name="example-of-a-while-loop"></a><span data-ttu-id="a9e0a-335">While loop の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-335">Example of a while loop</span></span>

    // This example demonstrates a while loop that traverses 
    // a container, cont, and prints out the contents of the container.
    public static void Iteration()
    {
        container cont;
        int no = 1;
        while (no <= conlen(cont))
        {
            print conpeek(cont,no);
            no = no + 1;
        }
    }

### <a name="dowhile-loops"></a><span data-ttu-id="a9e0a-336">do...while ループ</span><span class="sxs-lookup"><span data-stu-id="a9e0a-336">do...while loops</span></span>

<span data-ttu-id="a9e0a-337">**do**...**while** ループは、**while** ループと似ていますが、条件は実行する必要があるステートメントの後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-337">The **do**...**while** loop is similar to the **while** loop, but the condition appears after the statements that must be executed.</span></span> <span data-ttu-id="a9e0a-338">ステートメントは、ステートメントの実行後にテストされるため、少なくとも 1 回は常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-338">The statements are always executed at least one time, because the condition is tested after the statements are executed.</span></span> <span data-ttu-id="a9e0a-339">**do**...**while** ループは、レポートのパラメーターの取得など、必ず 1 回以上実行する必要があるタスクに適しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-339">The **do**...**while** loop is well-suited to tasks that must always be done at least one time, such as getting parameters for a report.</span></span> <span data-ttu-id="a9e0a-340">**do**...**while** ループの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-340">Here is the syntax for a **do**...**while** loop:</span></span>

<span data-ttu-id="a9e0a-341">**{** *明細書* **} とするのは、(** *式*\* **) ;** のときです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-341">**do {** *statement* **} while (** *expression* **) ;**</span></span>

<span data-ttu-id="a9e0a-342">*tatement* 明細書のブロックにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-342">*tatement* can be a block of statements.</span></span>

#### <a name="example-of-a-dowhile-loop"></a><span data-ttu-id="a9e0a-343">Do の例...while loop</span><span class="sxs-lookup"><span data-stu-id="a9e0a-343">Example of a do...while loop</span></span>

    // An example of a do...while loop designed to find 
    // the smallest power of 10 that is larger than _Value.
    int FindPower(real _Value)
    {
        int ex=-1;
        real curVal;
        ;
        do
        {
            ex += 1;
            curVal = power(10, ex);
        }
        while (_Value>curVal);
        return ex;
    }

### <a name="continue-and-break-statements"></a><span data-ttu-id="a9e0a-344">continue および break ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-344">continue and break statements</span></span>

<span data-ttu-id="a9e0a-345">**continue** ステートメントは、**for**、**while**、または **do**...**while** ループの次の反復処理に直接移動する実行を発生させます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-345">The **continue** statement causes execution to move directly to the next iteration of a **for**, **while**, or **do**...**while** loop.</span></span> <span data-ttu-id="a9e0a-346">**実行**または**途中**で、すぐにテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-346">For **do** or **while**, the test is executed immediately.</span></span> <span data-ttu-id="a9e0a-347">**対象**ステートメントで、増分手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-347">For a **for** statement, the increment step is executed.</span></span> <span data-ttu-id="a9e0a-348">ループ内の **break** ステートメントは、そのループを終了するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-348">The **break** statement within a loop is used to terminate that loop.</span></span> <span data-ttu-id="a9e0a-349">実行後、ループの後の最初のステートメントに移動します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-349">Execution then moves to the first statement after the loop.</span></span>

#### <a name="example-of-a-continue-statement"></a><span data-ttu-id="a9e0a-350">続行明細書の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-350">Example of a continue statement</span></span>

    // An example of a continue statement. 
    // If Iarray[i] <= 0, the remaining statements in the loop are not executed, 
    // and i is incremented before the if statement is tried again.
    int i;
    int Iarray[100];
    for (i=1; i<=100; i++)
    {
        if (Iarray[i] <= 0)
        continue;
        // Some statements.
    }

## <a name="print-statements"></a><span data-ttu-id="a9e0a-351">print ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-351">print statements</span></span>
<span data-ttu-id="a9e0a-352">一時的なウィンドウにメッセージ (テキストまたは選択した結果) を表示するには、**print** ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-352">You use the **print** statement to show messages (text or selected results) in a temporary window.</span></span> <span data-ttu-id="a9e0a-353">このウィンドウは、最初の **print** 文が実行されたときに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-353">This window appears when the first **print** statement is executed.</span></span> <span data-ttu-id="a9e0a-354">テスト中に、**印刷**明細書は情報ログのテキストを表示する **Global::info** 方法に代わる便利な手段となります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-354">During testing, the **print** statement can be a convenient alternative to the **Global::info** method, which shows text in the Infolog.</span></span> <span data-ttu-id="a9e0a-355">次のテーブルは、**print** ステートメントと **Global::info** メソッドを比較しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-355">The following table compares the **print** statement and the **Global::info** method.</span></span>

| <span data-ttu-id="a9e0a-356">機能</span><span class="sxs-lookup"><span data-stu-id="a9e0a-356">Feature</span></span>                                   | <span data-ttu-id="a9e0a-357">print ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-357">print statement</span></span>                                                                                                                             | <span data-ttu-id="a9e0a-358">情報メソッド</span><span class="sxs-lookup"><span data-stu-id="a9e0a-358">Info method</span></span>                                                                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a9e0a-359">呼び出し易さ</span><span class="sxs-lookup"><span data-stu-id="a9e0a-359">Ease of invocation</span></span>                        | <span data-ttu-id="a9e0a-360">**print** ステートメントは、さまざまなデータ型を自動的に文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-360">The **print** statement automatically converts various data types into strings.</span></span> <span data-ttu-id="a9e0a-361">1 つの呼び出しで複数のデータ型を変換できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-361">It can convert multiple data types in one invocation.</span></span>       | <span data-ttu-id="a9e0a-362">**info** メソッドでは、入力パラメーターを文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-362">The **info** method requires that the input parameter be a string.</span></span>               |
| <span data-ttu-id="a9e0a-363">クリップボードにコンテンツをコピーする機能</span><span class="sxs-lookup"><span data-stu-id="a9e0a-363">Ability to copy contents to the clipboard</span></span> | <span data-ttu-id="a9e0a-364">**印刷**明細書が開くウィンドウのコンテンツをクリップボードにコピーすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-364">The contents of the window that the **print** statement opens can't be copied to the clipboard.</span></span> <span data-ttu-id="a9e0a-365">ウィンドウのフォーカスを付与することはできません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-365">You can't give the window focus.</span></span>            | <span data-ttu-id="a9e0a-366">情報ログの内容は**情報ログ** ウィンドウからクリップボードに容易にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-366">Infolog contents are easily copied from the **Infolog** window to the clipboard.</span></span> |
| <span data-ttu-id="a9e0a-367">有効期間の範囲</span><span class="sxs-lookup"><span data-stu-id="a9e0a-367">Scope of lifetime</span></span>                         | <span data-ttu-id="a9e0a-368">このウィンドウは、X++ アプリケーションが終了すると終了し、アプリケーションを読むのを待たずに閉じることがあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-368">The window closes when the X++ application ends, and it might close before you have time to read it.</span></span>                                        | <span data-ttu-id="a9e0a-369">このウィンドウは、クライアント セッション全体にわたって存続します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-369">The window persists for the whole client session.</span></span>                                |
| <span data-ttu-id="a9e0a-370">サイズと場所</span><span class="sxs-lookup"><span data-stu-id="a9e0a-370">Size and location</span></span>                         | <span data-ttu-id="a9e0a-371">ウィンドウは特定のサイズで画面の特定の場所に配置できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-371">The window can be a specific size and in a specific location on the screen.</span></span>                                                                 | <span data-ttu-id="a9e0a-372">ウィンドウは、システムによってサイズが決められて配置されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-372">The window is sized and placed by the system.</span></span>                                    |
| <span data-ttu-id="a9e0a-373">一般的な使用</span><span class="sxs-lookup"><span data-stu-id="a9e0a-373">Typical usage</span></span>                             | <span data-ttu-id="a9e0a-374">**print** ステートメントは、テスト時に使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-374">The **print** statement is used for convenience during testing.</span></span> <span data-ttu-id="a9e0a-375">正式なデバッガーを実行する必要なく、小さな問題をデバッグすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-375">It can help you debug small issues without having to run a formal debugger.</span></span> | <span data-ttu-id="a9e0a-376">**info** メソッドは、生産での使用に適しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-376">The **info** method is appropriate for use in production.</span></span>                        |

### <a name="example-of-a-print-statement"></a><span data-ttu-id="a9e0a-377">印刷明細書の例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-377">Example of a print statement</span></span>

    // This example demonstrates the print statement automatically converting any
    // date type to a string. 
    static void PrintJob2(Args _args)
    {
        str s1 = "Hello";
        int n2 = 42;
        utcDateTime udt3 = DateTimeUtil::utcNow();
        Dialog dlog4 = new Dialog();
        print "The print statement automatically converts data types to strings.";
        print s1, " -- ", n2, " -- ", udt3, " -- ", dlog4;
        Global::info("User clicked 'Yes' to continue to this call to info.");
        info(int2Str(n2)); // int2Str converter is needed.
    }
    /***  Output to the Print window:
    The print statement automatically converts data types to strings.
    Hello -- 42 -- 10/3/2011 09:18:10 pm -- 1
    ***/

    /***  Output to Infolog window:
    Message (02:18:10 pm)
    User clicked 'Yes' to continue to this call to info.
    ***/

## <a name="todo-comments"></a><span data-ttu-id="a9e0a-378">TODO コメント</span><span class="sxs-lookup"><span data-stu-id="a9e0a-378">TODO comments</span></span>
<span data-ttu-id="a9e0a-379">コンパイラは、コメントの先頭に**仕事**という文字列があると認識します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-379">The compiler recognizes the string **TODO** when it occurs at the start of a comment.</span></span> <span data-ttu-id="a9e0a-380">**TODO** 文字列は、Microsoft Visual Studio の **タスク一覧** ウィンドウでコメント テキストの残りの部分を報告するようにコンパイラに求めます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-380">The **TODO** string prompts the compiler to report the rest of the comment text in the **Task List** window in Microsoft Visual Studio.</span></span> <span data-ttu-id="a9e0a-381">**タスク一覧** ウィンドウを開くには、**表示** を選択し、**タスク ウィンドウ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-381">To open the **Task List** window, select **View**, and then select **Task Window**.</span></span> <span data-ttu-id="a9e0a-382">**タスク ウィンドウ**は、明細行番号を報告します。**TODO** コメントがコード内にあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-382">The **Task Window** reports the line number where the **TODO** comment can be found in the code.</span></span> <span data-ttu-id="a9e0a-383">コメントで **TODO** を使用するためのルールを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-383">Here are the rules for using **TODO** in comments:</span></span>

- <span data-ttu-id="a9e0a-384">**TODO** 文字列は、**//** スタイル、または **/** スタイルを使うコメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-384">The **TODO** string can appear in a comment that uses either the **//** style or the **/** style.</span></span>
- <span data-ttu-id="a9e0a-385">**"TODO"** 文字列は、コメント内の最初の空白文字以外の文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-385">The **TODO** string must be the very first non–white space string in the comment.</span></span> <span data-ttu-id="a9e0a-386">キャリッジ リターン、改行、タブ、およびスペース、すべて空白と見なされます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-386">A carriage return, a line feed, a tab, and a space are all considered white space.</span></span>
- <span data-ttu-id="a9e0a-387">コメントの開始と **"仕事"** の間に空白は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-387">No white space is required between the start of the comment and the **TODO**.</span></span>
- <span data-ttu-id="a9e0a-388">**TODO** 文字列では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-388">The **TODO** string is case-insensitive.</span></span> <span data-ttu-id="a9e0a-389">ただし、規則では **ToDo** またはその他のバリエーションの代わりに、全大文字で **TODO** が入力されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-389">However, the convention is to type **TODO** in all uppercase letters, instead of **ToDo** or another variation.</span></span>
- <span data-ttu-id="a9e0a-390">**TODO** 文字列には任意の文字を追加できます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-390">The **TODO** string can have any characters appended to it.</span></span> <span data-ttu-id="a9e0a-391">ただし、規則は、コロンを **TODO** 文字列に追加するかまたは空白で続けるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-391">However, the convention is either to append a colon to the **TODO** string or to follow it with a white space.</span></span>
- <span data-ttu-id="a9e0a-392">**TODO** 文字列の後のコメントの残りは、タスク記述として報告されます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-392">The rest of the comment after the **TODO** string is reported as the task description.</span></span> <span data-ttu-id="a9e0a-393">コメントが 200 文字よりも長い場合は、**タスク** タブで切り詰められるとうに表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-393">If the comment is longer than 200 characters, it might appear truncated on the **Tasks** tab.</span></span>
- <span data-ttu-id="a9e0a-394">**/** コメント スタイルが使用されている場合、**TODO** タスクの説明は複数行にまたがることができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-394">The**TODO** task description can be spread over multiple lines when the **/** comment style is used.</span></span>

### <a name="examples-of-todo-comments"></a><span data-ttu-id="a9e0a-395">TODO コメントの例</span><span class="sxs-lookup"><span data-stu-id="a9e0a-395">Examples of TODO comments</span></span>

<span data-ttu-id="a9e0a-396">次の例では、**//** と **/** スタイルを使用する <strong>TODO</strong> コメントを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-396">The following examples show <strong>TODO</strong> comments that use the **//** and **/** styles.</span></span>

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

## <a name="unsupported-statements-changesite-pause-and-window"></a><span data-ttu-id="a9e0a-397">構文はサポートされていません: changeSite、一時停止、およびウィンドウ</span><span class="sxs-lookup"><span data-stu-id="a9e0a-397">Unsupported statements: changeSite, pause, and window</span></span>
<span data-ttu-id="a9e0a-398">**changeSite**、**pause**、**window** キーワードは、X++ 言語の一部ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-398">The **changeSite**, **pause**, and **window** keywords are no longer a part of the X++ language.</span></span> <span data-ttu-id="a9e0a-399">これらのキーワードを使用すると、コンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-399">These keywords will cause compilation errors if you use them.</span></span>

## <a name="using-clauses"></a><span data-ttu-id="a9e0a-400">句の使用</span><span class="sxs-lookup"><span data-stu-id="a9e0a-400">using clauses</span></span>
<span data-ttu-id="a9e0a-401">タイプの完全修飾名を指定する必要がないように、**using** 句を使用します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-401">You use **using** clauses so that you don't have to provide the fully qualified name of a type.</span></span> <span data-ttu-id="a9e0a-402">**using** 句は、適用されるクラスの前に配置する必要があり、適用先のすべてのソース ファイルに必要です。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-402">The **using** clause must precede the class that it applies, and it's required in every source file that you want it to apply to.</span></span> <span data-ttu-id="a9e0a-403">すべての **using** 句は通常、ソース ファイルの先頭に配置します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-403">Typically, all **using** clauses are put at the beginning of the source file.</span></span> <span data-ttu-id="a9e0a-404">完全修飾名の短縮名を導入するエイリアスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-404">You can also provide aliases that introduce a short name for a fully qualified name.</span></span> <span data-ttu-id="a9e0a-405">エイリアスは名前空間またはクラスを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-405">Aliases can denote namespaces or classes.</span></span> <span data-ttu-id="a9e0a-406">次の例では、**using** 句、名前空間エイリアス、およびクラス エイリアスを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-406">The following example shows a **using** clause, a namespace alias, and a class alias.</span></span>

    using System;
    using IONS=System.IO; // Namespace alias
    using Alist=System.Collections.ArrayList; // Class alias
    public class MyClass2
    {
        public static void Main(Args a)
        {
            Int32 I; // Alternative to System.Int32
            Alist al; // Using a class alias
            al = new Alist();
            str s;
            al.Add(1);
            s = IONS.Path::ChangeExtension(@"c:\tmp\test.xml", ".txt");
        }
    }

## <a name="using-statements"></a><span data-ttu-id="a9e0a-407">ステートメントの使用</span><span class="sxs-lookup"><span data-stu-id="a9e0a-407">using statements</span></span>
<span data-ttu-id="a9e0a-408">**using** ステートメントは、**IDisposable** を実行するオブジェクトが正しく破棄されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-408">The **using** statement helps guarantee that objects that implement **IDisposable** are disposed of correctly.</span></span> <span data-ttu-id="a9e0a-409">原則として、**IDisposable** オブジェクトを使用する場合は、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-409">When you use an **IDisposable** object, you should declare and instantiate it in a **using** statement.</span></span> <span data-ttu-id="a9e0a-410">**using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-410">The **using** statement calls the **Dispose** method on the object in the correct way, even if an exception occurs while you're calling methods on the object.</span></span> <span data-ttu-id="a9e0a-411">オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-411">You can achieve the same result by putting the object inside a **try** block and then explicitly calling **Dispose** in a **finally** block.</span></span> <span data-ttu-id="a9e0a-412">**using** ステートメントは構文を簡素化し、オブジェクトを正しく破棄します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-412">The **using** statement simplifies the syntax and disposes of the object correctly.</span></span> <span data-ttu-id="a9e0a-413">**using** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-413">Here is the syntax for a **using** statement:</span></span>

<span data-ttu-id="a9e0a-414">**(** *式* **) を使用して {** *明細書* **}**</span><span class="sxs-lookup"><span data-stu-id="a9e0a-414">**using (** *expression* **) {** *statement* **}**</span></span>

<span data-ttu-id="a9e0a-415">この構文では、*ステートメント*はステートメントのブロックとすることができ、*式*は **IDisposable** を実装するオブジェクトを宣言してインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-415">In this syntax, *statement* can be a block of statements, and *expression* declares and instantiates an object that implements **IDisposable**.</span></span> <span data-ttu-id="a9e0a-416">次の例では､**StreamReader** オブジェクトを作成して使用します。</span><span class="sxs-lookup"><span data-stu-id="a9e0a-416">The following example creates and uses a **StreamReader** object.</span></span>

    static void AnotherMethod()
    {
        str textFromFile;
        using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
        {
            textFromFile = sr.ReadToEnd();
        }
    }

