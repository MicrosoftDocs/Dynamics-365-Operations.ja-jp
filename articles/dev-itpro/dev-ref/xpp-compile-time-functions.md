<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="xpp-compile-time-functions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>xpp-compile-time-functions.650ad6.34e9438ef0764399ac9de3444330d05a47e72e5f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>34e9438ef0764399ac9de3444330d05a47e72e5f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-ref\xpp-compile-time-functions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>X++ compile-time functions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイル時関数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic lists the compile-time functions and describes their syntax, parameters, and return values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>X++ compile-time functions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイル時関数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic lists the compile-time functions and describes their syntax, parameters, and return values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Compile-time functions are executed early during compilation of X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>They should be used wherever possible in X++ code to make the code resilient to changes to the metadata stored in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Compile-time functions have their input value verified by the compiler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル時関数は、コンパイラによって入力値が検証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If the input value is not found to match any existing object in the Application Explorer, the compiler issues an error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The inputs to these functions must be literals, because the compiler cannot determine the value that a variable contains at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>A compile-time function is a metadata assertion function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル時関数は、メタデータ アサーション関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It takes arguments that represents an entity in the Application Explorer and validates the arguments at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>It has no effect at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に影響を与えません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Attributes are classes that inherit from the <bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性は <bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> クラスから継承するクラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To support the validation of form, report, query, and menu metadata, use the <bpt id="p1">**</bpt>AutoDeclaration<ept id="p1">**</ept> property on controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの <bpt id="p1">**</bpt>AutoDeclaration<ept id="p1">**</ept> プロパティを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Most of these functions retrieve metadata about items that are in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Some common compile time functions are as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの一般的なコンパイル時機能は、次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><ph id="ph1">`classNum`</ph> – Retrieves the ID of a class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`classNum`</ph> – クラスの ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><ph id="ph1">`classStr`</ph> – During compile time, verifies that a class of that name exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`classStr`</ph> – コンパイル時に、その名前のクラスが存在することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This approach is better than discovering the error later during run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、実行時にエラーを後で発見するよりも優れています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><ph id="ph1">`evalBuf`</ph>– Evaluates the input string of X++ code, and then returns the results as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`evalBuf`</ph>– X++ コードの入力文字列を評価し、結果を文字列として返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><ph id="ph1">`literalStr`</ph> – retrieves a label ID when given the string representation of a label, such as the string <ph id="ph2">`"@SYS12345"`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`literalStr`</ph> – は、文字列 <ph id="ph2">`"@SYS12345"`</ph> などのラベルの文字列表示が与えられたときにラベル ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For example, <ph id="ph1">`myLabel.exists(literalStr("@SYS12345"));`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">`myLabel.exists(literalStr("@SYS12345"));`</ph>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メモ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>X++ compile time functions cannot be called from a .NET program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Functions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>attributeStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">attributeStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Validates that the specified attribute class exists in the Application Explorer; if not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The name of the attribute to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する属性の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The name of the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>classNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">classNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Retrieves the ID of the specified class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたクラスの ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The class for which to retrieve the ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ID を取得するクラス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The ID of the specified class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたクラスの ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>classStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">classStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Retrieves the name of a class as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列としてクラスの名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The name of the class to return.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返すクラスの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The name of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Use this function instead of literal text to retrieve a string that contains the class name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>If the class does not exist, the function generates a syntax error at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>configurationKeyNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">configurationKeyNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Retrieves the ID of the specified configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたコンフィギュレーション キーの ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>keyname</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">keyname</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The configuration key for which to return the ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ID を返すコンフィギュレーション キー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The ID of the specified configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたコンフィギュレーション キーの ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>configurationKeyStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">configurationKeyStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Retrieves the name of a configuration key as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列としてコンフィギュレーション キーの名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>keyname</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">keyname</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The name of the configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The name of the configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Use this function instead of literal text to retrieve a string that contains the configuration key name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>If the key does not exist, the function generates a syntax error at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>dataEntityDataSourceStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataEntityDataSourceStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Retrieves the name of a data source of a data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのデータ ソースの名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>dataEntity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataEntity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The name of the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>dataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The name of the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The name of the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>delegateStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">delegateStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Returns the name of the delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任の名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The name of the class, table, or form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス、テーブル、またはフォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>instanceDelegate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">instanceDelegate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The name of the instance delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス デリゲートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The name of the delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任の名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>dimensionHierarchyLevelStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimensionHierarchyLevelStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Returns the name of the dimension hierarchy level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード階層レベルの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>dimensionHierarchyLevel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimensionHierarchyLevel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The name of the dimension hierarchy level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード階層レベルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The name of the dimension hierarchy level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード階層レベルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>dimensionHierarchyStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimensionHierarchyStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Returns the name of the dimension hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード階層の名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>dimensionHierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimensionHierarchy</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>The name of the dimension hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード階層の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>The name of the dimension hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード階層の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>dimensionReferenceStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimensionReferenceStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Returns the name of the dimension reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード参照の名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>dimensionReference</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimensionReference</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>The name of the dimension reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード参照の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The name of the dimension reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード参照の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>dutyStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dutyStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Retrieves a string that represents the name of the specified security duty.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したセキュリティ職務権限の名前を表す文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>securityDuty</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">securityDuty</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The name of the security duty.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ職務権限の名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The name of the security duty in a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列のセキュリティ職務の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>enumCnt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">enumCnt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Retrieves the number of elements in the specified enumeration type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された列挙型の要素数を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>enumtype</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">enumtype</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The enumeration type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型タイプ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The number of elements in the specified enumeration type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された列挙型の要素数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>enumLiteralStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">enumLiteralStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Indicates whether the specified string is an element of the specified enumeration type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した文字列が指定した列挙型の要素であるかどうかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>The enumeration type from which to retrieve the specified value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された値を取得する列挙型。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>The value of the <bpt id="p1">*</bpt>str<ept id="p1">*</ept> parameter if the specified string was found; otherwise, a compilation error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された文字列が見つかった場合の <bpt id="p1">*</bpt>str<ept id="p1">*</ept> パラメーターの値。それ以外の場合は、コンパイル エラーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>enumNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">enumNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Retrieves the ID of the specified enumeration type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された列挙型の ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>The enumeration for which to return the ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ID を返す列挙。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>The ID of the specified enumeration type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された列挙型の ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>enumStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">enumStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Retrieves the name of an enumeration as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列として列挙型の名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>The name of the enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>The name of the enumeration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>extendedTypeNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">extendedTypeNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Retrieves the ID of the specified extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された拡張データ型の ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>str</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">str</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The extended data type for which to return the ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ID を返す拡張データ型。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>The ID of the specified extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された拡張データ型の ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>extendedTypeStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">extendedTypeStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Retrieves the name of an extended data type as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列として拡張データ型の名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>str</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">str</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>The name of the extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>The name of the extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Use this function instead of literal text to return a string that contains the extended data type name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>If the data type does not exist, the <bpt id="p1">**</bpt>extendedTypeStr<ept id="p1">**</ept> function generates a syntax error at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ タイプが存在しない場合、<bpt id="p1">**</bpt>extendedTypeStr<ept id="p1">**</ept> 関数は、コンパイル時に、構文エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>fieldNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Returns the ID number of the specified field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したフィールドの ID 番号を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>tableName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>The name of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>fieldName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>The name of the field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>The ID of the specified field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたフィールドの ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>The following example prints the number of the <bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> field in the <bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> フィールドの番号を <bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> テーブルに出力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>fieldPName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldPName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Retrieves the label of the specified field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたフィールドのラベルを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>tableid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>The table that contains the specified field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたフィールドを含むテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>fieldid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>The field to convert.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換するフィールド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>The label of the field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドのラベル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>The following example prints the label of the <bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> フィールドのラベルを出力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>fieldStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Retrieves the field name of the specified field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したフィールドのフィールド名を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>tableid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>The table that contains the field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを含むテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>fieldid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>The field to convert.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換するフィールド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>The field name of the specified field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したフィールドのフィールド名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>The following example assigns the name of the <bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> field to the <bpt id="p2">*</bpt>myText<ept id="p2">*</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> フィールドの名前を <bpt id="p2">*</bpt>myText<ept id="p2">*</ept> 変数に割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>formControlStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formControlStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>Causes the X++ compiler to check whether the control exists on the form, and to replace the function call with a string of the valid control name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>formName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>The name of the form, not in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引用符ではなく、フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>controlName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">controlName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>The name of the control that is on the form, not in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム上のコントロールの名前で、引用符ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>A string that contains the name of the control as it appears in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>A compile error is issued if the compiler determines that the control does not exist on the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>If your X++ code uses a string that contains quotation marks to supply the control name, the error cannot be discovered until run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>Use of this function enables the compiler to discover the error earlier at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>X++ functions such as <bpt id="p1">**</bpt>formControlStr<ept id="p1">**</ept> that are executed by the compiler are called compile-time functions or compile-time functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラにより実行される <bpt id="p1">**</bpt>formControlStr<ept id="p1">**</ept> などの X++ 関数は、コンパイル時関数と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>That is why the input parameters are not standard strings in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>formDataFieldStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formDataFieldStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Returns the name of a data field in a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ フィールドの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>formName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>The name of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>dataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>The data source of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ ソース。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>dataField</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataField</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>The data field of the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースのデータ フィールド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>The name of a data field in a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ フィールドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>formDataSourceStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formDataSourceStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Returns the name of a data source in a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ ソースの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>formName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>The name of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>dataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>The data source of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ ソース。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>The name of a data source in a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ ソースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>formMethodStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formMethodStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>Returns the name of a method of a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのメソッドの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>formName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>The name of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>methodName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">methodName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>The method of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのメソッド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>The name of a method in a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのメソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>The following example prints the name of the <bpt id="p1">**</bpt>showDialog<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>showDialog<ept id="p1">**</ept> メソッドの名前を出力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>formStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">formStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>Retrieves the name of a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>The name of a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>A string that represents the name of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの名前を表す文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>The following example prints the name of the InventDim form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、InventDim フォームの名前を出力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>identifierStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">identifierStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>Converts the specified identifier to a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された識別子を文字列に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>ident</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ident</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>The identifier to convert.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換する ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>A string that represents the specified identifier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した ID を表す文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>You will receive a best practice warning if you use the <bpt id="p1">**</bpt>identifierStr<ept id="p1">**</ept> function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>identifierStr<ept id="p1">**</ept> 関数使用する場合、ベスト プラクティス警告が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>This occurs because existence checking is performed for <bpt id="p1">**</bpt>identifierStr<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、<bpt id="p1">**</bpt>identifierStr<ept id="p1">**</ept> に対して存在チェックが実行されたために発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>Try to use a more specific compile-time function if one is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用可能な場合は、より具体的なコンパイル時の関数を使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>For more information, <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>The following code example assigns the <bpt id="p1">*</bpt>myvar<ept id="p1">*</ept> variable name to the <bpt id="p2">*</bpt>thevar<ept id="p2">*</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、<bpt id="p1">*</bpt>myvar<ept id="p1">*</ept> 変数名を <bpt id="p2">*</bpt>thevar<ept id="p2">*</ept> 変数に割り当てています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>indexNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">indexNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>Converts the specified index to a number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたインデックスを数字に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>tableid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>The table that contains the index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド インデックスを含むテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>indexid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">indexid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>The index to convert.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換するインデックス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>The index number that represents the specified index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたインデックスを表すインデックス番号。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>The following example returns the index value of the Party index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、当事者インデックスのインデックス値を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>indexStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">indexStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Converts the specified index to a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたインデックスを文字列に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>tableid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>The table that contains the index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド インデックスを含むテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>indexid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">indexid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>The index to convert.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変換するインデックス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>A string that represents the specified index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定インデックスを表す文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>The following example assigns the <bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> index value to the <bpt id="p2">*</bpt>myText<ept id="p2">*</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>CashDisc<ept id="p1">**</ept> インデックス値を <bpt id="p2">*</bpt>myText<ept id="p2">*</ept> 変数に割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>licenseCodeNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">licenseCodeNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>codename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">codename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>The name of the license code to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するライセンス コードの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>The number of the specified license code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたライセンス コードの数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>licenseCodeStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">licenseCodeStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>codename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">codename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>The name of the license code to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するライセンス コードの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>The name of the specified license code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたライセンス コードの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>literalStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">literalStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>Validates that the specified string can be a literal string; if not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source>codename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">codename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>The string to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>The literal string if valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合は、リテラル文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source>maxDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">maxDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>Retrieves the maximum value allowed for a variable of type date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付型の変数に使用できる最大値を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source>The maximum value allowed for a variable of type <bpt id="p1">**</bpt>date<ept id="p1">**</ept>, which is <bpt id="p2">**</bpt>2154-12-31<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付<ept id="p1">**</ept> の変数に使用できる最大値は、<bpt id="p2">**</bpt>2154-12-31<ept id="p2">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source>maxInt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">maxInt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>Retrieves the maximum signed value that can be stored in an <bpt id="p1">**</bpt>int<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int<ept id="p1">**</ept> 型に格納可能な最大符号付き値を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>The maximum value allowed value of an integer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整数の許容値の最大値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source>Any other integer will be less than or equal to the returned value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の整数値は、戻り値以下になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>measurementStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">measurementStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source>Returns the name of a measurement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定の名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>measurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source>The name of the measurement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source>The name of the measurement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>measureStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">measureStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>Returns the name of a measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メジャーの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source>measure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source>The name of the measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>The name of the measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>menuItemActionStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">menuItemActionStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source>Validates that the specified menu item action exists in the Application Object Tree (Application Explorer); if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>codename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">codename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>The name of the menu item action to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するメニュー項目アクションの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source>The name of the menu item action, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、メニュー項目アクションの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source>menuItemDisplayStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">menuItemDisplayStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source>Validates that the specified menu item display exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="672">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="673">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="674">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="675">
          <source>codename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">codename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="676">
          <source>The name of the menu item display to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するメニュー項目nの表示の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="677">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="678">
          <source>The name of the specified menu item display, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定されたメニューの表示の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="679">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="680">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="681">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="682">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="683">
          <source>menuItemOutputStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">menuItemOutputStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="684">
          <source>Validates that the specified menu item output exists in the Application Explorer; if not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="685">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="686">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="687">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="688">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="689">
          <source>codename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">codename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="690">
          <source>The name of the menu item output to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するメニュー項目出力の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="691">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="692">
          <source>The specified menu item output if valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合、指定されたメニュー項目が出力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="693">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="694">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="695">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="696">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="697">
          <source>menuStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">menuStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="698">
          <source>Validates that the specified menu exists in the Application Explorer; if not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="699">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="700">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="701">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="702">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="703">
          <source>menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="704">
          <source>The name of the menu to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するメニューの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="705">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="706">
          <source>The name of the specified menu item if valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の指定されたメニュー項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="707">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="708">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="709">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="710">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="711">
          <source>methodStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">methodStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="712">
          <source>Validates that the specified method exists in the specified class; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="713">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="714">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="715">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="716">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="717">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="718">
          <source>The name of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="719">
          <source>method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="720">
          <source>The name of the method to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するメソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="721">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="722">
          <source>The name of the specified method, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定されたメソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="723">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="724">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="725">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="726">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="727">
          <source>minInt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">minInt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="728">
          <source>Retrieves the minimum signed value that can be stored in an <bpt id="p1">**</bpt>int<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int<ept id="p1">**</ept> 型に格納可能な最小符号付き値を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="729">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="730">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="731">
          <source>The minimum value of an <bpt id="p1">**</bpt>int<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>int<ept id="p1">**</ept> 型の最小値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="732">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="733">
          <source>Any other integer value will be greater than or equal to the returned value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の整数値は、戻り値以上になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="734">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="735">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="736">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="737">
          <source>privilegeStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">privilegeStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="738">
          <source>Returns the name of the privilege.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">権限の名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="739">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="740">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="741">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="742">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="743">
          <source>privilege</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">権限</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="744">
          <source>The privilege for which to return the name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を返す対象の特権。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="745">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="746">
          <source>The name of the privilege.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">権限の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="747">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="748">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="749">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="750">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="751">
          <source>queryDatasourceStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">queryDatasourceStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="752">
          <source>Causes the X++ compiler to check whether the data source exists on the query, and to replace the function call with a string of the valid data source name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="753">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="754">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="755">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="756">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="757">
          <source>queryName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">queryName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="758">
          <source>The name of the query, not in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引用符ではなく、クエリの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="759">
          <source>dataSourceName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataSourceName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="760">
          <source>The name of the data source that is on the query, not in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ上のデータ ソースの名前で、引用符ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="761">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="762">
          <source>A string that contains the name of the data source as it appears in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="763">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="764">
          <source>A compile error is issued if the compiler determines that the data source does not exist on the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="765">
          <source>If your X++ code uses a string that contains quotation marks to supply the data source name, the error cannot be discovered until run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="766">
          <source>Use of this function enables the compiler to discover the error earlier at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="767">
          <source>X++ functions such as <bpt id="p1">**</bpt>queryDataSourceStr<ept id="p1">**</ept> that are executed by the compiler are referred to as compile-time functions or compile-time functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラにより実行される <bpt id="p1">**</bpt>queryDataSourceStr<ept id="p1">**</ept> などの X++ 関数は、コンパイル時関数とみなされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="768">
          <source>That is why the input parameters are not standard strings in quotation marks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="769">
          <source>Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="770">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="771">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="772">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="773">
          <source>queryMethodStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">queryMethodStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="774">
          <source>Returns the name of a method of a query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリのメソッドの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="775">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="776">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="777">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="778">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="779">
          <source>queryName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">queryName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="780">
          <source>The name of the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="781">
          <source>methodName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">methodName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="782">
          <source>The method of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのメソッド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="783">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="784">
          <source>The name of a method in a query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリのメソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="785">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="786">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="787">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="788">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="789">
          <source>queryStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">queryStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="790">
          <source>Retrieves a string that represents an existing query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のクエリを表す文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="791">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="792">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="793">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="794">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="795">
          <source>query</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="796">
          <source>The query to retrieve.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">取得するクエリ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="797">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="798">
          <source>The name of the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="799">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="800">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="801">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="802">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="803">
          <source>reportStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">reportStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="804">
          <source>Retrieves a string that represents the name of the specified report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したレポートの名前を表す文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="805">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="806">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="807">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="808">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="809">
          <source>report</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="810">
          <source>The report for which to return the name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を返す対象のレポート。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="811">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="812">
          <source>The name of the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="813">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="814">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="815">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="816">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="817">
          <source>The following example assigns the name of the <bpt id="p1">**</bpt>AssetAddition<ept id="p1">**</ept> report to the <bpt id="p2">*</bpt>MyTxt<ept id="p2">*</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>AssetAddition<ept id="p1">**</ept> レポートの名前を <bpt id="p2">*</bpt>MyTxt<ept id="p2">*</ept> 変数に割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="818">
          <source>resourceStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">resourceStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="819">
          <source>Validates that the specified resource exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="820">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="821">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="822">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="823">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="824">
          <source>resourcename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">resourcename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="825">
          <source>The name of the resource to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するリソースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="826">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="827">
          <source>The name of the specified resource, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定されたリソースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="828">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="829">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="830">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="831">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="832">
          <source>roleStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">roleStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="833">
          <source>Retrieves a string that represents the name of the specified security role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したセキュリティ ロールの名前を表す文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="834">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="835">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="836">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="837">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="838">
          <source>securityRole</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">securityRole</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="839">
          <source>The name of the security role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ ロールの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="840">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="841">
          <source>The name of the security role in a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列のセキュリティ ロールの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="842">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="843">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="844">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="845">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="846">
          <source>ssrsReportStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ssrsReportStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="847">
          <source>Retrieves a string that represents the name of the specified report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したレポートの名前を表す文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="848">
          <source>Use this function when you want to specify the report that should be run by a report controller class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="849">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="850">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="851">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="852">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="853">
          <source>report</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="854">
          <source>The report to return the name for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を返す対象のレポート。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="855">
          <source>design</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">design</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="856">
          <source>The name of the design that is associated with the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートに関連付けられているデザインの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="857">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="858">
          <source>The name of the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="859">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="860">
          <source>The <bpt id="p1">**</bpt>ssrsReportStr<ept id="p1">**</ept> function parses the two values that are passed to it, to validate whether they belong to a valid report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ssrsReportStr<ept id="p1">**</ept> 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="861">
          <source>The report name must be set when a menu item points to a controller(), so that the controller can determine which report-design combination must be invoked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="862">
          <source>Use of the <bpt id="p1">**</bpt>ssrsReportStr<ept id="p1">**</ept> function provides the benefit of compile-time validation for the report and design name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ssrsReportStr<ept id="p1">**</ept> 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="863">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="864">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="865">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="866">
          <source>staticDelegateStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">staticDelegateStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="867">
          <source>Returns the name of a static delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的デリゲートの名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="868">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="869">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="870">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="871">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="872">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="873">
          <source>The name of a class, table, or form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス、テーブル、またはフォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="874">
          <source>delegate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="875">
          <source>The name of the delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任の名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="876">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="877">
          <source>The name of the delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任の名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="878">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="879">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="880">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="881">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="882">
          <source>staticMethodStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">staticMethodStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="883">
          <source>Validates that the specified static method exists in the specified class; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="884">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="885">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="886">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="887">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="888">
          <source>class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="889">
          <source>The name of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="890">
          <source>method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="891">
          <source>The name of the static method to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する静的メソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="892">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="893">
          <source>The name of the static method, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された静的メソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="894">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="895">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="896">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="897">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="898">
          <source>tableCollectionStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableCollectionStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="899">
          <source>Validates that the specified table collection exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="900">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="901">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="902">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="903">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="904">
          <source>tablecollection</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tablecollection</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="905">
          <source>The name of the table collection to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するテーブル コレクションの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="906">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="907">
          <source>The name of the specified table collection, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定されたテーブル コレクションの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="908">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="909">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="910">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="911">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="912">
          <source>tableFieldGroupStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableFieldGroupStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="913">
          <source>Retrieves the name of a field group as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列としてフィールド グループの名前を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="914">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="915">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="916">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="917">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="918">
          <source>tableName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="919">
          <source>The table that contains the field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド グループを含むテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="920">
          <source>fieldGroupName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldGroupName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="921">
          <source>The field group in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル内のフィールド グループ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="922">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="923">
          <source>The name of the field group as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列としてのフィールド グループの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="924">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="925">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="926">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="927">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="928">
          <source>The following example retrieves the name of the <bpt id="p1">**</bpt>Editing<ept id="p1">**</ept> field group as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept> フィールド グループの名前を文字列として取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="929">
          <source>tableMethodStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableMethodStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="930">
          <source>Validates that the specified method exists in the specified table; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="931">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="932">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="933">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="934">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="935">
          <source>table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="936">
          <source>The name of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="937">
          <source>method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="938">
          <source>The name of the method to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するメソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="939">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="940">
          <source>The name of the method, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、メソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="941">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="942">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="943">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="944">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="945">
          <source>tableNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="946">
          <source>Retrieves the table ID of the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のテーブルのテーブル ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="947">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="948">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="949">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="950">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="951">
          <source>table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="952">
          <source>The table to retrieve the table ID for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル ID を取得するテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="953">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="954">
          <source>The table ID of the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のテーブルのテーブル ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="955">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="956">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="957">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="958">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="959">
          <source>The following example sets the <bpt id="p1">**</bpt>tableID<ept id="p1">**</ept> variable to 77, which is the <bpt id="p2">**</bpt>ID<ept id="p2">**</ept> of the <bpt id="p3">**</bpt>CustTable<ept id="p3">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>tableID<ept id="p1">**</ept> 変数を 77 に設定します。これは、<bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> テーブルの <bpt id="p3">**</bpt>ID<ept id="p3">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="960">
          <source>tablePName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tablePName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="961">
          <source>Retrieves a string that contains the printable name of the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたテーブルの出力可能な名前を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="962">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="963">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="964">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="965">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="966">
          <source>table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="967">
          <source>The table to retrieve the printable name for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">印刷可能な名前を取得するテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="968">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="969">
          <source>The name of the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたテーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="970">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="971">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="972">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="973">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="974">
          <source>The following example assigns the label of the <bpt id="p1">**</bpt>CustTable<ept id="p1">**</ept> table to the <bpt id="p2">*</bpt>MyText<ept id="p2">*</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>CustTable<ept id="p1">**</ept> テーブルのラベルを <bpt id="p2">*</bpt>MyText<ept id="p2">*</ept> 変数に割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="975">
          <source>tableStaticMethodStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableStaticMethodStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="976">
          <source>Validates that the specified static method exists in the specified table; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="977">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="978">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="979">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="980">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="981">
          <source>table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="982">
          <source>The name of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="983">
          <source>method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="984">
          <source>The name of the static method to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する静的メソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="985">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="986">
          <source>The name of the specified static method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された静的メソッドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="987">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="988">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="989">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="990">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="991">
          <source>tableStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="992">
          <source>Retrieves a string that contains the name the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したテーブルの名前を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="993">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="994">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="995">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="996">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="997">
          <source>table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="998">
          <source>The table to retrieve a string for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列を取得するテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="999">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1000">
          <source>A string value that contains the name of the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したテーブルの名前を含む文字列値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1001">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1002">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1003">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1004">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1005">
          <source>The following example assigns the name of the <bpt id="p1">**</bpt>CustTable<ept id="p1">**</ept> table to the <bpt id="p2">*</bpt>MyTxt<ept id="p2">*</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>CustTable<ept id="p1">**</ept> テーブルの名前を <bpt id="p2">*</bpt>MyTxt<ept id="p2">*</ept> 変数に割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1006">
          <source>tileStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tileStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1007">
          <source>Retrieves a string that represents the name of the specified tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したタイルの名前を表す文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1008">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1009">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1010">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1011">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1012">
          <source>tile</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tile</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1013">
          <source>The name of the tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1014">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1015">
          <source>The name of the tile in a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列のタイルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1016">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1017">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1018">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1019">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1020">
          <source>varStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">varStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1021">
          <source>Retrieves a string that contains the name of the specified variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した変数の名前を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1022">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1023">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1024">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1025">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1026">
          <source>var</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">var</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1027">
          <source>The name of the variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変数の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1028">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1029">
          <source>A string that contains the name of the specified variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した変数の名前を含む文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1030">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1031">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1032">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1033">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1034">
          <source>webActionItemStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webActionItemStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1035">
          <source>Validates that the specified web action item exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1036">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1037">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1038">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1039">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1040">
          <source>webactionitem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webactionitem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1041">
          <source>The name of the web action item to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web アクション項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1042">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1043">
          <source>The name of the specified web action item, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web アクション項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1044">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1045">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1046">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1047">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1048">
          <source>webDisplayContentItemStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webDisplayContentItemStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1049">
          <source>Validates that the specified web display content item exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1050">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1051">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1052">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1053">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1054">
          <source>webdisplaycontentitem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webdisplaycontentitem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1055">
          <source>The name of the web display content item to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web 表示コンテンツ項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1056">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1057">
          <source>The name of the specified web display content item, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web 表示コンテンツ項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1058">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1059">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1060">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1061">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1062">
          <source>webFormStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webFormStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1063">
          <source>Validates that the specified web form exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1064">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1065">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1066">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1067">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1068">
          <source>name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1069">
          <source>The name of the web form to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1070">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1071">
          <source>The name of the specified web form, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web フォームの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1072">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1073">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1074">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1075">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1076">
          <source>webletItemStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webletItemStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1077">
          <source>Validates that the specified weblet item exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1078">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1079">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1080">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1081">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1082">
          <source>webletitem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webletitem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1083">
          <source>The name of the weblet item to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Weblet 項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1084">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1085">
          <source>The name of the specified weblet item, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Weblet 項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1086">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1087">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1088">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1089">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1090">
          <source>webMenuStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webMenuStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1091">
          <source>Validates that the specified web menu exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1092">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1093">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1094">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1095">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1096">
          <source>name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1097">
          <source>The name of the web menu to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web メニューの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1098">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1099">
          <source>The name of the specified web menu, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web メニューの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1100">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1101">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1102">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1103">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1104">
          <source>webOutputContentItemStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webOutputContentItemStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1105">
          <source>Validates that the specified web output content item exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1106">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1107">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1108">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1109">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1110">
          <source>weboutputcontentitem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">weboutputcontentitem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1111">
          <source>The name of the web output content item to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web 出力コンテンツ項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1112">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1113">
          <source>The name of the specified web output content item, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web 出力コンテンツ項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1114">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1115">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1116">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1117">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1118">
          <source>webpageDefStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webpageDefStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1119">
          <source>Validates that the specified Web page definition exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1120">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1121">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1122">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1123">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1124">
          <source>pagename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pagename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1125">
          <source>The name of the Web page definition to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web ページ定義の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1126">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1127">
          <source>The name of the specified web-page definition, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web ページ定義の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1128">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1129">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1130">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1131">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1132">
          <source>webReportStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webReportStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1133">
          <source>Validates that the specified web report exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1134">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1135">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1136">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1137">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1138">
          <source>name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1139">
          <source>The name of the web report to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web レポートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1140">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1141">
          <source>The name of the specified web report, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web レポートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1142">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1143">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1144">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1145">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1146">
          <source>websiteDefStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">websiteDefStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1147">
          <source>Validates that the specified web-site definition exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1148">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1149">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1150">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1151">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1152">
          <source>resourcename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">resourcename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1153">
          <source>The name of the Web site definition to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web サイト定義の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1154">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1155">
          <source>The name of the specified web-site definition, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web サイト定義の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1156">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1157">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1158">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1159">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1160">
          <source>webSiteTempStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webSiteTempStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1161">
          <source>Validates that the specified web-site template exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1162">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1163">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1164">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1165">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1166">
          <source>resourcename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">resourcename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1167">
          <source>The name of the Web site template to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web サイト テンプレートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1168">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1169">
          <source>The name of the specified web-site template, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web テンプレートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1170">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1171">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1172">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1173">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1174">
          <source>webStaticFileStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webStaticFileStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1175">
          <source>Validates that the specified web static file exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1176">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1177">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1178">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1179">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1180">
          <source>pagename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pagename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1181">
          <source>The name of the web static file to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web 静的ファイル テンプレートの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1182">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1183">
          <source>The name of the specified web static file, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web 静的ファイルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1184">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1185">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1186">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1187">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1188">
          <source>webUrlItemStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webUrlItemStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1189">
          <source>Validates that the specified web URL item exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1190">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1191">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1192">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1193">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1194">
          <source>weburlitem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">weburlitem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1195">
          <source>The name of the web URL item to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web URL 項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1196">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1197">
          <source>The name of the specified web URL item, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web URL 項目の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1198">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1199">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1200">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1201">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1202">
          <source>webWebPartStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">webWebPartStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1203">
          <source>Validates that the specified web part exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1204">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1205">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1206">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1207">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1208">
          <source>resourcename</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">resourcename</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1209">
          <source>The name of the web part to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証する Web パーツの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1210">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1211">
          <source>The name of the specified web part, if it is valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な場合の、指定された Web パーツの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1212">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1213">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1214">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1215">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1216">
          <source>workflowApprovalStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">workflowApprovalStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1217">
          <source>Retrieves the name of a workflow approval in the Application Object Tree (Application Explorer) as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1218">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1219">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1220">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1221">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1222">
          <source>approval</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">承認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1223">
          <source>The Application Explorer name of the workflow approval.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローの承認のアプリケーション エクスプローラーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1224">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1225">
          <source>A string that represents the Application Explorer name of the workflow approval.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1226">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1227">
          <source>Use this function instead of literal text to retrieve a string that contains the workflow approval name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1228">
          <source>If the workflow approval does not exist, the function generates a syntax error at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1229">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1230">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1231">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1232">
          <source>The following code example sets the variable <bpt id="p1">*</bpt>str s<ept id="p1">*</ept> to <bpt id="p2">**</bpt>MyWorkflowApproval<ept id="p2">**</ept> which is the name of the workflow approval in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、変数 <bpt id="p1">*</bpt>str s<ept id="p1">*</ept> を <bpt id="p2">**</bpt>MyWorkflowApproval<ept id="p2">**</ept> に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1233">
          <source>workflowCategoryStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">workflowCategoryStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1234">
          <source>Retrieves the name of a workflow category in the Application Object Tree (Application Explorer) as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1235">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1236">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1237">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1238">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1239">
          <source>category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1240">
          <source>The Application Explorer name of the workflow category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1241">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1242">
          <source>A string that represents the Application Explorer name of the workflow category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1243">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1244">
          <source>Use this function instead of literal text to retrieve a string that contains the workflow category name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1245">
          <source>If the workflow category does not exist, the function generates a syntax error at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1246">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1247">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1248">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1249">
          <source>The following code example sets the variable <bpt id="p1">*</bpt>str s<ept id="p1">*</ept> to <bpt id="p2">**</bpt>MyWorkflowCategory<ept id="p2">**</ept> which is the name of the workflow category in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、変数 <bpt id="p1">*</bpt>str s<ept id="p1">*</ept> を <bpt id="p2">**</bpt>MyWorkflowCategory<ept id="p2">**</ept> に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1250">
          <source>workflowTaskStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">workflowTaskStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1251">
          <source>Retrieves the name of a workflow task in the Application Object Tree (Application Explorer) as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1252">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1253">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1254">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1255">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1256">
          <source>task</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1257">
          <source>The Application Explorer name of the workflow task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー タスクのアプリケーション エクスプローラーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1258">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1259">
          <source>A string that represents the Application Explorer name of the workflow task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1260">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1261">
          <source>Use this function instead of literal text to retrieve a string that contains the workflow task name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1262">
          <source>If the workflow task does not exist, the function generates a syntax error at compile time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1263">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1264">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1265">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1266">
          <source>The following code example sets the variable <bpt id="p1">*</bpt>str s<ept id="p1">*</ept> to <bpt id="p2">**</bpt>MyWorkflowTask<ept id="p2">**</ept> which is the name of the workflow task in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、変数 <bpt id="p1">*</bpt>str s<ept id="p1">*</ept> を <bpt id="p2">**</bpt>MyWorkflowTask<ept id="p2">**</ept> に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1267">
          <source>workflowTypeStr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">workflowTypeStr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1268">
          <source>Validates that the specified workflow type exists in the Application Explorer; if it does not, a compiler error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1269">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1270">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1271">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1272">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1273">
          <source>workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1274">
          <source>The name of the workflow type to validate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証するワークフロー タイプの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1275">
          <source>Return Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1276">
          <source>The name of the workflow type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー タイプの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1277">
          <source>Remarks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">備考</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1278">
          <source>This is a compile-time function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、コンパイル時関数です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1279">
          <source>For more information, see <bpt id="p1">[</bpt>Overview<ept id="p1">](#overview)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>概要<ept id="p1">](#overview)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1280">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>