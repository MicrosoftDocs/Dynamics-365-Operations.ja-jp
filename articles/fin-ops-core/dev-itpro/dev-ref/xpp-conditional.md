---
title: X++ 条件付きステートメント
description: このトピックでは、X++の条件付きステートメントについて説明します。
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
ms.custom: 150213
ms.assetid: 16b30ff1-bb31-4f9d-8105-c73abd2455f6
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da572b40ca0919bfa9d5d620b8b02345d0ed4f2a
ms.sourcegitcommit: 260a820038c29f712e8f1483cca9315b6dd3df55
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778694"
---
# <a name="x-conditional-statements"></a><span data-ttu-id="33f28-103">X++ 条件付きステートメント</span><span class="sxs-lookup"><span data-stu-id="33f28-103">X++ conditional statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33f28-104">このトピックでは、X++の条件付きステートメントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="33f28-104">This topic describes conditional statements in X++.</span></span> <span data-ttu-id="33f28-105">条件付きステートメントは、**if**、**if**...**else**、**switch**、および 3 項演算子 (**?**) です。</span><span class="sxs-lookup"><span data-stu-id="33f28-105">The conditional statements are **if**, **if**...**else**, **switch**, and the ternary operator (**?**).</span></span> <span data-ttu-id="33f28-106">条件付きステートメントを使用して、コードのブロックを実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="33f28-106">You use conditional statements to specify whether a block of code is executed.</span></span> <span data-ttu-id="33f28-107">異なる条件文は、異なる状況において利点を提供する。</span><span class="sxs-lookup"><span data-stu-id="33f28-107">Different conditional statements offer advantages in different situations.</span></span>

## <a name="if-and-ifelse-statements"></a><span data-ttu-id="33f28-108">if および if...else ステートメント</span><span class="sxs-lookup"><span data-stu-id="33f28-108">if and if...else statements</span></span>

<span data-ttu-id="33f28-109">**if** ステートメントは、条件式を評価した後、条件式が **true** として評価された場合にステートメントまたは一連のステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="33f28-109">The **if** statement evaluates a conditional expression, and then executes a statement or a set of statements if the conditional expression is evaluated as **true**.</span></span> <span data-ttu-id="33f28-110">**else** 句を使用すると、条件が **false** と評価される場合に実行される代替ステートメントまたは一連のステートメントを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="33f28-110">You can use the **else** clause to provide an alternative statement or set of statements that is executed if the condition is evaluated as **false**.</span></span> <span data-ttu-id="33f28-111">**if**...**else** ステートメントの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="33f28-111">The syntax for an **if**...**else** statement is:</span></span>

<span data-ttu-id="33f28-112">**if (** *式* **)** *ステートメント* 
**\[else** *ステートメント* 
**\]**</span><span class="sxs-lookup"><span data-stu-id="33f28-112">**if (** *expression* **)** *statement* 
**\[else** *statement* 
**\]**</span></span>

<span data-ttu-id="33f28-113">この構文では、 どちらの *ステートメント* も複合ステートメント (中括弧で囲まれたステートメント) にすることができます。</span><span class="sxs-lookup"><span data-stu-id="33f28-113">In this syntax, both occurrences of *statement* can be compound statements (statements enclosed in braces).</span></span> <span data-ttu-id="33f28-114">かっこで囲まれた*式* (条件式) は、**true** または **false** として評価される有効な式にすることができます。</span><span class="sxs-lookup"><span data-stu-id="33f28-114">The *expression* in the parentheses (the conditional expression) can be any valid expression that is evaluated as **true** or **false**.</span></span> <span data-ttu-id="33f28-115">0 (ゼロ) を除くすべての番号は **true** です。</span><span class="sxs-lookup"><span data-stu-id="33f28-115">All numbers except 0 (zero) are **true**.</span></span> <span data-ttu-id="33f28-116">空でない文字列はすべて **true** です。</span><span class="sxs-lookup"><span data-stu-id="33f28-116">All non-empty strings are **true**.</span></span> <span data-ttu-id="33f28-117">**if** ステートメントは入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="33f28-117">You can nest **if** statements.</span></span> <span data-ttu-id="33f28-118">ただし、**if** ステートメントの入れ子が深すぎる場合、**switch** ステートメントを代わりに使用することを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33f28-118">However, if the nesting of **if** statements becomes too deep, you should consider using a **switch** statement instead.</span></span>

### <a name="examples-of-if-and-ifelse-statements"></a><span data-ttu-id="33f28-119">if および if...else ステートメントの例</span><span class="sxs-lookup"><span data-stu-id="33f28-119">Examples of if and if...else statements</span></span>

```X++
// if statement
if (a > 4)
{
   info("a is greater than 4");
}

// if... else statement 
if (a > 4)
{
   info("a is greater than 4");
}
else
{
   info("a is less than or equal to 4");
}
```

## <a name="switch-statements"></a><span data-ttu-id="33f28-120">switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="33f28-120">switch statements</span></span>

<span data-ttu-id="33f28-121">**Switch** ステートメントは、ネストされた **if** と同じ動作をするマルチブランチ言語コンストラクトです。</span><span class="sxs-lookup"><span data-stu-id="33f28-121">The **switch** statement is a multibranch language construct that has the same behavior as nested **if**.</span></span> <span data-ttu-id="33f28-122">**switch** ステートメントの式が評価され、それぞれの Case の値に対してチェックされます。</span><span class="sxs-lookup"><span data-stu-id="33f28-122">The expression of the **switch** statement is evaluated and checked against each case value.</span></span> <span data-ttu-id="33f28-123">大文字と小文字の値は、コンパイラが評価できる定数でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="33f28-123">The case values must be constants that the compiler can evaluate.</span></span> 

- <span data-ttu-id="33f28-124">ケース定数が**切り替え**式と一致する場合、**case** ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="33f28-124">If a case constant matches the **switch** expression, the **case** statement is executed.</span></span> 
- <span data-ttu-id="33f28-125">そのケースに **break** ステートメントが含まれている場合、プログラムはスイッチからジャンプ アウトします。</span><span class="sxs-lookup"><span data-stu-id="33f28-125">If the case contains a **break** statement, the program then jumps out of the switch.</span></span> 
- <span data-ttu-id="33f28-126">ケースに **break** ステートメントが含まれていない場合、プログラムは継続し、次の **ケース** ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="33f28-126">If the case doesn't contain a **break** statement, the program continues and executes the next **case** statements.</span></span> 
- <span data-ttu-id="33f28-127">一致が見つからない場合、**既定**ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="33f28-127">If no matches are found, the **default** statement is executed.</span></span> 
- <span data-ttu-id="33f28-128">一致するものがなく、**default** ステートメントがない場合、**switch** ステートメント内のステートメントは実行されません。</span><span class="sxs-lookup"><span data-stu-id="33f28-128">If there are no matches and no **default** statement, none of the statements inside the **switch** statement are executed.</span></span> 

<span data-ttu-id="33f28-129">**switch** ステートメントの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="33f28-129">Here is the syntax for a **switch** statement:</span></span>

<span data-ttu-id="33f28-130">**switch** **(** *式* **)** **{** **{ ケース }** **\[既定:** *ステートメント* **\]** **}**</span><span class="sxs-lookup"><span data-stu-id="33f28-130">**switch** **(** *expression* **)** **{** **{ case }** **\[default:** *statement* **\]** **}**</span></span>

<span data-ttu-id="33f28-131">**case** ステートメントの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="33f28-131">The syntax for a **case** statement is:</span></span>

<span data-ttu-id="33f28-132">**case** *式* **{ 、** *式* **} :** *ステートメント*</span><span class="sxs-lookup"><span data-stu-id="33f28-132">**case** *expression* **{ ,** *expression* **} :** *statement*</span></span>

<span data-ttu-id="33f28-133">**switch** ステートメントおよび **case** ステートメントの両方の構文で、 *ステートメント* があるごとに、かっこ ({}) でブロックを囲むことでステートメントのブロックを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="33f28-133">In the syntax for both a **switch** statement and a **case** statement, every occurrence of *statement* can be replaced with a block of statements by enclosing the block in braces ({}).</span></span>

### <a name="examples-of-switch-statements"></a><span data-ttu-id="33f28-134">切り替え明細書の例</span><span class="sxs-lookup"><span data-stu-id="33f28-134">Examples of switch statements</span></span>

<span data-ttu-id="33f28-135">Switch ステートメントに **break** キーワードを含めると、case ブランチの実行は終了し、switch に続くステートメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="33f28-135">When you include the **break** keyword in a switch statement, the execution of the case branch terminates, and the statement following the switch is executed.</span></span> <span data-ttu-id="33f28-136">次の例のように、Debtor のアカウント番号が 1000 の場合、プログラムは "作業をする" が実行され、 switch ステートメントの後で実行が継続されます。</span><span class="sxs-lookup"><span data-stu-id="33f28-136">As shown in the following example, if the Debtor account number is 1000, the program executes "do something", and then continues execution after the switch statement.</span></span>

```X++
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
```

<span data-ttu-id="33f28-137">次のコード例では、breakステートメントを省略して最初のcase 分岐から実行をドロップします。</span><span class="sxs-lookup"><span data-stu-id="33f28-137">The following code examples makes the execution drop through the first case branch by omitting a break statement.</span></span> <span data-ttu-id="33f28-138">Xが10の場合、bはaに割り当てられ、dはcに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="33f28-138">If x is 10, b is assigned to a, and d is assigned to c.</span></span> <span data-ttu-id="33f28-139">Xが11の場合、dはcに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="33f28-139">If x is 11, d is assigned to c.</span></span> <span data-ttu-id="33f28-140">Xが12の場合、fはeに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="33f28-140">If x is 12, f is assigned to e.</span></span>

```X++
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
```

<span data-ttu-id="33f28-141">Break ステートメントを使用しない場合は、switch ステートメントのプログラム フローが次のケースに進みます。</span><span class="sxs-lookup"><span data-stu-id="33f28-141">If you do not use the break statement, the program flow in the switch statement continues into the next case.</span></span> <span data-ttu-id="33f28-142">コード セグメント AとBには同じ動作が設定されています。</span><span class="sxs-lookup"><span data-stu-id="33f28-142">Code segments A and B have the same behavior.</span></span> 

```X++
// Code segment A (break omitted)
case 13:
case 17:
case 21:
case 500:
    info("g");
    break;

// Code segment B (the values are comma-delimited)
case 13, 17, 21, 500;
    info("g");
    break;
```

## <a name="ternary-operator-"></a><span data-ttu-id="33f28-143">三項演算子 (?)</span><span class="sxs-lookup"><span data-stu-id="33f28-143">Ternary operator (?)</span></span>

<span data-ttu-id="33f28-144">三項演算子 (**?**) は、2 つの式のうちの 1 つに解決される条件文です。</span><span class="sxs-lookup"><span data-stu-id="33f28-144">The ternary operator (**?**) is a conditional statement that is resolved to one of two expressions.</span></span> <span data-ttu-id="33f28-145">結果は、変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="33f28-145">The result can be assigned to a variable.</span></span> <span data-ttu-id="33f28-146">対照的に、**if** ステートメントはプログラム フローの条件付き分岐を提供しますが、変数に割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="33f28-146">By contrast, an **if** statement provides conditional branching of the program flow but can't be assigned to a variable.</span></span> <span data-ttu-id="33f28-147">三項演算子の構文を次に示します:</span><span class="sxs-lookup"><span data-stu-id="33f28-147">Here is the syntax for the ternary operator:</span></span>

<span data-ttu-id="33f28-148">*式1* **?**</span><span class="sxs-lookup"><span data-stu-id="33f28-148">*expression1* **?**</span></span> <span data-ttu-id="33f28-149">*式2* **:** *式3*</span><span class="sxs-lookup"><span data-stu-id="33f28-149">*expression2* **:** *expression3*</span></span>

<span data-ttu-id="33f28-150">この構文では、*expression1* は **true** または **false** の値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="33f28-150">In this syntax, *expression1* must return a value of **true** or **false**.</span></span> <span data-ttu-id="33f28-151">*expression1* が **true** である場合、三項全体の明細書は*式*を返します。</span><span class="sxs-lookup"><span data-stu-id="33f28-151">If *expression1* is **true**, the whole ternary statement returns *expression2*.</span></span> <span data-ttu-id="33f28-152">それ以外の場合、ステートメントは *expression3* を返します。</span><span class="sxs-lookup"><span data-stu-id="33f28-152">Otherwise, the statement returns *expression3*.</span></span> <span data-ttu-id="33f28-153">*expression2* と *expression3* の両方は同じタイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="33f28-153">Both *expression2* and *expression3* must have the same type.</span></span>

### <a name="examples-of-the-ternary-operator-"></a><span data-ttu-id="33f28-154">三項演算子 (?) の例</span><span class="sxs-lookup"><span data-stu-id="33f28-154">Examples of the ternary operator (?)</span></span>

<span data-ttu-id="33f28-155">次のコード例では、メソッド呼び出しからのブール値の戻り値に基づいて、2つの文字列のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="33f28-155">The following code example returns one of two strings based on a Boolean return value from a method call.</span></span> <span data-ttu-id="33f28-156">ブール式は、CustTable テーブルに、RecIdフィールド値を1とする行が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="33f28-156">The Boolean expression indicates whether the CustTable table has a row with a RecId field value of 1.</span></span> <span data-ttu-id="33f28-157">このブール式が true (つまり、RecId! = 0) である場合は、found が結果に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="33f28-157">If this Boolean expression is true (meaning RecId != 0), found is assigned to result.</span></span> <span data-ttu-id="33f28-158">それ以外の場合、代替のnot foundが結果に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="33f28-158">Otherwise, the alternative not found is assigned to result.</span></span>

```X++
result = (custTable::find("1").RecId) ? "found" : "not found";
```

<span data-ttu-id="33f28-159">三項演算子を使用してステートメントをネストできます。</span><span class="sxs-lookup"><span data-stu-id="33f28-159">You can nest statements with the ternary operator.</span></span> <span data-ttu-id="33f28-160">次の例では、 **x** の値に基づいて、3つの値のいずれかを **レベル** に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="33f28-160">The following example assigns one of three values to **level** based on the value of **x**.</span></span>

```X++
int x = 1001;
str level = x <= 1000 ? "A" : (x <= 2000 ? "B" : "C");
info(level);
// Output is "B".
```
