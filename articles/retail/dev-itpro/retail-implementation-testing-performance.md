<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-implementation-testing-performance.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-implementation-testing-performance.b17332.90d56b480a7b940d0a2998e550915d4e271b67d7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>90d56b480a7b940d0a2998e550915d4e271b67d7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-implementation-testing-performance.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Testing and performance issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストおよびパフォーマンスの問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes recommended practices for testing and performance for Microsoft Dynamics 365 for Retail implementation projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail のテスティングおよびパフォーマンスの推奨事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Testing and performance issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストおよびパフォーマンスに関する問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This document describes practices and tools that are related to functional testing, performance testing, and performance troubleshooting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このドキュメントでは、機能テスト、パフォーマンス テスト、およびパフォーマンスのトラブルシューティングに関連するプラクティスとツールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>User acceptance testing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー受け入れテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The main purpose of user acceptance testing (UAT) is to verify that specific business scenarios work as you expect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー受け入れテスト (UAT) の主な目的は、特定のビジネス シナリオが期待どおりに動作するかを確認することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The testing should include not only the customizations, but also out-of-box Microsoft functionality and non-happy-path testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストはカスタマイズだけでなく、最初から用意されている Microsoft の機能と、non-happy-path テストを含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The goal is to catch anything that doesn't work correctly before you go to the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境に移動する前に正しく動作しないものは、すべてキャッチすることが目標です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For the best results, the UAT environment should be a Tier 2 through Tier 5 environment, not a development environment (Tier 1).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最良の結果を得るには、UAT 環境が、開発環境 (階層 1) ではなく、階層 2 〜階層 5 環境である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If a development environment is used, there are scenarios where a developer who uses the same environment can cause errors (for example, uncommitted source changes or debugger attached errors).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境が使用される場合、開発者がエラーを引き起こす可能性がある同じ環境を使用するシナリオがあります (例えば、未確定のソース変更またはデバッガーの添付エラーなど)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The switch between Microsoft Internet Information Services (IIS) Express and IIS can also cause issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Internet Information Services (IIS) Express と IIS の間のスイッチは、問題を引き起こす可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Additionally, because there is no way to know exactly what has happened on a development machine, Microsoft support for a Tier 1 environment is very limited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、開発マシンの何が起こったかを正確に知る方法がないため、レベル 1 環境での Microsoft のサポートは非常に限られたものとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>A production environment can be used for UAT (for example, as a "dry run" for go-live).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UAT (たとえば、「ドライ ラン」の準備) で使用できる運用環境。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>However, if you require access to the database for any reason, you must go through deployment support engineer (DSE) service requests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、何らかの理由でデータベースへのアクセスを必要とする場合は、配置サポート エンジニア (DSE) サービスの要求を通す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Therefore, this approach might not be efficient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この方法は効率的ではない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Additionally, the production environment isn't available for a long period before the planned go-live date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、実稼動環境は、計画された稼動日以前には、長期間使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The UAT should be done after you deploy officially built deployable packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UAT は、正式にビルド展開可能なパッケージを配置した後に、実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>It should not be done on packages that are manually built in Microsoft Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio で手動でビルドされたパッケージでは実行できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The reason is that there is no way to prove what code changes were included in a manually built package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">理由として、どのコード変更が手動でビルドされたパッケージに含まれていたかを証明する手段が無いからです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Only an official build system provides assurance and an audit trail of the exact changes that are in a specific build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">公式のビルド システムだけが、特定のビルド内にある正確な変更の保証と監査証跡を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If you use Retail Modern POS/Cloud POS, make sure that you use the correct user roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS/クラウド POS を使用する場合は、正しいユーザー ロールを使用することを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>You should test by signing in as both a manager and a cashier who has lower privileges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マネージャー、およびより低い権限を持つレジ担当者としてログインすることにより、テストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Performance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Channel performance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネルの実績</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In some cases, channel performance might not be as good as you expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、チャネルのパフォーマンスが期待したほど良くないことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Poor performance is often caused by the following factors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンスの低下は、多くの場合次の要因によって発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This list is in order from highest to lowest impact.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリストは、影響の高い順に並べられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Additional custom calls to Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーへの追加カスタム呼び出し。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>If you extend the product with additional Retail Server calls, performance often decreases significantly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の Retail サーバーの呼び出しを使用して製品を拡張すると、多くの場合パフォーマンスが大幅に低下します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Not only is there a possibility of additional processing, but the network latency must also be considered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加処理の可能性だけでなく、ネットワーク待機時間も考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>We recommend that you try to avoid any additional Retail Server calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーの追加の呼び出しを回避することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Often, you can accomplish the same tasks by using extension properties and extending existing Commerce runtime (CRT) handlers or triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、拡張機能のプロパティを使用して、既存の <ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) のハンドラーやトリガーの拡張によって、同じタスクを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Additional channel database extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のチャネル データベース拡張機能。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Make sure that your custom SQL is efficient and uses correct indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム SQL が効率的で、正しいインデックスを使用していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Multiple runs of the same custom or built-in CRT SQL queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じカスタムまたは組み込みの CRT SQL クエリを複数回実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>If this approach is too expensive, caching in the CRT request handler can be applied, as appropriate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法ではコストがかかりすぎる場合は、CRT 要求ハンドラーでキャッシュを適切に適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>For more details, see the <bpt id="p1">[</bpt>Microsoft Dynamics 365 for Retail for IT pros and developers<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page)</ept> topics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>IT プロおよび開発者向け Microsoft Dynamics 365 for Retail<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>When you investigate store performance, follow the suggestions in <bpt id="p1">[</bpt>Retail Channel performance investigations<ept id="p1">](https://dynamicsnotes.com/retail-channel-performance-investigations/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗のパフォーマンスを調査するときは、<bpt id="p1">[</bpt>小売チャンネル実績調査<ept id="p1">](https://dynamicsnotes.com/retail-channel-performance-investigations/)</ept>にある提案に従ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Using telemetry data to find performance issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テレメトリ データを使用してパフォーマンスの問題を検索する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>If you must troubleshoot the performance of Microsoft Dynamics 365 for Retail and Microsoft Dynamics 365 for Finance and Operations (especially slow SQL queries or SQL deadlocks), the environment diagnostics page in Microsoft Dynamics Lifecycle Services (LCS) shows valuable telemetry data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail および Microsoft Dynamics 365 for Finance and Operations のパフォーマンスのトラブルシューティングを行う必要がある場合 (特に速度が低下する SQL クエリまたは SQL デッドロック)、Microsoft Dynamics Lifecycle Services (LCS) の環境診断ページでは、貴重な遠隔測定データが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>You can use this data to find potential performance issues in code, configuration, or design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータを使用して、コード、構成、またはデザインの潜在的なパフォーマンスの問題を見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For more details, see <bpt id="p1">[</bpt>How to use Environment Monitoring View Raw Logs<ept id="p1">](https://blogs.msdn.microsoft.com/axsa/2018/06/05/how-to-use-environment-monitoring-view-raw-logs/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>環境監視未加工ログの使用方法<ept id="p1">](https://blogs.msdn.microsoft.com/axsa/2018/06/05/how-to-use-environment-monitoring-view-raw-logs/)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>That information should help you determine why some batch processes or form loads are slow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その情報により、いくつかのバッチ処理またはフォームの読み込みが遅い理由が明らかになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Performance testing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Typically, when you test the performance of a system, you should focus on components where there is competition for many shared resources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、システムのパフォーマンスをテストするときは、多くの共有リソースが競合するコンポーネントに焦点を絞る必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>These resources might differ for different projects, customers, or requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのリソースは、さまざまなプロジェクト、顧客、または要件ごとに異なる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Here are some of the reasons why bottlenecks can occur:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボトルネックが発生するいくつかの理由は以下の通りです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Resource-intensive calculations in Finance and Operations, such as statement posting, change calculations for channel data synchronization, warehousing operations that involve a large product assortment, and MRP (Material Requirements Planning) runs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations でのリソース集中型の計算は、明細書の転記、チャネル データ同期の計算変更など、大規模な製品品揃えを含む倉庫管理の操作、および MRP (Material Requirements Planning) の実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Complex retail business logic for multiple terminals or stores that run on a few Retail Servers (either in the cloud or in a Retail store scale unit)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの Retail サーバー (クラウド内または <ph id="1">Retail Store Scale Unit</ph> のいずれか) で実行する、複数の端末またはストア用の複雑な小売ビジネス ロジック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Integrated third-party systems (integrated from either Finance and Operations or Retail Server)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合されたサード パーティ システム (Finance and Operations または Retail サーバーのいずれかから統合)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Real-time transaction services that are frequently called from Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーから頻繁に呼び出されるリアル タイム トランザクション サービス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Non-standard or extended standard functionality (for example, extended statement posting that uses a custom WHS code)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非標準または拡張された標準機能 (たとえば、カスタム WHS コードを使用する拡張明細書転記)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In general, default and non-real-time POS operations aren't considered bottlenecks because they have their own dedicated resource: the computer that the POS is installed or running on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的に、既定および非リアルタイム POS 操作は、専用のリソース (POS がインストールまたは実行されているコンピューター) を持っているため、ボトルネックとはみなされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Performance issues are typically caused by the business logic or "chatty" calls to Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンスの問題は、通常、ビジネス ロジックまたは Retail サーバーへの「Chatty」呼び出しによって発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Ideally, performance testing should be done after some initial optimizations have already been completed by using the information earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス テストはこのトピックで前述した情報を使用して、既にいくつかの初期最適化を完了した後に行う方が理想的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>If the system doesn't perform well for a single user or process, it won't perform well for concurrent users or processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一のユーザーまたはプロセスでシステムが正常に動作しない場合、同時ユーザーまたはプロセスでは正常に動作しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For more information, see <bpt id="p1">[</bpt>Retail Channel performance investigations<ept id="p1">](https://dynamicsnotes.com/retail-channel-performance-investigations/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Retail Channel Performance<ept id="p1">](https://dynamicsnotes.com/retail-channel-performance-investigations/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Additionally, in the Finance and Operations documentation, search for "PerfSdk" or "Trace parser."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、Finance and Operations ドキュメントで、「PerfSdk」または「Trace parser」を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Because every project is different, it's difficult to give a general answer about the exact performance tests that must be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのプロジェクトは異なっているため、実行する必要のある正確なパフォーマンス テストについての一般的な回答は困難です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, if the count of transaction sales lines is low (less than 100,000 per day for all stores), and if no custom extension code has been added for statement posting, a performance test should not be required for posting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、トランザクションの販売明細行が少ない (すべての店舗で 1 日あたり 10 万未満) 場合、および明細書転記にカスタム拡張コードが追加されていない場合は、転記にパフォーマンス テストを行う必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>However, if the count of sales lines is substantially higher, or if major custom changes have been added, a performance test for posting is a good idea.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、販売明細行が大幅に高い場合、または主要なカスタム変更が加えられた場合は、パフォーマンス テストを転記することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Usually, the hardware capabilities of every environment differ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、すべての環境でハードウェア機能は異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>However, performance issues can usually be reproduced in other environments if the code and data are similar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、コードおよびデータが類似している場合、通常他の環境でもパフォーマンスの問題は起こり得ます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>We don't recommend that you use a production environment for performance testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス テストに実稼働環境を使用することをお勧めしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>A good practice is to use the same data in development, test, and production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発、テスト、および運用環境で同じデータを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The development environment can then be used to work on and verify a fix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境は、修正プログラムの作成と検証に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Because many performance-critical code paths are data-dependent, the same issues might not be seen for a Contoso sample database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多数のパフォーマンス クリティカル コード パスはデータ依存のため、 Contoso サンプル データベースでは同じ問題が発生しないことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After you've completed a performance fix, you should verify the fix in a test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンスの修正を完了した後は、テスト環境で修正プログラムを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Deploy an officially built package to the test environment, and if the issue is fixed, mark the package as a release package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">公式に構築されたパッケージをテスト環境に展開し、問題が解決した場合は、パッケージをリリース パッケージとしてマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Any fix of a larger performance issue should be followed by a new performance test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらにパフォーマンスの問題を大きく修正するには、新しいパフォーマンステストを行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Often, a large issue masks other smaller issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、大きな問題は、他のより小さな問題をマスクします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>After the top issue is resolved, the next issues can be found and worked on until the performance meets the customer's expectations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の問題が解決された後、次の問題を検出し、パフォーマンスが顧客の期待に達するまで処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">[</bpt>Set up new environments, Azure DevOps, and branches for Retail projects<ept id="p1">](./new-environments-visual-studio-teams-branch-retail-projects.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail プロジェクトの新しい環境、Azure DevOps、およびブランチの設定<ept id="p1">](./new-environments-visual-studio-teams-branch-retail-projects.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt>Update code and environments for Retail projects<ept id="p1">](./updating-environments.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail プロジェクトのコードと環境の更新<ept id="p1">](./updating-environments.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>