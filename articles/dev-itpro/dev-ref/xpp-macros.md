<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="xpp-macros.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>xpp-macros.64fcca.2f7c4b720be22c25f742e83173be2e674418e228.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2f7c4b720be22c25f742e83173be2e674418e228</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-ref\xpp-macros.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Macros in X++</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ でのマクロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to create and use macros in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ でマクロを作成および使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Macros in X++</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ でのマクロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how to create and use macros in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ でマクロを作成および使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Precompiler directives are processed before the code is compiled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードをコンパイルする前に、プリコンパイラ ディレクティブが処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The directives declare and handle macros and their values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクティブは、マクロとその値を宣言して処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The directives are removed by the precompiler so that the X++ compiler never encounters them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクティブは、プリコンパイラによって削除され、X++ コンパイラがそれらを検出することはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The X++ compiler only sees the sequence of characters written into the X++ code by the directives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイラは、ディレクティブによって X++ コードに書き込まれた一連の文字だけを認識します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><ph id="ph1">\#</ph>define and <ph id="ph2">\#</ph>if directives</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>define および <ph id="ph2">\#</ph>if ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>All precompiler directives and symbols begin with the <ph id="ph1">\#</ph> character.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのプリコンパイラの指令および記号は <ph id="ph1">\#</ph> 文字から始まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>A macro can be defined at any point in the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロは、コード内の任意の時点で定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The variable can have a value that is a sequence of characters, but it is not required to have a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数は一連の文字である値を持つことができますが、値を持つ必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> directive tells the precompiler to create the macro variable, including an optional value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> ディレクティブは、省略可能な値を含む、マクロ変数を作成するようプリコンパイラに指示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> directive tests whether the variable is defined, and optionally, whether it has a specific value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> ディレクティブは、変数が定義されているかどうか、および必要に応じて、特定の値があるかどうかをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The X++ precompiler directives, the macro names that they define, and the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> directive value tests are all case-insensitive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ プリコンパイラ ディレクティブ、それが定義するマクロ名、および <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> ディレクティブ値テストではすべて、大文字と小文字が区別されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>However, it is a best practice to begin macro names with an uppercase letter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、マクロ名を大文字で始めるのがベスト プラクティスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In the following code sample, a macro named <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード サンプルでは、<bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> というマクロが定義されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>It is not given a value in the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define.MyMacro<ept id="p1">**</ept> definition line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>define.MyMacro<ept id="p1">**</ept> 定義の行に値は指定されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Therefore it behaves as if the value is a zero-length sequence of characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、値が長さゼロの文字列であるかのように動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.MyMacro<ept id="p1">**</ept> statement tests whether <bpt id="p2">**</bpt>MyMacro<ept id="p2">**</ept> is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.MyMacro<ept id="p1">**</ept> ステートメントは、<bpt id="p2">**</bpt>MyMacro<ept id="p2">**</ept> が定義されているかどうかをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Because <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> is defined, the lines of code before the first <bpt id="p2">**</bpt><ph id="ph1">\#</ph>endif<ept id="p2">**</ept> are included in the X++ code at the test location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> が定義されているため、最初の <bpt id="p2">**</bpt><ph id="ph1">\#</ph>endif<ept id="p2">**</ept> より前のコード行はテスト場所の X++ コードに含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Near the end of the example there is an <bpt id="p1">**</bpt><ph id="ph1">\#</ph>ifnot.MyMacro<ept id="p1">**</ept> test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例の最後の方に、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>ifnot.MyMacro<ept id="p1">**</ept> テストがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> is defined, that test is false and no lines are written into the X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> が定義されているため、そのテストは false であり X++ コードには行が書き込まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>After the precompile phase ends for this method, the <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> definition goes out of scope and is no longer known to the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドのプリコンパイル フェーズが終了した後、<bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> の定義はスコープ外となり、もはやシステムとして認識されなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Precompile and Compile Error Messages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージのプリコンパイルとコンパイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>When you are developing code that contains macros, you must understand whether an error message is generated during the precompile or the compile phase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロを含むコードを作成するときは、プリコンパイル中またはコンパイル中にエラー メッセージが生成されたかどうかを理解する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The two key words to look for are:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探し出す 2 つのキーワードは次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Lexical – This indicates a precompile error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">語彙: これはプリコンパイル エラーを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Syntax – This indicates a compile error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文: これはコンパイル エラーを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The following code example has a lexical error caused by the first closing parenthesis, which marks the end of the directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、ディレクティブの最後を示す最初の閉じかっこによって引き起こされる語彙エラーがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Therefore the precompiler is confused by the last two characters, "";)".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、プリコンパイラは最後の 2 文字 "";)" で混乱します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The following code example has a syntax error caused by using the non-existent <bpt id="p1">**</bpt><ph id="ph1">++++</ph><ept id="p1">**</ept> operator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、存在しない <bpt id="p1">**</bpt><ph id="ph1">++++</ph><ept id="p1">**</ept> 演算子を使用したために構文エラーが発生しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The X++ compiler encounters this operator after <bpt id="p1">**</bpt><ph id="ph1">\#</ph>MyMacro2<ept id="p1">**</ept> is replaced by the macro value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイラは、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>MyMacro2<ept id="p1">**</ept> がマクロの値に置き換えられた後に、この演算子を検出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The macro definition is correct even though its value is not accepted X++ syntax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ定義は、その値が X++ 構文で受け付けられていなくても正しいです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><ph id="ph1">\#</ph>undef directive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>undef ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>You can use the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef<ept id="p1">**</ept> directive to remove a macro definition that exists from a previous <bpt id="p2">**</bpt><ph id="ph2">\#</ph>define.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef<ept id="p1">**</ept> ディレクティブを使用すると、以前の <bpt id="p2">**</bpt><ph id="ph2">\#</ph>define<ept id="p2">**</ept> から存在するマクロ定義を削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After a macro name has been created by <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> and then removed by <bpt id="p2">**</bpt><ph id="ph2">\#</ph>undef,<ept id="p2">**</ept> the macro can be created again by another <bpt id="p3">**</bpt><ph id="ph3">\#</ph>define.<ept id="p3">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ名が <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> によって作成され、<bpt id="p2">**</bpt><ph id="ph2">\#</ph>undef<ept id="p2">**</ept> によって削除された後、別の <bpt id="p3">**</bpt><ph id="ph3">\#</ph>define<ept id="p3">**</ept> によってマクロが再度作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef<ept id="p1">**</ept> has no effect on macros that are created by the <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef<ept id="p1">**</ept> は、<bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> ディレクティブで作成されたマクロには影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>In the following code sample, the macro <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> is undefined by using the <ph id="ph1">\#</ph>undef directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード サンプルでは、マクロ <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> は <ph id="ph1">\#</ph>undef ディレクティブを使用して未定義となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The <ph id="ph1">\#</ph>undef occurs between the two <ph id="ph2">\#</ph>if tests for its existence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>undef は、その存在の 2 つの <ph id="ph2">\#</ph>if テスト間で発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The output shows only the first <ph id="ph1">\#</ph>if test was true.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力は、最初の <ph id="ph1">\#</ph>if テストのみが真であることを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Use a Macro Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ値の使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You can define a macro name to have a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を持つマクロ名を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>A macro value is a sequence of characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロの値は、文字の並びです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>A macro value is not a string (or <bpt id="p1">**</bpt>str<ept id="p1">**</ept>) in the formal sense of a data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロの値は、データ型の正式な意味での文字列 (または <bpt id="p1">**</bpt>str<ept id="p1">**</ept>) ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You assign a value to a macro by appending the value enclosed in parentheses at the end of a <ph id="ph1">\#</ph>define directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>define ディレクティブの最後にあるかっこで囲まれた値を加えることにより、値をマクロに割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>You can use the macro symbol where you want the value to occur in the X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コードで発生する値を必要とする箇所ではマクロ記号を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>A macro symbol is the name of the macro with the <ph id="ph1">\#</ph> character added as a prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ記号は、接頭語として追加された <ph id="ph1">\#</ph> 文字を持つマクロの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The following code sample shows a macro symbol <bpt id="p1">**</bpt><ph id="ph1">\#</ph>MyMacro.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、マクロ記号 <bpt id="p1">**</bpt><ph id="ph1">\#</ph>MyMacro<ept id="p1">**</ept> を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The symbol is replaced by the value of the macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シンボルはマクロの値に置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Test a Macro Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ値のテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>You can test a macro to see whether it has a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値があるかどうかを確認するマクロをテストすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You can also test to see whether its value is equal to a specific sequence of characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、値が特定の文字の並びと等しいか確認するためにテストすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>These tests enable you to conditionally include lines of code in your X++ program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテストでは、条件付きで X++ プログラムにコード行を含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>There is no way you can test whether a defined macro has a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義されたマクロに値があるかどうかをテストする方法はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>You can only test whether a specific value matches the value of a macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の値がマクロの値に一致するかどうかのみテストすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>As a best practice, any macro name that you define should always have a value, or it should never have a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスとしては、定義するマクロ名は常に値を持つ必要があります。または、決して値を持つことができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>When you alternate between these modes, your code becomes difficult to understand.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのモードを交互に使用するときは、コードを理解することが困難になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For macros that have a value, you can vary the value when you see fit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を持つマクロについては、フィットの検索時によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the following code sample, two <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> tests are run to determine whether the macro <bpt id="p2">**</bpt>MyIntMacro<ept id="p2">**</ept> exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード サンプルでは、2 つの <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> テストが実行され、マクロ <bpt id="p2">**</bpt>MyIntMacro<ept id="p2">**</ept> が存在するかどうか判定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.MyIntMacro()<ept id="p1">**</ept> test is true.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.MyIntMacro()<ept id="p1">**</ept> テストが true です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>This syntax behaves the same as <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.MyIntMacro.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構文の動作は、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.MyIntMacro.<ept id="p1">**</ept> と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The following code sample shows the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.DebugMacro(heavy)<ept id="p1">**</ept> directive that tests the value of the <bpt id="p2">**</bpt>DebugMacro<ept id="p2">**</ept> macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、<bpt id="p2">**</bpt>DebugMacro<ept id="p2">**</ept> マクロの値をテストする <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if.DebugMacro(heavy)<ept id="p1">**</ept>ディレクティブを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>If the value is the five character sequence <bpt id="p1">**</bpt>heavy<ept id="p1">**</ept>, then the test is true.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が 5 文字シーケンス <bpt id="p1">**</bpt>heavy<ept id="p1">**</ept> である場合、テストは true になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><ph id="ph1">\#</ph>defInc and <ph id="ph2">\#</ph>defDec directives</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>defInc および <ph id="ph2">\#</ph>defDec ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> are the only directives that interpret the value of a macro and they apply only to macros that have a value that can be converted to the formal <bpt id="p3">**</bpt>int<ept id="p3">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> および <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> は、マクロの値を解釈する唯一のディレクティブであり、正式な <bpt id="p3">**</bpt>int<ept id="p3">**</ept> タイプに変換できる値を持つマクロにのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The value can only contain numerals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は、数字のみを含むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The only non-numeric character allowed is a leading negative sign (-).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">唯一の数字以外の文字は、先頭にマイナス記号 (-) が付いています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The integer value is treated as an X++ <bpt id="p1">**</bpt>int<ept id="p1">**</ept>, not as an <bpt id="p2">**</bpt>int64<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数値は、<bpt id="p1">**</bpt>int64<ept id="p1">**</ept> ではなく、X++ <bpt id="p2">**</bpt>int<ept id="p2">**</ept> として扱われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>For macro names that are used by the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> directive, it is important that the <bpt id="p2">**</bpt><ph id="ph2">\#</ph>define<ept id="p2">**</ept> directive that creates the macro not reside in a class declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> ディレクティブにより使用されるマクロ名については、マクロを作成する<bpt id="p2">**</bpt><ph id="ph2">\#</ph>定義<ept id="p2">**</ept> ディレクティブがクラス宣言に配置されないようにすることが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The behavior of <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> in these cases is unpredictable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの場合の <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> の動作は予測できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Instead, such macros should be defined in only a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、このようなマクロはメソッドだけで定義される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>We recommend that the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> directives only be used for macros that have an integer value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数値を持つマクロには <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> および <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> ディレクティブのみを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The precompiler follows special rules for <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> when the macro value is not an integer, or when the value is unusual or extreme.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、マクロの値が整数でないとき、あるいは値が異常または極端なとき、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> の特別なルールに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table lists the values that <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> converts to zero (0) and then increments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> がゼロ (0) に変換してから増分する値を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>When a value is converted to 0 by <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc,<ept id="p1">**</ept> the original value cannot be recovered, not even by <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc、<ept id="p1">**</ept> によって値が 0 に変換されると、<bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> によっても元の値を回復できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Macro value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロの値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>(+55)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(+55)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The positive sign (+) prefix makes the precompiler treat this as a non-numeric string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラス記号 (+) 接頭語により、プリコンパイラはこれを数字以外の文字列として扱います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The precompiler treats all non-numeric strings as 0 when it handles a <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> (or <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec)<ept id="p2">**</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> (または <bpt id="p2">**</bpt><ph id="ph2">\#</ph>識別子)<ept id="p2">**</ept> ディレクティブを扱うとき、数値以外のすべての文字列を 0 として処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>("3")</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(「3」)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Integers enclosed in quotation marks are treated as 0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引用符で囲まれた整数は、0 として扱われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The quotation marks are discarded, and these changes persist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引用符は破棄され、これらの変更はそのまま残ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>( )</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">( )</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A string of spaces is treated as 0, and then incremented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スペースの文字列が 0 として扱われ、増加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>A zero-length string is treated as 0, and then incremented, when the value is enclosed in parentheses, as in <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define.MyMac().<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">長さゼロの文字列は、0 として処理され、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>define.MyMac()<ept id="p1">**</ept> のように、値がかっこで囲まれている場合は増加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>(Random string.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ランダムな文字列です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Any non-numeric string of characters is treated as 0, and then incremented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数値以外の文字列は 0 として扱われ、次に増加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>(0x12)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(0x12)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Hexadecimal numbers are treated as non-numeric strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">16 進数は、数値以外の文字列として扱われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Therefore they are converted to 0, and then incremented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、それらは 0 に変換され、次に増分されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>(-44)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(-44)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Negative numbers are acceptable, including integers without the negative sign (-).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マイナス記号 (-) のない整数を含め、負の数は許容されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>(2147483647)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(2147483647)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The maximum positive <bpt id="p1">**</bpt>int<ept id="p1">**</ept> value is changed to the minimum negative <bpt id="p2">**</bpt>int<ept id="p2">**</ept> value by <ph id="ph1">\#</ph>defInc.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大の正の <bpt id="p1">**</bpt>int<ept id="p1">**</ept> 値は、<ph id="ph1">\#</ph>defInc によって最小の負の <bpt id="p2">**</bpt>int<ept id="p2">**</ept> 値に変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>(999888777666555)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(999888777666555)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Any large number, beyond the capacity of <bpt id="p1">**</bpt>int<ept id="p1">**</ept> and <bpt id="p2">**</bpt>int64<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int<ept id="p1">**</ept> および <bpt id="p2">**</bpt>int64<ept id="p2">**</ept> の容量を超えた大きな数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>This is treated as the maximum positive <bpt id="p1">**</bpt>int<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは最大の正の <bpt id="p1">**</bpt>int<ept id="p1">**</ept> 値として扱われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>(5.8)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(5.8)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Real numbers are truncated by <ph id="ph1">\#</ph>defDec (and <ph id="ph2">\#</ph>defInc).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実数は、<ph id="ph1">\#</ph>defDec (および <ph id="ph2">\#</ph>defInc) により切り捨てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Subsequent symbol substitution shows that the truncation persists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後続の記号置き換えは、切り捨てが永続化することを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>When no value and no parentheses are provided for the directive <ph id="ph1">\#</ph>define.MyValuelessMacro, the precompiler rejects use of the directive <ph id="ph2">\#</ph>defInc.MyValuelessMacro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>define.MyValuelessMacro ディレクティブの値とかっこが指定されていない場合は、プリコンパイラは <ph id="ph2">\#</ph>defInc.MyValuelessMacro ディレクティブの使用を拒否します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>In the following code sample, the initial value of the macro <bpt id="p1">**</bpt>CounterMacroA<ept id="p1">**</ept> is a string that can be converted into an integer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード サンプルでは、マクロ <bpt id="p1">**</bpt>CounterMacroA<ept id="p1">**</ept> の初期値は、整数に変換できる文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The sample shows how the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> directives can be used for this macro name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプルでは、このマクロ名に <bpt id="p1">**</bpt><ph id="ph1">\#</ph>defInc<ept id="p1">**</ept> および <bpt id="p2">**</bpt><ph id="ph2">\#</ph>defDec<ept id="p2">**</ept> の各ディレクティブをどのように使用できるかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><ph id="ph1">\#</ph>globaldefine directive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>globaldefine ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> directive is similar to the <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>Globaldefine<ept id="p1">&lt;/strong&gt;</ept> ディレクティブは、<bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> ディレクティブに似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>The difference is that <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> directives generally take precedence over <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globalmacro<ept id="p2">&lt;/strong&gt;</ept> directives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">違いは、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> ディレクティブは一般的に <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globalmacro<ept id="p2">&lt;/strong&gt;</ept> ディレクティブよりも優先されるということです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>This is true regardless of which directive occurs first in the X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、どのディレクティブが最初に X++ コードで発生するかに関係なく当てはまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> never overwrites a <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> directive that has both a macro name and a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> は、マクロ名と値の両方を持つ <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> ディレクティブを上書きすることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>A <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> can overwrite another <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globaldefine. **A **<ph id="ph3">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> directive that has only a name does not overwrite a <ph id="ph4">\#</ph>globalmacro that has both a name and a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> は別の <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globaldefine を上書きすることができます。**A **<ph id="ph3">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> ディレクティブは、名前と値の両方を持つ <ph id="ph4">\#</ph>globalmacro を上書きしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>It is recommended that you use <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define,<ept id="p1">&lt;/strong&gt;</ept> and that you do not use <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globaldefine.<ept id="p2">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> を使用して <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globaldefine<ept id="p2">&lt;/strong&gt;</ept> を使用しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Use of <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> can create uncertainty that makes code difficult to maintain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> を使用すると、不確実性が生じてコードの保守が困難になる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>The exact semantics of <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> cannot be achieved through <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>if<ept id="p2">&lt;/strong&gt;</ept> test directives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> の正確なセマンティクスは、<bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>if<ept id="p2">&lt;/strong&gt;</ept> テストディレクティブでは達成できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>By using <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>if<ept id="p1">&lt;/strong&gt;</ept> tests you can avoid overwriting a <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> and a <bpt id="p3">&lt;strong&gt;</bpt><ph id="ph3">\#</ph>globaldefine.<ept id="p3">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>if<ept id="p1">&lt;/strong&gt;</ept> テストを使うことにより <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> および <bpt id="p3">&lt;strong&gt;</bpt><ph id="ph3">\#</ph>globaldefine<ept id="p3">&lt;/strong&gt;</ept> の上書きを回避することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>But <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>if<ept id="p1">&lt;/strong&gt;</ept> tests cannot distinguish between <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> and <bpt id="p3">&lt;strong&gt;</bpt><ph id="ph3">\#</ph>globaldefine<ept id="p3">&lt;/strong&gt;</ept> macros.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>if<ept id="p1">&lt;/strong&gt;</ept> テストは <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> と <bpt id="p3">&lt;strong&gt;</bpt><ph id="ph3">\#</ph>globaldefine<ept id="p3">&lt;/strong&gt;</ept> マクロを区別できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The following code sample is the closest you can come to achieving the <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> semantic with other directives such as <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>if.<ept id="p2">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、<bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>if<ept id="p2">&lt;/strong&gt;</ept> などの他のディレクティブで <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">&lt;/strong&gt;</ept> セマンティクスを達成するために最も近い例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The following code sample shows a difference in the behavior of <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>globaldefine.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> と <bpt id="p2">**</bpt><ph id="ph2">\#</ph>globaldefine<ept id="p2">**</ept> の動作の違いを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Following the code sample is a table explaining the conclusions from the output.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のコード サンプルは、出力からの結びを説明するテーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The primary test case in the code sample is labeled <bpt id="p1">**</bpt>12<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード サンプルの基本テスト ケースの名前は <bpt id="p1">**</bpt>12<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Macro parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>You can define macro values to include parameter symbols.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータ シンボルを含めるようにマクロの値を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The first parameter symbol is %1, the second is %2, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のパラメーター記号は %1、2 番目のパラメーター記号は %2 で、以降は同様の形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You pass values for the parameters when you reference the macro symbol name for expansion.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開のためにマクロ記号名を参照するときは、パラメーターの値を渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Macro parameter values are character sequences of no formal type, and they are comma delimited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ パラメーターの値は、正式な型のない文字シーケンスで、コンマで区切られます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>There is no way to pass in a comma as part of a parameter value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター値の一部としてカンマで渡す方法はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>The number of parameters passed can be less than, greater than, or equal to the number of parameters that the macro value is designed to receive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">渡されるパラメーターの数は、マクロ値が受け取るように設計されているパラメーターの数よりも少なくても、大きくても等しくてもかまいません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The system tolerates mismatches in the number of parameters passed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムは、渡されたパラメーターの数の不一致を許容します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>If fewer parameters are passed than the macro expects, each omitted parameter is treated as a zero-length sequence of characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロが期待するよりも少ないパラメーターが指定された場合、省略された各パラメーターは、長さが 0 の文字列として扱われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>In the following code sample, <bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> is defined to have a value that contains parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード サンプルでは、<bpt id="p1">**</bpt>MyMacro<ept id="p1">**</ept> はパラメーターを含む値を持つよう定義されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Macro substitution symbols are given with parameter values in parentheses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロの代入記号は、かっこで囲まれたパラメーターの値で指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><ph id="ph1">\#</ph>localmacro and <ph id="ph2">\#</ph>globalmacro directives</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>localmacro および <ph id="ph2">\#</ph>globalmacro ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> directive is a good choice when you want a macro to have a value that is several lines long, or when your macro value contains a closing parenthesis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>Localmacro<ept id="p1">&lt;/strong&gt;</ept> ディレクティブは、複数の行にまたがる値をマクロに設定する場合や、マクロの値にかっこが含まれている場合に推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> directive is a good choice when you want your macro value to be lines of X++ or SQL code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> ディレクティブは、マクロの値を数行の X++ または SQL コードにする場合に推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> directive can be written as <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>macro.<ept id="p2">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>Localmacro<ept id="p1">&lt;/strong&gt;</ept> ディレクティブは、<bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>macro.<ept id="p2">&lt;/strong&gt;</ept> として記述することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>However, <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> is the recommended term.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> が勧められている用語です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Both macros have the same behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どちらのマクロも同じ動作をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>By using the <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>if<ept id="p1">&lt;/strong&gt;</ept> directive, you can test whether a macro name is declared with the <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>if<ept id="p1">&lt;/strong&gt;</ept> ディレクティブを使用することにより、マクロ名が <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> ディレクティブで宣言されているかどうかをテストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>However, you cannot test whether the macro name is declared with the <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、マクロ名が <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> ディレクティブで宣言されているどうかをテストすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Only macros declared by using the <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> directive are affected by the <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>undef<ept id="p2">&lt;/strong&gt;</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> ディレクティブを使用して宣言されたマクロのみ、<bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>undef<ept id="p2">&lt;/strong&gt;</ept> ディレクティブの影響を受けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>In a <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> directive, you can specify a name that is already in scope as a <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>localmacro.<ept id="p2">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> ディレクティブでは、既にスコープ内にある名前を <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">&lt;/strong&gt;</ept> として指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The effect is to discard the <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> and create a <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果は、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept>を破棄して、<bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> マクロを作成することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This also applies to the opposite sequence, which means that a <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> can redefine a <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define.<ept id="p2">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは反対のシーケンスにも当てはまります。つまり、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> は <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>define<ept id="p2">&lt;/strong&gt;</ept> を再定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> (that has both a macro name and a value) always overrides a previous <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">&lt;/strong&gt;</ept> that has the same name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(マクロ名と値の両方を持つ) <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">&lt;/strong&gt;</ept> は、同じ名前を持つ前の <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">&lt;/strong&gt;</ept> を常に上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>However, you cannot always be sure whether the override occurs when you use <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globalmacro.<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globalmacro<ept id="p1">&lt;/strong&gt;</ept> を使用する場合、オーバーライドが発生するかどうかは必ず分かるわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>For this reason we recommend that you do not use <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>globalmacro. **This same problem occurs with **<ph id="ph2">\#</ph>globaldefine.<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このため、<bpt id="p1">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>globaldefine で**この同じ問題が発生**する <ph id="ph1">\#</ph>globalmacro<ept id="p1">&lt;/strong&gt;</ept> を使用しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The main difference between a <bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> macro and a <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">&lt;/strong&gt;</ept> macro is in how their syntax is terminated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><ph id="ph1">\#</ph>define<ept id="p1">&lt;/strong&gt;</ept> マクロと <bpt id="p2">&lt;strong&gt;</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">&lt;/strong&gt;</ept> マクロの主な違いは、構文がどのように終了するかです</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The terminators are as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のターミネーターがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> – is terminated by– <bpt id="p2">**</bpt>)<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>定義<ept id="p1">**</ept> - - によって終了<bpt id="p2">**</bpt>)<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> – is terminated by– <bpt id="p2">**</bpt><ph id="ph2">\#</ph>endmacro<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> - - によって終了 <bpt id="p2">**</bpt><ph id="ph2">\#</ph>endmacro<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source><bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> is a better choice for macros with multiple line values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> は、複数の行の値を持つマクロに適しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Multiple line values are typically lines of X++ or SQL code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の行の値は、通常 X++ または SQL コードの行です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>X++ and SQL contain lots of parentheses, and these would prematurely terminate a <ph id="ph1">\#</ph>define.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ および SQL には多くのパラメーターが含まれ、これらは処理の途中で <ph id="ph1">\#</ph>define を終了する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Both <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> can be declared and terminated on either a single line or on subsequent lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>定義<ept id="p1">**</ept>と <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> の両方を宣言し、単一行または後続の行で終了することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>In practice, the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> is terminated on the same line that it is declared on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> は宣言されている同じ行で終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>In practice, the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> is terminated on a subsequent line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> は後続の行で終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Where both macro names and values are supplied, the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>globalmacro<ept id="p1">**</ept> directive cannot override the <ph id="ph2">\#</ph>define directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ名と値の両方を指定すると、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>globalmacro<ept id="p1">**</ept> 指令は <ph id="ph2">\#</ph>define 指令を上書きできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Also, the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">**</ept> directive cannot override the <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>globaldefine<ept id="p1">**</ept> ディレクティブは <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> ディレクティブへの上書きができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Code examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The following code sample shows how to use the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> ディレクティブの使用方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>It demonstrates that the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef<ept id="p1">**</ept> directive does not affect <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> macros.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef<ept id="p1">**</ept> ディレクティブが <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> マクロに影響しないことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>It also shows that <ph id="ph1">\#</ph>if tests cannot determine whether a <bpt id="p1">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p1">**</ept> macro has been defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<ph id="ph1">\#</ph>if テストでは <bpt id="p1">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p1">**</ept> マクロが定義されているかどうかを決定できないことも示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The following X++ code sample shows that <bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> overrides a <bpt id="p2">**</bpt><ph id="ph2">\#</ph>globalmacro<ept id="p2">**</ept> of the same macro name, but that <bpt id="p3">**</bpt><ph id="ph3">\#</ph>globalmacro<ept id="p3">**</ept> does not override <bpt id="p4">**</bpt><ph id="ph4">\#</ph>localmacro.<ept id="p4">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の X++ コード例は、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>localmacro<ept id="p1">**</ept> が同じマクロ名の <bpt id="p2">**</bpt><ph id="ph2">\#</ph>globalmacro<ept id="p2">**</ept> を上書きしますが、<bpt id="p3">**</bpt><ph id="ph3">\#</ph>globalmacro<ept id="p3">**</ept> は <bpt id="p4">**</bpt><ph id="ph4">\#</ph>localmacro<ept id="p4">**</ept> を上書きしないことを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Nesting Macro Symbols</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になっているマクロ記号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>You can nest precompiler definition directives inside an outer definition directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラ定義ディレクティブは他の外部定義ディレクティブ内に入れ子にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The main definition directives are <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> and **<ph id="ph2">\#</ph>localmacro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主な定義ディレクティブは、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> と <ph id="ph2">\#</ph>localmacro です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>**The cases for which this topic provides code samples are as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">**このトピックでコード サンプルを提供する場合は、次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Transitive substitution: A <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> macro can have the symbol for another macro as its value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推移的置換: A <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> マクロは、別のマクロのシンボルをその値として持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Transitive substitution of the symbol occurs in X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シンボルの推移的置換は X++ コードで行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>No transitive substitution: An <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> directive test of a macro value does not perform substitutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推移的置換なし: マクロ値の <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> ディレクティブ テストは置換を実行しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Macro within a macro: A <ph id="ph1">\#</ph>define directive can be given inside a <bpt id="p1">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p1">**</ept> directive, or a <bpt id="p2">**</bpt><ph id="ph3">\#</ph>localmacro<ept id="p2">**</ept> can be inside a <bpt id="p3">**</bpt><ph id="ph4">\#</ph>define.<ept id="p3">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ内のマクロ: <ph id="ph1">\#</ph>define ディレクティブを <bpt id="p1">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p1">**</ept> ディレクティブ内に指定したり、<bpt id="p2">**</bpt><ph id="ph3">\#</ph>localmacro<ept id="p2">**</ept> を <bpt id="p3">**</bpt><ph id="ph4">\#</ph>define<ept id="p3">**</ept> 内に指定したりできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Transitive Substitution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推移的置換</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>In the following code sample, the value of the first <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> variable includes a symbol (<ph id="ph2">\#</ph>D) of the second <bpt id="p2">**</bpt><ph id="ph3">\#</ph>define<ept id="p2">**</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、最初の <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> 変数の値には、2 つ目の <bpt id="p2">**</bpt><ph id="ph3">\#</ph>define<ept id="p2">**</ept> 変数の記号 (<ph id="ph2">\#</ph>D) が含まれます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>This works even though the expansion symbol <ph id="ph1">\#</ph>D occurs before macro <bpt id="p1">**</bpt>D<ept id="p1">**</ept> is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、マクロ <bpt id="p1">**</bpt>D<ept id="p1">**</ept> を定義する前に拡張シンボル <ph id="ph1">\#</ph>D が存在していても機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>No transitive substitution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推移的置換なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The following code sample tries to determine whether two macro variables have the same value, without specifying what that value might be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、2 つのマクロ変数が同じ値を持っているかどうかを、その値が何であるかを指定せずに判断しようとしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>The output shows that this determination cannot be made..</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力は、この決定が行えないことを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The following code sample shows that the <ph id="ph1">\#</ph>defInc directive does not lead to transitive substitution of symbol values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、<ph id="ph1">\#</ph>defInc ディレクティブが記号値の推移的置換につながっていないことを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>For more information about the <ph id="ph1">\#</ph>defInc directive, see How to: Use the <ph id="ph2">\#</ph>defInc and <ph id="ph3">\#</ph>defDec Directives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>defInc ディレクティブの詳細については、方法: <ph id="ph2">\#</ph>defInc および <ph id="ph3">\#</ph>defDec ディレクティブの使用を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>After the <ph id="ph1">\#</ph>defInc.E2 directive, the subsequent output value for <ph id="ph2">\#</ph>E2 shows the value for <bpt id="p1">**</bpt>E2<ept id="p1">**</ept> is converted to zero (0) by <ph id="ph3">\#</ph>defInc.E2 before it is incremented to one (1).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>defInc.E2 ディレクティブの後、<ph id="ph2">\#</ph>E2 の次の出力値は、<bpt id="p1">**</bpt>E2<ept id="p1">**</ept> の値が 1 に増加する前に、<ph id="ph3">\#</ph>defInc.E2 によってゼロ (0) に変換されることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Before the conversion, the value of <bpt id="p1">**</bpt>E2<ept id="p1">**</ept> was the three characters <ph id="ph1">\#</ph>E2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換する前に、<bpt id="p1">**</bpt>E2<ept id="p1">**</ept> の値は 3 文字 <ph id="ph1">\#</ph>E2 でした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The output for test case <bpt id="p1">**</bpt>36<ept id="p1">**</ept> shows the value has been converted to 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト ケースの出力 <bpt id="p1">**</bpt>36<ept id="p1">**</ept> は、値が 1 に変換されたことを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Macro within a macro</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ内のマクロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>A <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> directive can be given inside a <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> directive, and a <bpt id="p3">**</bpt><ph id="ph3">\#</ph>localmacro<ept id="p3">**</ept> can be inside a <ph id="ph4">\#</ph>define.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> ディレクティブは <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> 内に指定することができ、また <bpt id="p3">**</bpt><ph id="ph3">\#</ph>localmacro<ept id="p3">**</ept> ディレクティブを<ph id="ph4">\#</ph> define 内に指定することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This is shown in the following code sample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、次のコード サンプルに示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><ph id="ph1">\#</ph>macrolib directive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>macrolib ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>In the Application Explorer under the Macros node, there are many library nodes that contain sets of macro directives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ ノードの下のアプリケーション エクスプローラーには、マクロ ディレクティブのセットが含まれる多くのライブラリ ノードがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Both <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> often appear in the contents of these macro libraries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>定義<ept id="p1">**</ept>および <bpt id="p2">**</bpt><ph id="ph2">\#</ph>localmacro<ept id="p2">**</ept> の両方がこれらのマクロ ライブラリの内容に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>You can use the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib.MyAOTMacroLibrary<ept id="p1">**</ept> to include the contents of a macro library in your X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib.MyAOTMacroLibrary<ept id="p1">**</ept> を使用すると、マクロ ライブラリのコンテンツをユーザーの X++ コードに含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph2">\#</ph>undef<ept id="p2">**</ept> directives do not apply to <bpt id="p3">**</bpt><ph id="ph3">\#</ph>macrolib<ept id="p3">**</ept> names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>if<ept id="p1">**</ept> および <bpt id="p2">**</bpt><ph id="ph2">\#</ph>undef<ept id="p2">**</ept> ディレクティブは、<bpt id="p3">**</bpt><ph id="ph3">\#</ph>macrolib<ept id="p3">**</ept> 名には適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>However, they do apply to <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> directives that are the contents of a <bpt id="p2">**</bpt><ph id="ph2">\#</ph>macrolib<ept id="p2">**</ept> macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、それは <bpt id="p2">**</bpt><ph id="ph2">\#</ph>macrolib<ept id="p2">**</ept> マクロのコンテンツである<bpt id="p1">**</bpt><ph id="ph1">\#</ph>定義<ept id="p1">**</ept>ディレクティブに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The directive <bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib.MyAOTMacroLibrary<ept id="p1">**</ept> can also be written as <bpt id="p2">**</bpt><ph id="ph2">\#</ph>MyAOTMacroLibrary.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクティブ <bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib.MyAOTMacroLibrary<ept id="p1">**</ept> は、<bpt id="p2">**</bpt><ph id="ph2">\#</ph>MyAOTMacroLibrary<ept id="p2">**</ept> として書き込むこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib<ept id="p1">**</ept> prefix is recommended because it is never ambiguous to a person who later reads the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib<ept id="p1">**</ept> プレフィックスを使うと後でコードを読むときにあいまいにならないため、推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Create a macro library</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ ライブラリの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>To create a macro library:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ ライブラリを作成するには、次のようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>In <bpt id="p1">**</bpt>Solution Explorer,<ept id="p1">**</ept> right-click on the project, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept> and then <bpt id="p3">**</bpt>New item.<ept id="p3">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、プロジェクトを右クリックし、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択してから<bpt id="p3">**</bpt>新しい項目<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>In the <bpt id="p1">**</bpt>Add New Item<ept id="p1">**</ept> dialog, select Installed and then <bpt id="p2">**</bpt>AX Artifacts<ept id="p2">**</ept> in the left pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい項目の追加<ept id="p1">**</ept>ダイアログで、インストール済みを選択してから左ウィンドウの <bpt id="p2">**</bpt>AX アーティファクト<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>In the middle pane, select <bpt id="p1">**</bpt>Macro.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">中央ウィンドウで<bpt id="p1">**</bpt>マクロ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Enter a name and click <bpt id="p1">**</bpt>Add.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を入力し、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Save the macro file and refresh the Application Explorer to find your macro library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロ ファイルを保存し、マクロ ライブラリを検索するためにアプリケーション エクスプローラーを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Code examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Finance and Operations has a macro library that is named <bpt id="p1">**</bpt>Event.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations には<bpt id="p1">**</bpt>イベント<ept id="p1">**</ept>と呼ばれるマクロ ライブラリがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>This macro library contains the directive <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define.DefaultEventPollFrequency(15)<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このマクロ ライブラリには、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>define.DefaultEventPollFrequency(15)<ept id="p1">**</ept> という指令が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>The following code sample shows that the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib.Event<ept id="p1">**</ept> directive makes the macro <bpt id="p2">**</bpt><ph id="ph2">\#</ph>DefaultEventPollFrequency<ept id="p2">**</ept> available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>macrolib.Event<ept id="p1">**</ept> ディレクティブがマクロ <bpt id="p2">**</bpt><ph id="ph2">\#</ph>DefaultEventPollFrequency<ept id="p2">**</ept> を使用可能にすることを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>The following code example shows what happens when you write a <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> for a name that is already the name of a node in the macro library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、既にマクロ ライブラリ内のノードの名前である名前に対して <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> を記述するとどうなるかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>For this example, there is a node named <bpt id="p1">**</bpt>MacLib23,<ept id="p1">**</ept> and its contents are one <bpt id="p2">**</bpt><ph id="ph1">\#</ph>define<ept id="p2">**</ept> as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>MacLib23<ept id="p1">**</ept>という名前のノードがあり、その内容は次のように 1 つの<bpt id="p2">**</bpt><ph id="ph1">\#</ph>定義<ept id="p2">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>After a <ph id="ph1">\#</ph>macrolib directive is issued for <bpt id="p1">**</bpt>MacLib23<ept id="p1">**</ept>, <bpt id="p2">**</bpt><ph id="ph2">\#</ph>define<ept id="p2">**</ept> and <bpt id="p3">**</bpt><ph id="ph3">\#</ph>undef<ept id="p3">**</ept> directives have no effect on the <bpt id="p4">**</bpt><ph id="ph4">\#</ph>macrolib<ept id="p4">**</ept> macro (see output <ph id="ph5">\_</ph>BB).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>macrolib ディレクティブが <bpt id="p1">**</bpt>MacLib23<ept id="p1">**</ept> に対して発行された後、<bpt id="p2">**</bpt><ph id="ph2">\#</ph>define<ept id="p2">**</ept> と <bpt id="p3">**</bpt><ph id="ph3">\#</ph>undef<ept id="p3">**</ept> ディレクティブは、<bpt id="p4">**</bpt><ph id="ph4">\#</ph>macrolib<ept id="p4">**</ept> マクロに影響しません (出力 <ph id="ph5">\_</ph>BB を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>However, a <bpt id="p1">**</bpt><ph id="ph1">\#</ph>define<ept id="p1">**</ept> in the contents of a <bpt id="p2">**</bpt><ph id="ph2">\#</ph>macrolib<ept id="p2">**</ept> macro can be overwritten by a subsequent <ph id="ph3">\#</ph>define or <bpt id="p3">**</bpt><ph id="ph4">\#</ph>undef<ept id="p3">**</ept> in the code (see output <ph id="ph5">\_</ph>DD).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p2">**</bpt><ph id="ph2">\#</ph>macrolib<ept id="p2">**</ept> マクロのコンテンツでの<bpt id="p1">**</bpt><ph id="ph1">\#</ph>定義<ept id="p1">**</ept>は、それ以降のコードでの<ph id="ph3">\#</ph>定義または <bpt id="p3">**</bpt><ph id="ph4">\#</ph>undef<ept id="p3">**</ept> により上書きされます (出力 <ph id="ph5">\_</ph>DD を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source><ph id="ph1">\#</ph>linenumber Directive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\#</ph>linenumber ディレクティブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>You can use the <ph id="ph1">\#</ph>linenumber directive during your development and debugging of code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発中およびコードのデバッグ中は、<ph id="ph1">\#</ph>linenumber ディレクティブを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>It is replaced by the physical line number in the code file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コード ファイル内の物理的な行番号に置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>The following X++ code sample shows the behavior of the <bpt id="p1">**</bpt><ph id="ph1">\#</ph>linenumber<ept id="p1">**</ept> directive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の X++ コード例は、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>linenumber<ept id="p1">**</ept> ディレクティブの動作を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Range (scope) of macros</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロの範囲 (スコープ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The range in which a macro can be referenced depends on where the macro is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロが参照できる範囲は、マクロが定義されている場所によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>In a class, macros that are defined in the parent class can be referenced, but macros defined in a child class cannot be referenced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスでは、親クラスで定義されているマクロを参照できますが、子クラスで定義されているマクロを参照することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>When the precompiler handles a child class, the precompiler first traces the inheritance chain to the most ascendant class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラが子クラスを処理するとき、プリコンパイラは最初に最上位の直系のクラスへの継承チェーンを追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>The precompiler processes all the directives from the class declaration part of the ascendant class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、上位クラスのクラス宣言部分からのすべてのディレクティブを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>It stores all the macros and their values in its internal tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内部テーブルにすべてのマクロとその値を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>The precompiler handles the next class in the inheritance chain the same way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、同じ方法で、継承チェーン内の次のクラスを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>The result of the directives in each class declaration are applied to the internal tables that are already populated from directives that were found earlier in the inheritance chain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各クラス宣言でのディレクティブの結果は、継承チェーンの初期段階で見つかったディレクティブからすでに入力されている内部テーブルに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>When the precompiler reaches the target child class, it again handles the class declaration part.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、ターゲットの子クラスに達すると、もう一度クラス宣言部分を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>However, it next handles each method in a series of separate operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、次に一連の個別操作で各メソッドを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>The precompiler updates its internal tables in a way that the state of the tables can be restored as they were before processing of the current method began.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、内部テーブルの状態を現在のメソッドの処理を開始する前の状態に復元できる方法で、その内部テーブルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>After the first method is handled, the internal tables are restored before the next method is handled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のメソッドが処理された後、内部テーブルは次のメソッドが処理される前に復元されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>The Method is All Contents of the Node</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドはノードのすべての内容</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In this context, a method is defined as the contents of a method node in the Application Object Tree (AOT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンテキストでは、メソッドがアプリケーション オブジェクト ツリー (AOT) でのメソッド ノードのコンテンツとして定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>In the AOT, you can expand the Classes node, expand a class node, right-click a method node, and then select Edit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT で、クラス ノードを展開し、クラス ノードを展開して、メソッドのノードを右クリックしてから編集を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Then you can add a line for <ph id="ph1">\#</ph>define.MyMacro("abc") before the method declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、メソッド宣言の前に <ph id="ph1">\#</ph>define.MyMacro("abc") の行を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>The precompiler treats this <ph id="ph1">\#</ph>define directive as part of the method, even though the <ph id="ph2">\#</ph>define occurs outside the <ph id="ph3">{}</ph> block of the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリコンパイラは、<ph id="ph2">\#</ph>define ディレクティブがメソッドの <ph id="ph3">{}</ph> ブロックの外である場合でも、その <ph id="ph1">\#</ph>define ディレクティブをメソッドの一部として処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Class Inheritance and Macro Reference Range</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス継承とマクロ参照範囲</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>The following code example demonstrates the range of macro referencing in class inheritance scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、クラス継承シナリオで参照するマクロの範囲を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>The primary line to notice in the method's output is the line labeled ClassC<ph id="ph1">\_</ph>h.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの出力にある基本明細行は、ClassC<ph id="ph1">\_</ph>hという名前の明細行です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>It shows that a macro defined in a grandparent class can be referenced in a method of the grandchild class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">親の親クラスで定義されたマクロを孫クラスのメソッドで参照できることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Another important line in the output is labeled ClassA<ph id="ph1">\_</ph>k.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力のもう 1 つの重要な行には ClassA<ph id="ph1">\_</ph>k というラベルが付いています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>This line shows that a macro defined in a method is not available in other methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この行は、あるメソッドで定義されたマクロが他のメソッドでは使用できないことを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>ClassA is the base class and it defines several macros in its class declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClassA は基本クラスであり、クラス宣言にいくつかのマクロを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Its descendant classes reference these macros.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その子孫クラスは、これらのマクロを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>The base class also defines a macro inside one of its methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラスは、そのいずれかのメソッドの内部のマクロも定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>A second method in this class determines the macro is defined out of range and cannot be referenced in the second method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスの 2 番目のメソッドは、マクロが範囲外に定義されていると判断し、2 番目のメソッドで参照することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>The <bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef.MacroRange333<ept id="p1">**</ept> in the method <bpt id="p2">**</bpt>UseOtherMethodMacro<ept id="p2">**</ept> affects the availability of macro <bpt id="p3">**</bpt>MacroRange333<ept id="p3">**</ept> in the rest of that method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド <bpt id="p2">**</bpt>UseOtherMethodMacro<ept id="p2">**</ept> の <bpt id="p1">**</bpt><ph id="ph1">\#</ph>undef.MacroRange333<ept id="p1">**</ept>は、そのメソッドの残りの部分でマクロ <bpt id="p3">**</bpt>MacroRange333<ept id="p3">**</ept> を使用できるかどうかに影響を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Descendant classes can still reference <bpt id="p1">**</bpt>MacroRange333<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">派生クラスは <bpt id="p1">**</bpt>MacroRange333<ept id="p1">**</ept> を参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>ClassB extends ClassA and it undefines the macro <bpt id="p1">**</bpt>MacroRangeA<ept id="p1">**</ept> that is defined in its parent class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClassB は ClassA を拡張し、親クラスで定義されている <bpt id="p1">**</bpt>MacroRangeA<ept id="p1">**</ept> マクロの定義を解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>This makes the macro unavailable to any class that extends the present class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、現在のクラスを拡張するすべてのクラスでマクロを使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>The present class also redefines the macro <bpt id="p1">**</bpt>MacroRangeB<ept id="p1">**</ept> that is defined in its parent class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、存在するクラスは、その親クラスで定義される <bpt id="p1">**</bpt>MacroRangeB<ept id="p1">**</ept> マクロの再定義も行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>This changes the value of the macro (from positive to negative).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、マクロの値が (正の値から負の値に) 変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>ClassC extends ClassB and it uses <bpt id="p1">**</bpt><ph id="ph1">\#</ph>ifnot<ept id="p1">**</ept> to demonstrate that it cannot access the <bpt id="p2">**</bpt>MacroRangeA<ept id="p2">**</ept> macro that the base class, ClassInheritanceOfMacrosCBase1, defines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClassC は ClassB を拡張し、<bpt id="p1">**</bpt><ph id="ph1">\#</ph>ifnot<ept id="p1">**</ept> を使用して、基本クラス ClassInheritanceOfMacrosCBase1 が定義する <bpt id="p2">**</bpt>MacroRangeA<ept id="p2">**</ept> マクロにアクセスできないことを実証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The reason is that the mid-level class undefined the macro.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その理由は、中間レベルのクラスがマクロを定義していないためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>This class also demonstrates that it can access the macro <bpt id="p1">**</bpt>MacroRange333<ept id="p1">**</ept> that ClassInheritanceOfMacrosCBase1 class defines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、このクラスは、ClassInheritanceOfMacrosCBase1 クラスが定義するマクロ <bpt id="p1">**</bpt>MacroRange333<ept id="p1">**</ept> にアクセスできることも示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>TestClass contains a method that calls the demonstration methods and displays the results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TestClass にはデモ メソッドを呼び出して結果を表示するメソッドが含まれています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>