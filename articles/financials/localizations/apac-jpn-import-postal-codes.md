<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="apac-jpn-import-postal-codes.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>apac-jpn-import-postal-codes.2f2970.ce8d5b7475e9b229235badd7febbfc7e3f7e1050.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ce8d5b7475e9b229235badd7febbfc7e3f7e1050</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\localizations\apac-jpn-import-postal-codes.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Import postal codes for Japan</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日本の郵便番号のインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to import postal codes for Japan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、日本の郵便番号をインポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Import postal codes for Japan</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日本の郵便番号のインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Japan, the Japan Postal Office provides a ZIP code file that you can import into Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日本では、日本郵便局が Microsoft Dynamics 365 for Finance and Operations にインポート可能な郵便番号コード ファイルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic walks you through the process for importing ZIP/postal codes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、郵便番号をインポートするためのプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This example uses the JPMF demo data company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、デモ データの会社 JPMF を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prepare the ZIP code file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">郵便番号コード ファイルを準備します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Download the comma-separated values (CSV) file from the <bpt id="p1">[</bpt>Japan Postal Office home page<ept id="p1">](https://www.post.japanpost.jp/zipcode/download.html)</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt>日本郵便局のホーム ページ<ept id="p1">](https://www.post.japanpost.jp/zipcode/download.html)</ept> からコンマ区切り値 (CSV) ファイルをダウンロードします</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Open the file for editing, and add the following row for column headings.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ファイルを編集するために開き、列見出しのために次の行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In the file, add zeros before any ZIP code that has fewer than seven digits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルで、7 桁に満たない郵便番号コードには前にゼロを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>(ZIP codes that have fewer than seven digits won't be accepted.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(7 桁に満たない郵便番号コードは認められません。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Create a data import project and import the data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート プロジェクトを作成し、データをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Go <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Workspaces<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Data management<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>ワークスペース<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>データ管理<ept id="p3">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Click <bpt id="p1">**</bpt>Import<ept id="p1">**</ept> to create an import project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポート<ept id="p1">**</ept>をクリックしてインポート プロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Enter a name, and select <bpt id="p1">**</bpt>ZIP Postal Code Japan<ept id="p1">**</ept> as the entity name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を入力し、<bpt id="p1">**</bpt>日本の郵便番号<ept id="p1">**</ept>をエンティティの名前として選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Upload the data file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ファイルをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Click <bpt id="p1">**</bpt>Import<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポート<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Validate the results of the import process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート プロセスの結果を検証します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>