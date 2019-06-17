<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="troubleshoot-perf-sdk-user-testing.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>troubleshoot-perf-sdk-user-testing.a4bf25.bb2c43ea125aa231458d791c6560e3bf33cfcb7d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bb2c43ea125aa231458d791c6560e3bf33cfcb7d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>c576b81dc3c93c09fb08fb0ba0c19f417360c5ab</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/05/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\perf-test\troubleshoot-perf-sdk-user-testing.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Troubleshooting guide for single-user or multi-user testing with the Performance SDK</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">パフォーマンスSDKを使用した、シングルユーザーまたはマルチユーザーテストのためのトラブルシューティングガイド</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides troubleshooting information for common issues that you might encounter during single-user or multi-user testing that uses the Performance SDK.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、パフォーマンスSDKを使用したシングルユーザーまたはマルチユーザーのテスト中に発生する可能性のある一般的な問題のトラブルシューティングについて説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Troubleshooting guide for single-user or multi-user testing with the Performance SDK</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">パフォーマンスSDKを使用した、シングルユーザーまたはマルチユーザーテストのためのトラブルシューティングガイド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>No client was opened in the time-out period</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">タイムアウト期間中クライアントが開かれていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This issue affects only single-user tests.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題はシングル ユーザー テストにのみ影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the test is running, a web client is opened, but a website is never loaded.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">テストの過程で、Webクライアントが起動するが、Webサイトが表示されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Instead, there is an empty web client that has a white background.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">webクライアントには何も表示されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The following message appears at the top of the page, "This is the initial start page for the WebDriver server."</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次のメッセージがページの上部に表示されます。「これはWebDriverサーバーの既定のスタートページです」。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The test eventually times out and fails, and an error message is shown.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match">テストは最終的にタイム アウトの後に失敗し、エラー メッセージが表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Initialization method <ph id="ph1">\&lt;</ph>Test class name<ph id="ph2">\&gt;</ph>.TestSetup threw an exception.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">初期化メソッド <ph id="ph1">\&lt;</ph>テストクラス名<ph id="ph2">\&gt;</ph> TestSetupが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System.TimeoutException: System.TimeoutException: No client was opened in the timeout period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">TimeoutException: TimeoutException: タイムアウト時間内にクライアントが開かれませんでした。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>See <bpt id="p1">[</bpt>Multi-user testing with the Performance SDK and a local test controller<ept id="p1">](multi-user-testing-local-test-controller.md)</ept>.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト<ept id="p1">](multi-user-testing-local-test-controller.md)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>That topic explains how to create a correct certificate for this type of test.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">リンク先セクションでは、このタイプのテストにおいて正しい証明書を作成する方法について説明しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>It also explains how to add the thumbprint of the certificate to the wif.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Zoom factor</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ズーム係数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>This issue affects only single-user tests.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">この問題はシングル ユーザー テストにのみ影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Initialization method <ph id="ph1">\&lt;</ph>Test class name<ph id="ph2">\&gt;</ph>.TestSetup threw exception.</source><target logoport:matchpercent="93" state="translated" state-qualifier="x-fuzzy-match-unedited">初期化メソッド <ph id="ph1">\&lt;</ph>テストクラス名<ph id="ph2">\&gt;</ph> TestSetupが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">System.InvalidOperationException: System.InvalidOperationException: Internet Explorerで予期しないエラーが発生しました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Browser zoom level was set to 200%.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ブラウザーのズームレベルが200% に設定されていました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>It should be set to 100% (NoSuchDriver).</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">ズームレベルは100%に設定してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup = 0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup = 0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup2 = 0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>ResetZoomOnStartup2 = 0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>Zoomfactor = 80000</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Computer<ph id="ph1">\\</ph>HKEY<ph id="ph2">\_</ph>CURRENT<ph id="ph3">\_</ph>USER<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Microsoft<ph id="ph6">\\</ph>Internet Explorer<ph id="ph7">\\</ph>Zoom<ph id="ph8">\\</ph>Zoomfactor = 80000</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select <bpt id="p1">**</bpt>Change the size of text, apps and other items<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、<bpt id="p1">**</bpt>テキスト、アプリ、その他のアイテムのサイズを変更<ept id="p1">**</ept>を選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This field is available in <bpt id="p1">**</bpt>Display settings<ept id="p1">**</ept> in Microsoft Windows.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">このフィールドは、 Microsoft Windows の <bpt id="p1">**</bpt>表示設定<ept id="p1">**</ept> で使用できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>If those steps don't work, change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">これらの手順が機能しない場合は、RDP セッションを開始する前に Internet Explorer で既定のズーム レベルが 100 % になるよう、リモート デスクトップのサイズを変更するようにします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Certificate thumbprint errors</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">証明書の拇印のエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup** threw an exception.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup** が例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><ph id="ph1"> --</ph><ph id="ph2">\&gt;</ph> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> --</ph><ph id="ph2">\&gt;</ph> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 拇印によるトークン作成用の証明書の検索に失敗しました: b4f01d2fc42718198852cd23957fc60a3e4bca2e.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>You might receive the error message for one of the following reasons:</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">以下に挙げるいずれかの理由でエラー メッセージが表示される可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the <bpt id="p1">**</bpt>HTML/XML<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、<bpt id="p1">**</bpt>HTML/XML<ept id="p1">**</ept> フィールドに余分な文字が表示されているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For example, you can use the Unicode converter that is available at <ph id="ph1">&lt;https://r12a.github.io/apps/conversion/&gt;</ph>.</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">たとえば、 <ph id="ph1">&lt;https://r12a.github.io/apps/conversion/&gt;</ph>にて提供されている Unicode コンバーターを使用できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Unicode conversion<ept id="p1">](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)</ept></source><target logoport:matchpercent="69" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ユニコード変換<ept id="p1">](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The certificate wasn't installed on the Application Object Server (AOS) machine.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">アプリケーション オブジェクト サーバー マシン (AOS) に証明書が 正しくインストールされていません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>To verify that the certificate can be found on the AOS machine, run the following Microsoft Windows PowerShell script.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">以下の Microsoft Windows PowerShell スクリプトを実行し、認証が必要となる証明書をAOSマシン内で検索します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate isn't installed.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書をインストールすることはできません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To fix the issue, copy and install a .cer file on all AOS machines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この問題を修正するには、すべてのAOSマシンに .cerファイルをコピーしてインストールします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Password in the .cmd file<ept id="p1">](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)</ept></source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>.cmd file のパスワード<ept id="p1">](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>No endpoint is listening</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">リッスンしているエンドポイントはありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>This issue can occur when you run single-user or multi-user tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The tests fail, or the user creation process fails, and the following error message is shown:</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">テスト、またはユーザー作成処理が失敗し、次のエラー メッセージが表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>web address<ph id="ph5">\&gt;</ph> that could accept the message.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph>System.ServiceModel.EndpointNotFoundException: <ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>web address<ph id="ph5">\&gt;</ph> にてメッセージを受領することができるエンドポイント リスニングがありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>This is often caused by an incorrect address or SOAP action.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">この事象は、正しくないアドレスまたは SOAP アクションによって引き起こされることがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In the CloudEnvironment.Config file, review the values that are specified by the following keys:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>ExecutionConfigurations Key="HostName" Value="<ph id="ph3">\&lt;</ph>web address of host<ph id="ph4">\&gt;</ph>" /<ph id="ph5">\&gt;</ph></source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match"><ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>ExecutionConfigurations Key="ホスト名" Value="<ph id="ph3">\&lt;</ph>ホストのWebアドレス<ph id="ph4">\&gt;</ph>" /<ph id="ph5">\&gt;</ph></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>ExecutionConfigurations Key="SoapHostName" Value="<ph id="ph3">\&lt;</ph>web address of SOAP<ph id="ph4">\&gt;</ph>" /<ph id="ph5">\&gt;</ph></source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match"><ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>ExecutionConfigurations Key="SoapHostName" Value="<ph id="ph3">\&lt;</ph>SOAPのWebアドレス<ph id="ph4">\&gt;</ph>" /<ph id="ph5">\&gt;</ph></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The web addresses that are specified by these keys must be in the environment that you're testing.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">これらのキーに指定する Web アドレスは、現在テストを実施している環境である必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>In a web browser on your developer machine, make sure that you can open the web address that is specified by the <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> key.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">開発者マシンの Web ブラウザで、<bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> キーによって指定された Web アドレスを開けれることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>For online load tests, the environment that is specified by the <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> key in the CloudEnvironment.Config file must be publicly accessible from any machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンライン負荷テストでは、CloudEnvironment.Config ファイルの <bpt id="p1">**</bpt>HostName<ept id="p1">**</ept> キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Therefore, if you must test a one-box environment, you won't be able to run the load test by using Microsoft Visual Studio Online, because the endpoint won't be accessible outside the one-box environment.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">したがって、ワンボックス環境をテストする必要がある場合、Microsoft Visual Studio Online Online を使用して負荷テストを実行することはできません。これは、エンドポイントが ワンボックス環境の外部にアクセスできないためです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Users can't be enumerated</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ユーザーを列挙できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This issue can occur when you run multi-user tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source>
        <target logoport:matchpercent="87" state="translated" state-qualifier="leveraged-inherited">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.InvalidOperationException: Could not enumerate AX users ---<ph id="ph3">\&gt;</ph> System.ServiceModel.FaultException'1<ph id="ph4">\[</ph>System.ComponentModel.Win32Exception<ph id="ph5">\]</ph>: Forbidden</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.InvalidOperationException: AX のユーザーを列挙することができませんでした ---<ph id="ph3">\&gt;</ph> System.ServiceModel.FaultException'1<ph id="ph4">\[</ph>System.ComponentModel.Win32Exception<ph id="ph5">\]</ph>: 禁止されています</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Two scenarios can cause this error:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2 つのシナリオで、このエラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The System Administrator role isn't assigned to the user who is specified as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> in the CloudEnvironment.config file.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">CloudEnvironment.config ファイルにて <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定されているユーザーに、システム管理者ロールが割り当てられていません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>To verify that you've specified the correct user, sign in to the endpoint, and view the user's roles.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">適切なユーザーが指定されていることを検証するには、エンドポイントにサインインし、ユーザーのロールを確認します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Users page<ept id="p1">](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ユーザーページ<ept id="p1">](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The user who is specified as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> in the CloudEnvironment.config file has a provider other than <ph id="ph1">`https://sts.windows-ppe.net/`</ph> or <ph id="ph2">`https://sts.windows.net/`</ph>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">CloudEnvironment.config ファイルにて <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定されているユーザーは、 <ph id="ph1">`https://sts.windows-ppe.net/`</ph> または <ph id="ph2">`https://sts.windows.net/`</ph> 以外のプロバイダーを持っています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Sometimes, a company-specific domain is included in the <bpt id="p1">**</bpt>Provider<ept id="p1">**</ept> field for the admin user.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">場合によっては、管理者ユーザーの<bpt id="p1">**</bpt>プロバイダ<ept id="p1">**</ept>フィールドに会社固有のドメインを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>To work around this issue, in Microsoft Dynamics 365 for Finance and Operations, create a user who has any name and email address.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Microsoft Dynamics 365 for Finance and Operations にてこの問題を回避するには、任意の名前と電子メール アドレスを持つユーザーを作成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Assign the <bpt id="p1">**</bpt>System Administrator<ept id="p1">**</ept> role to the new user.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>システム管理者<ept id="p1">**</ept> ロールを新しいユーザーに割り当てます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>You don't have to link the user to a real Microsoft Azure Active Directory (Azure AD) user.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">ユーザーを実在の Microsoft Azure Active Directory (Azure AD) ユーザーにリンクする必要はありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Specify this new admin user as <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> in the CloudEnvironment.config file.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.config ファイルで、この新しい管理者ユーザーを <bpt id="p1">**</bpt>SelfMintingAdminUser<ept id="p1">**</ept> として指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The HTTP request was forbidden with client authentication scheme 'Anonymous'</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Initialization method <ph id="ph1">\&lt;</ph>Test class name<ph id="ph2">\&gt;</ph>.TestSetup threw exception.</source>
        <target logoport:matchpercent="93" state="translated" state-qualifier="leveraged-inherited">初期化メソッド <ph id="ph1">\&lt;</ph>テストクラス名<ph id="ph2">\&gt;</ph> TestSetupが例外をスローしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: クライアント認証スキーム'Anonymous'でHTTP要求が禁止されました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.WebException: The remote server returned an error: (403) Forbidden.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.WebException: リモートサーバーからエラーが返されました: (403) 許可されていません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Two known scenarios can cause this error:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">既知の 2 つのシナリオでは、このエラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The test users are created by running MS.Dynamics.Performance.CreateUsers.exe without any arguments.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>For example, if the CreateUsers script is run without any arguments, the email addresses of test users that are created won't be correctly formatted.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">例えば、CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスが正しくフォーマットされません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>If these users are used to run the tests, the tests will generate the forbidden request error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>You can verify that this scenario is causing the error by viewing the users in Finance and Operations.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">このシナリオがエラーの原因であることを確認するには、Finance and Operations のユーザーを表示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The incorrect email addresses of the test users will resemble the email addresses in the following illustration.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>List of incorrect user email addresses<ept id="p1">](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>誤りのあるユーザーの電子メールアドレスの一覧<ept id="p1">](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To resolve the issue, delete the test users who have incorrectly formatted email addresses.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Rerun the CreateUsers script, and specify the user count and company.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を特定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The number of users that you specify in the <bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> field in the CloudEnvironment.Config file exceeds the number of test users that you created by using MS.Dynamics.Performance.CreateUsers.exe.</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">CloudEnvironment.Config ファイルの <bpt id="p1">**</bpt>UserCount<ept id="p1">**</ept> フィールドで指定しているユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Make sure that you created at least as many test users as you request in the CloudEnvironment.Config file.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CloudEnvironment.Config file<ept id="p1">](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)</ept></source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CloudEnvironment.config ファイル<ept id="p1">](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>At least one security token in the message could not be validated</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>This issue can occur when you run multi-user tests, when you create users by using MS.Dynamics.Performance.CreateUsers.exe, when the AOS machine differs from the developer machine.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成している場合、AOSマシンが開発用のマシンと異なる場合に発生する可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source>
        <target logoport:matchpercent="87" state="translated" state-qualifier="leveraged-inherited">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.Security.MessageSecurityException: セキュリティで保護されていない、または正しく保護されていない障害を受信しました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>See the inner FaultException for the fault code and detail.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">障害コードと詳細については、FaultException 内部を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.FaultException: At least one security token in the message could not be validated.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.FaultException: メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>There are two possible causes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの原因が考えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The certificate wasn't installed on the AOS machine.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">証明書が AOS マシンにインストールされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>To fix the issue, copy a .cer file to the AOS machine, and install it.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">この問題を修正するには、AOSマシンに .cerファイルをコピーしてインストールします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>To fix the issue, add the certificate to the wif.config file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この問題を修正するには、wifファイルに証明書を追加します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Be sure to restart Microsoft Internet Information Services (IIS) after you change the wif.config file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wifファイルを更新した後に、必ずMicrosoft インターネット インフォメーション サービス (IIS) を再起動してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>This issue usually occurs when you run load tests.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">この問題は、通常、負荷 テストを実行する場合にのみ発生します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source><ph id="ph1">\&lt;</ph>Test class name<ph id="ph2">\&gt;</ph>.TestSetup threw exception.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><ph id="ph1">\&lt;</ph>テストクラス名<ph id="ph2">\&gt;</ph> TestSetupが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">InvalidOperationException: InvalidOperationException: ServiceModelクライアント構成セクションに名前'ClientCommunicationManager'および契約'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager'を持つエンドポイント要素が見つかりませんでした。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element..</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これは、アプリケーションに対応する構成ファイルが見つからなかったか、またはこの名前と一致するエンドポイント要素がクライアント要素にて見つからないことが原因です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">SSystem.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors にて (ServiceEndpoint serviceEndpoint, String configurationName)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Verify that the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><ph id="ph1">\&lt;</ph>solution path<ph id="ph2">\&gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">\&lt;</ph>your test run<ph id="ph6">\&gt;</ph><ph id="ph7">\\</ph>Out</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\&lt;</ph>solution path<ph id="ph2">\&gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">\&lt;</ph>your test run<ph id="ph6">\&gt;</ph><ph id="ph7">\\</ph>Out</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>If the file is missing, add it to the deployment items in the test settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>There are two files that have very similar names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非常に似た名前を持つ 2 つのファイルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The name of one file ends in <ph id="ph1">\*</ph>.dll, and the name of the other file ends in <ph id="ph2">\*</ph>.dll.config. The <ph id="ph3">\*</ph>.dll.config file must be in the deployment items in the test settings.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">一方は名前が <ph id="ph1">\*</ph>.dll で終わるファイルで、もう一方は名前が <ph id="ph2">\*</ph>.dll.configで終わるファイルです。 <ph id="ph3">\*</ph>.dll.configファイルはテスト設定の配置項目に含まれている必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>CloudEnvironment.Config is missing from the deployment items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config が配置項目で見つかりません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>This issue usually occurs only when you run load tests.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題は、通常、ロード テストを実行する場合にのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Initialization method <ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>Test class name<ph id="ph3">\&gt;</ph>.TestSetup threw exception.</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">初期化メソッド <ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>Test class name<ph id="ph3">\&gt;</ph>. TestSetupが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> MS.Dynamics.TestTools.TestLogging.EvaluateException: アサートに失敗しました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DateTime="10/13/2017 14:42:55" "'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>It typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">一般的に、この問題は負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Verify that the CloudEnvironment.Config file is in the Out folder for the test run:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source><ph id="ph1">\&lt;</ph>solution path<ph id="ph2">\&gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">\&lt;</ph>your test run<ph id="ph6">\&gt;</ph><ph id="ph7">\\</ph>Out</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\&lt;</ph>solution path<ph id="ph2">\&gt;</ph><ph id="ph3">\\</ph>TestResults<ph id="ph4">\\</ph><ph id="ph5">\&lt;</ph>your test run<ph id="ph6">\&gt;</ph><ph id="ph7">\\</ph>Out</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the file is missing, add it to the deployment items in the test settings.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Deployment items in the Test Settings dialog box<ept id="p1">](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>テスト設定 ダイアログ ボックスの 配置 タブ<ept id="p1">](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>InteractiveClientId was not specified in the settings</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">InteractiveClientId が設定で指定されていませんでした</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientIdが設定で指定されていませんでした。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>This issue occurs when the <bpt id="p1">**</bpt>SelfSigningCertificateThumbprint<ept id="p1">**</ept> field is left blank in the CloudEnvironment.Config file.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題は、<bpt id="p1">**</bpt>SelfSigningCertificateThumbprint<ept id="p1">**</ept> フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>The remote host forcibly closed an existing connection</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">リモート ホストは、既存の接続を強制的に終了した</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.CommunicationException: An error occurred while making the HTTP request to <ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>Host name<ph id="ph5">\&gt;</ph>/Services/AxUserManagement/Service.svc/ws2007FedHttp.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ServiceModel.CommunicationException: <ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>Host name<ph id="ph5">\&gt;</ph>/Services/AxUserManagement/Service.svc/ws2007FedHttp.にHTTP要求をした際にエラーが発生しました</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">HTTPS の場合、サーバー証明書が HTTP.SYS で正しくコンフィギュレーションされていない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This could also be caused by a mismatch of the security binding between the client and the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、クライアントとサーバー間のセキュリティ バインドの不一致によっても発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.WebException: The underlying connection was closed: An unexpected error occurred on a send.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.WebException: 基礎的な接続が閉じられました: 送信時に予期しないエラーが発生しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.IO.IOException: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.IO.IOException: 転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.Sockets.SocketException: An existing connection was forcibly closed by the remote host.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.Sockets.SocketException: 既存の接続がリモートホストによって強制的に切断されました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Run the following Windows PowerShell script on the development machine.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Service w3svc was not found on computer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">コンピューターでサービス w3svc が見つかりませんでした</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This error occurs only when you run load tests by using Visual Studio Online.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">このエラーは Visual Studio Online を使用して負荷テストを実行する場合にのみ発生します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">テストメソッド MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend が例外をスローしました。System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement'のタイプイニシャライザが例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.InvalidOperationException: Service w3svc was not found on computer '.'.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.InvalidOperationException: コンピューターでサービス w3svc が見つかりませんでした</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.ComponentModel.Win32Exception: 指定されたサービスは、インストールされたサービスに存在しません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>A hotfix is available that resolves this issue.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">この問題を解決する修正プログラムが利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>The Microsoft Knowledge Base (KB) number is 4095640.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The file IEDriverServer.exe does not exist</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">The file IEDriverServer.exe ファイルが存在しません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>This issue affects only single-user tests.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">この問題はシングル ユーザー テストにのみ影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>The file K:<ph id="ph1">\\</ph>perfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>SampleProject<ph id="ph4">\\</ph>TestResults<ph id="ph5">\\</ph>Admin501201994c<ph id="ph6">\_</ph>devae648d1909-1 2018-06-25 03<ph id="ph7">\_</ph>40<ph id="ph8">\_</ph>51<ph id="ph9">\\</ph>Out<ph id="ph10">\\</ph>Common<ph id="ph11">\\</ph>External<ph id="ph12">\\</ph>Selenium<ph id="ph13">\\</ph>IEDriverServer.exe does not exist.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ファイル K:<ph id="ph1">\\</ph>perfSDK<ph id="ph2">\\</ph>PerfSDKLocalDirectory<ph id="ph3">\\</ph>SampleProject<ph id="ph4">\\</ph>TestResults<ph id="ph5">\\</ph>Admin501201994c<ph id="ph6">\_</ph>devae648d1909-1 2018-06-25 03<ph id="ph7">\_</ph>40<ph id="ph8">\_</ph>51<ph id="ph9">\\</ph>Out<ph id="ph10">\\</ph>Common<ph id="ph11">\\</ph>External<ph id="ph12">\\</ph>Selenium<ph id="ph13">\\</ph>IEDriverServer.exe が存在しません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>The driver can be downloaded at <ph id="ph1">`http://selenium-release.storage.googleapis.com/index.html`</ph>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ドライバーは、 <ph id="ph1">`http://selenium-release.storage.googleapis.com/index.html`</ph>にてダウンロードできます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Copy the <bpt id="p1">**</bpt>Common<ph id="ph1">\\</ph>External<ph id="ph2">\\</ph>Selenium<ept id="p1">**</ept> folder under <bpt id="p2">**</bpt><ph id="ph3">\&lt;</ph>Your<ph id="ph4">\_</ph>PerfSDK<ph id="ph5">\_</ph>Folder<ph id="ph6">\&gt;</ph><ept id="p2">**</ept> to the <bpt id="p3">**</bpt><ph id="ph7">\&lt;</ph>Your<ph id="ph8">\_</ph>PerfSDK<ph id="ph9">\_</ph>Folder&gt;<ph id="ph10">\\</ph>SampleProject<ph id="ph11">\\</ph> PerfSDKSample<ph id="ph12">\\</ph>bin<ph id="ph13">\\</ph>Debug<ept id="p3">**</ept> folder.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p2">**</bpt><ph id="ph3">\&lt;</ph>ご利用の<ph id="ph4">\_</ph>PerfSDK<ph id="ph5">\_</ph>フォルダ<ph id="ph6">\&gt;</ph><ept id="p2">**</ept> 配下の <bpt id="p1">**</bpt>Common<ph id="ph1">\\</ph>External<ph id="ph2">\\</ph>Selenium<ept id="p1">**</ept> フォルダを <bpt id="p3">**</bpt><ph id="ph7">\&lt;</ph>ご利用の<ph id="ph8">\_</ph>PerfSDK<ph id="ph9">\_</ph>Folder&gt;<ph id="ph10">\\</ph>SampleProject<ph id="ph11">\\</ph> PerfSDKSample<ph id="ph12">\\</ph>bin<ph id="ph13">\\</ph>Debug<ept id="p3">**</ept> フォルダにコピーします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Failed finding the certificate for minting tokens by thumbprint: <ph id="ph1">\&lt;</ph>your certificate thumbprint<ph id="ph2">\&gt;</ph></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">拇印によるトークン作成用の証明書の検索に失敗しました <ph id="ph1">\&lt;</ph>ご利用の証明書の拇印<ph id="ph2">\&gt;</ph></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Error message and error stack trace<ept id="p1">](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)</ept></source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>エラーメッセージとエラースタックの追跡<ept id="p1">](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Make sure that you install the generated certificate on each AOS machine in your sandbox environment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">生成された証明書は、サンドボックス環境内の各AOSマシンにインストールしてください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The action you are trying to perform requires a connection to Visual Studio Team Services</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">実行しようとしているアクションには、 Visual Studio チームサービスへの接続が必要です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>This issue affects only multi-user tests.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">この問題はマルチ ユーザー テストにのみ影響します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Error message details<ept id="p1">](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)</ept></source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>エラーメッセージの詳細<ept id="p1">](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>When you connect to Azure DevOps, use the old URI format (<bpt id="p1">**</bpt><ph id="ph1">\&lt;</ph>Azure<ph id="ph2">\_</ph>DevOps<ph id="ph3">\_</ph>Account<ph id="ph4">\&gt;</ph>.visualstudio.com<ept id="p1">**</ept>) instead of <bpt id="p2">**</bpt>dev.azure.com/<ph id="ph5">\&lt;</ph>Azure<ph id="ph6">\_</ph>DevOps<ph id="ph7">\_</ph>Account<ph id="ph8">\&gt;</ph><ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Azure DevOps に接続するときは、 <bpt id="p2">**</bpt>dev.azure.com/<ph id="ph5">\&lt;</ph>Azure<ph id="ph6">\_</ph>DevOps<ph id="ph7">\_</ph>Account<ph id="ph8">\&gt;</ph><ept id="p2">**</ept> ではなく、古いURI形式 (<bpt id="p1">**</bpt><ph id="ph1">\&lt;</ph>Azure<ph id="ph2">\_</ph>DevOps<ph id="ph3">\_</ph>Account<ph id="ph4">\&gt;</ph>.visualstudio.com<ept id="p1">**</ept>) を使用します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Additionally, open Azure DevOps by using the old URI, and then select <bpt id="p1">**</bpt>Open in Visual Studio<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">古いURIを使用して Azure DevOps を開き、 <bpt id="p1">**</bpt>Visual Studioで開く<ept id="p1">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Could not load file or assembly 'aoskernel.dll' or one of its dependencies</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">ファイルまたはアセンブリ 'aoskernel.dll' 、あるいは依存関係を読み込みできませんでした</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>This error affects only multi-user tests.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">このエラーはマルチ ユーザー テストにのみ影響します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Error message, error stack trace, and debug trace<ept id="p1">](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)</ept></source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>エラーメッセージとエラースタックの追跡,デバッグの追跡<ept id="p1">](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Make sure that you're using Open Database Connectivity (ODBC) Driver 17 in an environment that has Platform update 20 or later.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">プラットフォーム更新プログラム20 またはそれ以降が稼働している環境で、Open Database Connectivity (ODBC) ドライバ17が使用されていることを確認して下さい。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>AzureActiveDirectoryConfiguration node is missing in CloudEnvironment.config</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Initialization method MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup threw exception.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup が例外をスローしました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Reflection.TargetInvocationException: 呼び出しのターゲットによって例外がスローされました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.MissingFieldException: AzureActiveDirectoryConfiguration node is missing in CloudEnvironment.config.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.MissingFieldException: CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Replace all instances of <bpt id="p1">**</bpt>"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"<ept id="p1">**</ept> with <bpt id="p2">**</bpt>"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>AuthenticatorConfigurationCollection<ept id="p3">**</ept> section of the CloudEnvironment.config file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"<ept id="p1">**</ept> のすべてのインスタンスを、CloudEnvironment.config ファイルの <bpt id="p3">**</bpt>AuthenticatorConfigurationCollection<ept id="p3">**</ept> セクションにある <bpt id="p2">**</bpt>"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"<ept id="p2">**</ept> で置き換えます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Multiple warning messages before and after multi-user testing that uses Azure DevOps</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Azure DevOpsを使用したマルチユーザーテストの開始前と後に複数の警告メッセージが表示される</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Error example</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エラーの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Sample load test status<ept id="p1">](./media/troubleshoot-perf-sdk-10.jpg)](./media/troubleshoot-perf-sdk-10.jpg)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>負荷テストステータスの例<ept id="p1">](./media/troubleshoot-perf-sdk-10.jpg)](./media/troubleshoot-perf-sdk-10.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Sample load test output<ept id="p1">](./media/troubleshoot-perf-sdk-11.jpg)](./media/troubleshoot-perf-sdk-11.jpg)</ept></source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>負荷テスト結果の例<ept id="p1">](./media/troubleshoot-perf-sdk-11.jpg)](./media/troubleshoot-perf-sdk-11.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Solution</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>There is no impact, and the messages can be ignored.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">影響はありません。メッセージを無視しても問題ありません。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>