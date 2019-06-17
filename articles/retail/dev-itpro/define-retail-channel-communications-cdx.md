<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="define-retail-channel-communications-cdx.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>define-retail-channel-communications-cdx.0e37c1.35540a70b48d7d25e2e8ae11fcd243628c95523a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>35540a70b48d7d25e2e8ae11fcd243628c95523a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\define-retail-channel-communications-cdx.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Commerce Data Exchange and retail channel communications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange と小売チャネルのコミュニケーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides an overview of Commerce Data Exchange and its components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Commerce Data Exchange とその要素の概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It explains the part that each component plays in the transfer of data between Microsoft Dynamics 365 for Retail and retail channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、Microsoft Dynamics 365 for Retail と小売チャネルとの間でのデータの転送で各コンポーネントが果たす役割について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Commerce Data Exchange and retail channel communications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange と小売チャネルのコミュニケーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic provides an overview of Commerce Data Exchange and its components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Commerce Data Exchange とその要素の概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It explains the part that each component plays in the transfer of data between Microsoft Dynamics 365 for Retail headquarters and retail channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、Microsoft Dynamics 365 for Retail バックオフィスと小売チャネルとの間でのデータの転送で各コンポーネントが果たす役割について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Commerce Data Exchange is a system that transfers data between Retail headquarters and retail channels, such as online stores or brick-and-mortar stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange は、小売用バックオフィスと、オンライン ストア、実際の店舗などの小売チャネルの間でデータを転送するシステムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The database that stores data for a retail channel is separate from the Retail database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャンネルのデータを格納するデータベースは、小売りデータベースとは別にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The channel database holds only the data that is required for retail transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネルのデータベースは、小売トランザクションに必要なデータのみ格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Master data is configured in Retail headquarters and distributed to channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター データが小売用バックオフィスでコンフィギュレーションされ、チャネルに配分されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Transactional data is created in the point of sale (POS) system or the online store, and then uploaded to Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション データは販売時点管理 (POS) システムまたはオンライン店舗で作成され、小売用バックオフィスにアップロードされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data distribution is asynchronous.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ配送は非同期です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In other words, the process of gathering and packaging data at the source occurs separately from the process of receiving and applying data at the destination.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、データを収集してソースでパッケージングするプロセスは、データを取得して適用するプロセスとは別に行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For some scenarios, such as price and inventory lookups, data must be retrieved in real time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格および在庫検索などのシナリオの場合、データはリアルタイムに取得する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>To support these scenarios, Commerce Data Exchange also includes a service that enables real-time communication between Retail headquarters and a channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのシナリオをサポートするために、Commerce Data Exchange には、小売用バックオフィスとチャネル間のリアルタイム通信を可能にするサービスが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>updated-retail-graphic<ept id="p1">](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>更新済小売グラフィック<ept id="p1">](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Async Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非同期サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Microsoft SQL Server change tracking on the Retail database is used to determine the data changes that must be sent to channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売データベースの Microsoft SQL Server 変更追跡は、チャネルに送信する必要のあるデータの変更内容を特定するのに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Based on a distribution schedule, Retail headquarters packages that data and saves it to central storage (Azure blob storage).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送スケジュールに基づいて、小売用バックオフィスはそのデータをパッケージングして中央の保存場所 (Azure blob storage) に保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>A separate batch process uses the Commerce Data Exchange: Async Client library to insert this data package into the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のバッチ処理は、このデータ パッケージをチャネルのデータベースに挿入するために Commerce Data Exchange: Async Client ライブラリを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Async Service<ept id="p1">](./media/async-300x239.png)](./media/async.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>非同期サービス<ept id="p1">](./media/async-300x239.png)](./media/async.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Retail scheduler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用スケジューラ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Scheduler jobs are the mechanism for distributing data to and from locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スケジューラ ジョブとは、データを配送場所へ (から) 配送するためのメカニズムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Jobs are made up of subjobs, which specify the tables and table fields that contain the data to distribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ジョブは、配分するデータを含むテーブルおよびテーブル フィールドを指定するサブジョブで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Retail headquarters includes predefined scheduler jobs and subjobs that meet the replication requirements of most organizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスには、ほとんどの組織のレプリケーションの要件を満たすサブジョブと定義済スケジューラ ジョブが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following types of predefined jobs are created:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のタイプの定義済ジョブが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Download jobs<ept id="p1">**</ept> – Download jobs send data that has changed from Retail headquarters to channel databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンロード ジョブ<ept id="p1">**</ept> - ダウンロード ジョブは、小売用バックオフィスからチャネル データベースに変更されたデータを送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Modifications to records are tracked through SQL Server change tracking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードへの変更は、SQL Server 変更履歴によって追跡されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Upload jobs (P jobs)<ept id="p1">**</ept> – Upload jobs pull sales transactions from a channel into the Retail database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アップロード ジョブ (P ジョブ)<ept id="p1">**</ept> – アップロード ジョブは、チャンネルから小売データベースへの販売トランザクションをプルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>P jobs upload data incrementally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">P ジョブは、データを漸増的にアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>When a P job runs, the Async Client library checks the replication counter for records that have already been received from a location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">P ジョブが実行されると、Async Client ライブラリが場所から既に受け取ったレコードに対するレプリケーション カウンターをチェックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>A record is uploaded only if its replication counter is more than the largest value that is found.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードは、レプリケーション カウンターが検出された最大値を超える場合のみアップロードされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>P jobs don't update data that was previously uploaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">P ジョブは以前にアップロードされたデータを更新しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The distribution schedule is used to run the data transfer, either manually or by scheduling a batch job in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送スケジュールは、手動または小売用バックオフィスでスケジューリングされたバッチ ジョブによるデータ転送の実行に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>A distribution schedule can contain one or more channel data groups, and one or more scheduler jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送スケジュールには、1 つ以上のチャンネル データ グループと 1 つ以上のスケジューラ ジョブを含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>To ensure that the scheduler jobs are running smoothly, do not rename the "Default" database configured for the instance, and do not create a second database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スケジューラー・ジョブが円滑に実行されていることを確認するには、インスタンス用に構成された「既定の」データベース名を変更せず、2 番目のデータベースを作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>All non-Retail Store Scale Unit databases are managed by Microsoft, and only one default database is expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit ではないすべてのデータベースは Microsoft により管理され、1 つの既定のデータベースのみが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Realtime Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルタイム サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Commerce Data Exchange: Real-time Service is an integrated service that provides real-time communication between Retail headquarters and retail channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange: Real-time Service は、小売用バックオフィスと小売チャネル間のリアルタイム通信を提供する統合サービスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Real-time Service enables individual POS computers and online stores to retrieve specific data from Retail headquarters in real time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアル タイム サービスにより、個々の POS コンピューターとオンライン ストアが小売用バックオフィスから特定のデータをリアルタイムで取得できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Although most key operations can be performed in the local channel database, the following scenarios require direct access to the data that is stored in Retail headquarters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどのキー操作はローカルのチャンネル データベースで実行できますが、次のシナリオは小売用バックオフィスに格納されているデータへの直接アクセスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Issuing and redeeming gift cards</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフトカードの発行および引換え</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Redeeming loyalty points</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ ポイントを引き換え</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Issuing and redeeming credit memos</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クレジット メモの発行および引換え</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Creating and updating customer records</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客レコードを作成または更新します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Creating, updating, and completing sales orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売注文を作成、更新、完了しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Receiving inventory against a purchase order or transfer order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書または移動オーダーに対する在庫を入荷</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Performing inventory counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">棚卸資産会計の実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Retrieving sales transactions across stores and completing return transactions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗間から販売トランザクションを取得し、返品トランザクションを完了します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Real-time Service<ept id="p1">](./media/rts.png)](./media/rts.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Real-time Service<ept id="p1">](./media/rts.png)](./media/rts.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>A predefined Real-time Service profile is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義済の Real-time Service プロファイルが作成されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>