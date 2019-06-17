<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extend-number-sequence-scope.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extend-number-sequence-scope.cfdba8.f05c40e5b8e22d295e1c49ee608f92458f4823b6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f05c40e5b8e22d295e1c49ee608f92458f4823b6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extend-number-sequence-scope.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend the scope of number sequences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序スコープの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how developers can extend number sequence scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、開発者が番号シーケンスのスコープを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend the scope of number sequences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">番号順序スコープの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic shows you how to extend the number sequence scope.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、数値シーケンスのスコープを拡張する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The scope of a number sequence defines which organization uses the number sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数字シーケンスの範囲は、数字シーケンスを使用する組織を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The scope can be <bpt id="p1">**</bpt>Shared<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Company<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Legal entity<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>Operating unit<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">範囲は、<bpt id="p1">**</bpt>共有<ept id="p1">**</ept>、<bpt id="p2">**</bpt>会社<ept id="p2">**</ept>、<bpt id="p3">**</bpt>法人<ept id="p3">**</ept>、または<bpt id="p4">**</bpt>作業単位<ept id="p4">**</ept>のいずれかにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Legal entity<ept id="p2">**</ept> scopes can be combined with fiscal calendar periods to create even more specific number sequences.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>会社<ept id="p1">**</ept>と<bpt id="p2">**</bpt>法人<ept id="p2">**</ept>スコープを会計カレンダー期間と組み合わせて、より具体的な番号順序を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>New number sequence scopes can be added through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい番号順序の範囲は、拡張機能を通じて追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To create a new scope and have it show up in the client, complete the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープを作成してクライアントに表示させるには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Create an enum extension for <bpt id="p1">**</bpt>NumberSeqParameterType<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSeqParameterType<ept id="p1">**</ept> の列挙型拡張を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the extension, add a new enum value for the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能に、新しいスコープ タイプの新しい列挙値を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Create an enum extension for <bpt id="p1">**</bpt>NumberSequenceType<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceType<ept id="p1">**</ept> の列挙型拡張を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Add a new enum value for the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプの新しい列挙値を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>NumberSequenceType<ept id="p1">**</ept> enum is used in <bpt id="p2">**</bpt>NumberSequenceTableEntity<ept id="p2">**</ept> and <bpt id="p3">**</bpt>NumberSequencesReferenceEntity<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceType<ept id="p1">**</ept> 列挙は、<bpt id="p2">**</bpt>NumberSequenceTableEntity<ept id="p2">**</ept> および <bpt id="p3">**</bpt>NumberSequencesReferenceEntity<ept id="p3">**</ept> で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Create a table extension for the <bpt id="p1">**</bpt>NumberSequenceScope<ept id="p1">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceScope<ept id="p1">**</ept> テーブル拡張子を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Add a new field for the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプの新しいフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Create an extension class for <bpt id="p1">**</bpt>NumberSeqScope<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSeqScope<ept id="p1">**</ept> クラスの拡張クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Create a post handler for the <bpt id="p1">**</bpt>NumberSeqScope::getValidScopeTypes<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSeqScope::getValidScopeTypes<ept id="p1">**</ept> メソッドのポスト ハンドラーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In the event handler method, add the new scope type to the valid scope types list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ハンドラー メソッドでは、有効なスコープ タイプのリストに新しいスコープ タイプを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Create an event handler for the <bpt id="p1">**</bpt>onGetFormatSegmentShortName<ept id="p1">**</ept> delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>onGetFormatSegmentShortName<ept id="p1">**</ept> デリゲートのイベント ハンドラーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the event handler, return the short name for the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ハンドラーで、新しいスコープ タイプの短縮名を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Create a post handler for the <bpt id="p1">**</bpt>NumberSeqScope::find<ept id="p1">**</ept> method and add logic for the new scope type so the corresponding <bpt id="p2">**</bpt>NumberSeqScope<ept id="p2">**</ept> instance can be found.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSeqScope::find<ept id="p1">**</ept> メソッドのポスト ハンドラーを作成し、対応する <bpt id="p2">**</bpt>NumberSeqScope<ept id="p2">**</ept> インスタンスが見つかるように新しいスコープ タイプのロジックを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Create a post handler for the <bpt id="p1">**</bpt>NumberSeqScope::getId<ept id="p1">**</ept> method and add logic for the new scope type, so the corresponding record can be found (or created if it does not exist) in the <bpt id="p2">**</bpt>NumberSequenceScope<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSeqScope::getId<ept id="p1">**</ept> メソッドのポスト ハンドラーを作成し、新しいスコープ タイプのロジックを追加すると、<bpt id="p2">**</bpt>NumberSequenceScope<ept id="p2">**</ept> テーブルに対応するレコードが見つかる (存在しない場合は作成される) ようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Create an extension class for the <bpt id="p1">**</bpt>NumberSequenceScopeFactory<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceScopeFactory<ept id="p1">**</ept> クラスの拡張クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Add a method that initializes the new <bpt id="p1">**</bpt>NumberSeqScope<ept id="p1">**</ept> that represents the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプを表す新しい <bpt id="p1">**</bpt>NumberSeqScope<ept id="p1">**</ept> を初期化するメソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create a form extension for the <bpt id="p1">**</bpt>NumberSequenceDetails<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceDetails<ept id="p1">**</ept> フォームのフォーム拡張を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Add controls that show the new scope type to the <bpt id="p1">**</bpt>Scope<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スコープ<ept id="p1">**</ept> タブに新しいスコープ タイプを表示するコントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Create an extension class for the <bpt id="p1">**</bpt>NumberSequenceDetails<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceDetails<ept id="p1">**</ept> フォームの拡張クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Create a post handler for the <bpt id="p1">**</bpt>updateScopeControlVisibility<ept id="p1">**</ept> method to show the new scope type when the new scope type is selected in the <bpt id="p2">**</bpt>Scope<ept id="p2">**</ept> box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプが<bpt id="p2">**</bpt>スコープ<ept id="p2">**</ept>ボックスで選択されたときに新しいスコープ タイプを表示するために、<bpt id="p1">**</bpt>updateScopeControlVisibility<ept id="p1">**</ept> メソッドのポスト ハンドラーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Create a post handler for the <bpt id="p1">**</bpt>updateScopeControlValues<ept id="p1">**</ept> method to update the values of the controls in the <bpt id="p2">**</bpt>Scope<ept id="p2">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>updateScopeControlValues<ept id="p1">**</ept> メソッドのポスト ハンドラーを作成して、<bpt id="p2">**</bpt>スコープ<ept id="p2">**</ept>タブのコントロールの値を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Create a post handler for the <bpt id="p1">**</bpt>createScope<ept id="p1">**</ept> method to initialize a <bpt id="p2">**</bpt>NumberSeqScope<ept id="p2">**</ept> instance when the new scope type is selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプが選択されたときに <bpt id="p2">**</bpt>NumberSeqScope<ept id="p2">**</ept> インスタンスを初期化するための <bpt id="p1">**</bpt>createScope<ept id="p1">**</ept> メソッドのポスト ハンドラーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Create an event handler for the <bpt id="p1">**</bpt>getShortNameForParameterType<ept id="p1">**</ept> delegate to return the short name for the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプの短い名前を返す <bpt id="p1">**</bpt>getShortNameForParameterType<ept id="p1">**</ept> デリゲートのイベント ハンドラーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Add an extension class for the <bpt id="p1">**</bpt>NumberSequenceTableEntity<ept id="p1">**</ept> and <bpt id="p2">**</bpt>NumberSequencesReferenceEntity<ept id="p2">**</ept> data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberSequenceTableEntity<ept id="p1">**</ept> および <bpt id="p2">**</bpt>NumberSequencesReferenceEntity<ept id="p2">**</ept> データ エンティティの拡張クラスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Create post handlers for the <bpt id="p1">**</bpt>GenerateNumberSequenceScopeTypes<ept id="p1">**</ept> and <bpt id="p2">**</bpt>GenerateNumberSequenceScopeValues<ept id="p2">**</ept> methods to generate the <bpt id="p3">**</bpt>NumberSequenceScope<ept id="p3">**</ept> for the new scope type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいスコープ タイプの <bpt id="p3">**</bpt>NumberSequenceScope<ept id="p3">**</ept> を生成するために、<bpt id="p1">**</bpt>GenerateNumberSequenceScopeTypes<ept id="p1">**</ept> メソッドと <bpt id="p2">**</bpt>GenerateNumberSequenceScopeValues<ept id="p2">**</ept> メソッドのポスト ハンドラーを作成します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>