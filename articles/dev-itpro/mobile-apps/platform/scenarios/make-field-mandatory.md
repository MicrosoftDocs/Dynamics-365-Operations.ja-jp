<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="make-field-mandatory.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>make-field-mandatory.71c7ff.3a915c4ff49a0f01603e7eb34eafa3aef56b46d6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3a915c4ff49a0f01603e7eb34eafa3aef56b46d6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\scenarios\make-field-mandatory.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Make fields mandatory by using workspace classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのクラスを使用してフィールドを必須にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to use workspace classes to make a field mandatory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ワークスペース クラスを使用して、フィールドを必須にする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Make fields mandatory by using workspace classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのクラスを使用してフィールドを必須にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When you use the mobile app designer to select fields for actions, some properties can be inferred.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ デザイナーを使用してアクション用のフィールドを選択するとき、一部のプロパティは推定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>These properties include the field length, the type, and whether the field is mandatory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロパティには、フィールドの長さ、タイプ、フィールドが必須かどうかが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The workspace classes can be used to update these properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロパティを更新するには、ワークスペース クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For example, you might want to specify that the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field is mandatory when a customer record is created, as shown in the following images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次の図に示すように、顧客レコードが作成されると<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドが必須になるよう指定する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Action and fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションおよびフィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Action that has a mandatory field marked</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須フィールドがマークされているアクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Follow these steps to make the <bpt id="p1">**</bpt>Delivery terms<ept id="p1">**</ept> field mandatory by using the workspace class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース クラスを使用して<bpt id="p1">**</bpt>配送条件<ept id="p1">**</ept>フィールドを必須にするには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Get the control name by using the app designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリ デザイナーを使用して、コントロール名を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this example, the control name is <bpt id="p1">**</bpt>DynamicDetail_DlvTerm<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、コントロール名は <bpt id="p1">**</bpt>DynamicDetail_DlvTerm<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Add the following code to set the <bpt id="p1">**</bpt>Mandatory<ept id="p1">**</ept> property for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードを追加して、コントロールの<bpt id="p1">**</bpt>必須<ept id="p1">**</ept>プロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This code uses the reflection-based <bpt id="p1">**</bpt>setProperty<ept id="p1">**</ept> method to set the <bpt id="p2">**</bpt>Mandatory<ept id="p2">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードでは、リフレクションベースの <bpt id="p1">**</bpt>setProperty<ept id="p1">**</ept> メソッドを使用して<bpt id="p2">**</bpt>必須<ept id="p2">**</ept>プロパティを設定しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Build the solution, and then update the app metadata on the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドし、モバイル アプリでアプリのメタデータを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The <bpt id="p1">**</bpt>Delivery terms<ept id="p1">**</ept> field is now marked as <bpt id="p2">**</bpt>Mandatory<ept id="p2">**</ept>, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配送条件<ept id="p1">**</ept> フィールドは、次の図に示すように <bpt id="p2">**</bpt>必須<ept id="p2">**</ept> としてマークされるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Delivery terms field is marked as mandatory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配信条件フィールドは必須とマークされています</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>