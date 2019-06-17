<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="perfsdk-tutorial.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>perfsdk-tutorial.f57ead.a77db81384a6e4622ce5e9bd03a67e49f8f29187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a77db81384a6e4622ce5e9bd03a67e49f8f29187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\perf-test\perfsdk-tutorial.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Performance SDK and multiuser testing via Visual Studio Online</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic introduces the Performance SDK and shows how to do multiuser testing via Visual Studio Online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、パフォーマンス SDK および、 Visual Studio Online Online を使用したマルチユーザー テストを行う方法について解説します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Performance SDK and multiuser testing via Visual Studio Online</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the Performance software development kit (SDK) and shows how to do multiuser testing via Microsoft Visual Studio Online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) および、Microsoft Visual Studio Online Online を使用したマルチユーザー テストを行う方法について解説します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It also describes how to convert a scenario that you recorded in Task recorder to a single-user test and then a multiuser test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、タスク レコーダーで記録したシナリオをシングルユーザー テスト、そしてマルチユーザー テストに変換する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In the future, we will be publishing some recommendations for alternative solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来的には、代替ソリューションに向けた推奨案の提案に取り組んでいきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>You can continue using it until the end of support cycle.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート サイクルが終了するまで継続して使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you are using the cloud-based load testing service, the cloud-based load testing service will continue to run through March 31, 2020.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド ベースの負荷テストサービスをご利用の場合は、同サービスは2020年3月31日までの間、継続してご利用いただけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Until then, you can continue to use all of the experiences powered by this service without interruption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それまでの間は、同サービスの全機能を継続してご利用いただけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Alternatively, you can switch to on-premises load testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、オンプレミス負荷テストに切り替えることがも可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For more information, see <bpt id="p1">[</bpt>Cloud-based load testing service end of life<ept id="p1">](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、 <bpt id="p1">[</bpt>クラウド ベース 負荷テストサービスの終了について<ept id="p1">](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/)</ept> をご参照ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You must have access the environment as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として環境を利用できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For more information, see <bpt id="p1">[</bpt>Access instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>アクセス インスタンス<ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Microsoft Visual Studio 2015 Enterprise</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 年エンタープライズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>A deployment that has volume data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数量データを含むデプロイメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The Performance SDK (The SDK will likely be in K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス SDK (SDK は K:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory にある可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>However, depending on your environment, it might be in C:<ph id="ph1">\\</ph>PerfSDK.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、環境によっては C:<ph id="ph1">\\</ph>PerfSDK にある可能性があります。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Create a single-user C# test from an XML recording</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML 記録からシングル ユーザー C# テストを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Use Task recorder to create a recording of the scenario that you want to test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク レコーダーを使用して、テストするシナリオの記録を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If your recording doesn't start on the default dashboard page, the test won't be able to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のダッシュ ボード ページでレコードが起動しない場合、テストを実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Start Microsoft Visual Studio as an administrator, and build the <bpt id="p1">**</bpt>PerfSDKSample<ept id="p1">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio を管理者として起動し、<bpt id="p1">**</bpt>PerfSDKSample<ept id="p1">**</ept> プロジェクトをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This project is in the <bpt id="p1">**</bpt>PerfSDK<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロジェクトは <bpt id="p1">**</bpt>PerfSDK<ept id="p1">**</ept> フォルダーにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If you've already built the project, skip this step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを既に構築している場合、この手順を省略します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Select <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Addins<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Create C# perf test from recording<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アドイン<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>記録から C# パフォーマンス テストを作成<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the <bpt id="p1">**</bpt>Import Task Recording<ept id="p1">**</ept> dialog box, enter the required details, and then select <bpt id="p2">**</bpt>Import<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスクの記録をインポート<ept id="p1">**</ept> ダイアログ ボックスで、必要な詳細を入力し、<bpt id="p2">**</bpt>インポート<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Import Task Recording dialog box<ept id="p1">](./media/perf103a.png)](./media/perf103a.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>インポート タスク記録 ダイアログ ボックス<ept id="p1">](./media/perf103a.png)](./media/perf103a.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A C# test is generated in the Generated folder for the project that you selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Run a single-user performance test by using the Performance SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス SDK を使用して単一ユーザー パフォーマンス テストを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Control Panel in Microsoft Windows, select <bpt id="p1">**</bpt>System and Security<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>System<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Advanced System Settings<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows のコントロール パネルで、<bpt id="p1">**</bpt>システムとセキュリティ<ept id="p1">**</ept>  <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>システム<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>システムの詳細設定<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Verify that the <bpt id="p1">**</bpt>TestRoot<ept id="p1">**</ept> environment variable is set to the path of the PerfSDK folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TestRoot<ept id="p1">**</ept>環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>EnvironmentVariable<ept id="p1">](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>EnvironmentVariable<ept id="p1">](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Download the <bpt id="p1">**</bpt>selenium-dotnet-strongnamed-2.42.0.zip<ept id="p1">**</ept> and <bpt id="p2">**</bpt>IEDriverServer<ph id="ph1">\_</ph>Win32<ph id="ph2">\_</ph>2.42.0.zip<ept id="p2">**</ept> files from <bpt id="p3">[</bpt><ph id="ph3">https://selenium-release.storage.googleapis.com/index.html?path=2.42/</ph><ept id="p3">](https://selenium-release.storage.googleapis.com/index.html?path=2.42/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">[</bpt><ph id="ph3">https://selenium-release.storage.googleapis.com/index.html?path=2.42/</ph><ept id="p3">](https://selenium-release.storage.googleapis.com/index.html?path=2.42/)</ept> から、<bpt id="p1">**</bpt>selenium-dotnet-strongnamed-2.42.0.zip<ept id="p1">**</ept> および <bpt id="p2">**</bpt>IEDriverServer<ph id="ph1">\_</ph>Win32<ph id="ph2">\_</ph>2.42.0.zip<ept id="p2">**</ept> ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Extract the files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを抽出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Copy the dynamic-link libraries (DLLs) from the <bpt id="p1">**</bpt>selenium-dotnet-strongnamed-2.42.0.zip\net40<ept id="p1">**</ept> folder to the <bpt id="p2">**</bpt>PerfSDK<ph id="ph1">\\</ph>Common<ph id="ph2">\\</ph>External<ph id="ph3">\\</ph>Selenium<ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動的リンク ライブラリ (DLL) を、<bpt id="p1">**</bpt>selenium-dotnet-strongnamed-2.42.0.zip\net40<ept id="p1">**</ept> フォルダから <bpt id="p2">**</bpt>PerfSDK<ph id="ph1">\\</ph>Common<ph id="ph2">\\</ph>External<ph id="ph3">\\</ph>Selenium<ept id="p2">**</ept> フォルダにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Copy the <bpt id="p1">**</bpt>IEDriverServer.exe<ept id="p1">**</ept> from the <bpt id="p2">**</bpt>IEDriverServer_Win32_2.42.0.zip<ept id="p2">**</ept> to the <bpt id="p3">**</bpt>PerfSDK<ph id="ph1">\\</ph>Common<ph id="ph2">\\</ph>External<ph id="ph3">\\</ph>Selenium<ept id="p3">**</ept> folder as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IEDriverServer.exe<ept id="p1">**</ept> を、<bpt id="p2">**</bpt>IEDriverServer_Win32_2.42.0.zip<ept id="p2">**</ept> から <bpt id="p3">**</bpt>PerfSDK<ph id="ph1">\\</ph>Common<ph id="ph2">\\</ph>External<ph id="ph3">\\</ph>Selenium<ept id="p3">**</ept> フォルダにもコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>DLLs in the PerfSDK\Common\External\Selenium folder<ept id="p1">](./media/perf103d.png)](./media/perf103d.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>PerfSDK\Common\External\Selenium フォルダーにある DLL<ept id="p1">](./media/perf103d.png)](./media/perf103d.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Add a reference to the <bpt id="p1">**</bpt>WebDriver.dll<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>PerfSDK<ph id="ph1">\\</ph>Common<ph id="ph2">\\</ph>External<ph id="ph3">\\</ph>Selenium<ept id="p2">**</ept> folder to your Visual Studio project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>PerfSDK<ph id="ph1">\\</ph>Common<ph id="ph2">\\</ph>External<ph id="ph3">\\</ph>Selenium<ept id="p2">**</ept> フォルダーの <bpt id="p1">**</bpt>WebDriver.dll<ept id="p1">**</ept> への参照を、Visual Studio プロジェクトへ追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Generate and install a certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書を生成しインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>To generate a certificate file, open a Command Prompt window as an administrator, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>When you're prompted for a private key password, select <bpt id="p1">**</bpt>None<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライベート キーのパスワードを要求するメッセージが表示されたら、<bpt id="p1">**</bpt>なし<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Note the following elements in these commands:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのコマンドでは次の要素を注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>-n "CN=127.0.0.1"<ept id="p1">**</ept> gives a human-readable name to the certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>-n "CN=127.0.0.1"<ept id="p1">**</ept> 証明書に人が判読可能な名前が与えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>It's very important that the name of this certificate be <bpt id="p1">**</bpt>127.0.0.1<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書の名前が <bpt id="p1">**</bpt>127.0.0.1<ept id="p1">**</ept> であることが非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Otherwise, the single-user tests won't be able to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は、単一ユーザー テストは実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>-eku 1.3.6.1.5.5.7.3.1<ept id="p1">**</ept> gives the purpose of the certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>-eku 1.3.6.1.5.5.7.3.1<ept id="p1">**</ept> は、証明書の目的を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>After the script has finished running, you should see the following files in <bpt id="p1">**</bpt>C:<ph id="ph1">\\</ph>Temp<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトの実行が終了した後、<bpt id="p1">**</bpt>c:<ph id="ph1">\\</ph>Temp<ept id="p1">**</ept> で以下のファイルが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>authcert.pfx</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">authcert.pfx</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>authcert.cer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">authcert.cer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>authcert.pvk</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">authcert.pvk</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Install the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> and <bpt id="p2">**</bpt>authcert.cer<ept id="p2">**</ept> certificate files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> および <bpt id="p2">**</bpt>authcert.cer<ept id="p2">**</ept> 証明書ファイルをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When you install these files, make sure that you select <bpt id="p1">**</bpt>Local Machine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのファイルをインストールするときは、<bpt id="p1">**</bpt>ローカル コンピューター<ept id="p1">**</ept>をかならず選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Copy the <bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> file to the <bpt id="p2">**</bpt>PerfSDK<ept id="p2">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>authcert.pfx<ept id="p1">**</ept> ファイルを <bpt id="p2">**</bpt>PerfSDK<ept id="p2">**</ept> フォルダにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Open a Microsoft Windows PowerShell window as an administrator, and run the following commands to get the thumbprint of the installed certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> file, enter the thumbprint as the value for the <bpt id="p2">**</bpt>SelfSigningCertificateThumbprint<ept id="p2">**</ept> key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> ファイルで、<bpt id="p2">**</bpt>SelfSigningCertificateThumbprint<ept id="p2">**</ept> キーの値として拇印を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Updated CloudEnvironment.Config file<ept id="p1">](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>更新された CloudEnvironment.Config ファイル<ept id="p1">](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Follow these steps to update the <bpt id="p1">**</bpt>wif.config<ept id="p1">**</ept> file so that Application Object Server (AOS) trusts the certificate:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>wif.config<ept id="p1">**</ept> ファイルを更新して Application Object Server (AOS) が証明書を信頼できるようにするには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Start Microsoft Internet Information Services (IIS), and find <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Finance and Operations<ept id="p1">**</ept> in the list of sites.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft インターネット インフォメーション サービス (IIS) を起動し、サイトの一覧にある <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Finance and Operations<ept id="p1">**</ept> を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Explore<ept id="p1">**</ept>, and find the <bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスプローラー<ept id="p1">**</ept> を選択して、<bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> ファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>wif.config file<ept id="p1">](./media/wifconfig.jpg)](./media/wifconfig.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>wif.config ファイル<ept id="p1">](./media/wifconfig.jpg)](./media/wifconfig.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In the <bpt id="p1">**</bpt>wif.config<ept id="p1">**</ept> file, find the authority that is named <bpt id="p2">**</bpt>AxTokenIssuer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Wif.config<ept id="p1">**</ept> ファイルで、<bpt id="p2">**</bpt>AxTokenIssuer<ept id="p2">**</ept> という機関を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You must add your thumbprint to the list of thumbprints for this authority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この権限の捺印のリストに捺印を追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Thumbprint added to the list of authorities for AxTokenIssuer<ept id="p1">](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>拇印を AxTokenIssuer の機関一覧に追加<ept id="p1">](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Restart IIS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In Visual Studio, open the <bpt id="p1">**</bpt>PerfSDKSample<ept id="p1">**</ept> project, and find the <bpt id="p2">**</bpt>PurchaseReq.cs<ept id="p2">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で <bpt id="p1">**</bpt>PerfSDKSample<ept id="p1">**</ept> プロジェクトを開き、<bpt id="p2">**</bpt>PurchaseReq.cs<ept id="p2">**</ept> ファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This file is a sample single-user test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、サンプル シングルユーザー テストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>In the file, comment out the following lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルで、次の行をコメントアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Lines commented out in PurchaseReq.cs<ept id="p1">](./media/perf103e.png)](./media/perf103e.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>PurchaseReq.cs でコメント アウトされた行<ept id="p1">](./media/perf103e.png)](./media/perf103e.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Modify the <bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> file by entering your admin user name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者のユーザー名を入力することによって <bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> ファイルを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>ConfigName<ept id="p1">**</ept> must be set to <bpt id="p2">**</bpt>DEVFABRIC<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ConfigName<ept id="p1">**</ept> は <bpt id="p2">**</bpt>DEVFABRIC<ept id="p2">**</ept> に設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Modified CloudEnvironment.Config file<ept id="p1">](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>変更された CloudEnvironment.Config ファイル<ept id="p1">](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>In the <bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> file, enter your endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> ファイルに、エンドポイントを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If the environment is enabled for Application Request Routing (ARR), you have two endpoints.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境をアプリケーション リクエスト ルーティング (ARR) に対して有効にするには、2 つのエンドポイントがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Here is an example:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>apr-arr8aos<bpt id="p1">**</bpt>soap<ept id="p1">**</ept>.axcloud.test.dynamics.com</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">apr-arr8aos<bpt id="p1">**</bpt>soap<ept id="p1">**</ept>.axcloud.test.dynamics.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>apr-arr8aos.axcloud.test.dynamics.com</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">apr-arr8aos.axcloud.test.dynamics.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In this case, you must enter both endpoints in the CloudEnvironment.Config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、CloudEnvironment.Config ファイルに両方のエンドポイントを入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Endpoints in CloudEnvironment.Config<ept id="p1">](./media/perf103upd.png)](./media/perf103upd.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CloudEnvironment.Config のエンドポイント<ept id="p1">](./media/perf103upd.png)](./media/perf103upd.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Select <bpt id="p1">**</bpt>Test<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Test settings<ept id="p2">**</ept>, set <bpt id="p3">**</bpt>Default processor architecture<ept id="p3">**</ept> to <bpt id="p4">**</bpt>x64<ept id="p4">**</ept>, and then build the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テスト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>テストの設定<ept id="p2">**</ept> を選択し、<bpt id="p3">**</bpt>既定のプロセッサ アーキテクチャ<ept id="p3">**</ept> を <bpt id="p4">**</bpt>x64<ept id="p4">**</ept> に設定してソリューションをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Select <bpt id="p1">**</bpt>Test<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Windows<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Test Explorer<ept id="p3">**</ept> to view the list of tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テスト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Windows<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>テスト エクスプローラー<ept id="p3">**</ept> を選択してテストの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Sometimes, Visual Studio might not update the list of tests after you create a test script from a task recording.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、タスク記録からテスト スクリプトを作成した後、Visual Studio はテストの一覧を更新しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>In this case, restart Visual Studio, and then reopen Test Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Your new test will be named <bpt id="p1">**</bpt>TestMethod<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいテストに <bpt id="p1">**</bpt>TestMethod<ept id="p1">**</ept> という名前が付けられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>If you change the method name of TestMethod, your test will receive an individual name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TestMethod のメソッド名を変更すると、個々の名前がテストに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>You can now run the test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストを実行できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>When you run the test, Internet Explorer should be started, and it should replay the scenario that you recorded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Create a multiuser test from a single-user test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル ユーザー テストからマルチ ユーザー テストを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>After you create a single-user test by using the information in the previous section, you can convert it to a multiuser test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のセクションで情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Add <bpt id="p1">**</bpt>MS.Dynamics.TestTools.UIHelpers.Core;<ept id="p1">**</ept> to your test script, and find the following line in the <bpt id="p2">**</bpt>TestSetup<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト スクリプトに <bpt id="p1">**</bpt>MS.Dynamics.TestTools.UIHelpers.Core;<ept id="p1">**</ept> を追加して、<bpt id="p2">**</bpt>TestSetup<ept id="p2">**</ept> メソッドで次の行を見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Replace that line with the following lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その行を以下の行に置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The test script that was generated by the Task Importer might contain a line that resembles the following line in the <bpt id="p1">**</bpt>TestSetup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスクのインポーターによって生成されたテスト スクリプトには、<bpt id="p1">**</bpt>TestSetup<ept id="p1">**</ept> メソッドの次の明細行と似ている明細行が含まれている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>You must also remove the following line from the <bpt id="p1">**</bpt>TestCleanup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、<bpt id="p1">**</bpt>TestCleanup<ept id="p1">**</ept> メソッドから次の行を削除する必要もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Remove these lines from any tests that will be run as load tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロード テストとして実行される任意のテストからこれらの明細行を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>This code is required only for single-user tests and has a negative effect on the performance of load tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードはシングル ユーザー テストにのみ必要であり、ロード テストのパフォーマンスに悪影響があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Make sure that the values that you entered when you made the task recording are randomized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク記録が行われたときに入力した値がランダム化されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>You might have to use the Data Expansion Tool first to generate test data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データを生成するために、データ拡張ツールを最初に使用することが必要な可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Set up Azure DevOps for multiuser testing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps でマルチ ユーザー テストを設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>For this example, you will use the ProcureToPay.cs file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、ユーザーは ProcureToPay.cs ファイルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>To start Visual Studio, you must sign in to the <bpt id="p1">[</bpt>Azure DevOps portal<ept id="p1">](https://app.vssps.visualstudio.com/profile/view)</ept>, and then select <bpt id="p2">**</bpt>Open in Visual Studio<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を開始するにサインインする必要があります、<bpt id="p1">[</bpt>Azure DevOps ポータル<ept id="p1">](https://app.vssps.visualstudio.com/profile/view)</ept>にサインインし、<bpt id="p2">**</bpt>Visual Studio で開く<ept id="p2">**</ept>を選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You must complete this step only one time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップは 1 回のみ完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>After you've signed in to Azure DevOps, the settings are saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps にサインインした後、設定が保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Open in Visual Studio<ept id="p1">](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Visual Studio で開く<ept id="p1">](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Open the <bpt id="p1">**</bpt>PerfSDKSample<ept id="p1">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PerfSDKSample<ept id="p1">**</ept> プロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>In the <bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> file, update the <bpt id="p2">**</bpt>UserFormat<ept id="p2">**</ept> entry so that it reflects the admin user URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CloudEnvironment.Config<ept id="p1">**</ept> ファイルで、<bpt id="p2">**</bpt>UserFormat<ept id="p2">**</ept> エントリを更新して、管理者ユーザー URL を反映します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For example, for <ph id="ph1">`admin@example.com`</ph>, use <bpt id="p1">**</bpt>TST<ph id="ph2">\_</ph><ph id="ph3">{0}</ph>@example.com<ept id="p1">**</ept> as the user format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">`admin@example.com`</ph> に対して、ユーザー形式として <bpt id="p1">**</bpt>TST<ph id="ph2">\_</ph><ph id="ph3">{0}</ph>@example.com<ept id="p1">**</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Additionally, change the <bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> value to the number of users that you want to have in your performance test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> 値をパフォーマンス テストに含めるユーザーの数に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Updated CloudEnvironment.Config file<ept id="p1">](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>更新された CloudEnvironment.Config ファイル<ept id="p1">](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Open a Command Prompt window as an administrator, and navigate to the <bpt id="p1">**</bpt>PerfSDK<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者モードでコマンド プロンプトを開き、<bpt id="p1">**</bpt>PerfSDK<ept id="p1">**</ept> フォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Run the following command to create test users for your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行して環境のテスト ユーザーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>You can create as many users as you want.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な数のユーザーを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For example, the following command creates 150 test users for the USMF company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次のコマンドは、USMF 会社で 150 人のテスト ユーザーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Sign in to your endpoint as the admin user, and verify that users were created in the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者ユーザーとしてエンドポイントにログインし、ユーザーがシステムで作成されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Test the sandbox environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境をテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Up to this point, the instructions have assumed that you have a developer topology where the AOS machine is also your development machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここまでは、手順で、AOS マシンが開発マシンでもある開発者トポロジを使用していることを前提としていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>To run load tests in Azure DevOps, the environment that you test must be a sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps でロード テストを実行するには、テスト環境がサンドボックス環境である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>You must complete a few additional steps to establish trust between the sandbox environment and the computer that runs the load tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境と負荷テストを実行するコンピューター間の信頼関係を確立するには、いくつかの追加手順を完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The computer that runs the load tests can be either your development machine or the test agent that is created by Visual Studio Online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">負荷テストを実行できるコンピューターは、開発マシンまたは Visual Studio Online  にて作成したテスト エージェントのいずれかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Establish a Remote Desktop connection to your sandbox AOS machine, and copy over the <bpt id="p1">**</bpt>.cer<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス AOS マシンへのリモート デスクトップ の接続を確立し、<bpt id="p1">**</bpt>.cer<ept id="p1">**</ept> ファイルを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Double-click the file to install it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルをダブルクリックして、インストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>When you're prompted for the certificate store, select <bpt id="p1">**</bpt>Personal<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書ストアの入力を要求するメッセージが表示されたら、<bpt id="p1">**</bpt>個人<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Start IIS, and find <bpt id="p1">**</bpt>AOSService<ept id="p1">**</ept> in the list of sites.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS を起動し、サイトの一覧で <bpt id="p1">**</bpt>AOSService<ept id="p1">**</ept> を見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Then select <bpt id="p1">**</bpt>Explore<ept id="p1">**</ept>, and find the <bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>エクスプローラー<ept id="p1">**</ept> を選択して、<bpt id="p2">**</bpt>wif.config<ept id="p2">**</ept> ファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>In the <bpt id="p1">**</bpt>wif.config<ept id="p1">**</ept> file, find the authority that is named <bpt id="p2">**</bpt>AxTokenIssuer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Wif.config<ept id="p1">**</ept> ファイルで、<bpt id="p2">**</bpt>AxTokenIssuer<ept id="p2">**</ept> という機関を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You must add your thumbprint to the list of thumbprints for this authority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この権限の捺印のリストに捺印を追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>(Use the values from the certificate that you generated earlier.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(以前に生成した証明書の値を使用します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Thumbprint added to the list of authorities for AxTokenIssuer<ept id="p1">](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>拇印を AxTokenIssuer の機関一覧に追加<ept id="p1">](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Restart IIS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You can now run performance tests against the topology.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トポロジに対してパフォーマンス テストを実行することができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>If your topology has multiple AOS machines, you must install the certificate and update the wif.config file on every AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トポロジに複数の AOS マシンがある場合、証明書をインストールして、各 AOS マシンの wif.config ファイルを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Run the performance test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス テストの実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>In the Visual Studio editor, open the <bpt id="p1">**</bpt>ProcureToPay.cs<ept id="p1">**</ept> file, and append the following lines in the <bpt id="p2">**</bpt>TestSetup<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio エディターで、<bpt id="p1">**</bpt>ProcureToPay.cs<ept id="p1">**</ept> ファイルを開き、<bpt id="p2">**</bpt>TestSetup<ept id="p2">**</ept> メソッドに次の行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Download the installer (.msi) file for Microsoft ODBC Driver 13 for SQL Server from <bpt id="p1">[</bpt><ph id="ph1">https://www.microsoft.com/download/details.aspx?id=50420</ph><ept id="p1">](https://www.microsoft.com/download/details.aspx?id=50420)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">https://www.microsoft.com/download/details.aspx?id=50420</ph><ept id="p1">](https://www.microsoft.com/download/details.aspx?id=50420)</ept>から、SQL サーバーの Microsoft ODBC ドライバー 13 のインストーラー (MSI) ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>(Select the 64-bit version of the .msi file.) Put the file in the <bpt id="p1">**</bpt>Visual Studio Online<ept id="p1">**</ept> folder in the <bpt id="p2">**</bpt>PerfSDK<ept id="p2">**</ept> directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(64 ビット バージョンの .msi ファイルを選択します。) ファイルを <bpt id="p2">**</bpt>PerfSDK<ept id="p2">**</ept> ディレクトリの <bpt id="p1">**</bpt>Visual Studio Online<ept id="p1">**</ept> フォルダーに配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Modify the contents of the <bpt id="p1">**</bpt>setup.cmd<ept id="p1">**</ept> file in the <bpt id="p2">**</bpt>Visual Studio Online<ept id="p2">**</ept> folder so that they match the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Visual Studio Online<ept id="p2">**</ept> フォルダ内の <bpt id="p1">**</bpt>setup.cmd<ept id="p1">**</ept> ファイル内容を次のコードと一致するように変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Modify the contents of the <bpt id="p1">**</bpt>CloudCtuFakeACSInstall.cmd<ept id="p1">**</ept> file so that the <bpt id="p2">**</bpt>Import<ept id="p2">**</ept> command has an empty string instead of <bpt id="p3">**</bpt>'password'<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CloudCtuFakeACSInstall.cmd<ept id="p1">**</ept> ファイルの内容を変更して、<bpt id="p2">**</bpt>インポート<ept id="p2">**</ept>コマンドに <bpt id="p3">**</bpt>'パスワード'<ept id="p3">**</ept> の代わりに空の文字列が入るようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The third line of the script should resemble the following line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトの 3 行目は、次の行に似ているはずです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>In your solution files, double-click the <bpt id="p1">**</bpt>vsonline.testsettings<ept id="p1">**</ept> file to modify the test settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション ファイルで、テストの設定を変更する <bpt id="p1">**</bpt>vsonline.testsettings<ept id="p1">**</ept> ファイルをダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>In the <bpt id="p1">**</bpt>Test Settings<ept id="p1">**</ept> dialog box, on the <bpt id="p2">**</bpt>Deployment<ept id="p2">**</ept> tab, use the following settings:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テストの設定<ept id="p1">**</ept>ダイアログ ボックスの<bpt id="p2">**</bpt>配置<ept id="p2">**</ept>タブで、次の設定を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Select the <bpt id="p1">**</bpt>Enable deployment<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>展開の有効化<ept id="p1">**</ept> チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>In the <bpt id="p1">**</bpt>Additional files and directories to deploy<ept id="p1">**</ept> field, make sure that the following files and directories are listed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配置する追加のファイルやディレクトリ<ept id="p1">**</ept> フィールドで、以下のファイルおよびディレクトリが表示されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><ph id="ph1">&amp;lt;</ph>Solution Directory<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>PerfSDKSample<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>Debug<ph id="ph6">\\</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>ソリューション ディレクトリ<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>PerfSDKSample<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>デバッグ<ph id="ph6">\\</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>CloudEnvironment.Config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>CloudEnvironment.Config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>authcert.pfx</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>authcert.pfx</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph>Visual Studio Online<ph id="ph3">\\</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>PerfSDK<ph id="ph2">\\</ph> Visual Studio Online<ph id="ph3">\\</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Additional files and directories to deploy field<ept id="p1">](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>フィールドを配置するための追加ファイルおよびディレクトリ<ept id="p1">](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Your PerfSDK folder might differ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PerfSDK フォルダーが異なっている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>On the <bpt id="p1">**</bpt>Setup and Cleanup Scripts<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>setup.cmd<ept id="p2">**</ept> file that is in the <bpt id="p3">**</bpt>Visual Studio Online<ept id="p3">**</ept> folder in the <bpt id="p4">**</bpt>PerfSDK<ept id="p4">**</ept> directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定とクリーンアップ<ept id="p1">**</ept> タブで、 <bpt id="p4">**</bpt>PerfSDK<ept id="p4">**</ept> ディレクトリ内の <bpt id="p3">**</bpt>Visual Studio Online<ept id="p3">**</ept> フォルダーにある <bpt id="p2">**</bpt>setup.cmd<ept id="p2">**</ept> ファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>On the <bpt id="p1">**</bpt>Additional Settings<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>Run tests in 64 bit process on 64 bit machine<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加設定<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>64 ビット コンピューターで 64 ビット プロセスのテストを実行<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>To run the test, open the <bpt id="p1">**</bpt>SampleLoadTest.loadtest<ept id="p1">**</ept> file, and select <bpt id="p2">**</bpt>Run Load Test<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストを実行するには、<bpt id="p1">**</bpt>SampleLoadTest.loadtest<ept id="p1">**</ept> ファイルを開き、<bpt id="p2">**</bpt>負荷テストを実行<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Run Load Test<ept id="p1">](./media/perf103u.png)](./media/perf103u.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>負荷テストの実行<ept id="p1">](./media/perf103u.png)](./media/perf103u.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>When the test has finished running, you should see a summary that shows transaction results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Transaction results<ept id="p1">](./media/perf103v.png)](./media/perf103v.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>トランザクションの結果<ept id="p1">](./media/perf103v.png)](./media/perf103v.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>To view various indicators for the test controller and test scenario, you can switch to the <bpt id="p1">**</bpt>Graphs<ept id="p1">**</ept> view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、<bpt id="p1">**</bpt>グラフ<ept id="p1">**</ept> ビューに切り替えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Graphs view<ept id="p1">](./media/perf103w.png)](./media/perf103w.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>グラフ 表示<ept id="p1">](./media/perf103w.png)](./media/perf103w.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>While tests are being run, information about your system isn't available in this view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの実行中、システムに関する情報はこのビューで利用することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>To access this information, you must use Microsoft Dynamics Lifecycle Services (LCS) to monitor the CPU and memory usage of your AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Alternatively, you can set up perfmon directly on the AOS machine and set up the Microsoft Azure portal to monitor Microsoft SQL Server usage of Database Transaction Units (DTUs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>No client was opened in the time-out period</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイムアウト期間中クライアントが開かれていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>This issue affects only single-user tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題はシングル ユーザー テストにのみ影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>When the test is running, a web client opens, but a website is never loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストが実行されているとき、Web クライアントを開きますが、Web サイトが読み込まれることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Instead, there is an empty web client that has a white screen, and the following message appears at the top of the page: "This is the initial start page for the WebDriver server."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、白い画面を持つ空の Web クライアントがある場合、ページの上部で次のメッセージが表示されます: 「これは WebDriver サーバーの初期開始ページです。」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>The test will eventually time out and fail, and an error message will be shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストは最終的にタイム アウトおよび失敗し、エラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Follow steps 4 through 8 in the "Run a single-user performance test by using the Performance SDK" section of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの「パフォーマンス SDK を使用してシングル ユーザー パフォーマンス テストを実行する」セクションの、手順 4 から 8 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>That section explains how to create a correct certificate for this type of test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのセクションでは、このタイプのテストの正しい証明書を作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>It also explains how to add the thumbprint of the certificate to the wif.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Zoom factor</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ズーム係数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>This issue affects only single-user tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題はシングル ユーザー テストにのみ影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup = 0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup = 0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup2 = 0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup2 = 0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>Zoomfactor = 80000</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>Zoomfactor = 80000</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select <bpt id="p1">**</bpt>Change the size of text, apps and other items<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、<bpt id="p1">**</bpt>テキスト、アプリ、その他のアイテムのサイズを変更<ept id="p1">**</ept>を選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>This field is available in <bpt id="p1">**</bpt>Display settings<ept id="p1">**</ept> in Windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、Windows の<bpt id="p1">**</bpt>表示設定<ept id="p1">**</ept>で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>If those steps don't work, try to change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Certificate thumbprint errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の拇印のエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>You might receive the error message for several reasons:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のいくつかの理由でエラー メッセージを受け取る可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the <bpt id="p1">**</bpt>HTML/XML<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、<bpt id="p1">**</bpt>HTML/XML<ept id="p1">**</ept> フィールドに余分な文字が表示されているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>For example, you can use the  Unicode converter that is available at <bpt id="p1">[</bpt><ph id="ph1">https://r12a.github.io/apps/conversion/</ph><ept id="p1">](https://r12a.github.io/apps/conversion/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">[</bpt><ph id="ph1">https://r12a.github.io/apps/conversion/</ph><ept id="p1">](https://r12a.github.io/apps/conversion/)</ept> で使用可能な Unicode コンバーターを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Unicode code converter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Unicode コードの変換</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>The certificate wasn't installed on the AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書が AOS マシンにインストールされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>To verify that the certificate can be found on the AOS machine, run the following Windows PowerShell script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate can't be found.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>To fix the issue, copy and install the .cer file that you created earlier in this topic to the AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Password in the CloudCtuFakeACSInstall.cmd file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudCtuFakeACSInstall.cmd ファイルのパスワード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>No endpoint is listening</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リッスンしているエンドポイントはありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>This issue can occur when you run single-user or multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、シングルユーザーまたはマルチユーザーのテストを実行する場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The tests or user creation process fails, and the following error message is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストまたはユーザー作成プロセスが失敗し、次のエラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>In the CloudEnvironment.Config file, review the values that are specified by the following keys:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><ph id="ph1">&amp;lt;</ph>ExecutionConfigurations Key="HostName" Value="<ph id="ph2">&amp;lt;</ph>web address of host<ph id="ph3">&amp;gt;</ph>" /<ph id="ph4">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>ExecutionConfigurations キー ="HostName" 値 ="<ph id="ph2">&amp;lt;</ph>ホストの Web アドレス<ph id="ph3">&amp;gt;</ph>" /<ph id="ph4">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source><ph id="ph1">&amp;lt;</ph>ExecutionConfigurations Key="SoapHostName" Value="<ph id="ph2">&amp;lt;</ph>web address of SOAP<ph id="ph3">&amp;gt;</ph>" /<ph id="ph4">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>ExecutionConfigurations キー ="SoapHostName" 値 ="<ph id="ph2">&amp;lt;</ph>SOAP の Web アドレス<ph id="ph3">&amp;gt;</ph>" /<ph id="ph4">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>The web addresses that are specified by these keys must be the environment that you're testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>In a web browser on your developer machine, make sure that you can open the web address that is specified by the <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者マシンの Web ブラウザで、<bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> キーによって指定された Web アドレスを開けれることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>For online load tests, the environment that is specified by the <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> key in the CloudEnvironment.Config file must be publicly accessible from any machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンライン負荷テストでは、CloudEnvironment.Config ファイルの <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Therefore, if you must test a one-box environment, you won't be able to run the load test by using Visual Studio Online, because the endpoint won't be accessible outside the one-box environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ワンボックス開発環境をテストする必要がある場合、 Visual Studio Online Online を使用した負荷テストの実行はできません。これは、エンドポイントが ワンボックス環境の外部にアクセスできないためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Users can't be enumerated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーを列挙できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Two scenarios can cause this error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つのシナリオで、このエラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The user who is specified as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> in the CloudEnvironment.config file must have the System Administrator role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.config ファイルで <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定されたユーザーはシステム管理者ロールを持っている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>This issue occurs when the System Administrator role isn't assigned to the user who is specified as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、<bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定されたユーザーにシステム管理者の役割が割り当てられていない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>To verify that you've specified the correct user, you can sign in to the endpoint and view the user's roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Admin user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>The user who is specified as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> in the CloudEnvironment.config file has a <bpt id="p2">**</bpt>Provider<ept id="p2">**</ept> other than <ph id="ph1">`"&lt;https://sts.windows-ppe.net/&gt;"`</ph> or <ph id="ph2">`"&lt;https://sts.windows.net/&gt;"`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.config ファイルで <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定されたユーザーは、<ph id="ph1">`"&lt;https://sts.windows-ppe.net/&gt;"`</ph> または <ph id="ph2">`"&lt;https://sts.windows.net/&gt;"`</ph> 以外の<bpt id="p2">**</bpt>プロバイダー<ept id="p2">**</ept>を持ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Sometimes, a company-specific domain is included in the <bpt id="p1">**</bpt>Provider<ept id="p1">**</ept> field for the admin user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、管理者ユーザーの<bpt id="p1">**</bpt>プロバイダ<ept id="p1">**</ept>フィールドに会社固有のドメインを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>To work around this issue, in Finance and Operations, create a user who has any name and email address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、Finance and Operations で、任意の名前と電子メール アドレスを持つユーザーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Assign the System Administrator role to the new user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム管理者ロールを新しいユーザーに割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>You don't have to link the user to a real Azure Active Directory user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーを実在の Azure Active Directory ユーザーにリンクする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Specify this new admin user as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> in the CloudEnvironment.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.config ファイルで、この新しい管理者ユーザーを <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>The HTTP request was forbidden with client authentication scheme 'Anonymous'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Two known scenarios can cause this error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の 2 つのシナリオでは、このエラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>The test users are created by running MS.Dynamics.Performance.CreateUsers.exe without any arguments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>If the CreateUsers script is run without any arguments, the email addresses of test users that are created won't be correctly formatted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスは正しくフォーマットされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>If these users are used to run the tests, the tests will generate the forbidden request error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>You can verify that this scenario is causing the error by viewing the users in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオで Microsoft Dynamics 365 for Finance and Operations のユーザーを表示することによってエラーが発生することを確認できますします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>The incorrect email addresses of the test users will resemble the email addresses in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Incorrectly formatted email addresses<ept id="p1">](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>電子メール アドレスの設定が正しくない<ept id="p1">](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>To resolve the issue, delete the test users who have incorrectly formatted email addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Rerun the CreateUsers script, and specify the user count and company as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>The number of users that you specify in the <bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> field in the CloudEnvironment.Config file exceeds the number of test users that you created by running MS.Dynamics.Performance.CreateUsers.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config ファイルの <bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> フィールドで指定したユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Make sure that you created at least as many test users as you request in the CloudEnvironment.Config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Cloud environment configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド環境のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>At least one security token in the message could not be validated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>It tends to occur when the AOS machine differs from the developer machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>There are two possible causes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの原因が考えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The certificate wasn't installed on the AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書が AOS マシンにインストールされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>To fix the issue, copy the .cer file that you created earlier in this topic to the AOS machine, and install it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を解決するには、このトピックで以前に作成した .cer ファイルを AOS マシンにコピーして、インストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>To fix the issue, see step 8 in the "Run a single-user performance test by using the Performance SDK" section for information about how to add the certificate to the wif.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を解決するには、wif.config ファイルに証明書を追加する方法について、「パフォーマンス SDK を使用してシングル ユーザーのパフォーマンス テストを実行する」の手順 8 を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Be sure to restart IIS after you modify the wif.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">wif.config ファイルを変更した後は、必ず IIS を再起動してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>This issue usually occurs only when you run load tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、通常、ロード テストを実行する場合にのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Verify whether the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあるかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source><ph id="ph1">&amp;lt;</ph>solution path<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">&amp;lt;</ph>your test run<ph id="ph6">&amp;gt;</ph><ph id="ph7">\\</ph>Out</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>solution path<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">&amp;lt;</ph>your test run<ph id="ph6">&amp;gt;</ph><ph id="ph7">\\</ph>Out</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>If the file is missing, add it to the deployment items in the test settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>There are two files that have very similar names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非常に似た名前を持つ 2 つのファイルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>The name of one file ends in <bpt id="p1">**</bpt><ph id="ph1">\*</ph>.dll<ept id="p1">**</ept>, and the name of the other file ends in <bpt id="p2">**</bpt><ph id="ph2">\*</ph>.dll.config<ept id="p2">**</ept>. The <bpt id="p3">**</bpt><ph id="ph3">\*</ph>.dll.config<ept id="p3">**</ept> file must be in the deployment items in the test settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのファイルの名前は、<bpt id="p1">**</bpt><ph id="ph1">\*</ph>.dll<ept id="p1">**</ept> で終わり、もう 1 つのファイルの名前は、<bpt id="p2">**</bpt><ph id="ph2">\*</ph>.dll.config<ept id="p2">**</ept> で終わります。<bpt id="p3">**</bpt><ph id="ph3">\*</ph>.dll.config<ept id="p3">**</ept> ファイルは、テスト設定の配置項目に含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>CloudEnvironment.Config is missing from the deployment items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config が配置項目で見つかりません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>This issue usually occurs only when you run load tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、通常、ロード テストを実行する場合にのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>The issue typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Verify whether the CloudEnvironment.Config file is in the Out folder for the test run:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあるかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source><ph id="ph1">&amp;lt;</ph>solution path<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">&amp;lt;</ph>your test run<ph id="ph6">&amp;gt;</ph><ph id="ph7">\\</ph>Out</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>solution path<ph id="ph2">&amp;gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">&amp;lt;</ph>your test run<ph id="ph6">&amp;gt;</ph><ph id="ph7">\\</ph>Out</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>If the file is missing, add it to the deployment items in the test settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Test settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>InteractiveClientId wasn't specified in the settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InteractiveClientId は設定で指定されていませんでした</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>This issue occurs when the <bpt id="p1">**</bpt>SelfSigningCertificateThumbprint<ept id="p1">**</ept> field is left blank in the CloudEnvironment.Config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は、<bpt id="p1">**</bpt>SelfSigningCertificateThumbprint<ept id="p1">**</ept> フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>The remote host forcibly closed an existing connection</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート ホストは、既存の接続を強制的に終了した</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Run the following Windows PowerShell script on the development machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Service w3svc was not found on computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターでサービス w3svc が見つかりませんでした</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>This error only occurs when you run load tests by using Visual Studio Online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーは、 Visual Studio Online を使用して負荷テストを実行する場合にのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Error example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>A hotfix is available that resolves this issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決する修正プログラムが利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>The Microsoft Knowledge Base (KB) number is 4095640.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>