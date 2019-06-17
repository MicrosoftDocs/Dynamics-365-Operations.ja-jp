<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="add-enum-value.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>add-enum-value.c2d3de.d59e20efdc6da946f71c131bcf40e9d9cdb61edd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d59e20efdc6da946f71c131bcf40e9d9cdb61edd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\add-enum-value.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add values to enums through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して列挙体に値を追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to add new values to an enum by extending the enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、列挙型を拡張することによって列挙型に新しい値を追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add values to enums through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して列挙体に値を追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>To add new values to an enum, you should extend the enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい値を列挙型に追加するには、列挙型を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Any enum that is marked as <bpt id="p1">**</bpt>Extensible<ept id="p1">**</ept> (<bpt id="p2">**</bpt>IsExtensible = true<ept id="p2">**</ept>) can be extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張可能<ept id="p1">**</ept> (<bpt id="p2">**</bpt>IsExtensible = true<ept id="p2">**</ept>) としてマークされている列挙は拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can find the extensibility information in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window in Microsoft Visual Studio, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の情報は、次の図に示すように、Microsoft Visual Studio の <bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Extensible enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能な列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>When enum values of extensible enums are synchronized, the integer values of the baseline enum are deterministic, whereas the integer values of the extension enum values are non-deterministic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能な列挙の列挙値が同期されると、拡張可能な列挙の値が non-deterministic であるのに対して、ベースライン列挙の整数値は deterministic です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The values are generated during synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は、同期時に生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Therefore, you can't have logic that depends on the integer value of the enum values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、列挙値の整数値に依存する X++ ロジックを持つことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Here are some examples:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつか例を挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Range comparisons, such as <ph id="ph1">`&lt;`</ph>, <ph id="ph2">`&gt;`</ph>, and <ph id="ph3">`..`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`&lt;`</ph>、<ph id="ph2">`&gt;`</ph>、<ph id="ph3">`..`</ph> などの範囲比較</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Modeled ranges in views and queries</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビューおよびクエリのモデル化された範囲</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Query ranges that are created from code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードから作成されたクエリの範囲</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Usually, an extended enum must have its own implementation wherever it's used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、拡張された列挙型は、それが使用される場所で独自の実装を必要とします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Look for all uses of the enum, and uptake the implementation where it's required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙のすべての使用を確認して、必要な場合に実装を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Here are some significant places to look for:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索するいくつかの重要な場所を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Switch blocks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブロックの切り替え:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If the switch block doesn't have a default case block or a default case block that doesn't throw an exception, handle the extended enum value by subscribing to a delegate, if a delegate is provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Switch ブロックに、既定の case ブロックまたは例外が発生しない既定のケース ブロックがない場合、デリゲートが指定されている場合、デリゲートを購読することにより拡張の列挙値を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Otherwise, add a post-event handler to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、メソッドにポストイベント ハンドラーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If the enum is used in a switch that has a default case block that throws an exception, contact Microsoft to request a delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型に例外をスローする既定のケース ブロックを持つスイッチが使用されている場合、Microsoft に問い合わせ、デリゲートを要求します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>If the enum has an associated class hierarchy that handles the enum, create a subclass for the extended enum–specific implementation, and uptake the construct on the base class as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型に、列挙型を処理する関連付けられたクラス階層がある場合は、列挙型固有の実装に対してサブクラスを作成し、必要に応じて基本クラスにコンストラクターを取り込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For more information, see <bpt id="p1">[</bpt>Register a subclass for factory methods<ept id="p1">](register-subclass-factory-methods.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>ファクトリ メソッドのサブクラスの登録<ept id="p1">](register-subclass-factory-methods.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Extend an enum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>There are two ways to extend an enum:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型を拡張するには 2 つの方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create a project that has a model reference where you want the new enum extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい列挙拡張子を使用するモデル参照を持つプロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Right-click the enum to extend, and then select <bpt id="p1">**</bpt>Create extension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張する列挙値を右クリックし、<bpt id="p1">**</bpt>拡張を作成<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Create an extension enum (method 1)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張列挙を作成する (方法1)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Right-click the enum to extend, and then select <bpt id="p1">**</bpt>Create extension in new project<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張する列挙値を右クリックし、<bpt id="p1">**</bpt>新しいプロジェクトで拡張を作成<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>You're prompted to select the model that the extension enum should be created in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張列挙を作成する必要のあるモデルを選択するように求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Create an extension enum (method 2)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張列挙を作成する (方法2)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The enum extension is created in the selected model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択されたモデルで列挙型拡張が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You can add new enum values to this extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい列挙値をこの拡張に追加することができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>