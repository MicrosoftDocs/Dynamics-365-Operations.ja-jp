<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="form-design-requirements.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>form-design-requirements.4d9194.90ec551775477a92aa5b8535afe88288c1c29231.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>90ec551775477a92aa5b8535afe88288c1c29231</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\form-design-requirements.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Form design requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザインの要件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides in-depth information on designing mobile apps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、モバイル アプリの設計に関する詳細な情報を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Form design requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザインの要件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This section provides valuable guidelines for building Finance and Operations forms that work well with the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、モバイル アプリでうまく機能する Finance and Operations フォームを構築するための貴重なガイドラインを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Each form must have an associated Display Menu Item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各フォームは、表示メニュー項目を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The Display Menu Item's <bpt id="p1">**</bpt>Allow Root Navigation<ept id="p1">**</ept> property must be set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メニュー項目の <bpt id="p1">**</bpt>ルート ナビゲーションを許可する<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This setting enables the mobile framework to open the form that is referenced by the menu item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定により、モバイル フレームワークはメニュー項目によって参照されるフォームを開くことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Each form must be directly accessible via its Display Menu Item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それぞれのフォームは、表示メニュー項目から直接アクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To verify accessibility, open the menu item via a URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクセシビリティを確認するには、URL 経由でメニュー項目を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Just append <bpt id="p1">**</bpt>&amp;mi=<ept id="p1">**</ept> to the URL, where the value is the Application Object Tree (AOT) name of your menu item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値がメニュー項目のアプリケーション オブジェクト ツリー (AOT) の名前である場合、単純に <bpt id="p1">**</bpt>&amp;mi=<ept id="p1">**</ept> を URL に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If the form doesn't open or show data when you access it in this way, the form won't work with the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームにこの方法でアクセスするときに、そのフォームが開かないまたは表示されない場合、モバイル アプリケーションでは動作しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Each form that shows data must have one Master Root Data Source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データが表示する各フォームには、1 つのマスター ルート データ ソースが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This data source must be the first data source on the form (top-most in the designer).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータ ソースは、フォーム上の最初のデータ ソースでなければなりません (デザイナーの最上位)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This data source must not be joined to any other data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータ ソースは、他のデータ ソースに結合してはいけません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Each form must work with the data source filters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各フォームでは、データ ソース フィルターを作業する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>After you open the form in the web client, open the filter pane by using the <bpt id="p1">**</bpt>Show filters<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web クライアントでフォームを開いた後、<bpt id="p1">**</bpt>フィルターの表示<ept id="p1">**</ept>ボタンを使用してフィルター ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Show filters button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルター ボタンを表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Then click <bpt id="p1">**</bpt>Add a filter field<ept id="p1">**</ept>, and verify that the Master Root Data Source appears as the table for fields in the list of available fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後 <bpt id="p1">**</bpt>フィルター フィールドの追加<ept id="p1">**</ept> をクリックして、マスター ルート データ ソースが、使用可能なフィールドの一覧にあるフィールドのテーブルとして表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Other tables can also appear, but the Master Root Data Source <bpt id="p1">**</bpt>must<ept id="p1">**</ept> appear in this list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のテーブルも表示されますが、マスター ルート データ ソースがこの一覧に表示される<bpt id="p1">**</bpt>必要があります<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Otherwise, the mobile app won't enable searches and navigation that uses context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、モバイル アプリケーションは、コンテキストを使用する検索とナビゲーションを有効にしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Searching: The mobile app does online searches against Finance and Operations data by using the Filters framework behind the scenes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索中: モバイル アプリケーションは、バックグラウンドでフィルター フレームワークを使用して Finance and Operations のデータに対してオンライン検索を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Navigation that uses context: The mobile app enables list-to-details navigation (and other context-aware navigation) by first opening the target form via the menu item and then using the Filters framework to show only the specified record context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキストを使用するナビゲーション: モバイル アプリは、最初にメニュー項目からターゲット フォームを開いてから、指定されたレコード コンテキストのみを表示するフィルター フレームワークを使用することで、リストから詳細へのナビゲーション (およびその他のコンテキスト認識ナビゲーション) を可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>List-to-details navigation: The table that the grid is bound to on form A (the list form) must be the Master Root Data Source on the details form (form B).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストと詳細のナビゲーション: グリッドがフォーム A (リスト フォーム) 上にバインドされているテーブルは、詳細フォーム (フォーム B) 上のマスター ルート データ ソースである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When a user selects a record in the list on form A, the mobile framework navigates with record context by applying filters on form B that uniquely identify the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがフォーム A の一覧でレコードを選択すると、モバイル フレームワークは、レコードを一意に識別するフィルターをフォーム B に適用することによって、レコードのコンテキストで移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Design considerations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザインの考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Using data methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ メソッドの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You can use display methods to show data on pages (both list type pages and detail type pages).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メソッドを使用してページ (リスト タイプ ページおよび詳細タイプ ページの両方) 上にデータを表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>However, there are two key points to remember when you use display methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、表示メソッドを使用する場合、覚えておくべき 2 つのキー ポイントがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Searching<ept id="p1">**</ept> – When a user performs an “online” search (that is, a search that is run against data in Finance and Operations instead of locally cached data), the search won't match against display methods, because the Filtering framework in Finance and Operations doesn't support searches against data methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>検索中<ept id="p1">**</ept> – ユーザーが「オンライン」の検索 (つまり、ローカルにキャッシュされたデータの代わりに、Finance and Operations のデータに対して実行される検索) をする時、Finance and Operations におけるフィルタリング フレームワークは、データ メソッドに対する検索をサポートしていないため、検索は表示方法と一致しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>However, when a user does a search against locally cached data, the search will match against display methods, provided that the records have been cached on the device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ユーザーがローカルにキャッシュされたデータに対する検索を実行すると、レコードがデバイスにキャッシュされた場合、検索は表示方法と一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Offline<ept id="p1">**</ept> – If a user creates or updates data while his or her device isn’t connected to the Finance and Operations server, temporary records are created in the local cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オフライン<ept id="p1">**</ept> – デバイスが Finance and Operations サーバーに接続されていない状態で、ユーザーがデータを作成または更新すると、一時レコードがローカル キャッシュに作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Because these temporary records haven't yet been processed in Finance and Operations, if the records have any fields that are automatically populated or defaults by server-side business logic, these fields will remain empty until the records have been synced with Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの一時レコードは Finance and Operations でまだ処理されていないため、レコードに自動的に入力されるフィールドやサーバー側のビジネス ロジックによる既定のフィールドがある場合、これらのフィールドはレコードが Finance and Operations と同期されるまで空白です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Display methods fall into this category of fields that will be empty for a temporary record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メソッドは、一時的なレコードのために空になるフィールドのカテゴリに分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Designing for offline</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン用のデザイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Unlike the Finance and Operations web client, which is highly connected to the Finance and Operations server and maintains an open user session that has open forms on the server, the mobile app creates user sessions (and opens forms) only in short bursts while the app is being synced with the server (via data read for pages, or via data write/update for actions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations サーバーに密に接続され、サーバー上にオープン フォームを有するオープン ユーザー セッションを維持する Finance and Operations の Web クライアントとは異なり、モバイル アプリは短いバーストでのみユーザー セッションを生成する (およびフォームを開く)と同時に、サーバーと同期化します (ページの場合はデータの読み込み、アクションの場合はデータの書込み/更新による)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>If there are no actions to sync with the server, and if the local data cache is up to date, the mobile app won't communicate with the Finance and Operations server as a user navigates around the app (unless the user triggers an explicit pull-to-refresh).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバーと同期するアクションがなく、ローカル データ キャッシュが最新の場合、ユーザーが明示的にプルをトリガーしない限り、モバイル アプリは、ユーザーがアプリをナビゲートする際に、(ユーザーが明示的にプルして更新しない限り) Finance and Operations サーバーと通信しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>It's important that you keep this data flow pattern in mind while you design pages and actions in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリのページとアクションの設計中に、このデータ フロー パターンに注意することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>You should not expect Finance and Operations form logic to run every time that a page is loaded or an action is started.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページが読み込まれるか、アクションが起動するたびに Finance and Operations フォームのロジックが実行されるとは限りません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You should also never expect form logic to run while a user is completing an action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがアクションを実行している間にフォーム ロジックが実行されることを想定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Form logic is run only when the action is being synced with the Finance and Operations server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム ロジックは、アクションが Finance and Operations サーバーと同期されている場合にのみ実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The following list describes the only times when you should expect Form logic to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のリストは、フォーム ロジックの実行にかかる時間のみを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>Finance and Operations form logic runs right before a page is opened on the mobile app for the first time.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Finance and Operations フォーム ロジックは、ページがモバイルアプリで初めて開かれる直前に実行されます。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>When a user first opens a page, the mobile app reaches out to Finance and Operations and opens the associated forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがまずページを開くと、モバイル アプリが Finance and Operations と連絡を取って、関連付けられているフォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">*</bpt>During this process, logic such as form init and data source init is all run in the usual manner.<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>このプロセス中、フォーム初期化およびデータ ソースの初期化などのロジックはすべて通常通りに実行されます。<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The mobile app framework reads the required data directly from the controls on the forms and sends the data back to the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリ フレームワークは、フォームのコントロールから必要なデータを直接読み込み、データをモバイル アプリに送り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The mobile app caches the data and shows it in the page on the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリはデータをキャッシュし、モバイル アプリのページに表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Future attempts to open the page will load the cached data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページを開くための更なる試行は、キャッシュされたデータに読み込まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">*</bpt>These attempts won't run the form logic again, unless the user explicitly refreshes the page or the cache expires. (Currently, the cache set to expire after 30 minutes.)<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>これらの試行は、ユーザーがページを明示的にリフレッシュするか、キャッシュの有効期限が切れない限りフォーム ロジックを再度実行しません。(現在、キャッシュは 30 分後に期限切れになるように設定されています。)<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Processing an action that has been submitted to the server from the mobile app<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モバイル アプリからサーバーに送信されたアクションの処理<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>When a user opens an action and fills in the data in that action, <bpt id="p1">*</bpt>no form logic is run<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがアクションを開いて、そのアクションにデータを入力するとき、<bpt id="p1">*</bpt>どのフォーム ロジックも実行されません<ept id="p1">*</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A user can complete an action while he or she is either offline or online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、オンラインまたはオフラインのいずれかでアクションを完了できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The system behaves the same way in both cases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どちらの場合も、システムは同じように動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>After the user clicks <bpt id="p1">**</bpt>Done<ept id="p1">**</ept><ph id="ph1">/</ph><bpt id="p2">**</bpt>Save<ept id="p2">**</ept> on the action, the mobile app queues a data synchronization operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがアクションの<bpt id="p1">**</bpt>完了<ept id="p1">**</ept><ph id="ph1">/</ph><bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックすると、モバイル アプリはデータ同期操作をキューにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This operation will be synced with the server when the mobile app is connected to the Internet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作は、モバイル アプリがインターネットに接続されているときにサーバーと同期されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When an Internet connection is detected (which can happen immediately after the action is completed) the mobile app sends the data synchronization operation to the Finance and Operations server for processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット接続 (そのアクションの直後に発生することもあります) が検出されると、モバイル アプリは、処理用の Finance and Operations サーバーにデータ同期操作を送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>While the operation is processed on the server, the framework opens the associated forms and enters the data from the action by passing values into the form controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー上でオペレーションが処理される間、フレームワークにより関連フォームが開かれ、フォーム コントロールに値を渡すことによりアクションからのデータが入力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">*</bpt>During this process, Finance and Operations form logic is run in the usual manner (init, modified, clicked, and so on, are all run).<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>このプロセス中、Finance and Operations フォーム ロジックは通常の方法（init、変更、クリックなどはすべて実行）で実行されます。<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>However, the mobile user might have moved to a different part of the app while this processing is occurring.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この処理が行われている間、モバイル ユーザーがアプリの別の部分に移動した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">*</bpt>Any form logic that shows/hides controls will have no effect on the UI that is seen in the mobile app.<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>コントロールを表示 / 非表示するどのフォーム ロジックも、モバイルアプリに表示される UI は無効になります。<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Therefore, to minimize synchronization times, it's best not to include any UI logic on the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、同期時間を最小限に抑えるために、UI ロジックをフォームに含めないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Building mobile versions of existing forms</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のフォームのモバイル バージョンの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>If you decide to modify existing forms so that they work with the mobile framework, instead of building new mobile-specific forms, you might have to conditionally change the form's behavior for mobile-specific scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいモバイル固有フォームを作成するのではなく、モバイル フレームワークと連携できるように、既存のフォームを変更する場合は、条件付きでモバイル固有のシナリオのフォームの動作を変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>You can use the following static X++ application programming interfaces (APIs) in your X++ code to determine whether the code is being accessed during a session where a web client user is designing pages/actions or during a session that the mobile framework back end created to load pages/actions for a mobile user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web クライアント ユーザーがページ/アクションをデザインするセッション中、またはモバイル ユーザーのページ/アクションを読み込むためにモバイル フレームワーク バック エンドが作成したセッション中に、コードにアクセスしているかどうかを決定するために X++ コードでは次の静的 X++ アプリケーション プログラミング インターフェイス (API) を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>When a form is being used with the mobile designer<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モバイル デザイナーで、フォームが使用されている場合<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>When a form is being used by the mobile framework back end to load pages and run actions<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モバイル フレームワークによりバックエンドからページをロードしてアクションを実行するフォームを使用している場合<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Finance and Operations form control support</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のフォーム コントロール サポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The Finance and Operations form controls for the various base data types (strings, dates, and numbers) and grids are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各種の基本データ型 (文字列、日付、および番号) とグリッドの Finance and Operations がサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>However, a few common controls have limited support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、いくつかの一般的なコントロールのサポートは限定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Reference groups<ept id="p1">**</ept> Fields from within Reference groups controls are compatible when you design pages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照グループ<ept id="p1">**</ept> 参照グループ コントロール内のフィールドは、ページをデザインするときに互換性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>However, they aren't compatible when you design Actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、アクションをデザインする際に互換性がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Although you might be able to select these fields without experience any issue, Reference groups have a fundamental incompatibility with the mobile framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの問題を経験せずにこれらのフィールドを選択することができるかもしれませんが、参照グループはモバイル フレームワークと基本的に互換性がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>We recommend that you not use Reference groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照グループを使用しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Instead, add a control directly to the form, and then bind the control directly to the surrogate foreign key (SFK) by using the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、フォームに直接コントロールを追加してから、プロパティ シートを使用して代理外部キー (SFK) に直接コントロールをバインドします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>