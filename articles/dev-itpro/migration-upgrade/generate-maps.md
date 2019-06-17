<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="generate-maps.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>generate-maps.6c8b01.56095b255c114d7862f0627282ef3a8fe82d70fe.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>56095b255c114d7862f0627282ef3a8fe82d70fe</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\generate-maps.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>AX 2009 migration - Generate maps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 － マップの生成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to generate data maps to migrate data from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、データ マップを生成し、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations へデータを移行する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>AX 2009 migration – Generate maps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 の移行 － マップの生成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Before you can migrate your data from Microsoft Dynamics AX 2009 to Microsoft Dynamics 365 for Finance and Operations, you must align your source data with your target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations へデータを移行する前に、ターゲット環境で、ソース データを配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic explains how to generate source-to-target mappings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ソースとターゲットのマッピングを生成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Before you can generate maps, you must provide the target URL, tenant URL, and service app ID to validate the connection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップを生成するには、接続を検証するための対象の URL、テナント URL、およびサービス アプリケーション ID を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When you create a new app under Microsoft Azure Active Directory (Azure AD) in the Azure portal, you have two options, <bpt id="p1">**</bpt>Web API<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Native<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ポータルの Microsoft Azure Active Directory (Azure AD) で新しいアプリケーションを作成するとき、2 つのオプション <bpt id="p1">**</bpt>Web API<ept id="p1">**</ept> と <bpt id="p2">**</bpt>ネイティブ<ept id="p2">**</ept> があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Select <bpt id="p1">**</bpt>Native<ept id="p1">**</ept>, and grant permissions to the native Azure AD app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ネイティブ<ept id="p1">**</ept>を選択し、ネイティブ Azure AD アプリケーションへのアクセス許可を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Before you generate the data maps between the source and target environments, you must install the Data migration tool (DMT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース環境とターゲット環境間でデータ マップを生成する前に、データ移行ツール (DMT) をインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>Install the Data migration tool<ept id="p1">](install-dmt.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>データ移行ツールーのインストール<ept id="p1">](install-dmt.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Generate maps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップの生成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to generate maps for data migration between AX 2009 and Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 と Finance and Operations の間でのデータ移行のマップを生成するために、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In AX 2009, in the navigation pane, go to <bpt id="p1">**</bpt>Data migration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Configure connections<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2009 のナビゲーション ウィンドウで、<bpt id="p1">**</bpt>データ移行<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>接続の構成<ept id="p3">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Review the field information to verify that it's correct, and then click <bpt id="p1">**</bpt>Validate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの情報を確認して正しいことを確認し、<bpt id="p1">**</bpt>検証<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>After the validation is completed, close the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証の完了後、フォームを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Under <bpt id="p1">**</bpt>Setup<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Configure and generate maps<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>マップを構成および生成<ept id="p2">**</ept> ををクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Verify that the information in the form is correct, and then click <bpt id="p1">**</bpt>Validate path<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの情報が正しいことを確認してから、<bpt id="p1">**</bpt>パスの検証<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>After validation is completed, click <bpt id="p1">**</bpt>Generate maps<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証が完了したら、<bpt id="p1">**</bpt>マップを生成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>