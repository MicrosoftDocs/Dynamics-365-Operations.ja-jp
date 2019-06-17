<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="on-premises-diagnostics.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>on-premises-diagnostics.0959e1.06e7388ccca731996b705ec70aa8367091cc5ab7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>06e7388ccca731996b705ec70aa8367091cc5ab7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\deployment\on-premises-diagnostics.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>On-premises diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス診断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to expose the diagnostic data for on-premises deployments of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置の診断データを公開するための情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>On-premises diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス診断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The Microsoft Dynamics 365 for Finance and Operations team monitors the health and performance of the Azure Services that provide functionality for our cloud-based customers by using state-of-the-art Azure diagnostic tools.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations は、最新式の Azure Diagnostic Tool を使用して、クラウド ベースの顧客の機能を提供する Azure Services の正常性およびパフォーマンスを監視します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For customers who have implemented Finance and Operations on-premises and would like to have the ability to monitor the health and performance of their on-premises solution, there are several third-party offerings available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations オンプレミスで実装し、オンプレミス ソリューションの正常性とパフォーマンスを監視できるようにするには、いくつかのサード パーティ製品が利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic describes the setup and configuration of Elastic Stack, a third-party product, and one of many choices that can provide  diagnostic monitoring of your on-premises solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Elastic Stack の設定とコンフィギュレーション、サード パーティ製品、およびオンプレミス ソリューションの診断モニタリングを提供できる多くの選択肢の 1 つについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When you consider a diagnostic solution, consider the following fundamentals of your implementation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">診断ソリューションを検討する際、次の実装の基礎を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Your diagnostic system should be able to collect and store 30 days' worth of diagnostic information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">診断システムは、30 日分に相当する診断情報を収集し、格納できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Your diagnostic repository should be set up in a central location that is sharable among many client computers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">診断リポジトリは、多くのクライアント コンピューターで共有できるように中心的な場所に設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Create structured diagnostics events, including event type, classification, and data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント タイプ、分類、およびデータを含む構造化診断イベントを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Events stored in raw text (deserialized) can be easily queried and searched.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未加工のテキスト (逆シリアル化) に格納されているイベントを簡単に照会および検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Avoid storing sensitive or personal data in events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントに機密情報や個人データを格納しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>By default, communication in an Elastic Stack cluster is not sent over HTTPS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、Elastic Stack クラスター内の通信は HTTPS 経由で送信されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Don't set up the Elastic Stack unless you've considered the risks, and prepared or implemented mitigations for those risks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リスクを考慮し、それらのリスクの軽減策を準備または実装していない限り、Elastic スタックを設定しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The paid version of X-Pack can be used to encrypt communication in the Elastic Stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack の支払済バージョン は、Elastic Stack のコミュニケーションを暗号化するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For setup information, see Setting up TLS on a cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定の詳細については、クラスタでの TLS の設定を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>There is also an open source Elasticsearch plug-in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オープン ソース Elasticsearch プラグイン もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Although Microsoft hasn't tested this plug-in, according to the documentation, it can enable HTTPS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントによると、Microsoft はこのプラグインをテストしていませんが、HTTPS を有効にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Microsoft recommends that you always utilize encrypted communication using HTTPs, VPN, or another secure, encrypted protocol.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft では、HTTPs、VPN、または別のセキュリティで保護された、暗号化されたプロトコルを使用して、暗号化された通信を常に使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Many industry certifications and laws require the use of encrypted transmission if your content includes end user, customer, personal, or sensitive data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテンツにエンド ユーザー、顧客、個人または機密データが含まれている場合、多くの業界認定および法律では、暗号化された送信を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Diagnostic data guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">診断データのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>To diagnose the deployment and execution of Microsoft Dynamics 365 for Finance and Operations, you must have access to diagnostic data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations の配置と実行を診断するためには、診断データへのアクセスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For a cloud deployment, Microsoft stores and monitors the diagnostic data from services to help keep the environment healthy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウドの配置では、マイクロソフトは、サービスの診断データを保存して監視し、環境を健全に保ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>For an on-premises deployment, the customer is responsible for this task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置に関しては、顧客がこのタスクを担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can select the diagnostic data store and query tool that you prefer to use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用したい診断データ ストアおよびクエリ ツールを選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>However, at a minimum, the tool should perform the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、最低限、ツールは、次のタスクを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The store should be able to store 30 days' worth of diagnostic data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストアは、30 日間分の診断データを格納できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The events should be stored in a centralized location, so that support engineers don't have to switch between multiple machines to find events that are relevant to an issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントが集約される場所に格納されると、サポート エンジニアは問題に関連するイベントを検索する複数のマシン間を切り替える必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The events should be discoverable based on event type and event data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントは、イベント タイプおよびイベント データに基づいて、発見が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The event data (in XML format) should be deserialized so that the event data can be queried on and traversed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント データ (XML 形式) では、逆シリアル化すると、イベント データを照会および移動が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Elastic Stack example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elastic スタックの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>To meet the diagnostic data guidelines that are listed in the previous section, Microsoft tested the Elastic Stack setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションに表示されている診断データのガイドラインを満たすため、Microsoft は Elastic スタックの設定をテストしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>This setup includes the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定には次のコンポーネントが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Elasticsearch<ept id="p1">**</ept> – For storage, event indexing, and event querying.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Elasticsearch<ept id="p1">**</ept> – ストレージ、イベント インデックス作成、およびイベント クエリの実行。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For more information about Elasticsearch, see the <bpt id="p1">[</bpt>Elastic website<ept id="p1">](https://www.elastic.co/products/elasticsearch)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elasticsearch の詳細については、<bpt id="p1">[</bpt>Elastic Web サイト<ept id="p1">](https://www.elastic.co/products/elasticsearch)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Logstash<ept id="p1">**</ept> – For load distribution and event data transformation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Logstash<ept id="p1">**</ept> – 負荷分散およびイベント データ変換用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Winlogbeat<ept id="p1">**</ept> – For diagnostic data collection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Winlogbeat<ept id="p1">**</ept> – 診断データ収集用。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Kibana<ept id="p1">**</ept> – An interface for querying the data that is stored in Elasticsearch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Kibana<ept id="p1">**</ept> – Elasticsearch に格納されているデータを照会するためのインタフェース。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>By default, communication in an Elastic Stack cluster is <bpt id="p1">**</bpt>not<ept id="p1">**</ept> sent over HTTPS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、Elastic Stack クラスター内の通信は HTTPS 経由で送信され<bpt id="p1">**</bpt>ない<ept id="p1">**</ept>ようになっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Don't set up the Elastic Stack unless you've considered the risks, and prepared or implemented mitigations for those risks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リスクを考慮し、それらのリスクの軽減策を準備または実装していない限り、Elastic スタックを設定しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The <bpt id="p1">[</bpt>paid version<ept id="p1">](https://www.elastic.co/subscriptions)</ept> of X-Pack can be used to encrypt communication in the Elastic Stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack の<bpt id="p1">[</bpt>支払済バージョン<ept id="p1">](https://www.elastic.co/subscriptions)</ept> は、Elastic Stack のコミュニケーションを暗号化するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For setup information, see <bpt id="p1">[</bpt>Setting up TLS on a cluster<ept id="p1">](https://www.elastic.co/guide/en/x-pack/current/ssl-tls.html)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定の詳細については、<bpt id="p1">[</bpt>クラスタでの TLS の設定<ept id="p1">](https://www.elastic.co/guide/en/x-pack/current/ssl-tls.html)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>There is also an open source <bpt id="p1">[</bpt>Elasticsearch plug-in<ept id="p1">](https://github.com/floragunncom/search-guard-ssl)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オープン ソース <bpt id="p1">[</bpt>Elasticsearch プラグイン<ept id="p1">](https://github.com/floragunncom/search-guard-ssl)</ept> もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Although Microsoft hasn't tested this plug-in, according to the documentation, it can enable HTTPS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントによると、Microsoft はこのプラグインをテストしていませんが、HTTPS を有効にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If you deploy the Elastic Stack, your experience might vary if you follow the steps that are described in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elastic スタックを展開する場合、このトピックで説明されている手順を実行するなら異なる経験になるかもしれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For its tests, Microsoft used version 6.2.3 of the Elastic Stack components and Microsoft Dynamics 365 for Finance and Operations 7.3 with platform update 12.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストでは、Microsoft は、Elastic Stack コンポーネントのバージョン 6.2.3 と、Microsoft Dynamics 365 for Finance and Operations 7.3 およびプラットフォーム更新プログラム 12 を使用しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>This topic describes how Microsoft handled the setup and configuration steps that are required for the Elastic Stack to work for a on-premises deployment of Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Elastic Stack が Finance and Operations のオンプレミス配置のために動作するために必要な設定、およびコンフィギュレーションの手順を Microsoft がどのように処理したかについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>For guidance that isn't related to Finance and Operations, see the documentation on Elastic.co.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations に関連していないガイダンスについては、Elastic.co のドキュメントを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Install and configure the Elastic Stack</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elastic スタックのインストールと構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>All hosted components of the Elastic Stack, except Winlogbeat, run on Java.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat を除くすべての Elastic スタックのホストされているコンポーネントはすべて Java 上で動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>For the test scenario, Microsoft first downloaded and installed the latest version of Java Runtime Environment (JRE) 8 (64-bit) on each node that will run Elasticsearch, Logstash, or Kibana (that is, all the Orchestrator nodes).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト シナリオでは、Microsoft は最初に Elasticsearch、Logstash、または Kibana (つまり、すべてのオーケストレータ ノード) を実行する各ノードに、Java ランタイム環境 (JRE) 8 (64 ビット) の最新バージョンをダウンロードしてインストールしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>You can get Java 8 from <bpt id="p1">[</bpt><ph id="ph1">https://www.oracle.com/technetwork/java/javase/downloads/index.html</ph><ept id="p1">](https://www.oracle.com/technetwork/java/javase/downloads/index.html)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">https://www.oracle.com/technetwork/java/javase/downloads/index.html</ph><ept id="p1">](https://www.oracle.com/technetwork/java/javase/downloads/index.html)</ept> から Java 8 を取得することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>As of June 2018, the Elastic Stack runs on Java 8.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2018 年 6 月現在、Elastic スタックは Java 8 で実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Any attempt to run it on a newer version of Java might not work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Java の新しいバージョンで実行しようとすると、すべてが動作しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The whole Elastic Stack, except Winlogbeat, can be hosted on Linux.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Linux では、Winlogbeat を除く、全体の Elastic Stack をホストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>For its tests, Microsoft hosted the stack on Microsoft Windows Server 2016 virtual machines (VMs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストでは、Microsoft が Microsoft Windows サーバー 2016 の仮想マシン (Vm) のスタックをホストしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Remember to open ports in the firewall for the various components on each node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ノード上のさまざまなコンポーネントのファイアウォールで、ポートを開くことを忘れないようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>If you get stuck during setup, Elastic.co has extensive and well-written documentation about the installation and configuration of the Elastic Stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定中に行き詰まった場合、Elastic.co には Elastic スタックのインストールとコンフィギュレーションについての広範かつ適切なドキュメントがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>For help with specific types of errors, web searches yield reliable results from both the Elastic.co forum and StackOverflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のタイプのエラーについては、Web 検索で Elastic.co フォーラムと StackOverflow の両方から信頼性の高い結果が得られます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Component matrix</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントのマトリックス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For its tests, Microsoft used the following setup for a small to medium-sized Finance and Operations deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストでは、マイクロソフトは、小規模から中規模の Finance and Operations 配置用の次の設定を使用しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Node</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Elasticsearch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elasticsearch</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Logstash</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logstash</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Kibana</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Winlogbeat</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Orchestrator #1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ #1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Orchestrator #2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ #2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Orchestrator #3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ #3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>AOS #1...<bpt id="p1">*</bpt>n<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS #1...<bpt id="p1">*</bpt>n<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>For testing purposes, Microsoft used the Orchestrator machines for the ELK installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、テスト目的で、ELK インストールのために オーケストレータ機械を使用しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Because it can take up critical resources from the Orchestration services, don't use the Orchestrator machines for ELK installations on production environments or critical Sandbox Environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレーション サービスから重要なリソースを奪う可能性があるため、実稼動環境または重要なサンドボックス環境で ELK のインストールにオーケストレータ マシンを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Instead, use separate machines to host the ELK services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、別のマシンを使用して ELK サービスをホストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Elasticsearch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elasticsearch</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The installation of Elasticsearch is fairly straightforward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elasticsearch のインストールは、非常に簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>For its tests, Microsoft downloaded the <bpt id="p1">[</bpt>Microsoft Windows Installer (MSI) file<ept id="p1">](https://www.elastic.co/downloads/elasticsearch)</ept> onto the Orchestrator #1 and Orchestrator #2 nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストでは、Microsoft が、「<bpt id="p1">[</bpt>Microsoft Windows インストーラー (MSI) ファイル<ept id="p1">](https://www.elastic.co/downloads/elasticsearch)</ept>」をオーケストレータ #1 および オーケストレータ #2 ノードにダウンロードしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Most of the default settings in the installer can be left as is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラの既定の設定のほとんどはそのままにしておくことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>This section describes the settings that Microsoft changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、Microsoft が変更した設定について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>To facilitate Elasticsearch to start running again if the operating system (OS) is restarted, Microsoft installed it as a service on Windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オペレーティング システム (OS) が再起動された場合に、Elasticsearch がもう一度実行を開始するのを容易にするために、Microsoft は、それを Windows 上でサービスとしてインストールしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The installer can be used to set up the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーを使用して、サービスを設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>On the <bpt id="p1">**</bpt>Configuration<ept id="p1">**</ept> page of the installer, Microsoft used the same cluster name when it installed each Elasticsearch node in the cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーの<bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept>で、Microsoft は、各 Elasticsearch ノードをクラスターにインストールするときに、同じクラスター名を使用しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Microsoft set every Elasticsearch node to perform all three roles: Data, Master, and Ingest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft はすべての Elasticsearch ノードを Data、Master、Ingest という 3 つの役割をすべて実行するように設定しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Depending on the amount that you expect Kibana and Elasticsearch to be used, consider increasing the memory usage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana と Elasticsearch の使用量に応じて、メモリ増設を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>You can change this setting later by modifying the -Xm options in the C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>Elastic<ph id="ph3">\\</ph>Elasticsearch<ph id="ph4">\\</ph>config<ph id="ph5">\\</ph>jvm.options file and restarting Elasticsearch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>Elastic<ph id="ph3">\\</ph>Elasticsearch<ph id="ph4">\\</ph>config<ph id="ph5">\\</ph>jvm.options ファイルの -Xm オプションを後で変更し、Elasticsearch を再起動することによって、この設定を変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Depending on the number of Elasticsearch nodes that you set up, you can set the Discovery minimum master nodes appropriately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定した Elasticsearch ノードの数に応じて、検出の最小マスターノードを適切に設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>If you aren't sure, you can keep the master nodes empty.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">わからない場合は、マスター ノードを空にしておくことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>For more information about discovery and nodes, see <bpt id="p1">[</bpt>Node<ept id="p1">](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-node.html)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探索および Node の詳細については、<bpt id="p1">[</bpt>Node<ept id="p1">](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-node.html)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For discoverability, in <bpt id="p1">**</bpt>Network settings<ept id="p1">**</ept>, Microsoft set the <bpt id="p2">**</bpt>Network host<ept id="p2">**</ept> value of each node to that node's IP address and added the IP addresses of all Elasticsearch nodes to the <bpt id="p3">**</bpt>Unicast Hosts<ept id="p3">**</ept> list for each node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発見可能性に関しては、<bpt id="p1">**</bpt>ネットワークの設定<ept id="p1">**</ept>で、Microsoft は、各ノードの<bpt id="p2">**</bpt>ネットワーク ホスト<ept id="p2">**</ept>値をノードの IP アドレスに設定し、すべての Elasticsearch ノードの IP アドレスを、各ノードの <bpt id="p3">**</bpt>Unicast Hosts<ept id="p3">**</ept> リストに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>For example, for Orchestrator #1, which has the IP address 10.0.0.12, Microsoft set the <bpt id="p1">**</bpt>Network host<ept id="p1">**</ept> value to <bpt id="p2">**</bpt>10.0.0.12<ept id="p2">**</ept> and added the following IP addresses to the <bpt id="p3">**</bpt>Unicast Hosts<ept id="p3">**</ept> list: 10.0.0.12 and 10.0.0.13, where 10.0.0.13 is Orchestrator #2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、IP アドレスが 10.0.0.12 のオーケストレータ #1 の場合、Microsoft は <bpt id="p1">**</bpt>Network host<ept id="p1">**</ept> の値を <bpt id="p2">**</bpt>10.0.0.12<ept id="p2">**</ept> に設定し、次の IP アドレスを <bpt id="p3">**</bpt>Unicast Hosts<ept id="p3">**</ept> リストに追加しました。10.0.0.12 および 10.0.0.13 (10.0.0.13 はオーケストレータ #2)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>If you're installing Elasticsearch version 6.3 or higher, you can disregard this paragraph.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Elasticsearch 6.3 以降のバージョンをインストールする場合、この段落は無視できます。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>You can install X-Pack either now or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今または後で、X-Pack をインストールすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For more information about setup and whether you should install X-Pack, see the "X-Pack" section of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定および X-Pack をインストールする必要があるかどうかに関する詳細については、このトピックの「X-Pack」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>For now, unless you know what X-Pack is for, don't install it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、X-Pack がどういうものか理解していない限り、インストールしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Open the HTTP port (by default, port 9200) and the node communication port (by default, port 9300) in your firewall.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイアウォールの HTTP ポート (既定では、ポート 9200) と、ノード通信ポート (既定では、ポート 9300) を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>To verify that the installation was successful, start a browser, and open the application address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールが成功したことを確認するには、ブラウザーを起動し、アプリケーションのアドレスを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>You should see some JavaScript Object Notation (JSON) output.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの JavaScript Object Notation (JSON) 出力が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Logstash</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logstash</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>In its test setup, Microsoft found that some events from Winlogbeat required adjustments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの設定では、Microsoft は、Winlogbeat のいくつかのイベントで調整が必要なことがわかりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Logstash provides that functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logstash は、その機能を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Microsoft downloaded Logstash to C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash on the Orchestrator #2 and Orchestrator #3 nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は Logstash をオーケストレータ #2 および オーケストレータ #3 ノードで C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash にダウンロードしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>To help ensure that Logstash runs on startup, we used the Non-Sucking Service Manager (NSSM) to set up a service for the Logstash batch script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logstash が起動時に実行されることを確認するために、Non-Sucking サービス マネージャー (NSSM) を使用して、Logstash バッチ スクリプトのサービスを設定しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Copy nssm.exe to the Logstash bin folder (for example, C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nssm.exe を Logstash の bin フォルダーにコピーする (たとえば、C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>) 。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Open Windows PowerShell from the bin folder, and run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bin フォルダーから Windows PowerShell を開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Application<ept id="p1">**</ept> tab, set the following fields, and then click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション<ept id="p1">**</ept>タブで、次のフィールドを設定して、<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source><bpt id="p1">**</bpt>Path:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>logstash.bat</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パス:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>logstash.bat</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">**</bpt>Startup directory:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash\6.2.4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>起動ディレクトリ:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash\6.2.4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>Arguments:<ept id="p1">**</ept> -f C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>config<ph id="ph4">\\</ph>logstash-dyn365finops.conf</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引数:<ept id="p1">**</ept> -f C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>config<ph id="ph4">\\</ph>logstash-dyn365finops.conf</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>(There are more settings that you can set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(より多くの設定ができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>However, these settings suffice for now.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、今のところ、これらの設定で十分です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>In the tests that Microsoft performed, NSSM had trouble restarting the installed services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft が実行したテストでは、NSSM には、インストールされたサービスの再起動に問題がありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Because NSSM wasn't 100-percent reliable for Logstash and Kibana, the service was treated as an OS startup service and little else.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logstash と Kibana に対し NSSM は 100% の信頼性がなかったため、サービスは OS 起動サービスとして扱われました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Microsoft created a configuration file for Logstash and put it in <bpt id="p1">[</bpt>C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>config<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept>. This file performs useful transformations on Finance and Operations diagnostics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、Logstash に対し構成ファイルを作成し、<bpt id="p1">[</bpt>C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Logstash<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>config<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept> にプットします。このファイルは Finance and Operations 診断で、便利な変換を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>To make the configuration work for your setup, you must change the <bpt id="p1">**</bpt>hosts<ept id="p1">**</ept> fields in the <bpt id="p2">**</bpt>output<ept id="p2">**</ept> section so that they point to the Elasticsearch nodes in your cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定のためコンフィギュレーションを行うには、クラスターの Elasticsearch ノードを指すように、<bpt id="p2">**</bpt>出力<ept id="p2">**</ept>セクションの<bpt id="p1">**</bpt>ホスト<ept id="p1">**</ept>フィールドを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>For example, change <bpt id="p1">**</bpt>hosts<ept id="p1">**</ept> to <bpt id="p2">**</bpt><ph id="ph1">\[</ph>"ORCH1:9200", "ORCH2:9200"<ph id="ph2">\]</ph><ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>ホスト<ept id="p1">**</ept> を <bpt id="p2">**</bpt><ph id="ph1">\[</ph>"ORCH1:9200", "ORCH2:9200"<ph id="ph2">\]</ph><ept id="p2">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>The configuration was tested by using the Winlogbeat configuration from the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成は、次のセクションから Winlogbeat 構成を使用してテストされました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Remember to open the Winlogbeat port (by default, port 5044) in your firewall on the machine that is hosting Logstash, so that Beats can send data to Logstash.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビートが Logstash にデータを送信できるように、Logstash をホストしているコンピューターのファイアウォールで、Winlogbeat ポート (既定では、ポート 5044) を開くことを忘れないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Winlogbeat</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Microsoft downloaded Winlogbeat to each Application Object Server (AOS) and Orchestrator node at C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Winlogbeat, and configured the <bpt id="p1">[</bpt>winlogbeat.yml file<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は Winlogbeat を C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Winlogbeat の 各 Application Object Server (AOS) およびオーケストレータ ノードにダウンロードし、<bpt id="p1">[</bpt>winlogbeat.yml file<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept> を構成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>To make the configuration work for your set up, you must change the <bpt id="p1">**</bpt>output.logstash.hosts<ept id="p1">**</ept> fields so that they point to all your Logstash nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定のためコンフィギュレーションを行うには、すべての Logstash ノードを指すように <bpt id="p1">**</bpt>output.logstash.hosts<ept id="p1">**</ept> フィールドを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Winlogbeat handles the load balancing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat は、負荷分散を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>When Winlogbeat runs on an Orchestrator node, the <bpt id="p1">**</bpt>Tags<ept id="p1">**</ept> field can be changed from <bpt id="p2">**</bpt>AOS<ept id="p2">**</ept> to <bpt id="p3">**</bpt>ORCH<ept id="p3">**</ept> or a similar value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat が Orchestrator ノード上で実行されている場合、<bpt id="p1">**</bpt>Tags<ept id="p1">**</ept> フィールドは <bpt id="p2">**</bpt>AOS<ept id="p2">**</ept> から  <bpt id="p3">**</bpt>ORCH<ept id="p3">**</ept> もしくはそれに類する値に変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Microsoft also used the <bpt id="p1">**</bpt>fields.env<ept id="p1">**</ept> field to set the environment of the deployment (sandbox, sandbox-n, or production).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は <bpt id="p1">**</bpt>fields.env<ept id="p1">**</ept> フィールドを使用して、配置環境 (サンド ボックス、サンド ボックス -n、または生産) を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>In this way, there is a cleaner separation when data from multiple environments and node types is queried.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにして、複数の環境およびノード タイプからのデータが照会されると、より明確な分離が行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Winlogbeat includes a service installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat には、サービス インストーラーが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Microsoft used this installer to set up Winlogbeat as a service on each node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、このインストーラーを使用して、各ノード上のサービスとして Winlogbeat を設定しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Press the Windows logo key+R to start the Run tool, and then run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows ロゴキーと R キーを同時に押して、ツールの実行を開始し、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Kibana</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Kibana provides the interface to query the diagnostic data in Elasticsearch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana は、Elasticsearch の診断データをクエリするインターフェイスを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Microsoft downloaded Kibana to C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Kibana and configured the kibana.yml file in the following manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は Kibana を C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Kibana にダウンロードし、次の方法で kibana.yml ファイルを構成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>From Kibana, Microsoft had to define index patterns on the <bpt id="p1">**</bpt>Management<ept id="p1">**</ept> tab. Because index patterns group indexes by name, an index pattern was required for the two indexes that were made: deployment-<ph id="ph1">\*</ph> and runtime-<ph id="ph2">\*</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana から、Microsoft は<bpt id="p1">**</bpt>管理<ept id="p1">**</ept>タブでインデックス パターンを定義しなければなりませんでした。インデックス パターンは名前でインデックスをグループ化するため、1 つのインデックス パターンが作成された 2 つのインデックス: 配置-<ph id="ph1">\*</ph> およびランタイム-<ph id="ph2">\*</ph> を必要とするためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The index names are case-sensitive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックス名は、大文字と小文字が区別されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Microsoft set the runtime-<ph id="ph1">\*</ph> index pattern as the default pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、既定のパターンとしてランタイム -<ph id="ph1">\*</ph> インデックス パターンを設定しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>When you're looking at the index patterns on the <bpt id="p1">**</bpt>Management<ept id="p1">**</ept> tab, click the asterisk (<ph id="ph1">\*</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept>タブのインデックス パターンを確認するときは、アスタリスク (<ph id="ph1">\*</ph>) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The index pattern will then appear on the <bpt id="p1">**</bpt>Discover<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックス パターンが、<bpt id="p1">**</bpt>Discover<ept id="p1">**</ept> タブに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Runtime index pattern<ept id="p1">](./media/runtime-index-patter.png)](./media/runtime-index-patter.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ランタイム インデックス パターン<ept id="p1">](./media/runtime-index-patter.png)](./media/runtime-index-patter.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Microsoft ran Kibana as a service in the same manner as Logstash, so that Kibana is started at OS startup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は Kibana を Logstash と同じ方法でサービスとして実行し、Kibana が OS の起動時に起動されるようにしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Unlike Logstash, kibana.bat doesn't need the path of the configuration files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logstash とは異なり、kibana.bat は、コンフィギュレーション ファイルのパスは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Therefore, you can just install an NSSM service that points to C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Kibana<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>kibana.bat.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Kibana<ph id="ph3">\\</ph>6.2.4<ph id="ph4">\\</ph>bin<ph id="ph5">\\</ph>kibana.bat を参照する NSSM サービスをインストールできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If you want users to browse Kibana on your network, remember to open the port for Kibana.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワーク上で Kibana を参照したいなら、Kibana 用のポートを開くことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>The default port is 5601.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のポートは 5601 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Example queries on the Discover tab in Kibana</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana の検出タブでのクエリの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The following sample queries can help you start probing the diagnostic data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のサンプル クエリでは、診断データの調査を開始できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>If you require something more than the examples show, you can try one of the following queries:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例に示されているもの以上のものが必要な場合、次のクエリのいずれかをお試しください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Find slow database queries:<ept id="p1">**</ept> Enter <bpt id="p2">**</bpt>slow<ept id="p2">**</ept> in the search field to find events that have the word "slow" somewhere in the event data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>低速データベース クエリの検索:<ept id="p1">**</ept> 検索フィールドに<bpt id="p2">**</bpt>低速<ept id="p2">**</ept>と入力して、イベント データのどこかに「低速」という単語が含まれているイベントを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>If you want to be more precise, you can find events that have a task name of <bpt id="p1">**</bpt>AosDatabaseSlowQuery<ept id="p1">**</ept> and then enter <bpt id="p2">**</bpt>TaskName:AosDatabaseSlowQuery<ept id="p2">**</ept> in the search field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より正確にするには、<bpt id="p1">**</bpt>AosDatabaseSlowQuery<ept id="p1">**</ept> のタスク名を持つイベントを検索し、検索フィールドに <bpt id="p2">**</bpt>TaskName:AosDatabaseSlowQuery<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Find recent exceptions:<ept id="p1">**</ept> Enter <bpt id="p2">**</bpt>exception<ept id="p2">**</ept> in the search field to find events that have either thrown an exception, or handled an exception and logged it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>最新の例外を見つける:<ept id="p1">**</ept> <bpt id="p2">**</bpt>例外<ept id="p2">**</ept>を検索フィールドに入力して、例外をスローしたイベント、または例外を処理してログに記録したイベントを探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>In the upper-right corner of Kibana, you can select the time frame that the search should be limited to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana の右上隅で、検索を制限する必要がある期間を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>The time frame that you set there is persisted between tabs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そこで設定したタイム フレームは、タブの間で保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Therefore, the data on the <bpt id="p1">**</bpt>Visualize<ept id="p1">**</ept> tab will reflect the selected time frame.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>視覚化<ept id="p1">**</ept>タブ上のデータは選択されているタイム フレームに反映されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Search time frame<ept id="p1">](./media/time-visualize.png)](./media/time-visualize.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>検索の時間枠<ept id="p1">](./media/time-visualize.png)](./media/time-visualize.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Find events from an AOS node:<ept id="p1">**</ept> Enter <bpt id="p2">**</bpt>host:AOS1<ept id="p2">**</ept> in the search field to find all events from that node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOS ノードからイベントを検索:<ept id="p1">**</ept> ノードからすべてのイベントを検索するために、検索フィールドに <bpt id="p2">**</bpt>host:AOS1<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source><bpt id="p1">**</bpt>Find events with proximity, in time, to another:<ept id="p1">**</ept> When you've found an event that you're interested in, click <bpt id="p2">**</bpt>View surrounding documents<ept id="p2">**</ept> next to the header of that event to find events that occurred at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>他のイベントと最も近い、特定のイベントを見つける:<ept id="p1">**</ept> 興味のあるイベントが見つかったら、そのイベントのヘッダーの横にある<bpt id="p2">**</bpt>関連するドキュメントを表示します<ept id="p2">**</ept>をクリックして、同時に発生したイベントを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>If you see events that occurred at around the same time but from different AOS nodes, you can add additional filtering to view only events from the node that you want.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同時に発生した、異なる <ph id="1">Microsoft Dynamics</ph> <ph id="2">AX</ph> Application Object Server (AOS) ノードからのイベントが表示されている場合、追加のフィルターを追加して、必要なノードからのイベントのみを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>View surrounding documents<ept id="p1">](./media/events-with-proximity.PNG)](./media/events-with-proximity.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>関連するドキュメントを表示します<ept id="p1">](./media/events-with-proximity.PNG)](./media/events-with-proximity.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Thirty-day data retention</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">30 日間のデータの保持</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>To keep its hard disks free from stale data, Microsoft used Curator v5.5 to clean up indexes that were older than 30 days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">古いデータからハード ディスクを保持するために、Microsoft は Curator v5.5 を使用して 30 日以上経過したインデックスをクリーンアップしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Microsoft downloaded Curator to one of the Orchestrator nodes at C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft はキュレーターを C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator でオーケストレータ ノードのいずれかにダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Microsoft then used the configuration file that was put in <bpt id="p1">[</bpt>C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept> to connect Curator to its Elasticsearch cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、<bpt id="p1">[</bpt>C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept> に配置された構成ファイルを使用して、キュレーターを Elasticsearch クラスターに接続しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Curator runs actions, and Microsoft created an action to clean up 30-day-old indexes that were put in <bpt id="p1">[</bpt>C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キュレーターはアクションを実行し、Microsoft は <bpt id="p1">[</bpt>C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator<ept id="p1">](https://aka.ms/ConfigFilesOnPremises)</ept> 内に配置された 30 日前のインデックスをクリーンアップするアクションを作成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Microsoft created a basic task in Windows Task Scheduler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、Windows タスク スケジューラの基本的なタスクを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>This task has a weekly trigger on Saturday and Sunday, and the trigger has the following settings to start a program:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクは、土曜日と日曜日に毎週トリガーを持ち、トリガーにはプログラムを開始するための次の設定があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source><bpt id="p1">**</bpt>Program/script:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator<ph id="ph3">\\</ph>curator.exe</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プログラム/スクリプト:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator<ph id="ph3">\\</ph>curator.exe</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source><bpt id="p1">**</bpt>Add arguments:<ept id="p1">**</ept> --config curator.yml .<ph id="ph1">\\</ph>30day<ph id="ph2">\_</ph>data<ph id="ph3">\_</ph>retention<ph id="ph4">\_</ph>actions.yml</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引数を追加:<ept id="p1">**</ept> --curator.yml のコンフィグレーション .<ph id="ph1">\\</ph>30 日<ph id="ph2">\_</ph>データ<ph id="ph3">\_</ph>保存<ph id="ph4">\_</ph>actions.yml</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">**</bpt>Start in:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始:<ept id="p1">**</ept> C:<ph id="ph1">\\</ph>ELK<ph id="ph2">\\</ph>Curator</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>X-Pack</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>As of June 2018, Elastic Stack components have been released that start with version 6.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2018 年 6 月現在、バージョン 6.3 以降の Elastic スタック コンポーネントがリリースされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>This updated version handles X-Pack in a more graceful manner, by enabling the free features of X-Pack by default, without requiring that you update the license every year, and by letting you opt in to the paid features afterward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この更新されたバージョンでは、X-Pack の無料機能を毎年ライセンスを更新することなくデフォルトで有効にすること、また、後で有料機能にオプトインすることで、X-Pack をより上手く処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>If you install an Elastic Stack version that is earlier than 6.3, the content in this section only partially applies to the setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">6.3 よりも前の Elastic スタック バージョンをインストールしている場合、このセクションの内容は設定に部分的にのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>You can select to install X-Pack when you install Elasticsearch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Elasticsearch のインストール時に X-Pack をインストールするように選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Alternatively, you can <bpt id="p1">[</bpt>install it later<ept id="p1">](https://www.elastic.co/guide/en/x-pack/current/installing-xpack.html)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">[</bpt>インストールをすることができます。<ept id="p1">](https://www.elastic.co/guide/en/x-pack/current/installing-xpack.html)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>X-Pack has a free basic license that must be updated every year.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack には無料の基本ライセンスがあり、毎年更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Microsoft installed the free version to enable query data to be exported from Kibana in comma-separated value (CSV) format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft では、Kibana からコンマ区切り値 (CSV) 形式でエクスポートするデータのクエリを有効にするために無料版がインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>There are other useful features in X-Pack, but some are available only in a paid subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack ではその他の便利な機能がありますが、いくつかは有料サブスクリプションでのみ使用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>To enable only the free features and avoid using other X-Pack trial features, Microsoft added the following settings to our elasticsearch.yml and kibana.yml configuration files:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無料の機能だけを有効にし、他の X-Pack の試用版の機能を使用しないように、Microsoft は、elasticsearch.yml および kibana.yml のコンフィギュレーション ファイルに次の設定を追加しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>These settings also stop Kibana and Elasticsearch from asking for credentials because the security module is no longer enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの設定は、セキュリティ モジュールが有効ではないため、Kibana と Elasticsearch が資格情報を求めることも停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>For X-Pack to work, the logstash.yml configuration file must also be configured in the following manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack を動作させるには、logstash.yml 構成ファイルも次のように構成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The paid version of X-Pack includes HTTPS encryption for connections throughout the cluster, password-protected data access, and more.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack の支払済バージョンには、クラスター、パスワードで保護されたデータ アクセスなどの接続に使用するための HTTPS 暗号化が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>For more information about X-Pack, see the <bpt id="p1">[</bpt>Elastic website<ept id="p1">](https://www.elastic.co/products/x-pack)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X-Pack の詳細については、<bpt id="p1">[</bpt>Elastic Web サイト<ept id="p1">](https://www.elastic.co/products/x-pack)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Export a query to a CSV file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSV ファイルへのクエリのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>In Kibana, on the <bpt id="p1">**</bpt>Discover<ept id="p1">**</ept> tab, write a query, and save it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana では、<bpt id="p1">**</bpt>検出<ept id="p1">**</ept>タブで、クエリを作成し、保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>After you save the query, on the <bpt id="p1">**</bpt>Reporting<ept id="p1">**</ept> tab at the top of the <bpt id="p2">**</bpt>Discover<ept id="p2">**</ept> page, click <bpt id="p3">**</bpt>Generate CSV<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリを保存した後、<bpt id="p2">**</bpt>検出<ept id="p2">**</ept>ページの上部にある<bpt id="p1">**</bpt>レポート<ept id="p1">**</ept> タブの <bpt id="p3">**</bpt>CSV を生成<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>You don't receive any data in Kibana</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana 内のデータを受信しません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If you don't receive any data in Kibana, review the logs from Winlogbeat to Logstash, Elasticsearch, and Kibana.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kibana で、何もデータを受け取っていない場合、Winlogbeat から Logstash、Elasticsearch、および Kibana のログを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Note that the Winlogbeat installation puts its logs in C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>winlogbeat<ph id="ph3">\\</ph>Logs, whereas the other Elastic Stack components put their logs close to the installation path (for example, in C:<ph id="ph4">\\</ph>ELK<ph id="ph5">\\</ph>Elasticsearch<ph id="ph6">\\</ph>logs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Winlogbeat のインストールでは、C:<ph id="ph1">\\</ph>ProgramData<ph id="ph2">\\</ph>winlogbeat<ph id="ph3">\\</ph>Logs にログが記録されますが、他の Elastic スタック コンポーネントはログをインストール パスに近づけることに注意してください (例: C:<ph id="ph4">\\</ph>ELK<ph id="ph5">\\</ph>Elasticsearch<ph id="ph6">\\</ph>logs)。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>