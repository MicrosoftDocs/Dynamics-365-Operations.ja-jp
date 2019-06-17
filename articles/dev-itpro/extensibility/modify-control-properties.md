<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="modify-control-properties.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>modify-control-properties.4278af.1d291fb0c7a1bca852e40a7f6beeee8f8e0a5c7c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1d291fb0c7a1bca852e40a7f6beeee8f8e0a5c7c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\modify-control-properties.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Modify the properties of form controls through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して、フォーム コントロールのプロパティを変更する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can modify the properties of a control by using an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張機能を使用してコントロールのプロパティを変更する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Modify the properties of form controls through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して、フォーム コントロールのプロパティを変更する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Often, the way that users interact with the application requires modification.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、ユーザーがアプリとやりとりするには、変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Typically, you hide or disable controls on the page, replace standard labels with labels that are more appropriate, or even add new controls that the user requires.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、ページ上のコントロールを非表示または無効にしたり、標準ラベルをより適切なラベルに置き換えたり、ユーザーが必要とする新しいコントロールを追加したりします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can also create a form extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、フォーム拡張子を作成することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can achieve even more flexibility through event subscription on form control events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム コントロール イベント上のイベント サブスクリプションを使用して、より高い柔軟性を実現することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This approach is discussed in other topics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法については、他のトピックで説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In this topic, the focus is on metadata changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、メタデータの変更に焦点を当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The customer requires changes to the <bpt id="p1">**</bpt>Manage inventory<ept id="p1">**</ept> FastTab on the <bpt id="p2">**</bpt>Released product details<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客は <bpt id="p2">**</bpt>リリース済製品の詳細<ept id="p2">**</ept> ページの <bpt id="p1">**</bpt>在庫の管理<ept id="p1">**</ept> クイック タブへの変更が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You must change the label of the FastTab, disable the field group that shows the catch weight configuration, and add new controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クイック タブのラベルを変更、CW 構成を表示するフィールド グループを無効化、および新しいコントロールを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>(For this example, the new controls aren't bound to existing fields in the data source).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この例では、新しいコントロールはデータ ソース内の既存のフィールドにバインドされません)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Follow these steps to make the required changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な変更を行うには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the extension model, create an extension of the <bpt id="p1">**</bpt>EcoResProductDetailsExtended<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張モデルでは、<bpt id="p1">**</bpt>EcoResProductDetailsExtended<ept id="p1">**</ept> フォームの拡張機能を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Navigate through the form design tree to the <bpt id="p1">**</bpt>TabPageInventory<ept id="p1">**</ept> tab page (<bpt id="p2">**</bpt>Design<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Tab<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Details<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>GroupDetails<ept id="p5">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p6">**</bpt>TabHeader<ept id="p6">**</ept> <ph id="ph5">&amp;gt;</ph> <bpt id="p7">**</bpt>TabPageInventory<ept id="p7">**</ept>), select it in the designer, and open the <bpt id="p8">**</bpt>Property<ept id="p8">**</ept> sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイン ツリーを通じて、<bpt id="p1">**</bpt>TabPageInventory<ept id="p1">**</ept> タブ ページ (<bpt id="p2">**</bpt>デザイン<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>タブ<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>詳細<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>GroupDetails<ept id="p5">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p6">**</bpt>TabHeader<ept id="p6">**</ept> <ph id="ph5">&amp;gt;</ph> <bpt id="p7">**</bpt>TabPageInventory<ept id="p7">**</ept>) に移動し、デザイナーでそれを選択して、<bpt id="p8">**</bpt>プロパティ<ept id="p8">**</ept> シートを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Update the <bpt id="p1">**</bpt>Caption<ept id="p1">**</ept> property to the desired value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キャプション<ept id="p1">**</ept>プロパティを目的の値に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Caption property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプション プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Right-click the tab page, and then select <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タブ ページを右クリックし、<bpt id="p1">**</bpt>新規<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Set the required properties on the new control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコントロールで必要なプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You can also move the control up and down in the immediate container to position it correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、すぐそばのコンテナでコントロールを上下に移動して、適切に配置することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Alternatively, right-click the subnode that the new control should appear after, select <bpt id="p1">**</bpt>Insert sibling<ept id="p1">**</ept>, and then select the type of control to add.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、新しいコントロールに表示するサブノードを右クリックし、<bpt id="p1">**</bpt>Insert sibling<ept id="p1">**</ept> を選択し、追加するコントロールのタイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Insert sibling command</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">兄弟コマンドの挿入</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Of course, you can just drag bound controls over from the corresponding data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もちろん、対応するデータ ソースからバインドされたコントロールをドラッグすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Select the <bpt id="p1">**</bpt>PdsCatchWeight<ept id="p1">**</ept> group control, and change the <bpt id="p2">**</bpt>Enabled<ept id="p2">**</ept> property to <bpt id="p3">**</bpt>No<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PdsCatchWeight<ept id="p1">**</ept> グループ コントロールをオンにし、<bpt id="p2">**</bpt>有効<ept id="p2">**</ept> プロパティを <bpt id="p3">**</bpt>いいえ<ept id="p3">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Enabled property of the PdsCatchWeight group control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PdsCatchWeight グループ コントロールのプロパティを有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If you change metadata properties such as <bpt id="p1">**</bpt>Enabled<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Visible<ept id="p2">**</ept>, there is no guarantee that the control will stay in that state at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept>および<bpt id="p2">**</bpt>表示<ept id="p2">**</ept>のようにメタデータのプロパティを変更した場合、実行時にその状態のままでコントロールの保証はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>After a form is loaded, business logic on that form can change the state of controls through code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームが読み込まれた後、そのフォームのビジネス ロジックは、コードを使用してコントロールの状態を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When you've finished, the page includes additional fields, catch weight information can't be edited, and the whole FastTab has a different caption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、ページには追加のフィールドが含まれ、CW 情報を編集することはできず、クイック タブ全体のキャプションが異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Modified FastTab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更されたクイック タブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You can't modify the <bpt id="p1">**</bpt>AutoDeclaration<ept id="p1">**</ept> property on controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールで <bpt id="p1">**</bpt>AutoDeclaration<ept id="p1">**</ept> プロパティを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>However, you can still access the controls by name from code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、コードから名前でコントロールにアクセスすることはできます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>