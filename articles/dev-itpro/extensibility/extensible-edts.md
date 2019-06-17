<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-edts.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-edts.70aceb.6f9b02081fdfdead8b9c26e43992fcbd4bc5b7d4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6f9b02081fdfdead8b9c26e43992fcbd4bc5b7d4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extensible-edts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extended data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about extended data types (EDTs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張データ型 (EDT) について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extended data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Extended data types (EDTs) have a rich extension model that lets extenders change specific behaviors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 (EDT) には、拡張担当者が特定の動作を変更できる豊富な拡張モデルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To provide an extensible solution, keep the following guidelines in mind when you work with EDTs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なソリューションを提供するには、EDT を操作する際に次のガイドラインに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Label/Help text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル/ヘルプ テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Labels and Help text properties can be changed by an extension, but only one value can remain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルおよびヘルプ テキストのプロパティは、拡張によって変更できますが、値は 1 つだけ残すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If multiple solutions change the label of the same EDT, the various labels are, in functional terms, mutually exclusive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のソリューションで同じ EDT のラベルが変更される場合、機能の観点でさまざまなラベルが相互に排他的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Therefore, those labels can't all be installed on the same system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、それらのラベルをすべて同じシステムにインストールすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>String size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列サイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>String size can be defined only on root EDTs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列サイズは、ルート EDT でのみ定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The system will use the largest value that is defined across the EDT and its extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT とその拡張の間で定義されている最大値が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For derived EDTs, string size can't be changed by an extension, because the IS-A relationship between the EDTs will be broken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">派生 EDT の場合、EDT 間の IS-A 関係が壊れるため、文字列サイズを拡張によって変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Assignments to string EDTs will truncate the string to match the defined string size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列 EDT への割り当てでは、定義されている文字列のサイズを照合するために文字列が切り捨てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Extends</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The <bpt id="p1">**</bpt>extends<ept id="p1">**</ept> property can't be changed by an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張によって<bpt id="p1">**</bpt>拡張<ept id="p1">**</ept>プロパティを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Any change that is made to this property after release will cause a breaking change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリース後にこのプロパティに対して行った変更はすべて、重大な変更を引き起こします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Therefore, you must make sure that the property is set correctly before release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、リリース前に、プロパティが正しく設定されていることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If you set this property, neither you nor extenders will be able to make changes to the string size later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを設定した場合、自分も拡張担当者も後での文字列サイズを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Avoid unnecessary dependencies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">不要な依存関係を回避してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For example, don't extend generic EDTs such as Name and Description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、名前や説明などの一般的な EDT を拡張しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Number of decimals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小数点以下の桁数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The <bpt id="p1">**</bpt>Number of decimals<ept id="p1">**</ept> property can't be changed by an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張によって<bpt id="p1">**</bpt>拡張によって<ept id="p1">**</ept>プロパティを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>If you set this property to <bpt id="p1">**</bpt>True<ept id="p1">**</ept>, extenders can change the number of decimal places.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを <bpt id="p1">**</bpt>True<ept id="p1">**</ept> に設定した場合、拡張担当者は小数点以下桁数を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>If you set this property to <bpt id="p1">**</bpt>True<ept id="p1">**</ept>, make sure that the following conditions are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを <bpt id="p1">**</bpt>True<ept id="p1">**</ept> に設定した場合、以下の条件を満たすことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>All truncation logic honors the number of decimal places that is specified on the EDT, so that no implicit or hardcoded rounding will occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗黙的またはハードコードされた四捨五入が発生しないように、すべての切り捨てロジックでは、EDT で指定されている小数点以下の桁数が受け入れられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The value isn't assigned to other incompatible EDTs that don't correctly handle rounding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この値は、四捨五入が正しく処理されないその他の互換性のない EDT には割り当てられません。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>