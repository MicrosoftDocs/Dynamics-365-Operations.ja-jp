<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="xpp-operator-precedence.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>xpp-operator-precedence.cf1080.be5c383e958a4b83f542307824e2ee33336c89fc.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>be5c383e958a4b83f542307824e2ee33336c89fc</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-ref\xpp-operator-precedence.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Operator precedence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">演算子の優先順位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes operator precedence in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations の演算子の優先順位について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Operator precedence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">演算子の優先順位</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes operator precedence in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations の演算子の優先順位について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The order in which a compound expression is evaluated is important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複合式を評価する順番は重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For example, (x + y / 100) gives a different result depending on whether the addition or the division is performed first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、(x + y / 100) は追加または区分を最初に実行するかどうかによって、結果が異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can use parentheses ( ) to explicitly tell the X++ compiler how you want an expression to be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">かっこ () を使用すると、式の評価方法を明示的に X++ コンパイラに指示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, (x + y)/ 100.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例えば、(x + y)/ 100。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you do not explicitly tell the compiler the order that you want operations to be performed in, the order is based on the precedence assigned to the operators.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オペレーションを実行する順序をコンパイラーに明示的に伝えていない場合、順序はオペレーターに割り当てられた優先順位に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For example, the division operator has a higher precedence than the addition operator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、除算演算子には、加算演算子より高い優先順位があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For x + y / 100, the compiler would evaluate y/100 first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x + y / 100 については、コンパイラは y/100 を最初に評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>So, x + y / 100 is equivalent to x + (y / 100).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、x + y/100 は x + (y/100) と等しくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To make your code easy to read and maintain, be explicit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを読みやすく管理しやすくするために、明示的に記述します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Indicate with parentheses which operators should be evaluated first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に評価すべき演算子をかっこで示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Order of Operator Precedence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">演算子の優先度順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The operators in the following table are listed in precedence order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルの演算子は、優先順位の順に並べられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The higher in the table an operator appears, the higher precedence it has.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの演算子は高いほど、その優先順位が高くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Operators with higher precedence are evaluated before operators with a lower precedence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高い優先順位がある演算子は、低い優先順位がある演算子より前に評価されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Note that the operator precedence of X++ is not the same as other languages, for example C<ph id="ph1">\#</ph> and Java.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の演算子の優先順位は、C<ph id="ph1">\#</ph> および Java などの他の言語と同じではないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Operators in precedence order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">演算子 (優先順位)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>unary operators</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単項演算子</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>- ~ !</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">- ～ !</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>multiplicative, shift, bitwise AND, bitwise exclusive OR</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">乗算、シフト、AND、ビット演算排他的 OR</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><ph id="ph1">\*</ph> / % DIV <ph id="ph2">&amp;lt;</ph><ph id="ph3">&amp;lt;</ph> <ph id="ph4">&amp;gt;</ph><ph id="ph5">&amp;gt;</ph> &amp; ^</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph> / % DIV <ph id="ph2">&amp;lt;</ph><ph id="ph3">&amp;lt;</ph> <ph id="ph4">&amp;gt;</ph><ph id="ph5">&amp;gt;</ph> &amp; ^</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>additive, bitwise inclusive OR</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">加法、ビット演算包括的 OR</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>+ -</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">+ -</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>relational, equality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーショナル、同等</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><ph id="ph1">&amp;lt;</ph> <ph id="ph2">&amp;lt;</ph>= == != <ph id="ph3">&amp;gt;</ph> <ph id="ph4">&amp;gt;</ph>= like as is</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph> <ph id="ph2">&amp;lt;</ph>= == != <ph id="ph3">&amp;gt;</ph> <ph id="ph4">&amp;gt;</ph>= 現状のとおり</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>logical operators (AND, OR)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">論理演算子 (AND、OR)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>conditional</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件付</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">?</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Operators on the same line have equal precedence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ行の演算子には、同等な優先順位があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If there is more than one of these operators in an expression, the expression is evaluated from left to right unless assignment operators are used (these are evaluated from right to left).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">式にあるこれらの演算子が 1 つ以上ある場合、代入演算子が使用されていない限り、式は左から右に評価されます (これらは右から左に評価されます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For example, &amp;&amp; (logical AND) and || (logical OR) have the same precedence and are evaluated from left to right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、&amp;&amp; (論理的 AND) および || (論理的 OR) は、優先順位が等しく、左から右に評価されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>This means that:0&amp;&amp;0||1 == 1, and 1||0&amp;&amp;0 == 0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、0&amp;&amp;0||1 == 1、および 1||0&amp;&amp;0 == 0 です</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">[</bpt>Assignment Operators<ept id="p1">](https://msdn.microsoft.com/library/d4e86b9c-be82-4f19-ad86-7722344a05f3(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>代入演算子<ept id="p1">](https://msdn.microsoft.com/library/d4e86b9c-be82-4f19-ad86-7722344a05f3(AX.60).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">[</bpt>Arithmetic Operators<ept id="p1">](https://msdn.microsoft.com/library/cffbc613-3875-4520-9dea-046dc99aab99(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>算術演算子<ept id="p1">](https://msdn.microsoft.com/library/cffbc613-3875-4520-9dea-046dc99aab99(AX.60).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt>Relational Operators<ept id="p1">](https://msdn.microsoft.com/library/702af366-4d46-445e-bd4b-722c9845199f(AX.60).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>リレーショナル演算子<ept id="p1">](https://msdn.microsoft.com/library/702af366-4d46-445e-bd4b-722c9845199f(AX.60).aspx)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>