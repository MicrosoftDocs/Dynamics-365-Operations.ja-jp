<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="office-integration-tutorial.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>office-integration-tutorial.d27a27.d29324c626195462da1e4f435ebcd0d5dc0e54de.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d29324c626195462da1e4f435ebcd0d5dc0e54de</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\office-integration\office-integration-tutorial.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Office integration tutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office 統合のチュートリアル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this tutorial, you will use and build Office integration experiences that involve Excel, Word, Document Management, and email.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Excel、Word、ドキュメント管理および電子メールが関係する Office 統合エクスペリエンスを使用して構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Office integration tutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office 統合のチュートリアル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In this tutorial, you will use and build Office integration experiences that involve Excel, Word, Document Management, and email.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Excel、Word、ドキュメント管理および電子メールが関係する Office 統合エクスペリエンスを使用して構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In this tutorial, you will use and build Microsoft Office integration experiences that involve Microsoft Excel, Microsoft Word, the Document Management subsystem, and email.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、<ph id="1">Microsoft Excel</ph>、Microsoft Word、ドキュメント管理および電子メールが関係する <ph id="2">Microsoft Office</ph> 統合エクスペリエンスを使用して構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You will see how Excel and Word use data entities as an entry point into the system, how Excel can become a core part of the user experience, and how Excel and Word can be used for ad-hoc lightweight reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel と Word がデータ エンティティをシステムへのエントリ ポイントとして使用する方法、Excel がユーザー エクスペリエンスの中核になれる方法、Excel と Word を一時的な簡易レポートとして使用できる方法を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You will also see how files can be stored and shared by using the Document Management and email capabilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント管理機能と電子メール機能を使用してファイルを格納および共有する方法も表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For this tutorial, you must access the environment by using Remote Desktop, and you must be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>Access development instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>開発インスタンスへのアクセス<ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If you're running Internet Explorer on the virtual machine (VM), you must enable font and file downloads at <bpt id="p1">**</bpt>Internet Options<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Security<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Custom Level<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシン (VM) で Internet Explorer を実行している場合は、<bpt id="p1">**</bpt>インターネット オプション<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>セキュリティ<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>レベルのカスタマイズ<ept id="p3">**</ept>の順にフォントとファイルのダウンロードを有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Microsoft Visual Studio 2015 runs on the VM, and it must run as an administrator so that metadata and compilation files can be overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 は VM で実行され、メタデータとコンパイル ファイルを上書きできるように、管理者として実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To make sure that Visual Studio runs as an administrator, search for the program, and pin it to the taskbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio が管理者として実行されるようにするには、プログラムを検索してタスクバーに固定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Then right-click the shortcut on the taskbar, right-click <bpt id="p1">**</bpt>Visual Studio 2015<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Advanced<ept id="p3">**</ept>, and select the <bpt id="p4">**</bpt>Run as administrator<ept id="p4">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、タスクバーのショートカットを右クリックして、<bpt id="p1">**</bpt>Visual Studio 2015<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>詳細<ept id="p3">**</ept>をクリックして、<bpt id="p4">**</bpt>管理者として実行<ept id="p4">**</ept>チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Visual Studio will now run as an administrator via a single left click of the taskbar shortcut.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio は、タスク バーのショートカットの 1 回の左クリックで、管理者として実行されるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Entities and OData<ept id="p1">**</ept> – You will use the Microsoft Dynamics Excel Data Connector App (Excel App) to create, read, update, and delete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティと OData<ept id="p1">**</ept> - Microsoft Dynamics Excel データ コネクタ アプリ (Excel App) を使用して、作成、読み取り、更新、および削除を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The connector uses OData services that are created for any entity that is left in the default state of "public" (<bpt id="p1">**</bpt>DataEntity.Public<ept id="p1">**</ept><ph id="ph1">=</ph><bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コネクタは、デフォルト状態の「public」(<bpt id="p1">**</bpt>DataEntity.Public<ept id="p1">**</ept><ph id="ph1">=</ph><bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>) のまま残されているエンティティに対して作成された OData サービスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Apps for Office<ept id="p1">**</ept> – The Excel App is built by using the Apps for Office framework (which is also known as the Office Web API).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Office 用アプリ<ept id="p1">**</ept> - Excel アプリケーションは、Office 用アプリ フレームワーク (Office Web API とも呼ばれます) を使用して作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The Excel App is web-based, and therefore shares technology with the client and will run inside both on-premises Excel instances and Microsoft Excel Online (Microsoft Office 365).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリケーションは Web ベースのため、クライアントと技術を共有し、オンプレミス Excel インスタンスおよび Microsoft Excel Online (Microsoft Office 365) の両方の中で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The app runs inside Excel in a task pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリは、作業ウィンドウの Excel の内部で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Microsoft Office 2016<ept id="p1">**</ept> – The Excel and Word Apps use advances in the Apps for Office framework that were introduced in Office 2016.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Office 2016<ept id="p1">**</ept> – Excel アプリと Word アプリは、Office 2016 で導入された Apps for Office フレームワークの進歩を利用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Therefore, Office 2016 is required in order to run the Excel and Word Apps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、Excel および Word の各アプリケーションを実行するには Office 2016 が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Authentication<ept id="p1">**</ept> – The Excel and Word Apps run in an Internet Explorer window inside Excel and Word.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>認証<ept id="p1">**</ept> - Excel と Word アプリは、Excel と Word 内の Internet Explorer ウィンドウで実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Even if the user is running the client in an InPrivate Browsing session in Internet Explorer, or in a different browser, such as Chrome, Internet Explorer is still used to run the app inside Excel or Word.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが Internet Explorer の InPrivate Browsing セッションまたはクロムなどの異なるブラウザーでクライアントを実行する場合でも、Internet Explorer は Excel または Word 内のアプリを実行するために引き続き使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Authentication is facilitated by OAuth, and the user can select accounts and sign in within the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証は OAuth によって促進され、ユーザーはアプリ内でアカウントを選択してサインインすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Internet Explorer will first try to automatically sign the user in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer は最初にユーザーに自動的にサインインさせようと試みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Therefore, if you aren't signed in as the correct user, or if you have trouble signing in, you might have to force a sign-out from the app by using the sign-out link on the user menu in the lower-right corner of the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、正しいユーザーとしてログインしていない場合や、ログインに問題がある場合は、アプリの右下のユーザー メニューのログアウト リンクを使用して、強制的にアプリからログアウトする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>After sign-out, right-click in the app, and try to sign in again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインアウトの後に、アプリで右クリックし、再度ログインしてみます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Excel App<ept id="p1">**</ept> – In addition to facilitating refresh and publish data operations, the Excel App also provides source and field information, lookups, filtering, error messaging, and a design experience for adding or removing fields, table columns, or labels from entity data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Excel アプリ<ept id="p1">**</ept> - Excel アプリは、更新を促進し、データ操作を公開することに加えて、ソースとフィールド情報、ルックアップ、フィルタリング、エラーメッセージ、エンティティデータソースからフィールド、テーブル列、またはラベルを追加または削除するためのデザイン エクスペリエンスも提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">段取り</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Load the Fleet data set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート データセットの読み込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>During this tutorial, we will mainly use forms, entities, and data in the Fleet Management model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル中に、Fleet Management モデルのフォーム、エンティティ、およびデータを主に使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Therefore, we must first load the Fleet data set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、Fleet データ セットを最初にロードする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fleet<ept id="p3">**</ept> <bpt id="p4">**</bpt>setup<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>フリート<ept id="p3">**</ept> <bpt id="p4">**</bpt>設定<ept id="p4">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Click <bpt id="p1">**</bpt>Create<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Static Export to Excel experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel への静的エクスポート エクスペリエンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Static Export to Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel への静的エクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Static Export to Excel provides a quick mechanism for getting data into grids on a page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel への静的エクスポートは、ページのグリッドにデータを取得するための簡単なメカニズムを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The standard mechanism for triggering Export to Excel is the <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel へのエクスポートを開始するための標準的なメカニズムは、<bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>メニューです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Static Export to Excel is also available via a shortcut menu on the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel への静的エクスポートも、グリッドのショートカット メニューから使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Export to Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Customers<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excelにエクスポート<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>顧客<ept id="p4">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Download and open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックをダウンロードして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Note that the columns in the workbook match the columns in the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブックの列がグリッドの列と一致することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Select ("mark") the first two rows by clicking in the left edge of the row, below the "Select all" check mark.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[すべて選択] チェック マークの下の行の左端をクリックして、最初の 2 行を選択 ("マーク") します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Right-click the grid header to open the shortcut menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ショートカット メニューを表示するためにグリッド ヘッダーを右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Note that both <bpt id="p1">**</bpt>Export all rows<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Export marked rows<ept id="p2">**</ept> are available as commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべての行をエクスポート<ept id="p1">**</ept>および<bpt id="p2">**</bpt>マークした行をエクスポート<ept id="p2">**</ept>の両方がコマンドとして使用できることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Click <bpt id="p1">**</bpt>Export marked rows<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>マークした行をエクスポート<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Note that the columns in the workbook match the columns in the grid, and that the rows that are exported match the rows that you marked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブック内の列はグリッド内の列と一致しており、エクスポートされる行はマークされた行と一致することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Modify the static Export to Excel experience</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的な Excel へのエクスポート エクスペリエンスの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>You can suppress the static Export to Excel mechanism for a grid or change the label that appears on the <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドに Excel メカニズムへの静的エクスポートを非表示にするか、<bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> メニューの <bpt id="p1">**</bpt>開く<ept id="p1">**</ept> に表示されるラベルを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Start Visual Studio 2015.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio 2015 を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Make sure that it's running as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として実行していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> (or press Ctrl+E, Ctrl+E).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>の順にクリックします (または Ctrl + E、Ctrl + E を押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Navigate to <bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>User Interface<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Forms<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMCustomer<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ユーザー インターフェイス<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>フォーム<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMCustomer<ept id="p4">**</ept> と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Right-click <bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Add to new project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいプロジェクトに追加<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In Solution Explorer, double-click the <bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept> form to open the designer view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept> フォームをダブルクリックしてデザイナー ビューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Select <bpt id="p1">**</bpt>FMCustomerDesignTab(Tab)TabPageGrid(TabPage)MainGrid(Grid)<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomerDesignTab(Tab)TabPageGrid(TabPage)MainGrid(Grid)<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, find the <bpt id="p2">**</bpt>Export Label<ept id="p2">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>エクスポート ラベル<ept id="p2">**</ept> プロパティを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Set the <bpt id="p1">**</bpt>Export Label<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Fleet Customers<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスポート ラベル<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>フリート顧客<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Save the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>If you're asked whether you want to overwrite the existing form or save it as a new form, click <bpt id="p1">**</bpt>Overwrite<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のフォームを上書きするか、新しいフォームとしてそれを保存するかを尋ねられたら、<bpt id="p1">**</bpt>上書き<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Build the solution (press Ctrl+Shift+B).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします (Ctrl + Shift + B キーを押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Click <bpt id="p1">**</bpt>Open in Microsoft Office<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Office で開く<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Note that the <bpt id="p1">**</bpt>Customers<ept id="p1">**</ept> option has changed to <bpt id="p2">**</bpt>Fleet Customers<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>オプションが<bpt id="p2">**</bpt>フリート顧客<ept id="p2">**</ept>に変更されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Generated Open in Excel experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成された Excel で開くエクスペリエンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Generated Open in Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成された Excel で開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Generated Open in Excel options are automatically added to forms when the system finds data entities that have the same root data source as the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成された Excel で開くオプションは、フォームとして同じルート データ ソースを持つデータ エンティティをシステムが検出するときに、自動的にフォームに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The workbook that is generated will contain a single table data source where the data from that entity is loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたワークブックには、そのエンティティからのデータがロードされる単一のテーブルデータ ソースが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The Open in Excel experiences are listed on the <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で開くエクスペリエンスは、<bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>メニューにリストされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>(When an entity has the same root data source as a form, it's added as an option in the <bpt id="p1">**</bpt>Open in Excel<ept id="p1">**</ept> section of the <bpt id="p2">**</bpt>Open in Microsoft Office<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(エンティティがフォームと同じルート データ ソースを持っている場合は、<bpt id="p2">**</bpt>Microsoft Office で開く<ept id="p2">**</ept>メニューの <bpt id="p1">**</bpt>Excel で開く<ept id="p1">**</ept>セクションでオプションとして追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>This option is referred to as a “generated” option.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは「生成済み」オプションと呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Open in Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Fleet Management Customers (unfiltered)<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excel で開く<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>フリート管理の顧客 (フィルター処理なし)<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Download and open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックをダウンロードして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This workbook contains the Excel Data Connector App, a binding to the <bpt id="p1">**</bpt>Fleet Management Customer<ept id="p1">**</ept> entity, and a pointer to the server that the workbook was generated from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このブックには、<bpt id="p1">**</bpt>フリート管理顧客<ept id="p1">**</ept>エンティティへのバインドである Excel データ コネクタ アプリと、ブックを生成したサーバーへのポインタが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Click <bpt id="p1">**</bpt>Enable editing<ept id="p1">**</ept> to enable the Excel Data Connector App to load.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックすると、Excel データ コネクタ アプリがデータの読み込みを行えるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Customer data is read from the OData service on the server and added to the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客データは、サーバー上の OData サービスから読み取られ、テーブルに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>In Internet Explorer, on the <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept> (or press F2), and change the email address of one of the customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer 上の<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>編集<ept id="p2">**</ept>をクリックして (または F2 キーを押して)、いずれかの顧客の電子メール アドレスを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the Excel App, click <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリで、<bpt id="p1">**</bpt>更新<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Note that the new email address is shown in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel に新しい電子メール アドレスが表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In Excel, change the email address of one of the customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で、いずれかの顧客の電子メール アドレスを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>In the Excel App, click <bpt id="p1">**</bpt>Publish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリで、<bpt id="p1">**</bpt>公開<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>In Internet Explorer, click <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> in the upper right of the page (or press Shift+F5).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、ページの右上にある<bpt id="p1">**</bpt>更新<ept id="p1">**</ept>をクリックします (または Shift キーを押しながら F5 キーを押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Note that the new email address is shown on the <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい電子メール アドレスが<bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>ページに表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>In Excel, click the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> (gear) button in the lower-right corner of the Excel App.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で、Excel アプリの右下隅にある<bpt id="p1">**</bpt>設定<ept id="p1">**</ept> (歯車) ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>You can use the dialog box that appears to adjust the settings in the current workbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるダイアログ ボックスを使用すると、現在のブック内の設定を調整することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Note that the <bpt id="p1">**</bpt>Server URL<ept id="p1">**</ept> value matches the start of the URL that is shown in Internet Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サーバー URL<ept id="p1">**</ept> の値が、Internet Explorer で示されている URL の開始と一致していることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Also note that the data refresh and data publish operations are listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ更新およびデータ公開操作が一覧表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Click <bpt id="p1">**</bpt>Cancel<ept id="p1">**</ept> to close the <bpt id="p2">**</bpt>Settings<ept id="p2">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キャンセル<ept id="p1">**</ept>をクリックして<bpt id="p2">**</bpt>設定<ept id="p2">**</ept>ダイアログ ボックスを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Click the <bpt id="p1">**</bpt>Message Center<ept id="p1">**</ept> (flag) button in the lower-right corner of the Excel App.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリの右下隅にある<bpt id="p1">**</bpt>メッセージ センター<ept id="p1">**</ept> (旗) ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The message center dialog box that appears provides information about what is occurring in the Excel App.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるメッセージ センター ダイアログ ボックスには、Excel アプリケーションで発生している内容に関する情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Add and remove table columns from an existing table data source in the Excel App</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリケーションで既存のテーブル データ ソースからテーブルの列の追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The Excel App has a design experience that lets users add and edit bindings to entity data sources and labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリケーションには、ユーザーがエンティティ データ ソースおよびラベルへのバインディングを追加および編集できるデザイン エクスペリエンスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To add and remove fields from an existing binding, you use the edit experience that is outlined in the following steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のバインドからフィールドを追加および削除するには、、次の手順で説明している編集エクスペリエンスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Get a workbook that has an existing table data source:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のテーブル データ ソースを持つブックを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Click <bpt id="p1">**</bpt>Open in Microsoft Office<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Open in Excel<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fleet Management Customers (unfiltered)<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Office で開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Excel で開く<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>フリート管理の顧客 (フィルター処理なし)<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Download and open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックをダウンロードして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>This workbook contains the Excel Data Connector App, a binding to the Fleet Management Customer entity, and a pointer to the server that the workbook was generated from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このブックには、Excel データ コネクタ アプリ、フリート管理顧客エンティティへのバインド、およびブックを生成したサーバーへのポインターが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Click <bpt id="p1">**</bpt>Enable editing<ept id="p1">**</ept> to enable the Excel Data Connector App to load.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックすると、Excel データ コネクタ アプリがデータの読み込みを行えるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Customer data is read from the OData service on the server and added to the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客データは、サーバー上の OData サービスから読み取られ、テーブルに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Open the data source for editing:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">編集のためのデータ ソースを開く:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>In Excel, in the Excel App, click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel では、Excel アプリで<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>A list of table and field data sources appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルおよびフィールド データ ソースの一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Click the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> (pencil) button next to the existing table data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のテーブル データ ソースの横の<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>ボタン (鉛筆) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The data source details are shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの詳細が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Remove fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>In the <bpt id="p1">**</bpt>Selected<ept id="p1">**</ept> list, double-click a field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択済<ept id="p1">**</ept>リストで、フィールドをダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Alternatively, click a field, and then click <bpt id="p1">**</bpt>Remove<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、フィールドをクリックし、その後<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>To select multiple fields, keep the Ctrl key held down while you click them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>To select all fields, press Ctrl+A.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのフィールドを選択するには、Ctrl+A キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Add fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>In the <bpt id="p1">**</bpt>Available<ept id="p1">**</ept> list, double-click a field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>使用可能<ept id="p1">**</ept>リストで、フィールドをダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Alternatively, click a field, and then click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、フィールドをクリックし、その後<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>To select multiple fields, keep the Ctrl key held down while you click them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>To select all fields, press Ctrl+A.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのフィールドを選択するには、Ctrl+A キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Change the field order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの順序を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>In the <bpt id="p1">**</bpt>Selected<ept id="p1">**</ept> list, click a field, and then click <bpt id="p2">**</bpt>Up<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Down<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択済<ept id="p1">**</ept>リストで、フィールドをクリックしてから<bpt id="p2">**</bpt>上<ept id="p2">**</ept>または<bpt id="p3">**</bpt>下<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Change a field label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド ラベルの変更。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>In the <bpt id="p1">&lt;strong&gt;</bpt>Selected<ept id="p1">&lt;/strong&gt;</ept> list, click a field, and then click in the <bpt id="p2">&lt;strong&gt;</bpt>Column label<ept id="p2">&lt;/strong&gt;</ept> field below the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>選択済<ept id="p1">&lt;/strong&gt;</ept>リストで、フィールドをクリックしてから、リストの下にある<bpt id="p2">&lt;strong&gt;</bpt>列ラベル<ept id="p2">&lt;/strong&gt;</ept> フィールドをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>You can change the label to either a static string or a label identifier that will be translated to the active language (for example, <bpt id="p1">&lt;strong&gt;</bpt>@SYS129977<ept id="p1">&lt;/strong&gt;</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクティブ言語に翻訳される静的文字列またはラベル識別子のいずれかにラベルを変更することができます (たとえば、<bpt id="p1">&lt;strong&gt;</bpt>@SYS129977<ept id="p1">&lt;/strong&gt;</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Apply the changes that you made to data source fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース フィールドに行った変更を適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Click <bpt id="p1">**</bpt>Update<ept id="p1">**</ept> to return to the data source list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept>をクリックしてデータ ソース リストに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Click <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> to make sure that any new fields are filled with data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept>をクリックし、新しいフィールドにデータが入力されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Change an automatically generated Open in Excel experience</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動的に生成された Excel で開くエクスペリエンスを変更する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The automatically generated Open in Excel experiences that are created for entities have a single table binding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ向けに作成される自動生成された [Excel で開く] エクスペリエンスには、1 つのテーブル バインディングがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>The list of fields that are added to that table binding is defined by the <bpt id="p1">**</bpt>AutoReport<ept id="p1">**</ept> field group if the table binding contains fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのテーブル バインディングに追加されるフィールドのリストは、テーブル バインディングにフィールドが含まれている場合は、<bpt id="p1">**</bpt>AutoReport<ept id="p1">**</ept> フィールド グループによって定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Otherwise, the key and mandatory fields for the entity are automatically added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、エンティティのキーおよび必須フィールドが自動的に追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The order of fields in the <bpt id="p1">**</bpt>AutoReport<ept id="p1">**</ept> group determines the order of fields in the table binding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AutoReport<ept id="p1">**</ept> グループのフィールドの順序は、テーブル バインディングのフィールドの順序を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Start Visual Studio 2015.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio 2015 を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Make sure that it's running as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として実行していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> (or press Ctrl+E, Ctrl+E).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>の順にクリックします (または Ctrl + E、Ctrl + E を押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Navigate to <bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data Model<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Data Entities<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMCustomerEntity<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>データ モデル<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>データ エンティティ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMCustomerEntity<ept id="p4">**</ept> と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Right-click <bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Add to project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>プロジェクトに追加<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Expand <bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Field Groups<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>AutoReport<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>フィールド グループ<ept id="p2">**</ept><ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>AutoReport<ept id="p3">**</ept> を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Reverse the order of the <bpt id="p1">**</bpt>First name<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Last name<ept id="p2">**</ept> fields by clicking the <bpt id="p3">**</bpt>Last name<ept id="p3">**</ept> field and moving it up (press Alt+Up arrow key).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>性<ept id="p3">**</ept> フィールドをクリックして上に移動 (Alt+Up 矢印キーを押す) することにより、<bpt id="p1">**</bpt>名<ept id="p1">**</ept> と <bpt id="p2">**</bpt>性<ept id="p2">**</ept> フィールドを取り消します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Save the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>If you're asked whether you want to overwrite the existing entity or save it as a new entity, click <bpt id="p1">**</bpt>Overwrite<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のエンティティを上書きするか、新しいエンティティとしてそれを保存するかを尋ねられたら、<bpt id="p1">**</bpt>上書き<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Build the solution (press Ctrl+Shift+B).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします (Ctrl + Shift + B キーを押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Open in Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Fleet Management Customers<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excel で開く<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>フリート管理の顧客<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Click <bpt id="p1">**</bpt>Enable editing<ept id="p1">**</ept> to enable the Excel Data Connector App to load.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックすると、Excel データ コネクタ アプリがデータの読み込みを行えるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Note that the <bpt id="p1">**</bpt>Last name<ept id="p1">**</ept> column appears before the <bpt id="p2">**</bpt>First name<ept id="p2">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>姓<ept id="p1">**</ept>列は<bpt id="p2">**</bpt>名<ept id="p2">**</ept>列の前に表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Open in Excel Online</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel Online で開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>The Excel App is built by using a new Apps for Office framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリケーションは、Office フレームワークの新しいアプリケーションを使用して構築されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>This framework provides a JavaScript-based web application programming interface (API) that enables apps to communicate with Office applications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフレームワークは、アプリケーションが Office アプリケーションと通信できる JavaScript ベースの Web アプリケーション プログラミング インターフェイス (API) を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The biggest advantage of this new framework is that apps can run in on-premises Excel instances (Win32), Excel Online (Office 365), and Excel on the Apple iPad.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この新しいフレームワークの最大の利点は、アプリケーションが社内の Excel インスタンス (Win32)、Excel Online (Office 365)、および Excel の Apple iPad で実行できることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>They will also be able to run in other Excel apps in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来的に他の Excel アプリでも実行できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Open in Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Fleet Management Customers<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excel で開く<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>フリート管理の顧客<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Click <bpt id="p1">**</bpt>SharePoint<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細行プロパティの詳細については、<bpt id="p1">**</bpt>SharePoint<ept id="p1">**</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Browse to the desired Microsoft SharePoint folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的の Microsoft SharePoint フォルダーを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>The default behavior is to open the file after it's saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の動作では、保存後にファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Note that the workbook opens in Excel Online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブックが Excel Online で開くことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>In Excel Online, capabilities of the Excel App, such as refresh and publish, and the design experience, should work just as they work in on-premises Excel instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel Online では、更新や公開などの Excel アプリの機能、およびデザイン体験が、オンプレミスの Excel インスタンスと同様に機能する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Template Open in Excel experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で開いたテンプレートのエクスペリエンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Template Open in Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で開いたテンプレート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Template options resemble the generated Open in Excel options.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレート オプションは、生成された [Excel で開く] のオプションと似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>They are automatically added to forms when the system finds templates that have the same first data source as the root data source in the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム内のルート データ ソースと同じ最初のデータ ソースを持つテンプレートがシステムによって検出されると、フォームに自動的に追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>A workbook template can have multiple data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークブック テンプレートは、複数のデータ ソースを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>It can also have unbound content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、バインドされていないコンテンツを持つこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>The Open in Excel experiences are listed on the <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で開くエクスペリエンスは、<bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>メニューにリストされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>The <bpt id="p1">**</bpt>Excel workbook designer<ept id="p1">**</ept> page provides an easy way to get a generated Open in Excel experience for an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Excel ブック デザイナー<ept id="p1">**</ept> ページには、エンティティの生成された [Excel で開く] エクスペリエンスで取得する簡単な方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>It also provides a mechanism getting a blank workbook that contains just the Excel App and a pointer to the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、Excel アプリおよびサーバーへのポインターを含む空白のブックを取得するメカニズムも提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Common<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Common<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office integration<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Excel workbook designer<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>共通<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>共通<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office 統合<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Excel ブック デザイナー<ept id="p4">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select the <bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> エンティティを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Add all fields in the list of available fields to the list of selected fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したフィールドのリストに利用可能なフィールドのリストのすべてのフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Click <bpt id="p1">**</bpt>Create workbook<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブックの作成<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>This workbook contains the Excel Data Connector App, a binding to the <bpt id="p1">**</bpt>Fleet Management Customer<ept id="p1">**</ept> entity, and a pointer to the server that the workbook was generated from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このブックには、<bpt id="p1">**</bpt>フリート管理顧客<ept id="p1">**</ept>エンティティへのバインドである Excel データ コネクタ アプリと、ブックを生成したサーバーへのポインタが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Click <bpt id="p1">**</bpt>Enable editing<ept id="p1">**</ept> to enable the Excel Data Connector App to load.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックすると、Excel データ コネクタ アプリがデータの読み込みを行えるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Customer data is read from the OData service on the server and added to the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客データは、サーバー上の OData サービスから読み取られ、テーブルに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Insert a blank row above the table, and enter <bpt id="p1">**</bpt>Fleet Customers<ept id="p1">**</ept> as the title.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル上に空白行を挿入し、タイトルとして<bpt id="p1">**</bpt>フリート顧客<ept id="p1">**</ept>と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Rename the worksheet <bpt id="p1">**</bpt>FleetCustomers<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークシート <bpt id="p1">**</bpt>FleetCustomers<ept id="p1">**</ept> の名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Rearrange some of the fields in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの一部のフィールドを再配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> to open the design experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>をクリックし、デザイン体験を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Next to the <bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> data source, there are buttons for editing and deleting the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> データ ソースの横に、データ ソースを編集および削除するためのボタンがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> to see the field list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド リストを表示するには、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select fields, and move them as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを選択し、必要に応じてに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Set the order for the first three fields to <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept>, <bpt id="p2">**</bpt>LastName<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>DriverLicense<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の 3 つのフィールドの順序を <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept>、<bpt id="p2">**</bpt>LastName<ept id="p2">**</ept>、<bpt id="p3">**</bpt>DriverLicense<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Click <bpt id="p1">**</bpt>Update<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Note that the field order is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの順序は変わることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Click <bpt id="p1">**</bpt>Done<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Click the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> (gear) button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept> (ギア) ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Click <bpt id="p1">**</bpt>Clear binding data<ept id="p1">**</ept> so that the workbook contains no bound data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインドされたデータがワークブックに含まれないように<bpt id="p1">**</bpt>バインディング データのクリア<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Save the workbook as <bpt id="p1">**</bpt>FleetCustomersBasic.xlsx<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブックを <bpt id="p1">**</bpt>FleetCustomersBasic.xlsx<ept id="p1">**</ept> という名前で保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Common<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Common<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office integration<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Document templates<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>共通<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>共通<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office 統合<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>ドキュメント テンプレート<ept id="p4">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Browse to the file that you just saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存したファイルを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The template is added as a line in the templates table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートは、テンプレート テーブルの行として追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>In the <bpt id="p1">**</bpt>FleetCustomersBasic<ept id="p1">**</ept> row, clear the <bpt id="p2">**</bpt>Apply current record filter<ept id="p2">**</ept> check box, so that an unfiltered list of customers will be loaded after the template is opened.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomersBasic<ept id="p1">**</ept> 行で、<bpt id="p2">**</bpt>現在のレコード フィルターの適用<ept id="p2">**</ept>チェック ボックスをオフにすると、テンプレートが開かれた後にフィルター処理されていない顧客の一覧が読み込まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Change the <bpt id="p1">**</bpt>Template display name<ept id="p1">**</ept> value to <bpt id="p2">**</bpt>Fleet Customers Basic<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレートの表示名<ept id="p1">**</ept>値を<bpt id="p2">**</bpt>基本フリートカスタマー<ept id="p2">**</ept>に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Note that <bpt id="p1">**</bpt>Fleet Customers Basic<ept id="p1">**</ept> is now an option in the <bpt id="p2">**</bpt>Open in Excel<ept id="p2">**</ept> section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フリート顧客ベーシック<ept id="p1">**</ept>は、<bpt id="p2">**</bpt>Excel で開く<ept id="p2">**</ept>セクションのオプションになっていることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Click that option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのオプションをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Click <bpt id="p1">**</bpt>Enable editing<ept id="p1">**</ept> to enable the Excel Data Connector App to load.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックすると、Excel データ コネクタ アプリがデータの読み込みを行えるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Customer data is read from the OData service on the server and added to the table binding that you created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客データは、サーバー上の OData サービスから読み取られ、作成したテーブルのバインドに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Register a template as a system-defined template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム定義のテンプレートとしてテンプレートを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Templates that are registered as system-defined templates are loaded at deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム定義のテンプレートとして登録されているテンプレートは、配置時に読み込まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>This behavior is useful for independent software vendors (ISVs) and partners that want to package templates together with other model artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この動作は、他のモデル コンポーネントと一緒にテンプレートをパッケージ化する独立系ソフトウェア ベンダー (ISV) やパートナーにとって役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Start Visual Studio 2015 by opening the previously created project where the model is set to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept>, or create a new project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルが<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept>に設定されている以前に作成したプロジェクトを開いて Visual Studio 2015 を起動するか、または新しいプロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Right-click the project, and then click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Select the <bpt id="p1">**</bpt>Resource<ept id="p1">**</ept> item type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リソース<ept id="p1">**</ept> 品目タイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Set the name to <bpt id="p1">**</bpt>FleetCustomersBasicTemplate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を <bpt id="p1">**</bpt>FleetCustomersBasicTemplate<ept id="p1">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Make sure that the FleetCustomersBasic.xlsx file is closed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetCustomersBasic.xlsx ファイルが閉じられていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Select the <bpt id="p1">**</bpt>FleetCustomersBasic.xlsx<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomersBasic.xlsx<ept id="p1">**</ept> ファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Note that the resource is added to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソースがプロジェクトに追加されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> (or press Ctrl+E, Ctrl+E).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>の順にクリックします (または Ctrl + E、Ctrl + E を押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Navigate to <bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Code<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMTemplateRegistrations<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>クラス<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>コード<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMTemplateRegistrations<ept id="p4">**</ept> と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Right-click <bpt id="p1">**</bpt>FMTemplateRegistrations<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Add to project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTemplateRegistrations<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>プロジェクトに追加<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Open <bpt id="p1">**</bpt>FMTemplateRegistrations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTemplateRegistrations<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>The FMTemplateRegistrations.xpp code file should be shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTemplateRegistrations.xpp コード ファイルが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Copy one of the existing lines, and change it by providing the template name, resource name, description, display name, and <bpt id="p1">**</bpt>Apply current record filter<ept id="p1">**</ept> and <bpt id="p2">**</bpt>List in Open in Office menu<ept id="p2">**</ept> values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の行の 1 つをコピーし、テンプレート名、リソース名、説明、表示名、および<bpt id="p1">**</bpt>現在のレコード フィルターの適用<ept id="p1">**</ept>と <bpt id="p2">**</bpt>Office で開くメニューに表示<ept id="p2">**</ept>の値を指定して変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>The display name is the text that appears as an Open in Excel option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示名は、[Excel で開く] オプションとして表示されるテキストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>The description appears when the user holds the pointer over that item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがその項目の上にポインタを置くと説明が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>The display name and description can be either labels or static strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示名と説明には、ラベルまたは静的な文字列を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>The code should resemble the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードは次の例のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Save the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>If you're asked whether you want to overwrite the existing code or save it as a new file, click <bpt id="p1">**</bpt>Overwrite<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコードを上書きするか、新しいファイルとしてそれを保存するかを尋ねられたら、<bpt id="p1">**</bpt>上書き<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Build the solution (press Ctrl+Shift+B).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします (Ctrl + Shift + B キーを押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Verify that the change was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更が正常に完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Common<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Common<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office integration<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Document templates<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>共通<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>共通<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office 統合<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>ドキュメント テンプレート<ept id="p4">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Click <bpt id="p1">**</bpt>Reload system templates<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム テンプレートの再読み込み<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to confirm that you want to reload the system templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックして、システム テンプレートの再読み込みを確定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Verify that the new system-defined template is loaded, and that the template name is <bpt id="p1">**</bpt>FleetCustomersBasicTemplate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいシステム定義テンプレートが読み込まれたこと、そのテンプレート名が <bpt id="p1">**</bpt>FleetCustomersBasicTemplate<ept id="p1">**</ept> であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Journal Entry in Excel experience powered by a template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートによる Excel での仕訳入力エクスペリエンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>General ledger<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Journal entries<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>General journals<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>総勘定元帳<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>仕訳入力<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>一般仕訳帳<ept id="p3">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Make sure that you're in company <bpt id="p1">**</bpt>USMF<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社 <bpt id="p1">**</bpt>USMF<ept id="p1">**</ept> にいることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Create a new journal by clicking <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept>をクリックし、新しい仕訳帳を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Set the name to <bpt id="p1">**</bpt>GenJrn<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を <bpt id="p1">**</bpt>GenJrn<ept id="p1">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Click <bpt id="p1">**</bpt>Open lines in Excel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Excel で明細行を開く<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Open the workbook that is generated, and enable editing as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開いて、必要に応じて編集を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Note that header fields are filled with data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘッダー フィールドにデータが設定されていることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Enter a new line, and set the <bpt id="p1">**</bpt>MainAccount<ept id="p1">**</ept> field to <bpt id="p2">**</bpt>110110<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい行を入力し、<bpt id="p1">**</bpt>MainAccount<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>110110<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Enter a description, a currency, and a debit amount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明、通貨、および借方金額を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Note that lookups are provided for the company and currency fields, because those relationships are defined for this entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの関係はこのエンティティに定義されているため、ルックアップは会社と通貨のフィールドに指定されていることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Click <bpt id="p1">**</bpt>Publish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>発行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Note that the line is updated with the current date and a debit amount of 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細行が現在の日付と 0 (ゼロ) の借方金額がで更新されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>In Internet Explorer, click <bpt id="p1">**</bpt>Lines<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>行<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Note that line that you entered in Excel is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で入力した明細行が表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Lookups in Excel experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel でのルックアップ エクスペリエンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Lookups in the Excel App</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel アプリでのルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>To facilitate data entry, the Excel App provides lookups and data assistance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ入力を容易にするため、Excel App はルックアップとデータ支援を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Date fields provide a date picker, enumeration (enum) fields provide an enum list, and relationships provide a relationship lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付フィールドは日付の選択の提供、列挙 (列挙) フィールドは列挙リストの提供、リレーションシップはリレーションシップ ルックアップの提供をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Rentals<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Rental<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>レンタル<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>レンタル<ept id="p3">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Open in Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Fleet Management Rentals<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excel で開く<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>フリート管理のレンタル<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Click <bpt id="p1">**</bpt>Enable editing<ept id="p1">**</ept> to enable the Excel Data Connector App to load and read in data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックすると、Excel データ コネクタ アプリがデータの読み込みと読み取りを行えるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Click a <bpt id="p1">**</bpt>Drivers license<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>運転免許証<ept id="p1">**</ept>値をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Note that a relationship lookup now appears in the Excel App and shows a list of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ルックアップが Excel アプリで表示され、顧客の一覧を表示することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Because relationship lookups are in their first generation, no filtering or sorting is currently supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ルックアップは最初の世代であるため、現在フィルター処理または並べ替えはサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Click another customer in the lookup, and note that the <bpt id="p1">**</bpt>Drivers license<ept id="p1">**</ept> value changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップで別の顧客をクリックし、<bpt id="p1">**</bpt>運転免許証<ept id="p1">**</ept>の値が変化することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Because this field is part of the key, click the original <bpt id="p1">**</bpt>Drivers license<ept id="p1">**</ept> value to reset it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドはキーの一部なので、元の<bpt id="p1">**</bpt>運転免許証<ept id="p1">**</ept>値をクリックしてリセットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Note that the <bpt id="p1">**</bpt>Drivers license<ept id="p1">**</ept>, <bpt id="p2">**</bpt>First name<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>Last name<ept id="p3">**</ept> fields form a multi-part key, but the Excel App doesn’t immediately change all parts of the multi-part key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>運転免許証<ept id="p1">**</ept>、<bpt id="p2">**</bpt>名<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>姓<ept id="p3">**</ept>のフィールドはマルチパート キーを形成しますが、Excel アプリはマルチパート キーのすべての部分をすぐに変更しないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Click a <bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始日<ept id="p1">**</ept>値をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Note that a date picker now appears in the Excel App.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付の選択が Excel アプリで表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Click another date to change the <bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の日付をクリックすると、<bpt id="p1">**</bpt>開始日<ept id="p1">**</ept>の値が変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>, and edit the FleetRental data source by adding the <bpt id="p2">**</bpt>Status<ept id="p2">**</ept> field as a column in the table binding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>をクリックし、FleetRental データ ソースを編集するには、<bpt id="p2">**</bpt>ステータス<ept id="p2">**</ept> フィールドをテーブル バインディングの列として追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>When you've finished adding the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> column, click a <bpt id="p2">**</bpt>Status<ept id="p2">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>状態<ept id="p1">**</ept> 列の追加が完了したら、<bpt id="p2">**</bpt>状態<ept id="p2">**</ept> 値をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Note that an enum list now appears in the Excel App.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙リストが Excel アプリで表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>While focus is in the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> column, move up and down the list of rentals to see how quickly the enum list changes to reflect the current value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーカスが <bpt id="p1">**</bpt>状態<ept id="p1">**</ept> 列にあるとき、レンタルのリストを上下に動かして、現在の値を反映するために列挙型リストがどれだけ早く変更されるか確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>The whole enum list is shown, so that the user can quickly see all the available values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが使用可能なすべての値をすばやく表示できるように、列挙リスト全体が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Click a different <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> value to see how an enum value can be changed by using a single click.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の<bpt id="p1">**</bpt>状態<ept id="p1">**</ept>値をクリックすると、クリック 1 回で列挙値を変更する方法を確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Create a relationship lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ルックアップを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>When relationships exist between entities, a relationship lookup is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ間にリレーションシップが存在するときは、リレーションシップ ルックアップが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Start Visual Studio 2015 by opening the previously created project where the model is set to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept>, or create a new project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルが<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept>に設定されている以前に作成したプロジェクトを開いて Visual Studio 2015 を起動するか、または新しいプロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> (or press Ctrl+E, Ctrl+E).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>の順にクリックします (または Ctrl + E、Ctrl + E を押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Navigate to <bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data Model<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Tables<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMCustGroup<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOT<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>データ モデル<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>テーブル<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>FMCustGroup<ept id="p4">**</ept> と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Right-click, and then click <bpt id="p1">**</bpt>Open designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックしてから、<bpt id="p1">**</bpt>デザイナーを開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>In the designer, right-click <bpt id="p1">**</bpt>FMCustGroup<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Addins<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Create data entity<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>FMCustGroup<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>アドイン<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>データ エンティティの作成<ept id="p3">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Artifacts are added to the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントはプロジェクトに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Open the designer view for <bpt id="p1">**</bpt>FMCustGroupEntity<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustGroupEntity<ept id="p1">**</ept> のデザイナー ビューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>In the property sheet for <bpt id="p1">**</bpt>FMCustGroupEntity<ept id="p1">**</ept>, set <bpt id="p2">**</bpt>Public Collection Name<ept id="p2">**</ept> to <bpt id="p3">**</bpt>FleetCustomerGroups<ept id="p3">**</ept> and <bpt id="p4">**</bpt>Public Entity Name<ept id="p4">**</ept> to <bpt id="p5">**</bpt>FleetCustomerGroup<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustGroupEntity<ept id="p1">**</ept> のプロパティ シートで、<bpt id="p2">**</bpt>パブリック コレクション名<ept id="p2">**</ept>を <bpt id="p3">**</bpt>FleetCustomerGroups<ept id="p3">**</ept> に、<bpt id="p4">**</bpt>パブリック エンティティ名<ept id="p4">**</ept>を <bpt id="p5">**</bpt>FleetCustomerGroup<ept id="p5">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Add the <bpt id="p1">**</bpt>CustGroup<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Description<ept id="p2">**</ept> fields to the <bpt id="p3">**</bpt>AutoLookup<ept id="p3">**</ept> field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>AutoLookup<ept id="p3">**</ept> フィールド グループに <bpt id="p1">**</bpt>CustGroup<ept id="p1">**</ept> と <bpt id="p2">**</bpt>説明<ept id="p2">**</ept>フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>If <bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> isn't already in the project, add it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> がまだプロジェクトに入っていない場合、それを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Open the designer view for <bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> のデザイナー ビューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Right-click <bpt id="p1">**</bpt>Relations<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Relation<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>関係<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>On the new relation, set <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> to <bpt id="p2">**</bpt>CustomerGroup<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Cardinality<ept id="p3">**</ept> to <bpt id="p4">**</bpt>ZeroMore<ept id="p4">**</ept>, <bpt id="p5">**</bpt>RelatedDataEntity<ept id="p5">**</ept> to <bpt id="p6">**</bpt>FMCustGroupEntity<ept id="p6">**</ept>, <bpt id="p7">**</bpt>RelatedDataEntityCardinality<ept id="p7">**</ept> to <bpt id="p8">**</bpt>ZeroOne<ept id="p8">**</ept>, <bpt id="p9">**</bpt>RelationshipType<ept id="p9">**</ept> to <bpt id="p10">**</bpt>Association<ept id="p10">**</ept>, <bpt id="p11">**</bpt>Role<ept id="p11">**</ept> to <bpt id="p12">**</bpt>CustomerGroupSource<ept id="p12">**</ept>, and <bpt id="p13">**</bpt>RelatedDataEntityRole<ept id="p13">**</ept> to <bpt id="p14">**</bpt>CustomerGroupTarget<ept id="p14">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいリレーションで、<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>を <bpt id="p2">**</bpt>CustomerGroup<ept id="p2">**</ept> に、<bpt id="p3">**</bpt>基数<ept id="p3">**</ept>を <bpt id="p4">**</bpt>ZeroMore<ept id="p4">**</ept> に、<bpt id="p5">**</bpt>RelatedDataEntity<ept id="p5">**</ept> を <bpt id="p6">**</bpt>FMCustGroupEntity<ept id="p6">**</ept> に、<bpt id="p7">**</bpt>RelatedDataEntityCardinality<ept id="p7">**</ept> を <bpt id="p8">**</bpt>ZeroOne<ept id="p8">**</ept> に、<bpt id="p9">**</bpt>RelationshipType<ept id="p9">**</ept> を<bpt id="p10">**</bpt>関連<ept id="p10">**</ept>に、<bpt id="p11">**</bpt>ロール<ept id="p11">**</ept>を <bpt id="p12">**</bpt>CustomerGroupSource<ept id="p12">**</ept> に、および <bpt id="p13">**</bpt>RelatedDataEntityRole<ept id="p13">**</ept> を <bpt id="p14">**</bpt>CustomerGroupTarget<ept id="p14">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Build the solution (press Ctrl+Shift+B).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします (Ctrl + Shift + B キーを押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Verify that the change was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更が正常に完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Open in Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Fleet Management Customers<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excel で開く<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>フリート管理の顧客<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Click a <bpt id="p1">**</bpt>Customer group<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客分類グループ<ept id="p1">**</ept>値をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Change the <bpt id="p1">**</bpt>Customer group<ept id="p1">**</ept> value for a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の<bpt id="p1">**</bpt>顧客グループ<ept id="p1">**</ept>値を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Publish the change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Change the value back, and publish that change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を元に戻し、その変更を公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Create a custom lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ルックアップの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>You can create custom lookups to show data options when an enum or relationship isn't sufficient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型またはリレーションシップが十分でないとき、データ オプションを表示するカスタム ルックアップを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>The main use case is when data must be retrieved from an external service and presented in real time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主な使用例は、外部サービスからデータを取得し、リアルタイムで提示する必要がある場合です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Start Visual Studio 2015 by opening the previously created project where the model is set to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept>, or create a new project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルが<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept>に設定されている以前に作成したプロジェクトを開いて Visual Studio 2015 を起動するか、または新しいプロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Open the designer view for <bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMCustomerEntity<ept id="p1">**</ept> のデザイナー ビューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Right-click <bpt id="p1">**</bpt>Methods<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Method<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッド<ept id="p1">**</ept> を右クリックし、 <bpt id="p2">**</bpt>新規メソッド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Add the <bpt id="p1">**</bpt>lookup<ph id="ph1">\_</ph>Country<ept id="p1">**</ept> code from the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例から <bpt id="p1">**</bpt>lookup<ph id="ph1">\_</ph>Country<ept id="p1">**</ept> コードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Save the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>If you're asked whether you want to overwrite the existing code or save is as a new file, click <bpt id="p1">**</bpt>Overwrite<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコードを上書きするか、新しいファイルとして保存するかを尋ねられたら、<bpt id="p1">**</bpt>上書き<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Build the solution (press Ctrl+Shift+B).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします (Ctrl + Shift + B キーを押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Verify that the change was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更が正常に完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Open in Excel<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Fleet Management Customers<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Excel で開く<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>フリート管理の顧客<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Open the workbook that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたブックを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Click a <bpt id="p1">**</bpt>Country<ept id="p1">**</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>国<ept id="p1">**</ept>値をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Change the <bpt id="p1">**</bpt>Country<ept id="p1">**</ept> value for a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の<bpt id="p1">**</bpt>国<ept id="p1">**</ept>値を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Publish the change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Change the value back, and publish that change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を元に戻し、その変更を公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Export to Word experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word エクスペリエンスへエキスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Export to Word</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word にエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Export to Word experiences can be used for lightweight reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word エクスペリエンスへのエクスポートは、簡易レポートに使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>They are powered by pre-built templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">あらかじめ構築されたテンプレートによって強化されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>The Export to Word experiences are listed on the <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word へのエクスポート エクスペリエンスは、<bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>メニューにリストされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Let's look at an example experience that has been created for Fleet Management Customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理の顧客に対して作成された体験例を見てみましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>Click <bpt id="p1">**</bpt>Open in<ept id="p1">**</ept> <bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Export to Word<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Customer information Fleet Management Customers (unfiltered)<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Microsoft Office<ept id="p2">**</ept> で<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Word にエクスポート<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>顧客情報フリート管理の顧客 (フィルター処理なし)<ept id="p4">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Download and open the document that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたドキュメントをダウンロードして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>The document contains data from the record that is currently selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントには、現在選択されているレコードのデータが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>Create a Word template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word テンプレートを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>The Microsoft Dynamics App for Office can be run in Word to enable the creation of templates that can then be used for document generation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics App for Office は、Word で実行でき、ドキュメントの生成のために使用できるテンプレートの作成を可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Add a trusted catalog that points to the file share that contains the Microsoft Dynamics App manifest:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics アプリ マニフェストを含むファイル共有を指定する信頼済カタログを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>In Word, click <bpt id="p1">**</bpt>File<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Options<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word で、<bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>オプション<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Click <bpt id="p1">**</bpt>Trust Center<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Trust Center Settings<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Trust Center<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Trust Center の設定<ept id="p2">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Click <bpt id="p1">**</bpt>Trusted Add-in Catalogs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>信頼済のアドイン カタログ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>In the <bpt id="p1">**</bpt>Catalog URL<ept id="p1">**</ept> field, enter the file share location of the manifest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カタログ URL<ept id="p1">**</ept> フィールドに、マニフェストのファイル共有の場所を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Click <bpt id="p1">**</bpt>Add catalog<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カタログの追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Restart Word.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Add the Microsoft Dynamics App to a document:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics アプリをドキュメントに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>In Word, click <bpt id="p1">**</bpt>Insert<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>My Add-ins<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Shared Folder<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Microsoft Dynamics<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word で、<bpt id="p1">**</bpt>挿入<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アドイン<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>共有フォルダー<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Microsoft Dynamics<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>Click <bpt id="p1">**</bpt>Insert<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>挿入<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>In the app, click <bpt id="p1">**</bpt>Add server information<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリで、<bpt id="p1">**</bpt>サーバー情報の追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>In the <bpt id="p1">**</bpt>Server URL<ept id="p1">**</ept> field, enter the start of the URL (protocol + hostname).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サーバー URL<ept id="p1">**</ept> フィールドに、URL (プロトコル + ホスト名) の開始を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>For example, enter <ph id="ph1">`https://topo00dfa4stbobaos.cloudax.test.dynamics.com`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、「<ph id="ph1">`https://topo00dfa4stbobaos.cloudax.test.dynamics.com`</ph>」を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to apply the settings change and reload the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックして設定を適用し、アプリを再読み込みします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Sign in to the app:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリにログインします:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Click <bpt id="p1">**</bpt>Sign In<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サインイン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>The Azure Active Directory sign-in screen should provide a list of credentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Active Directory サインイン画面には、資格情報の一覧が表示される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>If you encounter an error, force a sign-out (by using the sign-out link in the lower-right corner of the app), and then sign in again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが発生した場合、(アプリケーションの右下隅にあるサインアウト リンクを使用し)、サインアウトを強制し、再度サイン インします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Select the appropriate account, or click <bpt id="p1">**</bpt>Use another account<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なアカウントを選択するか、<bpt id="p1">**</bpt>別のアカウントを使用<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Enter the credentials for that environment, and then click <bpt id="p1">**</bpt>Sign in<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の資格情報を入力し、次に<bpt id="p1">**</bpt>サイン イン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Load the template designer applet:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレート デザイナー アプレットの読み込み:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>After sign-in, click <bpt id="p1">**</bpt>Load applets<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインの後に、<bpt id="p1">**</bpt>アプレットの読み込み<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Select <bpt id="p1">**</bpt>Template Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレート デザイナー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>Click <bpt id="p1">**</bpt>OK.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to confirm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内容を確認して <bpt id="p1">**</bpt>はい<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to close the settings page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして設定ページを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>The latest OData metadata is loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の OData メタデータが読み込まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Follow one of these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順のいずれかを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>Add a fields data source:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド データ ソースの追加:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>In the app, click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリで<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Click <bpt id="p1">**</bpt>Add fields<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールドの追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>Select <bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to go to the field selection page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックしてフィールド選択ページに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>In the document, add a title and/or some blank lines at the top of the document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントで、ドキュメントの上部にタイトルまたはいくつかの空白行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>In the app, in the <bpt id="p1">**</bpt>Available<ept id="p1">**</ept> list, select the <bpt id="p2">**</bpt>FirstName<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリの<bpt id="p1">**</bpt>利用可<ept id="p1">**</ept>の一覧で、<bpt id="p2">**</bpt>FirstName<ept id="p2">**</ept> フィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Click <bpt id="p1">**</bpt>Add label<ept id="p1">**</ept> to add a content control that references the "First name" label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベルの追加<ept id="p1">**</ept>をクリックし、「名」ラベルを参照するコンテンツ コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>In the document, click to put focus into the document, click again to put focus at the end of the label, and then press the Right arrow key until the cursor is outside the content control (the control box will disappear).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントで、ドキュメントをクリックしてフォーカスを配置し、もう一度クリックしてラベルの終わりにフォーカスを配置してから、カーソルがコンテンツ コントロールの外に行く (コントロール ボックスが表示されなくなる) まで右矢印キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Add a separator, such as space+hyphen+space (" - ") or space+colon+space (" : ").</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スペース + ハイフン + スペース (「 - 」) またはスペース + コロン + スペース (「 : 」) などの区切り記号を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>In the app, click <bpt id="p1">**</bpt>Add value<ept id="p1">**</ept> to add a content control that references the <bpt id="p2">**</bpt>FirstName<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリで<bpt id="p1">**</bpt>値の追加<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>FirstName<ept id="p2">**</ept> フィールドを参照するコンテンツ コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Repeat the process for the <bpt id="p1">**</bpt>LastName<ept id="p1">**</ept> field label and value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LastName<ept id="p1">**</ept> フィールドのラベルおよび値に対してプロセスを繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>Continue to add fields as desired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてフィールドを追加し続けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>Add a table data source:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル データ ソースの追加:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>In the app, click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリで<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>Click <bpt id="p1">**</bpt>Add table<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブルの追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Select <bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to go to the field selection page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックしてフィールド選択ページに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>In the document, add a title and/or some blank lines at the top of the document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントで、ドキュメントの上部にタイトルまたはいくつかの空白行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>In the app, in the <bpt id="p1">**</bpt>Available fields<ept id="p1">**</ept> list, add the <bpt id="p2">**</bpt>FirstName<ept id="p2">**</ept>, <bpt id="p3">**</bpt>LastName<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>City<ept id="p4">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリの<bpt id="p1">**</bpt>使用可能なフィールド<ept id="p1">**</ept>の一覧で、<bpt id="p2">**</bpt>FirstName<ept id="p2">**</ept>、<bpt id="p3">**</bpt>LastName<ept id="p3">**</ept>、および <bpt id="p4">**</bpt>City<ept id="p4">**</ept> フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Click <bpt id="p1">**</bpt>Done<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>In Word, save the template document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word で、テンプレート ドキュメントを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>Create a Word template and use it for document generation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word テンプレートを作成し、ドキュメントの生成に使用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>After you've built a Word template, you can upload it to create an Export to Word experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word テンプレートを作成した後は、アップロードし、Word エクスペリエンスにエクスポートを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Upload a template:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテンプレートのアップロード: </target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Navigate to <bpt id="p1">**</bpt>Common<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Common<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office integration<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Document templates<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>共通<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>共通<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Office 統合<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>ドキュメント テンプレート<ept id="p4">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Alternatively, search for the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、ページを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>Click <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>In the dialog box, select a previously created template, and then click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、前に作成したテンプレートを選択してから<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Note that the Root data entity is obtained from the template and appears near the bottom of the dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルート データ エンティティはテンプレートから取得され、ダイアログ ボックスの下部付近に表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Scroll down the list of templates to confirm that the template was added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートが追加されたことを確認するためにテンプレートの一覧を下にスクロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>Optional: If the template should not be filtered to the user's current record, clear the <bpt id="p1">**</bpt>Apply current record filter<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: テンプレートがユーザーの現在のレコードにフィルター処理されない場合、<bpt id="p1">**</bpt>現在のレコード フィルターの適用<ept id="p1">**</ept> チェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>Optional: If the template should not be filtered to the user's current company, clear the <bpt id="p1">**</bpt>Apply company filter<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: テンプレートがユーザーの現在の会社にフィルター処理されない場合、<bpt id="p1">**</bpt>会社フィルターの適用<ept id="p1">**</ept> チェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>Use the uploaded template for document generation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントの生成にはアップロード済みのテンプレートを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>Navigate to a page that shares the same root data source as the template's root data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートのルート データ エンティティと同じルート データ ソースを共有するページに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>For <bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> (<bpt id="p2">**</bpt>FMCustomerEntity<ept id="p2">**</ept>), that page is <bpt id="p3">**</bpt>Fleet Management<ept id="p3">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p4">**</bpt>Customers<ept id="p4">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p5">**</bpt>Customer<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetCustomer<ept id="p1">**</ept> (<bpt id="p2">**</bpt>FMCustomerEntity<ept id="p2">**</ept>) で、そのページは<bpt id="p3">**</bpt>フリート管理<ept id="p3">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p4">**</bpt>顧客<ept id="p4">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p5">**</bpt>顧客<ept id="p5">**</ept>です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Click <bpt id="p1">**</bpt>Open in Microsoft Office<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Export to Word<ept id="p2">**</ept>, and click the template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Office で開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Word にエクスポート<ept id="p2">**</ept>の順に開き、テンプレートをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>Download and open the document that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成されたドキュメントをダウンロードして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>Document Management and SharePoint experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメントの管理と SharePoint の経験</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>Add a SharePoint document type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SharePoint ドキュメント タイプを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>The Document Management subsystem can be used to attach files to records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント管理サブシステムは、レコードにファイルを添付するために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>Most non-executable file types are supported as attachments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの非実行可能ファイルの種類が添付ファイルとしてサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>A document preview is provided for Office document files and PDFs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント プレビューは、Office ドキュメントのファイルおよび PDF に提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>Administrators create document types to indicate where attachments should be stored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は、添付ファイルが保存される場所を示すためにドキュメント タイプを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>When administrators use SharePoint as the storage location, they must provide a specific folder that the files should be put in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者が SharePoint を保管場所として使用するとき、ファイルを配置する特定のフォルダーを提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>Security of that SharePoint folder is a separate administration responsibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その SharePoint フォルダーのセキュリティは、個別の管理責任です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Document management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Document management parameters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ドキュメント管理<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ドキュメント管理パラメーター<ept id="p3">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>Click <bpt id="p1">**</bpt>SharePoint<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細行プロパティの詳細については、<bpt id="p1">**</bpt>SharePoint<ept id="p1">**</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>Make sure that the <bpt id="p1">**</bpt>Default SharePoint server<ept id="p1">**</ept> field is set to a default value for the tenant, such as <bpt id="p2">**</bpt>contosoax7.sharepoint.com<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定の SharePoint サーバー<ept id="p1">**</ept> フィールドが <bpt id="p2">**</bpt>contosoax7.sharepoint.com<ept id="p2">**</ept> などのテナントの既定値に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>Click <bpt id="p1">**</bpt>Test SharePoint connection<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Click <bpt id="p1">**</bpt>SharePoint 接続のテスト<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>Note a successful connection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正常に接続することに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>Navigate to <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Document management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Document types<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ドキュメント管理<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ドキュメント タイプ<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>Set <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> to <bpt id="p2">**</bpt>SharePointDoc<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Type<ept id="p1">**</ept> を <bpt id="p2">**</bpt>SharePointDoc<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>Set <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> to <bpt id="p2">**</bpt>SharePointDoc<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Name<ept id="p1">**</ept> を <bpt id="p2">**</bpt>SharePointDoc<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>Set <bpt id="p1">**</bpt>Location<ept id="p1">**</ept> to <bpt id="p2">**</bpt>SharePoint<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>場所<ept id="p1">**</ept>を <bpt id="p2">**</bpt>SharePoint<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>Click the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> (pencil) button next to the <bpt id="p2">**</bpt>SharePoint Address<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>SharePoint アドレス<ept id="p2">**</ept> フィールドの横にある<bpt id="p1">**</bpt>編集<ept id="p1">**</ept> (鉛筆) ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>On the left side of the dialog box, select a site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスの左側で、サイトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>For the contosoax7 tenant, select <bpt id="p1">**</bpt>ContosoAX Team Site<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">contosoax7 テナントについては、<bpt id="p1">**</bpt>ContosoAX チーム サイト<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>On the right side of the dialog box, select a folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスの右側で、フォルダーを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>For the contosoax7 tenant, select <bpt id="p1">**</bpt>ContosoAX Team Site<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Documents<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>OfficeIntegration<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Attachments<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">contosoax7 テナントについては、<bpt id="p1">**</bpt>ContosoAX チーム サイト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ドキュメント<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>OfficeIntegration<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>添付ファイル<ept id="p4">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>Click the <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> (globe) button next to the <bpt id="p2">**</bpt>SharePoint Address<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>SharePoint アドレス<ept id="p2">**</ept> フィールドの横にある<bpt id="p1">**</bpt>参照<ept id="p1">**</ept> (地球) ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>Note that a new browser tab that shows the selected folder appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したフォルダーを表示する新しいブラウザー タブが表示されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>Use Windows Explorer to create a Word document in the Documents folder, and enter a few words in the document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows エクスプローラーを使用して、ドキュメント フォルダーに Word ドキュメントを作成し、ドキュメントにいくつかの単語を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Customer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>フリート管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>顧客<ept id="p3">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>Put focus on the first customer, and then click the <bpt id="p1">**</bpt>Attach<ept id="p1">**</ept> (paperclip) button in the upper-right corner of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の顧客にフォーカスを配置し、ページの右上隅にある <bpt id="p1">**</bpt>添付<ept id="p1">**</ept> (クリップ) ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>SharePointDoc<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>SharePointDoc<ept id="p2">**</ept> とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>Click <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept>, and select the Word document that you created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照<ept id="p1">**</ept>をクリックし、作成した Word ドキュメントを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>Expand the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> FastTab to see a preview of the Word document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word ドキュメントのプレビューを表示するには、<bpt id="p1">**</bpt>プレビュー<ept id="p1">**</ept> FastTab を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>Expand the <bpt id="p1">**</bpt>Attachment<ept id="p1">**</ept> FastTab to see the file location of the Word document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Word ドキュメントのファイル場所を表示するには、<bpt id="p1">**</bpt>添付ファイル<ept id="p1">**</ept> FastTab を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>In Internet Explorer, use the previously opened tab that shows the SharePoint folder to double-check that the file has been placed appropriately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、以前に開かれたタブを使用し、SharePoint フォルダーを表示して、ファイルが適切に配置されていることを再確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>Email experiences</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メールの経験</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Send mail via a local mail client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル メール クライアント経由で電子メールを送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>Email workflows that are enabled via the SysEmail framework can generate email messages (.eml files) that contain attachments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmail フレームワークで有効になっている電子メール ワークフローでは、添付ファイルを含む電子メール メッセージ (.eml files) を生成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>You can then send these messages via Microsoft Outlook or another email client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメッセージは Microsoft Outlook または他の電子メール クライアント経由で送信することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>All customers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>すべての顧客<ept id="p3">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>Select <bpt id="p1">**</bpt>US-008 Sparrow Retail<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>US-008 Sparrow Retail<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>Click <bpt id="p1">**</bpt>Collect<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customer balances<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Collections<ept id="p3">**</ept> to open the <bpt id="p4">**</bpt>Collections<ept id="p4">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>回収<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客残高<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>コレクション<ept id="p3">**</ept>の順にクリックし、<bpt id="p4">**</bpt>コレクション<ept id="p4">**</ept> ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>Click <bpt id="p1">**</bpt>Communicate<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Email<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Statements to contact<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>連絡<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>電子メール<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>連絡先に対する明細書<ept id="p3">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to accept the default values in the dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで既定値を承諾する場合は、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>If you're prompted for the mail option to use, clear the <bpt id="p1">**</bpt>Do not ask again<ept id="p1">**</ept> check box (you can change this option from the user options page), select <bpt id="p2">**</bpt>Use an email app, such as Outlook<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>OK<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メール オプションの使用を促すメッセージが表示された場合は、<bpt id="p1">**</bpt>再度確認しない<ept id="p1">**</ept> チェックボックス (このオプションはユーザー オプション ページから変更できます) をオフにし、<bpt id="p2">**</bpt>Outlook などの電子メール アプリケーションを使用<ept id="p2">**</ept>を選択し、<bpt id="p3">**</bpt>OK<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>If you're running Internet Explorer on your laptop, open the email (.eml) file that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラップトップ上で Internet Explorer を実行している場合は、生成される電子メール (.eml) ファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>If you're running Internet Explorer on the VM, copy the file to your laptop, and open it there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM 上で Internet Explorer を実行している場合は、ファイルをラップトップにコピーし、そのラップトップでファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>Note the email address in the <bpt id="p1">**</bpt>To<ept id="p1">**</ept> field and the generated workbook attachment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>宛先<ept id="p1">**</ept>フィールドの電子メール アドレスと生成されたブック添付ファイルに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>Send mail via SMTP</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SMTP 経由でメールを送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Email workflows that are enabled via the SysEmail framework can also be created in a simple email dialog box and then sent via Simple Mail Transfer Protocol (SMTP).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmail フレームワークを介して有効になっている電子メール ワークフローは、簡単な電子メール ダイアログ ボックスで作成し、Simple Mail Transfer Protocol (SMTP) 経由で送信することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Email<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Email parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>電子メール<ept id="p3">**</ept>  <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>電子メール パラメータ<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>Click <bpt id="p1">**</bpt>SMTP settings<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SMTP 設定<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Set the <bpt id="p1">**</bpt>Outgoing mail server<ept id="p1">**</ept> to the desired SMTP server:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>送信メール サーバー<ept id="p1">**</ept> を要求された SMTP サーバーに設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>For <bpt id="p1">[</bpt>Office 365 production<ept id="p1">](https://support.office.com/en-us/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c)</ept> (including <ph id="ph1">\*</ph>.onmicrosoft.com accounts): smtp.office365.com (Find this setting via outlook.office.com, at <bpt id="p2">**</bpt>Settings<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Mail<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POP and IMAP<ept id="p4">**</ept>.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「<bpt id="p1">[</bpt>Office 365 製品<ept id="p1">](https://support.office.com/en-us/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c)</ept>」 (<ph id="ph1">\*</ph>.onmicrosoft.com アカウントを含む) の場合: smtp.office365.com (<bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>メール<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POP および IMAP<ept id="p4">**</ept> で outlook.office.com を通してこの設定を検索します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>For Outlook/Hotmail: smtp-mail.outlook.com</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Outlook/Hotmail 用: smtp-mail.outlook.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>Set the user name and password to an appropriate email account and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー名とパスワードを適切な電子メール アカウントとパスワードに設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Leave <bpt id="p1">**</bpt>SSLRequired<ept id="p1">**</ept> turned on, and leave <bpt id="p2">**</bpt>SMTP port number<ept id="p2">**</ept> set to <bpt id="p3">**</bpt>587<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SSLRequired<ept id="p1">**</ept> を有効のままにして、<bpt id="p2">**</bpt>SMTP ポート番号<ept id="p2">**</ept>は <bpt id="p3">**</bpt>587<ept id="p3">**</ept> に設定したままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>In Internet Explorer, navigate to <bpt id="p1">**</bpt>Accounts receivable<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customers<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>All customers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer で、<bpt id="p1">**</bpt>売掛金勘定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>すべての顧客<ept id="p3">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>Select <bpt id="p1">**</bpt>US-008 Sparrow Retail<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>US-008 Sparrow Retail<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>Click <bpt id="p1">**</bpt>Collect<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Customer balances<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Collections<ept id="p3">**</ept> to open the <bpt id="p4">**</bpt>Collections<ept id="p4">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>回収<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>顧客残高<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>コレクション<ept id="p3">**</ept>の順にクリックし、<bpt id="p4">**</bpt>コレクション<ept id="p4">**</ept> ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>Click <bpt id="p1">**</bpt>Communicate<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Email<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Statements to contact<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>連絡<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>電子メール<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>連絡先に対する明細書<ept id="p3">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to accept the default values in the dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで既定値を承諾する場合は、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>If you're prompted for the mail option to use, select <bpt id="p1">**</bpt>Use the Microsoft Dynamics 365 for Finance and Operations email client<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メール オプションを使用するように求められたら、<bpt id="p1">**</bpt>Microsoft Dynamics 365 for Finance and Operations 電子メール クライアントの使用<ept id="p1">**</ept>を選択し、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>To receive the test message, change the To address to your email address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト メッセージを受信するには、宛先アドレスをメール アドレスに変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Enter a subject and body for the message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージの件名および本文を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Click <bpt id="p1">**</bpt>Send<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>送信<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>The message should be delivered in one to five minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージは 1 〜 5 分で配信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Note that the message will appear to be sent from the email account that is set on the <bpt id="p1">**</bpt>Email parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが<bpt id="p1">**</bpt>電子メール パラメーター<ept id="p1">**</ept> ページに設定されている電子メール アカウントから送信されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>If that email account is given "Send As" (or "Send email from this mailbox") permissions for the From address that is used in the <bpt id="p1">**</bpt>Send email<ept id="p1">**</ept> dialog box, messages will appear to come from that address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのメール アカウントに<bpt id="p1">**</bpt>メールの送信<ept id="p1">**</ept>ダイアログ ボックスで使用されている送信元アドレスの「送信者」(または「このメールボックスからメールを送信」) のアクセス許可が与えられている場合、そのアドレスからのメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>You can configure "Send As" permissions in the Office 365 admin center (portal.office.com/Admin), at <bpt id="p1">**</bpt>Users<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Active users<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>User<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Edit mailbox permissions<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Send email from this mailbox<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send As 権限は、Office 365 管理センター (portal.office.com/Admin) にて、<bpt id="p1">**</bpt>ユーザー<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>有効なユーザー<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ユーザー<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>メールボックスのアクセス許可を編集<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>このメールボックスから電子メールを送信する<ept id="p5">**</ept> で構成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>For more information, see <bpt id="p1">[</bpt>Enable sending email from another user's mailbox in Office 365<ept id="p1">](https://support.office.com/en-us/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする<ept id="p1">](https://support.office.com/en-us/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>Before users can send email messages, "Send As" permissions for each user email account in the client must be given to the email account that is set on the <bpt id="p1">**</bpt>Email parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが電子メール メッセージを送信する前に、<bpt id="p1">**</bpt>電子メール パラメーター<ept id="p1">**</ept> ページで設定されている電子メール アカウントにクライアントの各ユーザー電子メール アカウントの 「送信者」権限を与える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>For more information, see <bpt id="p1">[</bpt>How to set up a multifunction device or application to send email using Office 365<ept id="p1">](https://technet.microsoft.com/en-us/library/dn554323(v=exchg.150).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>Office 365 を使用して電子メールを送信するためのマルチ機能デバイスまたはアプリケーションの設定方法<ept id="p1">](https://technet.microsoft.com/en-us/library/dn554323(v=exchg.150).aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>Email that is sent directly from the server, without user interaction, is sent via a batch process and requires that the <bpt id="p1">**</bpt>Email distributor batch<ept id="p1">**</ept> process be started.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの介入なしにサーバーから直接送信される電子メールは、バッチ処理を介して送信され、<bpt id="p1">**</bpt>電子メール ディストリビューター バッチ<ept id="p1">**</ept>プロセスを開始する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>Follow these steps to start the process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスを開始するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>Navigate to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Periodic tasks<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Email processing<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Batch<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>定期処理のタスク<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>電子メールの処理<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>バッチ<ept id="p4">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>Turn on <bpt id="p1">**</bpt>Batch processing<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バッチ処理<ept id="p1">**</ept>をオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source><bpt id="p1">[</bpt>Office integration<ept id="p1">](office-integration.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Office 統合<ept id="p1">](office-integration.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source><bpt id="p1">[</bpt>Office Integration Troubleshooting<ept id="p1">](office-integration-troubleshooting.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Office 統合のトラブルシューティング<ept id="p1">](office-integration-troubleshooting.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>