<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="view-model-ipage.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>view-model-ipage.67b979.62aef0d08536df4b966e6e0c43c981d930d5d78e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>62aef0d08536df4b966e6e0c43c981d930d5d78e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\client-apis\modules\view-model-ipage.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Page module</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ モジュール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>The IPage interface encapsulates the various properties, life cycle and event hooks associated with a page in a workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPage インターフェイスは、さまざまなプロパティ、ライフ サイクル、およびワークスペース内のページに関連付けられているイベント フックをカプセル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Page module</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ モジュール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The IPage interface encapsulates the various properties, life cycle and event hooks associated with a page in a workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPage インターフェイスは、さまざまなプロパティ、ライフ サイクル、およびワークスペース内のページに関連付けられているイベント フックをカプセル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Page data Synchronization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ データ同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Pages that can submit changes (also referred to as actions) go through various stages before they're completely in sync with the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を送信できるページ (アクションとも呼ばれる) は、サーバーと完全に同期される前にさまざまなステージを通過します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>As soon as a page is <bpt id="p1">[</bpt>submitted<ept id="p1">](../interfaces/view-model-ipage-ipage.md#submit)</ept>, there are three possible consequences:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページが <bpt id="p1">[</bpt>送信<ept id="p1">](../interfaces/view-model-ipage-ipage.md#submit)</ept> されるとすぐに、起こり得る結果が 3 つあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>It fails client-side validation: The client logic might prevent the page from being submitted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント側の検証に失敗する場合: クライアント ロジックによってページを送信できない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The client is online: The submission is processed as soon as the application-wide sync queue is cleared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントはオンラインです。アプリケーション全体の同期キューがクリアされるとすぐに、送信が処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The client is offline: The submission is added to the application-wide sync queue and stays there as long as the client is offline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントはオフラインです。送信はアプリケーション全体の同期キューに追加され、クライアントがオフラインである限り、そこにとどまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>While a submission is waiting to be synchronized, it can be in one of these states:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信の同期の待機中は、以下のいずれかの状態にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Pending: The submission is still pending and can still be edited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保留中: 送信が保留中ですが、編集することはできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Processing: The submission is currently being synchronized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処理: 送信は現在同期中です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In this state, any further edits are not allowed on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この状態では、ページをこれ以上編集できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>After a submission goes through to the server, it can be in one of these states:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信がサーバーに送られた後、次のいずれかの状態になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Synchronized: The submission is accepted by the server and is synchronized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同期済み: 送信はサーバーに受け入れられて同期されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Error: The server rejects the submission and the page enters an error state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: サーバーは、送信を拒否およびページがエラー状態を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Multiple pending submissions for a given page and context might be clubbed (and sent) together if the page is deemed to be idempotent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のページおよびコンテキストにおいて保留中の送信が複数あり、ページが冪等であるとみなされる場合、集められる (かつ送信される) 場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This implies that the server need not process all submissions in any order and depends on the design of the page on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、サーバーがすべての送信をさまざまな順序で処理する必要はなく、サーバー上のページの設計に依存することを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Index</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Enumerations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">[</bpt>PageState<ept id="p1">](../enums/view-model-ipage-pagestate.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageState<ept id="p1">](../enums/view-model-ipage-pagestate.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">[</bpt>CompleteEventArgs<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>CompleteEventArgs<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt>NavigationArgs<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>NavigationArgs<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Page<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ページ<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt>PageMetadata<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageMetadata<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt>PageOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">[</bpt>PageSubmitArgs<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageSubmitArgs<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Enumerations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>PageState</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageState</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Enumeration members</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型メンバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt>error<ept id="p1">](../enums/view-model-ipage-pagestate.md#error)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>エラー<ept id="p1">](../enums/view-model-ipage-pagestate.md#error)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>error:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>10</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The page is currently in the error state, but can be refreshed in an attempt to get out of this state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページは現在、エラー状態にありますが、更新することでこの状態から抜け出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">[</bpt>loaded<ept id="p1">](../enums/view-model-ipage-pagestate.md#loaded)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>読み込み済み<ept id="p1">](../enums/view-model-ipage-pagestate.md#loaded)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>loaded:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">loaded:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The page is fully loaded and can be refreshed and, if possible, submitted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページが完全に読み込まれ、更新可能であり、可能ならば送信できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">[</bpt>loading<ept id="p1">](../enums/view-model-ipage-pagestate.md#loading)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>読み込み中<ept id="p1">](../enums/view-model-ipage-pagestate.md#loading)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>loading:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">loading:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The page is currently being loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページが現在読み込まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">[</bpt>offline<ept id="p1">](../enums/view-model-ipage-pagestate.md#offline)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>オフライン<ept id="p1">](../enums/view-model-ipage-pagestate.md#offline)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>offline:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">offline:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The page was loaded in the offline mode, thus not refreshable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページはオフライン モードで読み込まれたので更新できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">[</bpt>refreshing<ept id="p1">](../enums/view-model-ipage-pagestate.md#refreshing)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>更新中<ept id="p1">](../enums/view-model-ipage-pagestate.md#refreshing)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>refreshing:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新中:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The page is currently refreshing its data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページは現在データを更新中です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>CompleteEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CompleteEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>CompleteEventArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CompleteEventArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">[</bpt>error<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md#error)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>エラー<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md#error)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>error: boolean (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー: boolean (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt>navigation<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md#navigation)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ナビゲーション<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md#navigation)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>navigation: <bpt id="p1">[</bpt>NavigationArgs<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">navigation: <bpt id="p1">[</bpt>NavigationArgs<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md)</ept> (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">[</bpt>processed<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md#processed)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>処理済<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md#processed)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>processed: boolean (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">processed: boolean (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Design</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Design</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>PageLinkDesign<ept id="p1">](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>PageLinkDesign<ept id="p1">](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>ContainerControlDesign<ept id="p1">](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>ContainerControlDesign<ept id="p1">](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>InputControlDesign<ept id="p1">](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>InputControlDesign<ept id="p1">](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>ImageDesign<ept id="p1">](../interfaces/view-model-control-image-iimage-iimagedesign.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>ImageDesign<ept id="p1">](../interfaces/view-model-control-image-iimage-iimagedesign.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">[</bpt>alignItems<ept id="p1">](../interfaces/view-model-ipage-idesign.md#alignitems)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>alignItems<ept id="p1">](../interfaces/view-model-ipage-idesign.md#alignitems)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>alignItems: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">alignItems: string (optional)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>This property is an alias for the CSS property "align-items".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、CSS プロパティ「align-items」のエイリアスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">[</bpt>alignSelf<ept id="p1">](../interfaces/view-model-ipage-idesign.md#alignself)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>alignSelf<ept id="p1">](../interfaces/view-model-ipage-idesign.md#alignself)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>alignSelf: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">alignSelf: string (optional)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">[</bpt>bindings<ept id="p1">](../interfaces/view-model-ipage-idesign.md#bindings)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>バインディング<ept id="p1">](../interfaces/view-model-ipage-idesign.md#bindings)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>bindings: any (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bindings: any (optional)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">[</bpt>border<ept id="p1">](../interfaces/view-model-ipage-idesign.md#border)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>枠線<ept id="p1">](../interfaces/view-model-ipage-idesign.md#border)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>border: "none" &amp;#124; "solid" &amp;#124; "left" &amp;#124; "right" &amp;#124; "top" &amp;#124; "bottom" (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">border: "none" &amp;#124; "solid" &amp;#124; "left" &amp;#124; "right" &amp;#124; "top" &amp;#124; "bottom" (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The border behavior of a control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの境界動作。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>This property will not be inherited by the children.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、子によって継承されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><bpt id="p1">[</bpt>color<ept id="p1">](../interfaces/view-model-ipage-idesign.md#color)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>色<ept id="p1">](../interfaces/view-model-ipage-idesign.md#color)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>color: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">color: string (optional)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>The foreground color of the container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーの前景色。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">[</bpt>flexFlow<ept id="p1">](../interfaces/view-model-ipage-idesign.md#flexflow)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>flexFlow<ept id="p1">](../interfaces/view-model-ipage-idesign.md#flexflow)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>flexFlow: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">flexFlow: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Specifying this property makes the component a flex container component.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt>flexSize<ept id="p1">](../interfaces/view-model-ipage-idesign.md#flexsize)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>flexSize<ept id="p1">](../interfaces/view-model-ipage-idesign.md#flexsize)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>flexSize: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">flexSize: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>One number or two numbers written as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの番号または 2 つの番号が文字列として書き込まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>E.g.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">E.g.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>"(size to grow) [(size-to-shrink)]" to accommodate available space in the immediate flex container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt>fontSize<ept id="p1">](../interfaces/view-model-ipage-idesign.md#fontsize)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>fontSize<ept id="p1">](../interfaces/view-model-ipage-idesign.md#fontsize)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>fontSize: "medium" &amp;#124; "xx-small" &amp;#124; "x-small" &amp;#124; "small" &amp;#124; "large" &amp;#124; "x-large" &amp;#124; "xx-large" (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fontSize: "medium" &amp;#124; "xx-small" &amp;#124; "x-small" &amp;#124; "small" &amp;#124; "large" &amp;#124; "x-large" &amp;#124; "xx-large" (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The proportional text size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">比例テキスト サイズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">[</bpt>fontWeight<ept id="p1">](../interfaces/view-model-ipage-idesign.md#fontweight)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>fontWeight<ept id="p1">](../interfaces/view-model-ipage-idesign.md#fontweight)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>fontWeight: "normal" &amp;#124; "bold" (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fontWeight: "normal" &amp;#124; "bold" (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Normal or bold text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準または太字のテキスト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">[</bpt>justifyItems<ept id="p1">](../interfaces/view-model-ipage-idesign.md#justifyitems)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>justifyItems<ept id="p1">](../interfaces/view-model-ipage-idesign.md#justifyitems)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>justifyItems: "flex-start" &amp;#124; "flex-end" &amp;#124; "center" &amp;#124; "space-between" (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">justifyItems: "flex-start" &amp;#124; "flex-end" &amp;#124; "center" &amp;#124; "space-between" (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>This property is an alias for the CSS property "justify-content".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは CSS プロパティ「justify-content」のエイリアスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source><bpt id="p1">[</bpt>label<ept id="p1">](../interfaces/view-model-ipage-idesign.md#label)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ラベル<ept id="p1">](../interfaces/view-model-ipage-idesign.md#label)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>label: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">label: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">[</bpt>labelPosition<ept id="p1">](../interfaces/view-model-ipage-idesign.md#labelposition)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>labelPosition<ept id="p1">](../interfaces/view-model-ipage-idesign.md#labelposition)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>labelPosition: "stacked" &amp;#124; "hidden" &amp;#124; "inline" (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">labelPosition: "stacked" &amp;#124; "hidden" &amp;#124; "inline" (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Determines how a label is positioned, if at all.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルの配置方法を決定します (行われる場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>By default, labelPosition is set to stacked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、labelPosition が stacked に設定されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">[</bpt>name<ept id="p1">](../interfaces/view-model-ipage-idesign.md#name)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>名前<ept id="p1">](../interfaces/view-model-ipage-idesign.md#name)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>name: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">name: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">[</bpt>padding<ept id="p1">](../interfaces/view-model-ipage-idesign.md#padding)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>スペース<ept id="p1">](../interfaces/view-model-ipage-idesign.md#padding)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>padding: "none" &amp;#124; "small" &amp;#124; "std" (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">padding: "none" &amp;#124; "small" &amp;#124; "std" (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Allows specifying the component's padding behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントのスペース動作を指定できるように許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><bpt id="p1">[</bpt>type<ept id="p1">](../interfaces/view-model-ipage-idesign.md#type)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>タイプ<ept id="p1">](../interfaces/view-model-ipage-idesign.md#type)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>type: <bpt id="p1">[</bpt>ControlType<ept id="p1">](view-model-control-basecontrol-icontrol.md#controltype)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">type: <bpt id="p1">[</bpt>ControlType<ept id="p1">](view-model-control-basecontrol-icontrol.md#controltype)</ept> (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The type of the control as a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列としてのコントロールのタイプ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>NavigationArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NavigationArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ NavigationArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ NavigationArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">[</bpt>label<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#label)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ラベル<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#label)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>label: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">label: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><bpt id="p1">[</bpt>options<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#options)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>オプション<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#options)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>options: any (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">options: any (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source><bpt id="p1">[</bpt>params<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#params)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>パラメーター<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#params)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>params: <bpt id="p1">[</bpt>PageOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">params: <bpt id="p1">[</bpt>PageOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md)</ept> (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Inherited from <bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept>.<bpt id="p2">[</bpt>params<ept id="p2">](../interfaces/view-model-ipage-ipagetarget.md#params)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept>.<bpt id="p2">[</bpt>params<ept id="p2">](../interfaces/view-model-ipage-ipagetarget.md#params)</ept> から継承</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source><bpt id="p1">[</bpt>replace<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#replace)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>置換<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#replace)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>replace: boolean (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">replace: boolean (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>If set to true, removes current view firing navigation from navigation history stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">true と設定されている場合は、ナビゲーション履歴スタックから現在のビューの起動ナビゲーションを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><bpt id="p1">[</bpt>to<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#to)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>to<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#to)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>to: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">to: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Inherited from <bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept>.<bpt id="p2">[</bpt>to<ept id="p2">](../interfaces/view-model-ipage-ipagetarget.md#to)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>PageTarget<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md)</ept>.<bpt id="p2">[</bpt>to<ept id="p2">](../interfaces/view-model-ipage-ipagetarget.md#to)</ept> から継承</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">[</bpt>url<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#url)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>url<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md#url)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>url: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">url: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>If provided, this link is directly opened.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した場合、このリンクは直接開かれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">[</bpt>children<ept id="p1">](../interfaces/view-model-ipage-ipage.md#children)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>子<ept id="p1">](../interfaces/view-model-ipage-ipage.md#children)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>children: <bpt id="p1">[</bpt>Control<ept id="p1">](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)</ept> [ ]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">children: <bpt id="p1">[</bpt>Control<ept id="p1">](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)</ept> [ ]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The list of all direct children controls of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページのすべての直接の子コントロールの一覧。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source><bpt id="p1">[</bpt>dataLoadedInitially<ept id="p1">](../interfaces/view-model-ipage-ipage.md#dataloadedinitially)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>dataLoadedInitially<ept id="p1">](../interfaces/view-model-ipage-ipage.md#dataloadedinitially)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>dataLoadedInitially: Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataLoadedInitially: Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>A promise which resolves when the data has loaded for the first time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初めてデータが読み込まれたときに解決する約束。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">[</bpt>initialized<ept id="p1">](../interfaces/view-model-ipage-ipage.md#initialized)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>初期化済み<ept id="p1">](../interfaces/view-model-ipage-ipage.md#initialized)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>initialized: boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">initialized: boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>True if the page instance has been initialized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ インスタンスが初期化されている場合は、true です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source><bpt id="p1">[</bpt>metadata<ept id="p1">](../interfaces/view-model-ipage-ipage.md#metadata)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>メタデータ<ept id="p1">](../interfaces/view-model-ipage-ipage.md#metadata)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>metadata: <bpt id="p1">[</bpt>PageMetadata<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">metadata: <bpt id="p1">[</bpt>PageMetadata<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The page metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ メタデータ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source><bpt id="p1">[</bpt>metadataLoaded<ept id="p1">](../interfaces/view-model-ipage-ipage.md#metadataloaded)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>metadataLoaded<ept id="p1">](../interfaces/view-model-ipage-ipage.md#metadataloaded)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>metadataLoaded: Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">metadataLoaded: Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>A promise which resolves when the metadata has finished loading.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータが読み込みを完了したときに解決する約束。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">[</bpt>pageContext<ept id="p1">](../interfaces/view-model-ipage-ipage.md#pagecontext)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>pageContext<ept id="p1">](../interfaces/view-model-ipage-ipage.md#pagecontext)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>pageContext: string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageContext: string</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>The current page context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のページ コンテキスト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source><bpt id="p1">[</bpt>pageFilter<ept id="p1">](../interfaces/view-model-ipage-ipage.md#pagefilter)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>pageFilter<ept id="p1">](../interfaces/view-model-ipage-ipage.md#pagefilter)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>pageFilter: DataFilter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageFilter: DataFilter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The current filter applied on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページに適用されている現在のフィルター。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source><bpt id="p1">[</bpt>state<ept id="p1">](../interfaces/view-model-ipage-ipage.md#state)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>状態<ept id="p1">](../interfaces/view-model-ipage-ipage.md#state)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>state: <bpt id="p1">[</bpt>PageState<ept id="p1">](../enums/view-model-ipage-pagestate.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">state: <bpt id="p1">[</bpt>PageState<ept id="p1">](../enums/view-model-ipage-pagestate.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The current state of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの現在のステータス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source><bpt id="p1">[</bpt>syncError<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncerror)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>syncError<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncerror)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>syncError: boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">syncError: boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>True if the page's submission is in error state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの送信がエラー状態の場合、true です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>This normally happens when the server rejects submissions due to validation errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは通常、検証エラーのためにサーバーが送信を拒否した場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source><bpt id="p1">[</bpt>syncPending<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncpending)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>syncPending<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncpending)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>syncPending: boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">syncPending: boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>True if the page's submission is waiting to be synced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの送信が同期の待機中の場合、true です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt>syncProcessing<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncprocessing)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>syncProcessing<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncprocessing)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>syncProcessing: boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">syncProcessing: boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>True if the page instance is currently syncing its submission.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ インスタンスが現在送信を同期している場合は true です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source><bpt id="p1">[</bpt>syncUnitEditable<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncuniteditable)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>syncUnitEditable<ept id="p1">](../interfaces/view-model-ipage-ipage.md#syncuniteditable)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>syncUnitEditable: boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">syncUnitEditable: boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>True if it's possible to edit a submission while it's waiting to be synchronized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同期の待機中に送信が編集可能な場合、true です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source><bpt id="p1">[</bpt>title<ept id="p1">](../interfaces/view-model-ipage-ipage.md#title)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>タイトル<ept id="p1">](../interfaces/view-model-ipage-ipage.md#title)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>title: string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">title: string</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The title of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページのタイトル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source><bpt id="p1">[</bpt>canSubmit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#cansubmit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>canSubmit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#cansubmit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>canSubmit(): boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">canSubmit(): boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Returns true if action page can be submitted and there are no validation error messages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ページが送信可能で、検証エラー メッセージが存在しない場合は、true を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">[</bpt>close<ept id="p1">](../interfaces/view-model-ipage-ipage.md#close)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>閉じる<ept id="p1">](../interfaces/view-model-ipage-ipage.md#close)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>close(): void</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">close(): void</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Dispose the page instance and all its lifecycle events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ インスタンスとすべてのライフ サイクルイベントを破棄します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source><bpt id="p1">[</bpt>getAction<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getaction)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>getAction<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getaction)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>getAction(actionName: string): <bpt id="p1">[</bpt>PageLink<ept id="p1">](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">getAction(actionName: string): <bpt id="p1">[</bpt>PageLink<ept id="p1">](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Get a page action by name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前でページ アクションを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source><bpt id="p1">[</bpt>getActions<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getactions)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>getActions<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getactions)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>getActions(): <bpt id="p1">[</bpt>PageLink<ept id="p1">](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md)</ept> [ ]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">getActions(): <bpt id="p1">[</bpt>PageLink<ept id="p1">](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md)</ept> [ ]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Get all page actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのページ アクションを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source><bpt id="p1">[</bpt>getControl<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getcontrol)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>getControl<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getcontrol)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>getControl(controlName: string): <bpt id="p1">[</bpt>Control<ept id="p1">](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">getControl(controlName: string): <bpt id="p1">[</bpt>Control<ept id="p1">](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Get a page control by name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前でページ コントロールを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source><bpt id="p1">[</bpt>getDesign<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getdesign)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>getDesign<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getdesign)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>getDesign(): <bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">getDesign(): <bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Get the design object associated with the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページに関連付けられているデザイン オブジェクトを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source><bpt id="p1">[</bpt>getEntityContext<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getentitycontext)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>getEntityContext<ept id="p1">](../interfaces/view-model-ipage-ipage.md#getentitycontext)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>getEntityContext(): EntityRef</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">getEntityContext(): EntityRef</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Get current entity context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のエンティティ コンテキストを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source><bpt id="p1">[</bpt>isEditable<ept id="p1">](../interfaces/view-model-ipage-ipage.md#iseditable)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>isEditable<ept id="p1">](../interfaces/view-model-ipage-ipage.md#iseditable)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>isEditable(): boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">isEditable(): boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Returns true if the page is an Action Page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページがアクション ページの場合は true を返します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source><bpt id="p1">[</bpt>refreshData<ept id="p1">](../interfaces/view-model-ipage-ipage.md#refreshdata)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>refreshData<ept id="p1">](../interfaces/view-model-ipage-ipage.md#refreshdata)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>refreshData(): Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">refreshData(): Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Force refresh page data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ データを強制更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source><bpt id="p1">[</bpt>resume<ept id="p1">](../interfaces/view-model-ipage-ipage.md#resume)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>経歴<ept id="p1">](../interfaces/view-model-ipage-ipage.md#resume)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>resume(): Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">resume(): Promise <ph id="ph1">&amp;lt;</ph>void<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Resume a temporarily suspended page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一時的停止されたページを再開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source><bpt id="p1">[</bpt>submit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#submit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>送信<ept id="p1">](../interfaces/view-model-ipage-ipage.md#submit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>submit(): Promise <ph id="ph1">&amp;lt;</ph><bpt id="p1">[</bpt>CompleteEventArgs<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md)</ept><ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">submit(): Promise <ph id="ph1">&amp;lt;</ph><bpt id="p1">[</bpt>CompleteEventArgs<ept id="p1">](../interfaces/view-model-ipage-icompleteeventargs.md)</ept><ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Submit an Action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source><bpt id="p1">[</bpt>suspend<ept id="p1">](../interfaces/view-model-ipage-ipage.md#suspend)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>中断<ept id="p1">](../interfaces/view-model-ipage-ipage.md#suspend)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>suspend(): void</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">suspend(): void</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Temporarily suspend a page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページを一時的に中断します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source><bpt id="p1">[</bpt>onClose<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onclose)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onClose<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onclose)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>onClose: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onClose: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Event that is raised when a page is closed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページを閉じるときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source><bpt id="p1">[</bpt>onComplete<ept id="p1">](../interfaces/view-model-ipage-ipage.md#oncomplete)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onComplete<ept id="p1">](../interfaces/view-model-ipage-ipage.md#oncomplete)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>onComplete: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onComplete: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Event that is raised when an action is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションが完了したときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source><bpt id="p1">[</bpt>onDataLoaded<ept id="p1">](../interfaces/view-model-ipage-ipage.md#ondataloaded)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onDataLoaded<ept id="p1">](../interfaces/view-model-ipage-ipage.md#ondataloaded)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>onDataLoaded: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onDataLoaded: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Event that fires when the page data has loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ データが読み込まれたときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source><bpt id="p1">[</bpt>onInit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#oninit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onInit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#oninit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>onInit: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onInit: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Event that fires when a page instance has been initialized, and the metadata has been loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ インスタンスが初期化され、メタデータがロードされたときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source><bpt id="p1">[</bpt>onPreInit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onpreinit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onPreInit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onpreinit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>onPreInit: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onPreInit: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Event that fires when a page instance has been initialized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ インスタンスが初期化されたときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source><bpt id="p1">[</bpt>onRefresh<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onrefresh)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onRefresh<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onrefresh)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>onRefresh: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onRefresh: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Event that fires on forced page refresh, before new data has been loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータが読み込まれる前に、強制的なページ更新で発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source><bpt id="p1">[</bpt>onStateChange<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onstatechange)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onStateChange<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onstatechange)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>onStateChange: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onStateChange: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Event that fires when the page state changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ状態が変更するときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source><bpt id="p1">[</bpt>onSubmit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onsubmit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onSubmit<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onsubmit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>onSubmit: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph><bpt id="p2">[</bpt>PageSubmitArgs<ept id="p2">](../interfaces/view-model-ipage-ipagesubmitargs.md)</ept><ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onSubmit: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph><bpt id="p2">[</bpt>PageSubmitArgs<ept id="p2">](../interfaces/view-model-ipage-ipagesubmitargs.md)</ept><ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Event that fires before an action is submitted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションが送信される前に発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>It can be intercepted for action validation deferring</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、アクションの検証遅延について中断できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source><bpt id="p1">[</bpt>onSyncStatusChange<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onsyncstatuschange)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>onSyncStatusChange<ept id="p1">](../interfaces/view-model-ipage-ipage.md#onsyncstatuschange)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>onSyncStatusChange: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onSyncStatusChange: <bpt id="p1">[</bpt>EventHook<ept id="p1">](../interfaces/event-ievent-ieventhook.md)</ept> <ph id="ph1">&amp;lt;</ph>null<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Event that fires when the page sync status changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの同期状態が変更するときに発生するイベント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>PageMetadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageMetadata</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>PageMetadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageMetadata</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source><bpt id="p1">[</bpt>Controls<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#controls)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>コントロール<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#controls)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Controls: <bpt id="p1">[</bpt>ControlMetadata<ept id="p1">](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)</ept> <ph id="ph1">\[</ph> <ph id="ph2">\]</ph> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール: <bpt id="p1">[</bpt>ControlMetadata<ept id="p1">](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)</ept> <ph id="ph1">\[</ph> <ph id="ph2">\]</ph> (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source><bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#design)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#design)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Design: <bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン: <bpt id="p1">[</bpt>デザイン<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept> (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source><bpt id="p1">[</bpt>Id<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#id)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ID<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#id)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Id: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Id: string (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source><bpt id="p1">[</bpt>QuickSubmit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#quicksubmit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>QuickSubmit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#quicksubmit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>QuickSubmit: boolean (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">QuickSubmit: ブール値 (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source><bpt id="p1">[</bpt>SourcePageId<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#sourcepageid)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SourcePageId<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#sourcepageid)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>SourcePageId: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SourcePageId: 文字列 (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source><bpt id="p1">[</bpt>SubmitButtonDesign<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#submitbuttondesign)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SubmitButtonDesign<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#submitbuttondesign)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>SubmitButtonDesign: <bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SubmitButtonDesign: <bpt id="p1">[</bpt>デザイン<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept> (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source><bpt id="p1">[</bpt>Tasks<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#tasks)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>仕事<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#tasks)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Tasks: <bpt id="p1">[</bpt>PageMetadata<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md)</ept> <ph id="ph1">\[</ph> <ph id="ph2">\]</ph> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク: <bpt id="p1">[</bpt>PageMetadata<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md)</ept><ph id="ph1">\[</ph><ph id="ph2">\]</ph> (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source><bpt id="p1">[</bpt>Title<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#title)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>タイトル<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#title)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Title: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイトル: 文字列 (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source><bpt id="p1">[</bpt>OnDataLoaded<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#ondataloaded)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>OnDataLoaded<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#ondataloaded)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>OnDataLoaded: function(sender: <bpt id="p1">[</bpt>Page<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept>, dataWrapper: any): void (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OnDataLoaded: 機能 (送信者: <bpt id="p1">[</bpt>ページ<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept>、dataWrapper: すべて) : 無効 (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source><bpt id="p1">[</bpt>OnInit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#oninit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>OnInit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#oninit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>OnInit: function(sender: <bpt id="p1">[</bpt>Page<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept>): void (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OnInit: 機能 (送信者: <bpt id="p1">[</bpt>ページ<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept>): 無効 (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source><bpt id="p1">[</bpt>OnPreInit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#onpreinit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>OnPreInit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#onpreinit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>OnPreInit: function(sender: <bpt id="p1">[</bpt>Page<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept>): void (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OnInit: 機能 (送信者: <bpt id="p1">[</bpt>ページ<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept>): 無効 (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source><bpt id="p1">[</bpt>OnSubmit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#onsubmit)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>OnSubmit<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#onsubmit)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>OnSubmit: function(dataValues: any, args: any): void (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OnSubmit: 機能 (dataValues: すべて、args: すべて): 無効 (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source><bpt id="p1">[</bpt>OnTaskSubmitted<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#ontasksubmitted)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>OnTaskSubmitted<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#ontasksubmitted)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>OnTaskSubmitted: function(taskHandle: any, taskOptions: any): any (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OnTaskSubmitted: 機能 (taskHandle: すべて、taskOptions: すべて): すべて (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source><bpt id="p1">[</bpt>OnTaskSubmitting<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#ontasksubmitting)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>OnTaskSubmitting<ept id="p1">](../interfaces/view-model-ipage-ipagemetadata.md#ontasksubmitting)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>OnTaskSubmitting: function(taskOptions: any): any (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OnTaskSubmitted: 機能 (taskOptions: すべて): すべて (オプション)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>PageOptions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageOptions</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>PageOptions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageOptions</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source><bpt id="p1">[</bpt>appId<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#appid)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>appId<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#appid)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>appId: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">appId: string (optional)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source><bpt id="p1">[</bpt>design<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#design)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>デザイン<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#design)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>design: <bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">design: <bpt id="p1">[</bpt>Design<ept id="p1">](../interfaces/view-model-ipage-idesign.md)</ept> (optional)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source><bpt id="p1">[</bpt>excludeContext<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#excludecontext)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>excludeContext<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#excludecontext)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>excludeContext: boolean (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">excludeContext: boolean (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source><bpt id="p1">[</bpt>filter<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#filter)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>フィルター<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#filter)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>filter: DataFilter (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">filter: DataFilter (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source><bpt id="p1">[</bpt>filterLocalOnly<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#filterlocalonly)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>filterLocalOnly<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#filterlocalonly)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>filterLocalOnly: boolean (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">filterLocalOnly: boolean (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source><bpt id="p1">[</bpt>pageContext<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#pagecontext)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>pageContext<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#pagecontext)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>pageContext: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageContext: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source><bpt id="p1">[</bpt>pageId<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#pageid)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>pageId<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#pageid)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>pageId: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageId: string (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source><bpt id="p1">[</bpt>readOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#readoptions)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>readOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md#readoptions)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>readOptions: IReadOptions (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">readOptions: IReadOptions (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>PageSubmitArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageSubmitArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>PageSubmitArgs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageSubmitArgs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source><bpt id="p1">[</bpt>dataValues<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#datavalues)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>dataValues<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#datavalues)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>dataValues: any</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dataValues: any</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Get the payload of the submit action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信アクションの伝送データを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source><bpt id="p1">[</bpt>sender<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#sender)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>送信者<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#sender)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>sender: <bpt id="p1">[</bpt>Page<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">sender: <bpt id="p1">[</bpt>Page<ept id="p1">](../interfaces/view-model-ipage-ipage.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Get the sender page instance of the submit action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信アクションの送信者ページ インスタンスを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source><bpt id="p1">[</bpt>addMessage<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#addmessage)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>addMessage<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#addmessage)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>addMessage(message: string, type: any): any</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">addMessage(message: string, type: any): any</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Add a validation error message to be displayed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示される検証エラー メッセージを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source><bpt id="p1">[</bpt>cancel<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#cancel)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>キャンセル<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#cancel)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>cancel(): any</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">cancel(): any</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>Prevent the action from submitting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションの送信を禁止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source><bpt id="p1">[</bpt>getMessages<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#getmessages)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>getMessages<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#getmessages)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>getMessages(): string [ ]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">getMessages(): string [ ]</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>Get all previously added messages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前に追加されたすべてのメッセージを取得します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source><bpt id="p1">[</bpt>isCancelled<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#iscancelled)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>isCancelled<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#iscancelled)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>isCancelled(): boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">isCancelled(): boolean</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>Check if the submit action is cancelled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信アクションがキャンセルされているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source><bpt id="p1">[</bpt>wait<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#wait)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>待機<ept id="p1">](../interfaces/view-model-ipage-ipagesubmitargs.md#wait)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>wait(promise: Promise <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph>): any</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">wait(promise: Promise <ph id="ph1">&amp;lt;</ph>any<ph id="ph2">&amp;gt;</ph>): any</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>Wait on a given promise before continuing with the submission.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信を続行する前に、指定された約束を待ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>PageTarget</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageTarget</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>Hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>PageTarget</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PageTarget</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>NavigationArgs<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph>└─ <bpt id="p1">[</bpt>NavigationArgs<ept id="p1">](../interfaces/view-model-ipage-inavigationargs.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Signature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source><bpt id="p1">[</bpt>params<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md#params)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>パラメーター<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md#params)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>params: <bpt id="p1">[</bpt>PageOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md)</ept> (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">params: <bpt id="p1">[</bpt>PageOptions<ept id="p1">](../interfaces/view-model-ipage-ipageoptions.md)</ept> (省略可)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source><bpt id="p1">[</bpt>to<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md#to)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>to<ept id="p1">](../interfaces/view-model-ipage-ipagetarget.md#to)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>to: string (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">to: string (省略可)</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>