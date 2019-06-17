<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-purge-objects.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-purge-objects.d7ce61.bbf251403e2928302688d4a3d525d22f0c958642.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bbf251403e2928302688d4a3d525d22f0c958642</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\create-purge-objects.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create purge objects for the Intelligent Data Management Framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intelligent Data Management Framework の削除オブジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to create IDMF purge objects that define hierarchical relationship trees among application tables in Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics AX のアプリケーション テーブル間で階層関係ツリーを定義する IDMF パージ オブジェクトを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create purge objects for the Intelligent Data Management Framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intelligent Data Management Framework の削除オブジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Considerations for Purge Objects, driver tables, relations, and rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクト、ドライバー テーブル、関係、およびルールに関する注意事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: Before you use Purge Objects, you must have experience in the maintenance and administration of the Microsoft Dynamics AX application and database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: 削除オブジェクトを使用する前に、Microsoft Dynamics AX アプリケーションとデータベースのメンテナンスと管理に精通している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>IDMF lets you create a Purge Object that defines a hierarchical relationship tree among the Microsoft Dynamics AX application tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF では、Microsoft Dynamics AX アプリケーション テーブル間の階層関係ツリーを定義する削除オブジェクトを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can then apply rules to selected records based on specific criteria.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の条件に基づき選択したレコードにルールを適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Records matching the selection criteria are deleted from the whole relationship tree in the Purge Object when a purge task runs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択基準に一致するレコードは、削除タスクが実行されたときに削除オブジェクト内の関係ツリー全体から削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Improper use of this framework can cause unexpected results, database corruption, and application downtime requiring full database and application recovery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフレームワークを不適切に使用すると、予期しない結果、データベース破損、データベース全体およびアプリケーションの復旧が必要となるアプリケーション ダウンタイムが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Exercise extreme caution, and thoroughly test your recycling strategy in a test environment before working in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境で作業する前に、十分に注意を払い、テスト環境でリサイクル戦略を入念にテストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Consider the following points when working with a Purge Object:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトで作業する場合は、次の点を考慮してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Tables that store transient or intermediate data are usually good candidates for a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一時的または中間的なデータを格納するテーブルは通常、削除オブジェクトの主な候補です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You must validate the data dependency and application functionality before creating a Purge Object with such tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">こうしたテーブルで削除オブジェクトを作成する前に、データの依存関係とアプリケーションの機能を検証する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Verify that the table you select as the driver table for a Purge Object is a header table, such as <bpt id="p1">**</bpt>SalesParmTable<ept id="p1">**</ept> or <bpt id="p2">**</bpt>SalesQuotationTable<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトのドライバー テーブルとして選択したテーブルが、<bpt id="p1">**</bpt>SalesParmTable<ept id="p1">**</ept> または <bpt id="p2">**</bpt>SalesQuotationTable<ept id="p2">**</ept> などのヘッダー テーブルであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>A good indication, although not always accurate, is that the <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> value for such a table is <bpt id="p2">**</bpt>WorkSheetHeader<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Miscellaneous<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>Transaction<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ずしもいつも正確ではありませんが、そのようなテーブルの <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> の値は、<bpt id="p2">**</bpt>WorkSheetHeader<ept id="p2">**</ept>、<bpt id="p3">**</bpt>Miscellaneous<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>Transaction<ept id="p4">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Tables with a <bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> value of <bpt id="p2">**</bpt>Main<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Parameter<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Group<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>WorkSheetLine<ept id="p5">**</ept> cannot be driver tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TableGroup<ept id="p1">**</ept> 値が <bpt id="p2">**</bpt>Main<ept id="p2">**</ept>、<bpt id="p3">**</bpt>Parameter<ept id="p3">**</ept>、<bpt id="p4">**</bpt>Group<ept id="p4">**</ept>、<bpt id="p5">**</bpt>WorkSheetLine<ept id="p5">**</ept> のテーブルをドライバー テーブルにすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The driver table becomes the root parent in the hierarchical relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルは、階層リレーションシップ ツリーのルート親になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>IDMF queries the <bpt id="p1">**</bpt>XRefTableRelation<ept id="p1">**</ept> table to determine the parent-child relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF は <bpt id="p1">**</bpt>XRefTableRelation<ept id="p1">**</ept> テーブルを照会して、親子関係を判別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Removing records from a Purge Object may cause data inconsistency in your application in these conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトからレコードを削除すると、次の条件では、アプリケーションでデータの不整合が発生する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The driver table has known parent tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルには既知の親テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The driver table has known child tables that are not added to the Purge Table as a relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルには、削除テーブルにリレーションとして追加されていない既知の子テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Always minimize the Purge Object, and keep only the necessary relations and rules for your implementations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に削除オブジェクトを最小化し、実装に必要なルールおよび関係のみを保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Consider removing a table from the Purge Object in these conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件の 削除オブジェクトからテーブルを削除することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The table does not contain any data, and it is not likely to contain data in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルにはデータが含まれておらず、将来もデータが含まれない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The table stores only transient data, such as <bpt id="p1">**</bpt>CustTransOpen<ept id="p1">**</ept> or <bpt id="p2">**</bpt>SpecTrans<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルには、<bpt id="p1">**</bpt>CustTransOpen<ept id="p1">**</ept> や <bpt id="p2">**</bpt>SpecTrans<ept id="p2">**</ept> などの一時データのみが格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The table stores open transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルには未処理のトランザクションが格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The table creates nested relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルはネストされたリレーションシップを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If a table appears multiple times on different levels in the relationship tree, with the same qualifying relationship condition or set of primary keys, consider keeping the occurrence only in the lowest-numbered level in the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルが、同じ特定関係条件のもとまたは主キーのセットで、関係ツリー上の異なるレベルで複数回表示される場合、関係ツリーの最も低い番号のレベルでのみ表示されるように検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>There may be multiple relationships between two tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つのテーブル間に複数のリレーションシップが存在することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>In that case, evaluate the relationships and functionality carefully.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場合、リレーションシップと機能を慎重に評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>We recommend that you use only a single relationship in the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトでは単一のリレーションシップのみを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>However, you can use multiple relationships if necessary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、必要に応じて、複数のリレーションシップを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Be sure to select a valid relationship using a unique index or primary key, if one exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なリレーションシップが存在する場合は固有インデックスまたは主キーを使用して、有効なリレーションシップを選択してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>A table is unrelated to the driver table and makes its own Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルは、ドライバー テーブルとは無関係で、独自の削除オブジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For example, if you use <bpt id="p1">**</bpt>ProdTable<ept id="p1">**</ept> as a driver table, it also discovers <bpt id="p2">**</bpt>ProdJournalTable<ept id="p2">**</ept>, which itself is a separate Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>ProdTable<ept id="p1">**</ept> をドライバー テーブルとして使用する場合、<bpt id="p2">**</bpt>ProdJournalTable<ept id="p2">**</ept> が検出され、それ自体は別の削除オブジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Another example is PurchReqTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もう 1 つの例は PurchReqTable です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you use <bpt id="p1">**</bpt>PurchReqTable<ept id="p1">**</ept> as a driver table, it discovers <bpt id="p2">**</bpt>PurchParmLine<ept id="p2">**</ept>, which itself is a part of the <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchReqTable<ept id="p1">**</ept> をドライバー テーブルとして使用する場合、<bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> 削除オブジェクトの一部として、<bpt id="p2">**</bpt>PurchParmLine<ept id="p2">**</ept> が検出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Verify that the relationship tree that you have created in the Purge Object actually purges the intended data from your system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトに作成したリレーションシップ ツリーがシステムから目的のデータを実際に削除していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>A Purge Object that you create must look at all related records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成された削除オブジェクトは、関連するすべてのレコードを参照する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Missing relationships lead to orphaned data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">不足している関係は、データの孤立を引き起こします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Thoroughly test the effect of the purge on your database and application in a test environment that resembles your production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境テスト環境でのデータベースとアプリケーションには、削除の影響を十分にテストします。運用環境に似たテスト環境でデータベースとアプリケーションに対するパージの影響を完全にテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Test all business processes, and obtain user sign-off before trying to implement the Purge Object in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての業務プロセスをテストし、実稼働環境に削除オブジェクトを実装する前にユーザーの承認を得ます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>When you create a Purge Object from a purge template that is included with IDMF, validate and thoroughly test the Purge Object in a test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF に含まれている削除テンプレートから削除オブジェクトを作成するときは、テスト環境で、削除オブジェクトを検証して徹底的にテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>These templates are created in a standard Microsoft Dynamics AX application and may not match your implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテンプレートは標準の Microsoft Dynamics AX アプリケーションで作成され、実装と一致しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>We recommend that you use the discovery process to create your own Purge Objects or Archive Objects, and compare them with the templates, if a matching template is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスを使用して独自の削除オブジェクトまたはアーカイブ オブジェクトを作成し、適合しているテンプレートを使用できる場合は、プロセスそれらのオブジェクトをそのテンプレートと比較することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Carefully analyze any difference between the object you created through the discovery process and the template, to determine the cause of the difference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探索プロセスで作成したオブジェクトとテンプレートの違いを慎重に分析し、その違いの原因を特定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Manually add relations and rules to, or remove relations and rules from, the Purge Objects and Archive Objects to fit your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要件に合わせるために、削除オブジェクトとアーカイブ オブジェクトの関係およびルールを手動で追加または削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Make sure that the TableGroup property is set for all custom tables in Microsoft Dynamics AX, so that the discovery process can retrieve all related tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスで関連するすべてのテーブルを取得できるように、TableGroup プロパティが Microsoft Dynamics AX ですべてのカスタム テーブルに対して設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Synchronize changes, such as adding, deleting, or updating a table in the Application Object Tree (AOT), or the data dictionary synchronization in the Microsoft Dynamics AX metadata with IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション オブジェクト ツリー (AOT) でのテーブルの追加、削除、更新や、IDMF を使った Microsoft Dynamics AX メタデータでのデータ ディクショナリ同期など、変更を同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Run the post-installation tasks to synchronize the metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータを同期するため、インストール後の作業を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>For information, see the "Post-installation tasks" section in the <bpt id="p1">[</bpt>Data Management Framework Installation Guide<ept id="p1">](http://www.microsoft.com/en-us/download/details.aspx?id=16111)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>データ管理フレームワークのインストール ガイド<ept id="p1">](http://www.microsoft.com/en-us/download/details.aspx?id=16111)</ept> の「インストール後の作業」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Caution<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Verify that any tables with a table group of type Transaction are part of the Purge Object only if it is acceptable to purge data from these tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション タイプのテーブル グループを持つテーブルが、これらのテーブルからデータをパージできる場合にのみ、パージ オブジェクトの一部であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Create a new Purge Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい削除オブジェクトを作成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Follow these steps to create a new Purge Object:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトを作成するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Create Purge Object<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>削除オブジェクトの作成<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>In the <bpt id="p1">**</bpt>Create Purge Object<ept id="p1">**</ept> dialog box, select a table from the <bpt id="p2">**</bpt>Driver table<ept id="p2">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除オブジェクトの作成<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>ドライバー テーブル<ept id="p2">**</ept> リストからテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The list excludes tables from the exception list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリストは例外リストのテーブルを除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Navigate to and select <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> に移動して選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>A driver table is the parent table that defines the relationship tree for a specific Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルは、特定の削除オブジェクトのリレーションシップ ツリーを定義する親テーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In a Purge Object, the driver table may have child entities, but it does not have a parent entity in the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトでは、ドライバー テーブルに子エンティティがある場合がありますが、リレーションシップ ツリーに親エンティティはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>To continue, select the most unique index for the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するには、テーブルの最もユニークなインデックスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>This index is used to create the parent-child relationship in the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このインデックスは、削除オブジェクトに親子関係を作成するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In the <bpt id="p1">**</bpt>Unique keys<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>ParmId<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>固有のキー<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>ParmId<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The <bpt id="p1">**</bpt>ParmTableRefIdx<ept id="p1">**</ept> index is created using the <bpt id="p2">**</bpt>ParmID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>TableRefID<ept id="p3">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ParmTableRefIdx<ept id="p1">**</ept> インデックスは、<bpt id="p2">**</bpt>ParmID<ept id="p2">**</ept> および <bpt id="p3">**</bpt>TableRefID<ept id="p3">**</ept> フィールドを使用して作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Notice that by selecting <bpt id="p1">**</bpt>ParmID<ept id="p1">**</ept>, you are selecting a partial key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ParmID<ept id="p1">**</ept> を選択して部分的なキーを選択していることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>A unique index enables the discovery process to identify related tables in the same functional area, such as Finance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固有インデックスを使用すると、探索プロセスは、Finance などの同じ機能エリアに関連するテーブルを識別できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you do not select a unique index, the discovery process may find related tables from all functional areas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固有のインデックスを選択しない場合、検出プロセスですべての機能領域から関連テーブルが検索されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You must make sure that the discovery process identifies the correct functional relationships for your implementation of Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探索プロセスにより、Microsoft Dynamics AX 実装の正しい機能関係を識別できるようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Click <bpt id="p1">**</bpt>Discover<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>検出<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>IDMF uses metadata that is imported from the Microsoft Dynamics AX database, and the exception parameters list, to generate a relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF は、Microsoft Dynamics AX データベースからインポートされたメタデータと例外パラメーター リストを使用して、関係ツリーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The relationship tree starts with the driver table and creates a hierarchy of parent-child relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーはドライバー テーブルで始まり、親子関係の階層を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Make sure that your Purge Object resembles the following graphic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトが次の図のようになっていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>IDMF Purge object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF 削除オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The relationship tree in this Purge Object is three levels deep.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この削除オブジェクトのリレーションシップ ツリーは 3 階層の深さです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Level 0, the topmost level, contains the driver table, PurchParmTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最上位レベルのレベル 0 には、ドライバー テーブル PurchParmTable が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Level 1 contains the child entities of the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 1 には、ドライバー テーブルの子エンティティが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The last level, level 2, contains the child entities of tables in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 2 の最後のレベルには、レベル 1 のテーブルの子エンティティが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This relationship tree is created based on the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この関係ツリーは、以下の情報に基づいて作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The Microsoft Dynamics AX metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX メタデータ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The discovery process uses the metadata to create a list of related tables that form the parent-child hierarchy based on the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスは、メタデータを使用して、ドライバー テーブルに基づいて親子階層を形成する関連テーブルのリストを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The exception parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外パラメーター。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Tables that belong to the exception parameters list are filtered out from the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外パラメーターの一覧に属しているテーブルは関係ツリーから除外されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Use the <bpt id="p1">**</bpt>Administer<ept id="p1">**</ept> menu to configure the exception parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理<ept id="p1">**</ept> メニューを使用して、例外パラメーターを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Verify the relationship tree, and assess the functional effect of the tree on your Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーを検証し、Microsoft Dynamics AX アプリケーション上でそのツリーの機能的効果を評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>As a result of your assessment, you may decide to manually add or remove some relations and rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価の結果、一部の関係やルールを手動で追加または削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For example, when you click <bpt id="p1">**</bpt>Restore<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, the Purge Object is restored from the default template that ships with IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept>ウィンドウで<bpt id="p1">**</bpt>復元<ept id="p1">**</ept>をクリックすると、IDMF で出荷する既定のテンプレートから削除オブジェクトが復元されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The restored relationship tree in this case differs from the Purge Object you created using <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> as the discovery table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合の復元されたリレーションシップ ツリーは、ディスカバリ テーブルとして <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> を使用して作成した削除オブジェクトとは異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>This is because the default template in IDMF is modified based on the functionality assessment of a standard Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、標準の Microsoft Dynamics AX アプリケーションの機能評価に基づいて、IDMF の既定のテンプレートが変更されるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The Purge Object you create through discovery may not agree with the default template that is included with IDMF, if one exists for the discovery table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出テーブルにいずれかが存在する場合、検索で作成した削除オブジェクトは、IDMF に含まれている既定のテンプレートと一致しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Be careful with your selection of the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルの選択には注意が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you select a table such as the <bpt id="p1">**</bpt>ProdTable<ept id="p1">**</ept> table, the relationship tree can go many levels deep, spanning many tables on each level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProdTable<ept id="p1">**</ept> テーブルなどのテーブルを選択すると、各レベルの多数のテーブルにまたがっている数多くのレベルの関係ツリーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Such a Purge Object creates a complex relationship tree and increases the potential for error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような削除オブジェクトは、複雑な関係ツリーを作成し、エラーが発生する可能性を高くします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The default template that is included with IDMF may not match the metadata of your Microsoft Dynamics AX implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF に含まれている既定のテンプレートは、Microsoft Dynamics AX 実装のメタデータと一致しない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>A table in the default template that is not found in the metadata from the production database is marked invalid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産データベースのメタデータに見つからない既定テンプレートのテーブルは、無効とマークされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>An invalid table appears with a dotted red border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なテーブルに破線の赤い点線の枠線が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>You must remove all invalid tables from the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトからすべての無効なテーブルを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The fields that you use to create relations and rules from the valid tables are also validated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なテーブルからリレーションおよびルールを作成するために使用するフィールドも検証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>A field with a disabled configuration key is considered invalid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なコンフィギュレーション キーが設定されたフィールドは無効と見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>A valid table with invalid fields is shown with a yellow dotted border, as shown in Figure 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なフィールドを持つ有効なテーブルは、図 2 に示すように、黄色の点線の枠線で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>You must remove any rules or relations in the Purge Object that are defined with the disabled fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効フィールドで定義された削除オブジェクトのルールや関係を、すべて削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>You can continue using the object after removing the invalid table or tables with invalid fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なテーブル、または無効なフィールドを含むテーブルを削除した後、オブジェクトの使用を続行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>IDMF Purge Object with Invalid Tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なテーブルを含む IDMF 削除オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Navigation of the Create Purge Object workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトの作成ワークスペースのナビゲーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The following tables provide descriptions for the controls in this workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルで、このワークスペースのコントロールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Panes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Relationship tree pane<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>リレーションシップ ツリー ウィンドウ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Provides a graphical view of all the tables in the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトにすべてのテーブルのグラフィック ビューを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>The following list describes the controls and command that you can use to navigate the relationship tree pane:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のリストでは、リレーションシップ ツリー ウィンドウを移動するために使用できるコントロールとコマンドについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>With the <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Level<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> slider, you can select a level and show only the tables at the selected and higher levels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>レベル<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> スライダーでは、レベルを選択して、選択したレベルおよび上位レベルにあるテーブルのみを表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>With the <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Zoom<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> slider, you can change the diagram size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>ズーム<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> スライダーでは、図のサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Right-click the driver table, and then click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove all invalid tables<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to remove all invalid tables, together with all related tables in the nested hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライバー テーブルを右クリックし、無効なすべてのテーブルを、関連するすべてのテーブルとともに入れ子になった階層で削除するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>無効なテーブルをすべて削除する<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Right-click a table to display a menu with the following options:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のオプションを含むメニューを表示するテーブルを右クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to remove the selected table and its related tables from the hierarchical tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブル、およびその関連テーブルを階層ツリーから削除するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>For example, the <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> table appears in level 2 and level 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> テーブルはレベル 2 とレベル 3 で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If you right-click the table in level 2, and then select <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>, the table is removed from level 2, together with its nested child relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 2 のテーブルを右クリックし、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>を選択すると、レベル 2 からテーブルが、入れ子になった子関係と共に削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The occurrence of the table remains intact in level 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの発生はレベル 3 のままです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Select all occurrences<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to display all occurrences of the selected table and its related tables in a dotted green border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>すべての発生を選択<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックすると、選択したテーブルとその関連テーブルのすべての出来事が緑色の点線の枠内に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In this case, the table <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> is selected in levels 2 and 3, together with all its nested child relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、テーブル <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> は入れ子になった子関係すべてと共にレベル 2 と 3 で選択されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove all occurrences<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to remove all occurrences of the selected table and its related tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブル、およびその関連テーブルのすべての内容を削除するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>すべてを削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>In this case, the table <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> is removed from levels 2 and 3, together with all its nested child relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、テーブル <bpt id="p1">&lt;strong&gt;</bpt>SpecTrans<ept id="p1">&lt;/strong&gt;</ept> は入れ子になった子関係すべてと共にレベル 2 と 3 から削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The removed tables appear in a gray-colored shape with a solid red border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除されたテーブルが赤い実線の入った灰色の図形に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Click <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Discover<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> to regenerate the hierarchical parent-child relationship for the selected table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルの親子関係階層を再生成するには、<bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>検出<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>This command is available only when you select a table with a <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>TableGroup<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> value of <bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>WorkSheetHeader<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、<bpt id="p3">&lt;strong&gt;</bpt><bpt id="p4">&lt;span class="ui"&gt;</bpt>WorkSheetHeader<ept id="p4">&lt;/span&gt;</ept><ept id="p3">&lt;/strong&gt;</ept> の <bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>TableGroup<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept> 値を持つテーブルを選択した場合にのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Properties<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>プロパティ<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Shows properties for the selected table and provides commands that you can use for the selected table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルのプロパティを表示し、選択したテーブルに使用できるコマンドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>When a table in the Purge Object contains multiple relations, you can use the <bpt id="p1">&lt;span class="ui"&gt;</bpt>Relations<ept id="p1">&lt;/span&gt;</ept> node in the tree view to disable one or more relations, as detailed later in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクト内のテーブルに複数のリレーションが存在するときは、ツリー ビューの <bpt id="p1">&lt;span class="ui"&gt;</bpt>Relations<ept id="p1">&lt;/span&gt;</ept> ノードを使用して、このトピックで後で詳しく説明しているように、1 つまたは複数のリレーションを無効にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Remove table<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>テーブルの削除<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Provides a data grid that you can use to select tables for removal from the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ツリーから削除するテーブルを選択するために使用できるデータ グリッドを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>This pane also provides an <bpt id="p1">&lt;span class="ui"&gt;</bpt>Advanced filter<ept id="p1">&lt;/span&gt;</ept> control that you can use to filter the data grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このペインには、データ グリッドをフィルタリングするために使用できる<bpt id="p1">&lt;span class="ui"&gt;</bpt>高度なフィルタ<ept id="p1">&lt;/span&gt;</ept>コントロールもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>Related information<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt><bpt id="p2">&lt;span class="ui"&gt;</bpt>関連情報<ept id="p2">&lt;/span&gt;</ept><ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Provides additional information for some of the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のテーブルの追加情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If related information is provided, read it carefully to understand the recycle relevance of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連する情報が指定された場合は、テーブルのリサイクルの妥当性を理解するために慎重に読んでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source><bpt id="p1">**</bpt>Remove<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Remove tables that are selected in the data grid in the Remove table pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[テーブルの削除] ウィンドウのデータ グリッドで選択されているテーブルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>When you remove a table, all of the child tables for the selected table are removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを削除すると、選択したテーブルのすべての子テーブルが削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The removal spans the whole relationship tree, and all nested parent-child relationships for the selected table's child tables are removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除すると、リレーションシップ ツリー全体が削除され、選択したテーブルの子テーブルのすべてのネストされた親子リレーションが削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source><bpt id="p1">**</bpt>Revert<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>元に戻す<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Reverse the modifications made to the Purge Object, back to the last save.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトに行われた変更を前回の変更まで戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>This is like an "undo" command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、「元に戻す」のようなものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><bpt id="p1">**</bpt>Show all/Show selected<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべて表示/選択されたものを表示<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Show all tables or selected tables, and switch the label of the command button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのテーブルまたは選択したテーブルを表示し、コマンド ボタンのラベルを切り替えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Removed tables appear with a dotted red line around them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除されたテーブルが、周囲に赤い点線付きで表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">**</bpt>Restore<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>復元<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Revert the Purge Object to the original source that you used to create it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成時に使用した元のソースに削除オブジェクトを戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>If a purge template was used, the Purge Object reverts to the template that is shipped with IDMF.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除テンプレートを使用していた場合、削除オブジェクトは IDMF に同梱されているテンプレートに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>If the discovery process was used, the Purge Object reverts to the first Purge Object that you discovered and saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出プロセスを使用していた場合、削除オブジェクトは、検出し保存した最初の削除オブジェクトに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Fields (Remove table pane)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド (テーブルの削除ウィンドウ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Check boxes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チェック ボックス<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Select the tables that you want to remove from the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ツリーから削除するテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>The name of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Configuration key<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンフィギュレーション キー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The configuration key of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルのコンフィギュレーション キー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source><bpt id="p1">**</bpt>Level<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レベル<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>The level of the table in the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリー内のテーブルのレベル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source><bpt id="p1">**</bpt>Row count<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>行数<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The number of rows in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの行数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Walkthrough: Create a Purge Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: 削除オブジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>This section provides a walkthrough for working with a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、削除オブジェクトの操作に関するチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>If you have not created the Purge Object already, create one.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトをまだ作成していない場合は、作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Use the <bpt id="p1">**</bpt>Zoom<ept id="p1">**</ept> slider to change the diagram size, so that you can read the table names easily.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ズーム<ept id="p1">**</ept> スライダーを使用して、テーブル名を簡単に読み取れるように図のサイズを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>In the relationship tree, move the mouse pointer over the table <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> to see the information that is displayed in the tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、テーブル <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> にマウス ポインターを移動し、ツール ヒントに表示される情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the relationship tree, move the mouse pointer over the <bpt id="p1">**</bpt>1:N relationship description<ept id="p1">**</ept> above the <bpt id="p2">**</bpt>PurchParmLine<ept id="p2">**</ept> table to see the information that is displayed in the tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、<bpt id="p2">**</bpt>PurchParmLine<ept id="p2">**</ept> テーブルの上の <bpt id="p1">**</bpt>1:N 関係の説明<ept id="p1">**</ept>にマウス ポインターを移動し、ツール ヒントに表示される情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, expand each node in the tree view to see the information that is provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、ツリー ビューの各ノードを展開して指定されている情報を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If the <bpt id="p1">**</bpt>Advanced filter<ept id="p1">**</ept> control does not show the selection criteria, click the <bpt id="p2">**</bpt>Advanced filter<ept id="p2">**</ept> arrow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>高度なフィルター<ept id="p1">**</ept> コントロールでの選択基準が表示されない場合、<bpt id="p2">**</bpt>高度なフィルター<ept id="p2">**</ept>矢印をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Type 1 in the level box, and then click <bpt id="p1">**</bpt>Search<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル ボックスに 1 と入力してから、<bpt id="p1">**</bpt>検索<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>This changes the grid so that it shows only those tables that are in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、レベル 1 にあるテーブルのみが表示されるようにグリッドが変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Select the <bpt id="p1">**</bpt>PurchParmLine<ept id="p1">**</ept> table by selecting the check box next to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">横にあるチェック ボックスをオンにして <bpt id="p1">**</bpt>PurchParmLine<ept id="p1">**</ept> テーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, click <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで<bpt id="p2">**</bpt>削除<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Notice that the table <bpt id="p1">**</bpt>PurchParmLine<ept id="p1">**</ept>, and all its child tables in levels 1 and 2, are marked with a red border, which indicates that these tables have been removed from the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル <bpt id="p1">**</bpt>PurchParmLine<ept id="p1">**</ept>、およびレベル 1 および 2 のすべての子テーブルが赤い枠線でマークされていることを確認します。これらのテーブルはリレーションシップ ツリーから削除されたことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Click the <bpt id="p1">**</bpt>Show all<ept id="p1">**</ept> button in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウの<bpt id="p1">**</bpt>すべて表示<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The diagram shows all the tables, with the removed tables in a gray-colored shape with solid red lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">図にはすべてのテーブルが表示され、削除されたテーブルは灰色の形で赤い線で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Click <bpt id="p1">**</bpt>Revert<ept id="p1">**</ept> to restore the original Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>元に戻す<ept id="p1">**</ept>をクリックし、元の削除オブジェクトを復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The diagram now reverts to the state it was in before you deleted <bpt id="p1">**</bpt>PurchParmLine<ept id="p1">**</ept> in step 7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この図は、手順 7で <bpt id="p1">**</bpt>PurchParmLine<ept id="p1">**</ept> を削除する前の状態に戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Repeat steps 6, 7, and 8 to remove the tables again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 6、7、8 を繰り返して、もう一度テーブルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You see all the removed tables in a gray-colored shape with solid red lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">赤い実線の入った灰色の図形に、削除されたすべてのテーブルが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Click <bpt id="p1">**</bpt>Show selected<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane to see the revised Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウ内の<bpt id="p1">**</bpt>選択項目の表示<ept id="p1">**</ept>をクリックし、改訂された削除オブジェクトを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Verify that the removed tables are not in the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除したテーブルが削除オブジェクトに存在しないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Save the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>A warning is displayed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">警告が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Read the warning carefully.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">警告を慎重に読みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>IDMF lets you create a Purge Object that defines a hierarchical relationship tree among the Microsoft Dynamics AX application tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF では、Microsoft Dynamics AX アプリケーション テーブル間の階層関係ツリーを定義する削除オブジェクトを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>You can then apply rules to selected records based on specific criteria.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の条件に基づき選択したレコードにルールを適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Records matching the selection criteria are deleted from the entire relationship tree in the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択基準に一致するレコードは、削除オブジェクト内の関係ツリー全体から削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Improper use of IDMF can cause unexpected results, database corruption, and application downtime requiring full database and application recovery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDMF を不適切に使用すると、予期しない結果、データベース破損、データベース全体およびアプリケーションの復旧が必要となるアプリケーション ダウンタイムが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Exercise extreme caution, and thoroughly test your recycling strategy in a test environment before working in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境で作業する前に、十分に注意を払い、テスト環境でリサイクル戦略を入念にテストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to continue saving the Purge Object or <bpt id="p2">**</bpt>No<ept id="p2">**</ept> to cancel the save operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトの保存を続ける場合は<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>を 、保存操作をキャンセルする場合は<bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to continue with the walkthrough.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアルを続行するには、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In the** Save as** dialog box, verify that the name is <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">**名前を付けて保存**ダイアログ ボックスで、名前が <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>In the <bpt id="p1">**</bpt>Overwrite Purge Object<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> to overwrite the Purge Object with the new version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除オブジェクトの上書き<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>をクリックして新しいバージョンで削除オブジェクトを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>In the <bpt id="p1">**</bpt>Save status<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存状態<ept id="p1">**</ept>ダイアログ ボックスで <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Purge template/Purge Objects<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>PurchParmTable<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>削除テンプレート/削除オブジェクト<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>PurchParmTable<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Notice that the icon of the Purge Object has changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトのアイコンが変更されたことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>This change in the icon differentiates a Purge Object from a purge template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアイコンの変更により、削除オブジェクトと削除テンプレートが区別されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Verify that the Purge Object diagram does not contain the tables you removed in step 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクト図に手順 10 で削除したテーブルが含まれていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Switch between <bpt id="p1">**</bpt>Show all/Show selected<ept id="p1">**</ept> to confirm that the removed tables still show up in the red border.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべての表示/選択項目の表示<ept id="p1">**</ept> を切り替えて、削除したテーブルが赤い境界線に引き続き表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, click <bpt id="p2">**</bpt>Revert<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで<bpt id="p2">**</bpt>元に戻す<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>The Purge Object does not change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトは変化しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>The revert action cannot undo the changes, because the Purge Object has been saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトが保存されているため、元に戻す操作で変更を元に戻すことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, click <bpt id="p2">**</bpt>Restore<ept id="p2">**</ept> to revert the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>復元<ept id="p2">**</ept>をクリックして削除オブジェクトを元に戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>The Purge Object reverts to the purge template that is included in IDMF, if one exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトは、いずれかが存在する場合、IDMF に含まれる削除テンプレートに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>If there is no default purge template, the Purge Object reverts to the first version you created through the discovery process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の削除テンプレートがない場合は、削除オブジェクトは検索プロセスで作成した最初のバージョンに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The restored Purge Object may be the same as, or different from, the Purge Object you started working with in step 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元された削除オブジェクトは、手順 1 で作業を開始した削除オブジェクトと同じか、異なる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The default purge template contains a modified or adjusted relationship tree based on the functional assessment of the Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の削除テンプレートには、Microsoft Dynamics AX アプリケーションの機能評価に基づいて変更または調整されたリレーションシップ ツリーが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to overwrite the object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトを上書きするには、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the <bpt id="p1">**</bpt>Save status<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存状態<ept id="p1">**</ept>ダイアログ ボックスで <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Keep the Purge Object open, because it is also used in the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでも使用するため、削除オブジェクトを開いたままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Walkthrough: Disable a relation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: リレーションの無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>This section provides a walkthrough for disabling relations in a table with multiple relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、複数の関係を持つテーブル内の関係を無効にするためのチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Click the <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept> メニューをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Purge template/Purge Objects<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>InventJournalTable<ept id="p2">**</ept> from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>削除テンプレート/削除オブジェクト<ept id="p1">**</ept>をクリックし、リストから <bpt id="p2">**</bpt>InventJournalTable<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In the relationship tree, move the mouse pointer over the <bpt id="p1">**</bpt>1:N relationship description<ept id="p1">**</ept> above the <bpt id="p2">**</bpt>InventJournalTrans<ept id="p2">**</ept> table to see the information displayed in the tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、<bpt id="p2">**</bpt>InventJournalTrans<ept id="p2">**</ept> テーブルの上の <bpt id="p1">**</bpt>1:N 関係の説明<ept id="p1">**</ept>にマウス ポインターを移動し、ツール ヒントに表示される情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Notice that this table has only one relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルに関係が 1 つだけあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>In the relationship tree, move the mouse pointer over the <bpt id="p1">**</bpt>1:N relationship description<ept id="p1">**</ept> above the <bpt id="p2">**</bpt>WMSJournalTable<ept id="p2">**</ept> table to see the information displayed in the tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、<bpt id="p2">**</bpt>WMSJournalTable<ept id="p2">**</ept> テーブルの上の <bpt id="p1">**</bpt>1:N 関係の説明<ept id="p1">**</ept>にマウス ポインターを移動し、ツール ヒントに表示される情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Notice that this table has many relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルに多くの関係があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>In the relationship tree, select <bpt id="p1">**</bpt>WMSJournalTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーで、<bpt id="p1">**</bpt>WMSJournalTable<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, expand <bpt id="p2">**</bpt>WMSJournalTable<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Relations<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで <bpt id="p2">**</bpt>WMSJournalTable<ept id="p2">**</ept><ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>関係<ept id="p3">**</ept>と展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>This table has many relations, and you can use the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane to disable one or more relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルには多くのリレーションが含まれていて、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウを使用して、1 つまたは複数のリレーションを無効にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Right-click the <bpt id="p1">**</bpt>InventBOM<ept id="p1">**</ept> relation to open the <bpt id="p2">**</bpt>Disable relation<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>InventBOM<ept id="p1">**</ept> 関係を右クリックして <bpt id="p2">**</bpt>関係の無効化<ept id="p2">**</ept> メニューを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>The <bpt id="p1">**</bpt>Disable relation<ept id="p1">**</ept> menu appears only when a table has multiple relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の無効化<ept id="p1">**</ept> メニューは、テーブルが複数の関係を持つ場合にのみ表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>In the <bpt id="p1">**</bpt>Relations<ept id="p1">**</ept> node, right-click <bpt id="p2">**</bpt>InventCount<ept id="p2">**</ept>, and select <bpt id="p3">**</bpt>Disable relation<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係<ept id="p1">**</ept>ノードで、<bpt id="p2">**</bpt>InventCount<ept id="p2">**</ept> を右クリックして<bpt id="p3">**</bpt>関係の無効化<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Notice that the disabled relation appears in red.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効な関係が赤色で表示されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Right-click <bpt id="p1">**</bpt>InventCount<ept id="p1">**</ept>, and select <bpt id="p2">**</bpt>Enable relation<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>InventCount<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>関係の有効化<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Notice that the enabled relation appears in black.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な関係が黒色で表示されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>An excluded relation does not become part of the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">除外された関係は削除オブジェクトの一部にはなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Multiple enabled relations form the "or" clause in the SQL statement that the Purge Object generates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の有効な関係が削除オブジェクトが生成する SQL ステートメントで「or」句を形成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Do not save the purge template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除テンプレートを保存しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source><bpt id="p1">**</bpt>Caution<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Exercise care, and thoroughly test the excluded relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">除外された関係を徹底的にテストし、慎重に行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>An erroneous or incorrect exclusion causes data corruption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">誤ったまたは間違った除外はデータの破損を引き起こします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Purge template/Purge Objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートの削除/オブジェクトの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>This command provides a list of purge templates and Purge Objects in your system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、システム内の削除テンプレートと削除オブジェクトのリストを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>A purge template is a template that is included with IDMF with a predefined relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除テンプレートは、事前定義されたリレーションシップ ツリーで IDMF に含まれているテンプレートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>You can use a purge template as a starting point to create a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出発点として削除テンプレートを使用し、削除オブジェクトを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>You must review a purge template to make sure that it meets your requirements, and save it before you can use it in a purge task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除タスクの使用前に、要件を満たしているかどうか確認するために削除テンプレートを確認して保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Walkthrough: Work with a purge template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: 削除テンプレートの操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>This section provides a walkthrough for working with a purge template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、削除テンプレートの操作に関するチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Purge template/Purge Objects<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>PurchReqTable<ept id="p2">**</ept> from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>削除テンプレート/削除オブジェクト<ept id="p1">**</ept>をクリックし、リストから <bpt id="p2">**</bpt>InventJournalTable<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Review the tables, table properties, and relationship tree to understand how the delete action on the <bpt id="p1">**</bpt>PurchReqTable<ept id="p1">**</ept> cascades through the relationship tree in the purge template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、テーブルのプロパティ、関係ツリーを確認し、<bpt id="p1">**</bpt>PurchReqTable<ept id="p1">**</ept> での削除アクションが削除テンプレートの関係ツリーを通じてカスケードする方法を理解します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Make sure that this relationship tree covers your application and any customizations you may have made to the Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリレーションシップ ツリーに、アプリケーションと、Microsoft Dynamics AX アプリケーションに対して行ったすべてのカスタマイズが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>You can either keep the same name or change the name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ名前を保持するか、名前を変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Change the name to PurchReqTable<ph id="ph1">\_</ph>object to identify this saved object as a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を PurchReqTable<ph id="ph1">\_</ph> オブジェクトに変更し、この保存されたオブジェクトを削除オブジェクトとして識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> in the dialog box to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するにはダイアログ ボックスで <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Purge template/Purge Objects<ept id="p1">**</ept>, and compare the icons of <bpt id="p2">**</bpt>PurchReqTable<ept id="p2">**</ept> and <bpt id="p3">**</bpt>PurchReqTable<ph id="ph1">\_</ph>object<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>削除テンプレート/削除オブジェクト<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>PurchReqTable<ept id="p2">**</ept> と <bpt id="p3">**</bpt>PurchReqTable <ph id="ph1">\_</ph>オブジェクト<ept id="p3">**</ept>のアイコンを比較します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Repeat steps 1 through 3, but save the object as <bpt id="p1">**</bpt>PurchReqTable<ept id="p1">**</ept>, the original name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1 ～ 3 を繰り返しますが、オブジェクトを元の名前 <bpt id="p1">**</bpt>PurchReqTable<ept id="p1">**</ept> で保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>In the <bpt id="p1">**</bpt>Overwrite Purge Object<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> to overwrite the object with the new version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除オブジェクトの上書き<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>をクリックして新しいバージョンでオブジェクトを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Repeat step 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5 を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Notice that the icons of a Purge Object and a saved purge template are same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトと保存された削除テンプレートのアイコンが同じであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>This is because when you save a purge template, it becomes a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、削除テンプレートを保存すると削除オブジェクトになるためです。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>