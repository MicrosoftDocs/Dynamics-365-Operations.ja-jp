<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-package-templates-dmt.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-package-templates-dmt.ad459c.5bae43939cd3bd5b8db3bbf689164c8c7026aab0.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5bae43939cd3bd5b8db3bbf689164c8c7026aab0</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\create-package-templates-dmt.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>AX 2009 migration - Create templates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 － テンプレートの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to create package templates that you can use to migrate data from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations へデータを移行するために使用できるパッケージ テンプレートを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>AX 2009 migration – Create package templates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 － パッケージ テンプレートの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Packages are created by following a predefined sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを作成するには、事前に定義された順序に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This sequence is based on the dependencies that the data entities have on each another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この順序は、データ エンティティが互いに持つ依存関係に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Because of these dependencies, when you import data entities into Microsoft Dynamics 365 for Finance and Operations, you must import the data entities in the defined order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの依存関係のため、Microsoft Dynamics 365 for Finance and Operations にデータ エンティティをインポートするときは、定義されている順序でデータ エンティティをインポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, you might encounter issues during import and configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうしないと、インポートおよびコンフィギュレーション中に問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The Data migration tool (DMT) provides twenty predefined templates, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ移行ツール (DMT) には、次の図に示すように、20 の事前に定義されたテンプレートが用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Data entity import template list<ept id="p1">](./media/data-entity-templates.png)](./media/data-entity-templates.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データ エンティティ インポート テンプレートの一覧<ept id="p1">](./media/data-entity-templates.png)](./media/data-entity-templates.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can customize an existing template, or you can create your own templates as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のテンプレートをカスタマイズできます。または、必要に応じて、独自のテンプレートを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Follow these steps to view and select the entity lists that will be used in the templates for migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順に従って、移行用のテンプレートで使用されるエンティティの一覧を表示して選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In Microsoft Dynamics AX 2009, click <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Common forms<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Entity list<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Apply sequence<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2009 で、<bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>共通フォーム<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>エンティティ リスト<ept id="p3">**</ept>を順にクリックしてから、<bpt id="p4">**</bpt>順序の適用<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Close the message box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージ ボックスを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Verify that the correct legal entity is selected, and then, in the <bpt id="p1">**</bpt>Show<ept id="p1">**</ept> field, select to view either all entities or only those entities that should be considered for migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しい法人が選択されていることを確認し、<bpt id="p1">**</bpt>表示<ept id="p1">**</ept> フィールドで、すべてのエンティティまたは移行のために考慮すべきエンティティのみのいずれを表示するかを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the <bpt id="p1">**</bpt>Template name<ept id="p1">**</ept> field, select a template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレート名<ept id="p1">**</ept> フィールドで、テンプレートを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the <bpt id="p1">**</bpt>Module selected<ept id="p1">**</ept> pane, select the module that contains the data entities to migrate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択されているモジュール<ept id="p1">**</ept> ウィンドウで、移行するデータ エンティティを含むモジュールを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Entity details<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>Select for migration<ept id="p2">**</ept> check box for every entity line that you want to migrate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティの詳細<ept id="p1">**</ept> タブで、移行するすべてのエンティティ行の <bpt id="p2">**</bpt>移行対象として選択<ept id="p2">**</ept> チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Click <bpt id="p1">**</bpt>Apply sequence<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>順序の適用<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To create a customized template, in the Application Object Tree, go to <bpt id="p1">**</bpt>Resources<ept id="p1">**</ept>, and create a new template in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズされたテンプレートを作成するには、アプリケーション オブジェクト ツリーで、<bpt id="p1">**</bpt>リソース<ept id="p1">**</ept> に移動し、XML 形式で新しいテンプレートを作成します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>