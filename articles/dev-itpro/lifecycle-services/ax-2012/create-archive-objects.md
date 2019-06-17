<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-archive-objects.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-archive-objects.5602db.e31891d188146d98ae856f7d9a5c362132ba2507.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e31891d188146d98ae856f7d9a5c362132ba2507</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\create-archive-objects.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create archive objects for the Intelligent Data Management Framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intelligent Data Management Framework のアーカイブ オブジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to use archive objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、アーカイブ オブジェクトの使用方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create archive objects for the Intelligent Data Management Framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intelligent Data Management Framework のアーカイブ オブジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Overview of Archive Objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>An Archive Object is a hierarchical relationship tree that you create based on a driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトはドライバー テーブルに基づき作成した階層関係ツリーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The Archive Object archives transactional records from the production database, based on the rules and selection criteria you created in the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトは、アーカイブ オブジェクトで作成したルールおよび選択基準に基づいて、生産データベースからトランザクション レコードをアーカイブします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This topic refers to archiving as copying records from the production database to the archive database, and then deleting these records from the production database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、運用データベースからアーカイブ データベースにレコードをコピーし、運用データベースからこれらのレコードを削除することによってアーカイブを実施する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You can create an Archive Object based either on the templates that are included in IDMF or on the discovery process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF に含まれているテンプレート、または探索プロセスに基づき、アーカイブ オブジェクトを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To use this topic, you must have experience in the maintenance and administration of the Microsoft Dynamics AX application and database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックを使用するには、Microsoft Dynamics AX のアプリケーションとデータベースのメンテナンスと管理に精通している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>IDMF lets you create an Archive Object that defines a hierarchical relationship tree among the Microsoft Dynamics AX application tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF では、Microsoft Dynamics AX アプリケーション テーブル間の階層関係ツリーを定義するアーカイブ オブジェクトを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can then apply rules to select records based on specific criteria.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の条件に基づきレコードを選択するルールを適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Records matching the selection criteria from the whole relationship tree in the Archive Object are moved from the production database to the archive database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト内の関係ツリー全体から選択基準に一致するレコードは、生産データベースからアーカイブ データベースに移動されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Improper use of this framework can cause unexpected results, database corruption, and application downtime requiring full database and application recovery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフレームワークを不適切に使用すると、予期しない結果、データベース破損、データベース全体およびアプリケーションの復旧が必要となるアプリケーション ダウンタイムが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Exercise extreme caution, and thoroughly test your recycling strategy in a test environment before working in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境で作業する前に、十分に注意を払い、テスト環境でリサイクル戦略を入念にテストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Overview of the data archiving process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アーカイブ プロセスの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The archive function archives records by using a scheduled archive task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ機能により、スケジュールされているアーカイブ タスクを使用してレコードがアーカイブされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>At run time, an archive task completes these tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に、アーカイブ タスクはこれらのタスクを完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Select qualifying records from the driver table, based on rules that are defined for the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルに対して定義されているルールに基づいて、ドライバー テーブルから対象のレコードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Select qualifying records from all child tables, based on the parent-child relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">親子関係に基づいて、すべての子テーブルから対象のレコードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Copy the qualifying records from the production database to the archive database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のレコードを生産データベースからアーカイブ データベースにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Delete the qualifying records from the production database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">運用データベースから特定のレコードを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Considerations for Archive Objects, driver tables, relations, and rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト、ドライバー テーブル、関係、およびルールに関する注意事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Consider the following points when working with an Archive Object:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトで作業する場合は、次の点を考慮してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Verify that the table you select as the driver table for an Archive Object is a header table, such as <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトのドライバー テーブルとして選択したテーブルが、<bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> などのヘッダー テーブルであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>A good indication, although not always accurate, is that the <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> value for such a table is <bpt id="p2">**</bpt>WorkSheetHeader<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Miscellaneous<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>Transaction<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ずしもいつも正確ではありませんが、そのようなテーブルの <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> の値は、<bpt id="p2">**</bpt>WorkSheetHeader<ept id="p2">**</ept>、<bpt id="p3">**</bpt>Miscellaneous<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>Transaction<ept id="p4">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Tables with a <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> value of <bpt id="p2">**</bpt>Main<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Parameter<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Group<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>WorkSheetLine<ept id="p5">**</ept> cannot be driver tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> 値が <bpt id="p2">**</bpt>Main<ept id="p2">**</ept>、<bpt id="p3">**</bpt>Parameter<ept id="p3">**</ept>、<bpt id="p4">**</bpt>Group<ept id="p4">**</ept>、<bpt id="p5">**</bpt>WorkSheetLine<ept id="p5">**</ept> のテーブルをドライバー テーブルにすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The driver table becomes the root parent in the hierarchical relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルは、階層リレーションシップ ツリーのルート親になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>IDMF queries the <bpt id="p1">**</bpt>XRefTableRelation<ept id="p1">**</ept> table to determine the parent-child relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF は <bpt id="p1">**</bpt>XRefTableRelation<ept id="p1">**</ept> テーブルを照会して、親子関係を判別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Archiving records based on an Archive Object may cause data inconsistency in your application in these conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトに基づいてレコードをアーカイブすると、次の条件では、アプリケーションでデータの不整合が発生する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The driver table has known parent tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルには既知の親テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The driver table has known child tables that are not added to the Archive Object as a relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルには、アーカイブ オブジェクトにリレーションとして追加されていない既知の子テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Always minimize the Archive Object, and keep only necessary relations and rules for your implementations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常にアーカイブ オブジェクトを最小化し、実装に必要なルールおよび関係のみを保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Consider removing a table from the Archive Object in these conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件のアーカイブ オブジェクトからテーブルを削除することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The table does not contain any data, and it is not likely to contain data in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルにはデータが含まれておらず、将来もデータが含まれない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The table stores only transient data, such as <bpt id="p1">**</bpt>SalesParmTable<ept id="p1">**</ept> or <bpt id="p2">**</bpt>SpecTrans<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルには、<bpt id="p1">**</bpt>SalesParmTable<ept id="p1">**</ept> や <bpt id="p2">**</bpt>SpecTrans<ept id="p2">**</ept> などの一時データのみが格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The table stores open transactions, such as <bpt id="p1">**</bpt>CustTransOpen<ept id="p1">**</ept> or <bpt id="p2">**</bpt>VendTransOpen<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルには、<bpt id="p1">**</bpt>CustTransOpen<ept id="p1">**</ept> や <bpt id="p2">**</bpt>VendTransOpen<ept id="p2">**</ept> などの未処理のトランザクションが格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The table creates nested relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルはネストされたリレーションシップを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>If a table appears multiple times on different levels in the relationship tree, with the same qualifying relationship condition or set of primary keys, consider keeping the occurrence only in the lowest-numbered level in the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルが、同じ特定関係条件のもとまたは主キーのセットで、関係ツリー上の異なるレベルで複数回表示される場合、関係ツリーの最も低い番号のレベルでのみ表示されるように検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If a table is related to the driver table and makes its own Archive Object, it is a good candidate to be a driver table itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルがドライバー テーブルに関連していて、独自のアーカイブ オブジェクトを作成している場合、ドライバー テーブル自体にすることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For example, if you use <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> as a driver table, it discovers <bpt id="p2">**</bpt>PurchTable<ept id="p2">**</ept> for intercompany.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> をドライバー テーブルとして使用する場合、会社間の <bpt id="p2">**</bpt>PurchTable<ept id="p2">**</ept> が検出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In this case, consider making <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> a separate Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> を別のアーカイブ オブジェクトにすることを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>If the driver table and the child table are from different functional areas, and if the child table is a good candidate to be archived separately, create a separate, independent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルと子テーブルが異なる機能領域からのものである場合は、子テーブルが別々にアーカイブされるのに適している場合は、独独立したアーカイブ オブジェクトを個別に作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Consider making this child table a Related Archive Object in these conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの条件で、この子テーブルを関連するアーカイブ オブジェクトにすることを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>This driver table and its child table must be archived together because of functional or relational dependencies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このドライバー テーブルとその子テーブルは、機能的またはリレーショナルの依存関係のために一緒にアーカイブする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You have to add rules for correct archiving of the child table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子テーブルの正しいアーカイブのルールを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You can only add rules for the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルにはルールのみ追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To add rules for the child table, it has to be the driver table of a Related Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子テーブルのルールを追加するには、関連するアーカイブ オブジェクトのドライバー テーブルでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Be sure that the rules you add to the Related Archive Object do not adversely affect the archiving from the parent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連アーカイブ オブジェクトに追加するルールが親アーカイブ オブジェクトからのアーカイブに悪影響を及ぼさないようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>There may be multiple relationships between two tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つのテーブル間に複数のリレーションシップが存在することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In that case, evaluate the relationships and functionality carefully.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場合、リレーションシップと機能を慎重に評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>We recommend that you use only a single relationship in the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトでは単一のリレーションシップのみを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you can use multiple relationships if necessary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、必要に応じて、複数のリレーションシップを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Be sure to select a valid relationship using a unique index or primary key, if one exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なリレーションシップが存在する場合は固有インデックスまたは主キーを使用して、有効なリレーションシップを選択してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Do not use the archive templates that are included with IDMF to create your Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを作成する IDMF に含まれているアーカイブ テンプレートを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>These templates are created in a specific Microsoft Dynamics AX application and may not match your implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテンプレートは特定の Microsoft Dynamics AX アプリケーションで作成され、実装と一致しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Instead, use the discovery option to create your own objects, and compare them with the templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、検出オプションを使用して独自のオブジェクトを作成し、テンプレートと比較します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Tables in the templates may not be valid for your implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレート内のテーブルは、実装で有効でない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Some valid and known tables may not appear in your discovered object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な既知のテーブルには、検出されたオブジェクトに表示されないものがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Carefully analyze any difference between the objects you created through the discovery process and the templates, to determine the cause of the difference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探索プロセスで作成したオブジェクトおよびテンプレートの違いを慎重に分析し、その違いの原因を特定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Manually add or remove tables from the Purge Objects and Archive Objects to fit your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要件に合わせるために、削除オブジェクトとアーカイブ オブジェクトからテーブルを手動で追加または削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Be sure that relationships among tables are set correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル間の関係が正しく設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Be sure that the <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> property is set for all custom tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのカスタム テーブルに対して <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> プロパティが設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Verify that the relationship tree that you have created in the Archive Object archives the intended data from your system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトに作成したリレーションシップ ツリーがシステムから目的のデータをアーカイブしていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>An Archive Object that you create must look at all related records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成するアーカイブ オブジェクトは関連するすべてのレコードを検索する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Missing relationships lead to orphaned data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">不足している関係は、データの孤立を引き起こします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>A table in the relationship tree becomes part of the archive function and becomes disabled from the master data tables list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーのテーブルは、アーカイブ機能の一部となり、マスター データ テーブルのリストから無効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Thoroughly test the effect of your Archive Objects and your archive strategy on your database and application in a test environment that resembles your production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">運用環境に似たテスト環境で、アーカイブ オブジェクトとアーカイブ戦略がデータベースとアプリケーションに及ぼす影響を十分にテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Test all business processes, and obtain user sign-off before trying to implement the Archive Objects in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての業務プロセスをテストし、実稼働環境にアーカイブ オブジェクトを実装する前にユーザーの承認を得ます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Overview of Related Archive Objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するアーカイブ オブジェクトの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The relationship tree of an Archive Object can be very complex.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトのリレーションシップ ツリーは非常に複雑である場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In order to archive data from all the related tables, complex relationship trees have to be managed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての関連するテーブルからデータをアーカイブするためには、複雑なリレーションシップ ツリーを管理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In some cases, one relationship tree has to include another relationship tree to guarantee data integrity and functionally valid archiving of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、1 つのリレーションシップ ツリーに、データの整合性との機能的に有効なアーカイブを保証するために別のリレーションシップ ツリーを含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Due to this complexity, you can create a relationship between two independent Archive Objects by adding one Archive Object in the other Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複雑であるため、別のアーカイブ オブジェクトに 1 つのアーカイブ オブジェクトを追加することによって、2 つの独立したアーカイブ オブジェクト間の関係を作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The child Archive Object is called the Related Archive Object and forms a relationship with the parent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子アーカイブ オブジェクトは関連アーカイブ オブジェクトと呼ばれ、親アーカイブ オブジェクトとの関係を形成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>An archive task archives selected records from all the tables in the Archive Object and the Related Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ タスクは選択したレコードをアーカイブ オブジェクト内の全てのテーブルおよび関連するアーカイブ オブジェクトにアーカイブします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following steps provide a walkthrough of an Archive Object with a Related Archive Object:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順では、関連するアーカイブ オブジェクトを含むアーカイブ オブジェクトのチュートリアルを行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Use the Microsoft Dynamics AX Windows client to work with the Application Object Tree (AOT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX Windows クライアントを使用して、アプリケーション オブジェクト ツリー (AOT) を操作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>In the AOT, expand <bpt id="p1">**</bpt>Data Dictionary<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Tables<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>CustInvoiceSalesLink<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Relations<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT で、<bpt id="p1">**</bpt>データ ディクショナリ<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>テーブル<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>CustInvoiceSalesLink<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>リレーション<ept id="p4">**</ept>と展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The <bpt id="p1">**</bpt>CustInvoiceSalesLink<ept id="p1">**</ept> table has two parents, <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> and <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceSalesLink<ept id="p1">**</ept> テーブルには、2つの親 <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> および <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept> があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Expand the <bpt id="p1">**</bpt>Relations<ept id="p1">**</ept> node for the <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> テーブルの<bpt id="p1">**</bpt>関係<ept id="p1">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> table does not have a relationship with <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> in the AOT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> テーブルには、AOT の <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> との関係がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>In IDMF, click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Archive templates/Archive Object<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept> to open the <bpt id="p4">**</bpt>SalesTable<ept id="p4">**</ept> Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF で、<bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept> とクリックして <bpt id="p4">**</bpt>SalesTable<ept id="p4">**</ept> アーカイブ オブジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Review the hierarchical tree, and understand the parent-child relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層ツリーを確認し、親/子の関係を理解します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Notice that the <bpt id="p1">**</bpt>CustInvoiceSalesLink<ept id="p1">**</ept> table from step 1 is not in the relationship tree as a child of <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept>, even though the AOT shows a relationship between the two tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOT が 2 つのテーブル間の関係を示す場合でも、手順 1 の <bpt id="p1">**</bpt>CustInvoiceSalesLink<ept id="p1">**</ept> テーブルが <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> の子としてリレーションシップ ツリーにないことに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Notice that the relationship tree contains two oval shapes, named <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> and <bpt id="p2">**</bpt>CustPackingSlipJour<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーに、<bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> および <bpt id="p2">**</bpt>CustPackingSlipJour<ept id="p2">**</ept> という 2 つの楕円図形が含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>These oval shapes represent Related Archive Objects for <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの楕円形は、<bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> の関連アーカイブ オブジェクトを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A Related Archive Object is an Archive Object that is part of the relationship tree of a parent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するアーカイブ オブジェクトは、親アーカイブ オブジェクトのリレーションシップ ツリーの一部であるアーカイブ オブジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Double-click <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Notice that the <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> Archive Object opens and shows the <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> in a green rectangle next to the root table, <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> アーカイブ オブジェクトがルート テーブル <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept> の横にある緑色の長方形に <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> を開いて表示していることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The green rectangle highlights <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> as the parent Archive Object of the <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">緑の長方形は、<bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> アーカイブ オブジェクトの親アーカイブ オブジェクトとして <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> を強調表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>The <bpt id="p1">**</bpt>CustInvoiceSalesLink<ept id="p1">**</ept> table is a child table of the <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceSalesLink<ept id="p1">**</ept> テーブルには、子テーブル <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Double-click <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> to return to the parent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連アーカイブ オブジェクトを戻すには、<bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Right-click <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept>, and select <bpt id="p2">**</bpt>View relation<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>関係の表示<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>In the <bpt id="p1">**</bpt>Configure Related Archive Object<ept id="p1">**</ept> window, review the relationship between the <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> and <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept> tables, and then click <bpt id="p4">**</bpt>Close<ept id="p4">**</ept> to close the window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連するアーカイブ オブジェクトの構成<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> および <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept> テーブルの関係を確認してから、<bpt id="p4">**</bpt>閉じる<ept id="p4">**</ept>をクリックしてウィンドウを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In the <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> Archive Object, right-click <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept>, and select <bpt id="p3">**</bpt>Remove<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> アーカイブ オブジェクトで、<bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> を右クリックして<bpt id="p3">**</bpt>削除<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Confirm that the Related Archive Object <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> is removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するアーカイブ オブジェクト <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> が削除されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Right-click <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept>, and select <bpt id="p2">**</bpt>Add Related Archive Object<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>関連するアーカイブ オブジェクトの追加<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>In the <bpt id="p1">**</bpt>Configure Related Archive Object<ept id="p1">**</ept> window, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連するアーカイブ オブジェクトの構成<ept id="p1">**</ept>ウィンドウで、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In the <bpt id="p1">**</bpt>Select Related Archive Object<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連するアーカイブ オブジェクトの選択<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Click <bpt id="p1">**</bpt>New relation<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい関係<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In the <bpt id="p1">**</bpt>Configure relations for Related Archive Object<ept id="p1">**</ept> pane, enter SalesTable in the <bpt id="p2">**</bpt>Relation name<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連するアーカイブ オブジェクトの関係を構成<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>関係名<ept id="p2">**</ept>フィールドに SalesTable と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Enter a valid description in the <bpt id="p1">**</bpt>Relation description<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リレーションの説明<ept id="p1">**</ept>フィールドの有効な説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>In the <bpt id="p1">**</bpt>Configure relations<ept id="p1">**</ept> pane, use the following table to select fields, and then click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の構成<ept id="p1">**</ept>ウィンドウで、次のテーブルを使用してフィールドを選択してから<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>From the list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Select the value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値を選択</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><bpt id="p1">**</bpt>dataAreaId<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ領域 ID<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">**</bpt>Condition<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">**</bpt>Related table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source><bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">**</bpt>Related field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source><bpt id="p1">**</bpt>dataAreaID<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ領域 ID<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Click <bpt id="p1">**</bpt>New Relation<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい関係<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Using the previous step, use the <bpt id="p1">**</bpt>SalesID<ept id="p1">**</ept> field to create a relationship between the <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> and <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept> tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のステップを使用することで、<bpt id="p1">**</bpt>SalesID<ept id="p1">**</ept> を使用して、<bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> テーブルと <bpt id="p3">**</bpt>CustInvoiceJour<ept id="p3">**</ept> テーブル間にリレーションを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Verify that the <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> and <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> tables are related using the <bpt id="p3">**</bpt>DataAreaId<ept id="p3">**</ept> and <bpt id="p4">**</bpt>SalesID<ept id="p4">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>DataAreaId<ept id="p3">**</ept> フィールと <bpt id="p4">**</bpt>SalesID<ept id="p4">**</ept> フィールドを使用して、<bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> テーブルと <bpt id="p2">**</bpt>CustInvoiceJour<ept id="p2">**</ept> テーブルが関連していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> to return to the parent SalesTable Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>をクリックして親の SalesTable アーカイブ オブジェクトに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Verify that the SalesTable Archive Object contains the CustInvoiceJour Related Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SalesTable Archive Object オブジェクトに CustInvoiceJour Related Archive オブジェクトが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>In the <bpt id="p1">**</bpt>Save as<ept id="p1">**</ept> dialog box, type SalesTable<ph id="ph1">\_</ph>a, and then click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前を付けて保存<ept id="p1">**</ept>ダイアログ ボックスに、SalesTable<ph id="ph1">\_</ph>a と入力してから<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>You must save an Archive Object with a new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトは、新しい名前で保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> on the upper-right side of the relationship tree workspace, and pin the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> window to the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリー ワークスペースの右上にある<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウをワークスペースにピン留めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>In the relationship tree, right-click the <bpt id="p1">**</bpt>Related Archive Object CustInoviceJour<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、<bpt id="p1">**</bpt>関連するアーカイブ オブジェクト CustInoviceJour<ept id="p1">**</ept> をクリックしてから<bpt id="p2">**</bpt>削除<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, click <bpt id="p2">**</bpt>Revert<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで<bpt id="p2">**</bpt>元に戻す<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The revert action reverses the changes you have made since the last time you clicked <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元に戻す操作は、最後に<bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックした後に行った変更を元に戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>The revert action here brings back the Related Archive Object <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept>, because you did not click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept> after you removed the Related Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するアーカイブ オブジェクトを削除した後に <bpt id="p2">**</bpt>保存<ept id="p2">**</ept> をクリックしなかったため、ここでは、関連するアーカイブ オブジェクト <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> は元に戻す操作で戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Remove the Related Archive Object <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するアーカイブ オブジェクト <bpt id="p1">**</bpt>CustInvoiceJour<ept id="p1">**</ept> をもう一度削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Save the Archive Object as <bpt id="p1">**</bpt>SalesTable<ph id="ph1">\_</ph>deleted<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを <bpt id="p1">**</bpt>SalesTable<ph id="ph1">\_</ph>deleted<ept id="p1">**</ept> という名前で保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Archive templates/Archive Object<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Compare the icon of the SalesTable Archive Object with other objects in the list, and notice the difference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SalesTable アーカイブ オブジェクトのアイコンをリスト内の他のオブジェクトと比較し、その違いを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The icon indicates that you have opened the default template and saved it as an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアイコンは、既定のテンプレートを開いてアーカイブ オブジェクトとして保存したことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>You can only use an Archive Object, and not an archive template, in an archive task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ タスクでは、アーカイブ テンプレートではなく、アーカイブ オブジェクトのみを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Click <bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesTable<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Notice that IDMF opens the Archive Object you just saved as <bpt id="p1">**</bpt>SalesTable<ph id="ph1">\_</ph>deleted<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF が <bpt id="p1">**</bpt>SalesTable<ph id="ph1">\_</ph>deleted<ept id="p1">**</ept> として保存したアーカイブ オブジェクトを開くことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>IDMF lets you save multiple versions of the Archive Object and uses the most recently saved version of the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF を使用すると、複数のバージョンのアーカイブ オブジェクトを保存し、最も最近に保存したバージョンのアーカイブ オブジェクトを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Show versions<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>バージョンの表示<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>In the <bpt id="p1">**</bpt>Version history<ept id="p1">**</ept> window, select <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>Archive template<ept id="p3">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バージョン履歴<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> を<bpt id="p3">**</bpt>アーカイブ テンプレート<ept id="p3">**</ept> リストで選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that the <bpt id="p1">**</bpt>Archive Object<ept id="p1">**</ept> list displays the different versions of <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept>, with the most recent version at the top.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アーカイブ オブジェクト<ept id="p1">**</ept> リストに、さまざまなバージョンの <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> が上部にある最新バージョンとともに表示されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>An archive task uses the most recent version of the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ タスクはアーカイブ オブジェクトの最新のバージョンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>This walkthrough explained the concept of including a Related Archive Object in an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、あるアーカイブ オブジェクトに、関連するアーカイブ オブジェクトを含めるという概念について説明しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>You must understand the Microsoft Dynamics AX metadata and functionality thoroughly before working with an Archive Object or including a Related Archive Object in a parent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを操作したり、親アーカイブ オブジェクトに関連アーカイブ オブジェクトを含める前に、Microsoft Dynamics AX のメタデータと機能について十分に理解する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Understanding the Archive Object exception list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト例外リストを理解する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>IDMF lets you create an exception parameters list as detailed in a later section of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF を使用すると、このトピックの後半のセクションで説明する例外パラメーター リストを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>The exception parameters list applies globally to all purge templates, Purge Objects, archive templates, and Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外パラメーター リストは、すべての削除テンプレート、削除オブジェクト、アーカイブ テンプレート、およびアーカイブ オブジェクトにグローバルに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>In addition to the exception parameters list, IDMF lets you maintain an exception tables list specifically for Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外パラメータ一覧に加えて、IDMF により、特にアーカイブ オブジェクトに対する例外テーブル リストを管理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>When you create a new Archive Object and select the driver table, IDMF displays the Archive Object exception tables window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいアーカイブ オブジェクトを作成し、ドライバー テーブルを選択すると、IDMF にアーカイブ オブジェクト例外テーブル ウィンドウが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The exception list contains tables that you can use as driver tables to create a separate and independent Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外リストには、個別に独立したアーカイブ オブジェクトを作成するためのドライバー テーブルとして使用できるテーブルが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Carefully evaluate these tables to determine whether you want to include them in the relationship tree as related child tables or as Related Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテーブルを慎重に評価し、関連する子テーブルまたは関連するアーカイブ オブジェクトとしてリレーションシップ ツリーに含めるかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>The discovery process ignores all tables in the Archive Object exception tables list and does not include them in the relationship tree, even if a relationship exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスは、アーカイブ オブジェクト例外テーブル リスト内のすべてのテーブルを無視し、リレーションシップが存在する場合でも、それらをリレーションシップ ツリーに含めません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>To include a table from the Archive Object exception tables list, deselect the table, and click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> before you click <bpt id="p2">**</bpt>Continue<ept id="p2">**</ept> to begin the discovery process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト例外テーブルの一覧からテーブルを含めるには、テーブルの選択を解除し、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックしてから <bpt id="p2">**</bpt>続行<ept id="p2">**</ept> をクリックして検出プロセスを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>In this case, the discovery process includes the deselected table if a relationship exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、関係が存在する場合、検出プロセスに選択解除されたテーブルが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>You can also add other tables to the list and select to exclude the newly added table from the discovery process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、他のテーブルをリストに追加して、新規追加したテーブルを探索プロセスから除外するように選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Navigation of the Archive Object exception tables window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト例外テーブル ウィンドウのナビゲーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>The following tables provide descriptions for the controls in this window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルで、このウィンドウのコントロールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Panes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source><bpt id="p1">**</bpt>Main<ept id="p1">**</ept> window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メイン<ept id="p1">**</ept> ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Provides the driver table, and a list of exception tables for this driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブル、およびこのドライバー テーブルの例外テーブルの一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The list of exception tables changes, depending on the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外テーブルのリストは、ドライバー テーブルに応じて変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">**</bpt>Add new exception table<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい例外テーブルの追加<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Provides controls to add a table to the exception tables list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外テーブルの一覧にテーブルを追加するためのコントロールを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Buttons (main window)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン (主要なウィンドウ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source><bpt id="p1">**</bpt>Save<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Save the changes to the exception tables list, such as change to the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> field and any added tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept> フィールドの変更や追加されたテーブルなど、例外テーブルの一覧への変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source><bpt id="p1">**</bpt>Continue<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>続行<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Continue with the discovery process for the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトの探索プロセスを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Buttons (Add new exception tables pane)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン (新しい例外テーブル ウィンドウの追加)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source><bpt id="p1">**</bpt>Add<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Add the selected table to the exception tables list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外テーブル リストに選択したテーブルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>You must select a table in the <bpt id="p1">**</bpt>Table name<ept id="p1">**</ept> list before you click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>追加<ept id="p2">**</ept> をクリックする前に、<bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept> の一覧からテーブルを選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">**</bpt>Clear<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クリア<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Clear the <bpt id="p1">**</bpt>Table name<ept id="p1">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept>リストをクリアします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Fields (main window)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド (主要なウィンドウ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The name of the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブル名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source><bpt id="p1">**</bpt>Exception tables<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例外テーブル<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>The names of the exception tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Each table in the list can become a driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リスト内の各テーブルは、ドライバー テーブルになることが可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source><bpt id="p1">**</bpt>Status<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>A table with the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> field selected is not added to the relationship tree during the discovery process, even if a relationship exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept> フィールドが選択されたテーブルは、リレーションシップが存在していても、検索プロセス中にリレーションシップ ツリーに追加されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>If the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> field is not selected, the table is added to the relationship tree if there is a relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept> フィールドが選択されていない場合、リレーションシップが存在している場合、テーブルは検索プロセス中にリレーションシップ ツリーに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Modified by</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>The Windows ID of the user who changed the status of an existing table or added a new table to the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のテーブルのステータス変更、または新しいテーブルの一覧への追加を行ったユーザーの Windows ID。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Fields (Add exception list)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド (例外リストの追加)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select the table that you want to add to the exception tables list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外テーブルの一覧に追加するテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Create a new Archive Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいアーカイブ オブジェクトを作成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>You can create an Archive Object by selecting a driver table and creating a relationship tree based on the driver table, instead of selecting a template that is included with IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF に含まれるテンプレートを選択する代わりに、ドライバー テーブルを選択してドライバー テーブルに基づきリレーションシップ ツリーを作成することにより、アーカイブ オブジェクトを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Follow these steps to create a new Archive Object:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを作成するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Create Archive Object<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>アーカイブ オブジェクトの作成<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>In the <bpt id="p1">**</bpt>Create Archive Object<ept id="p1">**</ept> dialog box, select a table from the <bpt id="p2">**</bpt>Driver table<ept id="p2">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アーカイブ オブジェクトの作成<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>ドライバー テーブル<ept id="p2">**</ept> リストからテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>The list excludes tables from the exception parameters list, which is covered later in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストでは、このトピックの後半で説明する例外パラメーター リストからテーブルを除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Navigate to and select <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> に移動して選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>A driver table is the parent table that defines the relationship tree for a specific Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルは、特定のアーカイブ オブジェクトのリレーションシップ ツリーを定義する親テーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>In an Archive Object, the driver table may have child entities but does not have a parent entity in the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトでは、ドライバー テーブルに子エンティティがある場合がありますが、リレーションシップ ツリーに親エンティティはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>To continue, you must select the most unique index for the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するには、テーブルの最もユニークなインデックスを選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>This index is used to create the parent-child relationship in the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このインデックスは、アーカイブ オブジェクトに親子関係を作成するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the Unique keys field, select orderid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固有のキー フィールドで、orderid を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The <bpt id="p1">**</bpt>WMSOrderIdx<ept id="p1">**</ept> index is created by using the <bpt id="p2">**</bpt>orderid<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>WMSOrderIdx<ept id="p1">**</ept> インデックスは、<bpt id="p2">**</bpt>orderid<ept id="p2">**</ept> フィールドを使用して作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Click <bpt id="p1">**</bpt>Discover<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>検出<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>In the <bpt id="p1">**</bpt>Archive Object exception tables<ept id="p1">**</ept> dialog box, review the exception tables list carefully.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アーカイブ オブジェクト例外テーブル<ept id="p1">**</ept> ダイアログ ボックスで、例外テーブルの一覧を慎重に確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>If you want a table from the list to be included in the relationship tree, clear the <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストからテーブルを関係ツリーに含めるには、<bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept> フィールドをクリアします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Use the <bpt id="p1">**</bpt>Add new exception table<ept id="p1">**</ept> pane to add a new table to the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい例外テーブルを追加<ept id="p1">**</ept> ウィンドウを使用して、新しいテーブルをリストに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The <bpt id="p1">**</bpt>Status<ept id="p1">**</ept> field for the newly added table is selected by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく追加されたテーブルの <bpt id="p1">**</bpt>ステータス<ept id="p1">**</ept> フィールドは、既定で選択されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> to save your changes in the Archive Object exception tables window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックして、変更をアーカイブ オブジェクト例外テーブル ウィンドウに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept> to start the discovery process and create the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探索プロセスを開始し、アーカイブ オブジェクトを作成するには、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>The <bpt id="p1">**</bpt>Administer<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Discovery<ept id="p2">**</ept> command lets you maintain an exception parameters list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>検出<ept id="p2">**</ept> コマンドを使用すると、例外パラメーター リストを管理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>A table that belongs to the exception parameters list, with Archive discovery selected, is excluded from the relationship tree when the Archive Object is created, even if there is a relationship between the driver table and the excluded table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ検索が選択されている例外パラメーター リストに属しているテーブルは、ドライバー テーブルと除外さらたテーブルの間にリレーションシップがあっても、アーカイブ オブジェクトが作成されると、リレーションシップ ツリーから除外されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Using the metadata that is imported from the Microsoft Dynamics AX database, the exception parameters, and the Archive Object exception tables list, IDMF generates a hierarchical relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX データベースからインポートされるメタデータと、例外パラメーター、およびアーカイブ オブジェクト例外テーブル リストを使用して、IDMF は階層的なリレーション ツリーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>The relationship tree starts with the driver table, in level 0, and creates a hierarchy of parent-child relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーは 0 階でドライバー テーブルで始まり、親子関係の階層を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Make sure that your Archive Object resembles the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトが次のスクリーン ショットのようになっていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Do not save the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを保存しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>IDMF Archive Object Expanded</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開された IDMF アーカイブ オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>The relationship tree in this Archive Object is five levels deep.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアーカイブ オブジェクトのリレーションシップ ツリーは 5 階層の深さです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Level 0, the topmost level, contains the driver table, <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最上位レベルのレベル 0 には、ドライバー テーブル <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Level 1 contains the child entities of the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 1 には、ドライバー テーブルの子エンティティが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Level 2 contains child entities of tables in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 2 には、レベル 1 のテーブルの子エンティティが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>The last level, level 4, contains the child entities of tables in level 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 4 の最後のレベルには、レベル 3 のテーブルの子エンティティが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>This relationship tree is created based on the following data:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この関係ツリーは、以下のデータに基づいて作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>The Microsoft Dynamics AX metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX メタデータ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>The discovery process uses the metadata to create a list of related tables that form the parent-child hierarchy based on the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスは、メタデータを使用して、ドライバー テーブルに基づいて親子階層を形成する関連テーブルのリストを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>The exception parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外パラメーター。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Tables that belong to the exception parameters list are filtered out of the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外パラメーターの一覧に属しているテーブルは関係ツリーから除外されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Use the <bpt id="p1">**</bpt>Administer<ept id="p1">**</ept> menu to configure the exception parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept> メニューを使用して、例外パラメーターを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>The tables listed in the Archive Object exception tables dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトの例外テーブル ダイアログ ボックスに一覧表示されているテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>The tables you selected in this dialog box are also filtered out of the hierarchical relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このダイアログ ボックスで選択したテーブルは、階層的なリレーションシップ ツリーからも除外されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Tables that you configure as master tables by clicking <bpt id="p1">**</bpt>Administer<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Master data tables<ept id="p2">**</ept> are replicated from the production database to the archive database by a master data synchronization task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>マスター データ テーブル<ept id="p2">**</ept> をクリックしてマスター テーブルとして構成するテーブルは、マスター データ同期タスクによって実稼働データベースからアーカイブ データベースに複製されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>The relationship tree created by the discovery process may include tables that are configured as master tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスによって作成されたリレーションシップ ツリーには、マスター テーブルとして構成されたテーブルが含まれている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Verify the tables in the relationship tree, and remove any tables that must be treated as master tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーに含まれるテーブルを確認し、マスタ テーブルとして扱う必要があるテーブルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Right-click the table, and select <bpt id="p1">**</bpt>Add to data replicate<ept id="p1">**</ept> to remove the table from the relationship and configure it as a master data table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを右クリックし、<bpt id="p1">**</bpt>データ レプリケーションを追加<ept id="p1">**</ept> を選択して関係からテーブルを削除し、マスター データ テーブルとしてコンフィギュレーションします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>If you do not remove these tables, tables in the relationship tree are automatically removed from that master data synchronization list when you save the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテーブルを削除しない限り場合、関係ツリー内のテーブルは、アーカイブ オブジェクトを保存するときにマスター データの同期リストから自動的に削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Verify the relationship tree, and assess the functional effect of the tree on your Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーを検証し、Microsoft Dynamics AX アプリケーション上でそのツリーの機能的効果を評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>As a result of your assessment, you may have to manually add, modify, or remove some relations and rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価の結果として、一部の関係やルールを手動で追加、変更、または削除が必要となる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>For example, click <bpt id="p1">**</bpt>Show versions<ept id="p1">**</ept> to display the Archive Object from the default template that is included with IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>バージョンの表示<ept id="p1">**</ept>をクリックして、IDMF に含まれる既定のテンプレートからアーカイブ オブジェクトを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Compare the relationship tree from the template with the relationship tree you created in the previous procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の手順で作成したリレーションシップ ツリーとテンプレートのリレーションシップ ツリーを比較します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>The relationship tree in the <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> archive template differs from the <bpt id="p2">**</bpt>WMSOrder<ept id="p2">**</ept> Archive Object you created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> アーカイブ テンプレートのリレーションシップ ツリーは、作成した <bpt id="p2">**</bpt>WMSOrder<ept id="p2">**</ept> アーカイブ オブジェクトと異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>The difference is caused by the modification made to the default template, based on the functionality assessment of the Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この違いは、Microsoft Dynamics AX アプリケーションの機能評価に基づいて既定のテンプレートに加えられた変更によるものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>As demonstrated by this walkthrough, an Archive Object you create through discovery may not match the default template that is included with IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルが示すように、検索によって作成するアーカイブ オブジェクトは、IDMF に含まれる既定のテンプレートと一致しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Be careful with your selection of the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルの選択には注意が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>If you select a table such as <bpt id="p1">**</bpt>ProdTable<ept id="p1">**</ept>, the relationship tree can go many levels deep, spanning many tables on each level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdTable<ept id="p1">**</ept> などのテーブルを選択すると、各レベルの多数のテーブルにまたがっている数多くのレベルの関係ツリーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Such an Archive Object creates a complex relationship tree and increases the potential for error, and for resulting data corruption and application downtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなアーカイブ オブジェクトは、複雑な関係ツリーを作成して、エラーの可能性を高くし、結果としてデータの破損やアプリケーションのダウンタイムが生じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>The default template that is included with IDMF may not match the metadata of your Microsoft Dynamics AX implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF に含まれている既定のテンプレートは、Microsoft Dynamics AX 実装のメタデータと一致しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>A table in the default template that is not found in the metadata from the production database is marked invalid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産データベースのメタデータに見つからない既定テンプレートのテーブルは、無効とマークされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>An invalid table appears with a dotted red border, as shown in Figure 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">図 2 に示すように、無効なテーブルに赤い点線の枠線が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>You must remove invalid tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なテーブルは削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>When you use fields from valid tables to create relations and rules, IDMF validates those fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なテーブルのフィールドを使用してリレーションとルールを作成するとき、IDMF はこれらのフィールドを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>A field with a disabled configuration key is considered invalid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なコンフィギュレーション キーが設定されたフィールドは無効と見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>A valid table with invalid fields is shown with a yellow dotted border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なフィールドを持つ有効なテーブルは、黄色の点線の枠線で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>You must either remove valid tables with invalid rules from the relationship tree or fix the relationships before you can save the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを保存する前に、リレーションシップ ツリーから無効なルールを含む有効なテーブルを削除するか、またはリレーションシップを修正する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Navigation of the Create Archive Object workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトの作成ワークスペースのナビゲーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>The following tables provide descriptions for the controls in this workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルで、このワークスペースのコントロールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Panes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Relationship tree<ept id="p1">&lt;/strong&gt;</ept> pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>リレーションシップ ツリー<ept id="p1">&lt;/strong&gt;</ept> ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Provides a graphical view of all the tables in the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトにすべてのテーブルのグラフィック ビューを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>The following list provides controls and commands that you can use to navigate the relationship tree pane:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のリストでは、リレーションシップ ツリー ウィンドウを移動するために使用できるコントロールとコマンドを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>With the <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Level<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> slider, you can select a level and show only the tables at the selected and higher levels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>レベル<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> スライダーでは、レベルを選択して、選択したレベルおよび上位レベルにあるテーブルのみを表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>With the <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Zoom<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> slider, you can change the diagram size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>ズーム<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> スライダーでは、図のサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Right-click the driver table to work with the following commands:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを操作するドライバー テーブルを右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Add Related Archive Object<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to add a Related Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>関連アーカイブ オブジェクトを追加する<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックし、関連アーカイブ オブジェクトを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove all invalid tables<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to remove all invalid tables, together with all their related tables, from the nested hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なすべてのテーブルを、関連するすべてのテーブルとともに入れ子になった階層から削除するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>無効なテーブルをすべて削除する<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Right-click a child table to work with the following commands:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを操作する子テーブルを右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to remove the selected table from the level, and to remove its nested child tables from the hierarchical tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルをレベルから削除し、階層ツリーから入れ子になった子テーブルを削除するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>For example, the <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> table appears in level 2 and level 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> テーブルはレベル 2 とレベル 3 で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>If you right-click the table in level 2, and then select <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>, the table is removed from level 2, together with its nested child relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 2 のテーブルを右クリックし、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>を選択すると、レベル 2 からテーブルが、入れ子になった子関係と共に削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>The occurrence of the table remains intact in level 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの発生はレベル 3 のままです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Select all occurrences<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to display all occurrences of the selected table and its related tables in a dotted green border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>すべての発生を選択<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックすると、選択したテーブルとその関連テーブルのすべての出来事が緑色の点線の枠内に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>In this case, the table <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> is selected in levels 2 and 3, together with all its nested child relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、テーブル <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> は入れ子になった子関係すべてと共にレベル 2 と 3 で選択されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove all occurrences<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to remove all occurrences of the selected table and its related tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブル、およびその関連テーブルのすべての内容を削除するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>すべてを削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>In this case, the table <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> is removed from levels 2 and 3, together with all its nested child relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、テーブル <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> は入れ子になった子関係すべてと共にレベル 2 と 3 から削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>The removed tables appear in a gray shape with a solid red border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除されたテーブルが赤い実線の入った灰色の図形に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Click <bpt id="p1">&lt;span class="ui"&gt;</bpt><bpt id="p2">&lt;strong&gt;</bpt>Add to data replicate<ept id="p2">&lt;/strong&gt;</ept><ept id="p1">&lt;/span&gt;</ept> to remove the selected table from the relationship tree and add it to the master tables list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルをリレーション ツリーから削除し、マスター テーブル リストに追加するには、<bpt id="p1">&lt;span class="ui"&gt;</bpt><bpt id="p2">&lt;strong&gt;</bpt>データ複製に追加<ept id="p2">&lt;/strong&gt;</ept><ept id="p1">&lt;/span&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>This command performs these tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは次のタスクを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Remove the selected table, together with all its nested child tables, from the relationship tree of all existing Archive Objects and archive templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての既存のアーカイブ オブジェクトとアーカイブ テンプレートから、選択したテーブルをそのネストされた子テーブルすべてと共に削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Add the selected table to the <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Recommended tables<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> tab in the master data tables list (<bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>Administer<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p5">&lt;strong&gt;</bpt><bpt id="p6">&lt;span class="ui"&gt;</bpt>Master data tables<ept id="p6">&lt;/span&gt;</ept><ept id="p5">&lt;/strong&gt;</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター データ テーブル リストの<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>推奨テーブル<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> タブで選択したテーブルを追加します (<bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>管理<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p5">&lt;strong&gt;</bpt><bpt id="p6">&lt;span class="ui"&gt;</bpt>マスター データ テーブル<ept id="p6">&lt;/span&gt;</ept><ept id="p5">&lt;/strong&gt;</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Discover<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to regenerate the hierarchical parent-child relationship for the selected table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルの親子関係階層を再生成するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>検出<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>This command is available only when you select a table with the table group property of <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>WorkSheetHeader<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>WorkSheetHeader<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> というテーブル グループ プロパティを持つテーブルを選択した場合にのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>メモ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>A table with the symbol X in the top-right corner meets the row size or table size configuration in the Framework options window (<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Administer<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>Framework options<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅の記号 X があるテーブルは、フレームワーク オプション ウィンドウの行サイズ、またはテーブルサイズのコンフィギュレーションを満たしています (<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>管理<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>フレームワーク オプション<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Review these tables carefully to determine whether such tables have to be removed from the relationship and added to the master data tables list (<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Administer<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>Master data tables<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテーブルを慎重に確認し、関係から削除してマスター データ テーブル リストに追加する必要があるかどうかを判断します (<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>管理<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>マスター データ テーブル<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>To add a table to the master data tables list, right-click the table, and then select <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Add to data replicate<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター データ テーブルの一覧にテーブルを追加するには、テーブルを右クリックし、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>データ レプリケートに追加<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Properties<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>プロパティ<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Shows properties for the selected table and provides commands that you can use for the selected table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルのプロパティを表示し、選択したテーブルに使用できるコマンドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>When a table in the Archive Object contains multiple relations, you can use the <bpt id="p1">&lt;span class="ui"&gt;</bpt>Relations<ept id="p1">&lt;/span&gt;</ept> node in the tree view to disable one or more relations, as detailed later in this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト内のテーブルに複数のリレーションが存在するときは、ツリー ビューの <bpt id="p1">&lt;span class="ui"&gt;</bpt>Relations<ept id="p1">&lt;/span&gt;</ept> ノードを使用して、このセクションで後で詳しく説明しているように、1 つまたは複数のリレーションを無効にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove table<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>テーブルの削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Provides a data grid that you can use to select tables that you want to remove from the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ツリーから削除するテーブルを選択するために使用できるデータ グリッドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>This pane also provides an <bpt id="p1">&lt;span class="ui"&gt;</bpt>Advanced filter<ept id="p1">&lt;/span&gt;</ept> control that you can use to filter the data grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このペインには、データ グリッドをフィルタリングするために使用できる<bpt id="p1">&lt;span class="ui"&gt;</bpt>高度なフィルタ<ept id="p1">&lt;/span&gt;</ept>コントロールもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Related Information<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>関連情報<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Provides additional information for some of the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のテーブルの追加情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>If related information is provided, read it carefully to understand the archive relevance of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連する情報が指定された場合は、テーブルのアーカイブの妥当性を理解するために慎重に読んでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source><bpt id="p1">**</bpt>Remove<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Remove tables that are selected in the data grid in the <bpt id="p1">**</bpt>Remove table<ept id="p1">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブルの削除<ept id="p1">**</ept> ウィンドウのデータ グリッドで選択されているテーブルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>When you remove a table, all the child tables for the selected table are removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを削除すると、選択したテーブルのすべての子テーブルが削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>The removal spans the whole relationship tree, and all nested parent-child relations for the selected table's child tables are removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除すると、リレーションシップ ツリー全体が削除され、選択したテーブルの子テーブルのすべてのネストされた親子関係が削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source><bpt id="p1">**</bpt>Revert<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>元に戻す<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Reverse the modifications made to the Archive Object, back to the last save.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ対象に行われた変更を前回の変更まで戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>This resembles an "undo" command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、「元に戻す」コマンドに似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source><bpt id="p1">**</bpt>Show allShow selected<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>allShow を選択して表示<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Show all tables or selected tables, and toggle the label of the button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのテーブルまたは選択したテーブルを表示し、ボタンのラベルを切り替えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Removed tables appear in gray boxes with a solid red line around them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除されたテーブルが、周囲に赤い実線の入った灰色のボックスに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Fields (Remove table pane)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド (テーブルの削除ウィンドウ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source><bpt id="p1">**</bpt>Check boxes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チェック ボックス<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>Select tables that you want to remove from the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ツリーから削除するテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>The name of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source><bpt id="p1">**</bpt>Configuration key<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンフィギュレーション キー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>The configuration key of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルのコンフィギュレーション キー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source><bpt id="p1">**</bpt>Level<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レベル<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>The level of the table in the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリー内のテーブルのレベル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source><bpt id="p1">**</bpt>Row count<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>行数<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>The number of rows in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの行数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Walkthrough: Work with an Archive Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: アーカイブ オブジェクトの操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>This section provides a walkthrough for working with an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、アーカイブ オブジェクトの操作に関するチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>If you have not created the Archive Object already, create one.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを既に作成していない場合は、1 つを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>In the next dialog box, read the warning message carefully, and then click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のダイアログ ボックスで、警告メッセージを注意深く読んでから<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>In the <bpt id="p1">**</bpt>Save as<ept id="p1">**</ept> dialog box, enter <bpt id="p2">**</bpt>WmsOrder1<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Save<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前を付けて保存<ept id="p1">**</ept>ダイアログ ボックスに、<bpt id="p2">**</bpt>WmsOrder1<ept id="p2">**</ept> と入力してから<bpt id="p3">**</bpt>保存<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>Click the <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> table in the hierarchy diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層図の <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> テーブルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>Use the <bpt id="p1">**</bpt>Zoom<ept id="p1">**</ept> slider to change the diagram size so that you can read the table names easily.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ズーム<ept id="p1">**</ept> スライダーを使用して、テーブル名を簡単に読み取れるように図のサイズを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>In the relationship tree, move the mouse pointer over table <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> to see the information that is displayed in the tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、テーブル <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> にマウス ポインターを移動し、ツール ヒントに表示される情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>In the relationship tree, move the mouse pointer over the <bpt id="p1">**</bpt>1:N relationship description<ept id="p1">**</ept> above the <bpt id="p2">**</bpt>WMSOrderTrans<ept id="p2">**</ept> table to see the information that is displayed in the tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、<bpt id="p2">**</bpt>WMSOrderTrans<ept id="p2">**</ept> テーブルの上の <bpt id="p1">**</bpt>1:N 関係の説明<ept id="p1">**</ept>にマウス ポインターを移動し、ツール ヒントに表示される情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, expand each node in the tree view to see the information that is provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、ツリー ビューの各ノードを展開して指定されている情報を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>If the <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept> filter control does not show the selection criteria, click the <bpt id="p2">**</bpt>Advanced<ept id="p2">**</ept> filter arrow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>高度な<ept id="p1">**</ept>フィルター コントロールでの選択基準が表示されない場合、<bpt id="p2">**</bpt>高度な<ept id="p2">**</ept>フィルター矢印をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Type 1 in the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> field, and then click <bpt id="p2">**</bpt>Search<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レベル<ept id="p1">**</ept> フィールドに 1 と入力してから、<bpt id="p2">**</bpt>検索<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>This changes the grid to show only those tables that are in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、レベル 1 にあるテーブルのみが表示されるようにグリッドが変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Select the <bpt id="p1">**</bpt>WMSOrderTrans<ept id="p1">**</ept> table by selecting the check box next to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">横にあるチェック ボックスをオンにして <bpt id="p1">**</bpt>WMSOrderTrans<ept id="p1">**</ept> テーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, click <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで<bpt id="p2">**</bpt>削除<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Note that table <bpt id="p1">**</bpt>WMSOrderTrans<ept id="p1">**</ept> and all its child tables in levels 2, 3, and 4 are removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル <bpt id="p1">**</bpt>WMSOrderTrans<ept id="p1">**</ept> とそこのレベル 2、3、4 にあるすべての子テーブルは削除されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Click the <bpt id="p1">**</bpt>Show all<ept id="p1">**</ept> button in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウの<bpt id="p1">**</bpt>すべて表示<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>The diagram shows all the tables, with the removed tables in red lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">図にはすべてのテーブルが表示され、削除されたテーブルは赤い線で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Click <bpt id="p1">**</bpt>Revert<ept id="p1">**</ept> to restore the original Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>元に戻す<ept id="p1">**</ept>をクリックし、元のアーカイブ オブジェクトを復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>The diagram now reverts to the state it was in before you deleted <bpt id="p1">**</bpt>WMSOrderTrans<ept id="p1">**</ept> in step 8.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この図は、手順 8で <bpt id="p1">**</bpt>WMSOrderTrans<ept id="p1">**</ept> を削除する前の状態に戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Repeat steps 7, 8, and 9 to remove the tables again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 7、8、9 を繰り返して、もう一度テーブルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>All the removed tables appear in gray shapes with solid red lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての削除されたテーブルが赤い実線の入った灰色の図形に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Click <bpt id="p1">**</bpt>Show selected<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane to see the revised Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウ内の<bpt id="p1">**</bpt>選択項目の表示<ept id="p1">**</ept>をクリックし、改訂されたアーカイブ オブジェクトを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>Verify that the removed tables are not in the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除したテーブルがアーカイブ オブジェクトに存在しないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> in the dialog box to save the Archive Object with a new version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを新しいバージョンで保存するには、ダイアログボックスの<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>You must provide a unique name when you save an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを保存するときに、一意の名前を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>IDMF treats the saved Archive Object as a new version of the original Archive Object or archive template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF は、新しいバージョンの元のアーカイブ オブジェクトまたはアーカイブ テンプレートとして保存されているアーカイブ オブジェクトを扱います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Archive template/Archive Objects<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>WMSOrder<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>WMSOrder<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>Verify that the Archive Object diagram does not contain the tables you removed in step 11.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクト図に手順 11 で削除したテーブルが含まれていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>Switch between <bpt id="p1">**</bpt>Show all/Show<ept id="p1">**</ept> selected to confirm that the removed tables still appear in gray shapes with solid red lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべての表示/選択項目の表示<ept id="p1">**</ept> を切り替えて、削除したテーブルが赤い実線による灰色の形状に表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, click <bpt id="p2">**</bpt>Revert<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで<bpt id="p2">**</bpt>元に戻す<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>The Archive Object does not change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトは変化しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>The revert action cannot undo the changes, because the Archive Object has been saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトが保存されているため、元に戻す操作で変更を元に戻すことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Show versions<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>バージョンの表示<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>In the <bpt id="p1">**</bpt>Version history<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>WMSOrder<ept id="p2">**</ept> from the list, and select the version of the Archive Object in the Archive Object list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バージョン履歴<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>WMSOrder<ept id="p2">**</ept> をリストから選択し、アーカイブ オブジェクト リストでアーカイブ オブジェクトのバージョンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Each version of the Archive Object is saved with a unique name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトの各バージョンは、一意の名前で保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Therefore, each Archive Object in the list provides a different version of <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、リストの各アーカイブ オブジェクトは、異なるバージョンの <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>Select the last item in the list, <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Show<ept id="p2">**</ept> to restore the Archive Object to the first version that is included as the archive template in IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧で最後の項目 <bpt id="p1">**</bpt>WMSOrder<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>表示<ept id="p2">**</ept> をクリックしてアーカイブ オブジェクトを IDMF にアーカイブ テンプレートとして含まれている最初のバージョンに復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>The restored Archive Object differs from the Archive Object you started working with in step 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元されたアーカイブ オブジェクトは、手順 1 で作業を開始したアーカイブ オブジェクトとは異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>The relationship tree in the default archive template has been adjusted based on the functional assessment of the Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のアーカイブ テンプレートのリレーションシップ ツリーは、Microsoft Dynamics AX アプリケーションの機能評価に基づいて調整されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to overwrite the object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトを上書きするには、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>In the <bpt id="p1">**</bpt>Save as<ept id="p1">**</ept> dialog box, enter the name for the Archive Object, and then click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前を付けて保存<ept id="p1">**</ept>ダイアログ ボックスで、アーカイブ オブジェクトの名前を入力してから<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to close the message indicating the success or failure of the save operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存操作の成功または失敗を示すメッセージを閉じるには、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>Keep the Archive Object open, because it is also used in the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでも使用するため、アーカイブ オブジェクトを開いたままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Archive templates/Archive Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ テンプレート/アーカイブ オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>This command provides a list of archive templates and Archive Objects in your system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、システム内のアーカイブ テンプレートとアーカイブ オブジェクトのリストを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>An archive template is a template that is included with IDMF with a predefined relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ テンプレートとは事前定義されたリレーションシップ ツリーで IDMF に含まれているテンプレートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>You can use an archive template as a starting point to create an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出発点としてアーカイブ テンプレートを使用し、アーカイブ オブジェクトを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>You must review an archive template to make sure that it meets your requirements, and save it before you can use it in a scheduled archive task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スケジュールされたアーカイブ タスクの使用前に、要件を満たしているかどうか確認するためにアーカイブ テンプレートを確認して保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>This command uses the same navigation and toolbar commands as the <bpt id="p1">**</bpt>Create Archive Object<ept id="p1">**</ept> workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、<bpt id="p1">**</bpt>アーカイブ オブジェクトの作成<ept id="p1">**</ept>ワークスペースと同じナビゲーションおよびツールバー コマンドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Walkthrough: Work with an archive template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: アーカイブ テンプレートの操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>This section provides a walkthrough for working with an archive template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、アーカイブ テンプレートの操作に関するチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Archive templates/Archive Object<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>Observe the icon of the <bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> テンプレートのアイコンを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Select <bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから <bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>Review the tables, table properties, and relationship tree to understand how the data archiving for <bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> cascades through the relationship tree in the archive template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、テーブルのプロパティ、関係ツリーを確認し、<bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> のデータ アーカイブがアーカイブ テンプレートの関係ツリーを通じてカスケードする方法を理解します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Make sure that this relationship tree covers your application and any customizations you may have made to the Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリレーションシップ ツリーに、アプリケーションと、Microsoft Dynamics AX アプリケーションに対して行ったすべてのカスタマイズが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>You must provide a unique name when you save an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを保存するときに、一意の名前を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>Change the name to BankChequeTable<ph id="ph1">\_</ph>object to identify this saved object as an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を BankChequeTable<ph id="ph1">\_</ph> オブジェクトに変更し、この保存されたオブジェクトをアーカイブ オブジェクトとして識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> in the dialog box to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するにはダイアログ ボックスで <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Archive templates/Archive Objects<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>You do not see <bpt id="p1">**</bpt>BankChequeTable<ph id="ph1">\_</ph>object<ept id="p1">**</ept> in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストの <bpt id="p1">**</bpt>BankChequeTable<ph id="ph1">\_</ph>オブジェクト<ept id="p1">**</ept> が表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>Unlike Purge Objects, Archive Objects are saved with the same name, but with a new version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パージ オブジェクトとは異なり、アーカイブ オブジェクトは同じ名前で保存されますが、新しいバージョンで保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>In this case, the <bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> object is created with a version name <bpt id="p2">**</bpt>BankChequeTable<ph id="ph1">\_</ph>object<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> オブジェクトはバージョン名 <bpt id="p2">**</bpt>BankChequeTable<ph id="ph1">\_</ph>object<ept id="p2">**</ept> で作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>As always, the latest version is effective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、最新バージョンは有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>Notice that the icon of <bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> is changed compared to earlier, which indicates that it is saved as an object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BankChequeTable<ept id="p1">**</ept> のアイコンが以前と比較して変わっていると、オブジェクトとして保存されることを示しています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>