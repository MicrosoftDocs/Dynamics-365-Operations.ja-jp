<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="import-demo-data-ax-2012-r3-test-data-transfer-tool.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>import-demo-data-ax-2012-r3-test-data-transfer-tool.ff37bb.2383184dffd2b04c9770fba94db9d08170f361e1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2383184dffd2b04c9770fba94db9d08170f361e1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\import-demo-data-ax-2012-r3-test-data-transfer-tool.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Import demo data for AX 2012 R3 by using the Test Data Transfer Tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツールを使用した AX 2012 R3 のデモ データのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this walkthrough, you will use the Test Data Transfer Tool (beta) to import the demo data for Microsoft Dynamics AX 2012 R3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、テスト データ転送ツール (ベータ) を使用して Microsoft Dynamics AX 2012 R3 のデモ データをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Import demo data for AX 2012 R3 by using the Test Data Transfer Tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツールを使用した AX 2012 R3 のデモ データのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In this walkthrough, you will use the Test Data Transfer Tool (beta) to import the demo data for Microsoft Dynamics AX 2012 R3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、テスト データ転送ツール (ベータ) を使用して Microsoft Dynamics AX 2012 R3 のデモ データをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>We strongly recommend that you work locally on the database server where the business database for AX 2012 R3 is stored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 のビジネス データベースが格納されているデータベース サーバーでローカルに作業することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This is both faster, and avoids any network communication issues during import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、より高速で、インポート中のネットワーク通信の問題を回避します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">**</bpt>Caution:<ept id="p1">**</ept> The Test Data Transfer Tool (beta) is only supported for use in a development, test, or demo environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意:<ept id="p1">**</ept> テスト データ転送ツール (ベータ) は、開発、テスト、またはデモ環境でのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Do not perform this procedure in a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境では、この手順を実行しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Download the demo data and Test Data Transfer Tool (beta)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データおよび Test Data Transfer Tool (beta) をダウンロード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Download the AX 2012 R3 demo data from the Release Page on <bpt id="p1">[</bpt>PartnerSource<ept id="p1">](http://go.microsoft.com/fwlink/?LinkId=403073)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 デモ データを、「<bpt id="p1">[</bpt>PartnerSource<ept id="p1">](http://go.microsoft.com/fwlink/?LinkId=403073)</ept>」のリリース ページからダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Extract the demo data from the package to the database server that hosts the AX 2012 R3 business database for your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データをパッケージから、使用している環境用の AX 2012 R3 ビジネス データベースをホストするデータベース サーバーに抽出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Download the Test Data Transfer Tool (beta) tool installer from the Downloadable tools section of <bpt id="p1">[</bpt>Microsoft Dynamics Lifecycle Services<ept id="p1">](https://lcs.dynamics.com)</ept>, and install it on the database server that hosts the AX 2012 R3 business database for your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Test Data Transfer Tool (beta) ツール インストーラーを「<bpt id="p1">[</bpt>Microsoft Dynamics Lifecycle Services<ept id="p1">](https://lcs.dynamics.com)</ept>」の Downloadable ツール セクションからダウンロードし、使用環境に合わせて AX 2012 R3 ビジネス データべースをホストするデータベース サーバーにインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Verify that you have appropriate permissions to import data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをインポートするための適切なアクセス許可があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You must have read access to the location where the demo data is stored, and in SQL Server Management Studio, permission to execute <bpt id="p1">**</bpt>SELECT<ept id="p1">**</ept> statements and <bpt id="p2">**</bpt>BULK INSERT<ept id="p2">**</ept> statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データが保存されている場所への読み取りアクセスが必要です。SQL Server Management Studio では、<bpt id="p1">**</bpt>選択<ept id="p1">**</ept> ステートメントおよび <bpt id="p2">**</bpt>一括挿入<ept id="p2">**</ept> ステートメントを実行するためのアクセス許可が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Install the Test Data Transfer Tool (beta) for Microsoft Dynamics AX<ept id="p1">](install-test-data-transfer-tool-beta.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ版) をインストールする<ept id="p1">](install-test-data-transfer-tool-beta.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Run the Test Data Transfer Tool (beta)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) の実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Go to <bpt id="p1">**</bpt>Control Panel<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Services<ept id="p2">**</ept>, and stop the AOS instance associated with your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロール パネル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>サービス<ept id="p2">**</ept>に移動し、環境に関連付けられている AOS インスタンスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Using Windows Explorer, browse to the <bpt id="p1">**</bpt>Test Data Transfer Tool (beta)<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows エクスプ ローラーを使用して、<bpt id="p1">**</bpt>テスト データ転送ツール (beta)<ept id="p1">**</ept> を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu in Windows Explorer, click <bpt id="p2">**</bpt>Open command prompt as administrator<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows エクスプローラーの<bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>管理者としてコマンド プロンプトを開く<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>At the command prompt, enter the following command to import the demo data:<bpt id="p1">**</bpt>dp.exe import<ept id="p1">**</ept> location<ph id="ph1">\_</ph>of<ph id="ph2">\_</ph>demo<ph id="ph3">\_</ph>data Name<ph id="ph4">\_</ph>of<ph id="ph5">\_</ph>AX<ph id="ph6">\_</ph>business<ph id="ph7">\_</ph>database ServernameInstanceName.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド プロンプトで次のコマンドを入力し、デモ データをインポートします。<bpt id="p1">**</bpt>dp.exe import<ept id="p1">**</ept> location<ph id="ph1">\_</ph>of<ph id="ph2">\_</ph>demo<ph id="ph3">\_</ph>data Name<ph id="ph4">\_</ph>of<ph id="ph5">\_</ph>AX<ph id="ph6">\_</ph>business<ph id="ph7">\_</ph>database ServernameInstanceName。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>We assume that you are running the Test Data Transfer Tool (beta) on the local computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル コンピューター上でテスト データ転送ツール (beta) を実行していると仮定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If you have a named instance on the local computer, you can use the syntax localhostInstanceName or <bpt id="p1">**</bpt>.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル コンピューターに名前付きインスタンスがある場合は、localhostInstanceName または <bpt id="p1">**</bpt>.<ept id="p1">**</ept> という構文を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>InstanceName.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InstanceName.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In the following example, the data is on the E drive, in the demodata folder, and the business database is named MicrosoftDynamicsAX:<bpt id="p1">**</bpt>dp.exe import e:demodata MicrosoftDynamicsAX<ept id="p1">**</ept> <bpt id="p2">**</bpt>Note:<ept id="p2">**</ept> It may take over 30 minutes to import the demo data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、データが E ドライブの demodata フォルダーにあり、ビジネス データベースには MicrosoftDynamicsAX:<bpt id="p1">**</bpt>dp.exe import e:demodata MicrosoftDynamicsAX<ept id="p1">**</ept> と名前が付けられています。<bpt id="p2">**</bpt>注記:<ept id="p2">**</ept> デモ データのインポートに 30 分以上がかかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If you encounter any issues during the import, you can open the log file <bpt id="p1">**</bpt>DPLog.xml<ept id="p1">**</ept>, which will be created in the folder where you ran the Test Data Transfer Tool (beta).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート中に問題が発生した場合は、ログ ファイル <bpt id="p1">**</bpt>DPLog.xml<ept id="p1">**</ept> を開くことができ、テスト データ転送ツール (ベータ) を実行したフォルダに作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Go to <bpt id="p1">**</bpt>Control Panel<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Services<ept id="p2">**</ept>, and restart the AOS instance associated with your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロール パネル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>サービス<ept id="p2">**</ept>に移動し、環境に関連付けられている AOS インスタンスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt>Test Data Transfer Tool (beta) for Microsoft Dynamics AX 2012<ept id="p1">](test-data-transfer-tool-beta-2012.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Microsoft Dynamics AX 2012 用のテスト データ転送ツール (ベータ)<ept id="p1">](test-data-transfer-tool-beta-2012.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">[</bpt>Install the Test Data Transfer Tool (beta) for Microsoft Dynamics AX<ept id="p1">](install-test-data-transfer-tool-beta.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ) のインストール<ept id="p1">](install-test-data-transfer-tool-beta.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">[</bpt>Run the Test Data Transfer Tool (beta) for Microsoft Dynamics AX<ept id="p1">](run-test-data-transfer-tool-beta.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ) の実行<ept id="p1">](run-test-data-transfer-tool-beta.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>