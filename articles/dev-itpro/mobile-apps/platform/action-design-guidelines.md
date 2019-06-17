<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="action-design-guidelines.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>action-design-guidelines.9e179c.f730acbd259cb588f051809c38c913cdf91ff51d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f730acbd259cb588f051809c38c913cdf91ff51d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\action-design-guidelines.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Action design guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション デザインのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides in-depth information on designing mobile apps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、モバイル アプリの設計に関する詳細な情報を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Action design guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション デザインのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Actions let users create, update, or delete data, and also run business processes on that data (such as <bpt id="p1">*</bpt>submit<ept id="p1">*</ept>, <bpt id="p2">*</bpt>confirm<ept id="p2">*</ept>, and <bpt id="p3">*</bpt>post<ept id="p3">*</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションでユーザーはデータの作成、更新、または削除を行うことができ、そのデータ (<bpt id="p1">*</bpt>送信<ept id="p1">*</ept>、<bpt id="p2">*</bpt>確認<ept id="p2">*</ept>、および<bpt id="p3">*</bpt>転記<ept id="p3">*</ept>など) で業務プロセスを実行することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>A user who completes an action first supplies the data for the action (if the action accepts data input).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを完了したユーザーは、アクションのデータを最初に提供します (アクションがデータ入力を受け入れる場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the user has finished supplying the data, the action is put into a queue of similar actions (which are sometimes referred to as <bpt id="p1">*</bpt>data sync operations<ept id="p1">*</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがデータの提供を完了すると、アクションは同様のアクションのキューに配置されます (これは <bpt id="p1">*</bpt>データ同期操作<ept id="p1">*</ept> と呼ばれることもあります)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If the device is connected/online, the queue is processed immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスが接続されているまたはオンラインである場合は、キューがすぐに処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Otherwise, it's processed the next time that the device is connected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、次回デバイスが接続されたときに処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The queue is processed asynchronously and doesn’t require the user’s attention unless there is an error during data synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キューは非同期で処理され、データ同期中にエラーが発生しない限り、ユーザーの注意を必要としません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Errors of this type can occur because of server-side data validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプのエラーは、サーバー側のデータ入力規則が原因で発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Actions are powered by a server-side mechanism that resembles Task recordings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションは、タスク記録に似たサーバー側メカニズムによって強化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This mechanism extracts the user’s input from the action and then automatically runs the business process steps on the server by using the input values that the user supplied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメカニズムはアクションからユーザーの入力を抽出し、ユーザーが入力した入力値を使用してビジネス プロセス ステップをサーバー上で自動的に実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The mechanism automatically opens forms, clicks buttons on the forms, and enters the user's input into controls on the forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仕組みは、自動的にフォームを開き、フォーム上のボタンをクリックし、ユーザーの入力をフォームのコントロールに入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This process of playing back the action against the forms on the server occurs asynchronously, against “headless” forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー上のフォームに対してアクションを再生するこのプロセスは、「ヘッドレス」フォームとは非同期で行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The mobile app informs the user when the process is completed, and shows the user any info, warning, or error messages that the forms logged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリは、プロセスが完了するとユーザーに通知し、フォームに記録された情報、警告、またはエラー メッセージをユーザーに表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>When you design an action, it’s important that you first consider what entity the action is related to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションをデザインするときは、アクションがどのようなエンティティに関連付けられているかを最初に検討することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the current framework, an action must operate on only one entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のフレームワークでは、アクションでエンティティを 1 つだけ操作する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>An action should not update multiple entities at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションは同時に複数のエンティティを更新するべきではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, an action to create a new sales order should create only the header for the order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、新しい販売注文を作成するアクションは、注文のヘッダーのみを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>It should not also try to create lines, because the lines are separate entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細行は別々のエンティティであるため、明細行を作成しないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>When you decide to design the action, consider the following questions to determine how to proceed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを設計することを決定したときは、以下の質問を検討して、展開の方法を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>How do I design an action that enables an entity to be created?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティが作成されるようにするアクションをどのように設計しますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Identify or create a list view page for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのリスト ビュー ページを識別または作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Make sure that the form that is used for the list view page includes a <bpt id="p1">**</bpt>New<ept id="p1">**</ept> button that can be used to add new records to the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リスト ビュー ページに使用されるフォームに、新しいレコードをリストに追加するために使用できる<bpt id="p1">**</bpt>新規<ept id="p1">**</ept>ボタンが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Use the designer to create a new action for the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーを使用して、ページに新しいアクションを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>While you're designing the action, be careful not to perform any unnecessary actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを作成するときは、不要なアクションを実行しないように注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Enter data only in those fields that should be available to the user, and click only those buttons that are required (for example the <bpt id="p1">**</bpt>New<ept id="p1">**</ept> button and the <bpt id="p2">**</bpt>Save<ept id="p2">**</ept> button).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが使用できるフィールドにのみデータを入力し、必要なボタンだけをクリックします (たとえば、<bpt id="p1">**</bpt>新規<ept id="p1">**</ept>ボタンおよび<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>ボタン)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>How do I design an action that enables an entity to be edited?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティが編集されるようにするアクションをどのように設計しますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Identify or create a details view page for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの詳細ビュー ページを識別または作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Make sure that the form that is used for the details view page includes an <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> button that can be used to edit the visible record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビュー ページに使用されるフォームに、表示されているレコードを編集するために使用できる<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>ボタンが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Make sure that the form that is used for the details view page lets users open a specific record by applying filters in the filter pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビュー ページに使用されるフォームから、ユーザーがフィルター ウィンドウにフィルターを適用することで特定のレコードを開けることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Use the designer to create a new action for the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーを使用して、ページに新しいアクションを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>While you're designing the action, be careful not to perform any unnecessary actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを作成するときは、不要なアクションを実行しないように注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Enter data only in those fields that should be available to the user, and click only those buttons that are required (for example, the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> button and the <bpt id="p2">**</bpt>Save<ept id="p2">**</ept> button).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが使用できるフィールドにのみデータを入力し、必要なボタンだけをクリックします (たとえば、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>ボタンおよび<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>ボタン)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>How do I design an action that enables an entity to be deleted?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティが削除されるようにするアクションをどのように設計しますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Identify or create a details view page for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの詳細ビュー ページを識別または作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Make sure that the form that is used for the details view page includes a <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept> button that can be used to delete the visible record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビュー ページに使用されるフォームに、表示されているレコードを削除するために使用できる<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>ボタンが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Make sure that the form that is used for the details view page lets users open a specific record by applying filters in the filter pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビュー ページに使用されるフォームから、ユーザーがフィルター ウィンドウにフィルターを適用することで特定のレコードを開けることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Use the designer to create a new action for the page, and just click <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept> as a part of the process of designing the action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーを使用してページの新しいアクションを作成し、アクションの設計プロセスの一部として <bpt id="p1">**</bpt>削除<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>How do I design an action that enables a business action to be performed on an entity?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティで実行される事業活動を有効にするアクションをどのように設計しますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Identify or create a details view page for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの詳細ビュー ページを識別または作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Make sure that the form that is used for the details view page includes a <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept> button that can be used to delete the visible record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビュー ページに使用されるフォームに、表示されているレコードを削除するために使用できる<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>ボタンが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Make sure that the form that is used for the details view page lets users open a specific record by applying filters in the filter pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビュー ページに使用されるフォームから、ユーザーがフィルター ウィンドウにフィルターを適用することで特定のレコードを開けることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Use the designer to create a new action for the page, and just perform the steps that are required in the business action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーを使用してページの新しいアクションを作成し、ビジネス アクションに必要な手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You don't necessarily have to enter data in fields as part of the action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションの一部として、必ずしもフィールドにデータを入力する必要があるわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For an action such as <bpt id="p1">*</bpt>submit<ept id="p1">*</ept>, you just have to click the <bpt id="p2">**</bpt>Submit<ept id="p2">**</ept> button (and acknowledge any confirmations that appear).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>送信<ept id="p1">*</ept>などのアクションについては、単に<bpt id="p2">**</bpt>送信<ept id="p2">**</ept>ボタン (および任意の確認書が表示されることを確認します) をクリックする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>How do I design an action that enables a field value to be set via a rich lookup?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">豊富なルックアップを介して設定するフィールド値を有効にするアクションをどのように設計しますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Lookups for fields in the mobile app don't have a correlation to the advanced lookup behaviors in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリでのフィールドのルックアップには、Finance and Operations の高度なルックアップ動作との相関関係はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Regardless of whether you have a custom lookup in Finance and Operations or an automatic lookup that uses a simple query, the mobile app doesn't run existing lookup code when it must determine which UI to show the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations にカスタム ルックアップがあるのか、単純なクエリを使用する自動ルックアップがあるのかに関係なく、モバイル アプリはユーザーに表示される UI を決定する必要があるときに既存のルックアップ コードを実行しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>(Remember that the user might be offline while he or she is using the app, and server-side code isn’t run until the action is synchronized.) However, lookup/control overrides such as <bpt id="p1">*</bpt>modified<ept id="p1">*</ept> are run when the value is set by the mobile back end as it synchronizes the data from the action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ユーザーがアプリケーションを使用している間はオフラインになっている可能性があり、アクションが同期されるまでサーバー側のコードは実行されないことに注意してください。) ただし、アクションからのデータを同期させるので、値がモバイル バック エンドによって設定される場合、<bpt id="p1">*</bpt>変更<ept id="p1">*</ept>などのルックアップ/コントロールの上書きは実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>When the mobile app detects that a field on an action was selected from a lookup field on a form, it shows a device-native combo box/list picker control, and populates the items by directly querying the backing table of that lookup field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル アプリは、アクションのフィールドがフォームのルックアップ フィールドから選択されたことを検出すると、デバイス ネイティブ コンボ ボックス / リスト選択コントロールを表示して、そのルックアップ フィールドのサポート テーブルを直接照会して項目を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The items in the list show the user data from the TitleField for records in that table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リスト内の項目は、そのテーブルのレコードの TitleField のユーザー データを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Follow these steps to add the rich lookup experience to your action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションに豊富なルックアップ エクスペリエンスを追加するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This lookup experience includes a full-page multi-column lookup selector that has offline search.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルックアップ エクスペリエンスには、フルページの複数列のルックアップ セレクターがあり、オフライン検索が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Identify or create a list view page for the entity behind the lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップの背後にあるエンティティの詳細ビュー ページを識別または作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>You can reuse existing list view pages that you've already created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に作成済みの既存のリスト ビュー ページを再利用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>After you've finished designing the action, select the field to add rich lookup functionality to, and then click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションのデザインが終了した後、フィールドを選択して豊富なルックアップ機能を追加し、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Control properties<ept id="p1">**</ept> dialog box, select the list view page that you identified or created in step 1, and set the other related properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロールのプロパティ<ept id="p1">**</ept> ダイアログ ボックスで、手順 1 で指定または作成したリスト ビュー ページを選択し、その他の関連するプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Setting the control properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール プロパティの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Save and publish your changes to the action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションに変更内容を保存して公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>If you don't see the property for the existing list view page or can't access the <bpt id="p1">**</bpt>Control properties<ept id="p1">**</ept> dialog box when you're designing your action, you might be using an older build of Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のリスト ビュー ページのプロパティが表示されていない、または<bpt id="p1">**</bpt>コントロールのプロパティ<ept id="p1">**</ept> ダイアログ ボックスにアクセスできない場合、Finance and Operations のより古いビルドを使用している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>In this case, you can still add rich lookup functionality by using a business logic file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、ビジネス ロジック ファイルを使用して、豊富なルックアップ機能を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>How do I prevent an action from appearing in the list of actions for a page?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを、ページのアクションの一覧に表示されないようにするにはどうすればよいですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To prevent an action from appearing in the list of actions for any page, call the following code from the <bpt id="p1">**</bpt>appInit()<ept id="p1">**</ept> section of your business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページのアクション一覧にアクションが表示されないようにするには、ビジネス ロジックの <bpt id="p1">**</bpt>appInit()<ept id="p1">**</ept> セクションから次のコードを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In this code, <bpt id="p1">**</bpt>action-name<ept id="p1">**</ept> is the name of your action (as specified in the <bpt id="p2">**</bpt>Action name<ept id="p2">**</ept> field in the designer).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードでは、<bpt id="p1">**</bpt>アクション名<ept id="p1">**</ept>はアクションの名前です (デザイナーの<bpt id="p2">**</bpt>アクション名<ept id="p2">**</ept>フィールドで指定したとおり)。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>