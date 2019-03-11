---
title: X++ ステートメント、ループ、および例外処理
description: このトピックでは、X++ の構文、ループ、および例外処理について説明します。
author: RobinARH
manager: AnnBe
ms.date: 10/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150213
ms.assetid: 16b30ff1-bb31-4f9d-8105-c73abd2455f6
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0eb1645c0f17456aec645420516f7bd25263eba8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369997"
---
# <a name="x-statements-loops-and-exception-handling"></a>X++ ステートメント、ループ、および例外処理

[!include [banner](../includes/banner.md)]

このトピックでは、X++ の構文、ループ、および例外処理について説明します。

<a name="comments"></a>コメント
--------

コードにコメントを追加することをお勧めします。 コメントは、プログラムを読みやすく、またわかりやすくします。 コメントは、プログラムをコンパイルする際には無視されます。 コメントには、**//** スタイルまたは **/** スタイルのいずれかを使用できます。 ただし、ベスト プラクティスは、コメント、および複数行コメントの**//** スタイルを使用するためのものです。

    // This is an example of a comment.
    /* Here is another example of a comment. */

## <a name="conditional-statements-if-ifelse-switch-and-ternary-operator-"></a>条件付きステートメント: if、if...else、switch、および 3 項演算子 (?) です。
条件付きステートメントは、**if**、**if**...**else**、**switch**、および 3 項演算子 (**?**) です。 条件付きステートメントを使用して、コードのブロックを実行するかどうかを指定します。 異なる条件文は、異なる状況において利点を提供する。

### <a name="if-and-ifelse-statements"></a>if および if...else ステートメント

**if** ステートメントは、条件式を評価した後、条件式が **true** として評価された場合にステートメントまたは一連のステートメントを実行します。 **else** 句を使用すると、条件が **false** と評価される場合に実行される代替ステートメントまたは一連のステートメントを提供することができます。 **if**...**else** ステートメントの構文を次に示します。

**(** *式* **)** の場合、*明細書* **\[ 他の** *明細書* **\]**

この構文では、*ステートメント*の回数は両方とも複合ステートメントとすることができます。 かっこで囲まれた*式* (条件式) は、**true** または **false** として評価される有効な式にすることができます。 0 (ゼロ) を除くすべての番号は **true** です。 すべての空でない文字列も **true** です。 **if** ステートメントは入れ子にすることができます。 ただし、**if** ステートメントの入れ子が深すぎる場合、**switch** ステートメントを代わりに使用することを考慮する必要があります。

#### <a name="examples-of-if-and-ifelse-statements"></a>if および if...else ステートメントの例

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

### <a name="switch-statements"></a>switch ステートメント

**switch** ステートメントは、同じ効果を生み出すために **if** ステートメントを入れ子にする必要がある **if** ステートメントとは異なり、マルチブランチ言語コンストラクトです。 **SWITCH** ステートメントの条件式が評価され、それぞれの Case の値に対してチェックされます。 大文字と小文字の値は、コンパイラが評価できる定数でなければなりません。 ケース定数が**切り替え**式と一致する場合、**case** ステートメントを実行します。 そのケースに**休憩**ステートメントが含まれている場合、プログラムはスイッチからジャンプ アウトします。 ケースに**休憩**ステートメントが含まれていない場合、プログラムは継続し、**ケース** ステートメントの次のセットを実行します。 一致が見つからない場合、**既定**ステートメントを実行します。 一致するものがなく、**default** ステートメントがない場合、**switch** ステートメント内のステートメントは実行されません。 **switch** ステートメントの構文を次に示します。

**switch (** *式* **) { { ケース } \[ 既定:** *ステートメント* **\] }**

**case** ステートメントの構文を次に示します。

**case** *式* **{ 、** *式* **} :** *ステートメント*

**switch** ステートメントおよび **case** ステートメントの両方の構文で、*ステートメント*があるごとに、かっこ ({}) でブロックを囲むことでステートメントのブロックを置き換えることができます。

#### <a name="examples-of-switch-statements"></a>切り替え明細書の例

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

### <a name="ternary-operator-"></a>三項演算子 (?)

三項演算子 (**?**) は、2 つの式のうちの 1 つに解決される条件文です。 結果は、変数に割り当てることができます。 対照的に、**if** ステートメントはプログラム フローの条件付き分岐を提供しますが、変数に割り当てることはできません。 三項演算子の構文を次に示します:

*式1* **?** *式2* **:** *式3*

この構文では、*expression1* は **true** または **false** の値を返す必要があります。 *expression1* が **true** である場合、三項全体の明細書は*式*を返します。 それ以外の場合、ステートメントは *expression3* を返します。 *expression2* と *expression3* の両方は同じタイプである必要があります。

#### <a name="examples-of-the-ternary-operator-"></a>三項演算子 (?) の例

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

## <a name="exception-handling-throw-trycatch-finally-and-retry"></a>例外処理: スロー、トライ、キャッチ、最後に再トライ
使用してエラーを処理するには、**throw**、**try**...**catch**、**finally**、および **retry** ステートメントを使用して例外を生成して処理します。 *例外*はプログラム実行の順序から離れて規制ジャンプします。 プログラムの実行が再開する指示は、**try**...**catch** ブロックとスローされる例外のタイプによって決まります。 例外は**例外**列挙の値で表されます。 多くの場合スローされる 1 つの例外は、**例外::エラー**列挙値です。 一般的には、例外がスローされる前に infolog に診断情報を書き込みます。 **Global::error** メソッドは多くの場合、情報ログに診断情報を書き込む最善の方法です。 たとえば、メソッドは無効な入力パラメーター値を受け取る場合があります。 この場合、メソッドは例外をスローして、このエラー状況を処理するためのロジックを含む **catch** コード ブロックにすぐにコントロールを転送します。 例外がスローされる場合、コントロールを受け取る **Catch** ブロックの場所を必ずしも知る必要はありません。

### <a name="throw-statements"></a>throw ステートメント

**Exception** 列挙値をスローするには、**throw** キーワードを使用します。 たとえば、次のステートメントは例外エラーをスローします。

    throw Exception::error;

列挙値をスローするのではなく、**Global::error** メソッドの出力を**スロー**のオペランドとして使用することがベスト プラクティスです。

    throw Global::error("The parameter value is invalid.");

**Global::error** メソッドは、対応するテキストにラベルを自動的に変換します。 この機能は、ローカライズ可能なコードを書くのに役立ちます。 

    throw Global::error("@SYS98765");

**Global** クラスの静的メソッドは、**Global::** プレフィックスなしで呼び出すことができます。 たとえば、**Global::error** メソッドは、次のように呼び出すことができます。

    error("My message.");

### <a name="try-catch-finally-and-retry-statements"></a>try ステートメント、catch ステートメント、最後に retry ステートメント

例外がスローされると、その例外は、もっとも内側の <strong>try</strong> ブロックの <strong>キャッチ</strong> リストによって最初に処理されます。 スローされている例外の種類を処理する <strong>catch</strong> ブロックが見つかった場合、プログラム コントロールはその <strong>キャッチ</strong> ブロックにジャンプします。 <strong>catch</strong> リストに例外を指定するブロックがない場合は、システムは、次の一番内側の <strong>try</strong> ブロックの<strong>catch</strong> リストに例外を渡します。 <strong>catch</strong> ステートメントは、コードに表示されているのと同じ順序で処理されます。 最初の <strong>catch</strong> ステートメントで <strong>Exception::Error</strong> 列挙値を処理することが一般的です。 1 つの方法は、最後の <strong>catch</strong> ステートメントの例外タイプを未指定のままにすることです。 この場合、前回の <strong>catch</strong> ステートメントは、前のいずれかの <strong>catch</strong> ステートメントで処理されていないすべての例外を処理します。 この戦略は、最も外側の <strong>try</strong> ... <strong>catch</strong>ブロックに適しています。 <strong>try</strong>...<strong>catch</strong> ステートメントにオプションの *<strong><em>finally</em></strong>* 句を含めることができます。 <strong>finally</strong> 節のセマンティクスは、C\# と同じです。 <strong>finally</strong> 句のステートメントは、通常または例外を介してコントロールが <strong>try</strong> ブロックを離れるときに実行されます。 <strong>retry</strong> ステートメントは、<strong>catch</strong> ブロックでのみ書き込むことができます。 <strong>retry</strong> ステートメントは、関連付けられている <strong>try</strong> ブロックの最初のコード行までコントロールをジャンプさせます。 <strong>retry</strong> ステートメントは、例外の原因を <strong>catch</strong> ブロック内のコードにより修正できる場合に使用されます。 <strong>retry</strong> ステートメントは、<strong>try</strong> ブロック内のコードに成功するための別の機会を与えます。 <strong>retry</strong> ステートメントは、プログラム コントロールが <strong>try</strong> ブロックに入ってから情報ログに書き込まれたすべてのメッセージを消去します。 <strong>注記:</strong> <strong>再試行</strong>ステートメントにより、無限ループが発生しないことを確認する必要があります。 ベスト プラクティスとして、<strong>試行</strong>ブロックは、ループ中であるかを確認するテストができる変数を含める必要があります。

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

#### <a name="the-system-exception-handler"></a>システム例外ハンドラー

**catch** ステートメントが例外を処理しない場合、システムの例外ハンドラーによって処理されます。 システム例外ハンドラーは、情報ログを作成できません。 したがって、ハンドルされない例外を診断することは難しい可能性があります。 効率的な例外処理を提供するために、これらすべてのガイドラインに従うことをお勧めします。

-   呼び出しスタックの最も外側のフレームで、すべての明細書を含む **try** ブロックがあります。
-   最も外側の **catch** リストの最後に非修飾の **catch** ブロックがあります。
-   **例外**列挙値を直接スローするのは避けてください。
-   **Global** クラスの **Global::error**、**Global::warning**、または **Global::info** のいずれかのメソッドから返された列挙値をスローします。 (暗黙的 **Global::** 接頭語を省略することができます)。
-   情報ログに表示されていない例外をキャッチするとき、**Global::info** 関数を呼び出してそれを表示します。

**Exception::CLRError**、**Exception::UpdateConflictNotRecovered**、およびシステム カーネルの例外は、情報ログに自動的に表示されていない例外の例です。

#### <a name="exceptions-and-clr-interop"></a>例外および CLR 相互運用

共通言語欄タイム (CLR) が管理するアセンブリ内にある、Microsoft .NET Framework クラスおよびメソッドを呼び出すことができます。 .NET Framework の **System.Exception** インスタンスがスローされたとき、**Exception::CLRError** を参照することによってコードでそのインスタンスをキャッチできます。 コードは、**CLRInterop::getLastException** メソッドを呼び出すことによって、**System.Exception** インスタンスへの参照を取得できます。

#### <a name="ensuring-that-exceptions-are-shown"></a>例外が表示されるようにする

**Exception::CLRError** タイプの例外は、**Global::error** などのメソッドの呼び出しでは発行されないため、Infolog には表示されません。 **catch** ブロックでは、コードで **Global::error** を呼び出して特定の例外を報告できます。

### <a name="global-class-methods"></a>グローバル クラス メソッド

このセクションでは、いくつかの**グローバル**クラス メソッドについて詳しく説明します。 これらのクラスのメソッドには、**Global::error**、**Global::info**、**Global::exceptionTextFallThrough** が含まれます。

#### <a name="globalerror-method"></a>Global::error メソッド

次のコードは、**error** メソッドの宣言方法を示しています。

    static Exception error
        (SysInfoLogStr txt,
        URL helpURL = '',
        SysInfoAction _sysInfoAction = null)

戻り値の型は、**Exception::Error** 列挙値です。 **error** メソッドは例外をスローしません。 **throw** ステートメントで使用できる列挙値を提供するだけです。 **throw** ステートメントは例外をスローします。 **エラー**メソッドのパラメーターの説明を次に示します。 最初のパラメーターのみ必要です。

- <strong>SysInfoLogStr</strong> txt は、メッセージ テキストの <strong>str</strong> です。 また、<strong>strFmt("@SYS12345", strThingName)</strong> などのラベルの参照にもなります。
- **URL** helpUrl は、アプリケーション エクスプローラーのヘルプ トピックの場所への参照です (**"KernDoc:\\\\\\\\Functions\\\\substr"**)。 \_sysInfoAction が提供された場合、このパラメータは無視されます。
- **SysInfoAction** \_sysInfoAction は、**SysInfoAction** クラスを拡張するクラスのインスタンスです。 **description** メソッド、**run** メソッド、**pack** メソッド、および **unpack** メソッドは、子クラスに対して推奨されるメソッドのオーバーライドです。

#### <a name="globalinfo-method"></a>Global::info メソッド

**Global::info** メソッドは、情報ログにテキストを表示するために頻繁に使用します。 プログラムでは、**情報 (「メッセージ。」)** としてよく書き込まれます。 **情報**メソッドは **Exception::Info** 列挙値を返しますが、まれに予期しないことが発生するため、**Exception::Info** をスローします。

#### <a name="globalexceptiontextfallthrough-method"></a>Global::exceptionTextFallThrough メソッド

場合によっては、**catch** ブロック内で何もしない場合があります。 ただし、空の **catch** ブロックがある場合、X++ コンパイラは警告が生成されます。 この警告を避けるためには、**catch** ブロック内の **Global::exceptionTextFallThrough** メソッドを呼び出します。 このメソッドは何もしませんが、コンパイラを満たします。

### <a name="exceptions-inside-transactions"></a>トランザクション内の例外

例外がトランザクションの内部でスローされる場合は、トランザクションが自動的にキャンセル (つまり、**ttsAbort** 操作が発生) されます。 この動作は、手動でスローされる例外とシステムがスローする例外の両方に適用されます。 **ttsBegin**-**ttsCommit** トランザクション ブロック内で例外がスローされるとき、そのトランザクション ブロック内の **catch** ステートメントは例外を処理できます。 代わりに、トランザクション ブロックの外部にある最も内側の **catch** ステートメントが、最初にテストされる **catch** ステートメントです。

### <a name="examples-of-exception-handling"></a>例外処理の例

#### <a name="showing-exceptions-in-the-infolog"></a>情報ログに例外を表示

次のコード例は、Infolog の例外を示しています。

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

#### <a name="using-the-error-method-to-write-exception-information-to-the-infolog"></a>エラー メソッドを使用して例外情報を情報ログに記述

次のコード例では、**error** メソッドを使用して例外情報を Infolog に書き出します。

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

#### <a name="handling-a-clrerror"></a>CLRError の処理

次のコード例は、**CLRError** 例外を処理します。

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

#### <a name="using-a-retry-statement"></a>再試行ステートメントの使用

次のコード例では、**retry** ステートメントを使用しています。

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

#### <a name="throwing-an-exception-inside-a-transaction"></a>トランザクション内での例外のスロー

次のコード例は、トランザクション ブロックに例外をスローします。

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

#### <a name="using-globalerror-with-a-sysinfoaction-parameter"></a>SysInfoAction パラメーターでの Global::error の使用

コードが例外をスローすると、情報ログにメッセージを書き込むことができます。 **SysInfoAction** クラスを使用すると、これらの情報ログ メッセージをさらに便利にすることができます。 次の例では、**SysInfoAction** パラメーターは **Global::error** メソッドに渡されます。 **error** メソッドは、情報ログにメッセージを書き込みます。 ユーザーが情報ログ メッセージをダブルクリックすると、**SysInfoAction.run** メソッドが実行されます。 **run** メソッドでは、診断を支援したり、例外が発生した問題を解決したりするコードを書き込めます。 **Global::error** メソッドに渡されるオブジェクトは、**SysInfoAction** を拡張して記述するクラスから構築されます。 次のコード例は 2 つの部分で示されています。 最初の部分は、**Global::error** メソッドを呼び出して、返された値をスローするジョブを示しています。 **SysInfoAction\_PrintWindow\_Demo** クラスのインスタンスが**エラー** メソッドに渡されます。 2 番目の部分は、**SysInfoAction\_PrintWindow\_Demo** クラスを示します。

##### <a name="part-1-calling-globalerror"></a>パート 1: Global::error を呼び出す

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

##### <a name="part-2-the-sysinfoactionprintwindowdemo-class"></a>パート 2: SysInfoAction\_PrintWindow\_Demo クラス

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

### <a name="list-of-exceptions"></a>例外のリスト

次のテーブルは、**例外** 列挙型の値である例外リテラルを示しています。

| リテラルの例外                 | 説明                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 分割                             | ユーザーは Break または Ctrl+C を押しました。                                                                                                                                   |
| CLRError                          | CLR 機能の使用中にエラーが発生しました。                                                                                                       |
| CodeAccessSecurity                | **CodeAccessPermission.demand** メソッドを使用中にエラーが発生しました。                                                                                  |
| DDEerror                          | **DDE** システム クラスを使用中にエラーが発生しました。                                                                                                    |
| デッドロック                          | 複数のトランザクションが相互に待機しているため、データベースのデッドロックが発生しました。                                                                              |
| DuplicateKeyException             | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。 |
| DuplicateKeyExceptionNotRecovered | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 このコードは再試行されません。 この例外は、トランザクション内では検出されません。    |
| エラー                             | 致命的なエラーが発生しました。 トランザクションは停止されました。                                                                                                           |
| 情報                              | この例外リテラルは、ユーザーのメッセージを保持します。 **情報**例外をスローしないでください。                                                                             |
| 内部                          | 開発システムで内部エラーが発生しました。                                                                                                               |
| 数値                           | **str2int**、**str2int64**、または **str2num** 機能を使用中にエラーが発生しました。                                                                     |
| 順番                          |                                                                                                                                                                     |
| UpdateConflict                    | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。 |
| UpdateConflictNotRecovered        | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 このコードは再試行されません。 この例外は、トランザクション内では検出されません。    |
| 警告                           | 例外的なイベントが発生しました。 ユーザーはアクションの実行をする必要がありますが、イベントは致命的ではありません。 **警告**例外をスローしないでください。                         |
| [TransientSqlConnectionError](sql-connection-error.md)       | クエリ実行時にエラーが発生しました。 トランザクションはキャンセルされます。 この例外は、トランザクション内では検出されません。 |

## <a name="loop-statements-for-while-and-dowhile"></a>ループ ステートメント: for、while、do...while
ループ ステートメントは、**for**、**while**、**do**、**while** の 3 つがあります。 ループでは、ループに設定された条件が **false** になるまで、そのステートメントを繰り返します。 loop ステートメント内では、**break** および **continue** ステートメントを使用することができます。

### <a name="for-loops"></a>for ループ

**for** ループは、条件式が **true** である限り、1 つ以上のステートメントを繰り返し実行します。 ステートメントは、条件が満たされた回数だけ実行されます。 **for** ループの本文は、条件テストの結果に応じて 0 回以上実行されることがあります。 **for** ループは、制御変数に初期値を割り当て、また変数の増減ステートメントがあるために、他のループとは異なります。 これらの追加は **for** ループを作成します。これは、リスト、コンテナー、配列をトラバースする場合に特に便利です。 また、明細書を各要素に適用して、要素全体を増分し、最後の要素をテストする条件を設定することができます。 **for** ステートメントの構文を次に示します。

**(** *初期化* **;** *テスト* **;** *増分* **) {** *明細書* **}** 対象

*tatement* 明細書のブロックにすることができます。

#### <a name="example-of-a-for-loop"></a>For loop の例

    // An example where all items are printed in 
    // a fixed array called ra with 100 reals. 
    int ra[100];
    int i; // Control variable.
    for (i=1; i<=100; i+=1)
    {
        print ra[i];
    }

### <a name="while-loops"></a>while loops

**while** ループは、条件式が **true** である限り、1 つ以上のステートメントを繰り返し実行します。 ステートメントは、条件が満たされた回数だけ実行されます (ゼロから多数)。 **while** ループの構文を次に示します。

**(** *式* **)** のとき、*明細書*

この構文では、*ステートメント*はステートメントのブロックで置き換えることができます。

#### <a name="example-of-a-while-loop"></a>While loop の例

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

### <a name="dowhile-loops"></a>do...while ループ

**do**...**while** ループは、**while** ループと似ていますが、条件は実行する必要があるステートメントの後に表示されます。 ステートメントは、ステートメントの実行後にテストされるため、少なくとも 1 回は常に実行されます。 **do**...**while** ループは、レポートのパラメーターの取得など、必ず 1 回以上実行する必要があるタスクに適しています。 **do**...**while** ループの構文を次に示します。

**do {** *ステートメント* **} while (** *式* **) ;**

*tatement* 明細書のブロックにすることができます。

#### <a name="example-of-a-dowhile-loop"></a>Do の例...while loop

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

### <a name="continue-and-break-statements"></a>continue および break ステートメント

**continue** ステートメントは、**for**、**while**、または **do**...**while** ループの次の反復処理に直接移動する実行を発生させます。 **実行**または**途中**で、すぐにテストを実行します。 **対象**ステートメントで、増分手順を実行します。 ループ内の **break** ステートメントは、そのループを終了するために使用されます。 実行後、ループの後の最初のステートメントに移動します。

#### <a name="example-of-a-continue-statement"></a>続行明細書の例

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

## <a name="print-statements"></a>print ステートメント
一時的なウィンドウにメッセージ (テキストまたは選択した結果) を表示するには、**print** ステートメントを使用します。 このウィンドウは、最初の **print** 文が実行されたときに表示されます。 テスト中に、**印刷**明細書は情報ログのテキストを表示する **Global::info** メソッドに代わる便利な手段となります。 次のテーブルは、**print** ステートメントと **Global::info** メソッドを比較しています。

| 機能                                   | print ステートメント                                                                                                                             | 情報メソッド                                                                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| 呼び出し易さ                        | **print** ステートメントは、さまざまなデータ型を自動的に文字列に変換します。 1 つの呼び出しで複数のデータ型を変換できます。       | **info** メソッドでは、入力パラメーターを文字列にする必要があります。               |
| クリップボードにコンテンツをコピーする機能 | **印刷**明細書が開くウィンドウのコンテンツをクリップボードにコピーすることはできません。 ウィンドウのフォーカスを付与することはできません。            | 情報ログの内容は**情報ログ** ウィンドウからクリップボードに容易にコピーされます。 |
| 有効期間の範囲                         | このウィンドウは、X++ アプリケーションが終了すると終了し、アプリケーションを読むのを待たずに閉じることがあります。                                        | このウィンドウは、クライアント セッション全体にわたって存続します。                                |
| サイズと場所                         | ウィンドウは特定のサイズで画面の特定の場所に配置できます。                                                                 | ウィンドウは、システムによってサイズが決められて配置されます。                                    |
| 一般的な使用                             | **print** ステートメントは、テスト時に使用すると便利です。 正式なデバッガーを実行する必要なく、小さな問題をデバッグすることができます。 | **info** メソッドは、生産での使用に適しています。                        |

### <a name="example-of-a-print-statement"></a>印刷明細書の例

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

## <a name="todo-comments"></a>TODO コメント
コンパイラは、コメントの先頭に**仕事**という文字列があると認識します。 **TODO** 文字列は、Microsoft Visual Studio の**タスク一覧**ウィンドウでコメント テキストの残りの部分を報告するようにコンパイラに求めます。 **タスク一覧** ウィンドウを開くには、**表示** を選択し、**タスク ウィンドウ** を選択します。 **タスク ウィンドウ**は、明細行番号を報告します。**TODO** コメントがコード内にあります。 コメントで **TODO** を使用するためのルールを次に示します。

- **TODO** 文字列は、**//** スタイル、または **/** スタイルを使うコメントに表示されます。
- **"TODO"** 文字列は、コメント内の最初の空白文字以外の文字列にする必要があります。 キャリッジ リターン、改行、タブ、およびスペース、すべて空白と見なされます。
- コメントの開始と **"仕事"** の間に空白は必要ありません。
- **TODO** 文字列では大文字と小文字が区別されません。 ただし、規則では **ToDo** またはその他のバリエーションの代わりに、全大文字で **TODO** が入力されます。
- **TODO** 文字列には任意の文字を追加できます。 ただし、規則は、コロンを **TODO** 文字列に追加するかまたは空白で続けるかのいずれかです。
- **TODO** 文字列の後のコメントの残りは、タスク記述として報告されます。 コメントが 200 文字よりも長い場合は、**タスク** タブで切り詰められるとうに表示されることがあります。
- **/** コメント スタイルが使用されている場合、**TODO** タスクの説明は複数行にまたがることができます。

### <a name="examples-of-todo-comments"></a>TODO コメントの例

次の例では、**//** と **/** スタイルを使用する <strong>TODO</strong> コメントを示しています。

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

## <a name="unsupported-statements-changesite-pause-and-window"></a>構文はサポートされていません: changeSite、一時停止、およびウィンドウ
**changeSite**、**pause**、**window** キーワードは、X++ 言語の一部ではなくなりました。 これらのキーワードを使用すると、コンパイル エラーが発生します。

## <a name="using-clauses"></a>句の使用
タイプの完全修飾名を指定する必要がないように、**using** 句を使用します。 **using** 句は、適用されるクラスの前に配置する必要があり、適用先のすべてのソース ファイルに必要です。 すべての **using** 句は通常、ソース ファイルの先頭に配置します。 完全修飾名の短縮名を導入するエイリアスを提供することもできます。 エイリアスは名前空間またはクラスを示すことができます。 次の例では、**using** 句、名前空間エイリアス、およびクラス エイリアスを示しています。

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

## <a name="using-statements"></a>ステートメントの使用
**using** ステートメントは、**IDisposable** を実行するオブジェクトが正しく破棄されることを保証するのに役立ちます。 原則として、**IDisposable** オブジェクトを使用する場合は、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。 **using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。 オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。 **using** ステートメントは構文を簡素化し、オブジェクトを正しく破棄します。 **using** ステートメントの構文を次に示します。

**(** *式* **) を使用して {** *ステートメント* **}**

この構文では、*ステートメント*はステートメントのブロックとすることができ、*式*は **IDisposable** を実装するオブジェクトを宣言してインスタンス化します。 次の例では､**StreamReader** オブジェクトを作成して使用します。

    static void AnotherMethod()
    {
        str textFromFile;
        using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
        {
            textFromFile = sr.ReadToEnd();
        }
    }
