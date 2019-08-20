---
title: X++ でのマクロ
description: このトピックでは、X++ でマクロを作成および使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 189441
ms.assetid: a2de1498-2c9d-4c5d-b396-5c8703a5ef72
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10174865081a41cf6f2b953179113e5dbaba0ded
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833612"
---
# <a name="macros-in-x"></a><span data-ttu-id="ba176-103">X++ でのマクロ</span><span class="sxs-lookup"><span data-stu-id="ba176-103">Macros in X++</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba176-104">このトピックでは、X++ でマクロを作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba176-104">This topic describes how to create and use macros in X++.</span></span>

<span data-ttu-id="ba176-105">コードをコンパイルする前に、プリコンパイラ ディレクティブが処理されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-105">Precompiler directives are processed before the code is compiled.</span></span> <span data-ttu-id="ba176-106">ディレクティブは、マクロとその値を宣言して処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-106">The directives declare and handle macros and their values.</span></span> <span data-ttu-id="ba176-107">ディレクティブは、プリコンパイラによって削除され、X++ コンパイラがそれらを検出することはありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-107">The directives are removed by the precompiler so that the X++ compiler never encounters them.</span></span> <span data-ttu-id="ba176-108">X++ コンパイラは、ディレクティブによって X++ コードに書き込まれた一連の文字だけを認識します。</span><span class="sxs-lookup"><span data-stu-id="ba176-108">The X++ compiler only sees the sequence of characters written into the X++ code by the directives.</span></span>

## <a name="define-and-if-directives"></a><span data-ttu-id="ba176-109">\#define および \#if ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-109">\#define and \#if directives</span></span>
<span data-ttu-id="ba176-110">すべてのプリコンパイラの指令および記号は \# 文字から始まります。</span><span class="sxs-lookup"><span data-stu-id="ba176-110">All precompiler directives and symbols begin with the \# character.</span></span> <span data-ttu-id="ba176-111">マクロは、コード内の任意の時点で定義できます。</span><span class="sxs-lookup"><span data-stu-id="ba176-111">A macro can be defined at any point in the code.</span></span> <span data-ttu-id="ba176-112">変数は一連の文字である値を持つことができますが、値を持つ必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-112">The variable can have a value that is a sequence of characters, but it is not required to have a value.</span></span> <span data-ttu-id="ba176-113">**\#define** ディレクティブは、省略可能な値を含む、マクロ変数を作成するようプリコンパイラに指示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-113">The **\#define** directive tells the precompiler to create the macro variable, including an optional value.</span></span> <span data-ttu-id="ba176-114">**\#if** ディレクティブは、変数が定義されているかどうか、および必要に応じて、特定の値があるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="ba176-114">The **\#if** directive tests whether the variable is defined, and optionally, whether it has a specific value.</span></span> <span data-ttu-id="ba176-115">X++ プリコンパイラ ディレクティブ、それが定義するマクロ名、および **\#if** ディレクティブ値テストではすべて、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-115">The X++ precompiler directives, the macro names that they define, and the **\#if** directive value tests are all case-insensitive.</span></span> <span data-ttu-id="ba176-116">ただし、マクロ名を大文字で始めるのがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="ba176-116">However, it is a best practice to begin macro names with an uppercase letter.</span></span>

### <a name="code-example"></a><span data-ttu-id="ba176-117">コードの例</span><span class="sxs-lookup"><span data-stu-id="ba176-117">Code example</span></span>

<span data-ttu-id="ba176-118">次のコード サンプルでは、**MyMacro** というマクロが定義されています。</span><span class="sxs-lookup"><span data-stu-id="ba176-118">In the following code sample, a macro named **MyMacro** is defined.</span></span> <span data-ttu-id="ba176-119">**\#define.MyMacro** 定義の行に値は指定されません。</span><span class="sxs-lookup"><span data-stu-id="ba176-119">It is not given a value in the **\#define.MyMacro** definition line.</span></span> <span data-ttu-id="ba176-120">したがって、値が長さゼロの文字列であるかのように動作します。</span><span class="sxs-lookup"><span data-stu-id="ba176-120">Therefore it behaves as if the value is a zero-length sequence of characters.</span></span> <span data-ttu-id="ba176-121">**\#if.MyMacro** ステートメントは、**MyMacro** が定義されているかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="ba176-121">The **\#if.MyMacro** statement tests whether **MyMacro** is defined.</span></span> <span data-ttu-id="ba176-122">**MyMacro** が定義されているため、最初の **\#endif** より前のコード行はテスト場所の X++ コードに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ba176-122">Because **MyMacro** is defined, the lines of code before the first **\#endif** are included in the X++ code at the test location.</span></span> <span data-ttu-id="ba176-123">例の最後の方に、**\#ifnot.MyMacro** テストがあります。</span><span class="sxs-lookup"><span data-stu-id="ba176-123">Near the end of the example there is an **\#ifnot.MyMacro** test.</span></span> <span data-ttu-id="ba176-124">**MyMacro** が定義されているため、そのテストは false であり X++ コードには行が書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="ba176-124">Because **MyMacro** is defined, that test is false and no lines are written into the X++ code.</span></span> <span data-ttu-id="ba176-125">このメソッドのプリコンパイル フェーズが終了した後、**MyMacro** の定義はスコープ外となり、もはやシステムとして認識されなくなります。</span><span class="sxs-lookup"><span data-stu-id="ba176-125">After the precompile phase ends for this method, the **MyMacro** definition goes out of scope and is no longer known to the system.</span></span>

    static void SimpleDefineIfJob(Args _args)
    {
        str sTest = "Initial value.";

        #define.MyMacro // MyMacro is now defined.
        #if.MyMacro
            sTest = "Yes, MyMacro is defined.";
            info(sTest);
        #endif
        // Notice the non-code sentence line causes no X++ compiler error,
        // because the X++ compiler never sees it.
        #ifnot.MyMacro
            The X++ compiler would reject this sentence.
            sTest = "No, MyMacro is not defined.";
            info(sTest);
        #endif
    /********** Actual output
    Message (03:46:20 pm)
    Yes, MyMacro is defined.
    **********/
    }

## <a name="precompile-and-compile-error-messages"></a><span data-ttu-id="ba176-126">エラー メッセージのプリコンパイルとコンパイル</span><span class="sxs-lookup"><span data-stu-id="ba176-126">Precompile and Compile Error Messages</span></span>
<span data-ttu-id="ba176-127">マクロを含むコードを作成するときは、プリコンパイル中またはコンパイル中にエラー メッセージが生成されたかどうかを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba176-127">When you are developing code that contains macros, you must understand whether an error message is generated during the precompile or the compile phase.</span></span> <span data-ttu-id="ba176-128">探し出す 2 つのキーワードは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ba176-128">The two key words to look for are:</span></span>

-   <span data-ttu-id="ba176-129">語彙: これはプリコンパイル エラーを示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-129">Lexical – This indicates a precompile error.</span></span>
-   <span data-ttu-id="ba176-130">構文: これはコンパイル エラーを示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-130">Syntax – This indicates a compile error.</span></span>

<span data-ttu-id="ba176-131">次のコード例では、ディレクティブの最後を示す最初の閉じかっこによって引き起こされる語彙エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="ba176-131">The following code example has a lexical error caused by the first closing parenthesis, which marks the end of the directive.</span></span> <span data-ttu-id="ba176-132">したがって、プリコンパイラは最後の 2 文字 "";)" で混乱します。</span><span class="sxs-lookup"><span data-stu-id="ba176-132">Therefore the precompiler is confused by the last two characters, "";)".</span></span>

    #define.MyMacro1(info("Hello");)

<span data-ttu-id="ba176-133">次のコード例では、存在しない **++++** 演算子を使用したために構文エラーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-133">The following code example has a syntax error caused by using the non-existent **++++** operator.</span></span> <span data-ttu-id="ba176-134">X++ コンパイラは、**\#MyMacro2** がマクロの値に置き換えられた後に、この演算子を検出します。</span><span class="sxs-lookup"><span data-stu-id="ba176-134">The X++ compiler encounters this operator after **\#MyMacro2** is replaced by the macro value.</span></span> <span data-ttu-id="ba176-135">マクロ定義は、その値が X++ 構文で受け付けられていなくても正しいです。</span><span class="sxs-lookup"><span data-stu-id="ba176-135">The macro definition is correct even though its value is not accepted X++ syntax.</span></span>

    #define.MyMacro2(++++iTest;) 
    #MyMacro2

## <a name="undef-directive"></a><span data-ttu-id="ba176-136">\#undef ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-136">\#undef directive</span></span>
<span data-ttu-id="ba176-137">**\#undef** ディレクティブを使用すると、以前の **\#define** から存在するマクロ定義を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-137">You can use the **\#undef** directive to remove a macro definition that exists from a previous **\#define.**</span></span> <span data-ttu-id="ba176-138">マクロ名が **\#define** によって作成され、**\#undef** によって削除された後、別の **\#define** によってマクロが再度作成されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-138">After a macro name has been created by **\#define** and then removed by **\#undef,** the macro can be created again by another **\#define.**</span></span> <span data-ttu-id="ba176-139">**\#undef** は、**\#localmacro** ディレクティブで作成されたマクロには影響しません。</span><span class="sxs-lookup"><span data-stu-id="ba176-139">**\#undef** has no effect on macros that are created by the **\#localmacro** directive.</span></span> <span data-ttu-id="ba176-140">次のコード サンプルでは、マクロ **MyMacro** は \#undef ディレクティブを使用して未定義となります。</span><span class="sxs-lookup"><span data-stu-id="ba176-140">In the following code sample, the macro **MyMacro** is undefined by using the \#undef directive.</span></span> <span data-ttu-id="ba176-141">\#undef は、その存在の 2 つの \#if テスト間で発生します。</span><span class="sxs-lookup"><span data-stu-id="ba176-141">The \#undef occurs between the two \#if tests for its existence.</span></span> <span data-ttu-id="ba176-142">出力は、最初の \#if テストのみが真であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-142">The output shows only the first \#if test was true.</span></span>

    static void UndefMacroJob(Args _args)
    {
        #define.MyMacro
        #if.MyMacro
            info("Macro is defined (1)");
        #endif
        #undef.MyMacro // Removes the macro.
        #if.MyMacro
            info("Macro is defined (2)");
        #endif
    /************* Actual output
    Message (10:19:15 am)
    Macro is defined (1)
    *************/
    }

## <a name="use-a-macro-value"></a><span data-ttu-id="ba176-143">マクロ値の使用</span><span class="sxs-lookup"><span data-stu-id="ba176-143">Use a Macro Value</span></span>
<span data-ttu-id="ba176-144">値を持つマクロ名を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-144">You can define a macro name to have a value.</span></span> <span data-ttu-id="ba176-145">マクロの値は、文字の並びです。</span><span class="sxs-lookup"><span data-stu-id="ba176-145">A macro value is a sequence of characters.</span></span> <span data-ttu-id="ba176-146">マクロの値は、データ型の正式な意味での文字列 (または **str**) ではありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-146">A macro value is not a string (or **str**) in the formal sense of a data type.</span></span> <span data-ttu-id="ba176-147">\#define ディレクティブの最後にあるかっこで囲まれた値を加えることにより、値をマクロに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ba176-147">You assign a value to a macro by appending the value enclosed in parentheses at the end of a \#define directive.</span></span> <span data-ttu-id="ba176-148">X++ コードで発生する値を必要とする箇所ではマクロ記号を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-148">You can use the macro symbol where you want the value to occur in the X++ code.</span></span> <span data-ttu-id="ba176-149">マクロ記号は、接頭語として追加された \# 文字を持つマクロの名前です。</span><span class="sxs-lookup"><span data-stu-id="ba176-149">A macro symbol is the name of the macro with the \# character added as a prefix.</span></span> <span data-ttu-id="ba176-150">次のコード例では、マクロ記号 **\#MyMacro** を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-150">The following code sample shows a macro symbol **\#MyMacro.**</span></span> <span data-ttu-id="ba176-151">シンボルはマクロの値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ba176-151">The symbol is replaced by the value of the macro.</span></span>

    static void MacroWithIntValueJob(Args _args)
    {
        int iTest = 8;
        ;
        #define.MyMacro(32)
        // This next #define, which has no value for the macro name,
        // would not disrupt the value 32 set by the previous #define.
        //#define.MyMacro
        // This next #define, which has a different value than 32,
        // would overwrite the value 32 set by the previous #define.
        //#define.MyMacro(444)
        iTest = #MyMacro;
        info(int2str(iTest));
    /**********  Actual output
    Message (04:33:49 pm)
    32
    **********/
    }

## <a name="test-a-macro-value"></a><span data-ttu-id="ba176-152">マクロ値のテスト</span><span class="sxs-lookup"><span data-stu-id="ba176-152">Test a Macro Value</span></span>
<span data-ttu-id="ba176-153">値があるかどうかを確認するマクロをテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-153">You can test a macro to see whether it has a value.</span></span> <span data-ttu-id="ba176-154">また、値が特定の文字の並びと等しいか確認するためにテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-154">You can also test to see whether its value is equal to a specific sequence of characters.</span></span> <span data-ttu-id="ba176-155">これらのテストでは、条件付きで X++ プログラムにコード行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-155">These tests enable you to conditionally include lines of code in your X++ program.</span></span> <span data-ttu-id="ba176-156">定義されたマクロに値があるかどうかをテストする方法はありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-156">There is no way you can test whether a defined macro has a value.</span></span> <span data-ttu-id="ba176-157">特定の値がマクロの値に一致するかどうかのみテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-157">You can only test whether a specific value matches the value of a macro.</span></span> <span data-ttu-id="ba176-158">ベスト プラクティスとしては、定義するマクロ名は常に値を持つ必要があります。または、決して値を持つことができません。</span><span class="sxs-lookup"><span data-stu-id="ba176-158">As a best practice, any macro name that you define should always have a value, or it should never have a value.</span></span> <span data-ttu-id="ba176-159">これらのモードを交互に使用するときは、コードを理解することが困難になります。</span><span class="sxs-lookup"><span data-stu-id="ba176-159">When you alternate between these modes, your code becomes difficult to understand.</span></span> <span data-ttu-id="ba176-160">値を持つマクロについては、フィットの検索時によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ba176-160">For macros that have a value, you can vary the value when you see fit.</span></span> <span data-ttu-id="ba176-161">次のコード サンプルでは、2 つの **\#if** テストが実行され、マクロ **MyIntMacro** が存在するかどうか判定します。</span><span class="sxs-lookup"><span data-stu-id="ba176-161">In the following code sample, two **\#if** tests are run to determine whether the macro **MyIntMacro** exists.</span></span> <span data-ttu-id="ba176-162">**\#if.MyIntMacro()** テストが true です。</span><span class="sxs-lookup"><span data-stu-id="ba176-162">The **\#if.MyIntMacro()** test is true.</span></span> <span data-ttu-id="ba176-163">この構文の動作は、**\#if.MyIntMacro.** と同じです。</span><span class="sxs-lookup"><span data-stu-id="ba176-163">This syntax behaves the same as **\#if.MyIntMacro.**</span></span>

    static void TestMacroValue6Job(Args _args)
    {
        #define.MyIntMacro(66)
        // #if tests.
        #if.MyIntMacro()
            info("A: " + int2str(#MyIntMacro));
        #endif
        #if.MyIntMacro(66)
            info("B: " + int2str(#MyIntMacro));
        #endif
        // #ifNOT tests.
        #ifNOT.MyIntMacro(7777)
            info("C: " + int2str(#MyIntMacro));
        #endif
        #ifNOT.No_Such_Macro_Name(66)
            info("D: " + int2str(#MyIntMacro));
        #endif
    /****************  Actual output
    Message (11:24:47 am)
    A: 66
    B: 66
    C: 66
    D: 66
    ****************/
    }

<span data-ttu-id="ba176-164">次のコード例は、**DebugMacro** マクロの値をテストする **\#if.DebugMacro(heavy)** ディレクティブを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-164">The following code sample shows the **\#if.DebugMacro(heavy)** directive that tests the value of the **DebugMacro** macro.</span></span> <span data-ttu-id="ba176-165">値が 5 文字シーケンス **heavy** である場合、テストは true になります。</span><span class="sxs-lookup"><span data-stu-id="ba176-165">If the value is the five character sequence **heavy**, then the test is true.</span></span>

    static void TestMacroSpecificValue8Job(Args _args)
    {
        ;
        // Uncomment either one of these defines, or neither.
        //#define.DebugMacro(light) // This line for: light debugging.
        #define.DebugMacro(heavy) // This line for: heavy debugging.
        #if.DebugMacro
            info("Starting the job.");
        #endif
        #if.DebugMacro(heavy)
            info("UTC == "
                + DateTimeUtil ::toStr
                    (DateTimeUtil::utcNow()
                    )
                );
        #endif
        // Do something useful here.
    /**********  Actual output
    Message (01:58:12 pm)
    Starting the job.
    UTC == 2007-12-05T21:58:12
    **********/
    }

## <a name="definc-and-defdec-directives"></a><span data-ttu-id="ba176-166">\#defInc および \#defDec ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-166">\#defInc and \#defDec directives</span></span>
<span data-ttu-id="ba176-167">**\#defInc** および **\#defDec** は、マクロの値を解釈する唯一のディレクティブであり、正式な **int** タイプに変換できる値を持つマクロにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-167">**\#defInc** and **\#defDec** are the only directives that interpret the value of a macro and they apply only to macros that have a value that can be converted to the formal **int** type.</span></span> <span data-ttu-id="ba176-168">値は、数字のみを含むことができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-168">The value can only contain numerals.</span></span> <span data-ttu-id="ba176-169">唯一の数字以外の文字は、先頭にマイナス記号 (-) が付いています。</span><span class="sxs-lookup"><span data-stu-id="ba176-169">The only non-numeric character allowed is a leading negative sign (-).</span></span> <span data-ttu-id="ba176-170">整数値は、**int64** ではなく、X++ **int** として扱われます。</span><span class="sxs-lookup"><span data-stu-id="ba176-170">The integer value is treated as an X++ **int**, not as an **int64**.</span></span> <span data-ttu-id="ba176-171">**\#defInc** ディレクティブにより使用されるマクロ名については、マクロを作成する**\#定義** ディレクティブがクラス宣言に配置されないようにすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="ba176-171">For macro names that are used by the **\#defInc** directive, it is important that the **\#define** directive that creates the macro not reside in a class declaration.</span></span> <span data-ttu-id="ba176-172">これらの場合の **\#defInc** の動作は予測できません。</span><span class="sxs-lookup"><span data-stu-id="ba176-172">The behavior of **\#defInc** in these cases is unpredictable.</span></span> <span data-ttu-id="ba176-173">代わりに、このようなマクロはメソッドだけで定義される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba176-173">Instead, such macros should be defined in only a method.</span></span> <span data-ttu-id="ba176-174">整数値を持つマクロには **\#defInc** および **\#defDec** ディレクティブのみを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba176-174">We recommend that the **\#defInc** and **\#defDec** directives only be used for macros that have an integer value.</span></span> <span data-ttu-id="ba176-175">プリコンパイラは、マクロの値が整数でないとき、あるいは値が異常または極端なとき、**\#defInc** の特別なルールに従います。</span><span class="sxs-lookup"><span data-stu-id="ba176-175">The precompiler follows special rules for **\#defInc** when the macro value is not an integer, or when the value is unusual or extreme.</span></span> <span data-ttu-id="ba176-176">次のテーブルは、**\#defInc** がゼロ (0) に変換してから増分する値を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-176">The following table lists the values that **\#defInc** converts to zero (0) and then increments.</span></span> <span data-ttu-id="ba176-177">**\#defInc、** によって値が 0 に変換されると、**\#defDec** によっても元の値を回復できません。</span><span class="sxs-lookup"><span data-stu-id="ba176-177">When a value is converted to 0 by **\#defInc,** the original value cannot be recovered, not even by **\#defDec.**</span></span>

| <span data-ttu-id="ba176-178">マクロの値</span><span class="sxs-lookup"><span data-stu-id="ba176-178">Macro value</span></span>       | <span data-ttu-id="ba176-179">動作</span><span class="sxs-lookup"><span data-stu-id="ba176-179">Behavior</span></span>                                                                                                                                                                                               |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba176-180">(+55)</span><span class="sxs-lookup"><span data-stu-id="ba176-180">(+55)</span></span>             | <span data-ttu-id="ba176-181">プラス記号 (+) 接頭語により、プリコンパイラはこれを数字以外の文字列として扱います。</span><span class="sxs-lookup"><span data-stu-id="ba176-181">The positive sign (+) prefix makes the precompiler treat this as a non-numeric string.</span></span> <span data-ttu-id="ba176-182">プリコンパイラは、**\#defInc** (または **\#識別子)** ディレクティブを扱うとき、数値以外のすべての文字列を 0 として処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-182">The precompiler treats all non-numeric strings as 0 when it handles a **\#defInc** (or **\#defDec)** directive.</span></span> |
| <span data-ttu-id="ba176-183">(「3」)</span><span class="sxs-lookup"><span data-stu-id="ba176-183">("3")</span></span>             | <span data-ttu-id="ba176-184">引用符で囲まれた整数は、0 として扱われます。</span><span class="sxs-lookup"><span data-stu-id="ba176-184">Integers enclosed in quotation marks are treated as 0.</span></span> <span data-ttu-id="ba176-185">引用符は破棄され、これらの変更はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="ba176-185">The quotation marks are discarded, and these changes persist.</span></span>                                                                                   |
| <span data-ttu-id="ba176-186">( )</span><span class="sxs-lookup"><span data-stu-id="ba176-186">( )</span></span>               | <span data-ttu-id="ba176-187">スペースの文字列が 0 として扱われ、増加します。</span><span class="sxs-lookup"><span data-stu-id="ba176-187">A string of spaces is treated as 0, and then incremented.</span></span>                                                                                                                                              |
| <span data-ttu-id="ba176-188">()</span><span class="sxs-lookup"><span data-stu-id="ba176-188">()</span></span>                | <span data-ttu-id="ba176-189">長さゼロの文字列は、0 として処理され、**\#define.MyMac()** のように、値がかっこで囲まれている場合は増加します。</span><span class="sxs-lookup"><span data-stu-id="ba176-189">A zero-length string is treated as 0, and then incremented, when the value is enclosed in parentheses, as in **\#define.MyMac().**</span></span>                                                                     |
| <span data-ttu-id="ba176-190">(ランダムな文字列です。)</span><span class="sxs-lookup"><span data-stu-id="ba176-190">(Random string.)</span></span>  | <span data-ttu-id="ba176-191">数値以外の文字列は 0 として扱われ、次に増加します。</span><span class="sxs-lookup"><span data-stu-id="ba176-191">Any non-numeric string of characters is treated as 0, and then incremented.</span></span>                                                                                                                            |
| <span data-ttu-id="ba176-192">(0x12)</span><span class="sxs-lookup"><span data-stu-id="ba176-192">(0x12)</span></span>            | <span data-ttu-id="ba176-193">16 進数は、数値以外の文字列として扱われます。</span><span class="sxs-lookup"><span data-stu-id="ba176-193">Hexadecimal numbers are treated as non-numeric strings.</span></span> <span data-ttu-id="ba176-194">したがって、それらは 0 に変換され、次に増分されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-194">Therefore they are converted to 0, and then incremented.</span></span>                                                                                       |
| <span data-ttu-id="ba176-195">(-44)</span><span class="sxs-lookup"><span data-stu-id="ba176-195">(-44)</span></span>             | <span data-ttu-id="ba176-196">マイナス記号 (-) のない整数を含め、負の数は許容されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-196">Negative numbers are acceptable, including integers without the negative sign (-).</span></span>                                                                                                                     |
| <span data-ttu-id="ba176-197">(2147483647)</span><span class="sxs-lookup"><span data-stu-id="ba176-197">(2147483647)</span></span>      | <span data-ttu-id="ba176-198">最大の正の **int** 値は、\#defInc によって最小の負の **int** 値に変更されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-198">The maximum positive **int** value is changed to the minimum negative **int** value by \#defInc.</span></span>                                                                                                       |
| <span data-ttu-id="ba176-199">(999888777666555)</span><span class="sxs-lookup"><span data-stu-id="ba176-199">(999888777666555)</span></span> | <span data-ttu-id="ba176-200">**int** および **int64** の容量を超えた大きな数。</span><span class="sxs-lookup"><span data-stu-id="ba176-200">Any large number, beyond the capacity of **int** and **int64**.</span></span> <span data-ttu-id="ba176-201">これは最大の正の **int** 値として扱われます。</span><span class="sxs-lookup"><span data-stu-id="ba176-201">This is treated as the maximum positive **int** value.</span></span>                                                                                 |
| <span data-ttu-id="ba176-202">(5.8)</span><span class="sxs-lookup"><span data-stu-id="ba176-202">(5.8)</span></span>             | <span data-ttu-id="ba176-203">実数は、\#defDec (および \#defInc) により切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="ba176-203">Real numbers are truncated by \#defDec (and \#defInc).</span></span> <span data-ttu-id="ba176-204">後続の記号置き換えは、切り捨てが永続化することを示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-204">Subsequent symbol substitution shows that the truncation persists.</span></span>                                                                              |
|                   | <span data-ttu-id="ba176-205">\#define.MyValuelessMacro ディレクティブの値とかっこが指定されていない場合は、プリコンパイラは \#defInc.MyValuelessMacro ディレクティブの使用を拒否します。</span><span class="sxs-lookup"><span data-stu-id="ba176-205">When no value and no parentheses are provided for the directive \#define.MyValuelessMacro, the precompiler rejects use of the directive \#defInc.MyValuelessMacro.</span></span>                                     |

### <a name="code-example"></a><span data-ttu-id="ba176-206">コードの例</span><span class="sxs-lookup"><span data-stu-id="ba176-206">Code example</span></span>

<span data-ttu-id="ba176-207">次のコード サンプルでは、マクロ **CounterMacroA** の初期値は、整数に変換できる文字列です。</span><span class="sxs-lookup"><span data-stu-id="ba176-207">In the following code sample, the initial value of the macro **CounterMacroA** is a string that can be converted into an integer.</span></span> <span data-ttu-id="ba176-208">サンプルでは、このマクロ名に **\#defInc** および **\#defDec** の各ディレクティブをどのように使用できるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-208">The sample shows how the **\#defInc** and **\#defDec** directives can be used for this macro name.</span></span>

    static void SimpleDefINCJob(Args _args)
    {
        ;
        #define.CounterMacroA(1)
        #defInc.CounterMacroA
        info("mg11: # CounterMacroA == " + int2str(#CounterMacroA));
        #if.CounterMacroA(2)
            info("mg12: # if confirms CounterMacroA == 2");
        #endif
        #defDec.CounterMacroA
        info("mg23: # CounterMacroA == " + int2str(#CounterMacroA));
        #if.CounterMacroA(1)
            info("mg24: # if confirms CounterMacroA == 1");
        #endif
    /**************  Actual Infolog output
    Message (12:47:57 pm)
    mg11: # CounterMacroA == 2
    mg12: # if confirms CounterMacroA == 2
    mg23: # CounterMacroA == 1
    mg24: # if confirms CounterMacroA == 1
    **************/
    }

## <a name="globaldefine-directive"></a><span data-ttu-id="ba176-209">\#globaldefine ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-209">\#globaldefine directive</span></span>
<span data-ttu-id="ba176-210"><strong>\#Globaldefine</strong> ディレクティブは、<strong>\#define</strong> ディレクティブに似ています。</span><span class="sxs-lookup"><span data-stu-id="ba176-210">The <strong>\#globaldefine</strong> directive is similar to the <strong>\#define</strong> directive.</span></span> <span data-ttu-id="ba176-211">違いは、<strong>\#define</strong> ディレクティブは一般的に <strong>\#globalmacro</strong> ディレクティブよりも優先されるということです。</span><span class="sxs-lookup"><span data-stu-id="ba176-211">The difference is that <strong>\#define</strong> directives generally take precedence over <strong>\#globalmacro</strong> directives.</span></span> <span data-ttu-id="ba176-212">これは、どのディレクティブが最初に X++ コードで発生するかに関係なく当てはまります。</span><span class="sxs-lookup"><span data-stu-id="ba176-212">This is true regardless of which directive occurs first in the X++ code.</span></span> <span data-ttu-id="ba176-213"><strong>\#globaldefine</strong> は、マクロ名と値の両方を持つ <strong>\#define</strong> ディレクティブを上書きすることはありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-213">A <strong>\#globaldefine</strong> never overwrites a <strong>\#define</strong> directive that has both a macro name and a value.</span></span> <span data-ttu-id="ba176-214"><strong>\#globaldefine</strong> は別の <strong>\#globaldefine を上書きすることができます。\*\*A \*\*\#define</strong> ディレクティブは、名前と値の両方を持つ \#globalmacro を上書きしません。</span><span class="sxs-lookup"><span data-stu-id="ba176-214">A <strong>\#globaldefine</strong> can overwrite another <strong>\#globaldefine. \*\*A \*\*\#define</strong> directive that has only a name does not overwrite a \#globalmacro that has both a name and a value.</span></span> <span data-ttu-id="ba176-215"><strong>\#define</strong> を使用して <strong>\#globaldefine</strong> を使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba176-215">It is recommended that you use <strong>\#define,</strong> and that you do not use <strong>\#globaldefine.</strong></span></span> <span data-ttu-id="ba176-216"><strong>\#globaldefine</strong> を使用すると、不確実性が生じてコードの保守が困難になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ba176-216">Use of <strong>\#globaldefine</strong> can create uncertainty that makes code difficult to maintain.</span></span> <span data-ttu-id="ba176-217"><strong>\#globaldefine</strong> の正確なセマンティクスは、<strong>\#if</strong> テストディレクティブでは達成できません。</span><span class="sxs-lookup"><span data-stu-id="ba176-217">The exact semantics of <strong>\#globaldefine</strong> cannot be achieved through <strong>\#if</strong> test directives.</span></span> <span data-ttu-id="ba176-218"><strong>\#if</strong> テストを使うことにより <strong>\#define</strong> および <strong>\#globaldefine</strong> の上書きを回避することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-218">By using <strong>\#if</strong> tests you can avoid overwriting a <strong>\#define</strong> and a <strong>\#globaldefine.</strong></span></span> <span data-ttu-id="ba176-219">ただし、<strong>\#if</strong> テストは <strong>\#define</strong> と <strong>\#globaldefine</strong> マクロを区別できません。</span><span class="sxs-lookup"><span data-stu-id="ba176-219">But <strong>\#if</strong> tests cannot distinguish between <strong>\#define</strong> and <strong>\#globaldefine</strong> macros.</span></span> <span data-ttu-id="ba176-220">次のコード例は、<strong>\#if</strong> などの他のディレクティブで <strong>\#globaldefine</strong> セマンティクスを達成するために最も近い例です。</span><span class="sxs-lookup"><span data-stu-id="ba176-220">The following code sample is the closest you can come to achieving the <strong>\#globaldefine</strong> semantic with other directives such as <strong>\#if.</strong></span></span>

    static void IfNotDefineNestGlobalJob (Args _args)
    {
        ;
        #undef.MaybeMac
        #ifnot.MaybeMac
            #define.MaybeMac(4444) // Works.
        #endif
        #if.MaybeMac
            info(int2str(#MaybeMac));
        #endif
    /**********************  Actual Infolog output
    Message (07:43:32 pm)
    4444
    **********************/
    }

### <a name="code-example"></a><span data-ttu-id="ba176-221">コードの例</span><span class="sxs-lookup"><span data-stu-id="ba176-221">Code example</span></span>

<span data-ttu-id="ba176-222">次のコード例は、**\#define** と **\#globaldefine** の動作の違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-222">The following code sample shows a difference in the behavior of **\#define** and **\#globaldefine.**</span></span> <span data-ttu-id="ba176-223">以下のコード サンプルは、出力からの結びを説明するテーブルです。</span><span class="sxs-lookup"><span data-stu-id="ba176-223">Following the code sample is a table explaining the conclusions from the output.</span></span> <span data-ttu-id="ba176-224">コード サンプルの基本テスト ケースの名前は **12** です。</span><span class="sxs-lookup"><span data-stu-id="ba176-224">The primary test case in the code sample is labeled **12**.</span></span>

    static void InteractDefineGlobalJob(Args _args)
    {
        ;
        // Pairs of #define - #globaldefine directives (same macro names).
        #define.11_DEFINEvalue_GLOBALnoval("11__DEFINE.")
        #globaldefine.11_DEFINEvalue_GLOBALnoval
        #define.12_DEFINEnoval_GLOBALvalue
        #globaldefine.12_DEFINEnoval_GLOBALvalue("12_GLOBAL.")
        #define.13_DEFINEvalue_GLOBALvalue("13__DEFINE.")
        #globaldefine.13_DEFINEvalue_GLOBALvalue("13_GLOBAL.")
        // Pairs of #globaldefine - #define directives.
        #globaldefine.27_GLOBALvalue_DEFINEnoval("27_GLOBAL.")
        #define.27_GLOBALvalue_DEFINEnoval
        #globaldefine.28_GLOBALnoval_DEFINEvalue
        #define.28_GLOBALnoval_DEFINEvalue("28__DEFINE.")
        #globaldefine.29_GLOBALvalue_DEFINEvalue("29_GLOBAL.")
        #define.29_GLOBALvalue_DEFINEvalue("29__DEFINE.")
        // Pairs of same directive types.
        #define.50_DEFINEvalue_DEFINEnoval("50__DEFINE 1.")
        #define.50_DEFINEvalue_DEFINEnoval
        #globaldefine.64_GLOBALvalue_GLOBALnoval("64_GLOBAL 1.")
        #globaldefine.64_GLOBALvalue_GLOBALnoval
        #globaldefine.65_GLOBALnoval_GLOBALvalue
        #globaldefine.65_GLOBALnoval_GLOBALvalue("65_GLOBAL 2.")
        #globaldefine.66_GLOBALvalue_GLOBALvalue("66_GLOBAL 1.")
        #globaldefine.66_GLOBALvalue_GLOBALvalue("66_GLOBAL 2.")
        // Infolog outputs.
        info(#11_DEFINEvalue_GLOBALnoval);
        info(#12_DEFINEnoval_GLOBALvalue);
        info(#13_DEFINEvalue_GLOBALvalue);
        info(#27_GLOBALvalue_DEFINEnoval);
        info(#28_GLOBALnoval_DEFINEvalue);
        info(#29_GLOBALvalue_DEFINEvalue);
        info(#50_DEFINEvalue_DEFINEnoval);
        info(#64_GLOBALvalue_GLOBALnoval);
        info(#65_GLOBALnoval_GLOBALvalue);
        info(#66_GLOBALvalue_GLOBALvalue);
    /*****************************  Actual Infolog output
    Message (09:31:26 pm)
    11__DEFINE.
    12_GLOBAL. Shows that #globaldefine overwrites #define when #globaldefine is giving a value to an existing macro that has no value. Test cases 13 and 29 are more common and realistic.
    13__DEFINE. Shows that #define usually takes precedence over #globaldefine, regardless of which directive occurs first in the X++ code. Test case 12 shows this is not always true.
    27_GLOBAL.
    28__DEFINE.
    29__DEFINE. Shows that #define usually takes precedence over #globaldefine, regardless of which directive occurs first in the X++ code. Test case 12 shows this is not always true.
    50__DEFINE 1. Shows that a #globaldefine that has a name but no value does not overwrite a #globaldefine that has both a name and a value. The same is true between a pair of #define directives. This resembles test case 12.
    64_GLOBAL 1. Shows that a #globaldefine that has a name but no value does not overwrite a #globaldefine that has both a name and a value. The same is true between a pair of #define directives. This resembles test case 12.
    65_GLOBAL 2. Shows that a #globaldefine that has both a name and a value overwrites a previous #globaldefine.
    66_GLOBAL 2. Shows that a #globaldefine that has both a name and a value overwrites a previous #globaldefine.
    *****************************/
    }

## <a name="macro-parameters"></a><span data-ttu-id="ba176-225">マクロ パラメーター</span><span class="sxs-lookup"><span data-stu-id="ba176-225">Macro parameters</span></span>
<span data-ttu-id="ba176-226">パラメータ シンボルを含めるようにマクロの値を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-226">You can define macro values to include parameter symbols.</span></span> <span data-ttu-id="ba176-227">最初のパラメーター記号は %1、2 番目のパラメーター記号は %2 で、以降は同様の形式です。</span><span class="sxs-lookup"><span data-stu-id="ba176-227">The first parameter symbol is %1, the second is %2, and so on.</span></span> <span data-ttu-id="ba176-228">展開のためにマクロ記号名を参照するときは、パラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="ba176-228">You pass values for the parameters when you reference the macro symbol name for expansion.</span></span> <span data-ttu-id="ba176-229">マクロ パラメーターの値は、正式な型のない文字シーケンスで、コンマで区切られます。</span><span class="sxs-lookup"><span data-stu-id="ba176-229">Macro parameter values are character sequences of no formal type, and they are comma delimited.</span></span> <span data-ttu-id="ba176-230">パラメーター値の一部としてカンマで渡す方法はありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-230">There is no way to pass in a comma as part of a parameter value.</span></span> <span data-ttu-id="ba176-231">渡されるパラメーターの数は、マクロ値が受け取るように設計されているパラメーターの数よりも少なくても、大きくても等しくてもかまいません。</span><span class="sxs-lookup"><span data-stu-id="ba176-231">The number of parameters passed can be less than, greater than, or equal to the number of parameters that the macro value is designed to receive.</span></span> <span data-ttu-id="ba176-232">システムは、渡されたパラメーターの数の不一致を許容します。</span><span class="sxs-lookup"><span data-stu-id="ba176-232">The system tolerates mismatches in the number of parameters passed.</span></span> <span data-ttu-id="ba176-233">マクロが期待するよりも少ないパラメーターが指定された場合、省略された各パラメーターは、長さが 0 の文字列として扱われます。</span><span class="sxs-lookup"><span data-stu-id="ba176-233">If fewer parameters are passed than the macro expects, each omitted parameter is treated as a zero-length sequence of characters.</span></span> <span data-ttu-id="ba176-234">次のコード サンプルでは、**MyMacro** はパラメーターを含む値を持つよう定義されています。</span><span class="sxs-lookup"><span data-stu-id="ba176-234">In the following code sample, **MyMacro** is defined to have a value that contains parameters.</span></span> <span data-ttu-id="ba176-235">マクロの代入記号は、かっこで囲まれたパラメーターの値で指定されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-235">Macro substitution symbols are given with parameter values in parentheses.</span></span>

    static void MacroParameterSubstitutionJob(Args _args)
    {
        ;
        #define.MyMacro("One == [%1] ,  Two == [%2]")
        // Make parameter substitutions:
        info("AA: " + #MyMacro(Apple));
        info("BB: " + #MyMacro(Apple,Banana));
        info("CC: " + #MyMacro(Apple, Banana, cranberry));
        info("DD: " + #MyMacro(,Apple,Banana));
        info("EE: " + #MyMacro());
        info("FF: " + #MyMacro);
    /************  Actual Infolog output
    Message (03:22:07 pm)
    AA: One == [Apple] ,  Two == []
    BB: One == [Apple] ,  Two == [Banana]
    CC: One == [Apple] ,  Two == [ Banana]
    DD: One == [] ,  Two == [Apple]
    EE: One == [] ,  Two == []
    FF: One == [] ,  Two == []
    ************/
    }

## <a name="localmacro-and-globalmacro-directives"></a><span data-ttu-id="ba176-236">\#localmacro および \#globalmacro ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-236">\#localmacro and \#globalmacro directives</span></span>
<span data-ttu-id="ba176-237"><strong>\#Localmacro</strong> ディレクティブは、複数の行にまたがる値をマクロに設定する場合や、マクロの値にかっこが含まれている場合に推奨されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-237">The <strong>\#localmacro</strong> directive is a good choice when you want a macro to have a value that is several lines long, or when your macro value contains a closing parenthesis.</span></span> <span data-ttu-id="ba176-238"><strong>\#localmacro</strong> ディレクティブは、マクロの値を数行の X++ または SQL コードにする場合に推奨されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-238">The <strong>\#localmacro</strong> directive is a good choice when you want your macro value to be lines of X++ or SQL code.</span></span> <span data-ttu-id="ba176-239"><strong>\#Localmacro</strong> ディレクティブは、<strong>\#macro.</strong> として記述することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-239">The <strong>\#localmacro</strong> directive can be written as <strong>\#macro.</strong></span></span> <span data-ttu-id="ba176-240">ただし、<strong>\#localmacro</strong> が勧められている用語です。</span><span class="sxs-lookup"><span data-stu-id="ba176-240">However, <strong>\#localmacro</strong> is the recommended term.</span></span> <span data-ttu-id="ba176-241">どちらのマクロも同じ動作をします。</span><span class="sxs-lookup"><span data-stu-id="ba176-241">Both macros have the same behavior.</span></span> <span data-ttu-id="ba176-242"><strong>\#if</strong> ディレクティブを使用することにより、マクロ名が <strong>\#define</strong> ディレクティブで宣言されているかどうかをテストできます。</span><span class="sxs-lookup"><span data-stu-id="ba176-242">By using the <strong>\#if</strong> directive, you can test whether a macro name is declared with the <strong>\#define</strong> directive.</span></span> <span data-ttu-id="ba176-243">ただし、マクロ名が <strong>\#localmacro</strong> ディレクティブで宣言されているどうかをテストすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ba176-243">However, you cannot test whether the macro name is declared with the <strong>\#localmacro</strong> directive.</span></span> <span data-ttu-id="ba176-244"><strong>\#define</strong> ディレクティブを使用して宣言されたマクロのみ、<strong>\#undef</strong> ディレクティブの影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="ba176-244">Only macros declared by using the <strong>\#define</strong> directive are affected by the <strong>\#undef</strong> directive.</span></span> <span data-ttu-id="ba176-245"><strong>\#define</strong> ディレクティブでは、既にスコープ内にある名前を <strong>\#localmacro</strong> として指定できます。</span><span class="sxs-lookup"><span data-stu-id="ba176-245">In a <strong>\#define</strong> directive, you can specify a name that is already in scope as a <strong>\#localmacro.</strong></span></span> <span data-ttu-id="ba176-246">結果は、<strong>\#localmacro</strong>を破棄して、<strong>\#define</strong> マクロを作成することです。</span><span class="sxs-lookup"><span data-stu-id="ba176-246">The effect is to discard the <strong>\#localmacro</strong> and create a <strong>\#define</strong> macro.</span></span> <span data-ttu-id="ba176-247">これは反対のシーケンスにも当てはまります。つまり、<strong>\#localmacro</strong> は <strong>\#define</strong> を再定義できます。</span><span class="sxs-lookup"><span data-stu-id="ba176-247">This also applies to the opposite sequence, which means that a <strong>\#localmacro</strong> can redefine a <strong>\#define.</strong></span></span> <span data-ttu-id="ba176-248">(マクロ名と値の両方を持つ) <strong>\#localmacro</strong> は、同じ名前を持つ前の <strong>\#localmacro</strong> を常に上書きします。</span><span class="sxs-lookup"><span data-stu-id="ba176-248">A <strong>\#localmacro</strong> (that has both a macro name and a value) always overrides a previous <strong>\#localmacro</strong> that has the same name.</span></span> <span data-ttu-id="ba176-249">ただし、<strong>\#globalmacro</strong> を使用する場合、オーバーライドが発生するかどうかは必ず分かるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="ba176-249">However, you cannot always be sure whether the override occurs when you use <strong>\#globalmacro.</strong></span></span> <span data-ttu-id="ba176-250">このため、<strong>\#globaldefine で**この同じ問題が発生**する \#globalmacro</strong> を使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba176-250">For this reason we recommend that you do not use <strong>\#globalmacro. \*\*This same problem occurs with \*\*\#globaldefine.</strong></span></span> <span data-ttu-id="ba176-251"><strong>\#define</strong> マクロと <strong>\#localmacro</strong> マクロの主な違いは、構文がどのように終了するかです</span><span class="sxs-lookup"><span data-stu-id="ba176-251">The main difference between a <strong>\#define</strong> macro and a <strong>\#localmacro</strong> macro is in how their syntax is terminated.</span></span> <span data-ttu-id="ba176-252">次のターミネーターがあります。</span><span class="sxs-lookup"><span data-stu-id="ba176-252">The terminators are as follows:</span></span>

-   <span data-ttu-id="ba176-253">**\#定義** - - によって終了 **)**</span><span class="sxs-lookup"><span data-stu-id="ba176-253">**\#define** – is terminated by– **)**</span></span>
-   <span data-ttu-id="ba176-254">**\#localmacro** - - によって終了 **\#endmacro**</span><span class="sxs-lookup"><span data-stu-id="ba176-254">**\#localmacro** – is terminated by– **\#endmacro**</span></span>

<span data-ttu-id="ba176-255">**\#localmacro** は、複数の行の値を持つマクロに適しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-255">**\#localmacro** is a better choice for macros with multiple line values.</span></span> <span data-ttu-id="ba176-256">複数の行の値は、通常 X++ または SQL コードの行です。</span><span class="sxs-lookup"><span data-stu-id="ba176-256">Multiple line values are typically lines of X++ or SQL code.</span></span> <span data-ttu-id="ba176-257">X++ および SQL には多くのパラメーターが含まれ、これらは処理の途中で \#define を終了する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ba176-257">X++ and SQL contain lots of parentheses, and these would prematurely terminate a \#define.</span></span> <span data-ttu-id="ba176-258">**\#定義**と **\#localmacro** の両方を宣言し、単一行または後続の行で終了することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-258">Both **\#define** and **\#localmacro** can be declared and terminated on either a single line or on subsequent lines.</span></span> <span data-ttu-id="ba176-259">実際、**\#define** は宣言されている同じ行で終了します。</span><span class="sxs-lookup"><span data-stu-id="ba176-259">In practice, the **\#define** is terminated on the same line that it is declared on.</span></span> <span data-ttu-id="ba176-260">実際、**\#localmacro** は後続の行で終了します。</span><span class="sxs-lookup"><span data-stu-id="ba176-260">In practice, the **\#localmacro** is terminated on a subsequent line.</span></span> <span data-ttu-id="ba176-261">マクロ名と値の両方を指定すると、**\#globalmacro** 指令は \#define 指令を上書きできません。</span><span class="sxs-lookup"><span data-stu-id="ba176-261">Where both macro names and values are supplied, the **\#globalmacro** directive cannot override the \#define directive.</span></span> <span data-ttu-id="ba176-262">また、**\#globaldefine** ディレクティブは **\#localmacro** ディレクティブへの上書きができません。</span><span class="sxs-lookup"><span data-stu-id="ba176-262">Also, the **\#globaldefine** directive cannot override the **\#localmacro** directive.</span></span>

### <a name="code-examples"></a><span data-ttu-id="ba176-263">コードの例</span><span class="sxs-lookup"><span data-stu-id="ba176-263">Code examples</span></span>

<span data-ttu-id="ba176-264">次のコード例は、**\#localmacro** ディレクティブの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-264">The following code sample shows how to use the **\#localmacro** directive.</span></span> <span data-ttu-id="ba176-265">**\#undef** ディレクティブが **\#localmacro** マクロに影響しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-265">It demonstrates that the **\#undef** directive does not affect **\#localmacro** macros.</span></span> <span data-ttu-id="ba176-266">また、\#if テストでは **\#localmacro** マクロが定義されているかどうかを決定できないことも示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-266">It also shows that \#if tests cannot determine whether a **\#localmacro** macro has been defined.</span></span>

    static void LocalMacroJob(Args _args)
    {
        ;
        #localmacro.LMacReportLog
            print("%1  --LM, print.");
            info("%1  --LM, Infolog.");
        #endmacro
        #LMacReportLog(g11: Hello World )
        #if.LMacReportLog
            info("The # IF LMacReportLog is true");
        #endif
        #undef.LMacReportLog
        #LMacReportLog(g22: Greetings World)
        #localmacro.LMacReportLog
        #endmacro // No lines for value before this end.
        #LMacReportLog(g33: Bye Bye) // Not present in the output.
    /*************  Actual Infolog output
    Message (03:10:17 pm)
    g11: Hello World   --LM, Infolog.
    g22: Greetings World  --LM, Infolog.
    *************/
    }

<span data-ttu-id="ba176-267">次の X++ コード例は、**\#localmacro** が同じマクロ名の **\#globalmacro** を上書きしますが、**\#globalmacro** は **\#localmacro** を上書きしないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-267">The following X++ code sample shows that **\#localmacro** overrides a **\#globalmacro** of the same macro name, but that **\#globalmacro** does not override **\#localmacro.**</span></span>

    static void GlobalMacroNotOverrideJob(Args _args)
    {
        ;
        //---------  LGMa ,  L then G  ---------
        #localmacro.LGMa
            info("LGMa: Loc 11");
        #endmacro
        #globalmacro.LGMa
            info("LGMa: Glob 12");
        #endmacro
        #LGMa
        //---------  LGMb ,  G then L  ---------
        #globalmacro.LGMb
            info("LGMb: Glob 24");
        #endmacro
        #localmacro.LGMb
            info("LGMb: Loc 25");
        #endmacro
        #LGMb
    /****************  Actual Infolog output
    Message (06:39:42 am)
    LGMa: Loc 11
    LGMb: Loc 25
    ****************/
    }

## <a name="nesting-macro-symbols"></a><span data-ttu-id="ba176-268">入れ子になっているマクロ記号</span><span class="sxs-lookup"><span data-stu-id="ba176-268">Nesting Macro Symbols</span></span>
<span data-ttu-id="ba176-269">プリコンパイラ定義ディレクティブは他の外部定義ディレクティブ内に入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-269">You can nest precompiler definition directives inside an outer definition directive.</span></span> <span data-ttu-id="ba176-270">主な定義ディレクティブは、**\#define** と \#localmacro です。</span><span class="sxs-lookup"><span data-stu-id="ba176-270">The main definition directives are **\#define** and \*\*\#localmacro.</span></span> <span data-ttu-id="ba176-271">\*\*このトピックでコード サンプルを提供する場合は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ba176-271">\*\*The cases for which this topic provides code samples are as follows:</span></span>

-   <span data-ttu-id="ba176-272">推移的置換: A **\#define** マクロは、別のマクロのシンボルをその値として持つことができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-272">Transitive substitution: A **\#define** macro can have the symbol for another macro as its value.</span></span> <span data-ttu-id="ba176-273">シンボルの推移的置換は X++ コードで行われます。</span><span class="sxs-lookup"><span data-stu-id="ba176-273">Transitive substitution of the symbol occurs in X++ code.</span></span>
-   <span data-ttu-id="ba176-274">推移的置換なし: マクロ値の **\#if** ディレクティブ テストは置換を実行しません。</span><span class="sxs-lookup"><span data-stu-id="ba176-274">No transitive substitution: An **\#if** directive test of a macro value does not perform substitutions.</span></span>
-   <span data-ttu-id="ba176-275">マクロ内のマクロ: \#define ディレクティブを **\#localmacro** ディレクティブ内に指定したり、**\#localmacro** を **\#define** 内に指定したりできます。</span><span class="sxs-lookup"><span data-stu-id="ba176-275">Macro within a macro: A \#define directive can be given inside a **\#localmacro** directive, or a **\#localmacro** can be inside a **\#define.**</span></span>

### <a name="transitive-substitution"></a><span data-ttu-id="ba176-276">推移的置換</span><span class="sxs-lookup"><span data-stu-id="ba176-276">Transitive Substitution</span></span>

<span data-ttu-id="ba176-277">次のコード例では、最初の **\#define** 変数の値には、2 つ目の **\#define** 変数の記号 (\#D) が含まれます</span><span class="sxs-lookup"><span data-stu-id="ba176-277">In the following code sample, the value of the first **\#define** variable includes a symbol (\#D) of the second **\#define** variable.</span></span> <span data-ttu-id="ba176-278">これは、マクロ **D** を定義する前に拡張シンボル \#D が存在していても機能します。</span><span class="sxs-lookup"><span data-stu-id="ba176-278">This works even though the expansion symbol \#D occurs before macro **D** is defined.</span></span>

    static void NestMacroJobA1(Args _args)
    {
        ;
        #define.Cd("Cd +: # D == " + #D)
        // If not commented out, this next code line would cause the
        // error message "The macro does not exist.", because
        // #D in the value of #Cd cannot be expanded before it is defined.
        //info(#Cd);
        #define.D("D")
        info(#Cd);
    /************  Actual Infolog output
    Message (10:42:13 am)
    Cd +: # D == D
    ************/
    }

### <a name="no-transitive-substitution"></a><span data-ttu-id="ba176-279">推移的置換なし</span><span class="sxs-lookup"><span data-stu-id="ba176-279">No transitive substitution</span></span>

<span data-ttu-id="ba176-280">次のコード例は、2 つのマクロ変数が同じ値を持っているかどうかを、その値が何であるかを指定せずに判断しようとしています。</span><span class="sxs-lookup"><span data-stu-id="ba176-280">The following code sample tries to determine whether two macro variables have the same value, without specifying what that value might be.</span></span> <span data-ttu-id="ba176-281">出力は、この決定が行えないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-281">The output shows that this determination cannot be made..</span></span>

    static void NestMacroJobA2(Args _args)
    {
        ;
        #define.A1(5)
        #define.A2(5)
        info("Status: A1==" + int2Str(#A1) + " , A2==" + int2Str(#A2));
        #if.A1(#A2)
            info("Yes, symbol substitution does work on # IF test.  Unexpected.");
        #endif
        #ifNOT.A1(#A2)
            info("No, symbol substitution does not work on # IF test.");
        #endif
    /************  Actual Infolog output
    Message (11:27:38 am)
    Status: A1==5 , A2==5
    No, symbol substitution does not work on # IF test.
    ************/
    }

<span data-ttu-id="ba176-282">次のコード例は、\#defInc ディレクティブが記号値の推移的置換につながっていないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-282">The following code sample shows that the \#defInc directive does not lead to transitive substitution of symbol values.</span></span> <span data-ttu-id="ba176-283">\#defInc ディレクティブの詳細については、方法: \#defInc および \#defDec ディレクティブの使用を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba176-283">For more information about the \#defInc directive, see How to: Use the \#defInc and \#defDec Directives.</span></span> <span data-ttu-id="ba176-284">\#defInc.E2 ディレクティブの後、\#E2 の次の出力値は、**E2** の値が 1 に増加する前に、\#defInc.E2 によってゼロ (0) に変換されることを示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-284">After the \#defInc.E2 directive, the subsequent output value for \#E2 shows the value for **E2** is converted to zero (0) by \#defInc.E2 before it is incremented to one (1).</span></span> <span data-ttu-id="ba176-285">変換する前に、**E2** の値は 3 文字 \#E2 でした。</span><span class="sxs-lookup"><span data-stu-id="ba176-285">Before the conversion, the value of **E2** was the three characters \#E2.</span></span> <span data-ttu-id="ba176-286">テスト ケースの出力 **36** は、値が 1 に変換されたことを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-286">The output for test case **36** shows the value has been converted to 1.</span></span>

    static void NestMacroJobA4(Args _args)
    {
        ;
        #define.E1(5)
        #define.E2(#E1)
        info("11:  # E1 == " + int2Str(#E1));
        info("12:  # E2 == " + int2Str(#E2));
        #defInc.E1
        info(" -------");
        info("23: After Inc.E1,  # E1 == " + int2Str(#E1));
        info("24: After Inc.E1,  # E2 == " + int2Str(#E2));
        #defInc.E2
        info(" -------");
        info("35: After Inc.E2,  # E1 == " + int2Str(#E1));
        info("36: After Inc.E2,  # E2 == " + int2Str(#E2));
    /************  Actual Infolog output
    Message (02:39:41 pm)
    11:  # E1 == 5
    12:  # E2 == 5
     -------
    23: After Inc.E1,  # E1 == 6
    24: After Inc.E1,  # E2 == 6
     -------
    35: After Inc.E2,  # E1 == 6
    36: After Inc.E2,  # E2 == 1
    ************/
    }

### <a name="macro-within-a-macro"></a><span data-ttu-id="ba176-287">マクロ内のマクロ</span><span class="sxs-lookup"><span data-stu-id="ba176-287">Macro within a macro</span></span>

<span data-ttu-id="ba176-288">**\#define** ディレクティブは **\#localmacro** 内に指定することができ、また **\#localmacro** ディレクティブを\# define 内に指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ba176-288">A **\#define** directive can be given inside a **\#localmacro** directive, and a **\#localmacro** can be inside a \#define.</span></span> <span data-ttu-id="ba176-289">これは、次のコード サンプルに示されています。</span><span class="sxs-lookup"><span data-stu-id="ba176-289">This is shown in the following code sample.</span></span>

    static void NestMacroJobB5(Args _args)
    {
        int iTest = 31;
        ;
        //-------------  J  ---------------
        #localmacro.LocMacOuterJL
            #define.DefinInnerJD(5)
        #endmacro
        #LocMacOuterJL
        info("J: Directive nesting works if 5 appears: # DefinInnerJD == "
                + int2Str(#DefinInnerJD));
        //-------------  K  ---------------
        #define.DefinOuterKD(#localmacro.LocMacInnerKL ++iTest; #endmacro)
        ++iTest; // Result is 32.
        #DefinOuterKD
        #LocMacInnerKL
        info("K: Directive nesting works if 33 appears: iTest == "
                + int2Str(iTest));
    /**************  Actual Infolog output
    Message (11:21:02 am)
    J: Directive nesting works if 5 appears: # DefinInnerJD == 5
    K: Directive nesting works if 33 appears: iTest == 33
    **************/
    }

## <a name="macrolib-directive"></a><span data-ttu-id="ba176-290">\#macrolib ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-290">\#macrolib directive</span></span>
<span data-ttu-id="ba176-291">マクロ ノードの下のアプリケーション エクスプローラーには、マクロ ディレクティブのセットが含まれる多くのライブラリ ノードがあります。</span><span class="sxs-lookup"><span data-stu-id="ba176-291">In the Application Explorer under the Macros node, there are many library nodes that contain sets of macro directives.</span></span> <span data-ttu-id="ba176-292">多くの場合、**\#定義**および **\#localmacro** の両方がこれらのマクロ ライブラリの内容に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-292">Both **\#define** and **\#localmacro** often appear in the contents of these macro libraries.</span></span> <span data-ttu-id="ba176-293">**\#macrolib.MyAOTMacroLibrary** を使用すると、マクロ ライブラリのコンテンツをユーザーの X++ コードに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-293">You can use the **\#macrolib.MyAOTMacroLibrary** to include the contents of a macro library in your X++ code.</span></span> <span data-ttu-id="ba176-294">**\#if** および **\#undef** ディレクティブは、**\#macrolib** 名には適用されません。</span><span class="sxs-lookup"><span data-stu-id="ba176-294">The **\#if** and **\#undef** directives do not apply to **\#macrolib** names.</span></span> <span data-ttu-id="ba176-295">ただし、それは **\#macrolib** マクロのコンテンツである**\#定義**ディレクティブに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-295">However, they do apply to **\#define** directives that are the contents of a **\#macrolib** macro.</span></span> <span data-ttu-id="ba176-296">ディレクティブ **\#macrolib.MyAOTMacroLibrary** は、**\#MyAOTMacroLibrary** として書き込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="ba176-296">The directive **\#macrolib.MyAOTMacroLibrary** can also be written as **\#MyAOTMacroLibrary.**</span></span> <span data-ttu-id="ba176-297">**\#macrolib** プレフィックスを使うと後でコードを読むときにあいまいにならないため、推奨されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-297">The **\#macrolib** prefix is recommended because it is never ambiguous to a person who later reads the code.</span></span>

### <a name="create-a-macro-library"></a><span data-ttu-id="ba176-298">マクロ ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="ba176-298">Create a macro library</span></span>

<span data-ttu-id="ba176-299">マクロ ライブラリを作成するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="ba176-299">To create a macro library:</span></span>

1.  <span data-ttu-id="ba176-300">**ソリューション エクスプローラー**で、プロジェクトを右クリックし、**追加**を選択してから**新しい項目**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba176-300">In **Solution Explorer,** right-click on the project, select **Add** and then **New item.**</span></span>
2.  <span data-ttu-id="ba176-301">**新しい項目の追加**ダイアログで、インストール済みを選択してから左ウィンドウの **AX アーティファクト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba176-301">In the **Add New Item** dialog, select Installed and then **AX Artifacts** in the left pane.</span></span>
3.  <span data-ttu-id="ba176-302">中央ウィンドウで**マクロ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba176-302">In the middle pane, select **Macro.**</span></span>
4.  <span data-ttu-id="ba176-303">名前を入力し、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba176-303">Enter a name and click **Add.**</span></span> <span data-ttu-id="ba176-304">マクロ ファイルを保存し、マクロ ライブラリを検索するためにアプリケーション エクスプローラーを更新します。</span><span class="sxs-lookup"><span data-stu-id="ba176-304">Save the macro file and refresh the Application Explorer to find your macro library.</span></span>

### <a name="code-examples"></a><span data-ttu-id="ba176-305">コードの例</span><span class="sxs-lookup"><span data-stu-id="ba176-305">Code examples</span></span>

<span data-ttu-id="ba176-306">Finance and Operations には**イベント**と呼ばれるマクロ ライブラリがあります。</span><span class="sxs-lookup"><span data-stu-id="ba176-306">Finance and Operations has a macro library that is named **Event.**</span></span> <span data-ttu-id="ba176-307">このマクロ ライブラリには、**\#define.DefaultEventPollFrequency(15)** という指令が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba176-307">This macro library contains the directive **\#define.DefaultEventPollFrequency(15)**.</span></span> <span data-ttu-id="ba176-308">次のコード例は、**\#macrolib.Event** ディレクティブがマクロ **\#DefaultEventPollFrequency** を使用可能にすることを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-308">The following code sample shows that the **\#macrolib.Event** directive makes the macro **\#DefaultEventPollFrequency** available.</span></span>

    static void SystemProvidedMacroLibraryJob(Args _args)
    {
        ;
        #macrolib.Event // Contains: #define.DefaultEventPollFrequency(15)
        info("# DefaultEventPollFrequency == "
                + int2str(#DefaultEventPollFrequency));
    /***************  Actual Infolog output
    Message (06:31:26 pm)
    # DefaultEventPollFrequency == 15
    ***************/
    }

次のコード例は、既にマクロ ライブラリ内のノードの名前である名前に対して **\#define** を記述するとどうなるかを示しています。 <span data-ttu-id="ba176-310">この例では、**MacLib23**という名前のノードがあり、その内容は次のように 1 つの**\#定義**です。</span><span class="sxs-lookup"><span data-stu-id="ba176-310">For this example, there is a node named **MacLib23,** and its contents are one **\#define** as follows:</span></span>

    #define.DefinInMacLib23("_This is inside AOT macrolib MacLib23.")

<span data-ttu-id="ba176-311">\#macrolib ディレクティブが **MacLib23** に対して発行された後、**\#define** と **\#undef** ディレクティブは、**\#macrolib** マクロに影響しません (出力 \_BB を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="ba176-311">After a \#macrolib directive is issued for **MacLib23**, **\#define** and **\#undef** directives have no effect on the **\#macrolib** macro (see output \_BB).</span></span> <span data-ttu-id="ba176-312">ただし、**\#macrolib** マクロのコンテンツでの**\#定義**は、それ以降のコードでの\#定義または **\#undef** により上書きされます (出力 \_DD を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="ba176-312">However, a **\#define** in the contents of a **\#macrolib** macro can be overwritten by a subsequent \#define or **\#undef** in the code (see output \_DD).</span></span>

    static void PrecedenceMacrolibDefineJob(Args _args)
    {
        ;
        #define.MacLib23("_11:  Plain #define value for MacLib23, same name as the AOT macrolib macro.")
        info("_AA: " + #MacLib23);
        #macrolib.MacLib23
        info("_BB: " + #DefinInMacLib23); // Defined inside the macrolib macro.
        info("_CC: " + #MacLib23); // Output shows plain #define, not the macrolib macro contents.
        #define.DefinInMacLib23("_33:  Plain #define in the job code, overwrite of same macro name defined inside the macrolib macro.")
        info("_DD: " + #DefinInMacLib23);
    /***************************  Actual Infolog output
    Message (10:53:13 am)
    _AA: 11:  Plain #define value for MacLib23, same name as the AOT macrolib macro.
    _BB: This is inside AOT macrolib MacLib23.
    _CC: 11:  Plain #define value for MacLib23, same name as the AOT macrolib macro.
    _DD: 33:  Plain #define in the job code, overwrite of same macro name defined inside the macrolib macro.
    ***************************/
    }

## <a name="linenumber-directive"></a><span data-ttu-id="ba176-313">\#linenumber ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="ba176-313">\#linenumber Directive</span></span>
<span data-ttu-id="ba176-314">開発中およびコードのデバッグ中は、\#linenumber ディレクティブを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-314">You can use the \#linenumber directive during your development and debugging of code.</span></span> <span data-ttu-id="ba176-315">これは、コード ファイル内の物理的な行番号に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ba176-315">It is replaced by the physical line number in the code file.</span></span>

### <a name="code-example"></a><span data-ttu-id="ba176-316">コードの例</span><span class="sxs-lookup"><span data-stu-id="ba176-316">Code example</span></span>

<span data-ttu-id="ba176-317">次の X++ コード例は、**\#linenumber** ディレクティブの動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-317">The following X++ code sample shows the behavior of the **\#linenumber** directive.</span></span>

    static void LinenumberPhysicalJob(Args _args)
    {
        ;
        #define.Debug(light)
        #if.Debug
            info("Physical Line 8: # linenumber == "
                + int2Str(#linenumber));
        #endif
    /******************  Actual Infolog output
    Message (08:55:26 pm)
    Physical Line 8: # linenumber == 8
    ******************/
    }

## <a name="range-scope-of-macros"></a><span data-ttu-id="ba176-318">マクロの範囲 (スコープ)</span><span class="sxs-lookup"><span data-stu-id="ba176-318">Range (scope) of macros</span></span>
<span data-ttu-id="ba176-319">マクロが参照できる範囲は、マクロが定義されている場所によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ba176-319">The range in which a macro can be referenced depends on where the macro is defined.</span></span> <span data-ttu-id="ba176-320">クラスでは、親クラスで定義されているマクロを参照できますが、子クラスで定義されているマクロを参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="ba176-320">In a class, macros that are defined in the parent class can be referenced, but macros defined in a child class cannot be referenced.</span></span> <span data-ttu-id="ba176-321">プリコンパイラが子クラスを処理するとき、プリコンパイラは最初に最上位の直系のクラスへの継承チェーンを追跡します。</span><span class="sxs-lookup"><span data-stu-id="ba176-321">When the precompiler handles a child class, the precompiler first traces the inheritance chain to the most ascendant class.</span></span> <span data-ttu-id="ba176-322">プリコンパイラは、上位クラスのクラス宣言部分からのすべてのディレクティブを処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-322">The precompiler processes all the directives from the class declaration part of the ascendant class.</span></span> <span data-ttu-id="ba176-323">内部テーブルにすべてのマクロとその値を格納します。</span><span class="sxs-lookup"><span data-stu-id="ba176-323">It stores all the macros and their values in its internal tables.</span></span> <span data-ttu-id="ba176-324">プリコンパイラは、同じ方法で、継承チェーン内の次のクラスを処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-324">The precompiler handles the next class in the inheritance chain the same way.</span></span> <span data-ttu-id="ba176-325">各クラス宣言でのディレクティブの結果は、継承チェーンの初期段階で見つかったディレクティブからすでに入力されている内部テーブルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-325">The result of the directives in each class declaration are applied to the internal tables that are already populated from directives that were found earlier in the inheritance chain.</span></span> <span data-ttu-id="ba176-326">プリコンパイラは、ターゲットの子クラスに達すると、もう一度クラス宣言部分を処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-326">When the precompiler reaches the target child class, it again handles the class declaration part.</span></span> <span data-ttu-id="ba176-327">ただし、次に一連の個別操作で各メソッドを処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-327">However, it next handles each method in a series of separate operations.</span></span> <span data-ttu-id="ba176-328">プリコンパイラは、内部テーブルの状態を現在のメソッドの処理を開始する前の状態に復元できる方法で、その内部テーブルを更新します。</span><span class="sxs-lookup"><span data-stu-id="ba176-328">The precompiler updates its internal tables in a way that the state of the tables can be restored as they were before processing of the current method began.</span></span> <span data-ttu-id="ba176-329">最初のメソッドが処理された後、内部テーブルは次のメソッドが処理される前に復元されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-329">After the first method is handled, the internal tables are restored before the next method is handled.</span></span>

#### <a name="the-method-is-all-contents-of-the-node"></a><span data-ttu-id="ba176-330">メソッドはノードのすべての内容</span><span class="sxs-lookup"><span data-stu-id="ba176-330">The Method is All Contents of the Node</span></span>

<span data-ttu-id="ba176-331">このコンテキストでは、メソッドがアプリケーション オブジェクト ツリー (AOT) でのメソッド ノードのコンテンツとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-331">In this context, a method is defined as the contents of a method node in the Application Object Tree (AOT).</span></span> <span data-ttu-id="ba176-332">AOT で、クラス ノードを展開し、クラス ノードを展開して、メソッドのノードを右クリックしてから編集を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba176-332">In the AOT, you can expand the Classes node, expand a class node, right-click a method node, and then select Edit.</span></span> <span data-ttu-id="ba176-333">その後、メソッド宣言の前に \#define.MyMacro("abc") の行を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-333">Then you can add a line for \#define.MyMacro("abc") before the method declaration.</span></span> <span data-ttu-id="ba176-334">プリコンパイラは、\#define ディレクティブがメソッドの {} ブロックの外である場合でも、その \#define ディレクティブをメソッドの一部として処理します。</span><span class="sxs-lookup"><span data-stu-id="ba176-334">The precompiler treats this \#define directive as part of the method, even though the \#define occurs outside the {} block of the method.</span></span>

### <a name="class-inheritance-and-macro-reference-range"></a><span data-ttu-id="ba176-335">クラス継承とマクロ参照範囲</span><span class="sxs-lookup"><span data-stu-id="ba176-335">Class Inheritance and Macro Reference Range</span></span>

<span data-ttu-id="ba176-336">次のコード例は、クラス継承シナリオで参照するマクロの範囲を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-336">The following code example demonstrates the range of macro referencing in class inheritance scenarios.</span></span> <span data-ttu-id="ba176-337">メソッドの出力にある基本明細行は、ClassC\_hという名前の明細行です。</span><span class="sxs-lookup"><span data-stu-id="ba176-337">The primary line to notice in the method's output is the line labeled ClassC\_h.</span></span> <span data-ttu-id="ba176-338">親の親クラスで定義されたマクロを孫クラスのメソッドで参照できることを示します。</span><span class="sxs-lookup"><span data-stu-id="ba176-338">It shows that a macro defined in a grandparent class can be referenced in a method of the grandchild class.</span></span> <span data-ttu-id="ba176-339">出力のもう 1 つの重要な行には ClassA\_k というラベルが付いています。</span><span class="sxs-lookup"><span data-stu-id="ba176-339">Another important line in the output is labeled ClassA\_k.</span></span> <span data-ttu-id="ba176-340">この行は、あるメソッドで定義されたマクロが他のメソッドでは使用できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-340">This line shows that a macro defined in a method is not available in other methods.</span></span> <span data-ttu-id="ba176-341">ClassA は基本クラスであり、クラス宣言にいくつかのマクロを定義します。</span><span class="sxs-lookup"><span data-stu-id="ba176-341">ClassA is the base class and it defines several macros in its class declaration.</span></span> <span data-ttu-id="ba176-342">その子孫クラスは、これらのマクロを参照します。</span><span class="sxs-lookup"><span data-stu-id="ba176-342">Its descendant classes reference these macros.</span></span> <span data-ttu-id="ba176-343">基本クラスは、そのいずれかのメソッドの内部のマクロも定義します。</span><span class="sxs-lookup"><span data-stu-id="ba176-343">The base class also defines a macro inside one of its methods.</span></span> <span data-ttu-id="ba176-344">このクラスの 2 番目のメソッドは、マクロが範囲外に定義されていると判断し、2 番目のメソッドで参照することができません。</span><span class="sxs-lookup"><span data-stu-id="ba176-344">A second method in this class determines the macro is defined out of range and cannot be referenced in the second method.</span></span> <span data-ttu-id="ba176-345">メソッド **UseOtherMethodMacro** の **\#undef.MacroRange333**は、そのメソッドの残りの部分でマクロ **MacroRange333** を使用できるかどうかに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="ba176-345">The **\#undef.MacroRange333** in the method **UseOtherMethodMacro** affects the availability of macro **MacroRange333** in the rest of that method.</span></span> <span data-ttu-id="ba176-346">派生クラスは **MacroRange333** を参照することができます。</span><span class="sxs-lookup"><span data-stu-id="ba176-346">Descendant classes can still reference **MacroRange333**.</span></span> <span data-ttu-id="ba176-347">ClassB は ClassA を拡張し、親クラスで定義されている **MacroRangeA** マクロの定義を解除します。</span><span class="sxs-lookup"><span data-stu-id="ba176-347">ClassB extends ClassA and it undefines the macro **MacroRangeA** that is defined in its parent class.</span></span> <span data-ttu-id="ba176-348">これにより、現在のクラスを拡張するすべてのクラスでマクロを使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="ba176-348">This makes the macro unavailable to any class that extends the present class.</span></span> <span data-ttu-id="ba176-349">また、存在するクラスは、その親クラスで定義される **MacroRangeB** マクロの再定義も行います。</span><span class="sxs-lookup"><span data-stu-id="ba176-349">The present class also redefines the macro **MacroRangeB** that is defined in its parent class.</span></span> <span data-ttu-id="ba176-350">これにより、マクロの値が (正の値から負の値に) 変更されます。</span><span class="sxs-lookup"><span data-stu-id="ba176-350">This changes the value of the macro (from positive to negative).</span></span> <span data-ttu-id="ba176-351">ClassC は ClassB を拡張し、**\#ifnot** を使用して、基本クラス ClassInheritanceOfMacrosCBase1 が定義する **MacroRangeA** マクロにアクセスできないことを実証します。</span><span class="sxs-lookup"><span data-stu-id="ba176-351">ClassC extends ClassB and it uses **\#ifnot** to demonstrate that it cannot access the **MacroRangeA** macro that the base class, ClassInheritanceOfMacrosCBase1, defines.</span></span> <span data-ttu-id="ba176-352">その理由は、中間レベルのクラスがマクロを定義していないためです。</span><span class="sxs-lookup"><span data-stu-id="ba176-352">The reason is that the mid-level class undefined the macro.</span></span> <span data-ttu-id="ba176-353">また、このクラスは、ClassInheritanceOfMacrosCBase1 クラスが定義するマクロ **MacroRange333** にアクセスできることも示しています。</span><span class="sxs-lookup"><span data-stu-id="ba176-353">This class also demonstrates that it can access the macro **MacroRange333** that ClassInheritanceOfMacrosCBase1 class defines.</span></span> <span data-ttu-id="ba176-354">TestClass にはデモ メソッドを呼び出して結果を表示するメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba176-354">TestClass contains a method that calls the demonstration methods and displays the results.</span></span>

    class ClassA
    {
        // Unless disturbed by other directives, these macros can
        // be referenced by method in this class in child classes.
        #define.MacroRangeA
        #define.MacroRangeB(22)
        #define.MacroRange333(333)

        static void UseMacros()
        {
            //  This method shows that a macro that is defined
            // in the class declaration is in range in every
            // method in that class.
            // This method also contains a define for macro
            // MacroDefInMethodD, and tests outside this
            // method determine the macro is not in range.
            ;
            info("ClassA: #MacroRangeB == " + int2str(#MacroRangeB));
            #define.MacroDefInMethodD // Cannot be referenced in other methods.
        }

        static void UseOtherMethodMacro()
        {
            // This method shows that the macro MacroDefInMethodD
            // that was defined in another method in this class
            // cannot be referenced in this method.
            // This method contains an #undef of MacroRange333,
            // yet descendant classes can still reference this macro.
            #ifnot.MacroDefInMethodD
            info("ClassA_k: This means MacroDefInMethodD is in not range here.");
            #endif
            #undef.MacroRange333
        }
    }


    class ClassB extends ClassA
    {
        // This class declaration makes the macro MacroRangeA
        // unavailable to methods in this class and child classes.
        // This class declaration also redefines MacroRangeB for
        // this class and child classes.
        #undef.MacroRangeA // Makes unavailable to child classes.
        #define.MacroRangeB(-22) 
        // Redefining with a different value.
        static void UseMacros()
        {
            // This method shows that the value for #MacroRangeB comes
            // from its redefinition in this class, instead of from
            // the definition in the parent class.

            info("ClassB_c: #MacroRangeB == " + int2str(#MacroRangeB)
                + " (Is now negative due to later redefinition.)");
        }
    }


    class ClassC extends ClassB
    {
        static void UseMacros()
        {
            //   This method shows that the #undef in the parent
            // class overwrites the #define in the grandparent class.
            //   This method also shows that a macro defined in the
            // grandparent class is in range in methods on this class.
            ;
            #ifnot.MacroRangeA
            info("ClassC_f: MacroRangeA is no longer defined, due to #undef in ClassB.");
            #endif
            info("ClassC_h: #MacroRange333 == " + int2str(#MacroRange333)
                + " (Defined in ClassA.)");
        }
    }


    class TestClass
    {
        static void JobClassesCC(Args _args)
        {
            ;
            ClassA ::UseMacros();
            ClassA ::UseOtherMethodMacro();
            ClassB ::UseMacros();
            ClassC ::UseMacros();
            /****************  Actual output
            Message (08:10:59 am)
            ClassA_a: #MacroRangeB == 22
            ClassA_k: This means MacroDefInMethodD is not in range here.
            ClassB_c: #MacroRangeB == -22 (Is now negative due to later redefinition.)
            ClassC_f: MacroRangeA is no longer defined, due to #undef in child class ClassB.
            ClassC_h: #MacroRange333 == 333 (Defined in ClassA.)
            ****************/
        }
    }



