<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="general-electronic-reporting-formulas-list-extension.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>general-electronic-reporting-formulas-list-extension.43a1cc.4d5e5dda02237dde0c3a5543ff3e0f3f7cb64b24.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4d5e5dda02237dde0c3a5543ff3e0f3f7cb64b24</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\general-electronic-reporting-formulas-list-extension.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend the list of Electronic reporting (ER) functions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告 (ER) 関数の一覧の拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Various types of functions are supported in Electronic reporting expressions for data transformation - text, date and time, mathematical logical, information, data type conversion, and other (business domain–specific functions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数がデータ変換のための電子報告式でサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>In addition to built-in functions, Electronic reporting lets you extend the list of available functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組み込み関数に加えて、電子申告により使用可能な関数の一覧を拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104" restype="x-metadata">
          <source>This article includes an overview of key tasks that you must complete to introduce a new function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、新しい機能を導入するために完了しなければならない重要なタスクの概要について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Extend the list of Electronic reporting (ER) functions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告 (ER) 関数の一覧の拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Various types of functions are supported in Electronic reporting expressions for data transformation – text, date and time, mathematical logical, information, data type conversion, and other (business domain–specific functions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数がデータ変換のための電子報告式でサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In addition to built-in functions, Electronic reporting lets you extend the list of available functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組み込み関数に加えて、電子申告により使用可能な関数の一覧を拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This article includes an overview of key tasks that you must complete to introduce a new function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、新しい機能を導入するために完了しなければならない重要なタスクの概要について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>All Electronic reporting functions in Microsoft Dynamics 365 for Finance and Operations code are represented as classes that extend the <bpt id="p1">**</bpt>ERExpression<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations コードのすべての電子レポート機能は、<bpt id="p1">**</bpt>ERExpression<ept id="p1">**</ept> クラスを拡張するクラスとして表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Two types of functions are recognized:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 種類の関数が認識されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>Fixed number of arguments<ept id="p1">**</ept> – These functions are represented by classes that include methods that have the prefix <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> (see <bpt id="p3">**</bpt>parmInput<ept id="p3">**</ept>, <bpt id="p4">**</bpt>parmStartNum<ept id="p4">**</ept> in the sample code the follows).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引数の数を固定<ept id="p1">**</ept> – これらの関数は、接頭語 <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> (次のサンプルコードの <bpt id="p3">**</bpt>parmInput<ept id="p3">**</ept>、<bpt id="p4">**</bpt>parmStartNum<ept id="p4">**</ept>を参照してください) を持つメソッドを含むクラスで表されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The order of arguments is set by the <bpt id="p1">**</bpt>SysOperationDisplayOrderAttribute<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引数の順序は、<bpt id="p1">**</bpt>SysOperationDisplayOrderAttribute<ept id="p1">**</ept> 属性によって設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Variable number of arguments<ept id="p1">**</ept> – These functions (see the <bpt id="p2">**</bpt>ERExpressionGenericCase<ept id="p2">**</ept> class) are represented by classes that implement the <bpt id="p3">**</bpt>ERIObjectContainer<ept id="p3">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>可変数の引数<ept id="p1">**</ept> – これらの機能は (<bpt id="p2">**</bpt>ERExpressionGenericCase<ept id="p2">**</ept> クラスを参照してください)<bpt id="p3">**</bpt>ERIObjectContainer<ept id="p3">**</ept> インターフェイスを実装するクラスで表されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>An additional <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> method is used to declare the types that a function accepts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>メソッドを使用して関数を受け入れる型を宣言します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Here are the recommended steps for introducing a new function for Electronic reporting expressions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告式の新しい機能を導入するのに推奨されている手順を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Select a base class for your function, based on the return value type (see <bpt id="p1">**</bpt>ERExpressionString<ept id="p1">**</ept> in the sample code that follows).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値の型に基づいて関数の基本クラスを選択します (以下のサンプル コードで <bpt id="p1">**</bpt>ERExpressionString<ept id="p1">**</ept> を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Create a new class that extends the selected class (see <bpt id="p1">**</bpt>ERExpressionStringMid<ept id="p1">**</ept> in the sample code the follows).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したクラスを拡張する新しいクラスを作成します (サンプル コードの <bpt id="p1">**</bpt>ERExpressionStringMid<ept id="p1">**</ept> を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Provide required attributes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須属性を提供:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>SysOperationLabelAttribute<ept id="p1">**</ept> – This attribute defines the function’s name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysOperationLabelAttribute<ept id="p1">**</ept> – この属性は、関数の名前を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>SysOperationHelpTextAttribute<ept id="p1">**</ept> – This attribute defines the function’s Help text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysOperationHelpTextAttribute<ept id="p1">**</ept> – この属性は、関数のヘルプ テキストを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>ERComponentGroupAttribute<ept id="p1">**</ept> – This attribute defines the group that the function belongs to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ERComponentGroupAttribute<ept id="p1">**</ept> - この属性は、この機能が属するグループを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>(For more information, see <bpt id="p1">[</bpt>Formula designer in Electronic reporting<ept id="p1">](general-electronic-reporting-formula-designer.md)</ept>.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(詳細については、「<bpt id="p1">[</bpt>電子申告のフォーミュラ デザイナー<ept id="p1">](general-electronic-reporting-formula-designer.md)</ept>」を参照してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Provide arguments:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引数を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>For a fixed number of arguments function, provide methods that have the prefix <bpt id="p1">**</bpt>parm<ept id="p1">**</ept>, and use the <bpt id="p2">**</bpt>SysOperationDisplayOrderAttribute<ept id="p2">**</ept> attribute to set the order of the arguments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引数関数の固定番号については、接頭語 <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> を持つメソッドを提供し、<bpt id="p2">**</bpt>SysOperationDisplayOrderAttribute<ept id="p2">**</ept> 属性を使用して引数の順序を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For a variable number of argument function, implement the <bpt id="p1">**</bpt>ERIObjectContainer<ept id="p1">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引数関数の変数番号で、<bpt id="p1">**</bpt>ERIObjectContainer<ept id="p1">**</ept> インターフェイスを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Provide an evaluation method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価方法を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Suggested guidance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推奨されるガイダンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The following guidance is intended to help you design your custom Electronic reporting functions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のガイダンスは、カスタム電子申告機能の設計を支援することを目的としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Reuse the names of Microsoft Excel functions whenever you can, so that Electronic reporting formulas remain Excel-like.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子レポート式が Excel と同じようにされるため、可能な限り Microsoft Excel の関数名を再利用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>In this way, you will keep Electronic reporting formulas intelligible for end users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、電子申告のフォーミュラをエンド ユーザーにわかりやすく保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Electronic reporting doesn't support list types for primitive data types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告では、プリミティブ データ型のリスト タイプがサポートされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Therefore, we have decided to use a data container list that has a single <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> item in it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、単一の <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> 項目を持つデータ コンテナー リストを使用することに決めました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Release a new function's list extension as a new Finance and Operations hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい関数の一覧の拡張機能を新しい Finance and Operations の修正プログラムとしてリリースします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Electronic reporting designers will refer to the hotfix number in Electronic reporting configurations that use that new custom function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告デザイナーは、新しいユーザー定義関数を使用する電子申告 コンフィギュレーションの修正プログラム番号を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Whenever a configuration of this type is imported into a new instance of Finance and Operations, Electronic reporting will evaluate whether the required hotfix has been installed, to maintain compliance between the Electronic reporting configuration and the Finance and Operations version that configuration is imported into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプの構成が Finance and Operations の新しいインスタンスにインポートされるときはいつでも、必要な修正プログラムがインストールされたかどうかが電子申告によって評価されて、電子申告構成と、構成がインポートされる Finance and Operations のバージョンとの間のコンプライアンスを維持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt>Electronic reporting overview<ept id="p1">](general-electronic-reporting.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>電子申告の概要<ept id="p1">](general-electronic-reporting.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">[</bpt>Formula designer in Electronic reporting<ept id="p1">](general-electronic-reporting-formula-designer.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>電子申告のフォーミュラ デザイナー<ept id="p1">](general-electronic-reporting-formula-designer.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>