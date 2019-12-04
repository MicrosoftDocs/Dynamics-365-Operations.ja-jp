---
title: X++ 例外処理
description: このトピックでは、X++の例外処理について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/01/2019
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
ms.openlocfilehash: bd12535768a989c78ae016931078e783398b7bf6
ms.sourcegitcommit: 260a820038c29f712e8f1483cca9315b6dd3df55
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778689"
---
# <a name="x-exception-handling"></a><span data-ttu-id="a9c17-103">X++ 例外処理</span><span class="sxs-lookup"><span data-stu-id="a9c17-103">X++ exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9c17-104">このトピックでは、X++の例外処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-104">This topic describes exception handling in X++.</span></span> <span data-ttu-id="a9c17-105">使用してエラーを処理するには、**throw**、**try**...**catch**、**finally**、および **retry** ステートメントを使用して例外を生成して処理します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-105">You handle errors by using the **throw**, **try**...**catch**, **finally**, and **retry** statements to generate and handle exceptions.</span></span> 

<span data-ttu-id="a9c17-106">*例外*はプログラム実行の順序から離れて規制ジャンプします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-106">An *exception* is a regulated jump away from the sequence of program execution.</span></span> <span data-ttu-id="a9c17-107">プログラムの実行が再開する指示は、**try**...**catch** ブロックとスローされる例外のタイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-107">The instruction where program execution resumes is determined by **try**...**catch** blocks and the type of exception that is thrown.</span></span> <span data-ttu-id="a9c17-108">例外は**例外**列挙の値で表されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-108">An exception is represented by a value of the **Exception** enumeration.</span></span> <span data-ttu-id="a9c17-109">多くの場合スローされる 1 つの例外は、**例外::エラー**列挙値です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-109">One exception that is often thrown is the **Exception::error** enum value.</span></span> <span data-ttu-id="a9c17-110">一般的には、例外がスローされる前に infolog に診断情報を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-110">A common practice is to write diagnostic information to the Infolog before the exception is thrown.</span></span> 

<span data-ttu-id="a9c17-111">**Global::error** メソッドは多くの場合、情報ログに診断情報を書き込む最善の方法です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-111">The **Global::error** method is often the best way to write diagnostic information to the Infolog.</span></span> <span data-ttu-id="a9c17-112">たとえば、メソッドは無効な入力パラメーター値を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-112">For example, your method might receive an input parameter value that isn't valid.</span></span> <span data-ttu-id="a9c17-113">この場合、メソッドは例外をスローして、このエラー状況を処理するためのロジックを含む **catch** コード ブロックにすぐにコントロールを転送します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-113">In this case, the method can throw an exception to immediately transfer control to a **catch** code block that contains logic for handling this error situation.</span></span> <span data-ttu-id="a9c17-114">例外がスローされる場合、コントロールを受け取る **Catch** ブロックの場所を必ずしも知る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-114">You don't necessarily have to know the location of the **catch** block that will receive control when the exception is thrown.</span></span>

## <a name="throw-statements"></a><span data-ttu-id="a9c17-115">throw ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9c17-115">throw statements</span></span>

<span data-ttu-id="a9c17-116">**Exception** 列挙値をスローするには、**throw** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-116">You use the **throw** keyword to throw an **Exception** enum value.</span></span> <span data-ttu-id="a9c17-117">たとえば、次のステートメントは例外エラーをスローします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-117">For example, the following statement throws an error exception.</span></span>

    throw Exception::error;

<span data-ttu-id="a9c17-118">列挙値をスローするのではなく、**Global::error** メソッドの出力を**スロー**のオペランドとして使用することがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-118">Instead of throwing an enum value, a best practice is to use the output of the **Global::error** method as the operand for **throw**.</span></span>

    throw Global::error("The parameter value is invalid.");

<span data-ttu-id="a9c17-119">**Global::error** メソッドは、対応するテキストにラベルを自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-119">The **Global::error** method can automatically convert a label into the corresponding text.</span></span> <span data-ttu-id="a9c17-120">この機能は、ローカライズ可能なコードを書くのに役立ちます。 </span><span class="sxs-lookup"><span data-stu-id="a9c17-120">This functionality helps you write code that can be localized more easily.</span></span>

    throw Global::error("@SYS98765");

<span data-ttu-id="a9c17-121">**Global** クラスの静的メソッドは、**Global::** プレフィックスなしで呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-121">The static methods on the **Global** class can be called without the **Global::** prefix.</span></span> <span data-ttu-id="a9c17-122">たとえば、**Global::error** メソッドは、次のように呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-122">For example, the **Global::error** method can be called like this.</span></span>

    error("My message.");

## <a name="try-catch-finally-and-retry-statements"></a><span data-ttu-id="a9c17-123">try ステートメント、catch ステートメント、最後に retry ステートメント</span><span class="sxs-lookup"><span data-stu-id="a9c17-123">try, catch, finally, and retry statements</span></span>

<span data-ttu-id="a9c17-124">例外がスローされると、その例外は、もっとも内側の <strong>try</strong> ブロックの <strong>キャッチ</strong> リストによって最初に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-124">When an exception is thrown, it's first processed through the <strong>catch</strong> list of the innermost <strong>try</strong> block.</span></span> <span data-ttu-id="a9c17-125">スローされている例外の種類を処理する <strong>catch</strong> ブロックが見つかった場合、プログラム コントロールはその <strong>キャッチ</strong> ブロックにジャンプします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-125">If a <strong>catch</strong> block is found that handles the kind of exception that is being thrown, program control jumps to that <strong>catch</strong> block.</span></span> <span data-ttu-id="a9c17-126"><strong>catch</strong> リストに例外を指定するブロックがない場合は、システムは、次の一番内側の <strong>try</strong> ブロックの<strong>catch</strong> リストに例外を渡します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-126">If the <strong>catch</strong> list has no block that specifies the exception, the system passes the exception to the <strong>catch</strong> list of the next-innermost <strong>try</strong> block.</span></span> <span data-ttu-id="a9c17-127"><strong>catch</strong> ステートメントは、コードに表示されているのと同じ順序で処理されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-127">The <strong>catch</strong> statements are processed in the same sequence as they appear in the code.</span></span> 

<span data-ttu-id="a9c17-128">最初の <strong>catch</strong> ステートメントで <strong>Exception::Error</strong> 列挙値を処理することが一般的です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-128">It's a common practice to have the first <strong>catch</strong> statement handle the <strong>Exception::Error</strong> enum value.</span></span> <span data-ttu-id="a9c17-129">1 つの方法は、最後の <strong>catch</strong> ステートメントの例外タイプを未指定のままにすることです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-129">One strategy is to have the last <strong>catch</strong> statement leave the exception type unspecified.</span></span> <span data-ttu-id="a9c17-130">この場合、前回の <strong>catch</strong> ステートメントは、前のいずれかの <strong>catch</strong> ステートメントで処理されていないすべての例外を処理します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-130">In this case, the last <strong>catch</strong> statement handles all exceptions that aren't handled by any earlier <strong>catch</strong> statement.</span></span> <span data-ttu-id="a9c17-131">この戦略は、最も外側の <strong>try</strong> ... <strong>catch</strong>ブロックに適しています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-131">This strategy is appropriate for the outermost <strong>try</strong>...<strong>catch</strong> blocks.</span></span> 

<span data-ttu-id="a9c17-132"><strong>try</strong>...<strong>catch</strong> ステートメントにオプションの *<strong><em>finally</em></strong>* 句を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-132">An optional *<strong><em>finally</em></strong>* clause can be included in <strong>try</strong>...<strong>catch</strong> statements.</span></span> <span data-ttu-id="a9c17-133"><strong>finally</strong> 節のセマンティクスは、C\# と同じです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-133">The semantics of a <strong>finally</strong> clause are the same as they are in C\#.</span></span> <span data-ttu-id="a9c17-134"><strong>finally</strong> 句のステートメントは、通常または例外を介してコントロールが <strong>try</strong> ブロックを離れるときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-134">The statements in the <strong>finally</strong> clause are executed when control leaves the <strong>try</strong> block, either normally or through an exception.</span></span> 

<span data-ttu-id="a9c17-135"><strong>retry</strong> ステートメントは、<strong>catch</strong> ブロックでのみ書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-135">The <strong>retry</strong> statement can be written only in a <strong>catch</strong> block.</span></span> <span data-ttu-id="a9c17-136"><strong>retry</strong> ステートメントは、関連付けられている <strong>try</strong> ブロックの最初のコード行までコントロールをジャンプさせます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-136">The <strong>retry</strong> statement causes control to jump up to the first line of code in the associated <strong>try</strong> block.</span></span> <span data-ttu-id="a9c17-137"><strong>retry</strong> ステートメントは、例外の原因を <strong>catch</strong> ブロック内のコードにより修正できる場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-137">The <strong>retry</strong> statement is used when the cause of the exception can be fixed by the code in the <strong>catch</strong> block.</span></span> <span data-ttu-id="a9c17-138"><strong>retry</strong> ステートメントは、<strong>try</strong> ブロック内のコードに成功するための別の機会を与えます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-138">The <strong>retry</strong> statement gives the code in the <strong>try</strong> block another opportunity to succeed.</span></span> <span data-ttu-id="a9c17-139"><strong>retry</strong> ステートメントは、プログラム コントロールが <strong>try</strong> ブロックに入ってから情報ログに書き込まれたすべてのメッセージを消去します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-139">The <strong>retry</strong> statement erases all messages that have been written to the Infolog since program control entered the <strong>try</strong> block.</span></span> 

> [!NOTE] 
> <span data-ttu-id="a9c17-140">**再試行**ステートメントにより、無限ループが発生しないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-140">You must make sure that your **retry** statements don't cause an infinite loop.</span></span> <span data-ttu-id="a9c17-141">ベスト プラクティスとして、**試行**ブロックは、ループ中であるかを確認するテストができる変数を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-141">As a best practice, the **try** block should include a variable that you can test to find out whether you're in a loop.</span></span>

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

### <a name="the-system-exception-handler"></a><span data-ttu-id="a9c17-142">システム例外ハンドラー</span><span class="sxs-lookup"><span data-stu-id="a9c17-142">The system exception handler</span></span>

<span data-ttu-id="a9c17-143">**catch** ステートメントが例外を処理しない場合、システムの例外ハンドラーによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-143">If no **catch** statement handles the exception, it's handled by the system exception handler.</span></span> <span data-ttu-id="a9c17-144">システム例外ハンドラーは、情報ログを作成できません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-144">The system exception handler doesn't write to the Infolog.</span></span> <span data-ttu-id="a9c17-145">したがって、ハンドルされない例外を診断することは難しい可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-145">Therefore, an unhandled exception can be hard to diagnose.</span></span> <span data-ttu-id="a9c17-146">効率的な例外処理を提供するために、これらすべてのガイドラインに従うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-146">We recommended that you follow all these guidelines to provide effective exception handling:</span></span>

-   <span data-ttu-id="a9c17-147">呼び出しスタックの最も外側のフレームで、すべての明細書を含む **try** ブロックがあります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-147">Have a **try** block that contains all your statements in the outermost frame on the call stack.</span></span>
-   <span data-ttu-id="a9c17-148">最も外側の **catch** リストの最後に非修飾の **catch** ブロックがあります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-148">Have an unqualified **catch** block at the end of your outermost **catch** list.</span></span>
-   <span data-ttu-id="a9c17-149">**例外**列挙値を直接スローするのは避けてください。</span><span class="sxs-lookup"><span data-stu-id="a9c17-149">Avoid throwing an **Exception** enum value directly.</span></span>
-   <span data-ttu-id="a9c17-150">**Global** クラスの **Global::error**、**Global::warning**、または **Global::info** のいずれかのメソッドから返された列挙値をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-150">Throw the enum value that is returned from one of the following methods on the **Global** class: **Global::error**, **Global::warning**, or **Global::info**.</span></span> <span data-ttu-id="a9c17-151">(暗黙的 **Global::** 接頭語を省略することができます)。</span><span class="sxs-lookup"><span data-stu-id="a9c17-151">(You can omit the implicit **Global::** prefix).</span></span>
-   <span data-ttu-id="a9c17-152">情報ログに表示されていない例外をキャッチするとき、**Global::info** 関数を呼び出してそれを表示します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-152">When you catch an exception that hasn't been shown in the Infolog, call the **Global::info** function to show it.</span></span>

<span data-ttu-id="a9c17-153">**Exception::CLRError**、**Exception::UpdateConflictNotRecovered**、およびシステム カーネルの例外は、情報ログに自動的に表示されていない例外の例です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-153">**Exception::CLRError**, **Exception::UpdateConflictNotRecovered**, and system kernel exceptions are examples of exceptions that aren't automatically shown in the Infolog.</span></span>

### <a name="exceptions-and-clr-interop"></a><span data-ttu-id="a9c17-154">例外および CLR 相互運用</span><span class="sxs-lookup"><span data-stu-id="a9c17-154">Exceptions and CLR interop</span></span>

<span data-ttu-id="a9c17-155">共通言語欄タイム (CLR) が管理するアセンブリ内にある、Microsoft .NET Framework クラスおよびメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-155">You can call Microsoft .NET Framework classes and methods that reside in assemblies that are managed by the common language runtime (CLR).</span></span> <span data-ttu-id="a9c17-156">.NET Framework の **System.Exception** インスタンスがスローされたとき、**Exception::CLRError** を参照することによってコードでそのインスタンスをキャッチできます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-156">When a .NET Framework **System.Exception** instance is thrown, your code can catch it by referencing **Exception::CLRError**.</span></span> <span data-ttu-id="a9c17-157">コードは、**CLRInterop::getLastException** メソッドを呼び出すことによって、**System.Exception** インスタンスへの参照を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-157">Your code can obtain a reference to the **System.Exception** instance by calling the **CLRInterop::getLastException** method.</span></span>

### <a name="ensuring-that-exceptions-are-shown"></a><span data-ttu-id="a9c17-158">例外が表示されるようにする</span><span class="sxs-lookup"><span data-stu-id="a9c17-158">Ensuring that exceptions are shown</span></span>

<span data-ttu-id="a9c17-159">**Exception::CLRError** タイプの例外は、**Global::error** などのメソッドの呼び出しでは発行されないため、Infolog には表示されません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-159">Exceptions of the **Exception::CLRError** type aren't shown in the Infolog, because these exceptions aren't issued by a call to a method such as **Global::error**.</span></span> <span data-ttu-id="a9c17-160">**catch** ブロックでは、コードで **Global::error** を呼び出して特定の例外を報告できます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-160">In your **catch** block, your code can call **Global::error** to report the specific exception.</span></span>

## <a name="global-class-methods"></a><span data-ttu-id="a9c17-161">グローバル クラス メソッド</span><span class="sxs-lookup"><span data-stu-id="a9c17-161">Global class methods</span></span>

<span data-ttu-id="a9c17-162">このセクションでは、いくつかの**グローバル**クラス メソッドについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-162">This section describes some **Global** class methods in more detail.</span></span> <span data-ttu-id="a9c17-163">これらのクラスのメソッドには、**Global::error**、**Global::info**、**Global::exceptionTextFallThrough** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-163">These class methods include **Global::error**, **Global::info**, and **Global::exceptionTextFallThrough**.</span></span>

### <a name="globalerror-method"></a><span data-ttu-id="a9c17-164">Global::error メソッド</span><span class="sxs-lookup"><span data-stu-id="a9c17-164">Global::error method</span></span>

<span data-ttu-id="a9c17-165">次のコードは、**error** メソッドの宣言方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-165">The following code shows how the **error** method is declared.</span></span>

    static Exception error
        (SysInfoLogStr txt,
        URL helpURL = '',
        SysInfoAction _sysInfoAction = null)

<span data-ttu-id="a9c17-166">戻り値の型は、**Exception::Error** 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-166">The return type is the **Exception::Error** enum value.</span></span> <span data-ttu-id="a9c17-167">**error** メソッドは例外をスローしません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-167">The **error** method doesn't throw an exception.</span></span> <span data-ttu-id="a9c17-168">**throw** ステートメントで使用できる列挙値を提供するだけです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-168">It just provides an enum value that can be used in a **throw** statement.</span></span> <span data-ttu-id="a9c17-169">**throw** ステートメントは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-169">The **throw** statement throws the exception.</span></span> <span data-ttu-id="a9c17-170">**エラー**メソッドのパラメーターの説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-170">Here are descriptions of the parameters for the **error** method.</span></span> <span data-ttu-id="a9c17-171">最初のパラメーターのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-171">Only the first parameter is required.</span></span>

- <span data-ttu-id="a9c17-172"><strong>SysInfoLogStr</strong> txt は、メッセージ テキストの <strong>str</strong> です。</span><span class="sxs-lookup"><span data-stu-id="a9c17-172"><strong>SysInfoLogStr</strong> txt is a <strong>str</strong> of the message text.</span></span> <span data-ttu-id="a9c17-173">また、<strong>strFmt("@SYS12345", strThingName)</strong> などのラベルの参照にもなります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-173">It can also be a label reference, such as <strong>strFmt("@SYS12345", strThingName)</strong>.</span></span>
- <span data-ttu-id="a9c17-174">**URL** helpUrl は、アプリケーション エクスプローラーのヘルプ トピックの場所への参照です (**"KernDoc:\\\\\\\\Functions\\\\substr"**)。</span><span class="sxs-lookup"><span data-stu-id="a9c17-174">The **URL** helpUrl is a reference to the location of a Help topic in Application Explorer, such as **"KernDoc:\\\\\\\\Functions\\\\substr"**.</span></span> <span data-ttu-id="a9c17-175">\_sysInfoAction が提供された場合、このパラメータは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-175">The parameter value is ignored if \_sysInfoAction is supplied.</span></span>
- <span data-ttu-id="a9c17-176">**SysInfoAction** は、**SysInfoAction** クラスを拡張するクラスのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-176">The **SysInfoAction** is an instance of a class that extends the **SysInfoAction** class.</span></span> <span data-ttu-id="a9c17-177">**description** メソッド、**run** メソッド、**pack** メソッド、および **unpack** メソッドは、子クラスに対して推奨されるメソッドのオーバーライドです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-177">The method overrides that we recommend for the child class are the **description** method, the **run** method, the **pack** method, and the **unpack** method.</span></span>

### <a name="globalinfo-method"></a><span data-ttu-id="a9c17-178">Global::info メソッド</span><span class="sxs-lookup"><span data-stu-id="a9c17-178">Global::info method</span></span>

<span data-ttu-id="a9c17-179">**Global::info** メソッドは、情報ログにテキストを表示するために頻繁に使用します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-179">The **Global::info** method is often used to show text in the Infolog.</span></span> <span data-ttu-id="a9c17-180">プログラムでは、**情報 (「メッセージ。」)** としてよく書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-180">In programs, it's often written as **info("My message.");**.</span></span> <span data-ttu-id="a9c17-181">**情報**メソッドは **Exception::Info** 列挙値を返しますが、まれに予期しないことが発生するため、**Exception::Info** をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-181">Although the **info** method returns an **Exception::Info** enum value, you will rarely want to throw **Exception::Info**, because nothing unexpected has occurred.</span></span>

### <a name="globalexceptiontextfallthrough-method"></a><span data-ttu-id="a9c17-182">Global::exceptionTextFallThrough メソッド</span><span class="sxs-lookup"><span data-stu-id="a9c17-182">Global::exceptionTextFallThrough method</span></span>

<span data-ttu-id="a9c17-183">場合によっては、**catch** ブロック内で何もしない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9c17-183">Occasionally, you want to do nothing inside your **catch** block.</span></span> <span data-ttu-id="a9c17-184">ただし、空の **catch** ブロックがある場合、X++ コンパイラは警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-184">However, the X++ compiler generates a warning if you have an empty **catch** block.</span></span> <span data-ttu-id="a9c17-185">この警告を避けるためには、**catch** ブロック内の **Global::exceptionTextFallThrough** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-185">To avoid this warning, call the **Global::exceptionTextFallThrough** method in the **catch** block.</span></span> <span data-ttu-id="a9c17-186">このメソッドは何もしませんが、コンパイラを満たし、意図を明示的に述べます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-186">The method does nothing, but it satisfies the compiler and explicitly states the intention.</span></span>

## <a name="exceptions-inside-transactions"></a><span data-ttu-id="a9c17-187">トランザクション内の例外</span><span class="sxs-lookup"><span data-stu-id="a9c17-187">Exceptions inside transactions</span></span>

<span data-ttu-id="a9c17-188">例外がトランザクションの内部でスローされる場合は、トランザクションが自動的にキャンセル (つまり、**ttsAbort** 操作が発生) されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-188">If an exception is thrown inside a transaction, the transaction is automatically canceled (that is, a **ttsAbort** operation occurs).</span></span> <span data-ttu-id="a9c17-189">この動作は、手動でスローされる例外とシステムがスローする例外の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-189">This behavior applies for both exceptions that are thrown manually and exceptions that the system throws.</span></span> <span data-ttu-id="a9c17-190">**ttsBegin**-**ttsCommit** トランザクション ブロック内で例外がスローされるとき、そのトランザクション ブロック内の **catch** ステートメントは例外を処理できます。(ただし、**UpdateConflict** または **DuplicateKeyException** 以外の場合に限ります)。</span><span class="sxs-lookup"><span data-stu-id="a9c17-190">When an exception is thrown inside a **ttsBegin**-**ttsCommit** transaction block, no **catch** statement inside that transaction block can process the exception, (unless it is a **UpdateConflict** or a **DuplicateKeyException**).</span></span> <span data-ttu-id="a9c17-191">代わりに、トランザクション ブロックの外部にある最も内側の **catch** ステートメントが、最初にテストされる **catch** ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="a9c17-191">Instead, the innermost **catch** statements that are outside the transaction block are the first **catch** statements that are tested.</span></span>

## <a name="examples-of-exception-handling"></a><span data-ttu-id="a9c17-192">例外処理の例</span><span class="sxs-lookup"><span data-stu-id="a9c17-192">Examples of exception handling</span></span>

### <a name="showing-exceptions-in-the-infolog"></a><span data-ttu-id="a9c17-193">情報ログに例外を表示</span><span class="sxs-lookup"><span data-stu-id="a9c17-193">Showing exceptions in the Infolog</span></span>

<span data-ttu-id="a9c17-194">次のコード例は、Infolog の例外を示しています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-194">The following code example shows exceptions in the Infolog.</span></span>

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

### <a name="using-the-error-method-to-write-exception-information-to-the-infolog"></a><span data-ttu-id="a9c17-195">エラー メソッドを使用して例外情報を情報ログに記述</span><span class="sxs-lookup"><span data-stu-id="a9c17-195">Using the error method to write exception information to the Infolog</span></span>

<span data-ttu-id="a9c17-196">次のコード例では、**error** メソッドを使用して例外情報を Infolog に書き出します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-196">The following code example uses the **error** method to write exception information to the Infolog.</span></span>

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

### <a name="handling-a-clrerror"></a><span data-ttu-id="a9c17-197">CLRError の処理</span><span class="sxs-lookup"><span data-stu-id="a9c17-197">Handling a CLRError</span></span>

<span data-ttu-id="a9c17-198">次のコード例は、**CLRError** 例外を処理します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-198">The following code example handles a **CLRError** exception.</span></span>

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

### <a name="using-a-retry-statement"></a><span data-ttu-id="a9c17-199">再試行ステートメントの使用</span><span class="sxs-lookup"><span data-stu-id="a9c17-199">Using a retry statement</span></span>

<span data-ttu-id="a9c17-200">次のコード例では、**retry** ステートメントを使用しています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-200">The following code example uses a **retry** statement.</span></span>

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

### <a name="throwing-an-exception-inside-a-transaction"></a><span data-ttu-id="a9c17-201">トランザクション内での例外のスロー</span><span class="sxs-lookup"><span data-stu-id="a9c17-201">Throwing an exception inside a transaction</span></span>

<span data-ttu-id="a9c17-202">次のコード例は、トランザクション ブロックに例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="a9c17-202">The following code example throws an exception in a transaction block.</span></span>

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

### <a name="using-globalerror-with-a-sysinfoaction-parameter"></a><span data-ttu-id="a9c17-203">SysInfoAction パラメーターでの Global::error の使用</span><span class="sxs-lookup"><span data-stu-id="a9c17-203">Using Global::error with a SysInfoAction parameter</span></span>

<span data-ttu-id="a9c17-204">コードが例外をスローすると、情報ログにメッセージを書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-204">When your code throws an exception, it can write messages to the Infolog.</span></span> <span data-ttu-id="a9c17-205">**SysInfoAction** クラスを使用すると、これらの情報ログ メッセージをさらに便利にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-205">You can make those Infolog messages more helpful by using the **SysInfoAction** class.</span></span> 

<span data-ttu-id="a9c17-206">次の例では、**SysInfoAction** パラメーターは **Global::error** メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-206">In the following example, a **SysInfoAction** parameter is passed in to the **Global::error** method.</span></span> <span data-ttu-id="a9c17-207">**error** メソッドは、情報ログにメッセージを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-207">The **error** method writes the message to the Infolog.</span></span> <span data-ttu-id="a9c17-208">ユーザーが情報ログ メッセージをダブルクリックすると、**SysInfoAction.run** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-208">When the user double-clicks the Infolog message, the **SysInfoAction.run** method is run.</span></span> 

<span data-ttu-id="a9c17-209">**run** メソッドでは、診断を支援したり、例外が発生した問題を解決したりするコードを書き込めます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-209">In the **run** method, you can write code that helps diagnose or fix the issue that caused the exception.</span></span> <span data-ttu-id="a9c17-210">**Global::error** メソッドに渡されるオブジェクトは、**SysInfoAction** を拡張して記述するクラスから構築されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-210">The object that is passed in to the **Global::error** method is constructed from a class that you write that extends **SysInfoAction**.</span></span> 

<span data-ttu-id="a9c17-211">次のコード例は 2 つの部分で示されています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-211">The following code sample is shown in two parts.</span></span> 

- <span data-ttu-id="a9c17-212">最初の部分は、**Global::error** メソッドを呼び出して、返された値をスローするジョブを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-212">The first part shows a job that calls the **Global::error** method and then throws the returned value.</span></span> <span data-ttu-id="a9c17-213">**SysInfoAction\_PrintWindow\_Demo** クラスのインスタンスが**エラー** メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-213">An instance of the **SysInfoAction\_PrintWindow\_Demo** class is passed in to the **error** method.</span></span> 
- <span data-ttu-id="a9c17-214">2 番目の部分は、**SysInfoAction\_PrintWindow\_Demo** クラスを示します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-214">The second part shows the **SysInfoAction\_PrintWindow\_Demo** class.</span></span>

#### <a name="part-1-calling-globalerror"></a><span data-ttu-id="a9c17-215">パート 1: Global::error を呼び出す</span><span class="sxs-lookup"><span data-stu-id="a9c17-215">Part 1: Calling Global::error</span></span>

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

#### <a name="part-2-the-sysinfoaction_printwindow_demo-class"></a><span data-ttu-id="a9c17-216">パート 2: SysInfoAction\_PrintWindow\_Demo クラス</span><span class="sxs-lookup"><span data-stu-id="a9c17-216">Part 2: The SysInfoAction\_PrintWindow\_Demo class</span></span>

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

## <a name="list-of-exceptions"></a><span data-ttu-id="a9c17-217">例外のリスト</span><span class="sxs-lookup"><span data-stu-id="a9c17-217">List of exceptions</span></span>

<span data-ttu-id="a9c17-218">次のテーブルは、**例外** 列挙型の値である例外リテラルを示しています。</span><span class="sxs-lookup"><span data-stu-id="a9c17-218">The following table shows the exception literals that are the values of the **Exception** enumeration.</span></span>

| <span data-ttu-id="a9c17-219">リテラルの例外</span><span class="sxs-lookup"><span data-stu-id="a9c17-219">Exception literal</span></span>                 | <span data-ttu-id="a9c17-220">説明</span><span class="sxs-lookup"><span data-stu-id="a9c17-220">Description</span></span>                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c17-221">分割</span><span class="sxs-lookup"><span data-stu-id="a9c17-221">Break</span></span>                             | <span data-ttu-id="a9c17-222">ユーザーは Break または Ctrl+C を押しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-222">The user pressed Break or Ctrl+C.</span></span>                                                                                                                                   |
| <span data-ttu-id="a9c17-223">CLRError</span><span class="sxs-lookup"><span data-stu-id="a9c17-223">CLRError</span></span>                          | <span data-ttu-id="a9c17-224">CLR 機能の使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-224">An error occurred while the CLR functionality was being used.</span></span>                                                                                                       |
| <span data-ttu-id="a9c17-225">CodeAccessSecurity</span><span class="sxs-lookup"><span data-stu-id="a9c17-225">CodeAccessSecurity</span></span>                | <span data-ttu-id="a9c17-226">**CodeAccessPermission.demand** メソッドを使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-226">An error occurred while the **CodeAccessPermission.demand** method was being used.</span></span>                                                                                  |
| <span data-ttu-id="a9c17-227">DDEerror</span><span class="sxs-lookup"><span data-stu-id="a9c17-227">DDEerror</span></span>                          | <span data-ttu-id="a9c17-228">**DDE** システム クラスを使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-228">An error occurred while the **DDE** system class was being used.</span></span>                                                                                                    |
| <span data-ttu-id="a9c17-229">デッドロック</span><span class="sxs-lookup"><span data-stu-id="a9c17-229">Deadlock</span></span>                          | <span data-ttu-id="a9c17-230">複数のトランザクションが相互に待機しているため、データベースのデッドロックが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-230">A database deadlock occurred, because several transactions are waiting for each other.</span></span>                                                                              |
| <span data-ttu-id="a9c17-231">DuplicateKeyException</span><span class="sxs-lookup"><span data-stu-id="a9c17-231">DuplicateKeyException</span></span>             | <span data-ttu-id="a9c17-232">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-232">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9c17-233">トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。</span><span class="sxs-lookup"><span data-stu-id="a9c17-233">The transaction can be retried (use a **retry** statement in the **catch** block).</span></span> |
| <span data-ttu-id="a9c17-234">DuplicateKeyExceptionNotRecovered</span><span class="sxs-lookup"><span data-stu-id="a9c17-234">DuplicateKeyExceptionNotRecovered</span></span> | <span data-ttu-id="a9c17-235">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-235">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9c17-236">このコードは再試行されません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-236">The code won't be retried.</span></span> <span data-ttu-id="a9c17-237">この例外は、トランザクション内では検出されません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-237">This exception can't be caught inside a transaction.</span></span>    |
| <span data-ttu-id="a9c17-238">エラー</span><span class="sxs-lookup"><span data-stu-id="a9c17-238">Error</span></span>                             | <span data-ttu-id="a9c17-239">致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-239">A fatal error occurred.</span></span> <span data-ttu-id="a9c17-240">トランザクションは停止されました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-240">The transaction has been stopped.</span></span>                                                                                                           |
| <span data-ttu-id="a9c17-241">情報</span><span class="sxs-lookup"><span data-stu-id="a9c17-241">Info</span></span>                              | <span data-ttu-id="a9c17-242">この例外リテラルは、ユーザーのメッセージを保持します。</span><span class="sxs-lookup"><span data-stu-id="a9c17-242">This exception literal holds a message for the user.</span></span> <span data-ttu-id="a9c17-243">**情報**例外をスローしないでください。</span><span class="sxs-lookup"><span data-stu-id="a9c17-243">Don't throw an **info** exception.</span></span>                                                                             |
| <span data-ttu-id="a9c17-244">内部</span><span class="sxs-lookup"><span data-stu-id="a9c17-244">Internal</span></span>                          | <span data-ttu-id="a9c17-245">開発システムで内部エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-245">An internal error occurred in the development system.</span></span>                                                                                                               |
| <span data-ttu-id="a9c17-246">数値</span><span class="sxs-lookup"><span data-stu-id="a9c17-246">Numeric</span></span>                           | <span data-ttu-id="a9c17-247">**str2int**、**str2int64**、または **str2num** 機能を使用中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-247">An error occurred while the **str2int**, **str2int64**, or **str2num** function was being used.</span></span>                                                                     |
| <span data-ttu-id="a9c17-248">順番</span><span class="sxs-lookup"><span data-stu-id="a9c17-248">Sequence</span></span>                          |                                                                                                                                                                     |
| <span data-ttu-id="a9c17-249">UpdateConflict</span><span class="sxs-lookup"><span data-stu-id="a9c17-249">UpdateConflict</span></span>                    | <span data-ttu-id="a9c17-250">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-250">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9c17-251">トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。</span><span class="sxs-lookup"><span data-stu-id="a9c17-251">The transaction can be retried (use a **retry** statement in the **catch** block).</span></span> |
| <span data-ttu-id="a9c17-252">UpdateConflictNotRecovered</span><span class="sxs-lookup"><span data-stu-id="a9c17-252">UpdateConflictNotRecovered</span></span>        | <span data-ttu-id="a9c17-253">オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-253">An error occurred in a transaction that is using Optimistic Concurrency Control.</span></span> <span data-ttu-id="a9c17-254">このコードは再試行されません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-254">The code won't be retried.</span></span> <span data-ttu-id="a9c17-255">この例外は、トランザクション内では検出されません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-255">This exception can't be caught within a transaction.</span></span>    |
| <span data-ttu-id="a9c17-256">警告</span><span class="sxs-lookup"><span data-stu-id="a9c17-256">Warning</span></span>                           | <span data-ttu-id="a9c17-257">例外的なイベントが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-257">An exceptional event has occurred.</span></span> <span data-ttu-id="a9c17-258">ユーザーはアクションの実行をする必要がありますが、イベントは致命的ではありません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-258">Although the user might have to take action, the event isn't fatal.</span></span> <span data-ttu-id="a9c17-259">**警告**例外をスローしないでください。</span><span class="sxs-lookup"><span data-stu-id="a9c17-259">Don't throw a **warning** exception.</span></span>                         |
| [<span data-ttu-id="a9c17-260">X++ の SQL 接続エラー例外</span><span class="sxs-lookup"><span data-stu-id="a9c17-260">SQL connection error X++ exception</span></span>](sql-connection-error.md)       | <span data-ttu-id="a9c17-261">クエリ実行時にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a9c17-261">An error occured when during the query execution.</span></span> <span data-ttu-id="a9c17-262">トランザクションはキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="a9c17-262">The transaction will be canceled.</span></span> <span data-ttu-id="a9c17-263">この例外は、トランザクション内では検出されません。</span><span class="sxs-lookup"><span data-stu-id="a9c17-263">This exception can't be caught within a transaction.</span></span> |
