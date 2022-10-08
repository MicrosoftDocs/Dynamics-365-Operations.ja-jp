---
title: X++ 例外処理
description: この記事では、X++ の例外処理について説明します。
author: josaw1
ms.date: 09/28/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ddfdaed31d6f719a3395234e7e8e07ca1153e89
ms.sourcegitcommit: 6b0efcfe2a1731011037d48df5b4a400ea1e1ce8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2022
ms.locfileid: "9597804"
---
# <a name="x-exception-handling"></a>X++ 例外処理

[!include [banner](../includes/banner.md)]

この記事では、X++ の例外処理について説明します。 使用してエラーを処理するには、**throw**、**try**...**catch**、**finally**、および **retry** ステートメントを使用して例外を生成して処理します。

*例外* はプログラム実行の順序から離れて規制ジャンプします。 プログラムの実行が再開する指示は、`try...catch` ブロックとスローされる例外のタイプによって決まります。 例外は、**Exception** 列挙の値、または .NET の `System.Exception` クラスまたは派生クラスのインスタンスによって表されます。 多くの場合スローされる 1 つの例外は、**例外::エラー** 列挙値です。 一般的には、例外がスローされる前に infolog に診断情報を書き込みます。

**Global::error** メソッドは多くの場合、情報ログに診断情報を書き込む最善の方法です。 たとえば、メソッドは無効な入力パラメーター値を受け取る場合があります。 この場合、メソッドは例外をスローして、このエラー状況を処理するためのロジックを含む **catch** コード ブロックにすぐにコントロールを転送します。 例外がスローされる場合、コントロールを受け取る **Catch** ブロックの場所を必ずしも知る必要はありません。

## <a name="throw-statements"></a>throw ステートメント

**Exception** 列挙値をスローするには、**throw** キーワードを使用します。 たとえば、次のステートメントは例外エラーをスローします。

```xpp
throw Exception::error;
```

列挙値をスローするのではなく、**Global::error** メソッドの出力を **スロー** のオペランドとして使用することがベスト プラクティスです。

```xpp
throw Global::error("The parameter value is invalid.");
```

**Global::error** メソッドは、対応するテキストにラベルを自動的に変換します。 この機能は、ローカライズ可能なコードを書くのに役立ちます。 

```xpp
throw Global::error("@SYS98765");
```

**Global** クラスの静的メソッドは、**Global::** プレフィックスなしで呼び出すことができます。 たとえば、**Global::error** メソッドは、次のように呼び出すことができます。

```xpp
error("My message.");
```

プラットフォーム更新 31 以降のバージョンでは、**throw** キーワードを使用して .NET 例外をスローできます。

```xpp
throw new InvalidOperationException("This function is not allowed");
```

また、プラットフォーム更新 31 以降では、**throw** キーワードを catch block の内部で使用することもできます。 そのような場合、**throw** は C\# の **rethrow** ステートメントのように動作します。 元の例外、例外メッセージ、およびコール スタックなどのコンテキストは再スローされ、呼び出しコード内のすべての catch ステートメントで使用可能になります。

```xpp
try
{
    throw Exception::error;
}
catch
{
    // locally handle exception
    // then rethrow for caller
    throw;
}
```

## <a name="try-catch-finally-and-retry-statements"></a>try ステートメント、catch ステートメント、最後に retry ステートメント

例外がスローされると、その例外は、もっとも内側の **try** ブロックの **キャッチ** リストによって最初に処理されます。 スローされている例外の種類を処理する **catch** ブロックが見つかった場合、プログラム コントロールはその **キャッチ** ブロックにジャンプします。 **catch** リストに例外を指定するブロックがない場合は、システムは、次の一番内側の **try** ブロックの **catch** リストに例外を渡します。 **catch** ステートメントは、コードに表示されているのと同じ順序で処理されます。

最初の **catch** ステートメントで **Exception::Error** 列挙値を処理することが一般的です。 1 つの方法は、最後の **catch** ステートメントの例外タイプを未指定のままにすることです。 この場合、前回の **catch** ステートメントは、前のいずれかの **catch** ステートメントで処理されていないすべての例外を処理します。 この戦略は、最も外側の **try** ... **catch** ブロックに適しています。

**try**...**catch** ステートメントにオプションの *finally* 句を含めることができます。 **finally** 節のセマンティクスは、C\# と同じです。 **finally** 句のステートメントは、通常または例外を介してコントロールが **try** ブロックを離れるときに実行されます。

**retry** ステートメントは、**catch** ブロックでのみ書き込むことができます。 **retry** ステートメントは、関連付けられている **try** ブロックの最初のコード行までコントロールをジャンプさせます。 **retry** ステートメントは、例外の原因を **catch** ブロック内のコードにより修正できる場合に使用されます。 **retry** ステートメントは、**try** ブロック内のコードに成功するための別の機会を与えます。 **retry** ステートメントは、プログラム コントロールが **try** ブロックに入ってから情報ログに書き込まれたすべてのメッセージを消去します。

> [!NOTE]
> **再試行** ステートメントにより、無限ループが発生しないことを確認する必要があります。 ベスト プラクティスとして、**試行** ブロックは、ループ中であるかを確認するテストができる変数を含める必要があります。

```xpp
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
```

### <a name="the-system-exception-handler"></a>システム例外ハンドラー

**catch** ステートメントが例外を処理しない場合、システムの例外ハンドラーによって処理されます。 システム例外ハンドラーは、情報ログを作成できません。 したがって、ハンドルされない例外を診断することは難しい可能性があります。 効率的な例外処理を提供するために、これらすべてのガイドラインに従うことをお勧めします。

+ 呼び出しスタックの最も外側のフレームで、すべての明細書を含む **try** ブロックがあります。
+ 最も外側の **catch** リストの最後に非修飾の **catch** ブロックがあります。
+ **例外** 列挙値を直接スローするのは避けてください。
+ **Global** クラスの **Global::error**、**Global::warning**、または **Global::info** のいずれかのメソッドから返された列挙値をスローします。 (暗黙的 **Global::** 接頭語を省略することができます)。
+ 情報ログに表示されていない例外をキャッチするとき、**Global::info** 関数を呼び出してそれを表示します。

**Exception::CLRError**、**Exception::UpdateConflictNotRecovered**、およびシステム カーネルの例外は、情報ログに自動的に表示されていない例外の例です。

### <a name="exceptions-and-clr-interop"></a>例外および CLR 相互運用

共通言語欄タイム (CLR) が管理するアセンブリ内にある、Microsoft .NET Framework クラスおよびメソッドを呼び出すことができます。 .NET Framework **System.Exception** インスタンスをスローすると、コードは **System.Exception** 型の変数を宣言して .NET の例外をキャッチするか、次の例に示すように、その派生クラスの 1 つを特定の .NET 例外タイプをキャッチすることでキャッチできます。

```xpp
System.ArgumentException ex;
try
{
    throw new System.ArgumentException("Invalid argument specified");
}
catch(ex)
{
    error(ex.Message);
}
```

プラットフォーム更新 31 より前のリリースでは、**Exception::CLRError** を参照することによって .NET 例外をキャッチできます。 コードは、**CLRInterop::getLastException** メソッドを呼び出すことによって、**System.Exception** インスタンスへの参照を取得できます。

```xpp
try
{
    // call to .NET code which throws exception
}
catch(Exception::CLRError)
{
    System.Exception ex = CLRInterop::getLastException();
    error(ex.Message);
}
```

### <a name="ensuring-that-exceptions-are-shown"></a>例外が表示されるようにする

**Exception::CLRError** タイプの例外は、**Global::error** などのメソッドの呼び出しでは発行されないため、Infolog には表示されません。 **catch** ブロックでは、コードで **Global::error** を呼び出して特定の例外を報告できます。

## <a name="global-class-methods"></a>グローバル クラス メソッド

このセクションでは、いくつかの **グローバル** クラス メソッドについて詳しく説明します。 これらのクラスのメソッドには、**Global::error**、**Global::info**、**Global::exceptionTextFallThrough** が含まれます。

### <a name="globalerror-method"></a>Global::error メソッド

次のコードは、**error** メソッドの宣言方法を示しています。

```xpp
static Exception error
    (SysInfoLogStr txt,
    URL helpURL = '',
    SysInfoAction _sysInfoAction = null)
```

戻り値の型は、**Exception::Error** 列挙値です。 **error** メソッドは例外をスローしません。 **throw** ステートメントで使用できる列挙値を提供するだけです。 **throw** ステートメントは例外をスローします。 **エラー** メソッドのパラメーターの説明を次に示します。 最初のパラメーターのみ必要です。

- **SysInfoLogStr** txt は、メッセージ テキストの **str** です。 また、**strFmt("@SYS12345", strThingName)** などのラベルの参照にもなります。
- **URL** helpUrl は、アプリケーション エクスプローラーのヘルプ記事の場所への参照です (**"KernDoc:\\\\\\\\Functions\\\\substr"**)。 \_sysInfoAction が提供された場合、このパラメータは無視されます。
- **SysInfoAction** は、**SysInfoAction** クラスを拡張するクラスのインスタンスです。 **description** メソッド、**run** メソッド、**pack** メソッド、および **unpack** メソッドは、子クラスに対して推奨されるメソッドのオーバーライドです。

### <a name="globalinfo-method"></a>Global::info メソッド

**Global::info** メソッドは、情報ログにテキストを表示するために頻繁に使用します。 プログラムでは、**情報 (「メッセージ。」)** としてよく書き込まれます。 **情報** メソッドは **Exception::Info** 列挙値を返しますが、まれに予期しないことが発生するため、**Exception::Info** をスローします。

### <a name="globalexceptiontextfallthrough-method"></a>Global::exceptionTextFallThrough メソッド

場合によっては、**catch** ブロック内で何もしない場合があります。 ただし、空の **catch** ブロックがある場合、X++ コンパイラは警告が生成されます。 この警告を避けるためには、**catch** ブロック内の **Global::exceptionTextFallThrough** メソッドを呼び出します。 このメソッドは何もしませんが、コンパイラを満たし、意図を明示的に述べます。

## <a name="exceptions-inside-transactions"></a>トランザクション内の例外

例外がトランザクションの内部でスローされる場合は、トランザクションが自動的にキャンセル (つまり、**ttsAbort** 操作が発生) されます。 この動作は、手動でスローされる例外とシステムがスローする例外の両方に適用されます。 **ttsBegin**-**ttsCommit** トランザクション ブロック内で例外がスローされるとき、そのトランザクション ブロック内の **catch** ステートメントは例外を処理できます。(ただし、**UpdateConflict** または **DuplicateKeyException** 以外の場合に限ります)。 代わりに、トランザクション ブロックの外部にある最も内側の **catch** ステートメントが、最初にテストされる **catch** ステートメントです。

finally 句は、トランザクション スコープ内でも実行されます。

## <a name="exceptions-and-using-statements"></a>例外および `using` ステートメント

`using` ステートメントのセマンティクスは、例外スコープの影響を受けません。

```xpp
using (var athing = new SomethingDisposable())
{
    // Do work.
}
```

次と全く同じになります:

```xpp
var athing = new SomethingDisposable();
try
{
    // Do work.
}
finally
{
    if (athing != null)
        athing.Dispose();
}
```

## <a name="examples-of-exception-handling"></a>例外処理の例

### <a name="showing-exceptions-in-the-infolog"></a>情報ログに例外を表示

次のコード例は、Infolog の例外を示しています。

```xpp
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
```

### <a name="using-the-error-method-to-write-exception-information-to-the-infolog"></a>エラー メソッドを使用して例外情報を情報ログに記述

次のコード例では、**error** メソッドを使用して例外情報を Infolog に書き出します。

```xpp
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
```

### <a name="handling-a-clrerror"></a>CLRError の処理

次のコード例は、**CLRError** 例外を処理します。

```xpp
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
```

### <a name="using-a-retry-statement"></a>再試行ステートメントの使用

次のコード例では、**retry** ステートメントを使用しています。

```xpp
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
```

### <a name="throwing-an-exception-inside-a-transaction"></a>トランザクション内での例外のスロー

次のコード例は、トランザクション ブロックに例外をスローします。

```xpp
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
```

### <a name="using-globalerror-with-a-sysinfoaction-parameter"></a>SysInfoAction パラメーターでの Global::error の使用

コードが例外をスローすると、情報ログにメッセージを書き込むことができます。 **SysInfoAction** クラスを使用すると、これらの情報ログ メッセージをさらに便利にすることができます。

次の例では、**SysInfoAction** パラメーターは **Global::error** メソッドに渡されます。 **error** メソッドは、情報ログにメッセージを書き込みます。 ユーザーが情報ログ メッセージをダブルクリックすると、**SysInfoAction.run** メソッドが実行されます。

**run** メソッドでは、診断を支援したり、例外が発生した問題を解決したりするコードを書き込めます。 **Global::error** メソッドに渡されるオブジェクトは、**SysInfoAction** を拡張して記述するクラスから構築されます。

次のコード例は 2 つの部分で示されています。

- 最初の部分は、**Global::error** メソッドを呼び出して、返された値をスローするジョブを示しています。 **SysInfoAction\_PrintWindow\_Demo** クラスのインスタンスが **エラー** メソッドに渡されます。
- 2 番目の部分は、**SysInfoAction\_PrintWindow\_Demo** クラスを示します。

#### <a name="part-1-calling-globalerror"></a>パート 1: Global::error を呼び出す

```xpp
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
```

#### <a name="part-2-the-sysinfoaction_printwindow_demo-class"></a>パート 2: SysInfoAction\_PrintWindow\_Demo クラス

```xpp
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
```

## <a name="list-of-exceptions"></a>例外のリスト

次のテーブルは、**例外** 列挙型の値である例外リテラルを示しています。

| リテラルの例外                 | 説明    |
|-----------------------------------|---------------------------------------------------|
| 分割                             | ユーザーは Break または Ctrl+C を押しました。 |
| CLRError                          | CLR 機能の使用中にエラーが発生しました。 |
| CodeAccessSecurity                | **CodeAccessPermission.demand** メソッドを使用中にエラーが発生しました。 |
| DDEerror                          | **DDE** システム クラスを使用中にエラーが発生しました。 |
| デッドロック                          | 複数のトランザクションが相互に待機しているため、データベースのデッドロックが発生しました。 |
| DuplicateKeyException             | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。 |
| DuplicateKeyExceptionNotRecovered | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 このコードは再試行されません。 この例外は、トランザクション内では検出されません。    |
| エラー                             | 致命的なエラーが発生しました。 トランザクションは停止されました。 |
| 情報                              | この例外リテラルは、ユーザーのメッセージを保持します。 **情報** 例外をスローしないでください。 |
| 内部                          | 開発システムで内部エラーが発生しました。 |
| 数値                           | **str2int**、**str2int64**、または **str2num** 機能を使用中にエラーが発生しました。 |
| 順番                          | |
| UpdateConflict                    | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 トランザクションは再試行できます (**catch** ブロックで **retry** ステートメントを使用します)。 |
| UpdateConflictNotRecovered        | オプティミスティック同時実行制御を使用しているトランザクションでエラーが発生しました。 このコードは再試行されません。 この例外は、トランザクション内では検出されません。    |
| 警告                           | 例外的なイベントが発生しました。 ユーザーはアクションの実行をする必要がありますが、イベントは致命的ではありません。 **警告** 例外をスローしないでください。 |
| [X++ の SQL 接続エラー例外](sql-connection-error.md)       | クエリ実行時にエラーが発生しました。 トランザクションはキャンセルされます。 この例外は、トランザクション内では検出されません。 |
| タイムアウト       | SQL クエリの実行がタイムアウトしました。トランザクション内では例外をキャッチできません。 catch ブロックで retry ステートメントを使用すると、例外を再試行できます。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
