<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-offline-functionality.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-offline-functionality.4aedac.056dd028410a4b3f7e8e1e22370f304d0c17263f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>056dd028410a4b3f7e8e1e22370f304d0c17263f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\pos-offline-functionality.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Offline point of sale (POS) functionality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン販売時点管理 (POS) の機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article provides information about offline mode for Retail Modern POS, in which POS devices automatically switch from the channel database to the offline database if the retail server is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、小売サーバーが利用できない場合にチャンネルのデータベースからオフライン データベースに POS デバイスが自動的に切り替わる、Retail Modern POS のオフライン モードについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This article also includes general setup information for offline mode and explains the data synchronization that occurs between the offline database and the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、この記事ではオフライン モードの一般的な設定情報も含まれ、オフライン データベースとチャンネルのデータベース間で発生するデータ同期についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Offline point of sale (POS) functionality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン販売時点管理 (POS) の機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article provides information about offline mode for Retail Modern POS, in which POS devices automatically switch from the channel database to the offline database if the retail server is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、小売サーバーが利用できない場合にチャンネルのデータベースからオフライン データベースに POS デバイスが自動的に切り替わる、Retail Modern POS のオフライン モードについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This article also includes general setup information for offline mode and explains the data synchronization that occurs between the offline database and the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、この記事ではオフライン モードの一般的な設定情報も含まれ、オフライン データベースとチャンネルのデータベース間で発生するデータ同期についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In Retail Modern POS, a point of sale (POS) device goes into offline mode whenever the retail server is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS では、小売サーバーが利用できないときはいつでも 販売時点管理 (POS) デバイスがオフライン モードになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Therefore, if the connection with the retail server is lost, Retail Modern POS automatically switches to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、小売サーバーとの接続が失われると、Retail Modern POS はオフライン データベースに自動的に切り替わります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>During a sales transaction, if a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売トランザクション中に、オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しなかった場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>While POS device is in offline mode, Retail Modern POS tries to reconnect to the retail server after the reconnection attempt interval that is configured in the offline profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デバイスがオフライン モードの間に、Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に再接続を試みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This reconnection attempt occurs only at the beginning of a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この再接続試行は、トランザクションの先頭でのみ実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Determining the connection mode of Retail Modern POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS の接続モードを決定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The status header in Retail Modern POS indicates the current connection status, and the <bpt id="p1">**</bpt>Connection status<ept id="p1">**</ept> window shows the status of the last attempt to sync with the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS のステータス ヘッダーは現在の接続ステータスを表示し、<bpt id="p1">**</bpt>接続ステータス<ept id="p1">**</ept> ウィンドウはオフライン データベースと同期する最後の試行のステータスを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Connection status<ept id="p1">](./media/status.png)](./media/status.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>接続ステータス<ept id="p1">](./media/status.png)](./media/status.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Creating a button to manually switch between online and offline modes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動でオンラインとオフライン モードを切り替えるためのボタンを作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can add a button to Retail Modern POS to manually switch between online and offline modes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Create a button for POS operation <bpt id="p1">**</bpt>917 – Database connection status<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 操作 <bpt id="p1">**</bpt>917 – データベース接続ステータス<ept id="p1">**</ept>のボタンを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The name of this button is <bpt id="p1">**</bpt>Disconnect<ept id="p1">**</ept> when Retail Modern POS is connected to the retail server and <bpt id="p2">**</bpt>Connect<ept id="p2">**</ept> when it is disconnected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このボタンの名前は、Retail Modern POS が小売サーバーに接続されている場合は<bpt id="p1">**</bpt>接続解除<ept id="p1">**</ept>となり、接続解除されている場合は<bpt id="p2">**</bpt>接続<ept id="p2">**</ept>となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can use this button to view the connection, and to disconnect from the retail server or connect to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このボタンは接続の表示、小売サーバーとの接続解除および接続に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Disconnect button in Retail Modern POS<ept id="p1">](./media/details-1024x537.png)](./media/details.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Retail Modern POS の接続解除ボタン<ept id="p1">](./media/details-1024x537.png)](./media/details.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To enable offline support for a POS device (register), set the <bpt id="p1">**</bpt>Support offline<ept id="p1">**</ept> option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> on the <bpt id="p3">**</bpt>Register<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS のデバイス (登録) のオフライン サポートを有効にするには、<bpt id="p3">**</bpt>登録<ept id="p3">**</ept> ページで、<bpt id="p1">**</bpt>オフラインのサポート<ept id="p1">**</ept> オプションを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>A new channel database entity is created and added to the store's channel data group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいチャンネル データベース エンティティが作成され、店舗のチャンネル データ グループに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Then run all the required distribution schedules to generate the data packages for the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、オフライン データベースのデータ パッケージを生成するためにすべての配送スケジュールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Next, install the offline version of Retail Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、Retail Modern POS のオフライン バージョンをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The installation process creates the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストール プロセスでは、オフライン データベースが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Additionally, install Microsoft SQL Server 2014 Express if it is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、必要な場合は、Microsoft SQL Server 2014 Express をインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Offline data synchronization starts after the first sign-in to Retail Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS への最初のサインイン後にオフライン データの同期が開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Data synchronization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The Retail scheduler is used to send master data to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用スケジューラはオフライン データベースにマスター データを送信するのに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>By default, when a distribution schedule is run, data changes are sent to both the channel database and the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、配送スケジュールの実行時に、データの変更がチャンネルのデータベースとオフライン データベースの両方に送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Retail Modern POS includes the async sync library, which downloads any available data packages and inserts them into the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS には、使用可能なすべてのデータ パッケージをダウンロードし、オフライン データベースに挿入する async sync ライブラリが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If any transactions are created offline, Retail Modern POS uploads them to the retail server, so that they can be inserted into the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションがオフラインで作成された場合、Retail Modern POS はそれらをチャンネル データベースに挿入するためにアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Offline data synchronization can occur only if Retail Modern POS is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフラインのデータ同期は、Retail Modern POS の実行時にのみ実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Offline synchronization<ept id="p1">](./media/offline-sync-1024x521.png)](./media/offline-sync.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>オフライン同期<ept id="p1">](./media/offline-sync-1024x521.png)](./media/offline-sync.png)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>