<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="copy-configuration-lcs.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>copy-configuration-lcs.a721ee.0bb5510a49eee25d26cc2f44d1a6d3ea04c50aa4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>0bb5510a49eee25d26cc2f44d1a6d3ea04c50aa4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\copy-configuration-lcs.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Copy configurations by using Configuration manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャーを使用して構成をコピーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>You can use the Configuration manager (beta) functionality in Microsoft Dynamics Lifecycle Services to copy a configuration from one instance of Microsoft Dynamics AX 2012 R3 to another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services の構成マネージャー (ベータ) 機能を使用して、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Copy configurations by using Configuration manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャーを使用して構成をコピーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Before you begin, you must set up Configuration manager (beta).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、構成マネージャー (ベータ) を設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For more information, see <bpt id="p1">[</bpt>Set up Configuration manager (Lifecycle Services, LCS)<ept id="p1">](set-up-configuration-manager-lcs.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>構成マネージャーの設定 (Lifecycle Services、LCS)<ept id="p1">](set-up-configuration-manager-lcs.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source><bpt id="p1">**</bpt>Important<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>重要<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This feature is <bpt id="p1">**</bpt>not<ept id="p1">**</ept> supported for production use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、運用上の用途ではサポートされて<bpt id="p1">**</bpt>いません<ept id="p1">**</ept>。 </target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Configuration manager (beta) relies on entities from the Data Import Export Framework in your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because these entities do not currently include all the functionality in AX 2012 R3, some configuration data is not copied between environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Export a configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can create a stored configuration by exporting it from a specified legal entity and entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の法人およびエンティティからエクスポートすることにより、保存済みの構成を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In the <bpt id="p1">**</bpt>Configurations to export<ept id="p1">**</ept> list, click the plus sign (+).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスポートするコンフィギュレーション<ept id="p1">**</ept> リストで、プラス記号 (+) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Enter a name for the configuration, and then click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション名を入力し、<bpt id="p1">**</bpt>開始<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Select a storage location, and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保管場所を選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You can store your configuration locally, in the cloud, or in both locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル、クラウド内、または両方の場所に、構成を保管することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Select an environment to connect to, and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接続先の環境を選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Review the legal entities that are available in the partitions in your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境内のパーティションで使用できる法人を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Select the legal entities to work with, and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処理する法人を選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Select the entities to copy to a stored configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存されているコンフィギュレーションにコピーするエンティティを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Optional: Tables that contain configuration data but are not in entities can't be copied to a stored configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: コンフィギュレーション データが含まれるがエンティティにはないテーブルは、保存されているコンフィギュレーションにコピーできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>To see these tables, click the <bpt id="p1">**</bpt>Missing tables<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテーブルを表示するには、<bpt id="p1">**</bpt>見つからないテーブル<ept id="p1">**</ept> タブをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept> to create your stored configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存された構成を作成するには、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>After a configuration has been created, you can review what it contains.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションが作成された後、その内容を確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Import a configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In the <bpt id="p1">**</bpt>Configurations to import<ept id="p1">**</ept> list, select an existing configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポートするコンフィギュレーション<ept id="p1">**</ept> リストで、既存のコンフィギュレーションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Use the default name, or enter a new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の名前を使用するか、新しい名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If the configuration was stored both locally and in the cloud, you can select which location to import the stored configuration from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションは、ローカルおよびクラウドの両方に格納されている場合、保存されているコンフィギュレーションのインポート元を選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Select the environment to import the configuration to, and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションをインポートする環境を選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Review the companies that are available in the partitions in your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境内のパーティションで使用できる会社を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Select the companies to work with by selecting the location of the company that you are importing from (for example, initialDAT), and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート元の会社の場所 (たとえば、initialDAT) を選択することによってと連携する会社を選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Select the entities to copy to a stored configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存されているコンフィギュレーションにコピーするエンティティを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept> to import your stored configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存された構成をインポートするには、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>After a configuration has been created, you can review what it contains.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションが作成された後、その内容を確認することができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>