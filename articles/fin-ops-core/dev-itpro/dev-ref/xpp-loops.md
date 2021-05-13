---
title: X++ ループ ステートメント
description: このトピックでは、X++のループ ステートメントについて説明します。
author: RobinARH
ms.date: 06/17/2019
ms.topic: article
audience: Developer
ms.devlang: xpp
ms.reviewer: rhaertle
ms.custom: 150213
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f38914d926af5a60ff20cd159f73395a83920809
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865863"
---
# <a name="x-loop-statements"></a><span data-ttu-id="fc830-103">X++ ループ ステートメント</span><span class="sxs-lookup"><span data-stu-id="fc830-103">X++ loop statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc830-104">このトピックでは、X++のループ ステートメントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fc830-104">This topic describes loop statements in X++.</span></span> 

<span data-ttu-id="fc830-105">ループ ステートメントは、**for**、**while**、**do**、**while** の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="fc830-105">There are three loop statements: **for**, **while**, and **do**...**while**.</span></span> <span data-ttu-id="fc830-106">ループでは、ループに設定された条件が **false** になるまで、そのステートメントを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="fc830-106">A loop repeats its statement until the condition that is set for the loop is **false**.</span></span> <span data-ttu-id="fc830-107">loop ステートメント内では、**break** および **continue** ステートメントを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fc830-107">Within the loop statements, you can use **break** and **continue** statements.</span></span>

## <a name="for-loops"></a><span data-ttu-id="fc830-108">for ループ</span><span class="sxs-lookup"><span data-stu-id="fc830-108">for loops</span></span>

<span data-ttu-id="fc830-109">**for** ループの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc830-109">The syntax of a **for** loop is:</span></span>

<span data-ttu-id="fc830-110">**(** *初期化* **;** *テスト* **;** *増分* **) {** *明細書* **}** 対象</span><span class="sxs-lookup"><span data-stu-id="fc830-110">**for (** *initialization* **;** *test* **;** *increment* **) {** *statement* **}**</span></span>

<span data-ttu-id="fc830-111">**for** ループは、条件式 *テスト* が **true** である限り、 **ステートメント** を繰り返し実行します。</span><span class="sxs-lookup"><span data-stu-id="fc830-111">The **for** loop repeatedly executes **statement** for as long as the conditional expression *test* is **true**.</span></span> <span data-ttu-id="fc830-112">*ステートメント* はステートメントのブロックにすることができます。</span><span class="sxs-lookup"><span data-stu-id="fc830-112">*statement* can be a block of statements.</span></span> <span data-ttu-id="fc830-113">*テスト* の結果に応じて、 **for** ループの本文 (*ステートメント*) は、 0 回以上実行されることがあります。</span><span class="sxs-lookup"><span data-stu-id="fc830-113">The body of the **for** loop (*statement*) might be executed zero or more times, depending on the results of *test*.</span></span> 

<span data-ttu-id="fc830-114">**for** ループは、制御変数に初期値を割り当て、また変数の増減ステートメントがあるために、他のループとは異なります。</span><span class="sxs-lookup"><span data-stu-id="fc830-114">A **for** loop differs from other loops because an initial value can be assigned to a control variable, and because there is a statement for incrementing or decrementing the variable.</span></span> <span data-ttu-id="fc830-115">これらの追加は **for** ループを作成します。これは、リスト、コンテナー、配列をトラバースする場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="fc830-115">These additions make a **for** loop especially useful for traversing lists, containers, and arrays because they have a fixed number of elements.</span></span> 

<span data-ttu-id="fc830-116">また、明細書を各要素に適用して、要素全体を増分し、最後の要素をテストする条件を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fc830-116">You can also apply a statement to each element and increment your way through the elements, setting the condition to test for the last element.</span></span>

### <a name="example-of-a-for-loop"></a><span data-ttu-id="fc830-117">For loop の例</span><span class="sxs-lookup"><span data-stu-id="fc830-117">Example of a for loop</span></span>

<span data-ttu-id="fc830-118">次のコード例では、整数の配列内の項目が出力されます。</span><span class="sxs-lookup"><span data-stu-id="fc830-118">In the following code example, the items in an array of integers are printed.</span></span>

```xpp
int integers[10];
for (int i = 0; i < 10; i++)
{
    info(int2str(integers[i]));
}
// The output is a series of 0's.
```

## <a name="while-loops"></a><span data-ttu-id="fc830-119">while loops</span><span class="sxs-lookup"><span data-stu-id="fc830-119">while loops</span></span>

<span data-ttu-id="fc830-120">**while** ループの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc830-120">The syntax of a **while** loop is:</span></span>

<span data-ttu-id="fc830-121">**(** *式* **)** のとき、*明細書*</span><span class="sxs-lookup"><span data-stu-id="fc830-121">**while (** *expression* **)** *statement*</span></span>

<span data-ttu-id="fc830-122">**while** ループは、条件 *式* が **true** である限り、 *ステートメント* を繰り返し実行します。</span><span class="sxs-lookup"><span data-stu-id="fc830-122">A **while** loop repeatedly executes *statement* for as long as the conditional *expression* is **true**.</span></span> <span data-ttu-id="fc830-123">*ステートメント* はステートメントのブロックで置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="fc830-123">*statement* can be replaced by a block of statements.</span></span> <span data-ttu-id="fc830-124">*ステートメント* は、条件が満たされた回数 (ゼロから多数) 実行されます。</span><span class="sxs-lookup"><span data-stu-id="fc830-124">*statement* is executed as many times as the condition is met (zero to many).</span></span> 

### <a name="example-of-a-while-loop"></a><span data-ttu-id="fc830-125">While loop の例</span><span class="sxs-lookup"><span data-stu-id="fc830-125">Example of a while loop</span></span>

<span data-ttu-id="fc830-126">次のコード例は、コンテナーを走査してコンテナーの内容を出力する **while** ループを示します。</span><span class="sxs-lookup"><span data-stu-id="fc830-126">The following code example demonstrates a **while** loop that traverses a container and prints out the contents of the container.</span></span>

```xpp
container cont = ["one", "two", "three"];
int no = 0;
while (no <= conlen(cont))
{
    info(conPeek(cont, no));
    no++;
}
// The output is "one", "two", "three".
```

## <a name="dowhile-loops"></a><span data-ttu-id="fc830-127">do...while ループ</span><span class="sxs-lookup"><span data-stu-id="fc830-127">do...while loops</span></span>

<span data-ttu-id="fc830-128">**do...while** の構文ループは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc830-128">The syntax of the **do...while** loop is:</span></span>

<span data-ttu-id="fc830-129">**do {** *ステートメント* **} while (** *式* **) ;**</span><span class="sxs-lookup"><span data-stu-id="fc830-129">**do {** *statement* **} while (** *expression* **) ;**</span></span>

<span data-ttu-id="fc830-130">**do**...**while** ループは、 **while** ループと似ていますが、条件は実行する必要がある *ステートメント* の後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc830-130">The **do**...**while** loop is similar to the **while** loop, but the condition appears after the *statement* that must be executed.</span></span> <span data-ttu-id="fc830-131">*ステートメント* はステートメントのブロックにすることができます。</span><span class="sxs-lookup"><span data-stu-id="fc830-131">*statement* can be a block of statements.</span></span> <span data-ttu-id="fc830-132">*ステートメント* は、 *ステートメント* の実行後にテストされるため、少なくとも 1 回は常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fc830-132">The *statement* is always executed at least one time, because the condition is tested after *statement* is executed.</span></span> <span data-ttu-id="fc830-133">**do**...**while** ループは、レポートのパラメーターの取得など、必ず 1 回以上実行する必要があるタスクに適しています。</span><span class="sxs-lookup"><span data-stu-id="fc830-133">The **do**...**while** loop is well-suited to tasks that must always be done at least one time, such as getting parameters for a report.</span></span> 

### <a name="example-of-a-dowhile-loop"></a><span data-ttu-id="fc830-134">Do の例...while loop</span><span class="sxs-lookup"><span data-stu-id="fc830-134">Example of a do...while loop</span></span>

<span data-ttu-id="fc830-135">次のコード例では、 `realNumber` より大きい10の最小累乗を検索します。</span><span class="sxs-lookup"><span data-stu-id="fc830-135">The following code example finds the smallest power of 10 that is larger than `realNumber`.</span></span>

```xpp
int FindPower(real realNumber)
{
    int exponent = -1;
    real curVal;

    do
    {
        exponent++;
        curVal = power(10, exponent);
    }
    while (realNumber > curVal);

    return exponent;
}
```

## <a name="continue-statement"></a><span data-ttu-id="fc830-136">ステートメントの続行</span><span class="sxs-lookup"><span data-stu-id="fc830-136">continue statement</span></span>

<span data-ttu-id="fc830-137">**continue** ステートメントは、**for**、**while**、または **do**...**while** ループの次の反復処理に直接移動する実行を発生させます。</span><span class="sxs-lookup"><span data-stu-id="fc830-137">The **continue** statement causes execution to move directly to the next iteration of a **for**, **while**, or **do**...**while** loop.</span></span> <span data-ttu-id="fc830-138">**実行** または **途中** で、すぐにテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="fc830-138">For **do** or **while**, the test is executed immediately.</span></span> <span data-ttu-id="fc830-139">**対象** ステートメントで、増分手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fc830-139">For a **for** statement, the increment step is executed.</span></span> 

### <a name="example-of-a-continue-statement"></a><span data-ttu-id="fc830-140">続行明細書の例</span><span class="sxs-lookup"><span data-stu-id="fc830-140">Example of a continue statement</span></span>

<span data-ttu-id="fc830-141">次のコード例では、 `Iarray[i] <= 0` の場合、ループ内の残りのステートメントは実行されず、 **if** ステートメントが再度試行される前に `i` が増分されます。</span><span class="sxs-lookup"><span data-stu-id="fc830-141">In the following code example, if `Iarray[i] <= 0`, the remaining statements in the loop are not executed, and `i` is incremented before the **if** statement is tried again.</span></span>

```xpp
int Iarray[100];
for (int i = 0; i < 100; i++)
{
    if (Iarray[i] <= 0)
    {
        Info("Will continue.");
        continue;
    }

    info("Did not continue.");
}
// The output is "Will continue." for all 100 interations.
```

## <a name="break-statement"></a><span data-ttu-id="fc830-142">break ステートメント</span><span class="sxs-lookup"><span data-stu-id="fc830-142">break statement</span></span>

<span data-ttu-id="fc830-143">ループ内の **break** ステートメントは、そのループを終了するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc830-143">The **break** statement within a loop is used to terminate that loop.</span></span> <span data-ttu-id="fc830-144">実行後、ループの後の最初のステートメントに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc830-144">Execution then moves to the first statement after the loop.</span></span>

### <a name="example-of-a-break-statement"></a><span data-ttu-id="fc830-145">break ステートメントの例</span><span class="sxs-lookup"><span data-stu-id="fc830-145">Example of a break statement</span></span>

<span data-ttu-id="fc830-146">**while** ループにおける **break** ステートメントの例</span><span class="sxs-lookup"><span data-stu-id="fc830-146">This example is uses a **break** statement within a **while** loop.</span></span> <span data-ttu-id="fc830-147">ループ内で使用すると、ループは終了し、ループに続くステートメントから実行が継続します。</span><span class="sxs-lookup"><span data-stu-id="fc830-147">When used within a loop, the loop is terminated and execution continues from the statement following the loop.</span></span> <span data-ttu-id="fc830-148">これは、 **do... while** と **for** ループでも機能します。</span><span class="sxs-lookup"><span data-stu-id="fc830-148">This works for **do... while** and **for** loops as well.</span></span> 

```xpp
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
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]