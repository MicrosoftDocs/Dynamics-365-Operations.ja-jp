---
title: "X++ でのマクロ"
description: "このトピックでは、X++ でマクロを作成および使用する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 189441
ms.assetid: a2de1498-2c9d-4c5d-b396-5c8703a5ef72
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 839dabd270c576a32a39875cd98e5f074ecc50be
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="macros-in-x"></a>X++ でのマクロ

[!include [banner](../includes/banner.md)]

このトピックでは、X++ でマクロを作成および使用する方法について説明します。

コードをコンパイルする前に、プリコンパイラ ディレクティブが処理されます。 ディレクティブは、マクロとその値を宣言して処理します。 ディレクティブは、プリコンパイラによって削除され、X++ コンパイラがそれらを検出することはありません。 X++ コンパイラは、ディレクティブによって X++ コードに書き込まれた一連の文字だけを認識します。

## <a name="define-and-if-directives"></a>\#define および \#if ディレクティブ
すべてのプリコンパイラの指令および記号は \# 文字から始まります。 マクロは、コード内の任意の時点で定義できます。 変数は一連の文字である値を持つことができますが、値を持つ必要はありません。 **\#define** ディレクティブは、省略可能な値を含む、マクロ変数を作成するようプリコンパイラに指示します。 **\#if** ディレクティブは、変数が定義されているかどうか、および必要に応じて、特定の値があるかどうかをテストします。 X++ プリコンパイラ ディレクティブ、それが定義するマクロ名、および **\#if** ディレクティブ値テストではすべて、大文字と小文字が区別されます。 ただし、マクロ名を大文字で始めるのがベスト プラクティスです。

### <a name="code-example"></a>コードの例

次のコード サンプルでは、**MyMacro** というマクロが定義されています。 **\#define.MyMacro** 定義の行に値は指定されません。 したがって、値が長さゼロの文字列であるかのように動作します。 **\#if.MyMacro** ステートメントは、**MyMacro** が定義されているかどうかをテストします。 **MyMacro** が定義されているため、最初の **\#endif** より前のコード行はテスト場所の X++ コードに含まれます。 例の最後の方に、**\#ifnot.MyMacro** テストがあります。 **MyMacro** が定義されているため、そのテストは false であり X++ コードには行が書き込まれません。 このメソッドのプリコンパイル フェーズが終了した後、**MyMacro** の定義はスコープ外となり、もはやシステムとして認識されなくなります。

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

## <a name="precompile-and-compile-error-messages"></a>エラー メッセージのプリコンパイルとコンパイル
マクロを含むコードを作成するときは、プリコンパイル中またはコンパイル中にエラー メッセージが生成されたかどうかを理解する必要があります。 探し出す 2 つのキーワードは次のとおりです。

-   語彙: これはプリコンパイル エラーを示します。
-   構文: これはコンパイル エラーを示します。

次のコード例では、ディレクティブの最後を示す最初の閉じかっこによって引き起こされる語彙エラーがあります。 したがって、プリコンパイラは最後の 2 文字 "";)" で混乱します。

    #define.MyMacro1(info("Hello");)

次のコード例では、存在しない **++++** 演算子を使用したために構文エラーが発生しています。 X++ コンパイラは、**\#MyMacro2** がマクロの値に置き換えられた後に、この演算子を検出します。 マクロ定義は、その値が X++ 構文で受け付けられていなくても正しいです。

    #define.MyMacro2(++++iTest;) 
    #MyMacro2

## <a name="undef-directive"></a>\#undef ディレクティブ
**\#undef** ディレクティブを使用すると、以前の **\#define** から存在するマクロ定義を削除することができます。 マクロ名が **\#define** によって作成され、**\#undef** によって削除された後、別の **\#define** によってマクロが再度作成されます。 **\#undef** は、**\#localmacro** ディレクティブで作成されたマクロには影響しません。 次のコード サンプルでは、マクロ **MyMacro** は \#undef ディレクティブを使用して未定義となります。 \#undef は、その存在の 2 つの \#if テスト間で発生します。 出力は、最初の \#if テストのみが真であることを示しています。

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

## <a name="use-a-macro-value"></a>マクロ値の使用
値を持つマクロ名を定義することができます。 マクロの値は、文字の並びです。 マクロの値は、データ型の正式な意味での文字列 (または **str**) ではありません。 \#define ディレクティブの最後にあるかっこで囲まれた値を加えることにより、値をマクロに割り当てます。 X++ コードで発生する値を必要とする箇所ではマクロ記号を使用することができます。 マクロ記号は、接頭語として追加された \# 文字を持つマクロの名前です。 次のコード例では、マクロ記号 **\#MyMacro** を示しています。 シンボルはマクロの値に置き換えられます。

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

## <a name="test-a-macro-value"></a>マクロ値のテスト
値があるかどうかを確認するマクロをテストすることができます。 また、値が特定の文字の並びと等しいか確認するためにテストすることができます。 これらのテストでは、条件付きで X++ プログラムにコード行を含めることができます。 定義されたマクロに値があるかどうかをテストする方法はありません。 特定の値がマクロの値に一致するかどうかのみテストすることができます。 ベスト プラクティスとしては、定義するマクロ名は常に値を持つ必要があります。または、決して値を持つことができません。 これらのモードを交互に使用するときは、コードを理解することが困難になります。 値を持つマクロについては、フィットの検索時によって異なります。 次のコード サンプルでは、2 つの **\#if** テストが実行され、マクロ **MyIntMacro** が存在するかどうか判定します。 **\#if.MyIntMacro()** テストが true です。 この構文の動作は、**\#if.MyIntMacro.** と同じです。

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

次のコード例は、**DebugMacro** マクロの値をテストする **\#if.DebugMacro(heavy)** ディレクティブを示しています。 値が 5 文字シーケンス **heavy** である場合、テストは true になります。

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

## <a name="definc-and-defdec-directives"></a>\#defInc および \#defDec ディレクティブ
**\#defInc** および **\#defDec** は、マクロの値を解釈する唯一のディレクティブであり、正式な **int** タイプに変換できる値を持つマクロにのみ適用されます。 値は、数字のみを含むことができます。 唯一の数字以外の文字は、先頭にマイナス記号 (-) が付いています。 整数値は、**int64** ではなく、X++ **int** として扱われます。 **\#defInc** ディレクティブにより使用されるマクロ名については、マクロを作成する**\#定義** ディレクティブがクラス宣言に配置されないようにすることが重要です。 これらの場合の **\#defInc** の動作は予測できません。 代わりに、このようなマクロはメソッドだけで定義される必要があります。 整数値を持つマクロには **\#defInc** および **\#defDec** ディレクティブのみを使用することをお勧めします。 プリコンパイラは、マクロの値が整数でないとき、あるいは値が異常または極端なとき、**\#defInc** の特別なルールに従います。 次のテーブルは、**\#defInc** がゼロ (0) に変換してから増分する値を示しています。 **\#defInc、** によって値が 0 に変換されると、**\#defDec** によっても元の値を回復できません。

| マクロの値       | 動作                                                                                                                                                                                               |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (+55)             | プラス記号 (+) 接頭語により、プリコンパイラはこれを数字以外の文字列として扱います。 プリコンパイラは、**\#defInc** (または **\#識別子)** ディレクティブを扱うとき、数値以外のすべての文字列を 0 として処理します。 |
| (「3」)             | 引用符で囲まれた整数は、0 として扱われます。 引用符は破棄され、これらの変更はそのまま残ります。                                                                                   |
| ( )               | スペースの文字列が 0 として扱われ、増加します。                                                                                                                                              |
| ()                | 長さゼロの文字列は、0 として処理され、**\#define.MyMac()** のように、値がかっこで囲まれている場合は増加します。                                                                     |
| (ランダムな文字列です。)  | 数値以外の文字列は 0 として扱われ、次に増加します。                                                                                                                            |
| (0x12)            | 16 進数は、数値以外の文字列として扱われます。 したがって、それらは 0 に変換され、次に増分されます。                                                                                       |
| (-44)             | マイナス記号 (-) のない整数を含め、負の数は許容されます。                                                                                                                     |
| (2147483647)      | 最大の正の **int** 値は、\#defInc によって最小の負の **int** 値に変更されます。                                                                                                       |
| (999888777666555) | **int** および **int64** の容量を超えた大きな数。 これは最大の正の **int** 値として扱われます。                                                                                 |
| (5.8)             | 実数は、\#defDec (および \#defInc) により切り捨てられます。 後続の記号置き換えは、切り捨てが永続化することを示します。                                                                              |
|                   | \#define.MyValuelessMacro ディレクティブの値とかっこが指定されていない場合は、プリコンパイラは \#defInc.MyValuelessMacro ディレクティブの使用を拒否します。                                     |

### <a name="code-example"></a>コードの例

次のコード サンプルでは、マクロ **CounterMacroA** の初期値は、整数に変換できる文字列です。 サンプルでは、このマクロ名に **\#defInc** および **\#defDec** の各ディレクティブをどのように使用できるかを示しています。

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

## <a name="globaldefine-directive"></a>\#globaldefine ディレクティブ
<strong>\#Globaldefine</strong> ディレクティブは、<strong>\#define</strong> ディレクティブに似ています。 違いは、<strong>\#define</strong> ディレクティブは一般的に <strong>\#globalmacro</strong> ディレクティブよりも優先されるということです。 これは、どのディレクティブが最初に X++ コードで発生するかに関係なく当てはまります。 <strong>\#globaldefine</strong> は、マクロ名と値の両方を持つ <strong>\#define</strong> ディレクティブを上書きすることはありません。 <strong>\#globaldefine</strong> は別の <strong>\#globaldefine を上書きすることができます。**A **\#define</strong> ディレクティブは、名前と値の両方を持つ \#globalmacro を上書きしません。 <strong>\#define</strong> を使用して <strong>\#globaldefine</strong> を使用しないことをお勧めします。 <strong>\#globaldefine</strong> を使用すると、不確実性が生じてコードの保守が困難になる可能性があります。 <strong>\#globaldefine</strong> の正確なセマンティクスは、<strong>\#if</strong> テストディレクティブでは達成できません。 <strong>\#if</strong> テストを使うことにより <strong>\#define</strong> および <strong>\#globaldefine</strong> の上書きを回避することができます。 ただし、<strong>\#if</strong> テストは <strong>\#define</strong> と <strong>\#globaldefine</strong> マクロを区別できません。 次のコード例は、<strong>\#if</strong> などの他のディレクティブで <strong>\#globaldefine</strong> セマンティクスを達成するために最も近い例です。

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

### <a name="code-example"></a>コードの例

次のコード例は、**\#define** と **\#globaldefine** の動作の違いを示しています。 以下のコード サンプルは、出力からの結びを説明するテーブルです。 コード サンプルの基本テスト ケースの名前は **12** です。

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

## <a name="macro-parameters"></a>マクロ パラメーター
パラメータ シンボルを含めるようにマクロの値を定義することができます。 最初のパラメーター記号は %1で、2 番目のパラメーター記号は %2 などです。 展開のためにマクロ記号名を参照するときは、パラメーターの値を渡します。 マクロ パラメーターの値は、正式な型のない文字シーケンスで、コンマで区切られます。 パラメーター値の一部としてカンマで渡す方法はありません。 渡されるパラメーターの数は、マクロ値が受け取るように設計されているパラメーターの数よりも少なくても、大きくても等しくてもかまいません。 システムは、渡されたパラメーターの数の不一致を許容します。 マクロが期待するよりも少ないパラメーターが指定された場合、省略された各パラメーターは、長さが 0 の文字列として扱われます。 次のコード サンプルでは、**MyMacro** はパラメーターを含む値を持つよう定義されています。 マクロの代入記号は、かっこで囲まれたパラメーターの値で指定されます。

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

## <a name="localmacro-and-globalmacro-directives"></a>\#localmacro および \#globalmacro ディレクティブ
<strong>\#Localmacro</strong> ディレクティブは、複数の行にまたがる値をマクロに設定する場合や、マクロの値にかっこが含まれている場合に推奨されます。 <strong>\#localmacro</strong> ディレクティブは、マクロの値を数行の X++ または SQL コードにする場合に推奨されます。 <strong>\#Localmacro</strong> ディレクティブは、<strong>\#macro.</strong> として記述することができます。 ただし、<strong>\#localmacro</strong> が勧められている用語です。 どちらのマクロも同じ動作をします。 <strong>\#if</strong> ディレクティブを使用することにより、マクロ名が <strong>\#define</strong> ディレクティブで宣言されているかどうかをテストできます。 ただし、マクロ名が <strong>\#localmacro</strong> ディレクティブで宣言されているどうかをテストすることはできません。 <strong>\#define</strong> ディレクティブを使用して宣言されたマクロのみ、<strong>\#undef</strong> ディレクティブの影響を受けます。 <strong>\#define</strong> ディレクティブでは、既にスコープ内にある名前を <strong>\#localmacro</strong> として指定できます。 結果は、<strong>\#localmacro</strong>を破棄して、<strong>\#define</strong> マクロを作成することです。 これは反対のシーケンスにも当てはまります。つまり、<strong>\#localmacro</strong> は <strong>\#define</strong> を再定義できます。 (マクロ名と値の両方を持つ) <strong>\#localmacro</strong> は、同じ名前を持つ前の <strong>\#localmacro</strong> を常に上書きします。 ただし、<strong>\#globalmacro</strong> を使用する場合、オーバーライドが発生するかどうかは必ず分かるわけではありません。 このため、<strong>\#globaldefine で**この同じ問題が発生**する \#globalmacro</strong> を使用しないことをお勧めします。 <strong>\#define</strong> マクロと <strong>\#localmacro</strong> マクロの主な違いは、構文がどのように終了するかです 次のターミネーターがあります。

-   **\#定義** - - によって終了 **)**
-   **\#localmacro** - - によって終了 **\#endmacro**

**\#localmacro** は、複数の行の値を持つマクロに適しています。 複数の行の値は、通常 X++ または SQL コードの行です。 X++ および SQL には多くのパラメーターが含まれ、これらは処理の途中で \#define を終了する場合があります。 **\#定義**と **\#localmacro** の両方を宣言し、単一行または後続の行で終了することができます。 実際、**\#define** は宣言されている同じ行で終了します。 実際、**\#localmacro** は後続の行で終了します。 マクロ名と値の両方を指定すると、**\#globalmacro** 指令は \#define 指令を上書きできません。 また、**\#globaldefine** ディレクティブは **\#localmacro** ディレクティブへの上書きができません。

### <a name="code-examples"></a>コードの例

次のコード例は、**\#localmacro** ディレクティブの使用方法を示しています。 **\#undef** ディレクティブが **\#localmacro** マクロに影響しないことを示します。 また、\#if テストでは **\#localmacro** マクロが定義されているかどうかを決定できないことも示します。

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

次の X++ コード例は、**\#localmacro** が同じマクロ名の **\#globalmacro** を上書きしますが、**\#globalmacro** は **\#localmacro** を上書きしないことを示しています。

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

## <a name="nesting-macro-symbols"></a>入れ子になっているマクロ記号
プリコンパイラ定義ディレクティブは他の外部定義ディレクティブ内に入れ子にすることができます。 主な定義ディレクティブは、**\#define** と \#localmacro です。 **このトピックでコード サンプルを提供する場合は、次のとおりです。

-   推移的置換: A **\#define** マクロは、別のマクロのシンボルをその値として持つことができます。 シンボルの推移的置換は X++ コードで行われます。
-   推移的置換なし: マクロ値の **\#if** ディレクティブ テストは置換を実行しません。
-   マクロ内のマクロ: \#define ディレクティブを **\#localmacro** ディレクティブ内に指定したり、**\#localmacro** を **\#define** 内に指定したりできます。

### <a name="transitive-substitution"></a>推移的置換

次のコード例では、最初の **\#define** 変数の値には、2 つ目の **\#define** 変数の記号 (\#D) が含まれます これは、マクロ **D** を定義する前に拡張シンボル \#D が存在していても機能します。

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

### <a name="no-transitive-substitution"></a>推移的置換なし

次のコード例は、2 つのマクロ変数が同じ値を持っているかどうかを、その値が何であるかを指定せずに判断しようとしています。 出力は、この決定が行えないことを示しています。

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

次のコード例は、\#defInc ディレクティブが記号値の推移的置換につながっていないことを示しています。 \#defInc ディレクティブの詳細については、方法: \#defInc および \#defDec ディレクティブの使用を参照してください。 \#defInc.E2 ディレクティブの後、\#E2 の次の出力値は、**E2** の値が 1 に増加する前に、\#defInc.E2 によってゼロ (0) に変換されることを示します。 変換する前に、**E2** の値は 3 文字 \#E2 でした。 テスト ケースの出力 **36** は、値が 1 に変換されたことを示しています。

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

### <a name="macro-within-a-macro"></a>マクロ内のマクロ

**\#define** ディレクティブは **\#localmacro** 内に指定することができ、また **\#localmacro** ディレクティブを\# define 内に指定することもできます。 これは、次のコード サンプルに示されています。

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

## <a name="macrolib-directive"></a>\#macrolib ディレクティブ
マクロ ノードの下のアプリケーション エクスプローラーには、マクロ ディレクティブのセットが含まれる多くのライブラリ ノードがあります。 多くの場合、**\#定義**および **\#localmacro** の両方がこれらのマクロ ライブラリの内容に表示されます。 **\#macrolib.MyAOTMacroLibrary** を使用すると、マクロ ライブラリのコンテンツをユーザーの X++ コードに含めることができます。 **\#if** および **\#undef** ディレクティブは、**\#macrolib** 名には適用されません。 ただし、それは **\#macrolib** マクロのコンテンツである**\#定義**ディレクティブに適用されます。 ディレクティブ **\#macrolib.MyAOTMacroLibrary** は、**\#MyAOTMacroLibrary** として書き込むこともできます。 **\#macrolib** プレフィックスを使うと後でコードを読むときにあいまいにならないため、推奨されます。

### <a name="create-a-macro-library"></a>マクロ ライブラリの作成

マクロ ライブラリを作成するには、次のようにします。

1.  **ソリューション エクスプローラー**で、プロジェクトを右クリックし、**追加**を選択してから**新しい項目**を選択します。
2.  **新しい項目の追加**ダイアログで、インストール済みを選択してから左ウィンドウの **AX アーティファクト**を選択します。
3.  中央ウィンドウで**マクロ**を選択します。
4.  名前を入力し、**追加**をクリックします。 マクロ ファイルを保存し、マクロ ライブラリを検索するためにアプリケーション エクスプローラーを更新します。

### <a name="code-examples"></a>コードの例

Finance and Operations には**イベント**と呼ばれるマクロ ライブラリがあります。 このマクロ ライブラリには、**\#define.DefaultEventPollFrequency(15)** という指令が含まれています。 次のコード例は、**\#macrolib.Event** ディレクティブがマクロ **\#DefaultEventPollFrequency** を使用可能にすることを示しています。

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

次のコード例は、既にマクロ ライブラリ内のノードの名前である名前に対して **\#define** を記述するとどうなるかを示しています。 この例では、**MacLib23**という名前のノードがあり、その内容は次のように 1 つの**\#定義**です。

    #define.DefinInMacLib23("_This is inside AOT macrolib MacLib23.")

\#macrolib ディレクティブが **MacLib23** に対して発行された後、**\#define** と **\#undef** ディレクティブは、**\#macrolib** マクロに影響しません (出力 \_BB を参照してください)。 ただし、**\#macrolib** マクロのコンテンツでの**\#定義**は、それ以降のコードでの\#定義または **\#undef** により上書きされます (出力 \_DD を参照してください)。

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

## <a name="linenumber-directive"></a>\#linenumber ディレクティブ
開発中およびコードのデバッグ中は、\#linenumber ディレクティブを使用することができます。 これは、コード ファイル内の物理的な行番号に置き換えられます。

### <a name="code-example"></a>コードの例

次の X++ コード例は、**\#linenumber** ディレクティブの動作を示しています。

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

## <a name="range-scope-of-macros"></a>マクロの範囲 (スコープ)
マクロが参照できる範囲は、マクロが定義されている場所によって異なります。 クラスでは、親クラスで定義されているマクロを参照できますが、子クラスで定義されているマクロを参照することはできません。 プリコンパイラが子クラスを処理するとき、プリコンパイラは最初に最上位の直系のクラスへの継承チェーンを追跡します。 プリコンパイラは、上位クラスのクラス宣言部分からのすべてのディレクティブを処理します。 内部テーブルにすべてのマクロとその値を格納します。 プリコンパイラは、同じ方法で、継承チェーン内の次のクラスを処理します。 各クラス宣言でのディレクティブの結果は、継承チェーンの初期段階で見つかったディレクティブからすでに入力されている内部テーブルに適用されます。 プリコンパイラは、ターゲットの子クラスに達すると、もう一度クラス宣言部分を処理します。 ただし、次に一連の個別操作で各メソッドを処理します。 プリコンパイラは、内部テーブルの状態を現在のメソッドの処理を開始する前の状態に復元できる方法で、その内部テーブルを更新します。 最初のメソッドが処理された後、内部テーブルは次のメソッドが処理される前に復元されます。

#### <a name="the-method-is-all-contents-of-the-node"></a>メソッドはノードのすべての内容

このコンテキストでは、メソッドがアプリケーション オブジェクト ツリー (AOT) でのメソッド ノードのコンテンツとして定義されます。 AOT で、クラス ノードを展開し、クラス ノードを展開して、メソッドのノードを右クリックしてから編集を選択します。 その後、メソッド宣言の前に \#define.MyMacro("abc") の行を追加することができます。 プリコンパイラは、\#define ディレクティブがメソッドの {} ブロックの外である場合でも、その \#define ディレクティブをメソッドの一部として処理します。

### <a name="class-inheritance-and-macro-reference-range"></a>クラス継承とマクロ参照範囲

次のコード例は、クラス継承シナリオで参照するマクロの範囲を示しています。 メソッドの出力にある基本明細行は、ClassC\_hという名前の明細行です。 親の親クラスで定義されたマクロを孫クラスのメソッドで参照できることを示します。 出力のもう 1 つの重要な行には ClassA\_k というラベルが付いています。 この行は、あるメソッドで定義されたマクロが他のメソッドでは使用できないことを示しています。 ClassA は基本クラスであり、クラス宣言にいくつかのマクロを定義します。 その子孫クラスは、これらのマクロを参照します。 基本クラスは、そのいずれかのメソッドの内部のマクロも定義します。 このクラスの 2 番目のメソッドは、マクロが範囲外に定義されていると判断し、2 番目のメソッドで参照することができません。 メソッド **UseOtherMethodMacro** の **\#undef.MacroRange333**は、そのメソッドの残りの部分でマクロ **MacroRange333** を使用できるかどうかに影響を与えます。 派生クラスは **MacroRange333** を参照することができます。 ClassB は ClassA を拡張し、親クラスで定義されている **MacroRangeA** マクロの定義を解除します。 これにより、現在のクラスを拡張するすべてのクラスでマクロを使用できなくなります。 また、存在するクラスは、その親クラスで定義される **MacroRangeB** マクロの再定義も行います。 これにより、マクロの値が (正の値から負の値に) 変更されます。 ClassC は ClassB を拡張し、**\#ifnot** を使用して、基本クラス ClassInheritanceOfMacrosCBase1 が定義する **MacroRangeA** マクロにアクセスできないことを実証します。 その理由は、中間レベルのクラスがマクロを定義していないためです。 また、このクラスは、ClassInheritanceOfMacrosCBase1 クラスが定義するマクロ **MacroRange333** にアクセスできることも示しています。 TestClass にはデモ メソッドを呼び出して結果を表示するメソッドが含まれています。

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




