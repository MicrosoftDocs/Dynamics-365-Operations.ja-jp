<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="multi-user-testing-local-test-controller.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>multi-user-testing-local-test-controller.0acc43.1e88e238063586ca58bf94a30a82c6cc77b6b23a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1e88e238063586ca58bf94a30a82c6cc77b6b23a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>6a975e23130a77aa625d4213000fc0ffbc32dadf</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/05/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\perf-test\multi-user-testing-local-test-controller.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Multi-user testing with the Performance SDK and a local test controller</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to do multi-user testing by using Microsoft Visual Studio and the Performance SDK together with performance test scripts that are generated from Task recorder.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">このトピックでは、タスク レコーダーから生成されたパフォーマンス テスト スクリプトと共に Microsoft Visual Studio とパフォーマンス SDK を使用してマルチユーザー テストを行う方法を説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Multi-user testing with the Performance SDK and a local test controller</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In the future, we will publish some recommendations for alternative solutions.</source>
        <target logoport:matchpercent="89" state="translated" state-qualifier="leveraged-inherited">将来的に、代替ソリューションの推奨を公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can continue using it until the end of the support cycle.</source>
        <target logoport:matchpercent="91" state="translated" state-qualifier="leveraged-inherited">そのサポート サイクルが終了するまで継続して使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you are using the cloud-based load testing service, it will continue to run through March 31, 2020.</source>
        <target logoport:matchpercent="74" state="translated" state-qualifier="leveraged-inherited">クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Until then, you can continue to use all of the experiences powered by this service without interruption.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">それまでの間は、同サービスの全機能を継続してご利用いただけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Alternatively, you can switch to on-premises load testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、オンプレミス負荷テストに切り替えることがも可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>Cloud-based load testing service end of life<ept id="p1">](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/)</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">詳細については、 <bpt id="p1">[</bpt>クラウド ベース 負荷テストサービスの終了について<ept id="p1">](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/)</ept> をご参照ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Before you complete the steps in this topic, verify that the following prerequisites are met:</source><target logoport:matchpercent="96" state="translated" state-qualifier="x-fuzzy-match-unedited">このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You have a Microsoft Dynamics 365 for Finance and Operations development environment that has Platform update 21 or later in own your Microsoft Azure subscription.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">自身の Microsoft Azure サブスクリプションで、プラットフォーム更新プログラム 21 以降の Microsoft Dynamics 365 for Finance and Operations 開発環境があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You have Microsoft Visual Studio 2015 Enterprise edition in a development environment.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">開発環境に Microsoft Visual Studio 2015 Enterprise edition がある</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>You have a tier-2 or above sandbox environment that has the same release (application version and platform update) as your development environment.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックス環境があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You've configured your development environment by following the steps in <bpt id="p1">[</bpt>Single-user testing with Task recorder and the Performance SDK<ept id="p1">](single-user-test-perf-sdk.md)</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt>タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト<ept id="p1">](single-user-test-perf-sdk.md)</ept> の手順に従って開発環境を構成しました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>C<ph id="ph1">\#</ph> performance testing classes have been generated for your end-to-end (E2E) scenarios, and you can run a single-user test by following the steps in <bpt id="p1">[</bpt>Single-user testing with Task recorder and the Performance SDK<ept id="p1">](single-user-test-perf-sdk.md)</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">エンド ツー エンド (E2E) シナリオ用に C<ph id="ph1">\#</ph> パフォーマンス テスト クラスが生成され、<bpt id="p1">[</bpt>タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト<ept id="p1">](single-user-test-perf-sdk.md)</ept> の手順に従ってシングルユーザー テストを実行できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Configure a Finance and Operations development environment for multi-user testing</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">マルチユーザー テストのための Finance and Operations 開発環境の構成</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Download <bpt id="p1">[</bpt>ODBC Driver 17 for SQL Server<ept id="p1">](https://download.microsoft.com/download/E/6/B/E6BFDC7A-5BCD-4C51-9912-635646DA801E/en-US/msodbcsql_17.2.0.1_x64.msi)</ept>, rename the download file <bpt id="p2">**</bpt>msodbcsql<ept id="p2">**</ept>, and copy it to the <bpt id="p3">**</bpt>Visual Studio Online<ept id="p3">**</ept> folder under the <bpt id="p4">**</bpt>PerfSDK<ept id="p4">**</ept> folder.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt>SQL Server の ODBC ドライバー 17<ept id="p1">](https://download.microsoft.com/download/E/6/B/E6BFDC7A-5BCD-4C51-9912-635646DA801E/en-US/msodbcsql_17.2.0.1_x64.msi)</ept> をダウンロードして、ダウンロードしたファイルを <bpt id="p2">**</bpt>msodbcsql<ept id="p2">**</ept> に名前を変更して、それを <bpt id="p4">**</bpt>PerfSDK<ept id="p4">**</ept> フォルダーの <bpt id="p3">**</bpt>Visual Studio Online<ept id="p3">**</ept> フォルダーにコピーします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>msodbcsql file in Visual Studio Online folder<ept id="p1">](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)</ept></source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Visual Studio Online フォルダーの msodbcsql ファイル<ept id="p1">](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Create an environment variable that is named <bpt id="p1">**</bpt>TestRoot<ept id="p1">**</ept>, and point it to the <bpt id="p2">**</bpt>PerfSDK<ept id="p2">**</ept> folder by running the following cmdlet in Microsoft Windows PowerShell.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TestRoot<ept id="p1">**</ept> という名前の環境変数を作成し、Microsoft Windows PowerShell で次のコマンドレットを実行して <bpt id="p2">**</bpt>PerfSDK<ept id="p2">**</ept> フォルダーをポイントします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To view the new environment variable, in the <bpt id="p1">**</bpt>System Properties<ept id="p1">**</ept> dialog box, on the <bpt id="p2">**</bpt>Advanced<ept id="p2">**</ept> tab, select <bpt id="p3">**</bpt>Environment Variables<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">新しい環境変数を表示するには、<bpt id="p1">**</bpt>システム プロパティ<ept id="p1">**</ept> ダイアログ ボックスの <bpt id="p2">**</bpt>詳細<ept id="p2">**</ept> タブで <bpt id="p3">**</bpt>環境変数<ept id="p3">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Environment Variables and System Properties dialog boxes<ept id="p1">](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>[環境変数とシステム プロパティ] ダイアログ ボックス<ept id="p1">](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an admin, and enter the following commands to generate and install the required certificate.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">管理者として <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを入力して必要な証明書を生成してインストールします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>When you're prompted for a private key password, select <bpt id="p1">**</bpt>None<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">プライベート キーのパスワードを要求するメッセージが表示されたら、<bpt id="p1">**</bpt>なし<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Here is an explanation of the elements in preceding commands:</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">上記のコマンドの要素について説明します:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>-n "CN=127.0.0.1"<ept id="p1">**</ept> gives a human-readable name to the certificate.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>-n "CN=127.0.0.1"<ept id="p1">**</ept> 証明書に人が判読可能な名前が与えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>It's very important that the name of this certificate be <bpt id="p1">**</bpt>127.0.0.1<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書の名前が <bpt id="p1">**</bpt>127.0.0.1<ept id="p1">**</ept> であることが非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Otherwise, the single-user tests won't be able to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は、単一ユーザー テストは実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>-eku 1.3.6.1.5.5.7.3.1<ept id="p1">**</ept> gives the purpose of the certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>-eku 1.3.6.1.5.5.7.3.1<ept id="p1">**</ept> は、証明書の目的を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The commands generate the following certificates and save them in C:<ph id="ph1">\\</ph>Temp:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのコマンドは次の証明書を生成し C:<ph id="ph1">\\</ph>Temp に保存します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Authcert.pvk</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Authcert.pvk</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Authcert.cer</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Authcert.cer</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Authcert.pfx</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Authcert.pfx</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Install the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> and <bpt id="p2">**</bpt>authcert.cer<ept id="p2">**</ept> certificates in the <bpt id="p3">**</bpt>Local Machine<ph id="ph1">\\</ph>Personal<ept id="p3">**</ept> certificate store.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p3">**</bpt>ローカル コンピューター<ph id="ph1">\\</ph>個人<ept id="p3">**</ept> 証明書ストアで <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> と <bpt id="p2">**</bpt>authcert.cer<ept id="p2">**</ept> 証明書をインストールします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Local Machine\Personal certificate store<ept id="p1">](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ローカル コンピューター\個人証明書ストア<ept id="p1">](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Copy the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> certificate to the <bpt id="p2">**</bpt>PerfSDK<ph id="ph1">\\</ph>PerfSDKLocalDirectory<ept id="p2">**</ept> folder.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p2">**</bpt>PerfSDK<ph id="ph1">\\</ph>PerfSDKLocalDirectory<ept id="p2">**</ept> フォルダーに <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> 証明書をコピーします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Certificate in PerfSDK<ph id="ph2">\\</ph>PerfS folder<ept id="p1">](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>PerfSDK の証明書 <ph id="ph2">\\</ph> PerfS フォルダー<ept id="p1">](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Replace the <bpt id="p1">**</bpt>setup.md<ept id="p1">**</ept> file in the <bpt id="p2">**</bpt>Visual Studio Online<ept id="p2">**</ept> folder by running the following commands.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次のコマンドを実行して <bpt id="p2">**</bpt>Visual Studio Online<ept id="p2">**</ept> フォルダーの <bpt id="p1">**</bpt>setup.md<ept id="p1">**</ept> ファイルを置き換えます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>Visual Studio Online<ept id="p1">**</ept> folder, in the <bpt id="p2">**</bpt>CloudCtuFakeACSInstall.cmd<ept id="p2">**</ept> file, remove <bpt id="p3">**</bpt>%TestCertPassword%<ept id="p3">**</ept> from the <bpt id="p4">**</bpt>Import<ept id="p4">**</ept> command.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Visual Studio Online<ept id="p1">**</ept> フォルダーの <bpt id="p2">**</bpt>CloudCtuFakeACSInstall.cmd<ept id="p2">**</ept> ファイルで、<bpt id="p4">**</bpt>インポート<ept id="p4">**</ept> コマンドから <bpt id="p3">**</bpt>%TestCertPassword%<ept id="p3">**</ept> を削除します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CloudCtuFakeACSInstall.cmd Import command<ept id="p1">](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CloudCtuFakeACSInstall.cmd インポート コマンド<ept id="p1">](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Prepare the PerfSDKSample solution for multi-user testing</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">マルチユーザー テスト用の PerfSDKSample ソリューションの準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In Microsoft Visual Studio, on the <bpt id="p1">**</bpt>Test<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Test settings<ept id="p2">**</ept>, point to <bpt id="p3">**</bpt>Default processor architecture<ept id="p3">**</ept>, and then select <bpt id="p4">**</bpt>x64<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Microsoft Visual Studio の <bpt id="p1">**</bpt>テスト<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>テストの設定<ept id="p2">**</ept> にポイントして、<bpt id="p3">**</bpt>既定のプロセッサ アーキテクチャ<ept id="p3">**</ept> にポイントして、そして <bpt id="p4">**</bpt>x64<ept id="p4">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Retrieve the thumbprint of the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> certificate in your development environment by running the following cmdlets as an admin. Save the thumbprint somewhere, because you will need it when you configure the tier-2 or above sandbox environment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">管理者として次のコマンドレットを実行して、開発環境の <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> 証明書の拇印を取得します。階層 2 以上のサンドボックス環境を構成するときに必要になるため、拇印をどこかに保存します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The following illustration shows an example of a thumbprint that these cmdlets return.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の図は、これらのコマンドレットが返す拇印の例を示しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Thumbprint in the Command Prompt window<ept id="p1">](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>コマンド プロンプト ウィンドウの拇印<ept id="p1">](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In an environment that has Platform update 21 or later, a certificate that has <bpt id="p1">**</bpt>127.0.0.1<ept id="p1">**</ept> as the issuer is automatically installed.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">プラットフォーム更新プログラム 21 以降の環境では、発行者として <bpt id="p1">**</bpt>127.0.0.1<ept id="p1">**</ept> を持つ証明書が自動的にインストールされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Verify that you retrieve the thumbprint of the certificate that you generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">生成した証明書の拇印を取得したことを確認します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Update the <bpt id="p1">**</bpt>CloudEnvironment.config<ept id="p1">**</ept> file to reflect your configurations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>CloudEnvironment.config<ept id="p1">**</ept> ファイルを更新してコンフィギュレーションを反映します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>As part of this update, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この更新プログラムの一部として、次の手順を実行します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Verify that <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SOAPHostName<ept id="p2">**</ept> match your tier-2 or above sandbox environment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> と <bpt id="p2">**</bpt>SOAPHostName<ept id="p2">**</ept> が階層 2 以上のサンドボックス環境と一致することを確認します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Add the thumbprint of the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> certificate as a value of <bpt id="p2">**</bpt>SelfSigningCertificateThumbprint<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> 証明書の拇印を <bpt id="p2">**</bpt>SelfSigningCertificateThumbprint<ept id="p2">**</ept> の値として追加します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Update <bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> to reflect the number of test users in your case.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> を更新して、このケースでテスト ユーザーの数を反映します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Update <bpt id="p1">**</bpt>UserFormat<ept id="p1">**</ept> to reflect your naming convention for test users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>UserFormat<ept id="p1">**</ept> を更新して、テスト ユーザーの命名規則を反映します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Updated CloudEnvironment.config file<ept id="p1">](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)</ept></source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>更新された CloudEnvironment.config ファイル<ept id="p1">](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Configure <bpt id="p1">**</bpt>vsonline.testsettings<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>vsonline.testsettings<ept id="p1">**</ept> を構成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In the <bpt id="p1">**</bpt>Test Settings<ept id="p1">**</ept> dialog box, on the <bpt id="p2">**</bpt>General<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Test run Location<ept id="p3">**</ept> field group, select the <bpt id="p4">**</bpt>Run tests using local computer or a test controller<ept id="p4">**</ept> option.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>テストの設定<ept id="p1">**</ept> ダイアログ ボックスの <bpt id="p2">**</bpt>一般<ept id="p2">**</ept> タブの <bpt id="p3">**</bpt>テストの実行場所<ept id="p3">**</ept> フィールド グループで <bpt id="p4">**</bpt>ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行<ept id="p4">**</ept> オプションを選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>General tab of the Test Settings dialog box<ept id="p1">](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>[テストの設定] ダイアログボックスの [一般] タブ<ept id="p1">](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>If you don't see <bpt id="p1">**</bpt>vsonline.testsettings<ept id="p1">**</ept>, reopen the solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>vsonline.testsettings<ept id="p1">**</ept> が表示されない場合は、ソリューションをもう一度開きます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>On the <bpt id="p1">**</bpt>Deployment<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>Enable deployment<ept id="p2">**</ept> check box, and then use the <bpt id="p3">**</bpt>Add Directory<ept id="p3">**</ept> and <bpt id="p4">**</bpt>Add File<ept id="p4">**</ept> buttons to add the following folders and files to the <bpt id="p5">**</bpt>Additional files and directories to deploy<ept id="p5">**</ept> field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>配置<ept id="p1">**</ept> タブで <bpt id="p2">**</bpt>配置を有効にする<ept id="p2">**</ept> チェック ボックスを選択し、<bpt id="p3">**</bpt>ディレクトリの追加<ept id="p3">**</ept> と <bpt id="p4">**</bpt>ファイルの追加<ept id="p4">**</ept> ボタンを使用して <bpt id="p5">**</bpt>配置する追加のファイルやディレクトリ<ept id="p5">**</ept> フィールドにフォルダーとファイルを追加します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>SampleProject<ph id="ph4">\\</ph>PerfSDKSample<ph id="ph5">\\</ph>bin<ph id="ph6">\\</ph>Debug<ept id="p1">**</ept> folder</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>SampleProject<ph id="ph4">\\</ph>PerfSDKSample<ph id="ph5">\\</ph>bin<ph id="ph6">\\</ph>Debug<ept id="p1">**</ept> フォルダー</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>Visual Studio Online<ept id="p1">**</ept> folder</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>Visual Studio Online<ept id="p1">**</ept> フォルダー</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>CloudEnvironment.Config<ept id="p1">**</ept> file</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>CloudEnvironment.Config<ept id="p1">**</ept> ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>authcert.pfx<ept id="p1">**</ept> file</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>authcert.pfx<ept id="p1">**</ept> ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config<ept id="p1">**</ept> file</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config<ept id="p1">**</ept> ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Deployment tab of the Test Settings dialog box<ept id="p1">](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)</ept></source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>[テストの設定] ダイアログ ボックスの [配置] タブ<ept id="p1">](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>When you receive a warning that states, "Deployment item not in solution folder," select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">"展開項目がソリューション フォルダにありません" という警告が表示されたら <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択して続行します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>On the <bpt id="p1">**</bpt>Hosts<ept id="p1">**</ept> tab, in the <bpt id="p2">**</bpt>Run tests in 32 bits or 64 bits process<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Run test in 64 bits process on 64 bits machine<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ホスト<ept id="p1">**</ept> タブの <bpt id="p2">**</bpt>32 ビットまたは 64 ビット プロセスでテストを実行<ept id="p2">**</ept> フィールドで、<bpt id="p3">**</bpt>64 ビット コンピューターで 64 ビット プロセスのテストを実行<ept id="p3">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Select <bpt id="p1">**</bpt>Apply<ept id="p1">**</ept>, and then close the <bpt id="p2">**</bpt>Test Settings<ept id="p2">**</ept> dialog box.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>適用<ept id="p1">**</ept> を選択して <bpt id="p2">**</bpt>テストの設定<ept id="p2">**</ept> ダイアログ ボックスを閉じます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Modify your C<ph id="ph1">\#</ph> performance class by adding the following statement to your C<ph id="ph2">\#</ph> performance tests.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">C<ph id="ph2">\#</ph> パフォーマンス テストに次のステートメントを追加して、C<ph id="ph1">\#</ph> パフォーマンス クラスを変更します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>using MS.Dynamics.TestTools.UIHelpers.Core; statement in the Command Prompt window<ept id="p1">](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>MS.Dynamics.TestTools.UIHelpers.Core の使用; コマンド プロンプト ウィンドウのステートメント<ept id="p1">](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Modify the <bpt id="p1">**</bpt>TestSetup<ept id="p1">**</ept> method by adding the following lines to the beginning of the <bpt id="p2">**</bpt>TestSetup()<ept id="p2">**</ept> method.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p2">**</bpt>TestSetup()<ept id="p2">**</ept> メソッドの先頭に次の行を追加して <bpt id="p1">**</bpt>TestSetup<ept id="p1">**</ept> メソッドを変更します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Lines added to the TestSetup method<ept id="p1">](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>TestSetup メソッドに追加された行<ept id="p1">](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>In the <bpt id="p1">**</bpt>TestSetup<ept id="p1">**</ept> method, uncomment lines in the code titled "for multi-user uncomment following lines", and comment out the following line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TestSetup<ept id="p1">**</ept> メソッドで "マルチユーザーの場合は以下の行をコメント解除" というコードの行をコメント解除して、次の行をコメント アウトします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Modified code<ept id="p1">](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>変更されたコード<ept id="p1">](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Modify the <bpt id="p1">**</bpt>TestCleanup<ept id="p1">**</ept> method so that it resembles the following example.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例と同様に <bpt id="p1">**</bpt>TestCleanup<ept id="p1">**</ept> メソッドを変更します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Repeat steps 2 through 11 for all the C<ph id="ph1">\#</ph> performance test classes that you have.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">持っているすべての C<ph id="ph1">\#</ph> パフォーマンス テスト クラスについてステップ 2 から 11 を繰り返します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When you've finished, build the solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">完了したらソリューションをビルドします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In <bpt id="p1">**</bpt>SampleLoadTest.loadtest<ept id="p1">**</ept>, select your test class under <bpt id="p2">**</bpt>Test Mix<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>SampleLoadTest.loadtest<ept id="p1">**</ept> で <bpt id="p2">**</bpt>テスト ミックス<ept id="p2">**</ept> の下のテスト クラスを選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Edit Test Mix dialog box<ept id="p1">](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>[テスト ミックスの編集] ダイアログ ボックス<ept id="p1">](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In <bpt id="p1">**</bpt>SampleLoadTest.loadtest<ept id="p1">**</ept>, update the <bpt id="p2">**</bpt>Timing<ept id="p2">**</ept> fields of <bpt id="p3">**</bpt>Run Settings1 <ph id="ph1">\[</ph>Active<ph id="ph2">\]</ph><ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>SampleLoadTest.loadtest<ept id="p1">**</ept> で <bpt id="p3">**</bpt>実行設定 1 <ph id="ph1">\[</ph>有効<ph id="ph2">\]</ph><ept id="p3">**</ept> の <bpt id="p2">**</bpt>タイミング<ept id="p2">**</ept> フィールドを更新します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>These fields include <bpt id="p1">**</bpt>Warm-up Duration<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Run Duration<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>Cool-down Duration<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのフィールドは <bpt id="p1">**</bpt>ウォームアップ期間<ept id="p1">**</ept>、<bpt id="p2">**</bpt>実行期間<ept id="p2">**</ept>、<bpt id="p3">**</bpt>クールダウン期間<ept id="p3">**</ept> を含みます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Timing fields<ept id="p1">](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)</ept></source><target logoport:matchpercent="67" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>タイミング フィールド<ept id="p1">](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>In <bpt id="p1">**</bpt>Constant Load Pattern<ept id="p1">**</ept>, set the <bpt id="p2">**</bpt>Constant User Count<ept id="p2">**</ept> parameter to the total number of users that you want to use to run the test.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>定数負荷パターン<ept id="p1">**</ept> で、テストの実行に使用するユーザーの総数に <bpt id="p2">**</bpt>定数ユーザー数<ept id="p2">**</ept> パラメーターを設定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Constant User Count parameter<ept id="p1">](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>定数ユーザー数パラメーター<ept id="p1">](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Configure a tier-2 or above sandbox environment for multi-user testing</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">マルチユーザー テスト用に階層 2 以上のサンドボックス環境を構成する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>On each Application Object Server (AOS) computer, install the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> and <bpt id="p2">**</bpt>authcert.cer<ept id="p2">**</ept> certificates under <bpt id="p3">**</bpt>Local Machine<ph id="ph1">\\</ph>Personal<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">各 Application Object Server (AOS) コンピューターの <bpt id="p3">**</bpt>ローカル コンピュータ<ph id="ph1">\\</ph>パーソナル<ept id="p3">**</ept> の下に <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> と <bpt id="p2">**</bpt>authcert.cer<ept id="p2">**</ept> 証明書をインストールします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Certificates installed<ept id="p1">](./media/multi-user-test-local-21.png)](./media/multi-user-test-local-21.png)</ept></source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>インストールした証明書<ept id="p1">](./media/multi-user-test-local-21.png)](./media/multi-user-test-local-21.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Add the thumbprint of the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> certificate in the <bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> file of your tier-2 or above sandbox environment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> 証明書の拇印を階層 2 以上のサンドボックス環境の <bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> ファイルに追加します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Open Microsoft Internet Information Services (IIS) Manager from <bpt id="p1">**</bpt>Administrative Tools<ept id="p1">**</ept>, and then, under <bpt id="p2">**</bpt>Sites<ept id="p2">**</ept>, select <bpt id="p3">**</bpt>AOSService<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>管理ツール<ept id="p1">**</ept> から Microsoft インターネット インフォメーション サービス (IIS) マネージャを開き、<bpt id="p2">**</bpt>サイト<ept id="p2">**</ept> から <bpt id="p3">**</bpt>AOSService<ept id="p3">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>On the right, select <bpt id="p1">**</bpt>Explore in Actions<ept id="p1">**</ept>, and then find the <bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> file at the bottom of the window.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">右側で <bpt id="p1">**</bpt>アクションの確認<ept id="p1">**</ept> を選択し、次にウィンドウの一番下から <bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> ファイルを見つけます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Add the thumbprint of the generated certificate to the bottom of the <ph id="ph1">`https://fakeacs.accesscontrol.windows.net/`</ph> authority.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">生成された証明書の拇印を <ph id="ph1">`https://fakeacs.accesscontrol.windows.net/`</ph> 認証局の末尾に追加します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Thumbprint added from the generated certificate<ept id="p1">](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-21.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>生成された証明書から追加された拇印<ept id="p1">](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-21.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Save the change, and do an IIRESET.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">変更を保存して IIRESET を実行します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Repeat steps 3 through 6 on each AOS computer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">各 AOS コンピューターで手順 3 ～ 6 を繰り返します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Open the <bpt id="p1">**</bpt>SampleLoadTest.load<ept id="p1">**</ept> test to create test users and import them into your target environment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>SampleLoadTest.load<ept id="p1">**</ept> テストを開き、テスト ユーザーを作成してターゲット環境にインポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Then assign the <bpt id="p1">**</bpt>System Administrator<ept id="p1">**</ept> security role to each user.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次に各ユーザーに <bpt id="p1">**</bpt>システム管理者<ept id="p1">**</ept> セキュリティ ロールを割り当てます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Users page in the target environment<ept id="p1">](./media/multi-user-test-local-23.png)](./media/multi-user-test-local-22.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ターゲット環境のユーザー ページ<ept id="p1">](./media/multi-user-test-local-23.png)](./media/multi-user-test-local-22.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>You can also create test users by running <bpt id="p1">**</bpt>MS.Dynamics.Performance.CreateUsers.exe<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>MS.Dynamics.Performance.CreateUsers.exe<ept id="p1">**</ept> を実行してテスト ユーザーを作成することもできます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>In this case, you don't have to do an IISRESET.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">この場合、IISRESET を実行する必要はありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Run multi-user testing by using a local test controller</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ローカル テスト コントローラーを使用したマルチユーザー テストの実行</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the devbox, in Visual Studio, select <bpt id="p1">**</bpt>Run Load Test<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">devbox 上の Visual Studio で <bpt id="p1">**</bpt>負荷テストの実行<ept id="p1">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Run Load Test<ept id="p1">](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>負荷テストの実行<ept id="p1">](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the test output.</source>
        <target logoport:matchpercent="77" state="translated" state-qualifier="leveraged-inherited">テスト出力を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Test output<ept id="p1">](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)</ept></source><target logoport:matchpercent="67" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>テストの出力<ept id="p1">](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For information about single-user or multi-user testing that uses the Performance SDK, see <bpt id="p1">[</bpt>Troubleshooting guide<ept id="p1">](troubleshoot-perf-sdk-user-testing.md)</ept>.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">パフォーマンス SDK を使用したシングルユーザーまたはマルチユーザー テストの詳細は <bpt id="p1">[</bpt>トラブルシューティング ガイド<ept id="p1">](troubleshoot-perf-sdk-user-testing.md)</ept> を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>