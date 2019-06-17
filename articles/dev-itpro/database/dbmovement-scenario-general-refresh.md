<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="dbmovement-scenario-general-refresh.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>dbmovement-scenario-general-refresh.ca6e17.12a19e4010ebb24ffcb49f65ed67ad44fd880041.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>12a19e4010ebb24ffcb49f65ed67ad44fd880041</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\dbmovement-scenario-general-refresh.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Refresh for training purposes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレーニング用の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains a general-purpose database refresh scenario for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の汎用データベース更新シナリオについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Refresh for training purposes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレーニング用の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This tutorial shows how to use the refresh database operation in a training scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、トレーニング シナリオでデータベース更新操作の使用方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In this tutorial, you will learn how to:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、次の方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prepare the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット環境を準備します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Run the refresh.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Reconfigure the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット環境を再構成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Enable selected users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したユーザーを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>As an example of this scenario, a customer who has already gone live with Microsoft Dynamics 365 for Finance and Operations wants to load a recent copy of production transactions into the user acceptance testing (UAT) environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations を既に稼働している顧客が、ユーザー受け入れテスト (UAT) 環境に生産トランザクションの最新のコピーを読み込もうとしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this way, the customer can support training of new employees and evaluate configuration changes without affecting the live environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにして、顧客は、新しい従業員のトレーニングをサポートし、実際の環境に影響を与えずに構成の変更を評価できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To do a refresh database operation, your production environment must be deployed, or you must have a minimum of two standard UAT environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース更新操作を行うには、実稼働環境を配置する必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Notify users about the pending downtime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保留中のダウンタイムについてユーザーに通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Before you start the bulk of the work, notify users of the target environment that the environment will be offline for a period.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業の大部分を開始する前に、環境が一定期間オフラインになる対象となる環境についてユーザーに通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can notify users either manually via Microsoft Dynamics Lifecycle Services (LCS) or programmatically by using RESTful application programming interface (API) calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) から手動で、または RESTful アプリケーション プログラミング インターフェイス (API) 呼び出しを使用してプログラムによりユーザーに通知できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Manually send a broadcast message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動でブロードキャスト メッセージを送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To notify users manually via LCS, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS を通して手動でユーザーに通知するには、以下の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In LCS, open the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page for the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で、ターゲット環境の <bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Select <bpt id="p1">**</bpt>Maintain<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Message online users<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>オンライン ユーザーにメッセージ<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Select <bpt id="p1">**</bpt>Broadcast a new message for downtime<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンタイムに関する新しいメッセージの配信<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select the valid from/valid to times in your local time zone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル タイム ゾーンで有効開始/有効終了の時刻を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Select <bpt id="p1">**</bpt>Post<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>投稿<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Programmatically send a broadcast message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラムによりブロードキャスト メッセージを送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The following sample code can be used as shown in a console application, or it can be modified to make it work with other services that can be called on demand, such as Microsoft Azure Functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のサンプル コードをコンソール アプリケーションに示されたとおりに使用するか、Microsoft Azure の機能など、オンデマンドで呼び出せる他のサービスと連携するように変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Before this sample code will work, you must set up your application registration as described in <bpt id="p1">[</bpt>How to authenticate custom services<ept id="p1">](../data-entities/services-home-page.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプル コードが動作するには、<bpt id="p1">[</bpt>カスタム サービスの認証方法<ept id="p1">](../data-entities/services-home-page.md)</ept>の説明に従ってアプリケーション登録を設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Both approaches, manual via LCS and programmatic via RESTful API calls, will show users that a period of downtime is pending.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どちらの方法でも (LCS 経由の手動、RESTful API 呼び出しでプログラムにより)、ダウンタイムの期間が保留中であることがユーザーに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Begin the refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新の開始</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Depending on the size of your source environment, it might make sense to begin the refresh process immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース環境の規模によっては、即座に更新プロセスを開始することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The larger the source database, the longer it will take to copy to your target Azure SQL Database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース データベースが大きいほど、ターゲット Azure SQL データベース インスタンスへのコピーに時間がかかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>While the copy is in progress, the target environment will still be online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーの進行中も、対象となる環境はオンラインになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The downtime will start after the copy is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーが完了した後、ダウンタイムが開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>This process can be done manually via LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは、LCS 経由で手動で行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For the latest steps, see <bpt id="p1">[</bpt>Refresh database quickstart<ept id="p1">](database-refresh.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の手順については、<bpt id="p1">[</bpt>データベースの更新クイックスタート<ept id="p1">](database-refresh.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In a future release of LCS, you will also be able to trigger this process via a RESTful API.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の将来のリリースでは、RESTful API 経由でこのプロセスがトリガーすることもできるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Reconfigure environment specific settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の固有の設定を変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After the refresh is completed, use the <bpt id="p1">**</bpt>Sign off<ept id="p1">**</ept> button in LCS to close out of the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新が完了した後、LCS で<bpt id="p1">**</bpt>サインオフ<ept id="p1">**</ept> ボタンを使用し、操作を閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can then start to configure the environment-specific settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、環境固有の設定のコンフィギュレーションを開始できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>First, sign in to the environment by using the admin account that can be found on the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まず、環境にログインします。LCS の<bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept>ページにある管理者アカウントを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Here are typical areas of reconfiguration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再設定の標準的な領域を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>You might require additional reconfiguration, based on your setup and the independent software vendor (ISV) solutions that are installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定およびインストールされている独立系ソフトウェア ベンダー (ISV) ソリューションによっては、追加の再設定が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Batch groups:<ept id="p3">**</ept> Add the various Application Object Server (AOS) instances to the batch server groups that you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>バッチ グループ:<ept id="p3">**</ept> 必要なバッチ サーバー グループにさまざまなアプリケーション おぶじぇくと サーバー (AOS) インスタンスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Entity Store:<ept id="p3">**</ept> Refresh the various entities that you require for Microsoft Power BI reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>エンティティ店舗:<ept id="p3">**</ept> Microsoft Power BI レポートに必要なさまざまなエンティティを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>System parameters:<ept id="p3">**</ept> Reconnect the environment to the LCS Help configuration for task guides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>システム パラメーター:<ept id="p3">**</ept>タスク ガイドの LCS ヘルプ コンフィギュレーションに環境を再接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Email<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>Email parameters:<ept id="p4">**</ept> Enter the Simple Mail Transfer Protocol (SMTP) settings if you use email in your UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>電子メール<ept id="p3">**</ept><ph id="ph3">\&gt;</ph><bpt id="p4">**</bpt>パラメータを電子メールで送信:<ept id="p4">**</ept> UAT 環境内で電子メールを使用する場合は、簡易メール転送プロトコル (SMTP) の設定を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Inquiries<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Batch jobs:<ept id="p3">**</ept> Select the jobs that you want to run in your UAT environment, and update the status to <bpt id="p4">**</bpt>Waiting<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>照会<ept id="p2">**</ept><ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>バッチ ジョブ:<ept id="p3">**</ept> UAT 環境で実行するジョブを選択し、ステータスを <bpt id="p4">**</bpt>待機中<ept id="p4">**</ept> に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>To complete this reconfiguration more quickly, we recommend that you build a custom web service endpoint that can be called on demand after the refresh is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この再設定をより迅速に完了するには、更新が完了した後に必要に応じて呼び出すことができるカスタム Web サービス エンドポイントを構築することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>An example of this type of web service will be added in a future update of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この種類の Web サービスの例は、このトピックの将来の更新で追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Open the environment to users</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーに環境を開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>When the system is configured as you require, you can enable selected users to let them access the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、システムを構成する場合は、選択したユーザーが環境にアクセスできるようにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>By default, all users except the admin and Microsoft service accounts are disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デフォルトでは、管理者と Microsoft サービス アカウントを除くすべてのユーザーが無効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Users<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Users<ept id="p3">**</ept>, and enable the users that should have access to the UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>ユーザー<ept id="p2">**</ept><ph id="ph2">\&gt;</ph><bpt id="p3">**</bpt>ユーザー<ept id="p3">**</ept> に移動し、UAT 環境へのアクセスが必要なユーザーを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If many users must be enabled, you can complete this task more quickly by using the <bpt id="p1">[</bpt>Microsoft Excel Add-In<ept id="p1">](../office-integration/use-excel-add-in.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くのユーザーを有効にする必要がある場合、<bpt id="p1">[</bpt>Microsoft Excel アドイン<ept id="p1">](../office-integration/use-excel-add-in.md)</ept>を使用してこのタスクをすばやく完了できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>