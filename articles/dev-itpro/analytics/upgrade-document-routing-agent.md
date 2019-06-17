<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="upgrade-document-routing-agent.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>upgrade-document-routing-agent.5328e7.96c09e7784a6e3111247466c4e933f0198936e78.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>96c09e7784a6e3111247466c4e933f0198936e78</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\upgrade-document-routing-agent.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade the Document Routing Agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント回覧エージェントのアップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to upgrade the Document Routing Agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ドキュメント巡回エージェントをアップグレードする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade the Document Routing Agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント回覧エージェントのアップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Microsoft Dynamics 365 for Finance and Operations with platform update 12 includes several important enhancements to the components that provide network printing capabilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 12 には、ネットワーク印刷機能を提供するコンポーネントに対するいくつかの重要な拡張機能が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For example, the solution for managing the print job queue has been redesigned so that the Print Job Management service can be scaled to satisfy high-volume printing requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、印刷ジョブ キューを管理するソリューションは、印刷ジョブの管理サービスが大量の印刷要件を満たすために調整されるよう再設計されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Although the Print Job Management service is backward-compatible with in-market versions of the Document Routing Agent (DRA) client, we strongly recommend that customers upgrade <bpt id="p1">**</bpt>all<ept id="p1">**</ept> existing DRA clients that are hosted on-premises.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">印刷ジョブの管理サービスには、市場バージョンのドキュメント回覧エージェント (DRA) クライアントと下位互換性のあるバージョンがありますが、顧客がオンプレミスでホストされている既存の DRA クライアントを<bpt id="p1">**</bpt>すべて<ept id="p1">**</ept>アップグレードすることを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If you don't upgrade existing installations of the DRA to Platform update 12 or later, you might experience the following issues:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DRA の既存のインストールをプラットフォーム更新プログラム 12 またはそれ以降のバージョンにアップグレードしない場合は、次の問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Observable performance degradation in Finance and Operations applications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations アプリケーションの監視可能なパフォーマンス低下</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Document loss that is associated with orphaned print jobs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">孤立した印刷ジョブに関連する文書の消失</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Inconsistent handling of printed documents that have custom margins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムの余白がある印刷ドキュメントの一貫性のない処理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>IT administrators must perform the following procedures on each domain resource that is used to host a DRA for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IT 管理者は、Finance and Operations の DRA をホストするために使用される各ドメイン リソースに対して、次の手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Get started</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用開始</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To continue to run the DRA as a Microsoft Windows service, you must have both the user name and the password of the domain account that is used to run the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DRA を Microsoft Windows サービスとして引き続き実行するには、サービスを実行するために使用されるドメイン アカウントのユーザー名とパスワードの両方が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This information must be available after the upgrade is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この情報は、アップグレード完了後に使用可能になっている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To find the information for the active service account, start the Microsoft Management Console (MMC) Services snap-in, and select <bpt id="p1">**</bpt>Microsoft Dynamics 365 Document Routing Service<ept id="p1">**</ept> in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なサービス アカウントの情報を検索するには、Microsoft 管理コンソール (MMC) サービス スナップインを起動し、一覧から <bpt id="p1">**</bpt>Microsoft Dynamics 365 ドキュメント回覧サービス<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Services snap-in</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マネージャー スナップイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Uninstall an existing Document Routing Agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のドキュメント回覧エージェントのアンインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Open <bpt id="p1">**</bpt>Programs and Features<ept id="p1">**</ept>, and then find and uninstall <bpt id="p2">**</bpt>Microsoft Dynamics 365 for Finance and Operations: Document Routing<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プログラムと機能<ept id="p1">**</ept>を開き、<bpt id="p2">**</bpt>Microsoft Dynamics 365 for Finance and Operations: ドキュメント回覧<ept id="p2">**</ept>を検索し、削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Uninstall or change a program window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラム ウィンドウのアンインストールまたは変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>During the uninstallation process, if you're prompted to close the Microsoft Dynamics 365 Document Routing Service application, select <bpt id="p1">**</bpt>Automatically close applications and attempt to restart them after setup is complete.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アンインストールのプロセス中に、Microsoft Dynamics 365 ドキュメント回覧サービス アプリケーションを終了するメッセージが表示された場合は、<bpt id="p1">**</bpt>セットアップが完了したら、アプリケーションを自動的に閉じて再起動します。<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Dialog box that prompts you to close applications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの終了を促すダイアログ ボックス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Install the latest Document Routing Agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新のドキュメント回覧エージェントのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For information about how to install the latest DRA that is available with your subscription, see <bpt id="p1">[</bpt>Install the Document Routing Agent to enable network printer devices<ept id="p1">](install-document-routing-agent.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定期売買で使用可能な最新の DRA をインストールする方法の詳細については、<bpt id="p1">[</bpt>ネットワーク プリンター デバイスを有効にするためにドキュメント回覧エージェントをインストールする<ept id="p1">](install-document-routing-agent.md)</ept> を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>