<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="troubleshoot-on-prem.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>troubleshoot-on-prem.f1583c.2674b4c65d33369e0d4b96679c38bbffad3233fb.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2674b4c65d33369e0d4b96679c38bbffad3233fb</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>d1029dcf8d890278fb90abd9a96f70654586533b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/30/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\deployment\troubleshoot-on-prem.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Troubleshoot on-premises deployments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置のトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides troubleshooting information for on-premises deployments of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Troubleshoot on-premises deployments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置のトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides troubleshooting information for on-premises deployments of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Access Service Fabric Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer へのアクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can access Service Fabric Explorer in a web browser by using the default address, <ph id="ph1">`https://sf.d365ffo.onprem.contoso.com:19080`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer には、Web ブラウザーと既定のアドレス <ph id="ph1">`https://sf.d365ffo.onprem.contoso.com:19080`</ph> を使ってアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To verify the address, note the value that was used in the "Create DNS zones and add A records" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドレスを確認するには、環境の適切なセットアップおよび配置トピックの「DNS ゾーンの作成と A レコードの追加」セクションで使用されていた値をメモします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#createdns)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#createdns)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#createdns)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#createdns)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can access the site only if the client certificate is in cert:<ph id="ph1">\\</ph>CurrentUser<ph id="ph2">\\</ph>My on the machine that you're accessing the site on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント証明書が、サイトにアクセスするマシンの証明書、cert:<ph id="ph1">\\</ph>CurrentUser<ph id="ph2">\\</ph>My に含まれている場合のみ、サイトにアクセスできます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>(In Certificate Manger, go to <bpt id="p1">**</bpt>Certificates - Current User<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Personal<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Certificates<ept id="p3">**</ept>.) When you access the site, select the client certificate when you're prompted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(証明書マネージャーで、<bpt id="p1">**</bpt>証明書 - 現在のユーザー<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>個人<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>証明書<ept id="p3">**</ept>に移動します。) サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Monitor the deployment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置の監視</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Identify the primary orchestrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライマリ オーケストレータを識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To determine the machine that is the primary instance for stateful services such as a local agent, in Service Fabric Explorer, expand <bpt id="p1">**</bpt>Cluster<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Applications<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt><ph id="ph3">\&lt;</ph><bpt id="p4">*</bpt>intended application example<ept id="p4">*</ept><ph id="ph4">\&gt;</ph> LocalAgentType<ept id="p3">**</ept> <ph id="ph5">\&gt;</ph> <bpt id="p5">**</bpt>fabric:/LocalAgent/OrchestrationService<ept id="p5">**</ept> <ph id="ph6">\&gt;</ph> <bpt id="p6">**</bpt>(GUID)<ept id="p6">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer でローカル エージェントなどのステートフル サービスのプライマリ インスタンスであるマシンを判別するには、<bpt id="p1">**</bpt>クラスター<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt><ph id="ph3">\&lt;</ph><bpt id="p4">*</bpt>対象のアプリケーションの例<ept id="p4">*</ept><ph id="ph4">\&gt;</ph> LocalAgentType<ept id="p3">**</ept> <ph id="ph5">\&gt;</ph> <bpt id="p5">**</bpt>fabric:/LocalAgent/OrchestrationService<ept id="p5">**</ept> <ph id="ph6">\&gt;</ph> <bpt id="p6">**</bpt>(GUID)<ept id="p6">**</ept> を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The primary node is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライマリ ノードが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For stateless services or the remaining applications, you must check all the nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステートレス サービスまたは残りのアプリケーションについては、すべてのノードを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Note the following points:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のポイントに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>OrchestrationService orchestrates the deployment and servicing actions for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrchestrationService は、Finance and Operations の配置およびサービス アクションを調整します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>ArtifactsManager downloads files from Microsoft Azure cloud storage to the local agent file share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ArtifactsManager は、ファイルを Microsoft Azure クラウド ストレージからローカル エージェント ファイル共有にダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>It also unzips the files into the required format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを必要な形式にも解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Review the orchestrator event logs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ イベント ログを確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>From the primary OrchestrationService orchestrator machine, in Event Viewer, go to <bpt id="p1">**</bpt>Applications and Services Logs<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AX-LocalAgent<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアー内の プライマリ OrchestrationService オーケストレータ マシンから、 <bpt id="p1">**</bpt>アプリケーションとサービス ログ<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AX-LocalAgent<ept id="p4">**</ept> と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To view the full error message, you must select the <bpt id="p1">**</bpt>Details<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なエラー メッセージを表示するには、 <bpt id="p1">**</bpt>詳細<ept id="p1">**</ept> タブを選択してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The following modules must be installed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のモジュールがインストールされます:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Common</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共通</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>ReportingServices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReportingServices</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>FinancialReporting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinancialReporting</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The following commands must be run:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Setup<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セットアップ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Dvt<ept id="p1">**</ept> – This command runs a deployment verification test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dvt<ept id="p1">**</ept> – このコマンドは配置検証テストを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cleanup<ept id="p1">**</ept> – This command is used to service and delete an environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Cleanup<ept id="p1">**</ept> – このコマンドは環境のサービスと削除に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The following folders contain additional information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフォルダには、追加の情報が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>AX-SetupModuleEvents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX-SetupModuleEvents</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>AX-SetupInfrastructureEvents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX-SetupInfrastructureEvents</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>AX-BridgeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX-BridgeService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>To review Microsoft Dynamics entries in Event Viewer, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアーで Microsoft Dynamics エントリを確認するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In Event Viewer, right-click <bpt id="p1">**</bpt>Custom Views<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Create Custom View<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアーで <bpt id="p1">**</bpt>カスタム ビュー<ept id="p1">**</ept> を右クリックして、<bpt id="p2">**</bpt>カスタム ビューの作成<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Create custom view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム表示の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>In the <bpt id="p1">**</bpt>Event logs<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Dynamics<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>イベント ログ<ept id="p1">**</ept> フィールドで <bpt id="p2">**</bpt>Dynamics<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Select Dynamics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics の選択</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Also look at <bpt id="p1">**</bpt>Administrative Events<ept id="p1">**</ept> in <bpt id="p2">**</bpt>Custom Views<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p2">**</bpt>カスタム ビュー<ept id="p2">**</ept> で <bpt id="p1">**</bpt>管理イベント<ept id="p1">**</ept> も確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Service Fabric Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Note the state of the cluster, application, and nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスタ、アプリケーション、およびノードの状態に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>For information about how to access Service Fabric Explorer, see <bpt id="p1">[</bpt>Access Service Fabric Explorer<ept id="p1">](troubleshoot-on-prem.md#access-service-fabric-explorer)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer にアクセスする方法については、<bpt id="p1">[</bpt>Service Fabric Explorer にアクセスする<ept id="p1">](troubleshoot-on-prem.md#access-service-fabric-explorer)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Error: "Partition is below target replica or instance count"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエラーが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Partition is below target replica or instance count</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーティションがターゲット レプリカまたはインスタンス数を下回っています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This error isn't a root error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーはルート エラーではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>It indicates that the status of each node isn't ready.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ノードのステータスが準備できていないことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>For AXSFType (AOS), the status might still be <bpt id="p1">**</bpt>InBuild<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXSFType (AOS) では、ステータスがまだ <bpt id="p1">**</bpt>InBuild<ept id="p1">**</ept> である可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>On the machines that are related to the error message, use Event Viewer to view the latest activity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージに関連するコンピューターで、イベント ビューアーを使用して最新の活動を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>AXSFType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXSFType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If a status of <bpt id="p1">**</bpt>InBuild<ept id="p1">**</ept> is shown for AXSFType (AOS), review the DB Sync status and other events from Application Object Server (AOS) machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXSFType (AOS) に <bpt id="p1">**</bpt>InBuild<ept id="p1">**</ept> のステータスが表示される場合、DB Sync ステータスおよび Application Object Server (AOS) コンピューターからの他のイベントを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>To diagnose errors, use Event Viewer to review the following event logs:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーを診断するには、イベント ビューアーを使用して次のイベント ログを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Applications and Services Logs <ph id="ph1">\&gt;</ph> Microsoft <ph id="ph2">\&gt;</ph> Dynamics <ph id="ph3">\&gt;</ph> AX-DatabaseSynchronize</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションとサービス ログ <ph id="ph1">\&gt;</ph> Microsoft <ph id="ph2">\&gt;</ph> Dynamics <ph id="ph3">\&gt;</ph> AX-DatabaseSynchronize</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Custom Views <ph id="ph1">\&gt;</ph> Administrative Events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ビュー <ph id="ph1">\&gt;</ph> 管理イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Error: "'ExtractInstallerService failed to extract' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: "'ExtractInstallerService は抽出に失敗しました' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエラーが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>"ExtractInstallerService failed to extract" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"ExtractInstallerService は抽出に失敗しました" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>If you receive this error, download the latest version of <bpt id="p1">[</bpt>Azure Service Fabric<ept id="p1">](https://go.microsoft.com/fwlink/?LinkId=730690)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーが発生した場合は <bpt id="p1">[</bpt>Azure Service Fabric<ept id="p1">](https://go.microsoft.com/fwlink/?LinkId=730690)</ept> の最新バージョンをダウンロードしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Note that the user name and path in the error message vary, depending on your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージのユーザー名およびパスは、環境によって変化することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Service Fabric logs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric ログ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>You can find more details about Service Fabric applications in the log files at C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>OrchestratorMachineName<ph id="ph5">\&gt;</ph><ph id="ph6">\\</ph>Fabric<ph id="ph7">\\</ph>work<ph id="ph8">\\</ph>Applications<ph id="ph9">\\</ph>LocalAgentType<ph id="ph10">\_</ph>App<ph id="ph11">\&lt;</ph>N<ph id="ph12">\&gt;</ph><ph id="ph13">\\</ph>log.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric アプリケーションのさらなる詳細については、C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>OrchestratorMachineName<ph id="ph5">\&gt;</ph><ph id="ph6">\\</ph>Fabric<ph id="ph7">\\</ph>work<ph id="ph8">\\</ph>Applications<ph id="ph9">\\</ph>LocalAgentType<ph id="ph10">\_</ph>App<ph id="ph11">\&lt;</ph>N<ph id="ph12">\&gt;</ph><ph id="ph13">\\</ph>log のログ ファイルを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Lifecycle Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Note the current deployment status for the environment in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) で環境のに対する現在の配置ステータスに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>A time-out error occurs when a Service Fabric cluster is created</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric cluster の作成時にタイムアウト エラーが発生する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Run Test-D365FOConfiguration.ps1 as noted in the "Set up a standalone Service Fabric cluster" section of the appropriate setup and deployment topic for your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当するセットアップ トピックの "スタンドアロン <ph id="1">Service Fabric Cluster</ph> のセットアップ" セクションおよび環境の配置トピックに記載されているように Test-D365FOConfiguration.ps1 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Note any errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupsfcluster)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupsfcluster)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Be sure to complete these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順を必ず実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Verify that the Service Fabric Server client certificate exists in the LocalMachine store on all Service Fabric nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Verify that the Service Fabric Server certificate has the access control list (ACL) for Network Service on all Service Fabric nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Server 証明書にすべての Service Fabric ノード上にネットワーク サービス用アクセス制御リスト (ACL) が含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Review the antivirus exclusions that are noted in <bpt id="p1">[</bpt>Environment setup<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>環境設定<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)</ept> で記載されているウイルス対策の除外を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A time-out error occurs while you're waiting for Installer Service to be completed for machine x.x.x.x</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウト エラーが発生する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Only one node type is supported for each Internet Protocol (IP) address (that is, for each machine).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット プロトコル (IP) アドレスごとに (つまり、コンピューターごとに) 1 つのノード タイプがサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Check whether the nodes are being reused on the same machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノードが同じマシン上で再利用されているかどうかを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>For example, AOS and ORCH must not be on the same machine, and ConfigTemplate.xml must be correctly defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、AOS および ORCH は、同一のマシン上に存在してはならず、ConfigTemplate.xml が正しく定義されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Remove a specific application</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のアプリケーションを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>We recommend that you use LCS to remove or clean up deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置の削除またはクリーンアップに LCS を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, you can also use Service Fabric Explorer to remove an application as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、必要に応じて、アプリケーションを削除する Service Fabric Explorer を使用することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In Service Fabric Explorer, go to <bpt id="p1">**</bpt>Application node<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Applications<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>MonitoringAgentAppType-Agent<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric エクスプローラーで、<bpt id="p1">**</bpt>アプリケーション ノード<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>MonitoringAgentAppType-Agent<ept id="p3">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Select the ellipsis button (<bpt id="p1">**</bpt>...<ept id="p1">**</ept>) next to <bpt id="p2">**</bpt>fabric:/Agent-Monitoring<ept id="p2">**</ept>, and delete the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>ファブリック:/エージェント監視<ept id="p2">**</ept> の横にある省略記号ボタン (<bpt id="p1">**</bpt>...<ept id="p1">**</ept>) を選択し、アプリケーションを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Enter the full name of the application to confirm the deletion of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの完全な名前を入力して、アプリケーションの削除を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>You can also remove MonitoringAgentAppType-Agent by selecting the ellipsis button and then selecting <bpt id="p1">**</bpt>Unprovision Type<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、省略記号ボタンの選択および<bpt id="p1">**</bpt>非引当タイプ<ept id="p1">**</ept>の順に選択することにより、MonitoringAgentAppType-Agent を削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Enter the full name to confirm the removal of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの削除を確認するために、正式名称を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Remove all applications from Service Fabric</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric からすべてのアプリケーションを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The following script removes and unprovisions all Service Fabric applications except LocalAgent and the monitoring agent for LocalAgent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトは、LocalAgent および LocalAgent の監視エージェントを除く、すべての Service Fabric アプリケーションを削除してプロビジョニング解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>You must run this script on an orchestrator virtual machine (VM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ仮想マシン (VM) 上でこのスクリプトを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Remove Service Fabric</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric の削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>To completely remove the Service Fabric cluster, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスターを完全に削除するには、以下の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>If an error occurs, remove a specific node on the cluster by using the <bpt id="p1">**</bpt>CleanFabric.ps1<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが発生した場合は、<bpt id="p1">**</bpt>CleanFabric.ps1<ept id="p1">**</ept>コマンドを使用して、クラスタ内の特定のノードを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>You can find this command in C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft Service Fabric<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>fabric<ph id="ph5">\\</ph>fabric.code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft Service Fabric<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>fabric<ph id="ph5">\\</ph>fabric.code で検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Remove the <bpt id="p1">**</bpt>C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ept id="p1">**</ept> folder, if you're using the default location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の場所を使用している場合、<bpt id="p1">**</bpt>C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ept id="p1">**</ept> フォルダーを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Otherwise, remove the specified folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、指定したフォルダーを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>If you receive an "Access denied" error, restart Microsoft Windows PowerShell or the machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"アクセス拒否" エラーが発生した場合は、Microsoft Windows PowerShell を再起動するか、マシンを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Clean up an existing environment and redeploy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存環境のクリーンアップと再配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>To clean up an existing environment and redeploy, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の環境をクリーンアップして再配置するには、以下の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In LCS, open the project, and then, in the <bpt id="p1">**</bpt>Environments<ept id="p1">**</ept> section, delete the deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でプロジェクトを開き、<bpt id="p1">**</bpt>環境<ept id="p1">**</ept>セクションで展開を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The applications should start to disappear from Service Fabric Explorer in the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>This process will take one to two minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは 1、2 分かかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Access the orchestrator machine that contains LocalAgentCLI.exe, and follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LocalAgentCLI.exe を含むオーケストレーター マシンにアクセスし、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Run the local agent cleanup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント クリーンアップを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Remove Service Fabric.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>If any nodes fail, run the <bpt id="p1">**</bpt>CleanFabric.ps1<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノードが失敗した場合、<bpt id="p1">**</bpt>CleanFabric.ps1<ept id="p1">**</ept> コマンドを実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>You can find this command in C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft Service Fabric<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>fabric<ph id="ph5">\\</ph>fabric.code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft Service Fabric<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>fabric<ph id="ph5">\\</ph>fabric.code で検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Remove the <bpt id="p1">**</bpt>C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph><ept id="p1">**</ept> folder on all Service Fabric nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての Service Fabric ノードの <bpt id="p1">**</bpt>C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph><ept id="p1">**</ept> フォルダーを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>If you receive an "Access denied" error, restart the machine, and try again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"アクセス拒否" エラーが発生した場合は、マシンを再起動してからもう一度実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Remove or update certificates as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて証明書を削除または更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Remove old certificates from all AOS, BI, ORCH, and DC nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>The certificates exist in the following certificate stores: Cert:<ph id="ph1">\\</ph>CurrentUser<ph id="ph2">\\</ph>My<ph id="ph3">\\</ph>, Cert:<ph id="ph4">\\</ph>LocalMachine<ph id="ph5">\\</ph>My, and Cert:<ph id="ph6">\\</ph>LocalMachine<ph id="ph7">\\</ph>Root.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書は、次の証明書ストアに存在します: Cert:<ph id="ph1">\\</ph>CurrentUser<ph id="ph2">\\</ph>My<ph id="ph3">\\</ph>、Cert:<ph id="ph4">\\</ph>LocalMachine<ph id="ph5">\\</ph>My, and Cert:<ph id="ph6">\\</ph>LocalMachine<ph id="ph7">\\</ph>Root。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If the setup of Microsoft SQL Server will be modified, remove the SQL Server certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server の設定が変更される場合は、SQL Server 証明書を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If the settings for Active Directory Federation Services (AD FS) will be modified, remove the AD FS certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory フェデレーション サービス (AD FS) の設定が変更される場合は、AD FS 証明書を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Update the following configuration files as required:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、次の構成ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>ConfigTemplate.xml</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ConfigTemplate.xml</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>ClusterConfig.json</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ClusterConfig.json</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>For information about how to correctly fill in the fields in the templates, see the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートのフィールドに正しく入力する方法については、ご使用の環境に適した設定と配置のトピックを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>In LCS, open the project, and update the LCS on-premises connector as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でプロジェクトを開き、必要に応じて LCS のオンプレミス コネクタを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Re-create the LCS on-premises connector for the environment, or edit the settings of an existing connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の LCS オンプレミス コネクタを再作成するか、または既存のコネクタの設定を編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>To obtain easy-to-copy values for LCS, use the .<ph id="ph1">\\</ph>Get-AgentConfiguration.ps1 script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の値を簡単にコピーするには、.<ph id="ph1">\\</ph>Get-AgentConfiguration.ps1 script を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Download the latest local agent configuration, localagent-config.json.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新のローカル エージェント コンフィギュレーション、localagent config.json をダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Deploy again by following the instructions in the appropriate setup and deployment topic for the environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境に適したセットアップと展開のトピックで次の指示に従って、再度展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Find the local agent values that are used</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用するローカル エージェント値の検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>You can find local agent values in Service Fabric Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer でローカル エージェント値を見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Go to <bpt id="p1">**</bpt>Cluster<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Applications<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>LocalAgentType<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>fabric:/LocalAgent<ept id="p4">**</ept>, and then select <bpt id="p5">**</bpt>Details<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラスター<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>LocalAgentType<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>fabric:/LocalAgent<ept id="p4">**</ept> に移動して <bpt id="p5">**</bpt>詳細<ept id="p5">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Alternatively, run the following Windows PowerShell command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、次の Windows PowerShell コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Install, upgrade, or uninstall a local agent</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ローカル エージェントのインストール、アップグレード、アンインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>For information about how to update the local agent, see <bpt id="p1">[</bpt>Update the local agent<ept id="p1">](../lifecycle-services/update-local-agent.md)</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ローカルエージェントを更新する方法については、 <bpt id="p1">[</bpt>ローカルエージェントを更新する<ept id="p1">](../lifecycle-services/update-local-agent.md)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>You can also use the following upgrade and uninstallation commands:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">また、以下のアップグレードおよびアンインストール コマンドを使用することができます:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The <bpt id="p1">**</bpt>Cleanup<ept id="p1">**</ept> command doesn't remove any files that were put in the file share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クリーンアップ<ept id="p1">**</ept> コマンドはファイル共有に配置された一切のファイルを削除しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The file share can be reused.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル共有は再利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>An error occurs when local agent services are started</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント サービスを開始される際にエラーが発生</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>When local agent services are started, you might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント サービスが開始されると、次のエラーが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Could not load file or assembly 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル、アセンブリ 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35'、もしくはその依存関係の 1 つをロードできませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>This error means that strong name verification is turned on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーは厳密な名前検証が有効になっていることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>You can turn off this verification by using Configure-PreReqs.ps1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Configure-PreReqs.ps1 を使用して、この確認をオフにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>To validate that strong name verification is no longer turned on, run Test-D365FOConfiguration.ps1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">厳密な名前検証がもう有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>A "Validation in progress" message is shown for several minutes in LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「検証が進行中」のメッセージが LCS に数分表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Follow these steps to troubleshoot general issues with local agent validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Run <bpt id="p1">**</bpt>Configure-PreReqs.ps1<ept id="p1">**</ept> on all orchestrator machines to configure the machines correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で <bpt id="p1">**</bpt>Configure-PreReqs.ps1<ept id="p1">**</ept> を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Verify that the Test-D365FOConfiguration.ps1 script passes on all the orchestrator machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Test-D365FOConfiguration.ps1 スクリプトがすべてのオーケストレータ マシンで通ることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Verify that the installation of LocalAgentCLI.exe is successfully completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LocalAgentCLI.exe のインストールが正常に完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>In Service Fabric Explorer, verify that all the applications are healthy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer で、すべてのアプリケーションが正常であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If the applications aren't healthy, find the primary node for the service that is failing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションが正常でない場合は、障害が発生しているサービスのプライマリ ノードを探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In Event Viewer, look for events in the following locations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアーでは、次の場所でのイベントを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Custom Views <ph id="ph1">\&gt;</ph> Administrative Events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ビュー <ph id="ph1">\&gt;</ph> 管理イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Applications and Services Log <ph id="ph1">\&gt;</ph> Microsoft <ph id="ph2">\&gt;</ph> Dynamics <ph id="ph3">\&gt;</ph> AX-LocalAgent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションとサービス ログ <ph id="ph1">\&gt;</ph> Microsoft <ph id="ph2">\&gt;</ph> Dynamics <ph id="ph3">\&gt;</ph> AX-LocalAgent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Local agent errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Issue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept> You might receive the following errors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept> 次のエラーが表示される場合があります:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Unable to process commands</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドを処理できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Unable to get the channel information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル情報を取得できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>RunAsync failed due to an unhandled exception causing the host process to crash: System.ArgumentNullException: Value cannot be null.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Parameter name: certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター名: 証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> These errors can occur because the certificate that is specified for the OnPremLocalAgent certificate either isn't valid or isn't correctly configured for the tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> これらのエラーは OnPremLocalAgent 証明書に指定された証明書が有効でないか、またはテナントに対して正しく構成されていないために発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> Follow these steps to resolve the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> エラーを解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Run <bpt id="p1">**</bpt>Test-D365FOConfiguration.ps1<ept id="p1">**</ept> on all orchestrator nodes to make sure that all checks pass.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのオーケストレータ ノードで <bpt id="p1">**</bpt>Test-D365FOConfiguration.ps1<ept id="p1">**</ept> を実行し、すべてのチェックに合格することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Verify that the certificate that is specified in the local agent configuration is correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Make sure that the thumbprint that you specify in LCS and in the ConfigTemplate.xml file has no special characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS および ConfigTemplate.xml ファイルで指定する拇印に特殊文字がないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>The certificate should be the same certificate that is specified in the following section in infrastructure<ph id="ph1">\\</ph>ConfigTemplate.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書は、infrastructure<ph id="ph1">\\</ph>ConfigTemplate.xml の次のセクションで指定されているものと同じ証明書である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Make sure that the same certificate that is specified in the local agent configuration in LCS was used to complete the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS のローカル エージェント コンフィギュレーションで指定される同じ証明書が、環境に対する適切な設定および配置トピックの「テナント用 LCS 接続の構成」セクションで手順の完了に使用されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configurelcs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configurelcs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#configurelcs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#configurelcs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Uninstall the local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントをアンインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Specify the correct certificate in the local agent configuration, and download the configuration file again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Install the local agent again by using the new configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept> During servicing, you receive an "Unable to download asset" error, and the details state, "The credentials supplied to the package were not recognized."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept> サービス中に "資産をダウンロードできません" というエラーが表示され、詳細に "パッケージに提供された資格情報が認識されません" と表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> The ACL wasn't correctly defined on certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> ACL が証明書で正しく定義されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Check whether ACL was removed from client certificate on orchestrator machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ マシンのクライアント証明書から ACL が削除されたかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Run the .\Test-D365FOConfiguration.ps1 script on orchestrator machines, and verify the ACL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ マシンの .\Test-D365FOConfiguration.ps1 スクリプトを実行し、ACL を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>To resolve the error, run the .\Set-CertificateAcls.ps1 script to reset the ACLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーを解決するには、.\Set-CertificateAcls.ps1 スクリプトを実行して ACL をリセットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Access to the path '<ph id="ph1">\\</ph>...<ph id="ph2">\\</ph>agent<ph id="ph3">\\</ph>assets<ph id="ph4">\\</ph>StandAloneSetup-76308-1.zip' is denied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パス '<ph id="ph1">\\</ph>...<ph id="ph2">\\</ph>agent<ph id="ph3">\\</ph>assets<ph id="ph4">\\</ph>StandAloneSetup-76308-1.zip' へアクセスすることは、拒否されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> The file share that is specified in the local agent configuration isn't valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> Follow these steps to resolve the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> エラーを解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Verify that the specified share exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した共有が存在することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Verify that the local agent user has full permission on the share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The local agent user is the Domain Name System (DNS) name that is specified in the following section in ConfigTemplate.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定されるドメイン ネーム システム (DNS) 名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Make sure that the "Set up file storage" section of the appropriate setup and deployment topic for your environment is completed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックが完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupfile)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupfile)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupfile)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupfile)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Uninstall the local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントをアンインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Specify the correct file share in the local agent configuration, and download the configuration file again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Install the local agent again by using the new configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept> When you do a servicing operation, you receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept> サービス操作を行うと次のエラーが表示されます:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Unable to get extract setup folder for command</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドの抽出セットアップ フォルダーを取得できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> The file share has been removed or changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> そのファイル共有は削除または変更されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> To see what the file share is set to, open Microsoft SQL Server Management Studio, and run the following query on the orchestrator database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>手順:<ept id="p1">**</ept> ファイル共有の設定内容を確認するには、Microsoft SQL Server Management Studio を開いてオーケストレータ データベースで次のクエリを実行します:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Login failed for user 'D365<ph id="ph1">\\</ph>svc-LocalAgent$'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー 'D365<ph id="ph1">\\</ph>svc-LocalAgent$' へのログインが失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Reason: Could not find a login matching the name provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">理由: 指定した名前に一致するログインが見つかりませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source><ph id="ph1">\[</ph>CLIENT: 10.0.2.23<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>CLIENT: 10.0.2.23<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> The local agent user can't connect to the orchestrator database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>This issue can occur because users have been deleted and then re-created in Active Directory Domain Services (AD DS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが削除され、Active Directory ドメイン サービス (AD DS) に再作成されているために、この問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Therefore, the security identifier (SID) of the user has changed, and any access that was given to the user for the SQL Server instance or the database no longer works.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ユーザーのセキュリティ識別子 (SID) が変更され、SQL Server インスタンスまたはデータベースのユーザーに与えられたアクセスは機能しなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> Follow these steps to resolve the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> エラーを解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Run the following script on the SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server インスタンスで次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>This script creates an empty orchestrator database, if an empty database doesn't already exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、空のデータベースがまだ存在していない場合に、空のオーケストレータ データベースを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>It then adds the local agent user to the database and gives it db<ph id="ph1">\_</ph>owner permission.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント ユーザーをデータベースに追加し、データベース<ph id="ph1">\_</ph>アクセス許可の所有者に渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>After the correct permissions are provided, the application should automatically go to a healthy state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なアクセス許可が付与された後、アプリケーションは自動的に正常な状態になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>If any settings, such as the fully qualified domain name (FQDN) of the SQL Server instance, the database name, or the local agent user, were provided incorrectly in LCS, change the settings, and then reinstall the local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server インスタンスの完全修飾ドメイン名 (FQDN)、データベース名、ローカル エージェント ユーザーなどの設定が LCS で間違って提供された場合は、設定を変更し、ローカル エージェントを再インストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>If the preceding steps don't resolve the error, manually remove the local agent user from the SQL Server instance and the database, and then rerun the Initialize-Database script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の手順でエラーが解決しない場合は、SQL Server インスタンスとデータベースからローカル エージェント ユーザーを手動で削除し、Initialize-Database スクリプトを再実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>If you re-create a user in AD DS, remember that the SID will change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD DS でユーザーを再作成する場合、SID が変更されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>In this case, remove the previous SID for the user, and add a new SID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、ユーザーの以前の SID を削除し、新しい SID を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Unable to migrate database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを移行できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Verify that you have access to the SQL Server listener.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server リスナーへのアクセスがあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>If you're doing testing, you can start over and use an empty orchestrator database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストをしている場合は、最初からやり直して空のオーケストレータ データベースを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Issue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題点</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>When you performing the <bpt id="p1">[</bpt>Configure the databases<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb)</ept> procedure, if the SQL Server instance is a named instance, use the <bpt id="p2">**</bpt>-DatabaseServer <ph id="ph1">\[</ph>FQDN/Instancename<ph id="ph2">\]</ph><ept id="p2">**</ept> parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>データベースを構成する<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb)</ept> プロシージャを実行するときに SQL Server インスタンスが名前付きインスタンスの場合は、<bpt id="p2">**</bpt>-DatabaseServer <ph id="ph1">\[</ph>FQDN/Instancename<ph id="ph2">\]</ph><ept id="p2">**</ept> パラメーターを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Issue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題点</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>The local agent user can't connect to the SQL Server instance or the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェント ユーザーは、SQL Server インスタンスまたはデータベースに接続できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> Follow these steps to resolve the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> エラーを解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Delete the svc-LocalAgent user from the SQL Server primary node databases, and then remove the login from both servers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Run the following scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>These scripts don't work when an <bpt id="p1">**</bpt>always-on<ept id="p1">**</ept> setup is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのスクリプトは、<bpt id="p1">**</bpt>常時オン<ept id="p1">**</ept>に設定されているときは機能しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>The database must first be created in the primary node and then replicated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースは最初にプライマリ ノードに作成されてから複製される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>RunAsync failed due to an unhandled exception causing the host process to crash: System.Net.Http.HttpRequestException: An error occurred while sending the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.WebException: The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1"> ---</ph><ph id="ph2">\&gt;</ph> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> The local agent machines can't connect to lcsapi.lcs.dynamics.com.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> ローカル エージェント マシンは lcsapi.lcs.dynamics.com に接続できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Review the AX-BridgeService event log for "The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'」に対する AX-BridgeService イベント ログを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> Follow these steps to resolve the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> エラーを解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Run <bpt id="p1">**</bpt>psping lcsapi.lcs.dynamics.com:80<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>psping lcsapi.lcs.dynamics.com:80<ept id="p1">**</ept> を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>If you don't receive a response from the preceding command, contact the IT department at your organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前述のコマンドから応答を受信しない場合は、組織の IT 部門に問い合わせます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Either the firewall is blocking access to lcsapi, or proxy issues are occurring.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイアウォールが lcsapi へのアクセスをブロックしているか、もしくはプロキシの問題が発生しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Restart applications (such as AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション (AOS など) を再起動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>In Service Fabric, expand <bpt id="p1">**</bpt>Nodes<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AOSx<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>fabric:/AXSF<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AXSF<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>Code Packages<ept id="p5">**</ept> <ph id="ph5">\&gt;</ph> <bpt id="p6">**</bpt>Code<ept id="p6">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric で、<bpt id="p1">**</bpt>ノード<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AOSx<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>fabric:/AXSF<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AXSF<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>コード パッケージ<ept id="p5">**</ept> <ph id="ph5">\&gt;</ph> <bpt id="p6">**</bpt>コード<ept id="p6">**</ept>の順に展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Select the ellipsis button (<bpt id="p1">**</bpt>...<ept id="p1">**</ept>), and then select <bpt id="p2">**</bpt>Restart<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">省略記号ボタン (<bpt id="p1">**</bpt>...<ept id="p1">**</ept>) を選択し、<bpt id="p2">**</bpt>再起動<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>When you're prompted, enter the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">求められたらコードを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Upgrade Service Fabric</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Service Fabric Explorer will show a message that resembles the following message:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer は次のようなメッセージを表示します:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Unhealthy event: SourceId='System.UpgradeOrchestrationService', Property='ClusterVersionSupport', HealthState='Warning', ConsiderWarningAsError=false.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題のあるイベント: SourceId=「System.UpgradeOrchestrationService」、プロパティ =「ClusterVersionSupport」、HealthState=「警告」、ConsiderWarningAsError=false。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>The current cluster version 6.1.467.9494 support ends 5/30/2018 12:00:00 AM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のクラスタ バージョン 6.1.467.9494 のサポートは、5/30/2018 12:00:00 AM に終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Please view available upgrades using Get-ServiceFabricRegisteredClusterCodeVersion and upgrade using Start-ServiceFabricClusterUpgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Get-ServiceFabricRegisteredClusterCodeVersion を使用して利用可能なアップグレードを表示し、Start-ServiceFabricClusterUpgrade を使用してアップグレードしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Because the minimum requirement is one Microsoft SQL Server Reporting Services (SSRS) node and one Management Reporter node, you must pass in a parameter to skip PreUpgradeSafetyCheck.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最小要件が 1 つの Microsoft SQL Server Reporting Services (SSRS) ノードと 1 つの Management Reporter ノードであるため、PreUpgradeSafetyCheck をスキップするパラメータを渡す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Follow these steps to upgrade Service Fabric in Windows PowerShell.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows PowerShell で Service Fabric をアップグレードするにはこれらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Connect to the Service Fabric cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Service Fabric Cluster</ph> に接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>In the following command, replace <bpt id="p1">**</bpt>123<ept id="p1">**</ept> with the server/star thumbprint, and use the appropriate IP address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドで <bpt id="p1">**</bpt>123<ept id="p1">**</ept> をサーバー / スター拇印に置き換えて、適切な IP アドレスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Get the latest version that was downloaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロードされた最新バージョンを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Start the upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>For <bpt id="p1">**</bpt>-CodePackageVersion<ept id="p1">**</ept>, enter the latest version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>-CodePackageVersion<ept id="p1">**</ept> には、最新バージョンを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source><bpt id="p1">**</bpt>-UpgradeReplicaSetCheckTimeout<ept id="p1">**</ept> is used to skip PreUpgradeSafetyCheck for SSRS and Management Reporter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>-UpgradeReplicaSetCheckTimeout<ept id="p1">**</ept> は SSRS と Management Reporter の PreUpgradeSafetyCheck をスキップするために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>For more information, see <bpt id="p1">[</bpt>Service Fabric service upgrade not working<ept id="p1">](https://github.com/Azure/service-fabric-issues/issues/595)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Service Fabric サービスのアップグレードが動作しない<ept id="p1">](https://github.com/Azure/service-fabric-issues/issues/595)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>You might also want to use <bpt id="p1">**</bpt>-UpgradeDomainTimeoutSec 600 -UpgradeTimeoutSec 1800<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>UpgradeDomainTimeoutSec 600 UpgradeTimeoutSec 1800<ept id="p1">**</ept> を使用することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>For more information, see <bpt id="p1">[</bpt>Application upgrade parameters<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>アプリケーション アップグレード パラメーター<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Get the upgrade status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードの状態を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>For more information, see <bpt id="p1">[</bpt>Troubleshoot application upgrades<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>アプリケーション アップグレードのトラブルシューティング<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>To learn when a new Service Fabric release comes out, see the <bpt id="p1">[</bpt>Azure Service Fabric team blog<ept id="p1">](https://blogs.msdn.microsoft.com/azureservicefabric/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Service Fabric リリースの時期については、<bpt id="p1">[</bpt>Azure Service Fabric チームのブログ<ept id="p1">](https://blogs.msdn.microsoft.com/azureservicefabric/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>If you receive a warning in Service Fabric Explorer after you upgrade, make a note of the node, and then restart by expanding <bpt id="p1">**</bpt>Nodes<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AOSx<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>fabric:/AXSF<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AXSF<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>Code Packages<ept id="p5">**</ept> <ph id="ph5">\&gt;</ph> <bpt id="p6">**</bpt>Code<ept id="p6">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード後に Service Fabric Explorer で警告が表示された場合は、ノードを記録して、<bpt id="p1">**</bpt>ノード<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AOSx<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>fabric:/AXSF<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AXSF<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>コード パッケージ<ept id="p5">**</ept> <ph id="ph5">\&gt;</ph> <bpt id="p6">**</bpt>コード<ept id="p6">**</ept> を展開して再起動してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Select the ellipsis button (<bpt id="p1">**</bpt>...<ept id="p1">**</ept>), and then select <bpt id="p2">**</bpt>Restart<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">省略記号ボタン (<bpt id="p1">**</bpt>...<ept id="p1">**</ept>) を選択し、<bpt id="p2">**</bpt>再起動<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Error: "Unable to load DLL 'FabricClient.dll'"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「DLL 'FabricClient.dll' を読み込むことができません」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>If you receive an error that states, "Unable to load DLL 'FabricClient.dll'," close and restart Windows PowerShell.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"DLL 'FabricClient.dll' をロードできません" というエラーが表示された場合は、Windows PowerShellを 閉じて再起動してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>If the error persists, restart the machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが引き続き発生する場合は、コンピューターを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>What cluster ID should be used in the agent configuration?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エージェント コンフィギュレーションでどのようなクラスター ID を使用する必要がありますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>The cluster ID can be any globally unique identifier (GUID).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスタ ID は、任意のグローバル一意識別子 (GUID) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>This GUID is used for tracking purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この GUID は、追跡目的で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Encryption errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Some examples of encryption errors include "AXBootstrapperAppType," "Bootstrapper," "AXDiagnostics," "RTGatewayAppType," "Gateway potential failure related," and "Microsoft.D365.Gateways.ClusterGateway.exe."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化エラーの例は "AXBootstrapperAppType"、"Bootstrapper"、"AXDiagnostics"、"RTGatewayAppType"、"ゲートウェイの潜在的なエラー関連"、 "Microsoft.D365.Gateways.ClusterGateway.exe" を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>You might receive one of these errors if the data encipherment certificate that was used to encrypt the AOS account password wasn't installed on the machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS アカウント パスワードを暗号化するために使用されたデータ暗号化証明書がマシンにインストールされていない場合、これらのエラーのいずれかが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>This certificate might be in the certificates (local computer), or the provider type might be incorrect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書が証明書 (ローカル コンピューター) に含まれているか、プロバイダーの種類が正しくない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>To resolve the error, validate the credentials.json file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーを解決するには、credentials.json ファイルを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Verify that the text is correctly decrypted by entering the following command (on AOS1).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを (AOS1 上で) 入力することにより、テキストが正しく復号化されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>This error can also occur if the <bpt id="p1">**</bpt>''<ept id="p1">**</ept> parameter isn't defined in the ApplicationManifest file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーも、<bpt id="p1">**</bpt>''<ept id="p1">**</ept> パラメーターが ApplicationManifest ファイルで定義されていない場合にも発生させることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>To determine whether this parameter is defined, in Event Viewer, go to <bpt id="p1">**</bpt>Custom Views<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Administrative Events<ept id="p2">**</ept>, and verify the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアーで、このパラメータが定義されているどうかを確認するには、<bpt id="p1">**</bpt>カスタム ビュー<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>管理イベント<ept id="p2">**</ept>の順に移動し、次の情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>The encrypt credentials for the credentials.json file have the correct layout/structure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Credentials.json ファイルの資格情報の暗号化には、正しいレイアウト/構造があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>For more information, see the "Encrypt credentials" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、ご使用の環境に適した設定および配置のトピックの「資格情報の暗号化」のセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#encryptcred)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#encryptcred)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#encryptcred)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#encryptcred)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>A closing quotation mark appears at the end of the line or on the next line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">決算引用符が線の終わりまたは次の線に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>In Event Viewer, under <bpt id="p1">**</bpt>Custom Views<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Administrative Events<ept id="p2">**</ept>, note any errors in the <bpt id="p3">**</bpt>Microsoft-Service Fabric<ept id="p3">**</ept> source category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアーの <bpt id="p1">**</bpt>カスタム ビュー<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>管理イベント<ept id="p2">**</ept> で、<bpt id="p3">**</bpt>Microsoft-Service Fabric<ept id="p3">**</ept> ソース カテゴリのエラーに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Properties to create a DataEncryption certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEncryption 証明書を作成するためのプロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Use the following properties to create the DataEncryption certificate:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEncryption 証明書を作成するのにには、次のプロパティを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source><bpt id="p1">**</bpt>Is self-signed certificate<ept id="p1">**</ept> – Enable this parameter only when you're using self-signed certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>自己署名証明書<ept id="p1">**</ept> – このパラメータは、自己署名証明書を使用する場合にのみ有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source><bpt id="p1">**</bpt>Certificate purposes<ept id="p1">**</ept> – Enable all purposes for this certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>証明書の目的<ept id="p1">**</ept> – この証明書のすべての目的を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source><bpt id="p1">**</bpt>Signature algorithm<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>sha256RSA<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>署名アルゴリズム<ept id="p1">**</ept> – <bpt id="p2">**</bpt>sha256RSA<ept id="p2">**</ept> を指定してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source><bpt id="p1">**</bpt>Signature hash algorithm<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>sha256<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>署名ハッシュ アルゴリズム<ept id="p1">**</ept> – <bpt id="p2">**</bpt>sha256<ept id="p2">**</ept> を指定してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source><bpt id="p1">**</bpt>Issuer<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>CN = DataEncryptionCertificate<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>発行者<ept id="p1">**</ept> – 指定 <bpt id="p2">**</bpt>CN = DataEncryptionCertificate<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source><bpt id="p1">**</bpt>Public Key<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>RSA (2048 bits)<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>公開キー<ept id="p1">**</ept> – <bpt id="p2">**</bpt>RSA (2048 ビット)<ept id="p2">**</ept> を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source><bpt id="p1">**</bpt>Thumbprint algorithm<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>sha1<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Thumbprint アルゴリズム<ept id="p1">**</ept> – <bpt id="p2">**</bpt>sha1<ept id="p2">**</ept> を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Don't use self-signed certificates in production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境では、自己署名証明書を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Instead, use certificates that are issued by certificate authorities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、証明書機関によって発行された証明書を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>The certificate and private key that should be used for decryption can't be found (0x8009200C)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号の解読に使用すべき証明書と秘密キーを見つけることができません (0x8009200C)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>If you're missing a certificate and ACL, or if you have the wrong thumbprint entry, check for special characters, and look for thumbprints in C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>AOSMachineName<ph id="ph5">\&gt;</ph><ph id="ph6">\\</ph>Fabric<ph id="ph7">\\</ph>work<ph id="ph8">\\</ph>Applications<ph id="ph9">\\</ph>AXBootstrapperAppType<ph id="ph10">\_</ph>App<ph id="ph11">\&lt;</ph>N<ph id="ph12">\&gt;</ph><ph id="ph13">\\</ph>log<ph id="ph14">\\</ph>ConfigureCertificates-<ph id="ph15">\&lt;</ph>timestamp<ph id="ph16">\&gt;</ph>.txt.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書と ACL がない、または間違った拇印の入力がある場合は、特殊文字をチェックし、C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph><ph id="ph4">\&lt;</ph>AOSMachineName<ph id="ph5">\&gt;</ph><ph id="ph6">\\</ph>Fabric<ph id="ph7">\\</ph>work<ph id="ph8">\\</ph>Applications<ph id="ph9">\\</ph>AXBootstrapperAppType<ph id="ph10">\_</ph>App<ph id="ph11">\&lt;</ph>N<ph id="ph12">\&gt;</ph><ph id="ph13">\\</ph>log<ph id="ph14">\\</ph>ConfigureCertificates-<ph id="ph15">\&lt;</ph>timestamp<ph id="ph16">\&gt;</ph>.txt で拇印を探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>You can also validate the encrypted text by using the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを使用して暗号化されたテキストを検証することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>If you receive the message, "Cannot find the certificate and private key to use for decryption," verify the axdataenciphermentcert and svc-AXSF$ AXServiceUser ACLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACLs を確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>If the credentials.json file has changed, delete and redeploy the environment from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">credentials.json ファイルが変更された場合は、LCS から環境を削除して再配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>If none of the preceding solutions work, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のソリューションのいずれも機能しない場合は、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Verify that the domain name and Active Directory account names that are specified in the ConfigTemplate.xml file are correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ConfigTemplate.xml ファイルで指定されたドメイン名と Active Directory アカウント名が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Verify that the thumbprints that are specified in the ConfigTemplate.xml file are correct if the certificate wasn't generated by using the scripts that are provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml ファイルで指定された拇印が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Verify that the certificate thumbprints that are specified in LCS are correct, and that they match the thumbprints that are specified in ConfigTemplate.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと拇印が一致することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Make sure that there are no special characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特殊文字がないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>You can run <bpt id="p1">**</bpt>.<ph id="ph1">\\</ph>Get-DeploymentSettings.ps1<ept id="p1">**</ept> to obtain the thumbprints in an easy-to-copy manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>.<ph id="ph1">\\</ph>Get-DeploymentSettings.ps1<ept id="p1">**</ept> を実行して、コピーしやすい方法で拇印を取得することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>If the certificates aren't self-generated, make sure that the provider names match for the following certificate types:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書が自己生成されない場合、プロバイダー名が次の証明書タイプと一致することを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source><bpt id="p1">**</bpt>ServiceFabricEncryption type:<ept id="p1">**</ept> Microsoft Enhanced Cryptographic Provider v1.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ServiceFabricEncryption type:<ept id="p1">**</ept>Microsoft Enhanced Cryptographic Provider v1.0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source><bpt id="p1">**</bpt>All other certificate types:<ept id="p1">**</ept> Microsoft Enhanced RSA and AES Cryptographic Provider</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>その他のすべての証明書タイプ:<ept id="p1">**</ept> Microsoft の拡張された RSA および AES 暗号化プロバイダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Verify that the Set-CertificateAcls.ps1 and Test-D365FOConfiguration.ps1 scripts were successfully run on all Service Fabric machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Set-CertificateAcls.ps1 および Test-D365FOConfiguration.ps1 スクリプトがすべての Service Fabric マシンで正常に実行されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Verify that the credentials.json file exists, and that the entries are decrypted to correct values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Credentials.json ファイルが存在し、エントリが適切な値に復号化されるよう確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>On one of the AOS machines, run the following command to verify that the data encryption certificate is correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS マシンのいずれかで、データの暗号化証明書が正しいことを確認する次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>If any of the certificates must be changed, or if the configuration was incorrect, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかの証明書を変更する必要がある場合、もしくは構成が正しくない場合は、次の手順を実行してください:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Edit the <bpt id="p1">**</bpt>ConfigTemplate.xml<ept id="p1">**</ept> file so that it has the correct values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ConfigTemplate.xml<ept id="p1">**</ept> ファイルを編集して、正しい値が出るようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Run all the setup scripts and the <bpt id="p1">**</bpt>Test-D365FOConfiguration<ept id="p1">**</ept> script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのセットアップ スクリプトと <bpt id="p1">**</bpt>Test-D365FOConfiguration<ept id="p1">**</ept> スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>In LCS, reconfigure the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で環境を再構成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Management Reporter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Additional logging can be done by registering providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のログは、プロバイダーを登録することで実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>Download <bpt id="p1">[</bpt>ETWManifest.zip<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=864672)</ept> to the <bpt id="p2">**</bpt>primary<ept id="p2">**</ept> orchestrator machine, and then run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ETWManifest.zip<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=864672)</ept> を <bpt id="p2">**</bpt>プライマリ<ept id="p2">**</ept>オーケストレータ マシン にダウンロードし、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>To determine which machine is the primary instance, in Service Fabric Explorer, expand <bpt id="p1">**</bpt>Cluster<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Applications<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>LocalAgentType<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>fabric:/LocalAgent/OrchestrationService<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>(GUID)<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライマリ インスタンスであるマシンを判別するには、Service Fabric Explorerで、<bpt id="p1">**</bpt>クラスター<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>LocalAgentType<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>fabric:/LocalAgent/OrchestrationService<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>(GUID)<ept id="p5">**</ept> の順に展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>If results in Event Viewer don't appear correct (for example, if words are truncated), get the latest manifest and .dll files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアーの結果が正しく表示されない場合 (たとえば、単語が切り詰められた場合など)、最新のマニフェストおよび .dll ファイルを取得してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>To get the latest manifest and .dll files, go to the WP folder in the agent file share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新のマニフェストと .dll ファイルを取得するには、エージェント ファイル共有の WP フォルダに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>This share was created in the "Set up file storage" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この共有は、適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックで作成されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupfile)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupfile)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupfile)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupfile)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source><bpt id="p1">**</bpt>Example:<ept id="p1">**</ept> <ph id="ph1">\[</ph><bpt id="p2">*</bpt>Agent Share<ept id="p2">*</ept><ph id="ph2">\]</ph><ph id="ph3">\\</ph>wp<ph id="ph4">\\</ph><ph id="ph5">\[</ph><bpt id="p3">*</bpt>Deployment name<ept id="p3">*</ept><ph id="ph6">\]</ph><ph id="ph7">\\</ph>StandaloneSetup-...<ph id="ph8">\\</ph>Apps<ph id="ph9">\\</ph>ETWManifests</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例:<ept id="p1">**</ept> <ph id="ph1">\[</ph><bpt id="p2">*</bpt>エージェント共有<ept id="p2">*</ept><ph id="ph2">\]</ph><ph id="ph3">\\</ph>wp<ph id="ph4">\\</ph><ph id="ph5">\[</ph><bpt id="p3">*</bpt>配置名<ept id="p3">*</ept><ph id="ph6">\]</ph><ph id="ph7">\\</ph>StandaloneSetup-...<ph id="ph8">\\</ph>アプリ<ph id="ph9">\\</ph> ETWManifests</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>If you must unregister providers, use the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーの登録を解除する必要がある場合は、次のコマンドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>After providers are registered, additional details about the new deployment are logged in Event Viewer, at <bpt id="p1">**</bpt>Applications and Services Logs<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーが登録されると、新しい配置についての追加詳細は<bpt id="p1">**</bpt>アプリケーションとサービス ログ<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> でイベント ビューアーにログインされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>The following folders will be shown:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフォルダが表示されます:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>MR-Logger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MR-Logger</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>MR-Sql</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MR-Sql</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>To see the new folders, you must close and reopen Event Viewer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフォルダーを表示するには、イベント ビューアーを終了して、再表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>To see additional details, you must deploy an environment again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の詳細を表示するには、もう一度環境を配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>An error occurs while AddAXDatabaseChangeTracking is running</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddAXDatabaseChangeTracking の実行中に発生するエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>If you receive an error while you run AddAXDatabaseChangeTracking at Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet), verify that the full path is correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet) で AddAXDatabaseChangeTracking を実行しているときにエラーが発生した場合は、フル パスが正しいことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>An example of a full path is <bpt id="p1">**</bpt>ax.d365ffo.onprem.contoso.com<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フル パスの例は <bpt id="p1">**</bpt>ax.d365ffo.onprem.contoso.com<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>The error might also occur because of an issue with the star certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スター証明書での問題が原因でエラーが発生する可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>For example, the remote certificate CN=<ph id="ph1">\*</ph>.d365ffo.onprem.contoso.com has a name that isn't valid or that doesn't match the host, ax.d365ffo.onprem.contoso.com.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、リモート証明書 CN=<ph id="ph1">\*</ph>.d365ffo.onprem.contoso.com には、無効な、またはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>Run the initialize database script, and validate that databases have correct users</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース初期化スクリプトを実行し、データベースのユーザーが適切であることを検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>If you receive only the AddAXDatabaseChangeTracking event, try to reach the MetadataService service for Finance and Operations by going to <ph id="ph1">`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddAXDatabaseChangeTracking イベントのみを受け取った場合は、<ph id="ph1">`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService`</ph> にアクセスし、Finance and Operations の MetadataService サービスにアクセスしてみてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Next, check the certificates of the service in the wif.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、wif.config ファイルでサービスの証明書を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>To find the file, sign in to one of the AOS machines, and then, in Task Manager, find <bpt id="p1">**</bpt>AxService.exe<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを検索するには、AOS マシンにサインインし、タスク マネージャーで <bpt id="p1">**</bpt>AxService.exe<ept id="p1">**</ept> を探してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>Right-click, and select <bpt id="p1">**</bpt>Open file location<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TimeZonePatcherを右クリックし、 <bpt id="p1">**</bpt>ファイルの場所を開く<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>In the wif.config file, you should see three thumbprints.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">wif.config ファイルでは、3 つの拇印を確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Note the following requirements for these thumbprints:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの拇印に関する次の要件に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>They must be different.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは異なる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>They must be in this order:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、この順序である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Financialreporting thumbprint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Financialreportingの拇印</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>ReportingService thumbprint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReportingServiceの拇印</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>SessionAuthentication thumbprint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SessionAuthenticationの拇印</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>If the thumbprints don't meet both these requirements, you must redeploy from LCS by using correct thumbprints.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拇印がこれらの要件の両方を満たしていない場合は、正しい拇印を使用して LCS から再配置をする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>The remote name can't be resolved</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート名を解決できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>The remote name could not be resolved: 'x.d365fo.onprem.contoso.com' / There was no endpoint listening at <ph id="ph1">`https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService`</ph> that could accept the message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった <ph id="ph1">`https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService`</ph> をリッスンしていたエンドポイントはありませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> This issue is often caused by an incorrect address or SOAP action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> この問題は、通常正しくないアドレスまたは SOAP アクションによって引き起こされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> Verify that the address can be reached, by manually opening the URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>手順:<ept id="p1">**</ept> URL を手動で開き、アドレスにアクセスできることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>For more details, see the "InnerException" text in the Event Viewer, if it's present.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、イベント ビューアーで <ph id="1">[InnerException]</ph> のテキストが存在するかどうか確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Error on ImportDefaultReports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ImportDefaultReports のエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>If Management Reporter reports are checked out during deployment, the deployment will fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置中に Management Reporter レポートがチェックアウトされると、配置処理は失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>To see whether reports are checked out, run the following <bpt id="p1">**</bpt>select<ept id="p1">**</ept> statements on the FinancialReporting database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートがチェック アウトされているかどうかを表示するには、FinancialReporting データベースで次の<bpt id="p1">**</bpt>選択<ept id="p1">**</ept>明細書を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>To learn which user has objects checked out, you can run the following <bpt id="p1">**</bpt>select<ept id="p1">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのユーザーがオブジェクトをチェック アウトするかを知るには、次の<bpt id="p1">**</bpt>選択<ept id="p1">**</ept>ステートメントを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>To resolve this issue manually, update the following tables, and set <bpt id="p1">**</bpt>checkedoutto<ept id="p1">**</ept> to <bpt id="p2">**</bpt>null<ept id="p2">**</ept> by using the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を手動で解決するには、以下のテーブルを次のコマンドを使用して更新し、 <bpt id="p1">**</bpt>checkedoutto<ept id="p1">**</ept> を <bpt id="p2">**</bpt>null<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>axdbadmin can't connect to the database server SQL-LS.contoso.com</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> The user doesn't have permission to connect to the AXDB database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept>AXDB データベースに接続するためのアクセス許可がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Remove the axdbadmin user from the database, if it already exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に存在する場合は、データベースから axdbadmin ユーザーを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>In the <bpt id="p1">**</bpt>ConfigTemplate.xml<ept id="p1">**</ept> file, specify the user name that must be added to the AXDB database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ConfigTemplate.xml<ept id="p1">**</ept> ファイルで、AXDB データベースに追加する必要があるユーザー名を指定してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Run the initialize database script again to add the axdbadmin user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Unable to resolve the xPath value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">xPath 値を解決することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>In the expected behavior, the following <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> value can't be resolved:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予想される動作では、次の <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> 値を解決することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source><ph id="ph1">\[</ph>TopologyInstance/CustomizationGroup<ph id="ph2">\[</ph>@name='ServiceConfiguration'<ph id="ph3">\]</ph>/Group<ph id="ph4">\[</ph>@name='AOSServicePrincipalUser'<ph id="ph5">\]</ph>/Customizations/Customization<ph id="ph6">\[</ph>@fieldName='PrincipalUserAccountPassword'<ph id="ph7">\]</ph>/@selectedValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>TopologyInstance/CustomizationGroup<ph id="ph2">\[</ph>@name='ServiceConfiguration'<ph id="ph3">\]</ph>/Group<ph id="ph4">\[</ph>@name='AOSServicePrincipalUser'<ph id="ph5">\]</ph>/Customizations/Customization<ph id="ph6">\[</ph>@fieldName='PrincipalUserAccountPassword'<ph id="ph7">\]</ph>/@selectedValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>Therefore, the fact that the <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> value can't be resolved isn't an issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、 <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> の値が解決できないことは問題ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>The <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> value looks for AOS runtime user information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> 値は、AOS ランタイム ユーザーの情報を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>However, because of integrated security, that information isn't required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、セキュリティが統合されているため、その情報は必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>The fact that the <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> value can't be resolved is communicated in case the failure must be investigated for another reason.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の理由でエラーを調査する必要がある場合は、 <bpt id="p1">**</bpt>xPath<ept id="p1">**</ept> の値を解決できないと通知されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>AD FS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>The sign-in page doesn't redirect you</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインイン ページにリダイレクトされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>The sign-in page might not redirect you but continues to prompt for credentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインイン ページにはリダイレクトされない可能性がありますが、資格情報の確認を続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Alternatively, you might be redirected but receive the following message:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、リダイレクトの可能性がありますが、次のメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>An error occurred.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが発生しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>Contact your administrator for more information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、システム管理者に問い合わせてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>In these cases, you can follow these steps to resolve the issue:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような場合、問題を解決するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Add the AD FS link to the list of trusted sites.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS リンクを信頼されているサイトの一覧に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Add the Dynamics 365 link to the list of trusted sites.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 リンクを信頼されているサイトの一覧に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Add a trailing slash (/), and see whether the behavior changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">末尾にスラッシュ「/」を追加し、動作が変更されるかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>Verify the AD FS Manager by going to <bpt id="p1">**</bpt>ADFS<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Application groups<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ADFS<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション グループ<ept id="p2">**</ept>の順に移動して、AD FS マネージャーを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>Double-click <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations on-premises<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations オンプレミス<ept id="p1">**</ept>をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>Then, under <bpt id="p1">**</bpt>Native application<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>Microsoft Dynamics 365 for Operations on-premises - Native application<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>ネイティブ アプリケーション<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション<ept id="p2">**</ept>をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Note the <bpt id="p1">**</bpt>Redirect URI<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リダイレクト URI<ept id="p1">**</ept> 値に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>It should match the DNS forward lookup zone for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の DNS 前方参照ゾーンに一致させる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Error: "Could not establish trust relationship for the SSL/TLS secure channel"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>If you receive an error that states, "Could not establish trust relationship for the SSL/TLS secure channel," follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「SSL/TLS のセキュリティで保護されているチャネルに対する信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>In Service Fabric, go to <bpt id="p1">**</bpt>Cluster<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Applications<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>AXSFType<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>fabric:/AXSF<ept id="p4">**</ept>, and then, on the <bpt id="p5">**</bpt>Details<ept id="p5">**</ept> tab, scroll down and note the URLs for <bpt id="p6">**</bpt>Aad<ph id="ph4">\_</ph>AADMetadataLocationFormat<ept id="p6">**</ept> and <bpt id="p7">**</bpt>Aad<ph id="ph5">\_</ph>FederationMetadataLocation<ept id="p7">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric で、<bpt id="p1">**</bpt>クラスタ<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>AXSFType<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>fabric:/AXSF<ept id="p4">**</ept> の順に移動し、<bpt id="p5">**</bpt>詳細<ept id="p5">**</ept>タブでスクロールし、<bpt id="p6">**</bpt>Aad<ph id="ph4">\_</ph>AADMetadataLocationFormat<ept id="p6">**</ept> および <bpt id="p7">**</bpt>Aad<ph id="ph5">\_</ph>FederationMetadataLocation<ept id="p7">**</ept> の URL に注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>Browse to those URLs from AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS からそれらの URL を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>On the AOS machine, in Event Viewer, go to <bpt id="p1">**</bpt>Applications and Services Logs<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AX-SystemRuntime<ept id="p4">**</ept> for details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、AOS マシンの、イベント ビューアーで、<bpt id="p1">**</bpt>アプリケーションとサービス ログ<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AX-SystemRuntime<ept id="p4">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Verify that the AD FS certificate is trusted:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS 証明書が信頼されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Verify the AD FS certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS 証明書を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>On the AD FS machine, in Server Manager, go to <bpt id="p1">**</bpt>Tools<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AD FS Management<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マシンの、サーバー マネージャーで、<bpt id="p1">**</bpt>ツール<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AD FS の管理<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>Expand <bpt id="p1">**</bpt>AD FS<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Service<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Certificates<ept id="p3">**</ept>, and make a note of the certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AD FS<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>サービス<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>証明書<ept id="p3">**</ept> を展開し、証明書を記録しておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>For example, one certificate might be dc1.contoso.com.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、1 つの証明書は、dc1.contoso.com の場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>On the AOS machine, in the Microsoft Management Console Certificates snap-in, go to <bpt id="p1">**</bpt>Certificates (Local Computer)<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Trusted Root Certification Authorities<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Certificates<ept id="p3">**</ept>, and verify that the AD FS certificate is listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS マシンの、Microsoft 管理コンソール証明書スナップインで、<bpt id="p1">**</bpt>証明書 (ローカル コンピューター)<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>信頼済ルート証明機関<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>証明書<ept id="p3">**</ept>の順に移動し、AD FS 証明書が一覧表示されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>If you receive a message that states that the site isn't secure, you haven't added your Secure Sockets Layer (SSL) certificate for AD FS to the Trusted Root Certification Authorities store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイトが安全でないことを示すメッセージが表示された場合は、AD FS の Secure Sockets Layer (SSL) 証明書が信頼済ルート証明機関ストアに追加されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>You can't connect to the remote server in some locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部の地域ではリモート サーバーに接続できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>You might not be able to connect to the remote server at the following places:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の場所でリモート サーバーに接続できない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>System.Net.HttpWebRequest.GetResponse()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Net.HttpWebRequest.GetResponse()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>In this case, go to the C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOS<ph id="ph4">\_</ph>1<ph id="ph5">\\</ph>Fabric<ph id="ph6">\\</ph>work<ph id="ph7">\\</ph>Applications<ph id="ph8">\\</ph>AXSFType<ph id="ph9">\_</ph>App35<ph id="ph10">\\</ph>log folder where you receive the error, and note the out file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合は、エラーの受信元である C: <ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOS<ph id="ph4">\_</ph>1<ph id="ph5">\\</ph>Fabric<ph id="ph6">\\</ph>work<ph id="ph7">\\</ph>Applications<ph id="ph8">\\</ph>AXSFType<ph id="ph9">\_</ph>App35<ph id="ph10">\\</ph> ログ フォルダーに移動し、出力ファイルを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>The out file contains the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">out ファイルには、次の情報が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>System.Net.WebException: Unable to connect to the remote server ---<ph id="ph1">\&gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Net.WebException: リモート サーバーに接続できません ---<ph id="ph1">\&gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond x.x.x.x:443</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>You can also use Psping to try to reach the remote server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Psping を使用してリモート サーバーに対する接続を試みることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>For information about Psping, see <bpt id="p1">[</bpt>Psping<ept id="p1">](/sysinternals/downloads/psping)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Psping の詳細については、<bpt id="p1">[</bpt>Psping<ept id="p1">](/sysinternals/downloads/psping)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>Redirect sign-in questions and issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインイン時の質問および問題をリダイレクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>If you're having issues when you sign-in, in Service Fabric Explorer, verify that the <bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Provisioning<ph id="ph2">\_</ph>AdminIdentityProvider<ept id="p2">**</ept> values are valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインイン時に問題が発生した場合は、Service Fabric Explorer で、<bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept> および <bpt id="p2">**</bpt>Provisioning<ph id="ph2">\_</ph>AdminIdentityProvider<ept id="p2">**</ept> の値が有効であることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>Here is an example:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source><bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept>: <ph id="ph2">`AXServiceUser@contoso.com`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロビジョニング <ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept>: <ph id="ph2">`AXServiceUser@contoso.com`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source><bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminIdentityProvider<ept id="p1">**</ept>: <ph id="ph2">`https://DC1.contoso.com/adfs`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロビジョニング<ph id="ph1">\_</ph>AdminIdentityProvider<ept id="p1">**</ept>: <ph id="ph2">`https://DC1.contoso.com/adfs`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>If the values aren't valid, you won't be able to proceed, and you must redeploy from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が有効でない場合は、処理を続行できず、LCS から再配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>If you used Reset-DatabaseUsers.ps1, you must restart the Dynamics Service before your changes take effect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reset-DatabaseUsers.ps1 を使用した場合、変更内容を有効にする前に、Dynamics サービスを再起動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>If you still have sign-in issues, in the USERINFO table, note the <bpt id="p1">**</bpt>NETWORKDOMAIN<ept id="p1">**</ept> and <bpt id="p2">**</bpt>NETWORKALIAS<ept id="p2">**</ept> values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引き続きサインインの問題がある場合は、USERINFO テーブルで、<bpt id="p1">**</bpt>NETWORKDOMAIN<ept id="p1">**</ept> および <bpt id="p2">**</bpt>NETWORKALIAS<ept id="p2">**</ept> の値を記録してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>Here is an example:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source><bpt id="p1">**</bpt>NETWORKDOMAIN:<ept id="p1">**</ept> <ph id="ph1">`https://DC1.contoso.com/adfs`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NETWORKDOMAIN:<ept id="p1">**</ept> <ph id="ph1">`https://DC1.contoso.com/adfs`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source><bpt id="p1">**</bpt>NETWORKALIAS:<ept id="p1">**</ept> <ph id="ph1">`AXServiceUser@contoso.com`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NETWORKALIAS:<ept id="p1">**</ept> <ph id="ph1">`AXServiceUser@contoso.com`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source><bpt id="p1">**</bpt>IDENTITYPROVIDER:<ept id="p1">**</ept> This should match the <bpt id="p2">**</bpt>NETWORKDOMAIN<ept id="p2">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IDENTITYPROVIDER:<ept id="p1">**</ept> これは <bpt id="p2">**</bpt>NETWORKDOMAIN<ept id="p2">**</ept> の内容と一致している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>On the AD FS machine, in Server Manager, go to <bpt id="p1">**</bpt>Tools<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AD FS Management<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Service<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マシンの、サーバー マネージャーで、<bpt id="p1">**</bpt>ツール<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AD FS の管理<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>サービス<ept id="p3">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>Right-click <bpt id="p1">**</bpt>Service and Edit Federation Service Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フェデレーション サービス プロパティの保守と編集<ept id="p1">**</ept> を右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>The <bpt id="p1">**</bpt>Federation Service identifier<ept id="p1">**</ept> value should match the <bpt id="p2">**</bpt>USERINFO.NETWORKDOMAIN<ept id="p2">**</ept> value, and it should have <bpt id="p3">**</bpt>https<ept id="p3">**</ept> in the URL (for example, <ph id="ph1">`https://DC1.contoso.com/adfs`</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フェデレーション サービスの識別子<ept id="p1">**</ept> は <bpt id="p2">**</bpt>USERINFO.NETWORKDOMAIN<ept id="p2">**</ept> の値と一致している必要があり、URL に <bpt id="p3">**</bpt>https<ept id="p3">**</ept> が入っている必要があります (たとえば <ph id="ph1">`https://DC1.contoso.com/adfs`</ph>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>On the AD FS machine, in Event Viewer, go to <bpt id="p1">**</bpt>Applications and Services Logs<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AD FS<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Admin<ept id="p3">**</ept>, and make a note of any errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マシンの、イベント ビューアーで、<bpt id="p1">**</bpt>アプリケーションとサービス ログ<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>AD FS<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>管理者<ept id="p3">**</ept>に移動してエラーを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>Fiddler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiddler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>Fiddler can be used for additional debugging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のデバッグには Fiddler を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>For in-depth information about Fiddler, see <bpt id="p1">[</bpt>AD FS 2.0: How to Use Fiddler Web Debugger to Analyze a WS-Federation Passive Sign-In<ept id="p1">](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx)</ept> and <bpt id="p2">[</bpt>Cracking the AD FS Token from another AD FS Claims Provider<ept id="p2">](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiddler について詳しい情報は、 <bpt id="p1">[</bpt>AD FS 2.0: Fiddler Web デバッガーを使って WS フェデレーション パッシブ サインインを分析する方法<ept id="p1">](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx)</ept> と <bpt id="p2">[</bpt>別の AD FS クレーム プロバイダーからの AD FS トークンのクラッキング<ept id="p2">](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/)</ept> をご覧ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>The following sections provide focused debugging steps for claims that are returned to Microsoft Dynamics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のセクションでは、 Microsoft Dynamics に返される要求に対する重点的なデバッグの手順を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>Repo/capture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リポジトリ/キャプチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>Open Fiddler, go to <bpt id="p1">**</bpt>Tools <ph id="ph1">\&gt;</ph> Options <ph id="ph2">\&gt;</ph> HTTPS<ept id="p1">**</ept>, and select <bpt id="p2">**</bpt>Decrypt HTTPS traffic<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiddler を起動し、 <bpt id="p1">**</bpt>ツール <ph id="ph1">\&gt;</ph> オプション <ph id="ph2">\&gt;</ph> HTTPS<ept id="p1">**</ept> から <bpt id="p2">**</bpt>HTTPS トラフィックの復号化<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Start to capture traffic (the shortcut key is F12).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラフィックのキャプチャを開始します (ショートカット キーは F12 キーです)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>You can verify that that traffic is being captured by looking at the lower left of the tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールの左下を確認すると、該当のトラフィックがキャプチャされていることを確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>Open an InPrivate instance of Internet Explorer or an Incognito instance of Chrome.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer の InPrivate モード、またはChrome の Incognito モードを使用して開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>Open Finance and Operations (for example, <ph id="ph1">`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations を開きます (例 <ph id="ph1">`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`</ph>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>Sign in by using the USERINFO.NETWORKALIAS account and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">USERINFO.NETWORKALIAS のアカウントとパスワードを使用してログオンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>After you're signed in, stop Fiddler from capturing traffic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ログイン後、Fiddler によるトラフィックのキャプチャを停止してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>Analyze</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>In the right pane of Fiddler, notice that a horizontal divider separates the request from the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiddler の右側のウィンドウには、リクエストとレスポンスが上段と下段にに分割されていることを留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>Unlike a network trace, where you typically get one frame for a request and another frame for a response, Fiddler provides one frame that contains both the request and the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リクエストとレスポンスとでそれぞれ別個のフレームを取得するようなネットワーク トレースとは異なり、Fiddler はリクエストとレスポンスの両方を1 つのフレームで提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>In Fiddler, in the upper-right corner, select <bpt id="p1">**</bpt>Inspectors<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Raw<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiddlerを起動し、画面右上隅の <bpt id="p1">**</bpt>Inspectors<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Raw<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>In the lower-right corner, select <bpt id="p1">**</bpt>Cookies<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右下隅の <bpt id="p1">**</bpt>Cookie<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>Do a search for <bpt id="p1">**</bpt>MSISAuth<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MSISAuth<ept id="p1">**</ept> を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>Select the row that has a result of <bpt id="p1">**</bpt>200<ept id="p1">**</ept> for the AD FS host.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS をホストするには、結果が <bpt id="p1">**</bpt>200<ept id="p1">**</ept> 件ある行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Look above the row that you just selected to find a row that has a result of <bpt id="p1">**</bpt>302<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記で選択した上の行のなかで、 <bpt id="p1">**</bpt>302<ept id="p1">**</ept> 件の結果がある行を探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>Select the row.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">確認した行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>You should see the AD FS URL, host, user name, and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS URL、ホスト、ユーザー名、およびパスワードが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>For privacy, you might have to scrub personally identifiable information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライバシー保護のため、状況に応じて個人を特定できる情報を削除してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>Personally identifiable information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個人情報</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>Select the next row that has a result of <bpt id="p1">**</bpt>302<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次は、結果が <bpt id="p1">**</bpt>302<ept id="p1">**</ept> 件ある行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>The URL should be <bpt id="p1">**</bpt>.../namespaces/AXSF/<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL が、 <bpt id="p1">**</bpt>.../namespaces/AXSF/<ept id="p1">**</ept> となっていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Find the code line that is shown on that row.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記で選択した行に示されているコード行を探してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>Code line</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>Copy the value of code line after the equal sign (=).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">等号 (=) の後に表示されているコード値をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>Go to <ph id="ph1">&lt;https://www.base64decode.org/&gt;</ph>, and paste the code that you just copied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&lt;https://www.base64decode.org/&gt;</ph> に移動し、上記でコピーしたコードを貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>In the <bpt id="p1">**</bpt>Source charset<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>ASCII<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Source charset<ept id="p1">**</ept> フィールドで、 <bpt id="p2">**</bpt>ASCII<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>Select <bpt id="p1">**</bpt>Decode<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Decode<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Copy the results, and follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示された結果をコピーし、以下の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>Make sure that the <bpt id="p1">**</bpt>upn<ept id="p1">**</ept> value matches the user name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>upn<ept id="p1">**</ept> の値が、ユーザー名と一致していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>Make sure that the <bpt id="p1">**</bpt>unique_name<ept id="p1">**</ept> value is the Active Directory user that is being tested.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>unique_name<ept id="p1">**</ept> の値がテストで使用している Active Directoryユーザー名であることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Go to <bpt id="p1">**</bpt>Active Directory Users and Computers<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>domain<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Users<ept id="p3">**</ept>, and make sure that this user is being tested.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Active Directory ユーザーとコンピューター<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>ドメイン<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>ユーザー<ept id="p3">**</ept> に移動し、テスト中のユーザーが表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Sign-in issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインの問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>If you or other users experience sign-in issues, in Service Fabric Explorer, verify that the <bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Provisioning<ph id="ph2">\_</ph>AdminIdentityProvider<ept id="p2">**</ept> values are valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインに関する問題が発生した場合には、Service Fabric Explorer で、<bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept> および <bpt id="p2">**</bpt>Provisioning<ph id="ph2">\_</ph>AdminIdentityProvider<ept id="p2">**</ept> の値が有効であることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>If the values are valid, run the following command on the primary SQL Server machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が有効な場合は、プライマリ SQL Server マシンで次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>On each AOS machine, in Task Manager, select <bpt id="p1">**</bpt>AXService.exe<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>End task<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク マネージャーの各 AOS マシンで、<bpt id="p1">**</bpt>AXService.exe<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>タスクの終了<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>To verify that a user has been reset, run the following <bpt id="p1">**</bpt>select<ept id="p1">**</ept> query in the AXDB SQL database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがリセットされたことを確認するには、AXDB SQL databaseで次の <bpt id="p1">**</bpt>select<ept id="p1">**</ept> 文を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>In an Azure Active Directory (Azure AD) environment (that is, an online environment), the SID is a hash of a network alias and a network domain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Active Directory (Azure AD) 環境 (オンライン環境) では、SID はネットワーク エイリアスおよびネットワーク ドメインのハッシュの役割を果たします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>In an AD DS environment (that is, an on-premises environment), the SID is a hash of a network alias and an identify provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD DS 環境 (オンプレミス環境) では、SID はネットワーク エイリアスのハッシュとして機能し、プロバイダーを識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>In some cases, you still might not be able to sign in, and you might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、引き続きサインインができず、次のエラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>You are not authorized to login with your current credentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在の資格情報でログインする権限がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>You will be redirected to the login page in a few seconds.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マシンで、サーバー マネージャー &gt; ツール &gt; AD FS の管理 に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>If this error occurs, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーが表示された場合は、次の手順に従ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>On the AD FS machine, go to <bpt id="p1">**</bpt>Server Manager<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Tools<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>AD FS Management<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マシンで、 <bpt id="p1">**</bpt>Server Manager<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Tools<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>AD FS Management<ept id="p3">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>Right-click <bpt id="p1">**</bpt>AD FS<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Edit Federation Service Properties<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AD FS<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>フェデレーション サービス プロパティの編集<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>Make sure that the <bpt id="p1">**</bpt>Federation Service Identifier<ept id="p1">**</ept> value matches the <bpt id="p2">**</bpt>Userinfo.NetworkDomain<ept id="p2">**</ept> and <bpt id="p3">**</bpt>UserInfo.IdentityProvider<ept id="p3">**</ept> values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フェデレーション サービス 識別子<ept id="p1">**</ept> の値が、 <bpt id="p2">**</bpt>Userinfo.NetworkDomain<ept id="p2">**</ept> および <bpt id="p3">**</bpt>UserInfo.IdentityProvider<ept id="p3">**</ept> の値と一致していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>On the AD FS machine, open Windows PowerShell, and run <bpt id="p1">**</bpt>Get-AdfsProperties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マシンで、Windows PowerShell を開き、 <bpt id="p1">**</bpt>Get-AdfsProperties<ept id="p1">**</ept> を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>Make sure that the <bpt id="p1">**</bpt>IdTokenIssuer<ept id="p1">**</ept> value matches the <bpt id="p2">**</bpt>Federation Service Identifier<ept id="p2">**</ept> value from step 3, and also the <bpt id="p3">**</bpt>Provisioning_AdminIdentityProvider<ept id="p3">**</ept> value on the <bpt id="p4">**</bpt>fabric:/AXSF Details<ept id="p4">**</ept> tab at <bpt id="p5">**</bpt>Service Fabric Explorer<ept id="p5">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p6">**</bpt>Cluster<ept id="p6">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p7">**</bpt>Applications<ept id="p7">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p8">**</bpt>AXSFType<ept id="p8">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IdTokenIssuer<ept id="p1">**</ept> の値が、手順3の <bpt id="p2">**</bpt>フェデレーション サービス 識別子<ept id="p2">**</ept> の値、および <bpt id="p3">**</bpt>Provisioning_AdminIdentityProvider<ept id="p3">**</ept> の値と一致していることを確認してください。 (これは <bpt id="p4">**</bpt>fabric:/AXSF Details<ept id="p4">**</ept> タブに表示されています。 <bpt id="p5">**</bpt>Service Fabric Explorer<ept id="p5">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p6">**</bpt>Cluster<ept id="p6">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p7">**</bpt>Applications<ept id="p7">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p8">**</bpt>AXSFType<ept id="p8">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>In Service Fabric Explorer, verify that the <bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Provisioning<ph id="ph2">\_</ph>AdminIdentityProvider<ept id="p2">**</ept> values are valid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Explorer で、 <bpt id="p1">**</bpt>Provisioning<ph id="ph1">\_</ph>AdminPrincipalName<ept id="p1">**</ept> 値と <bpt id="p2">**</bpt>Provisioning<ph id="ph2">\_</ph>AdminIdentityProvider<ept id="p2">**</ept> の値が有効であることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>If the preceding steps don't resolve the issue, see the <bpt id="p1">[</bpt>AD FS<ept id="p1">](troubleshoot-on-prem.md#ad-fs)</ept> section of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の手順で問題が解決しない場合は、このトピックの 「 <bpt id="p1">[</bpt>AD FS<ept id="p1">](troubleshoot-on-prem.md#ad-fs)</ept> 」 を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>System.Data.SqlClient.SqlException (0x80131904) and System.ComponentModel.Win32Exception (0x80004005)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>You might receive one of the following errors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエラーのいずれかが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>System.Data.SqlClient.SqlException (0x80131904): A connection was successfully established with the server, but then an error occurred during the sign-in process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、サインイン プロセス時にエラーが発生しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>(provider: SSL Provider, error: 0 - The certificate chain was issued by an authority that is not trusted.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>System.ComponentModel.Win32Exception (0x80004005): The certificate chain was issued by an authority that is not trusted</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>In this case, either the certificates haven't been installed, or they haven't given access to the correct users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、証明書がインストールされていないか、それらがしかるべきユーザーに結びついていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>To resolve this error, add the public key SQL Server certificate to all the Service Fabric nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>Keyset doesn't exist</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Keyset が存在しません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>If you find that the keyset doesn't exist, scripts weren't run on all machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キーセットが存在しないことが判明した場合は、スクリプトがすべてのコンピューターで実行されなていなかったことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>Review and complete the "Set up VMs" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な設定の「VM の設定」セクション、および環境の配置トピックを確認し完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupvms)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupvms)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupvms)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#setupvms)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Copy the scripts in each folder to the VMs that correspond to the folder name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>Additionally, check the .csv file to verify that the correct domain is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、正しいドメインを使うことを検証する .csv ファイルを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>Error: "RunAsync failed due to an unhandled FabricException causing replica to fault"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source>You might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエラーが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>RunAsync failed due to an unhandled FabricException causing replica to fault: System.Fabric.FabricException: The first Fabric upgrade must specify both the code and config versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException: 最初の Fabric アップグレードではコード バージョンと設定バージョンの両方を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>Requested value: 0.0.0.0:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求された値: 0.0.0.0:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>In this case, in the ClusterConfig.json file, change <bpt id="p1">**</bpt>diagnosticsStore<ept id="p1">**</ept> from a network share to a local path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、ClusterConfig.json ファイルで、 <bpt id="p1">**</bpt>diagnosticsStore<ept id="p1">**</ept> をネットワーク共有からローカル パスに変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source>For example, change <bpt id="p1">**</bpt><ph id="ph1">\\</ph><ph id="ph2">\\</ph>server<ph id="ph3">\\</ph>path<ept id="p1">**</ept> to a default value of <bpt id="p2">**</bpt>C:<ph id="ph4">\\</ph>ProgramData<ph id="ph5">\\</ph>SF<ph id="ph6">\\</ph>DiagnosticsStore<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt><ph id="ph1">\\</ph><ph id="ph2">\\</ph>サーバー<ph id="ph3">\\</ph>パス<ept id="p1">**</ept>を、規定値の <bpt id="p2">**</bpt>C:<ph id="ph4">\\</ph>ProgramData<ph id="ph5">\\</ph>SF<ph id="ph6">\\</ph>DiagnosticsStore<ept id="p2">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>Service Fabric AOS node error during build: The execution time-out expired</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>The timeout period elapsed prior to completion of the operation or the server is not responding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作を完了する前にタイムアウト期間が経過したか、サーバーが応答していません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source>The statement has been terminated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細書は終了しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>Only one AOS machine can run DB Sync at a time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一度に 1 つの AOS マシンのみ DB Sync を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source>You can safely ignore this error, because it means that one of the AOS VMs is running DB Sync. Therefore, the other VMs produce a warning that they can't run it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーは無視しても問題ありません。 AOS VM のいずれかが DB Sync で実行されているため、他の VM が実行できないという警告が表示されたためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source>To verify that DB Sync is running, on the AOS VM that isn't producing warnings, in Event Viewer, go to <bpt id="p1">**</bpt>Applications and Services Log<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AX-DatabaseSynchronize/Operational<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DB Sync が実行されていることを確認するには、イベント ビューアの、警告を生成していない AOS VM で<bpt id="p1">**</bpt>アプリケーションおよびサービスのログ<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>AX-DatabaseSynchronize/Operational<ept id="p4">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source>Error: "RequireNonce is 'true' (default) but validationContext.Nonce is null"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source>You might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエラーが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>RequireNonce is 'true' (default) but validationContext.Nonce is null</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「RequireNonce が True (既定) となっていますが、validationContext.Nonce は Null となっています」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>This error also appears as an HTTP error 500 in Internet Explorer after you sign in to the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーは、クライアントにサインインした後も Internet Explorer で HTTP エラー 500 として表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source>The nonce that is issued can't be validated if Internet Explorer is in Enhanced Security Configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source>To sign in to the client, disable Enhanced Security Configuration for Internet Explorer via Server Manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントにサインインするには、サーバー マネージャーを介して Internet Explorer のセキュリティ強化設定を無効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>Error: "Invalid algorithm specified / Cryptography"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「無効なアルゴリズムが指定されている/暗号化」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source>If you receive an "Invalid algorithm specified / Cryptography" error, you must use the Microsoft Enhanced RSA and AES Cryptographic Provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"Invalid algorithm specified / Cryptography" エラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source>For more information, see the certificate requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、証明書の要件を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>Additionally, verify that the structure of the credentials.json file is correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、credentials.json ファイルの構造が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>If you must re-create the certificate by using the correct provider, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source>Create the certificate again by using the correct provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しいプロバイダーを使用して証明書を再度作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source>Change the <bpt id="p1">**</bpt>ConfigTemplate.xml<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ConfigTemplate.xml<ept id="p1">**</ept> ファイルの変更。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>Run the infrastructure scripts on all machines in the cluster, and make sure that the <bpt id="p1">**</bpt>Test-D365FOConfiguration.ps1<ept id="p1">**</ept> script passes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、<bpt id="p1">**</bpt>Test-D365FOConfiguration.ps1<ept id="p1">**</ept> スクリプトに合格するかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>Reconfigure the environment from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS から環境を再構成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>An "Unable to find certificate" error occurs when you run Test-D365FOConfiguration.ps1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Test-D365FOConfiguration.ps1 を実行した際、「証明書を検出できません」エラーが発生</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source>If you receive an "Unable to find certificate" error when you run Test-D365FOConfiguration.ps1, check whether certificates or thumbprints are being combined for multiple purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Test-D365FOConfiguration.ps1 を実行時に 「証明書を検出できません」 というエラーが発生した場合は、証明書または拇印がその他複数の用途で併用されているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source>For example, you will receive this error if the client certificate and the SessionAuthentication certificate are combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、クライアントと SessionAuthentication の証明書が併用されてされる場合、このエラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>We recommend that you not combine certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書を結合しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>For more information, see the certificate requirements, and check the acl.csv file for <bpt id="p1">**</bpt>domain.com<ph id="ph1">\\</ph>user<ept id="p1">**</ept> versus <bpt id="p2">**</bpt>domain<ph id="ph2">\\</ph>user<ept id="p2">**</ept> (for example, NETBIOS structure).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、 証明書の必要要件を参照し、 <bpt id="p1">**</bpt>domain.com<ph id="ph1">\\</ph>user<ept id="p1">**</ept> versus <bpt id="p2">**</bpt>domain<ph id="ph2">\\</ph>user<ept id="p2">**</ept> 内 (たとえば、NETBIOS 構造) のacl.csv ファイルを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source>The client and server can't communicate because they don't have a common algorithm</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントとサーバーは共通のアルゴリズムを持たないため通信できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>If the client and server can't communicate because they don't have a common algorithm, verify that the certificates that are created use the specified provider, as explained in the "Plan and acquire your certificates" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントとサーバーが疎通できない場合は双方のアルゴリズムが異なることが原因です。作成した証明書が指定したプロバーダーを使用しているか確認をしてください。これについては"Plan and acquire your certificates" の項目で解説しています。ご利用の環境に応じた適切な設定と配置を行ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#plancert)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#plancert)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#plancert)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#plancert)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source>Find a list of group managed service accounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グループ管理サービス アカウント の一覧の検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>To find a list of all groups and hosts, run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのグループとホストの一覧を検索するには、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>AddCertToServicePrincipal script fails on Import-Module</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Import-Module での AddCertToServicePrincipal スクリプトの失敗</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source>AddCertToServicePrincipal script failing on Import-Module : Could not load file or assembly 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>Strong name validation failed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">厳密な名前の検証に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>(Exception from HRESULT: 0x8013141A) may have multiple versions of the same module installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> To resolve this issue, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> 問題を解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source>Run the following command in Windows PowerShell.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows PowerShell で次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source>Close the Windows PowerShell window, and try to run the script again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows PowerShell ウィンドウを閉じて、スクリプトを再度実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source>ReportingServicesSetup.exe error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReportingServicesSetup.exe エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source>ReportingServicesSetup.exe Error: 0 : Application fabric:/ReportingService is not OK after 10 minutes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReportingServicesSetup.exe エラー: 0 : アプリケーション fabric:/ReportingService は10分後から OK ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source>Application: ReportingServicesBootstrapper.exe</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション: ReportingServicesBootstrapper.exe</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>Framework Version: v4.0.30319</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワーク バージョン: v4.0.30319</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source>Description: The process was terminated due to an unhandled exception.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明: プロセスは未処理の例外によって中止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source><bpt id="p1">**</bpt>Reason:<ept id="p1">**</ept> If you receive this error, strong name validation is enabled in the Reporting server, but it should not be enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>理由:<ept id="p1">**</ept> このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効にされていますが、有効にしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> To resolve this issue, run the <bpt id="p2">**</bpt>config-PreReq<ept id="p2">**</ept> script on the Reporting server machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ:<ept id="p1">**</ept> 問題を解決するには、レポート サーバー マシンで <bpt id="p2">**</bpt>config-PreReq<ept id="p2">**</ept> スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>The requested operation requires elevation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求された操作には、昇格が必要です</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>This issue occurs because AOS users aren't in the local administrator group, and User Account Control (UAC) hasn't been disabled correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS ユーザーはローカル管理者グループに属しておらず、ユーザー アカウント コントロール (UAC) が正しく無効化されていないために、この問題が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source>To resolve the issue, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>Add AOS users as local admins, as described in the "Join VMs to the domain" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の適切な設定および配置トピックの「VMs とドメインを結合」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#joindomain)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#joindomain)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#joindomain)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#joindomain)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source>Run the <bpt id="p1">**</bpt>Config-PreReq<ept id="p1">**</ept> script on all the AOS machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての AOS コンピューターで、<bpt id="p1">**</bpt>Config-PreReq<ept id="p1">**</ept> スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>Make sure that the <bpt id="p1">**</bpt>Test-Configuration<ept id="p1">**</ept> script passes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テスト構成<ept id="p1">**</ept>スクリプトがパスすることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>If UAC was changed, you must restart the machine before the changes take effect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UAC が変更された場合は、変更を有効にする前にマシンを再起動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source>Files in use errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用中ファイルのエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source>If these "Files in use" errors occur, set up the exclusion rules that Service Fabric advises.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「ファイルは使用中です」のエラーが発生した場合は、Service Fabric に示されている例外ルールを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>For information, see <bpt id="p1">[</bpt>Environment setup<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>環境設定<ept id="p1">](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source>Apply deployable packages during deployment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置中に配置可能パッケージを適用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>Package deployment fails because of a "path too long" exception</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「パスが長過ぎる」例外によってパッケージの展開が失敗する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source>Because of a 260-character limit in Microsoft Windows, deployment will fail if a package has a longer name, or if the on-premises share has the full FQDN path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source>If the character limit is exceeded, you receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字数の制限を超過した場合、次のエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source>System.IO.PathTooLongException: The specified path, file name, or both are too long.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.IO.PathTooLongException: 指定されたパス、ファイル名、またはその両方が長すぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source>The fully qualified file name must be less than 260 characters, and the directory name must be less than 248 characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全に記述されたファイル名は 260 文字未満である必要があり、ディレクトリ名は 248 文字未満である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="672">
          <source>at System.IO.PathHelper.GetFullPathName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">at System.IO.PathHelper.GetFullPathName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="673">
          <source>To work around this issue, shorten the package name, and then apply the package again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、パッケージ名を短くし、パッケージをもう一度適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="674">
          <source>Alternatively, shorten the overall length of the share path for the on-premises assets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、オンプレミス資産の共有パス全体の長さを短くしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="675">
          <source>Package deployment fails because of a serialization error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シリアル化エラーが原因でパッケージの展開に失敗する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="676">
          <source>During package deployment, you might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ配置中、次のエラーが発生する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="677">
          <source>Serialization version mismatch detect, make sure the runtime DLLs are in sync with the deployed metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シリアル化バージョンの不一致が検出されたので、ランタイム DLL が配置されたメタデータと同期していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="678">
          <source>Version of file 'XXX'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「XXX」ファイルのバージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="679">
          <source>Version of DLL 'XXX'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DLL 「XXX」のバージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="680">
          <source>In this case, the version of the environment where the package was developed might differ from the version of the environment that the package is being deployed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合は、パッケージが開発された環境のバージョンと、パッケージを配置する環境のバージョンが異なっている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="681">
          <source>To work around this issue, keep the development or build environments on the same version as the deployed on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="682">
          <source>You can confirm the package version by looking in the <bpt id="p1">**</bpt>Additional details<ept id="p1">**</ept> section in the Asset library where the package is uploaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージのアップロード先にあるアセット ライブラリの<bpt id="p1">**</bpt>追加の詳細<ept id="p1">**</ept>セクションをクリックすることにより、パッケージ バージョンを確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="683">
          <source>To fix the error, generate the package on a version that is the same as or earlier than the version that is deployed in the on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーを修正するには、オンプレミス環境に配置されたバージョンと同じか、またはそれ以前のバージョンでパッケージを生成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="684">
          <source>Package deployment fails because of dependencies on missing modules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="685">
          <source>If you try to apply a package that is missing dependent modules, package application will fail, and you will receive a message that resembles the following message:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次のようなメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="686">
          <source>Package <ph id="ph1">\[</ph>dynamicsax-My<ph id="ph2">\_</ph>commonextension.7.0.4679.35176.nupkg has missing dependencies: <ph id="ph3">\[</ph>dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor<ph id="ph4">\]</ph><ph id="ph5">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ <ph id="ph1">\[</ph>dynamicsax-My<ph id="ph2">\_</ph>commonextension.7.0.4679.35176.nupkg に依存関係がありません: <ph id="ph3">\[</ph>dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor<ph id="ph4">\]</ph><ph id="ph5">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="687">
          <source>Package <ph id="ph1">\[</ph>dynamicsax-My<ph id="ph2">\_</ph>coreextension.7.0.4679.35176.nupkg has missing dependencies: <ph id="ph3">\[</ph>dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor<ph id="ph4">\]</ph><ph id="ph5">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ <ph id="ph1">\[</ph>dynamicsax-My<ph id="ph2">\_</ph>coreextension.7.0.4679.35176.nupkg に依存関係がありません: <ph id="ph3">\[</ph>dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor<ph id="ph4">\]</ph><ph id="ph5">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="688">
          <source>Package <ph id="ph1">\[</ph>dynamicsax-My<ph id="ph2">\_</ph>uiextension.7.0.4679.35176.nupkg has missing dependencies: <ph id="ph3">\[</ph>dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests<ph id="ph4">\]</ph><ph id="ph5">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージ <ph id="ph1">\[</ph>dynamicsax-My<ph id="ph2">\_</ph>uiextension.7.0.4679.35176.nupkg に依存関係がありません: <ph id="ph3">\[</ph>dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests<ph id="ph4">\]</ph><ph id="ph5">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="689">
          <source>To confirm the issue and find the missing dependencies, in Event Viewer, open <bpt id="p1">**</bpt>Application and Services<ept id="p1">**</ept>, and then go to <bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p4">**</bpt>AX-SetupModuleEvents<ept id="p4">**</ept> to view events that have missing modules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーで、<bpt id="p1">**</bpt>アプリケーションとサービス<ept id="p1">**</ept>を開き、<bpt id="p2">**</bpt>Microsoft<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>Dynamics<ept id="p3">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p4">**</bpt>AX-SetupModuleEvents<ept id="p4">**</ept> の順で移動して、見つからないモジュールのあるイベントを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="690">
          <source>For example, one of the modules that is typically missing is ApplicationFoundationFormAdaptor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="691">
          <source>To fix this issue and successfully apply the package, either add dependent modules, or remove modules that require dependent modules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="692">
          <source>To add dependent modules, you must include the dependencies when you build the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="693">
          <source>To remove modules, you can use ModelUtil.exe to delete a module.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="694">
          <source>For more information, see <bpt id="p1">[</bpt>Export and import a model<ept id="p1">](../dev-tools/models-export-import.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>モデルのエクスポートとインポート<ept id="p1">](../dev-tools/models-export-import.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="695">
          <source>Package deployment works in a one-box environment but not in the sandbox environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="696">
          <source>A one-box environment might have all the modules installed, whereas the sandbox environment might have only the modules that are required in order to run your production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、一方ではサンドボックス環境には実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="697">
          <source>If the package that was built in the dev environment has a dependency on modules that are present in the one-box environment but not in the sandbox environment, the package won't work in the sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境で作成されたパッケージが、サンドボックス環境ではなく、ワン ボックス環境にあるモジュールに依存する場合、パッケージはサンドボックス環境では動作しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="698">
          <source>To resolve this issue, look at all the modules that you're dependent on, and make sure that you don't pull any farm adapter or any other module that isn't required in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、依存関係のあるすべてのモジュールを確認し、実稼動環境で不要なアダプターまたはその他のモジュールを使用しないようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="699">
          <source>The best practice is to take the package from the build box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド ボックスからパッケージを取得することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="700">
          <source>An error occurs when you sign in to on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境へのログイン時にエラーが発生</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="701">
          <source><bpt id="p1">**</bpt>Platform update 12:<ept id="p1">**</ept> Turn off the Skype integration by going to <bpt id="p2">**</bpt>System administration<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>Setup<ept id="p3">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p4">**</bpt>Client performance options<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プラットフォーム更新 12:<ept id="p1">**</ept> <bpt id="p2">**</bpt>システム管理<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>設定<ept id="p3">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p4">**</bpt>クライアント パフォーマンス オプション<ept id="p4">**</ept>に移動して、Skype 統合を無効にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="702">
          <source>When you go to the app, append <bpt id="p1">**</bpt>?debug=true<ept id="p1">**</ept> to the URL, as shown in the following example: <ph id="ph1">`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリに移動するとき、<ph id="ph1">`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</ph> の例のように、<bpt id="p1">**</bpt>?debug=true<ept id="p1">**</ept> を URL に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="703">
          <source><bpt id="p1">**</bpt>Platform update 8 and Platform update 11:<ept id="p1">**</ept> A known issue for the Skype application programming interface (API) affects the ability to sign in to on-premises environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11:<ept id="p1">**</ept> 確認されている問題は、 Skype の アプリケーション プログラミング インターフェイス (API) が、オンプレミス環境へのサインインする機能に影響を及ぼしているというものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="704">
          <source>Microsoft is investigating a resolution for this issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoftはこの問題の解決方法を調査しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="705">
          <source>To work around this issue, you can add <bpt id="p1">**</bpt>?debug=true<ept id="p1">**</ept> to the end of the URL, as shown in the following example: <ph id="ph1">`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するために、次の例のように URL の末尾に <bpt id="p1">**</bpt>?debug=true<ept id="p1">**</ept> を追加できます。<ph id="ph1">`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="706">
          <source>The local agent stops working after the tenant for the project from LCS is changed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="707">
          <source>Follow these steps to configure the local agent with the updated tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新されたテナントでローカル エージェントを構成するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="708">
          <source>Uninstall the local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントをアンインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="709">
          <source>Follow the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの環境での適切なセットアップと配置トピックの「テナントの LCS 接続のコンフィギュレーション」セクションにある手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="710">
          <source><bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configurelcs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configurelcs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="711">
          <source><bpt id="p1">[</bpt>Platform update 8 and Platform update 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#configurelcs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11<ept id="p1">](setup-deploy-on-premises-pu8-pu11.md#configurelcs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="712">
          <source>Create a new LCS connector in the new tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいテナントに新しい LCS コネクタを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="713">
          <source>Download the <bpt id="p1">**</bpt>local-agent.config<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>local-agent.config<ept id="p1">**</ept> ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="714">
          <source>Install the local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="715">
          <source>Additional deployments (for example, two sandbox deployments, or a sandbox and production deployment)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の配置 (たとえば、2 つのサンド ボックス展開、またはサンド ボックスおよび生産の配置)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="716">
          <source>You will receive the following error when you deploy an additional environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の環境を展開すると、次のエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="717">
          <source>.<ph id="ph1">\\</ph>Publish-ADFSApplicationGroup.ps1 -HostUrl <ph id="ph2">`https://ax.d365ffo.onprem.contoso.com`</ph> New-AdfsApplicationGroup : MSIS9908: The application group identifier must be unique in AD FS configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Publish-ADFSApplicationGroup.ps1 -HostUrl <ph id="ph2">`https://ax.d365ffo.onprem.contoso.com`</ph> New-AdfsApplicationGroup : MSIS9908: アプリケーション グループ ID は、AD FS コンフィギュレーションで一意である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="718">
          <source>You can skip or modify the following sections in the deployment instructions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配備手順の次のセクションをスキップまたは変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="719">
          <source>Plan and acquire your certificates (as documented for <bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#plancert)</ept> or <bpt id="p2">[</bpt>Platform update 8 and Platform update 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#plancert)</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の計画と取得 (<bpt id="p1">[</bpt>プラットフォーム更新プログラム 12<ept id="p1">](setup-deploy-on-premises-pu12.md#plancert)</ept> または <bpt id="p2">[</bpt>プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#plancert)</ept> で記載されたものとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="720">
          <source>You must use the same on-premises local agent certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同一のオンプレミスのローカル エージェント証明書を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="721">
          <source>You can use same star certificates (AOS SSL and Service Fabric).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同一のスター証明書を使用することができます(AOS SSL および Service Fabric)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="722">
          <source>The remaining certificates should probably differ from the certificates for the existing environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">残りの証明書は既存の環境の証明書とは異なる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="723">
          <source>Download setup scripts from LCS (as documented for <bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#downloadscripts)</ept> or <bpt id="p2">[</bpt>Platform update 8 and Platform update 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#downloadscripts)</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS からのセットアップ スクリプトのダウンロード (<bpt id="p1">[</bpt>プラットフォーム更新プログラム 12<ept id="p1">](setup-deploy-on-premises-pu12.md#downloadscripts)</ept> または <bpt id="p2">[</bpt>プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#downloadscripts)</ept> で記載されたものとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="724">
          <source>The scripts that are downloaded should be copied into a new folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="725">
          <source>Set up a standalone Service Fabric cluster (as documented for <bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupsfcluster)</ept> or <bpt id="p2">[</bpt>Platform update 8 and Platform update 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">[</bpt>プラットフォーム更新プログラム 12<ept id="p1">](setup-deploy-on-premises-pu12.md#setupsfcluster)</ept> または <bpt id="p2">[</bpt>プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)</ept> に記載されているように) スタンドアロン Service Fabric クラスタを設定します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="726">
          <source>The scripts that are downloaded should be copied into a new folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="727">
          <source>Configure LCS connectivity for the tenant (as documented for <bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configurelcs)</ept> or <bpt id="p2">[</bpt>Platform update 8 and Platform update 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#configurelcs)</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テナント用 LCS 接続 のコンフィギュレーション (<bpt id="p1">[</bpt>プラットフォーム更新プログラム 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configurelcs)</ept> または <bpt id="p2">[</bpt>プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#configurelcs)</ept> で記載されたものとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="728">
          <source>You must complete this task only one time for the tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テナントに対して、このタスクを 1 回のみ実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="729">
          <source>Configure AD FS (as documented for <bpt id="p1">[</bpt>Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configureadfs)</ept> or <bpt id="p2">[</bpt>Platform update 8 and Platform update 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#configureadfs)</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS のコンフィギュレーション (<bpt id="p1">[</bpt>プラットフォーム更新プログラム 12<ept id="p1">](setup-deploy-on-premises-pu12.md#configureadfs)</ept> または <bpt id="p2">[</bpt>プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11<ept id="p2">](setup-deploy-on-premises-pu8-pu11.md#configureadfs)</ept> で記載されたものとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="730">
          <source>You can skip scripts 1, 2, and 3, because they have already been done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すでに完了しているので、スクリプト 1、スクリプト 2、スクリプト 3 はスキップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="731">
          <source>The .<ph id="ph1">\\</ph>Publish-ADFSApplicationGroup.ps1 script will fail even when the new <bpt id="p1">**</bpt>hosturl<ept id="p1">**</ept> value is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい <bpt id="p1">**</bpt>hosturl<ept id="p1">**</ept> 値を使用している場合でも、.<ph id="ph1">\\</ph>Publish-ADFSApplicationGroup.ps1 スクリプトは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="732">
          <source>Therefore, you must manually complete these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この手順を手動で完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="733">
          <source>In AD FS Manager, go to <bpt id="p1">**</bpt>AD FS<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Application groups<ept id="p2">**</ept>, and open <bpt id="p3">**</bpt>Microsoft Dynamics 365 for Operations On-premises<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS マネージャーで、<bpt id="p1">**</bpt>AD FS<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>アプリケーション グループ<ept id="p2">**</ept>に移動し、<bpt id="p3">**</bpt>Microsoft Dynamics 365 for Operations オンプレミス<ept id="p3">**</ept>を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="734">
          <source>Open the <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations On-premises - Native application<ept id="p1">**</ept> native application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations  オンプレミス - ネイティブ アプリケーション<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="735">
          <source>Add the redirect URI of the new environment (DNS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境 (DNS) の リダイレクト URI を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="736">
          <source>Open the <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations On-premises - Financial Reporting - Native application<ept id="p1">**</ept> native application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 - ネイティブ アプリケーション<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="737">
          <source>Add the redirect URI of the new environment (DNS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境 (DNS) の リダイレクト URI を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="738">
          <source>Open the <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations On-premises - Web API<ept id="p1">**</ept> Web API.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations オンプレミス - Web AP I<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="739">
          <source>Add the two entries of the redirect URI of the new environment (DNS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境 (DNS) のリダイレクト URI の 2 つのエントリを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="740">
          <source>Open the <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations On-premises - Financial Reporting Web API<ept id="p1">**</ept> Web API.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 Web API<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="741">
          <source>Add the redirect URI of the new environment (DNS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境 (DNS) の リダイレクト URI を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="742">
          <source>Redeploy SSRS reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSRS レポートを再配置する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="743">
          <source>Delete the entry in SF.SyncLog, and then restart one of the AOS machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SF.SyncLog のエントリを削除して、AOS マシンの 1 つを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="744">
          <source>The AOS machine will rerun DB Sync and then deploy reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS コンピューターは DB 同期を再実行し、レポートを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="745">
          <source>Add axdbadmin to tempdb after a SQL Server restart via a stored procedure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストアド プロシージャ経由で SQL Server を再起動した後、tempdb に axdbadmin を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="746">
          <source>When SQL Server is restarted, the tempdb database is re-created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server を再起動すると、tempdb データベースが再作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="747">
          <source>Therefore, there will be missing permissions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、アクセス許可が不十分です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="748">
          <source>Run the following script to create a stored procedure on the master database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター データベースでストアド プロシージャを作成する次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="749">
          <source>Error: "Updates to existing credential with KeyId '<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>' is not allowed"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー、「KeyId『<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>』による既存の資格情報の更新は許可されていません」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="750">
          <source>You might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のエラーが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="751">
          <source>Updates to existing credential with KeyId '<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>' is not allowed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KeyId「<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>」を保持している既存の資格情報を更新することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="752">
          <source>The steps to resolve this issue depend on whether you have only an on-premises project, or whether you have both an online project and an on-premises project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するための手順は、オンプレミス プロジェクトのみをご利用しているか、オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用しているかによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="753">
          <source>If have only an on-premises project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合設置プロジェクトのみ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="754">
          <source>If have only an on-premises project, you can't update the existing credential with KeyId '<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス プロジェクトのみの場合は、KeyId '<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>' を保持している既存の資格情報を更新することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="755">
          <source>New-AzureRmADSpCredential : Update to existing credential with KeyId '<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>' is not allowed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">New-AzureRmADSpCredential : KeyId '<ph id="ph1">\&lt;</ph>key<ph id="ph2">\&gt;</ph>' による既存の資格情報の更新は許可されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="756">
          <source>At C:<ph id="ph1">\\</ph>InfrastructureScripts<ph id="ph2">\\</ph>Add-CertToServicePrincipal.ps1:62 char:1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">At C:<ph id="ph1">\\</ph>InfrastructureScripts<ph id="ph2">\\</ph>Add-CertToServicePrincipal.ps1:62 char:1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="757">
          <source>New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="758">
          <source>CategoryInfo : InvalidOperation: (:) <ph id="ph1">\[</ph>New-AzureRmADSpCredential<ph id="ph2">\]</ph>, Exception</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CategoryInfo : InvalidOperation: (:) <ph id="ph1">\[</ph>New-AzureRmADSpCredential<ph id="ph2">\]</ph>, Exception</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="759">
          <source>FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="760">
          <source>Run the following PowerShell command to resolve the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、次の PowerShell コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="761">
          <source>If you have both an online project and an on-premises project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="762">
          <source>If you have both an online project and an on-premises project, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合は、次の手順に従ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="763">
          <source>Verify that the Microsoft .NET Framework version 4.7.2 is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft .NET フレームワーク version 4.7.2 がインストールされていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="764">
          <source>Run the following Windows PowerShell script to install the Azure PowerShell module.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のWindows PowerShell スクリプトを実行し、Azure PowerShell moduleをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="765">
          <source>Run the following Windows PowerShell script to upload the new certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のWindows PowerShellスクリプトを実行し、新規証明書をアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="766">
          <source>Run the following command to remove the duplicate certificate, if more than one certificate exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の証明書が存在する場合は、以下のコマンドを実行して重複する証明書を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="767">
          <source>ODBC driver 17 is required for platform updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォームの更新には ODBC ドライバー 17 が必要です</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="768">
          <source>The latest platform binary update uses Open Database Connectivity (ODBC) driver 17.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム バイナリを最新に更新するには、Open Database Connectivity ODBC ドライバー 17 を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="769">
          <source>This upgrade resolves stability issues that are linked to older ODBC drivers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアップグレードでは、古いバージョンの ODBC ドライバーに関連する安定性の問題を修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="770">
          <source>The <bpt id="p1">[</bpt>Setup perquisites<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites)</ept> documentation has been updated to reflect the change in which ODBC driver 17 must be installed on each AOS server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>追加の設定<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites)</ept> に関するドキュメントが更新されており、次の変更が記載されています。各AOSサーバーにはODBC ドライバー 17 がインストールされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="771">
          <source>If you don't install ODBC driver 17, you will receive DB Sync errors during servicing of the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ODBC ドライバー 17 をインストールしない場合は、環境のメンテナンス処理中に DB 同期エラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="772">
          <source>Here are some examples of errors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="773">
          <source>In Service Fabric:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric で:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="774">
          <source>Unhealthy event: SourceId='System.RA', Property='ReplicaOpenStatus', HealthState='Warning', ConsiderWarningAsError=false.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題のあるイベント: SourceId=「System.RA」、プロパティ =「ReplicaOpenStatus」、HealthState=「警告」、ConsiderWarningAsError=false。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="775">
          <source>Replica had multiple failures during open on AOS3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レプリカで、AOS3 で開いているときに複数の障害が発生しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="776">
          <source>API call: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API 呼び出し: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="777">
          <source><bpt id="p1">**</bpt>DB sync failed.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DB の同期に失敗しました。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="778">
          <source>On AOS machines:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS コンピューターで:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="779">
          <source>Event Viewer <ph id="ph1">\&gt;</ph> Custom Views <ph id="ph2">\&gt;</ph> Administrative Events:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ビューアー <ph id="ph1">\&gt;</ph> カスタム ビュー <ph id="ph2">\&gt;</ph> 管理イベント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="780">
          <source>Application: Microsoft.Dynamics.AX.Deployment.Setup.exe Framework Version: v4.0.30319 Description: The process was terminated due to an unhandled exception.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション: Microsoft.Dynamics.AX.Deployment.Setup.exe フレームワーク バージョン: v4.0.30319 説明: プロセスは未処理の例外によって中止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="781">
          <source>Exception Info: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String<ph id="ph1">\[</ph><ph id="ph2">\]</ph>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外情報: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String<ph id="ph1">\[</ph><ph id="ph2">\]</ph>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="782">
          <source>C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOSx<ph id="ph4">\\</ph>Fabric<ph id="ph5">\\</ph>work<ph id="ph6">\\</ph>Applications<ph id="ph7">\\</ph>AXSFType<ph id="ph8">\_</ph>Appxx<ph id="ph9">\\</ph>log:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOSx<ph id="ph4">\\</ph>Fabric<ph id="ph5">\\</ph>work<ph id="ph6">\\</ph>Applications<ph id="ph7">\\</ph>AXSFType<ph id="ph8">\_</ph>Appxx<ph id="ph9">\\</ph>log:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="783">
          <source>Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOS1<ph id="ph4">\\</ph>Fabric<ph id="ph5">\\</ph>work<ph id="ph6">\\</ph>Applications<ph id="ph7">\\</ph>AXSFType<ph id="ph8">\_</ph>App18<ph id="ph9">\\</ph>AXSF.Code.1.0.20180831174152<ph id="ph10">\\</ph>Packages" -metadatadir "C:<ph id="ph11">\\</ph>ProgramData<ph id="ph12">\\</ph>SF<ph id="ph13">\\</ph>AOS1<ph id="ph14">\\</ph>Fabric<ph id="ph15">\\</ph>work<ph id="ph16">\\</ph>Applications<ph id="ph17">\\</ph>AXSFType<ph id="ph18">\_</ph>App18<ph id="ph19">\\</ph>AXSF.Code.1.0.20180831174152<ph id="ph20">\\</ph>Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOS1<ph id="ph4">\\</ph>Fabric<ph id="ph5">\\</ph>work<ph id="ph6">\\</ph>Applications<ph id="ph7">\\</ph>AXSFType<ph id="ph8">\_</ph>App18<ph id="ph9">\\</ph>AXSF.Code.1.0.20180831174152<ph id="ph10">\\</ph>Packages" -metadatadir "C:<ph id="ph11">\\</ph>ProgramData<ph id="ph12">\\</ph>SF<ph id="ph13">\\</ph>AOS1<ph id="ph14">\\</ph>Fabric<ph id="ph15">\\</ph>work<ph id="ph16">\\</ph>Applications<ph id="ph17">\\</ph>AXSFType<ph id="ph18">\_</ph>App18<ph id="ph19">\\</ph>AXSF.Code.1.0.20180831174152<ph id="ph20">\\</ph>Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="784">
          <source>Unhandled Exception: System.IO.FileNotFoundException: <bpt id="p1">**</bpt>Could not load file or assembly 'aoskernel.dll' or one of its dependencies. The specified module could not be found.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドルされない例外: System.IO.FileNotFoundException: <bpt id="p1">**</bpt>ファイルまたはアセンブリ 'aoskernel.dll'、あるいはその依存関係のうちのいずれか 1 つを読み込めませんでした。指定されたモジュールが見つかりませんでした。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="785">
          <source>at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String<ph id="ph1">\[</ph><ph id="ph2">\]</ph> args)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String<ph id="ph1">\[</ph><ph id="ph2">\]</ph> args) にて</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="786">
          <source><bpt id="p1">**</bpt>DB sync failed.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DB の同期に失敗しました。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="787">
          <source>A "No subscription found in the context" error occurs when you run Add-CertToServicePrincipal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Add-CertToServicePrincipal を実行すると、"コンテキストにサブスクリプションが見つかりません" エラーが発生します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="788">
          <source>Recent versions of Windows PowerShell might cause a "No subscription found in the context" error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新バージョンの Windows PowerShell が原因で "コンテキストにサブスクリプションが見つかりません" エラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="789">
          <source>To resolve this issue, install and load an older version of Windows PowerShell, such as version 5.7.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、Windows PowerShellのバージョン5.7.0などの古いバージョンをインストールし、上書きしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="790">
          <source>Service Fabric Explorer warnings occur after you restart a machine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターの再起動後に Service Fabric Explorer の警告メッセージが表示される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="791">
          <source><bpt id="p1">**</bpt>Error:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="792">
          <source>Error event: SourceId='MonitoringAgentService', Property='ServiceState'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: event: SourceId='MonitoringAgentService', Property='ServiceState'.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="793">
          <source>System.Management.Automation.RuntimeException: Error: <bpt id="p1">**</bpt>The GUID passed was not recognized as valid by a WMI data provider.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">System.Management.Automation.RuntimeException: エラー: <bpt id="p1">**</bpt>渡された GUID は WMI データ プロバイダーにより有効と認識されませんでした。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="794">
          <source>(Exception from HRESULT: 0x80071068).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(HRESULT からの例外: 0x80071068)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="795">
          <source>Stack trace:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタック トレース:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="796">
          <source><bpt id="p1">**</bpt>Steps:<ept id="p1">**</ept> To resolve this issue, restart the application package that generated the warning message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>手順:<ept id="p1">**</ept> この問題を解決するには、警告メッセージの原因であるアプリケーション パッケージを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="797">
          <source>For more information, see <bpt id="p1">[</bpt>Restart applications (such as AOS)<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/troubleshoot-on-prem#restart-applications-such-as-aos)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳しくは、 <bpt id="p1">[</bpt>アプリケーション(AOS など)を再起動してください<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/troubleshoot-on-prem#restart-applications-such-as-aos)</ept> をご覧ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="798">
          <source>The internal time zone version number that is stored in the database is higher than the version that is supported by the kernel (13/12)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースに格納されている内部タイム ゾーンのバージョン番号が、カーネル (13/12) でサポートされているバージョンよりも大きくなっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="799">
          <source>This database synchronization error can cause an old platform build (Platform update 12) to be deployed on top of a database that had a newer build (Platform update 15).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベースの同期エラーにより、新しいビルド (プラットフォーム更新 15) があったデータベースの上に古いプラットフォーム ビルド (プラットフォーム更新 12) が配置されてしまう可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="800">
          <source>To resolve this issue, note the <bpt id="p1">**</bpt>SYSTIMEZONESVERSION<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、 <bpt id="p1">**</bpt>SYSTIMEZONESVERSION<ept id="p1">**</ept> の値が重要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="801">
          <source>Update the value to the version that was returned in the error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージにて表示されたバージョンの値で [value] を更新します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="802">
          <source>Printing randomly stops</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">印刷がランダムに停止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="803">
          <source>Make sure that all network printers that have been installed on the AOS server are running as the Windows service account that the AXService.EXE process is running as.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS サーバーにインストールされているすべてのネットワーク プリンターが、AXService.EXE プロセスが実行されている Windows サービス アカウントとして実行されていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="804">
          <source>Ax-DatabaseSynchronize isn't populated with events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ax-DatabaseSynchronize にイベントが設定されていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="805">
          <source>In Platform update 20 and later, there is database synchronization log issue where the synchronization logs aren't written under <bpt id="p1">**</bpt>Ax-DatabaseSynchronize<ept id="p1">**</ept> in Event Viewer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォームの更新 20 およびそれ以降では、データベース同期ログに問題があり、イベント ビューアーで同期ログが <bpt id="p1">**</bpt>Ax-DatabaseSynchronize<ept id="p1">**</ept> の下に作成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="806">
          <source>To resolve this issue, go to <ph id="ph1">\&lt;</ph>SF-dir<ph id="ph2">\&gt;</ph><ph id="ph3">\\</ph>AOS<ph id="ph4">\_</ph><ph id="ph5">\&lt;</ph>x<ph id="ph6">\&gt;</ph><ph id="ph7">\\</ph>Fabric<ph id="ph8">\\</ph>work<ph id="ph9">\\</ph>Applications<ph id="ph10">\\</ph>AXSFType<ph id="ph11">\_</ph>App<ph id="ph12">\&lt;</ph>X<ph id="ph13">\&gt;</ph><ph id="ph14">\\</ph>log.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、 <ph id="ph1">\&lt;</ph>SF-dir<ph id="ph2">\&gt;</ph><ph id="ph3">\\</ph>AOS<ph id="ph4">\_</ph><ph id="ph5">\&lt;</ph>x<ph id="ph6">\&gt;</ph><ph id="ph7">\\</ph>Fabric<ph id="ph8">\\</ph>work<ph id="ph9">\\</ph>Applications<ph id="ph10">\\</ph>AXSFType<ph id="ph11">\_</ph>App<ph id="ph12">\&lt;</ph>X<ph id="ph13">\&gt;</ph><ph id="ph14">\\</ph>log に移動してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="807">
          <source>For example, go to C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOS<ph id="ph4">\_</ph>11<ph id="ph5">\\</ph>Fabric<ph id="ph6">\\</ph>work<ph id="ph7">\\</ph>Applications<ph id="ph8">\\</ph>AXSFType<ph id="ph9">\_</ph>App183<ph id="ph10">\\</ph>log.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例えば次の場所に移動します。 C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>SF<ph id="ph3">\\</ph>AOS<ph id="ph4">\_</ph>11<ph id="ph5">\\</ph>Fabric<ph id="ph6">\\</ph>work<ph id="ph7">\\</ph>Applications<ph id="ph8">\\</ph>AXSFType<ph id="ph9">\_</ph>App183<ph id="ph10">\\</ph>log</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="808">
          <source>Here, you can see the output from DatabaseSynchronize in the Code<ph id="ph1">\_</ph>AXSF<ph id="ph2">\_</ph>M<ph id="ph3">\_</ph><ph id="ph4">\&lt;</ph>X<ph id="ph5">\&gt;</ph>.out files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、DatabaseSynchronize からの出力された内容を確認できます。 Code<ph id="ph1">\_</ph>AXSF<ph id="ph2">\_</ph>M<ph id="ph3">\_</ph><ph id="ph4">\&lt;</ph>X<ph id="ph5">\&gt;</ph>.out files.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="809">
          <source>Troubleshoot any issues that pertain to this component.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンポーネントに関する問題をトラブルシューティングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="810">
          <source>You can't access Finance and Operations: "AADSTS50058: A silent sign-in request was sent but no user is signed in"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations にアクセスできません: 「AADSTS50058: サイレント サインインの要求が送信されましたが、ログインしているユーザーがいません」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="811">
          <source>After a user enters credentials to sign in to Finance and Operations, the browser briefly shows the application layout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations へのログイン資格情報を入力すると、ブラウザでアプリケーションのレイアウトが少しの間表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="812">
          <source>However, it then tries to redirect outside Finance and Operations, but fails with the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しかしその後、Finance and Operations外部へのリダイレクトを試みた結果、次のエラーが出て失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="813">
          <source>AADSTS50058: A silent sign-in request was sent but no user is signed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AADSTS50058: サイレント サインイン要求が送信されましたが、ユーザーがログインしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="814">
          <source>The cookies that represent the user's session weren't sent in the request to Azure AD.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーのセッションを表すために使用する Cookie が Azure AD への要求で送信されませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="815">
          <source>This issue can occur if the user is using Internet Explorer or Microsoft Edge, and if the web app that sends the silent sign-in request is in a different IE security zone than the Azure AD endpoint (login.microsoftonline.com).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、 Internet Explorer または Microsoft Edge を使用している場合で、webアプリケーションが送信しているサイレント サインインのリクエストが Azure AD エンドポイント (login.microsoftonline.com)とは異なる IEのセキュリティ ゾーンに設定されている場合に発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="816">
          <source>This issue occurs because there was a change in the Skype Presence API, and on-premises environments connect to this API by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、次の PowerShell コマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="817">
          <source>To resolve the issue, run the following SQL Server query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、次の SQL Server query を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="818">
          <source>Alternatively, turn off the <bpt id="p1">**</bpt>Skype presence enabled<ept id="p1">**</ept> option on the <bpt id="p2">**</bpt>Client performance options<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>System administration<ept id="p3">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p4">**</bpt>Setup<ept id="p4">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p5">**</bpt>Client performance options<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、<bpt id="p2">**</bpt>クライアント パフォーマンス オプション<ept id="p2">**</ept> ページの <bpt id="p1">**</bpt>Skype プレゼンスが有効<ept id="p1">**</ept> オプションを無効にします (<bpt id="p3">**</bpt>システム管理<ept id="p3">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p4">**</bpt>設定<ept id="p4">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p5">**</bpt>クライアント パフォーマンス オプション<ept id="p5">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="819">
          <source>To use this approach, you must be able to sign in to Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法を使用するには、Finance and Operations にログインできる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="820">
          <source>Therefore, you must first block redirection in the browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、最初にブラウザのリダイレクトをブロックする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="821">
          <source>After you disable the Skype presence, you can unblock redirection again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skypeのプレゼンス機能を無効にすると、リダイレクトのブロックを解除しても構いません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="822">
          <source>The Google Chrome browser blocks redirection by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chrome ブラウザーでは、最初からリダイレクトがブロックされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="823">
          <source>Error: "There was an error during CodePackage activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: CodePackage の有効化でエラーが発生しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="824">
          <source>Service host failed to activate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス ホストの有効化に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="825">
          <source>Error:0x8007052e"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: 0x8007052e"</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="826">
          <source>You might receive the following error during a new installation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新規インストールの際に以下のエラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="827">
          <source>Error event: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー イベント: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="828">
          <source>There was an error during CodePackage activation.Service host failed to activate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CodePackage の有効化でエラーが発生しました。サービス ホストの有効化に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="829">
          <source>Error:0x8007052e</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: 0x8007052e</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="830">
          <source>This error will cause the AXSF service to fail with the same error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーと同じエラーが、AXSFサービスでも発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="831">
          <source>To resolve this issue, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="832">
          <source>In the <bpt id="p1">[</bpt>agent share path<ept id="p1">](setup-deploy-on-premises-pu12.md#setupfile)</ept>, find the <bpt id="p2">**</bpt>netstandard.dll<ept id="p2">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>エージェント共有パス<ept id="p1">](setup-deploy-on-premises-pu12.md#setupfile)</ept> にて、 <bpt id="p2">**</bpt>netstandard.dll<ept id="p2">**</ept> ファイルを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="833">
          <source>For example, this file might be at <ph id="ph1">\\</ph>wp<ph id="ph2">\\</ph><ph id="ph3">\&lt;</ph>name<ph id="ph4">\&gt;</ph><ph id="ph5">\\</ph>StandaloneSetup-<ph id="ph6">\&lt;</ph>ver<ph id="ph7">\&gt;</ph><ph id="ph8">\\</ph>Apps<ph id="ph9">\\</ph>AOS<ph id="ph10">\\</ph>AXServiceApp<ph id="ph11">\\</ph>AXSF<ph id="ph12">\\</ph>Code<ph id="ph13">\\</ph>bin<ph id="ph14">\\</ph>netstandard.dll.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、例えば <ph id="ph1">\\</ph>wp<ph id="ph2">\\</ph><ph id="ph3">\&lt;</ph>名<ph id="ph4">\&gt;</ph><ph id="ph5">\\</ph>StandaloneSetup -<ph id="ph6">\&lt;</ph>バージョン<ph id="ph7">\&gt;</ph><ph id="ph8">\\</ph>アプリケーション<ph id="ph9">\\</ph>AOS<ph id="ph10">\\</ph>AXServiceApp<ph id="ph11">\\</ph>AXSF<ph id="ph12">\\</ph>コード<ph id="ph13">\\</ph>在庫置場<ph id="ph14">\\</ph>netstandard.dll に多くの場合存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="834">
          <source>On each AOS server, open a Command Prompt window as an administrator, and run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それぞれの AOS サーバーにて、管理者権限で コマンド プロンプトを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="835">
          <source>Delete <bpt id="p1">**</bpt>AXBootstrapperApp<ept id="p1">**</ept> from Service Fabric.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric から <bpt id="p1">**</bpt>AXBootstrapperApp<ept id="p1">**</ept> を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="836">
          <source>Delete the <bpt id="p1">**</bpt>fabric:/Bootstrapper/AXBootstrapper<ept id="p1">**</ept> service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>fabric:/Bootstrapper/AXBootstrapper<ept id="p1">**</ept> サービス を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="837">
          <source>Delete the <bpt id="p1">**</bpt>fabric:/Bootstrapper<ept id="p1">**</ept> application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>fabric:/Bootstrapper<ept id="p1">**</ept> アプリケーションを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="838">
          <source>Unprovision the <bpt id="p1">**</bpt>AXBootstrapperAppType<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AXBootstrapperAppType<ept id="p1">**</ept> のプロヴィジョニングを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="839">
          <source>Redeploy the environment from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS から環境を再配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="840">
          <source>SQL Server 2016 service pack 2 is recommended for Reporting Services instances</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Servicesのインスタンス には SQL Server 2016 service pack 2 を推奨します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="841">
          <source>When you go through LCS servicing operations, you might receive the following error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCSにてサービス操作を行うと次のエラーが表示されることがあります:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="842">
          <source>The process cannot access the file 'C:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft SQL Server<ph id="ph3">\\</ph>MSRS13.MSSQLSERVER<ph id="ph4">\\</ph>Reporting Services<ph id="ph5">\\</ph>ReportServer<ph id="ph6">\\</ph>bin<ph id="ph7">\\</ph>Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' because it is being used by another process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスが次のファイルにアクセスできません ' c:<ph id="ph1">\\</ph>Program Files<ph id="ph2">\\</ph>Microsoft SQL Server<ph id="ph3">\\</ph>MSRS13.MSSQLSERVER<ph id="ph4">\\</ph>Reporting Services<ph id="ph5">\\</ph>ReportServer<ph id="ph6">\\</ph>bin<ph id="ph7">\\</ph>Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' 別のプロセスによって使用されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="843">
          <source>This issue occurs because Reporting Services has a lock on a Microsoft Dynamics .dll file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は Reporting Services が Microsoft Dynamics .dllファイル をロックしているために発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="844">
          <source>We currently recommend that you have SQL Server 2016 service pack 2 installed on Reporting Services instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Servicesのインスタンスには、SQL Server 2016 service pack 2をインストールすることを推奨しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="845">
          <source>You must have service pack 2 installed, and no additional cumulative updates or hotfixes must be installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス パック2のインストールが必要し、累積的な更新を追加または修正プログラムをインストールする必要がないです。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>