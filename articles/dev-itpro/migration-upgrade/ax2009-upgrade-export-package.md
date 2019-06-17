<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="ax2009-upgrade-export-package.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>ax2009-upgrade-export-package.1cad75.94366c6a904e9cdb6a0bd3daa3ca514973ab18cd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>94366c6a904e9cdb6a0bd3daa3ca514973ab18cd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\ax2009-upgrade-export-package.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>AX 2009 migration - Export packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 － パッケージのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to export a data package for migration from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations に移行するためにデータ パッケージをエクスポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>AX 2009 migration – Export packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 - パッケージのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can use the Data Import/Export Framework (DIXF) service in Microsoft Dynamics AX 2009 to retrieve data that must be migrated to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワーク (DIXF) サービスを Microsoft Dynamics AX 2009 で使用して、Microsoft Dynamics 365 for Finance and Operations に移行する必要があるデータを取得することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The export process is completed through a job ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート プロセスは、ジョブ ID を使用して行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When you export, you can specify how the export job is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートする場合は、エクスポート ジョブを定義する方法を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can select the source data to export, the conversion value, and the field mapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするソース データ、変換値、およびフィールド マップを選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You can also apply a query to each source to limit what is exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ソースにクエリを適用して、エクスポートされる内容を制限することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The export package that the Data migration tool (DMT) generates can consist of one or many data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ移行ツール (DMT) が生成するエクスポート パッケージは、1 つまたは複数のデータ エンティティで構成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>A typical data package consists of a group of entities for a specific task, such as import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準的なデータ パッケージは、インポートなどの特定のタスクのエンティティ グループで構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For example, the data entities that are required for system setup might be part of one data package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、システムの設定に必要なデータ エンティティは、1 つのデータ パッケージの一部である可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The format of a data package is a compressed file that contains a package manifest, a package header, and any additional files for the data entities that are included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ パッケージの形式は、パッケージ マニフェスト、パッケージ ヘッダー、および含まれているデータ エンティティの追加ファイルを含む圧縮ファイルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Before you create a data package, plan out what should be included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ パッケージを作成する前に、何を含める必要があるかを計画します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In this way, you help guarantee that the correct entities, entity sequence, and fields are included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、正しいエンティティ、エンティティの順序、およびフィールドが含まれていることを保証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Follow these steps to export the data package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ パッケージをエクスポートするには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In AX 2009, in the navigation pane, click <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Common<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Create migration group<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の、ナビゲーション ウィンドウで、<bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>共通<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>移行グループの作成<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the <bpt id="p1">**</bpt>Migration group<ept id="p1">**</ept> form, select the migration group to export, and then click <bpt id="p2">**</bpt>Export now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>移行グループ<ept id="p1">**</ept> フォームで、エクスポートする移行グループを選択し、<bpt id="p2">**</bpt>今すぐエクスポート<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In the <bpt id="p1">**</bpt>Export data<ept id="p1">**</ept> form, update the export file path as required, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データのエクスポート<ept id="p1">**</ept> フォームで、必要に応じてエクスポート ファイル パスを更新し、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>