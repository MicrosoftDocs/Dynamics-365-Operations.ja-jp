<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cdx-extensibility.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cdx-extensibility.7abe0b.1a346c6831556f7f23fb92dbdc78a89c786af2e7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1a346c6831556f7f23fb92dbdc78a89c786af2e7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\cdx-extensibility.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Enable custom Commerce Data Exchange synchronization via extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を介したカスタム Commerce Data Exchange 同期の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can extend the Retail initialization class to support custom Commerce Data Exchange (CDX) synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Retail 初期化クラスを拡張して、カスタムの Commerce Data Exchange (CDX) 同期をサポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Enable custom Commerce Data Exchange synchronization via extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を介したカスタム Commerce Data Exchange 同期の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how you can extend the Retail initialization class to support custom Commerce Data Exchange (CDX) synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Retail 初期化クラスを拡張して、カスタムの Commerce Data Exchange (CDX) 同期をサポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For this extension, you use the new extension points that were added in Microsoft Dynamics 365 for Finance and Operations platform update 8 or Microsoft Dynamics 365 for Retail platform update 8.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この拡張機能では、Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 8 または Microsoft Dynamics 365 for Retail プラットフォーム更新プログラム 8 で追加された新しい拡張ポイントを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>CDX is a system that transfers data between Retail headquarters (Retail HQ) and retail channels, such as online stores or brick-and-mortar stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX は、小売用バックオフィス (小売 HQ)、およびオンライン ストア、実際の店舗などの小売チャンネルの間でデータを転送するシステムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data transfer between Retail HQ and the channel database is controlled by scheduler jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail HQ とチャネル データベース間のデータ転送は、スケジューラ ジョブによって制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Each scheduler job contains a list of scheduler subjobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各スケジューラ ジョブには、スケジューラ サブジョブの一覧が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The scheduler subjobs contain the names of the source tables and destination tables, and the transfer field mapping of those tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スケジューラ サブジョブには、ソース テーブルと出力先テーブルの名前と、それらのテーブルの転送フィールド マッピングが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>There are two ways to configure the data synchronization between Retail HQ and the channel database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail HQ とチャネル データベース間のデータ同期を設定するには、2 つの方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Configure all the custom jobs and subjobs by using the configuration user interface (UI) for CDX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX のコンフィギュレーション ユーザー インターフェイス (UI) を使用して、すべてのカスタム ジョブとサブジョブをコンフィギュレーションします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Extend the Retail initialization class by using the extension points that are provided to support custom jobs and subjobs for both push and pull.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プッシュおよびプルの両方のカスタム ジョブとサブジョブをサポートするために用意されている拡張子ポイントを使用して、Retail 初期化クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The advantage of using the Retail initialization class is that you don't have to configure the custom jobs in different environments (dev, test, and production).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 初期化クラスを使用する利点は、さまざまな環境 (開発、テスト、および実稼働) でカスタム ジョブを構成する必要がないことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Instead, you can run the retail CDX initialization by using the <bpt id="p1">**</bpt>Initialize retail scheduler<ept id="p1">**</ept> dialog box from <bpt id="p2">**</bpt>Retail &gt; Headquarters setup &gt; Retail scheduler &gt;Initialize retail scheduler<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p2">**</bpt>Retail &gt; 本社の設定 &gt; 小売用スケジューラ &gt; 小売用スケジューラの初期化<ept id="p2">**</ept>から<bpt id="p1">**</bpt>小売用スケジューラの初期化<ept id="p1">**</ept>ダイアログ ボックスを使用して、小売 CDX 初期化を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Information about the custom job for the data synchronization is then automatically created in CDX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの同期のためのカスタム ジョブに関する情報は CDX で自動的に作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>There are various scenarios for data transfer between Retail HQ and the channel database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail HQ とチャネル データベース間のデータ転送には、さまざまなシナリオがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Send data from a new Retail HQ table to a new channel database table by using a download job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロード ジョブを使用して新しい Retail HQ テーブルから新しいチャンネル データベース テーブルにデータを送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Pull data from a new channel database table to a new Retail HQ table by using a push job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プッシュ ジョブを使用して新しい Retail HQ テーブルに新しいチャンネル データベース テーブルからのデータを取り込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Send data from a new Retail HQ table to a new channel database table by using a download job</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロード ジョブを使用して新しい Retail HQ テーブルから新しいチャンネル データベース テーブルにデータを送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Before you push or pull data, you must understand various metadata definitions in the XML resource file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをプッシュまたはプルする前に、XML リソース ファイルのさまざまなメタデータ定義を理解する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The resource file contains the custom job information that will be initialized in your environment to push and pull data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソース ファイルには、データのプッシュやプルを実行する環境で初期化されるカスタム ジョブ情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Here is a list of the resource files that you must configure:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションする必要があるリソース ファイルの一覧を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>ChannelDBSchema<ept id="p1">**</ept> – The extension schema that you created in the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ChannelDBSchema<ept id="p1">**</ept> - チャンネル データベースで作成した拡張スキーマです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>TargetTableSchema<ept id="p1">**</ept> – The extension schema that you created in the channel database to add your custom tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TargetTableSchema<ept id="p1">**</ept> – カスタム テーブルを追加するチャンネル データベースで作成した拡張スキーマ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>AxTableName<ept id="p1">**</ept> – The table name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AxTableName<ept id="p1">**</ept> - テーブル名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>IsUpload<ept id="p1">**</ept> – A flag that determines whether the job is a push job or a pull job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IsUpload<ept id="p1">**</ept> – ジョブがプッシュ ジョブかプル ジョブかを判断するフラグ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>(In other words, the flag indicates whether you want to send data from Retail HQ to the channel database or pull data from the channel database to Retail HQ).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(つまり、フラグは、Retail HQ からチャンネル データベースにデータを送信するか、チャンネル データベースから Retail HQ にデータをプルするかを示します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The default value is <bpt id="p1">**</bpt>false<ept id="p1">**</ept>, which indicates that you're sending data from Retail HQ to the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値は <bpt id="p1">**</bpt>false<ept id="p1">**</ept> で、Retail HQ からチャネル データベースにデータを送信していることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>ScheduledByJob<ept id="p1">**</ept> – This resource file contains one or more subjobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ScheduledByJob<ept id="p1">**</ept> – このリソース ファイルには、1 つ以上のサブジョブが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Subjob<ept id="p1">**</ept> – Each table is added as a subjob, and each subjob is scheduled by one or more scheduler jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブジョブ<ept id="p1">**</ept> – 各テーブルは、サブジョブとして追加され、各サブジョブは 1 つまたは複数のスケジューラ ジョブによってスケジュールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>TargetTable<ept id="p1">**</ept> – The name of the channel database table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TargetTable<ept id="p1">**</ept> – チャンネル データベース テーブルの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This table is the target table that the push job or pull job must send data to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルは、プッシュ ジョブまたはプル ジョブのデータの送り先となるターゲット テーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>If a value isn't specified, the system assumes that name of the target table and the name of the source table are the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が指定されていない場合、ターゲット テーブルの名前とソース テーブルの名前が同じになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If you created a new Retail HQ table and a new channel database table, follow these steps to push the data between the two tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Retail HQ テーブルと新しいチャンネル データベース テーブルを作成した場合は、2 つのテーブル間でデータをプッシュするためのこれらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Create a custom project and use the Application Object Tree (AOT) to add a custom table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム プロジェクトを作成し、アプリケーション オブジェクト ツリー (AOT) を使用してカスタム テーブルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Create a new resource file to add all custom job information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのカスタム ジョブ情報を追加する新しいリソース ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Here is the template for the resource file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソース ファイルのテンプレートを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Use the AOT to create a new XML resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT を使用して新しい XML リソースを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In the XML file for the resource, specify the new table and new job details, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソースの XML ファイルで、次の例に示すように新しいテーブルと新しいジョブの詳細を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>[NOTE] You can either add the new table as part of the existing job, or create a new job and add this table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[注記] 新規テーブルを既存のジョブの一部として追加するか、または新しいジョブを作成してからこのテーブルを追加するかのいずれかを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In this case, we are creating a new job, where the job ID is <bpt id="p1">**</bpt>7000<ept id="p1">**</ept> and the custom table is named <bpt id="p2">**</bpt>ContosoRetailSeatingArrangementData<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、ジョブ ID が <bpt id="p1">**</bpt>7000<ept id="p1">**</ept> で、カスタムのテーブルに <bpt id="p2">**</bpt>ContosoRetailSeatingArrangementData<ept id="p2">**</ept> と名前が付けられている場合、新しいジョブを作成しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>By default, the name of the target table isn't specified here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、ターゲット テーブルの名前がここでは指定されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The system assumes the name of the target table on the channel side is the same as the name of the source table on the Finance and Operations side (<bpt id="p1">**</bpt>AXTableName<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムでは、チャネル側のターゲット表の名前が Finance and Operations 側のソース テーブルの名前 (<bpt id="p1">**</bpt>AXTableName<ept id="p1">**</ept>) と同じであることが前提です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>However, the name of the target table on the channel side might sometimes differ from the name of the source table on the Finance and Operations side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、チャンネル側のターゲット テーブルの名前は、時に Finance and Operations 側にあるソース テーブルの名前とは異なる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this case, in the <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Subjob<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> node, you can use the <bpt id="p2">**</bpt><ph id="ph3">&amp;lt;</ph>TargetTableName<ph id="ph4">&amp;gt;</ph><ept id="p2">**</ept> attribute to set the name of the target table on the channel side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>サブジョブ<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> ノードで <bpt id="p2">**</bpt><ph id="ph3">&amp;lt;</ph>TargetTableName<ph id="ph4">&amp;gt;</ph><ept id="p2">**</ept> 属性を使用してチャネル側でターゲット テーブルの名前を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Similarly, in the mapping section, only the names of fields on the Finance and Operations side are specified (<bpt id="p1">**</bpt>AxFields<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、マッピング セクションでは、Finance and Operations 側にあるフィールドの名前だけが指定されています (<bpt id="p1">**</bpt>AxFields<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>By default, it's assumed that the same field name is also used on the channel side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、同じフィールド名がチャネル側でも使用されていると想定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>However, the field name on the corresponding channel table might sometimes differ from the field name on the Finance and Operations side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、対応するチャンネル テーブルのフィールド名は、時に Finance and Operations 側にあるフィールド名とは異なる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, in the mapping, you can use the <bpt id="p1">**</bpt>ToName<ept id="p1">**</ept> attribute of the <bpt id="p2">**</bpt><ph id="ph1">&amp;lt;</ph>Field<ph id="ph2">&amp;gt;</ph><ept id="p2">**</ept> node to set the name of the field on the channel side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、マッピングで <bpt id="p2">**</bpt><ph id="ph1">&amp;lt;</ph>フィールド<ph id="ph2">&amp;gt;</ph><ept id="p2">**</ept> ノードの <bpt id="p1">**</bpt>ToName<ept id="p1">**</ept> 属性を使用してチャネル側でフィールドの名前を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Right-click the project, and then select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>New Item<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>新しい項目<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In the <bpt id="p1">**</bpt>Add New item<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Resources<ept id="p2">**</ept>, name the resource file <bpt id="p3">**</bpt>RetailCDXSeedDataAX7_Custom<ept id="p3">**</ept>, and then select <bpt id="p4">**</bpt>Add<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい項目の追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>リソース<ept id="p2">**</ept>を選択し、リソース ファイルに <bpt id="p3">**</bpt>RetailCDXSeedDataAX7_Custom<ept id="p3">**</ept> と名前を付けてから、<bpt id="p4">**</bpt>追加<ept id="p4">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Add a new item</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい品目の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In the <bpt id="p1">**</bpt>Select a Resource file<ept id="p1">**</ept> dialog box, find the resource file that you created in step 2, and then select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リソース ファイルの選択<ept id="p1">**</ept>ダイアログ ボックスで、手順 2 で作成したリソース ファイルを検索し、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Add a new class that should be used to handle the <bpt id="p1">**</bpt>registerCDXSeedDataExtension<ept id="p1">**</ept> event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>registerCDXSeedDataExtension<ept id="p1">**</ept> イベントを処理するために使用する新しいクラスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Search for the <bpt id="p1">**</bpt>RetailCDXSeedDataBase<ept id="p1">**</ept> class, and then open it in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailCDXSeedDataBase<ept id="p1">**</ept> クラスを検索し、デザイナーで開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Right-click the <bpt id="p1">**</bpt>registerCDXSeedDataExtension<ept id="p1">**</ept> delegate, and then select <bpt id="p2">**</bpt>Copy event handler<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>registerCDXSeedDataExtension<ept id="p1">**</ept> デリゲートを右クリックし、<bpt id="p2">**</bpt>イベント ハンドラーをコピー<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Go to the event handler class that you created and paste the following event handler code into it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したイベント ハンドラー クラスに移動して、次のイベント ハンドラー コードを貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>[NOTE] Because there are two definitions for CDX seed data in the system, you must specify that your extension CDX seed data should be added only if the CDX seed data that is being generated is the version that you're trying to extend.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[注記] システムに CDX シード データに対して 2 つの定義があるため、生成する CDX シード データが拡張の対象のバージョンである場合にのみ、拡張 CDX データが追加されるように指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>If the <bpt id="p1">**</bpt>if<ept id="p1">**</ept> condition is removed, your extension CDX seed data could also be applied on top of the N-1 CDX seed data and cause unintended results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>if<ept id="p1">**</ept> 条件が削除されている場合、拡張 CDX シード データが N-1 CDX シード データの上にも適用され、意図しない結果が生じる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>You don't have to create separate resource files for the various scenarios that are mentioned later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で言及されるさまざまなシナリオの個別のリソース ファイルを作成する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>You can have one file that contains all the custom job information and register that file from the extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのファイルにすべてのカスタム ジョブ情報を含め、拡張機能クラスからそのファイルを登録することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Whenever the Retail initialization class runs, it looks for any extension that implements this handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 初期化クラスが実行されるときはいつでも、このクラスはこのハンドラーを実装する拡張機能を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>If an extension is found, the runtime will also initialize the custom information that is found in the resource file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子が見つかった場合、ランタイムはリソース ファイルに含まれるカスタム情報も初期化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Navigate to <bpt id="p1">**</bpt>Retail &gt; Headquarters setup &gt; Retail scheduler &gt;Initialize retail scheduler<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail &gt; 本社の設定 &gt; 小売用スケジューラ &gt; 小売用スケジューラの初期化<ept id="p1">**</ept>と移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the Retail CDX initialization by clicking the OK button on <bpt id="p1">**</bpt>Initialize retail scheduler<ept id="p1">**</ept> dialog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売用スケジューラの初期化<ept id="p1">**</ept> ダイアログをクリックして、Retail CDX の初期化を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Pull data from a new channel database table to a new Retail HQ table by using a push job</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プッシュ ジョブを使用して新しい Retail HQ テーブルに新しいチャンネル データベース テーブルからのデータを取り込む</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>To pull data from a new channel table to Retail HQ, you have two options:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいチャネル テーブルから小売用バックオフィスにデータを引き出すには、次の 2 つの方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Create a new resource file and add the new resource to the event handler as a second line, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここに示すように、新しいリソース ファイルを作成し、新しいリソースを 2 行目のイベント ハンドラーに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Update the existing resource file with the new information, so that you don't have to add a new line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい行を追加しなくて済むように、新しい情報を含む既存のリソース ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>To upload you set the <bpt id="p1">**</bpt>IsUpload<ept id="p1">**</ept> attribute to <bpt id="p2">**</bpt>true<ept id="p2">**</ept> in the resource file and add information about your custom pull job, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップロードするには、次の例に示すように、リソース ファイルの <bpt id="p1">**</bpt>IsUpload<ept id="p1">**</ept> 属性を <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に設定し、カスタム プルジョブに関する情報を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>[NOTE] You can either add this new table as part of the existing pull job (P-1000) or create a new pull job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[注記] この新規テーブルを既存のプル ジョブ (P-1000) の一部として追加するか、または新しいプル ジョブを作成するかのいずれかを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Other scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のシナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>For the remaining push and pull scenarios, only the information for the sample resource file is described, because initialization is the same as we described in the previous sections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">残りのプッシュとプル シナリオでは、サンプル リソース ファイルの情報のみが記載されます。それは前のセクションの説明にあるように、初期化が同じであるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Push existing columns that aren't mapped as part of any subjobs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のサブジョブの一部としてマップされていない既存の列をプッシュ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>You can push the existing unmapped column to either new extension columns or existing columns in the channel database, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例で示すように、マッピングされていない既存の列を、新しい拡張列またはチャンル データベース内の既存の列のいずれかにプッシュすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>If the table has a primary key that isn't <bpt id="p1">**</bpt>RecId<ept id="p1">**</ept>, your extension table on the channel side should also contain the non-<bpt id="p2">**</bpt>RecId<ept id="p2">**</ept> primary keys, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに <bpt id="p1">**</bpt>RecId<ept id="p1">**</ept> ではない主キーがある場合、次の例に示されるように、チャンネル側の拡張子テーブルに 非 <bpt id="p2">**</bpt>RecId<ept id="p2">**</ept> 主キーも含まれる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Pull new columns to an existing table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい列を既存のテーブルにプルする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If you add new columns and want to pull in part of the existing table, use the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい列を追加して既存のテーブルの一部を取得する場合は、次のコードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Move an existing subjob to another subjob</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のサブジョブへの既存のサブジョブの移動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>To move an existing subjob to another job, you can change the <bpt id="p1">**</bpt>ScheduledByJob<ept id="p1">**</ept> attribute in the resource file and it is run as part of the event handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のサブジョブを別のジョブに移動するには、リソース ファイルの <bpt id="p1">**</bpt>ScheduledByJob<ept id="p1">**</ept> 属性を変更することができます。この属性はイベント ハンドラの一部として実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>CDX sample - Pull new columns to an existing table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX サンプル - 新しい列を既存のテーブルにプルする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>In Microsoft Dynamics 365 for Retail App update 5, we added a new sample in RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables, it has all the sample SQL scripts, ax project files for different CDX extension scenarios, please use it as a reference for different CDX extension scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail アプリケーション更新プログラム 5 では、RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables に新しいサンプルが追加され、そこにすべてのサンプル SQL スクリプト、さまざまな CDX 拡張機能シナリオの ax プロジェクト ファイルがありますが、さまざまな CDX 拡張機能シナリオの参照として使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the next sections, we discuss the steps and best practices for customizing Retail transactional tables by using extension tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、拡張テーブルを使用して Retail トランザクション テーブルをカスタマイズする手順とベスト プラクティスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Another section shows how to customize CDX to upload the customized (extension) tables on the channel side back to Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もう 1 つのセクションでは、CDX をカスタマイズしてチャネル側のカスタマイズされた (拡張子) テーブルを Finance and Operations にアップロードする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>We have also included a section that describes how to test the customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタマイズのテスト方法を説明するセクションも含めました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Setup steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>We recommend that you implement these changes on an untouched Retail software development kit (SDK).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更していない Retail ソフトウェア開発キット (SDK) にこれらの変更を実装することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Alternatively, you can put the SDK under source control, such as Microsoft Azure DevOps, so that you can easily revert your changes at any step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、SDK を Microsoft Azure DevOps などのソース管理下で配置することにより、どのステップでも変更を簡単に元に戻すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>To begin, you import the .axpp package that is located in the SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まず、SDK にある .axpp パッケージをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>You then run the SQL update script on your channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、チャンネル データベースで、SQL 更新スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Import the package on the Finance and Operations side that contains the customization code:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ コードを含む Finance and Operations 側にパッケージをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Copy the ExtensionTablesAndCDXCustomization.axpp file from the RetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables   folder and paste in your extension project folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExtensionTablesAndCDXCustomization.axpp ファイルをRetailSDK\Documents\SampleExtensionsInstructions\ExtensionTables フォルダーからコピーし、拡張プロジェクト フォルダーに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Start Microsoft Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Select <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Import project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>インポート プロジェクト<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In the <bpt id="p1">**</bpt>Import project<ept id="p1">**</ept> dialog box, specify the path of the .axpp file you copied in step 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトのインポート<ept id="p1">**</ept> ダイアログ ボックスで、手順 1 でコピーした .axpp ファイルのパスを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Select either <bpt id="p1">**</bpt>Current solution<ept id="p1">**</ept> or <bpt id="p2">**</bpt>New solution<ept id="p2">**</ept>, according to your preference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、<bpt id="p1">**</bpt>現在のソリューション<ept id="p1">**</ept> または <bpt id="p2">**</bpt>新しいソリューション<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to begin to import the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択してパッケージのインポートを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>After the import is completed, you have the files in Solution Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートが完了した後、ソリューション エクスプローラーにファイルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Build the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Right-click the project, and then select <bpt id="p1">**</bpt>Synchronize database<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>データベースの同期<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Run the SQL update script:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL 更新スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Copy the <bpt id="p1">**</bpt>ContosoRetailExtensionTablesUpdate.sql<ept id="p1">**</ept> file from the Retail SDK folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK フォルダーから <bpt id="p1">**</bpt>ContosoRetailExtensionTablesUpdate.sql<ept id="p1">**</ept> ファイルをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>You can run the other sample files in a similar manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様の仕方で他のサンプル ファイルを実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Open the script in Microsoft SQL Server Browser, and run the script against your channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server ブラウザーでスクリプトを開いて、チャネル データベースに対してスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>This step creates the extension tables and views that are required in order to customize the transactional tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップでは、トランザクション テーブルをカスタマイズするために必要な拡張テーブルとビューを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Note that the script also creates other tables that are used for other sample scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトはその他のサンプル シナリオに使用されるその他のテーブルも作成することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Extend the Finance and Operations data in the sample</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプルの Finance and Operations データを拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The table extension on the Finance and Operations side is already created in the sample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations 側のテーブル拡張は、サンプルですでに作成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>To create it manually, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動で作成するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Start Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>On the menu, select <bpt id="p1">**</bpt>View<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニューで、<bpt id="p1">**</bpt>表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Select <bpt id="p1">**</bpt>Data Model<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Tables<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>RetailTransactionTable<ept id="p3">**</ept>, right-click <bpt id="p4">**</bpt>RetailTransactionTable<ept id="p4">**</ept>, and then select <bpt id="p5">**</bpt>Create extension<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ モデル<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>テーブル<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>RetailTransactionTable<ept id="p3">**</ept> を選択し、<bpt id="p4">**</bpt>RetailTransactionTable<ept id="p4">**</ept> を右クリックして <bpt id="p5">**</bpt>拡張機能を作成<ept id="p5">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>As a best practice, you should change the default name to something like <bpt id="p1">**</bpt>RetailTransactionTable.ContosoRetailExtension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスは、デフォルトの名前を次のように変更する必要があります <bpt id="p1">**</bpt>RetailTransactionTable.ContosoRetailExtension<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Always add your unique prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に一意の接頭語を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>In this sample, <bpt id="p1">**</bpt>ContosoRetail<ept id="p1">**</ept> is used as a unique prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルでは、<bpt id="p1">**</bpt>ContosoRetail<ept id="p1">**</ept> が一意の接頭語として使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>By using a unique prefix, you help prevent naming conflicts if a table is extended by multiple independent software vendors (ISVs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一意の接頭語を使用することにより、複数の独立系ソフトウェア ベンダー (ISV) によってテーブルが拡張されている場合、名前の競合を防ぐことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>In the new <bpt id="p1">**</bpt>RetailTransactionTable.ContosoRetailExtension<ept id="p1">**</ept> table, create two new fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい <bpt id="p1">**</bpt>RetailTransactionTable.ContosoRetailExtension<ept id="p1">**</ept> テーブルで、2 つの新しいフィールドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source><bpt id="p1">**</bpt>Type=string, name=ContosoRetailServerStaffId<ept id="p1">**</ept>: Set the <bpt id="p2">**</bpt>Extended data type<ept id="p2">**</ept> property to <bpt id="p3">**</bpt>RetailStaffId<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイプ = 文字列、名前 =ContosoRetailServerStaffId<ept id="p1">**</ept>: <bpt id="p2">**</bpt>拡張データ型<ept id="p2">**</ept>プロパティを <bpt id="p3">**</bpt>RetailStaffId<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source><bpt id="p1">**</bpt>Type=int, name=ContosoRetailSeatNumber<ept id="p1">**</ept>: Set the <bpt id="p2">**</bpt>Extended data type<ept id="p2">**</ept> property to <bpt id="p3">**</bpt>ContosoRetailSeatNumber<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイプ = 整数、名前 =ContosoRetailSeatNumber<ept id="p1">**</ept>: <bpt id="p2">**</bpt>拡張データ型<ept id="p2">**</ept>プロパティを <bpt id="p3">**</bpt>ContosoRetailSeatNumber<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Save the changes, and build your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を保存し、プロジェクトをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Right-click your project, and then select <bpt id="p1">**</bpt>Synchronize the database<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>データベースの同期<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>NOTE: As a best practice, the unique prefix is added to the new column names to help prevent future naming conflicts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注記: ベスト プラクティスとして、今後の名前の競合を回避するために新しい列名に固有の接頭語が追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>A naming conflict can occur if another ISV creates a column that has the same name, or if Microsoft releases an update that uses a column that has the same name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の ISV が同じ名前を持つ列を作成する場合、または Microsoft が同じ名前を持つ列を使用する更新プログラムをリリースする場合、名前付けの競合が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Even though the extension table is created in a different AOT asset, the new columns are added to the original table in SQL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張テーブルでは異なる AOT 資産に作成されますが、新しい列は SQL の元のテーブルに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Extend the database on the channel side</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル側にあるデータベースを拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>From the Retail SDK folder, open and run the SQL Server <bpt id="p1">**</bpt>ContosoRetailExtensionTablesUpdate.sql<ept id="p1">**</ept> script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK フォルダーから SQL Server <bpt id="p1">**</bpt>ContosoRetailExtensionTablesUpdate.sql<ept id="p1">**</ept> スクリプトを開いて実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Several items are created and configured:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の品目が作成され、コンフィギュレーションされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The <bpt id="p1">**</bpt>[ext].ContosoRetailTransactionTable<ept id="p1">**</ept> table that has the foreign key and custom (extension) fields is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部キーとカスタム (拡張子) フィールドを含む <bpt id="p1">**</bpt>[ext].ContosoRetailTransactionTable<ept id="p1">**</ept> テーブルが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>In addition to the extension columns that we added in the tables, the extension table on the channel side must have the same primary key columns as the original table on the channel side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに追加した拡張列に加えて、チャネル側の拡張テーブルにはチャネル側にある元のテーブルと同じ主キー列が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Therefore, [ext].RetailTransactionTable_ContosoRetailExtension has the four primary key columns that are used in [ax].RetailTransactionTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、[ext].RetailTransactionTable_ContosoRetailExtension には、[ax].RetailTransactionTable で使用される 4 つの主キー列があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>As a best practice, when you add the primary key columns to the extension table on the channel side, keep the names of the columns the same as the names of the primary key column on the original table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスは、チャンネル側の拡張子テーブルに主キー列を追加するときに、列の名前を元のテーブルの主キー列の名前と同じにしておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>CDX is configured to upload and pull the custom columns from the channel extension table back to Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDXは、チャネル拡張テーブルのカスタム列をアップロードして Finance and Operations に戻すように構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The RetailCDXSeedDataAX7 resource contains the information for the table mapping from Finance and Operations to the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailCDXSeedDataAX7 リソースには、Finance and Operations からチャネル データベースへのテーブル マッピングの情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>CDX uses this information to create the required data transfer scheduler jobs and subjobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX はこの情報を使用して、必要なデータ転送スケジューラのジョブとサブジョブを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>To include your new extension tables or columns in the data transfer, you must provide a resource file that specifies the customization for the CDX data transfer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ転送に新しい拡張テーブルまたは列を含めるには、CDX データ転送のカスタマイズを指定するリソース ファイルを提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>As a best practice, use the following naming convention to prevent conflicts: <bpt id="p1">**</bpt>RetailCDXSeedDataAX7_ContosoRetailExtension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスは、競合を防ぐため次のような名前付け規則を使用します。 <bpt id="p1">**</bpt>RetailCDXSeedDataAX7_ContosoRetailExtension<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>(Here, <bpt id="p1">**</bpt>ContosoRetail<ept id="p1">**</ept> is your unique extension.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ここでは、<bpt id="p1">**</bpt>ContosoRetail<ept id="p1">**</ept> は、固有の拡張機能です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>The sample CDX resource file in the Retail SDK contains additional customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK のサンプル CDX リソース ファイルには、追加のカスタマイズが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>However, for our example of RetailTransactionTable extension, the section in the following code is the only section that is required to pull data from the channel side back to Retail HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、RetailTransactionTable 拡張子の例では、次のコードのセクションは、チャンネル側から Retail HQ にデータを引き出すために必要な唯一のセクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source><bpt id="p1">**</bpt>Description  of the fields used in this resource file:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>このリソース ファイルで使用されるフィールドの説明:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source><bpt id="p1">**</bpt>ChannelDBSchema='ext'<ept id="p1">**</ept> – This field is included so that the resource reads from the extension schema in the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ChannelDBSchema ='ext'<ept id="p1">**</ept> - リソースがチャンネル データベース内の拡張スキーマから読み取るように、このフィールドが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source><bpt id="p1">**</bpt>Subjob Id="RetailTransactionTable"<ept id="p1">**</ept> – You must make sure that the SubJob ID is the same as the orginal subjob id for that table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブジョブ ID ="RetailTransactionTable"<ept id="p1">**</ept> – SubJob ID がそのテーブルの元のサブジョブ ID と同じであることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>so that the extensibility framework can determine that you're customizing the existing subjob.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうすると、拡張性フレームワークはユーザーが既存のサブジョブをカスタマイズすることを判断することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>If you use new subjob di, system will throw duplicate subjob error for the same table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいサブジョブ di を使用すると、同じテーブルに対してサブジョブの重複エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">**</bpt>TargetTableName ="CONTOSORETAILTRANSACTIONTABLE"<ept id="p1">**</ept> - Your channel extension table name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TargetTableName = "CONTOSORETAILTRANSACTIONTABLE"<ept id="p1">**</ept> - チャンネル拡張子のテーブル名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><bpt id="p1">**</bpt>TargetTableSchema="ext"<ept id="p1">**</ept> - Your channel extension schema.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TargetTableSchema="拡張"<ept id="p1">**</ept> - チャンネル拡張子スキーマ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Currently we support the extension schema name only as ext.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のところ、拡張子スキーマ名は外部としてのみサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source><bpt id="p1">**</bpt>OverrideTarget="false"<ept id="p1">**</ept> - For upload subjobs (the ones that bring data from the channel to the headquarters), OverrideTarget when set to "false" will tell CDX that the table defined by TargetTableName is an extension table and data will be uploaded along with the primary table already defined in the subjob.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OverrideTarget ="false"<ept id="p1">**</ept> - アップロード サブジョブ (チャンネルから本社にデータを取り込むもの) の場合、OverrideTarget が false に設定されていると、TargetTableName で定義されたテーブルが拡張テーブルであり、サブジョブで既に定義されているプライマリ テーブルに沿ってデータがアップロードされることが CDX に通知されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If OverrideTarget is set to "true" the table defined by TargetTableName will override the primary table for the subjob (default value fields will be omitted during the pull job and only the extension fields will be considered).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OverrideTarget が "true" に設定されている場合、TargetTableName で定義されたテーブルはサブジョブのプライマリ テーブルをオーバーライドします (プル ジョブでは既定値フィールドが省略され、拡張フィールドのみが考慮されます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>For instance, in this sample, if you set this value to true, this would mean that instead of uploading the data from ax.RetailTransactionTable, CDX would only upload the data from ext.CONTOSORETAILTRANSACTIONTABLE.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、このサンプルでは、この値を true に設定する場合は、これは ax.RetailTransactionTable からデータをアップロードするのではなく、CDX は ext.CONTOSORETAILTRANSACTIONTABLE からのデータのみをアップロードすることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The <bpt id="p1">**</bpt>AxTableName<ept id="p1">**</ept> attribute isn't specified, because the framework can already determine the <bpt id="p2">**</bpt>AxTableName<ept id="p2">**</ept> value that the specified subjob uses as a sink.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたサブジョブがシンクとして使用する <bpt id="p2">**</bpt>AxTableName<ept id="p2">**</ept> 値をフレームワークが既に判断できるので、<bpt id="p1">**</bpt>AxTableName<ept id="p1">**</ept> 属性は指定されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>You only have to specify the differences when you customize the RetailCDXSeedDataAX7 resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailCDXSeedDataAX7 リソースをカスタマイズする場合は、相違点を指定するだけで済みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Any data that the framework can infer doesn't have to be added by extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワークが推定できるすべてのデータは、拡張機能により追加する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Similarly, in the <ph id="ph1">&lt;AXFields&gt;</ph>&lt;/AXFields? section, you can see that we specified only the custom or new fields, because the extensibility framework can determine the list of remaining fields from the specified subjob ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、<ph id="ph1">&lt;AXFields&gt;</ph>&lt;/AXFields? セクションでは、カスタム フィールドまたは新しいフィールドのみ指定されているのがわかります。拡張フレームワークにより、指定されたサブジョブ ID からの残りのフィールドのリストが決まるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The CDX module that has the CDX customization resource is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX カスタマイズ リソースを持つ CDX モジュールが更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>To apply the customization that is specified in RetailCDXSeedDataAX7_ContosoRetailExtension, you must subscribe to the registerCDXSeedDataExtension delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailCDXSeedDataAX7_ContosoRetailExtensionで指定されているカスタマイズを適用するには、registerCDXSeedDataExtension デリゲートを購読する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>By subscribing to this event, you help guarantee that the customization is applied when initialization of the CDX seed data is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このイベントをサブスクライブすることで、CDX シード データの初期化が実行されるときにカスタマイズが適用されることを保証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Subscribe to the registerCDXSeedDataExtension delegate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">registerCDXSeedDataExtension デリゲートにサブスクライブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Select <bpt id="p1">**</bpt>View<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Search for the <bpt id="p1">**</bpt>RetailCDXSeedDataBase<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailCDXSeedDataBase<ept id="p1">**</ept> クラスを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Right-click the class, and then select <bpt id="p1">**</bpt>Open in designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスを右クリックし、<bpt id="p1">**</bpt>デザイナーで開く<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In the designer, in the list of delegates and methods, select the <bpt id="p1">**</bpt>registerCDXSeedDataExtension<ept id="p1">**</ept> delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーのデリゲートおよびメソッドの一覧で、<bpt id="p1">**</bpt>registerCDXSeedDataExtension<ept id="p1">**</ept> デリゲートを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Right-click, and then select <bpt id="p1">**</bpt>Copy event handler<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>イベント ハンドラーのコピー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The method signature that you must implement is copied, so that CDX picks up the customized resource for CDX seed data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装する必要があるメソッド シグネチャがコピーされるため、CDX は CDX シード データのカスタマイズされたリソースを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Create a new class, and give it a name, such as <bpt id="p1">**</bpt>ContosoRetailCDXSeedDataAX7EventHandler<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスを作成し、<bpt id="p1">**</bpt>ContosoRetailCDXSeedDataAX7EventHandler<ept id="p1">**</ept> などの名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>You can specify any name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の名前を指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>However, as a best practice, be sure to prefix the class name with your prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ベスト プラクティスとしては、接頭語をクラス名の前に付けてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Paste the code that you copied in step 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 5 でコピーしたコードを貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>The CDX extensibility framework calls this method when you select the Retail initialization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX 機能拡張フレームワークは、Retail の初期化を選択するとこのメソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To help guarantee that the CDX extensibility module uses the CDX customization, paste the following code into the preceding method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX 拡張モジュールが CDX カスタマイズを使用するようにするためには、上記のメソッドに次のコードを貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Before you add your custom resource to the list, you must verify that the originalCDXSeedDataResource resource that is being processed is RetailCDXSeedDataAX7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム リソースをリストに追加する前に、処理中の originalCDXSeedDataResource リソースが RetailCDXSeedDataAX7 であることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Otherwise, you might cause unintended results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうしないと、予期しない結果が生じる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>To initialize or reinitialize the CDX module with the customized configuration, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズした構成で CDX モジュールを初期化または再初期化するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>Scheduler jobs<ept id="p4">**</ept><ph id="ph4"> &gt; </ph><bpt id="p5">**</bpt>Initialize retail scheduler<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>スケジューラ ジョブ<ept id="p4">**</ept><ph id="ph4"> &gt; </ph><bpt id="p5">**</bpt>小売用スケジューラの初期化<ept id="p5">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>In the dialog box that appears, select <bpt id="p1">**</bpt>Delete existing configuration<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるダイアログ ボックスで、<bpt id="p1">**</bpt>既存のコンフィギュレーションの削除<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to start the initialization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択して、初期化を開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>When the initialization is completed, the CDX scheduler jobs, subjob definitions, and distribution schedules are updated by using the original RetailCDXSeedDataAX7 resource and the customized RetailCDXSeedDataAX7_ContosoRetailExtension resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化が完了したとき、CDX スケジューラ ジョブ、サブジョブの定義、および配布スケジュールは、元の RetailCDXSeedDataAX7 リソースとカスタマイズされた RetailCDXSeedDataAX7_ContosoRetailExtension リソースを使用して更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Test the customization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズのテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Verify that your customization works correctly:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズが正しく動作することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>After the initialization is completed, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept>, and then select the <bpt id="p4">**</bpt>Scheduler subjobs<ept id="p4">**</ept> link.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初期化が完了した後、<bpt id="p1">**</bpt>小売<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept>、<bpt id="p4">**</bpt>スケジューラ サブジョブ<ept id="p4">**</ept> リンクに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>On the subjobs table, search for the <bpt id="p1">**</bpt>RetailTransactionTable<ept id="p1">**</ept> subjob ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブジョブ テーブルで、<bpt id="p1">**</bpt>RetailTransactionTable<ept id="p1">**</ept> サブジョブ ID を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>On the <bpt id="p1">**</bpt>Set up<ept id="p1">**</ept> FastTab, verify that the <bpt id="p2">**</bpt>Channel table name<ept id="p2">**</ept> field is set to <bpt id="p3">**</bpt>[ext].RetailTransactionTableView<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>チャネル テーブル名<ept id="p2">**</ept>フィールドが <bpt id="p3">**</bpt>[ext].RetailTransactionTableView<ept id="p3">**</ept> に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>In the details section, in the <bpt id="p1">**</bpt>Channel field mapping<ept id="p1">**</ept> section, verify that the new custom (extension) columns are listed in the mapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細セクションの<bpt id="p1">**</bpt>チャネル フィールド マッピング<ept id="p1">**</ept> セクションで、新しいカスタム (拡張) 列がマッピングに表示されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Test that the CDX job will upload and pull from the original and extension tables on the channel side by using their unified view:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDX ジョブがアップロードし、統合されたビューを使用してチャンネル側にある元のテーブルと拡張テーブルから取得するテスト:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Create some transactions in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) でいくつかのトランザクションを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Because the extension table isn't used in the Commerce Runtime (CRT) and MPOS, you must manually insert data into the extension table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張テーブルは Commerce Runtime (CRT) および MPOS では使用されないため、拡張テーブルに手動でデータを挿入する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Run the following script after you change the required values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な値を変更した後、次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Repeat this step for the other transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のトランザクションにもこの手順を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Don't add corresponding data in [ext].[CONTOSORETAILTRANSACTIONTABLE] for some of the transactions that you created in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS で作成したトランザクションの一部 [ext].[CONTOSORETAILTRANSACTIONTABLE] に対応するデータを追加しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>In this way, you can verify that the data from [ax].RetailTransactionTable is pulled and uploaded even if there is no corresponding data in the extension table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、拡張テーブルに対応するデータがない場合でも、[ax].RetailTransactionTable からデータを取得してアップロードすることを確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Go to <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Retail<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Retail IT<ept id="p3">**</ept>, and then select <bpt id="p4">**</bpt>Distribution schedule<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>小売<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>小売 IT<ept id="p3">**</ept> の順に移動し、<bpt id="p4">**</bpt>配送スケジュール<ept id="p4">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>In the list of distribution schedules, select <bpt id="p1">**</bpt>P-0001<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送スケジュールの一覧で、<bpt id="p1">**</bpt>P-0001<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>This distribution schedule contains the RetailTransactionTable subjob that you customized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この配布スケジュールには、カスタマイズした RetailTransactionTable のサブジョブが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>When the confirmation message appears, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">確認メッセージが表示されたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>History<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>History<ept id="p2">**</ept> page, where you can verify that the uploaded session was completed successfully.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>履歴<ept id="p1">**</ept>を選択し<bpt id="p2">**</bpt>履歴<ept id="p2">**</ept>ページを開き、アップロードされたセッションが正常に完了したことを確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>On the <bpt id="p1">**</bpt>History<ept id="p1">**</ept> page, verify that there is a new upload session record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>履歴<ept id="p1">**</ept>ページで、新しいアップロード セッション レコードがあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Also verify that the status of the record is set to <bpt id="p1">**</bpt>Applied<ept id="p1">**</ept>, and that the <bpt id="p2">**</bpt>Rows Affected<ept id="p2">**</ept> value isn't <bpt id="p3">**</bpt>0<ept id="p3">**</ept> (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードのステータスが<bpt id="p1">**</bpt>申請済<ept id="p1">**</ept>に設定され、さらに<bpt id="p2">**</bpt>影響を受けた行<ept id="p2">**</ept>値は<bpt id="p3">**</bpt>0<ept id="p3">**</ept> (ゼロ) でないことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>If the upload session is applied successfully, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Inquiries and reports<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Retail store transactions<ept id="p3">**</ept>, and search for the new transactions that you just uploaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップロード セッションが正常に適用されていると、<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>照会やレポート<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>小売店舗のトランザクション<ept id="p3">**</ept>の順に移動し、アップロードした新しいトランザクションを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Verify that the transactions, seat number, and server staff ID custom columns have the expected values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション、シート番号、およびサーバー スタッフ ID の各カスタム列に期待された値が入っていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Additionally, verify that the transactions that don't have a corresponding record in the [ext].ContosoRetailTransactionTable extension table on the channel side are also uploaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、チャネル側の [ext].ContosoRetailTransactionTable 拡張テーブルに対応するレコードを持たないトランザクションもアップロードされていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Verify that these transactions have default values for the seat number and server staff ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのトランザクションにシート番号とサーバー スタッフ ID の既定値が含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>The seat number should be set to <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero), and the server staff ID should be set to <bpt id="p2">**</bpt>000160<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シート番号は <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (ゼロ) に設定し、サーバー スタッフ ID は <bpt id="p2">**</bpt>000160<ept id="p2">**</ept> に設定する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>