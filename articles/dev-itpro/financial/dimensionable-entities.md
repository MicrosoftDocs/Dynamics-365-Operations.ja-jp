<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="dimensionable-entities.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>dimensionable-entities.23013f.e43eeb97b0032e35299280662c19cd7ec5a04010.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e43eeb97b0032e35299280662c19cd7ec5a04010</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\dimensionable-entities.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Make backing tables consumable as financial dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードとして使用可能なバッキング テーブルの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides the steps that you need to follow to make a backing table usable as a Financial dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Make backing tables consumable as financial dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードとして使用可能なバッキング テーブルの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides the steps that you need to follow if you want to make a backing table usable as a Financial dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Do not create financial dimensions that have values that are not reusable or use one-to-one dimension value combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再利用できない値を持つまたは 1 対 1 の分析コード値を使用する、財務分析コードを作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Do not create financial dimensions that have values that are not reusable or use one-to-one dimension value combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再利用できない値を持つまたは 1 対 1 の分析コード値を使用する、財務分析コードを作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Views cannot be used as a source of dimension values for a DimAttribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビューを、DimAttribute の分析コード値のソースとして使用することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although this may seem to work, it will cause MR to fall back to row-by-row processing in order to get the dimension fact data imported to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これはうまくいくように見えますが、分析コードのファクト データがデータベースにインポートされるようにするため、MR が行ごとの処理にフォールバックされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This results in extremely slow performance or broken reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、パフォーマンスがかなり低下したり、レポートが遮断されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The primary table that is to be used as a source of financial dimension data MUST have a unique natural key value of 30 characters or less, and that value MUST resolve to a single RECID within that table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードのデータのソースとして使用する基本テーブルには、30 文字以内の固有ナチュラル キー値が必用であり、その値はそのテーブル内の 1 つの RECID を解決する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The extended Name column can come from another source join (such as DirPartyTable or elsewhere) because it is used only for displaying additional context to the user and is not used to resolve uniqueness on natural key entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張された名前列は、追加のコンテキストをユーザーに表示する場合にのみ使用され、ナチュラル キー エントリの一意性を解決するためには使用されないため、もう 1 つのソース結合 (DirPartyTable や別の場所など) から取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Financial dimensions should be reusable values needed for transaction and analytical processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードは、トランザクションおよび分析プロセスに必要な再利用可能な値にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>These dimensions should represent sources of data that can provide high level of reuse across multiple transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの分析コードは、複数のトランザクションにわたって全体的な再利用を提供できるデータのソースを表す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Do not select a backing table that supplies identity data that represents high volatility when represented with other dimension values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の分析コード値に表示される際、高変動を表す ID データを供給するバッキング テーブルを選択しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This can increase storage and processing costs and negatively impact performance and analytical value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、ストレージと処理のコストが増加し、パフォーマンスと分析の価値に悪影響を及ぼします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Examples of highly volatile data include timestamps and identifiers that are frequently incremented, such as:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">揮発性の非常に高いデータの例としては、以下のように、頻繁に増分されるタイムスタンプや識別子などがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Documents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Sales orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売注文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Purchase orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Transactions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Checks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小切手</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Serials</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シリアル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Tickets</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チケット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>License numbers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス番号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>These are referred to as degenerate dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは縮退分析コードと呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Tracking these values should be done outside of financial dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの値の追跡は、財務分析コード以外で行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This means that you should use customizations for the transactional records that need information, and these values should not be stored along with the financial dimension values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、情報を必要とするトランザクション レコードのカスタマイズを使用する必要があります。これらの値は、財務分析コード値と共に保存しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>By following these steps, your view will automatically appear in the <bpt id="p1">**</bpt>Use values from<ept id="p1">**</ept> drop-down menu on the <bpt id="p2">**</bpt>Financial dimensions<ept id="p2">**</ept> page, and the values will be populated on the <bpt id="p3">**</bpt>Financial dimension values<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順に従うことにより、<bpt id="p2">**</bpt>財務分析コード<ept id="p2">**</ept> ページの<bpt id="p1">**</bpt>値の使用元<ept id="p1">**</ept>のドロップダウン メニューにビューが自動的に表示され、値は<bpt id="p3">**</bpt>財務分析コード値<ept id="p3">**</ept>ページに入力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>If your dimension is backed by the <bpt id="p1">**</bpt>OMOperatingUnit<ept id="p1">**</ept> table then many of the steps are already completed for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードが <bpt id="p1">**</bpt>OMOperatingUnit<ept id="p1">**</ept> テーブルによってサポートされている場合、手順の多くは既に完了しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Follow the steps in the "<bpt id="p1">[</bpt>Add a new OMOperatingUnit type backed entity<ept id="p1">](#add-a-new-omoperatingunit-type-backed-entity)</ept>" section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「<bpt id="p1">[</bpt>新しい OMOperatingUnit タイプがサポートしているエンティティを追加<ept id="p1">](#add-a-new-omoperatingunit-type-backed-entity)</ept>」セクション の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Step 1: Create a view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1: ビューを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The first step is to create a view in the same model as your backing table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のステップは、バッキング テーブルと同じモデルでビューを作成することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Before you complete the following steps, verify that the backing table has <bpt id="p1">**</bpt>Create Rec Id Index = Yes<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Table Properties<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の手順を実行する前に、<bpt id="p2">**</bpt>テーブルのプロパティ<ept id="p2">**</ept> ウィンドウでバッキング テーブルが <bpt id="p1">**</bpt>Create Rec Id Index = Yes<ept id="p1">**</ept> であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Alternatively, ensure that the table has a unique index and RECID is the first segment of that index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、テーブルに一意のインデックスがあり、RECID がそのインデックスの最初のセグメントであることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In your project, click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>New Item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトで<bpt id="p1">**</bpt>追加<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Select <bpt id="p1">**</bpt>View<ept id="p1">**</ept> and then click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Right-click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> and select <bpt id="p2">**</bpt>Rename<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>名前の変更<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Name the view <bpt id="p1">**</bpt>DimAttribute<ept id="p1">**</ept>[BackingTableName].</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DimAttribute<ept id="p1">**</ept>[BackingTableName] ビューに名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>For example, DimAttributeCustTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、DimAttributeCustTable。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Expand <bpt id="p1">**</bpt>View Metadata<ept id="p1">**</ept>, and then drag your table to the <bpt id="p2">**</bpt>Data Sources<ept id="p2">**</ept> node on the view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メタデータの表示<ept id="p1">**</ept>を展開し、テーブルを画面上の<bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept>ノードにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Rename the node from <bpt id="p1">**</bpt>BackingTableName<ept id="p1">**</ept> to <bpt id="p2">**</bpt>BackingEntity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノードの名前を <bpt id="p1">**</bpt>BackingTableName<ept id="p1">**</ept> から <bpt id="p2">**</bpt>BackingEntity<ept id="p2">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Identify the key, value, and name for the table that you want to use as a financial dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務分析コードとして使用するテーブルのキー、値、および名前を識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Find the fields and drag to the BackingEntity data source list, or copy and paste the fields on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを検索して、BackingEntity データ ソースの一覧にドラッグし、またはデータ ソース上のフィールドにコピーして貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Rename the three fields to:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 つのフィールドの名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Key<ept id="p1">**</ept> – This is the surrogate key, typically the RecID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キー<ept id="p1">**</ept> – これは代理キーで、通常は RecID です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept> - This is the natural key, for example the AccountNum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept> - これは、AccountNum のようなナチュラル キーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>It is a string up to 30 characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大 30 文字の文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Name<ept id="p1">**</ept> – This is the description, which is typically the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Description<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept> – これは説明で、通常は<bpt id="p2">**</bpt>名前<ept id="p2">**</ept>または<bpt id="p3">**</bpt>説明<ept id="p3">**</ept>フィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>It is a string up to 60 characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大 60 文字の文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You may need to create a <bpt id="p1">**</bpt>Range<ept id="p1">**</ept> on the view if the backing table removes data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッキング テーブルがデータを削除する場合、ビューで <bpt id="p1">**</bpt>範囲<ept id="p1">**</ept> を作成することが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>For example, if you are using an Operating unit and only want Department, you will want to use the range for that operating unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、作業単位を使用し部門のみを必要とする場合、その作業単位の範囲を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Right-click <bpt id="p1">**</bpt>Indexes<ept id="p1">**</ept> and select <bpt id="p2">**</bpt>New Index<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいインデックス<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいインデックス<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Select <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> as the Data field on the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウでデータ フィールドとして <bpt id="p1">**</bpt>値<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You can rename the index if needed, however you need to set <bpt id="p1">**</bpt>Allow Duplicates<ept id="p1">**</ept> to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてインデックスの名前を変更することができますが、<bpt id="p1">**</bpt>重複の許可<ept id="p1">**</ept> を <bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept> にセットする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Right-click <bpt id="p1">**</bpt>Indexes<ept id="p1">**</ept> and select <bpt id="p2">**</bpt>New Index<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいインデックス<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいインデックス<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Select <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> as the Data field on the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウでデータ フィールドとして <bpt id="p1">**</bpt>名前<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>You can rename the index if needed, however you need to set <bpt id="p1">**</bpt>Allow Duplicates<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてインデックスの名前を変更することができますが、<bpt id="p1">**</bpt>重複の許可<ept id="p1">**</ept> を <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> にセットする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Click <bpt id="p1">**</bpt>View<ept id="p1">**</ept>, and in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the <bpt id="p3">**</bpt>Singular label<ept id="p3">**</ept> field to the reference label ID of your choice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで、選択した参照ラベル ID に <bpt id="p3">**</bpt>単数形ラベル<ept id="p3">**</ept> フィールドを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>This should be the label that indicates a single value, such as Customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、顧客などの単一の値を示すラベルである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Set the <bpt id="p1">**</bpt>Label<ept id="p1">**</ept> field to the reference label ID of your choice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル<ept id="p1">**</ept> フィールドを選択した参照ラベル ID に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This should be the label that indicates multiple values, such as Customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、顧客などの複数の値を示すラベルである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This value will show in the drop-down list in the <bpt id="p1">**</bpt>Use Values from<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Financial dimensions<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この値は、<bpt id="p2">**</bpt>財務分析コード<ept id="p2">**</ept> ページの <bpt id="p1">**</bpt>値の使用元<ept id="p1">**</ept> フィールドのドロップダウン リストに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Enter <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>TitleField1<ept id="p2">**</ept> field in the <bpt id="p3">**</bpt>Properties<ept id="p3">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>プロパティ<ept id="p3">**</ept>ウィンドウの <bpt id="p2">**</bpt>TitleField1<ept id="p2">**</ept> フィールドに、<bpt id="p1">**</bpt>値<ept id="p1">**</ept>を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Enter <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>TitleField2<ept id="p2">**</ept> field in the <bpt id="p3">**</bpt>Properties<ept id="p3">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>プロパティ<ept id="p3">**</ept>ウィンドウの <bpt id="p2">**</bpt>TitleField2<ept id="p2">**</ept> フィールドに、<bpt id="p1">**</bpt>名前<ept id="p1">**</ept>を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Review the backing table properties and identify the config key it is using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッキング テーブルのプロパティを確認し、使用している config キーを識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>On <bpt id="p1">**</bpt>View<ept id="p1">**</ept>, enter the same <bpt id="p2">**</bpt>Configuration key<ept id="p2">**</ept> as the backing table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept>で、バッキング テーブルと同じ<bpt id="p2">**</bpt>コンフィギュレーション キー<ept id="p2">**</ept>を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Security access must be granted to non-admin users for the new view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者以外のユーザーに、新しいビューのセキュリティ アクセス権を付与する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>For releases 7.2 and earlier where over-layering is used - Search for <bpt id="p1">**</bpt>DimensionEssentials<ept id="p1">**</ept> and add it to the Project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイが使用されるリリース 7.2 およびそれ以前では、<bpt id="p1">**</bpt>DimensionEssentials<ept id="p1">**</ept> を検索し、プロジェクトに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Expand <bpt id="p1">**</bpt>DimensionEssentials<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>Permissions<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>New Permission<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DimensionEssentials<ept id="p1">**</ept> を展開し、<bpt id="p2">**</bpt>アクセス許可<ept id="p2">**</ept>を右クリックし、その後<bpt id="p3">**</bpt>新しいアクセス許可<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, set the <bpt id="p2">**</bpt>Access Level<ept id="p2">**</ept> to <bpt id="p3">**</bpt>Read<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>アクセス レベル<ept id="p2">**</ept>を<bpt id="p3">**</bpt>読み取り<ept id="p3">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Click <bpt id="p1">**</bpt>Security Privilege<ept id="p1">**</ept> and add the view under the <bpt id="p2">**</bpt>Permissions<ept id="p2">**</ept> node with an <bpt id="p3">**</bpt>Access Level<ept id="p3">**</ept> of <bpt id="p4">**</bpt>Read<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティ権限<ept id="p1">**</ept>をクリックし、<bpt id="p4">**</bpt>読み取り<ept id="p4">**</ept>の<bpt id="p3">**</bpt>アクセス レベル<ept id="p3">**</ept>を<bpt id="p2">**</bpt>アクセス許可<ept id="p2">**</ept>ノードの下に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You may need to extend one of these into the model that you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの 1 つを使用しているモデルに拡張することが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>For releases 7.3 and later where extensions are used - Create a new Security Privilege in your custom model alongside the new view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能が使用されているリリース 7.3 以降では、新しいビューと共にカスタム モデルで新しいセキュリティ権限を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Right-click the <bpt id="p1">**</bpt>Permissions<ept id="p1">**</ept> node, and choose <bpt id="p2">**</bpt>New Permission<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクセス許可<ept id="p1">**</ept> ノードを右クリックし、<bpt id="p2">**</bpt>新しいアクセス許可<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Enter the name of new DimAttribute[DimensionName] view created above in step 2 and set the <bpt id="p1">**</bpt>Access Level<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Read<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の手順 2 で作成した新しい DimAttribute[DimensionName] ビューの名前を入力し、<bpt id="p1">**</bpt>アクセス レベル<ept id="p1">**</ept> を<bpt id="p2">**</bpt>読み取り<ept id="p2">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Search for <bpt id="p1">**</bpt>Security Duty SysServerAXBasicMaintain<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティ職務権限 SysServerAXBasicMaintain<ept id="p1">**</ept> を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Right-click and choose <bpt id="p1">**</bpt>Create extension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>拡張機能の作成<ept id="p1">**</ept> を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Rename the extension as appropriate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて拡張機能の名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Drag-and-drop the newly created <bpt id="p1">**</bpt>Security Privilege<ept id="p1">**</ept> into the <bpt id="p2">**</bpt>Privileges list<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新たに作成された <bpt id="p1">**</bpt>セキュリティ特権<ept id="p1">**</ept> を <bpt id="p2">**</bpt>特権リスト<ept id="p2">**</ept> にドラッグ アンド ドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Right-click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> and select <bpt id="p2">**</bpt>View Code<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>コードの表示<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Add the following code to the view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビューに次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This will register it in the dimension framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、分析コード フレームワークに登録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Here is an example using the view created for CustTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustTable に対して作成されたビューを使用する例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Select <bpt id="p1">**</bpt>Microsoft Dynamics 365<ept id="p1">**</ept> and click <bpt id="p2">**</bpt>Options<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>オプション<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Select <bpt id="p1">**</bpt>Best Practices<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ベスト プラクティス<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Select your model and then scroll until you find <bpt id="p1">**</bpt>Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルを選択し、<bpt id="p1">**</bpt>Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker<ept id="p1">**</ept> が表示されるまでスクロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Verify that the rule and its children are selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールとその子が選択されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Build and then synchronize the view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビューをビルドしてから同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Step 2: Validate that the view returns the correct data in SQL</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 2: ビューが SQL で正しいデータを返すことを検証する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>At this point you should be able to run the following query in SQL Server Management Studio to ensure that it's pulling the correct data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点で SQL Server Management Studio で次のクエリを実行して、正しいデータが引き出されているかを確認をする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Here is an abbreviated example using the view created for CustTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustTable に対して作成されたビューを使用する省略例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>KEY_</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KEY_</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>VALUE</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>DATA AREA ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ範囲 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>PARTITION</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーティション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>RECID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RECID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>NAME</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>PARTITION #2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーティション 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>22565425322</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">22565425322</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>US<ph id="ph1">\_</ph>SI<ph id="ph2">\_</ph>0129</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">US<ph id="ph1">\_</ph>SI<ph id="ph2">\_</ph>0129</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>ussi</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ussi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>5637144576</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">5637144576</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>22565425322</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">22565425322</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Adventure Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Adventure Services</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>5637144576</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">5637144576</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>22565424579</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">22565424579</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>US<ph id="ph1">\_</ph>SI<ph id="ph2">\_</ph>0128</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">US<ph id="ph1">\_</ph>SI<ph id="ph2">\_</ph>0128</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>ussi</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ussi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>5637144576</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">5637144576</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>22565424579</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">22565424579</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Alpine Electronics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アルペン エレクトロニクス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>5637144576</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">5637144576</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Step 3: Override methods on the backing table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 3: バッキング テーブルでメソッドを上書きする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>To integrate with the dimensions framework when deleting or renaming the natural key of the backing table, you must write custom code on the backing table's delete method, and on either the update or renamePrimaryKey method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッキング テーブルのナチュラル キーを削除または名前を変更するときに分析コード フレームワークと統合するには、バッキング テーブルの delete メソッドと、update または renamePrimaryKey メソッドにカスタム コードを記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If your table blocks updates of the natural key, you will need to use the renamePrimaryKey override.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルがナチュラル キーの更新をブロックする場合、renamePrimaryKey のオーバーライドを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>If it does not, then you can put the code in the update method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">存在しない場合は、更新メソッドでコードを格納できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Here is an example from CustTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustTable からの例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Step 4: Clear caches to force detection of the new view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 4: キャッシュをクリアして新しいビューの検出を強制的する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Because the list of entities that can be consumed as a dimension are cached on the server, the creation of a new entity will not appear in the list of existing entities until a call to clear the caches is performed, or until both the client and the server are restarted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードとして消費できるエンティティのリストはサーバー上でキャッシュされるため、キャッシュをクリアする呼び出しが実行されるか、クライアントとサーバーの両方が再起動されるまで新しいエンティティの作成は既存のエンティティのリストに表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>To clear the caches and have the new view appear immediately, you must execute the following line of code within a runnable class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュをクリアして新しいビューをすぐに表示させるには、実行可能なクラス内で次のコード行を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Step 5: Verify that the dimension appears in the Use Value From lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 5: 分析コードが [ルックアップからの値を使用] に表示されることを確認する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Now that you have completed the steps, navigate to the <bpt id="p1">**</bpt>Financial dimensions<ept id="p1">**</ept> page in the General ledger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順を完了したら、総勘定元帳の<bpt id="p1">**</bpt>財務分析コード<ept id="p1">**</ept> ページに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Click the drop-down menu on the <bpt id="p1">**</bpt>Use Values from<ept id="p1">**</ept> field and verify that your value is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値の使用元<ept id="p1">**</ept>フィールドのドロップダウン メニューをクリックし、値が使用可能であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Add a new OMOperatingUnit type backed entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい OMOperatingUnit タイプがサポートしているエンティティの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>If a new Organization Model OMOperatingUnitType enumeration is added, the steps to make it consumable as a dimension are similar but can be made shorter as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい組織モデル OMOperatingUnitType 列挙が追加された場合、次元として使用可能にする手順は類似していますが、次のように短くすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Copy one of the existing DimAttributeOM[BackingTableName] views, rename it appropriately, and then adjust all associated labels and help text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の DimAttributeOM[BackingTableName] ビューの 1 つをコピーし、適切に名前を変更して、関連するすべてのラベルとヘルプ テキストを調整します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Expand the Datasource\BackingEntity (OMOperatingUnit)\Ranges node on the copied view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーしたビューで、Datasource\BackingEntity (OMOperatingUnit) \Ranges ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Change the value property on the range to the new OMOperatingUnitType enumeration value that was just added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">範囲内の値プロパティを、追加された新しい OMOperatingUnitType 列挙型に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Build and synchronize the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをビルドして同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Follow the steps in this topic starting with Step 2, where you validate the data in SQL, and then continue through Step 5, where you validate that the dimension appears in the <bpt id="p1">**</bpt>Use Value From<ept id="p1">**</ept> lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL でデータを検証するステップ２で始まるこのトピックの手順に従い、<bpt id="p1">**</bpt>値の使用<ept id="p1">**</ept>ルックアップで表示される分析コードを検証するステップ 5 まで続けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Because the <bpt id="p1">**</bpt>OMOperatingUnitType<ept id="p1">**</ept> is backed by the <bpt id="p2">**</bpt>OMOperatingUnit<ept id="p2">**</ept> table, generic code already exists to handle the delete, update, and <bpt id="p3">**</bpt>renamePrimaryKey<ept id="p3">**</ept> methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OMOperatingUnitType<ept id="p1">**</ept> は <bpt id="p2">**</bpt>OMOperatingUnit<ept id="p2">**</ept> テーブルによってサポートされているため、削除、更新および <bpt id="p3">**</bpt>renamePrimaryKey<ept id="p3">**</ept> メソッドを処理するための汎用コードがすでに存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Therefore, you do not need to update these methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらのメソッドを更新する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Step 6: Setting a dimension to be self-referenced</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 6: 自己参照される分析コードを設定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>If you also want to create an data entity for your new entity, and that entity has a reference to default dimensions, add this code to the persistEntity() method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいエンティティのデータ エンティティも作成し、そのエンティティが既定の分析コードへの参照を持っている場合、persistEntity() メソッドにこのコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>This ensures that if you also want the dimension to use itself as a default dimension value, the information is created in the correct sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、分析コードが自身を既定の既定値として使用するようにする場合、情報が正しい順序で作成されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>