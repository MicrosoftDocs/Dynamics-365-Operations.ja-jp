<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="data-entities.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>data-entities.20f8ad.ef86e9707455a1ed2bc6321e57d768ab5208d21c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ef86e9707455a1ed2bc6321e57d768ab5208d21c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\data-entities.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic defines and provides an overview of data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、データ エンティティを定義し、その概要について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It includes information about the capabilities of data entities, the scenarios that they support, the categories that are used for them, and the methods for creating them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、データ エンティティの機能、サポートされるシナリオ、およびそれらに使用されるカテゴリ、作成するメソッドに関する情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic defines and provides an overview of data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、データ エンティティを定義し、その概要について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It includes information about the capabilities of data entities, the scenarios that they support, the categories that are used for them, and the methods for creating them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、データ エンティティの機能、サポートされるシナリオ、およびそれらに使用されるカテゴリ、作成するメソッドに関する情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A <bpt id="p1">*</bpt>data entity<ept id="p1">*</ept> is an abstraction from the physical implementation of database tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>データ エンティティ<ept id="p1">*</ept>はデータベース テーブルの物理的な実装から抽象化したものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, in normalized tables, a lot of the data for each customer might be stored in a customer table, and then the rest might be spread across a small set of related tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、正規化テーブルでは、各顧客の大量データが顧客テーブルに格納されており、残りは小さな一連の関連テーブル間で拡大している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In this case, the data entity for the customer concept appears as one de-normalized view, in which each row contains all the data from the customer table and its related tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、顧客概念のデータ エンティティは非正規化ビューとして表示され、各行に顧客テーブルと関連するテーブルからのすべてのデータが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>A data entity encapsulates a business concept into a format that makes development and integration easier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティは、開発と統合を簡単にする形式に、ビジネス コンセプトをカプセル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The abstracted nature of a data entity can simplify application development and customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティには、抽象化された性質があるため、アプリケーションの開発とカスタマイズを簡略化できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Later, the abstraction also insulates application code from the inevitable churn of the physical tables between versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、抽象化によってアプリケーション コードもバージョン間の物理テーブルの避けられないチャーンから隔離されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>To summarize:<ept id="p1">**</ept> Data entity provides conceptual <bpt id="p2">**</bpt>abstraction<ept id="p2">**</ept> and <bpt id="p3">**</bpt>encapsulation<ept id="p3">**</ept> (de-normalized view) of underlying table schemas to represent key data concepts and functionalities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>集計する:<ept id="p1">**</ept> データ エンティティは重要なデータの概念および機能を表すための基礎となるテーブル スキーマの<bpt id="p2">**</bpt>抽象化<ept id="p2">**</ept>および<bpt id="p3">**</bpt>カプセル化<ept id="p3">**</ept> (非正規化ビュー) の概念を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Capabilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処理能力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A data entity has the following capabilities:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティには次の機能があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>It replaces diverging and fragmented concepts of AXD, Data Import/Export Framework (DIXF) entities, and aggregate queries with single concept.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXD、データのインポート/エクスポート フレームワーク (DIXF) エンティティ、1 つの概念を持つ集計クエリの分岐して細分化された概念を置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>It provides a single stack to capture business logic, and to enable scenarios such as import/export, integration, and programmability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックをキャプチャして、インポート/エクスポート、統合、およびプログラマビリティなどのシナリオを有効にする 1 つのスタックを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>It becomes the primary mechanism for exporting and importing data packages for Application Lifecycle Management (ALM) and demo data scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Application Lifecycle Management (ALM) およびデモ データ シナリオに関するデータ パッケージのエクスポートおよびインポートの主要なメカニズムとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>It can be exposed as OData services, and then used in tabular-style synchronous integration scenarios and Microsoft Office integrations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData サービスとして公開して、表スタイルの同期統合シナリオと Microsoft Office 統合で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Data entity architecture<ept id="p1">](./media/over1.png)](./media/over1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データ エンティティ アーキテクチャ<ept id="p1">](./media/over1.png)](./media/over1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Entity example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>A consumer wants to access data that is related to a customer object, but this data is currently scattered across multiple normalized tables, such as DirParty, CustTable, LogisticPostalAddress, and LogisticElectronicAddress.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンシューマーは、顧客オブジェクトに関連付けられているデータにアクセスしようとしていますが、このデータは DirParty、CustTable、LogisticPostalAddress、LogisticElectronicAddress などの複数の正規化テーブルに分散されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Therefore, the process of reading and writing customer data is very tedious.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、顧客データを読み書きするプロセスは非常に手間がかかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Instead, the following customer entity can be designed to encapsulate the entire underlying physical schema into a single de-normalized view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、次の顧客エンティティは、1 つの非正規化ビューに基になる物理スキーマ全体をカプセル化するように設計できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This enables simpler read/write operations and also enables abstraction of any internal interaction between the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、より簡単な読み取り/書き込み操作が可能になり、テーブル間の内部相互作用の抽象化も可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Denormalized tables<ept id="p1">](./media/over2.png)](./media/over2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>非正規化テーブル<ept id="p1">](./media/over2.png)](./media/over2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Normalized entity<ept id="p1">](./media/over3.png)](./media/over3.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>正規化エンティティ<ept id="p1">](./media/over3.png)](./media/over3.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Supported scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされているシナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Data entities support all the following scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティは、以下のすべてのシナリオをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Integration scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Synchronous service (OData)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同期サービス (OData)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Data entities enable public application programming interfaces (APIs) on entities to be exposed, which enables synchronous services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティは、エンティティ上の公開アプリケーション プログラミング インターフェイス (API) を公開して、同期サービスを可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Synchronous services are used for the following purposes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同期サービスは、次の目的で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Office integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office 統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Third-party mobile apps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サード パーティ モバイル アプリケーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Asynchronous integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非同期の統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Data entities also support asynchronous integration through a data management pipeline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティは、データ管理パイプラインを介した非同期統合もサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>This enables asynchronous and high-performing data insertion and extraction scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、非同期かつ高性能のデータ挿入および抽出シナリオが可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Here are some examples:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつか例を挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Interactive file-based import/export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対話型ファイル ベースのインポート/エクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Recurring integrations (file, queue, and so on)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定期的な統合 (ファイル、キューなど)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Business intelligence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Aggregate data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Standardized key performance indicators (KPIs)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準化された主要業績評価指標 (KPI)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Application Lifecycle Management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ライフサイクル管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Besides integration and business intelligence (BI) scenarios, data entities also initially support two critical ALM scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合およびビジネス インテリジェンス (BI) のシナリオの他に、データ エンティティも最初は 2 つの重要な ALM シナリオをサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The following two progressive levels of an ALM scenario show the scope of coverage by data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ALM シナリオの次の 2 つのプログレッシブ レベルは、データ エンティティによるカバレッジの範囲を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Entities and lifecycle management<ept id="p1">](./media/over4.png)](./media/over4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>エンティティおよびライフ サイクル管理<ept id="p1">](./media/over4.png)](./media/over4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Configuration data provisioning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション データのプロビジョニング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A system implementer will use both a guided data collection wizard and bulk data input mechanisms to <bpt id="p1">**</bpt>bootstrap the initial deployment<ept id="p1">**</ept> (or module) with configuration data through Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムの実装担当者は、ガイド付きデータ収集ウィザードとバルク データ入力メカニズムの両方を使用して、Microsoft Dynamics Lifecycle Services (LCS) を介して、構成データで<bpt id="p1">**</bpt>初期展開 (またはモジュール) をブート<ept id="p1">**</ept>します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Configuration primarily targets to cover the following entity categories:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションは、主に次のエンティティ カテゴリを対象としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>All of Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのパラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Reference</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>System parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Number sequence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">整理番号</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通貨</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Data migration from legacy or external systems</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レガシ システムまたは外部システムからのデータ移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>After the initial deployment is up and running, the system implementer will <bpt id="p1">**</bpt>migrate existing data assets of the customer<ept id="p1">**</ept> into Microsoft Dynamics 365 for Finance and Operations, especially the following assets:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の配置が立ち上がって動作した後、システム実装担当者は、Microsoft Dynamics 365 for Finance and Operations に<bpt id="p1">**</bpt>顧客の既存データ資産を移行<ept id="p1">**</ept>します。特に、以下の資産を移行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Master data (for example, customers and vendors)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター データ (たとえば、顧客および仕入先)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Subsets of documents (for example, sales orders)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント (たとえば、販売注文) のサブセット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Categories of entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのカテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Entities are categorized based on their functions and the type of data that they serve.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは、それらの機能およびそれらが提供するデータのタイプに基づいて分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The following are five categories for data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下は、データ エンティティの 5 つのカテゴリです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Functional or behavioral parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能的または行動のパラメーター。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Required to set up a deployment or a module for a specific build or customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のビルドまたは顧客の展開またはモジュールを設定するために必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Can include data that is specific to an industry or business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">産業またはビジネスに固有のデータを含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The data can also apply to a broader set of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データは、より広範な顧客にも適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Tables that contain only one record, where the columns are values for settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列の設定の値になっている、1 つだけのレコードが含まれているテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Examples of such tables exist for Account payable (AP), General ledger (GL), client performance options, workflows, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなテーブルの例としては、買掛金勘定 (AP)、一般会計 (GL)、クライアント パフォーマンス オプション、ワークフローなどが存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Reference</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Simple reference data, of small quantity, which is required to operate a business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスを操作するために必要な少量の簡易参照データです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Data that is specific to an industry or a business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">産業または業務プロセスに固有のデータ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Examples include units, dimensions, and tax codes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例には、単位、分析コード、および税コードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Master</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Data assets of the business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネスのデータ資産。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Generally, these are the "nouns" of the business, which typically fall into categories such as people, places, and concepts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、これらはビジネスの「名詞」で、通常ユーザー、場所、および概念などのカテゴリに分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Complex reference data, of large quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大量の複雑な参照データ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Examples include customers, vendors, and projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例には、顧客、仕入先、およびプロジェクトが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Document</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">書類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Worksheet data that is converted into transactions later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後でトランザクションに変換されるワークシート データ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Documents that have complex structures, such a several line items for each header record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ヘッダー レコードに対する複数の明細行品目のような複雑な構造体をもつドキュメント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Examples include sales orders, purchase orders, open balances, and journals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例には、販売注文、発注書、オープン残高、 およびジャーナルが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The operational data of the business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネスの運用データ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The operational transaction data of the business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネスの運用トランザクション データ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Posted transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転記済トランザクション。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>These are non‑idempotent items such as posted invoiced and balances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、請求された請求書や残高などの非冪等項目です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Typically, these items are excluded during a full dataset copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、これらの項目は完全なデータセットのコピー中に除外されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Examples include pending invoices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例には保留中の請求書を含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Building an entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>There are multiple ways to create an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを作成するには複数の方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, you can use a wizard, or you can build an entity from a table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ウィザードを使用する、またはテーブルからのエンティティを構築できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Building an entity by using a wizard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードを使用したエンティティの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>The simplest way to build an entity is to use a wizard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティをビルドする最も簡単な方法は、ウィザードを使用することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>This wizard lets you select a root data source and expand to other related data sources, and then select fields for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このウィザードでは、ルート データ ソースを選択して他の関連するデー タソースに展開し、エンティティのフィールドを選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To start the wizard, add a new item of type <bpt id="p1">**</bpt>Data entity<ept id="p1">**</ept> to your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードを開始するには、<bpt id="p1">**</bpt>データ エンティティ<ept id="p1">**</ept> タイプの新しい項目をプロジェクトに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For step-by-step instructions for using the wizard to build an entity, see <bpt id="p1">[</bpt>Building and consuming Data Entities<ept id="p1">](build-consuming-data-entities.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを構築するウィザードを使用するためのステップ バイ ステップの手順については、<bpt id="p1">[</bpt>データ エンティティの構築と消費<ept id="p1">](build-consuming-data-entities.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The following table provides information about the properties that you set for an entity in the wizard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、ウィザードでエンティティに設定したプロパティに関する情報を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Primary data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライマリ データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The root data source (table or view) that is used to construct the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを根ストラクトするために使用されるルート データ ソース (テーブルまたはビュー)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>You can add more related data sources, based on this root data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルート データ ソースに基づき、さらに関連データ ソースを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Data entity name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The name of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Entity category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Thy type of entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのタイプ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Entity categories are similar to table groups for tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのカテゴリは、テーブルのテーブル グループに類似しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>The available categories include <bpt id="p1">**</bpt>Parameter<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Reference<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Master<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Document<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>Transaction<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用可能なカテゴリには、<bpt id="p1">**</bpt>パラメーター<ept id="p1">**</ept>、<bpt id="p2">**</bpt>参照<ept id="p2">**</ept>、<bpt id="p3">**</bpt>マスター<ept id="p3">**</ept>、<bpt id="p4">**</bpt>ドキュメント<ept id="p4">**</ept>、および<bpt id="p5">**</bpt>トランザクション<ept id="p5">**</ept>があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Public entity name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック エンティティ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>The public resource name for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのパブリック リソース名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Public collection name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック コレクション名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The public resource set name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック リソースは名前を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Enable public API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック API の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Select this option to enable the entity for OData services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData サービスのエンティティを有効にするには、このオプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Enable data management capabilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理能力の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Select this option to enable the entity for asynchronous integrations such as data import/export and connector integration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポートおよびコネクタの統合など、エンティティで非同期統合を有効にするには、このオプションを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Staging table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The name of the staging table that will be generated for the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティに対して生成されるステージング テーブルの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The staging table is used in asynchronous integrations and high-volume scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブルは、非同期の統合および大規模なシナリオで使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Adding data sources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>When you build an entity, you start with a root data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティを作成するときは、ルート データ ソースから開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>However, you can add additional data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、他のデータ ソースを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>You can either manually add new data sources, or select a surrogate foreign key field in the root data source to automatically expand the required data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動で新しいデータ ソースを追加するか、ルート データ ソースで代理外部キー フィールドを選択して必要なデータ ソースを自動的に展開することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Output</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>When you complete the wizard, it produces the following items:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードを完了したら、次の項目が生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Data entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Staging table (optional, if data management was enabled)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステージング テーブル (データの管理が有効であった場合は省略可能)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Building an entity from a table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルからエンティティを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You can quickly create an entity from a table, and then customize the properties, data sources, and fields later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルからエンティティを素早く作成して、プロパティ、データ ソース、およびフィールドを後でカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Right-click the table, and then select <bpt id="p1">**</bpt>Addins<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Create data entity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを右クリックし、<bpt id="p1">**</bpt>アドイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>データ エンティティの作成<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Create data entity<ept id="p1">](./media/over5.png)](./media/over5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データ エンティティの作成<ept id="p1">](./media/over5.png)](./media/over5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Entity list refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Entities in an environment must be refreshed using the following guidelines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境のエンティティは、次のガイドラインを使用して更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>When a new environment is deployed and the user navigates to the data management workspace, entity list refresh starts automatically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい環境が展開され、ユーザーがデータ管理ワークスペースに移動すると、エンティティ リストの更新が自動的に開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>When code packages are deployed to an environment where data management has already been used, entity list refresh must be manually started from <bpt id="p1">**</bpt>Data management &gt; Framework parameters &gt; Entity settings &gt; Refresh entity list<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理が既に使用されている環境にコード パッケージが展開されるとき、<bpt id="p1">**</bpt>データ管理 &gt; フレームワーク パラメーター &gt; エンティティ設定 &gt; エンティティ リストの更新<ept id="p1">**</ept> からエンティティ リストの更新はから手動で開始する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>When configuration keys are modified, entity list must be refreshed manually from <bpt id="p1">**</bpt>Data management &gt; Framework parameters &gt; Entity settings &gt; Refresh entity list<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーが変更されるとき、<bpt id="p1">**</bpt>データ管理 &gt; フレームワーク パラメーター &gt; エンティティ設定 &gt; 更新エンティティ リスト<ept id="p1">**</ept> からエンティティ リストを手動で更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Refreshing the entity list ensures all entities are available in the environment and that the entities have the latest metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストを更新すると、環境ですべてのエンティティを使用できるようになり、エンティティのメタデータが最新になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Configuration keys and data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーおよびデータ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Before you use data entities to import or export data, we recommended that you first determine the impact of configuration keys on the data entities that you are planning to use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティを使用してデータをインポートまたはエクスポートする前に、使用を計画しているデータ エンティティでコンフィギュレーション キーの影響を最初に判断することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>To learn more about configuration keys in Finance and Operations, see the <bpt id="p1">[</bpt>License codes and configuration keys report<ept id="p1">](../sysadmin/license-codes-configuration-keys-report.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations でコンフィギュレーション キーの詳細については、<bpt id="p1">[</bpt>ライセンス コードとコンフィギュレーション キーのレポート<ept id="p1">](../sysadmin/license-codes-configuration-keys-report.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Configuration key assignments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの割り当て</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Configuration keys can be assigned to one or all of the following artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーは、次のアーティファクトの 1 つまたはすべてに割り当てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Tables used as data sources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースとして使用されるテーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Table fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Data entity fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>The following table summarizes how configuration key values, on the different artifacts that underlie an object, change the expected behavior of the object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、オブジェクトの基になるさまざまなアーティファクトで、コンフィギュレーション キーの値がオブジェクトの予想される動作を変更する方法を集計したものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Configuration key setting on data entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティでコンフィギュレーション キーを設定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuration key setting on table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルでコンフィギュレーション キーを設定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Configuration key setting on table field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル フィールドでコンフィギュレーション キーを設定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Configuration key on data entity field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ フィールドのコンフィギュレーション キー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Expected behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予想される動作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Not evaluated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Not evaluated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Not evaluated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>If the configuration key for the data entity is disabled, the data entity will not be functional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのコンフィギュレーション キーが無効である場合、データ エンティティは機能しなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>It does not matter whether the configuration keys in the underlying tables and fields are enabled or disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基になるテーブルやフィールド内でコンフィギュレーション キーが有効または無効かどうかは重要ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Not evaluated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Not evaluated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>If the configuration key for a data entity is enabled, the data management framework checks the configuration key on each of the underlying tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのコンフィギュレーション キーが有効である場合、データ管理フレームワークは基になるテーブルごとのコンフィギュレーション キーを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>If the configuration key for a table is disabled, that table will not be available in the data entity for functional use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルのコンフィギュレーション キーが無効である場合、テーブルは機能を使用するデータ エンティティで使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>If a table's configuration key is disabled, the table and data entity configuration key settings are not evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルのコンフィギュレーション キーが無効である場合、テーブルおよびデータ エンティティのコンフィギュレーション キー設定は評価されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If the primary table in the entity has its configuration key disabled, then the system will act as though the entity’s configuration key were disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの主テーブルでそのコンフィギュレーション キーが無効になっている場合、エンティティのコンフィギュレーション キーが無効にされたのと同じように、システムは実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Not evaluated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未評価</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>If the configuration key for a data entity is enabled, and the underlying tables configuration keys are enabled, the data management framework will check the configuration key on the fields in the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのコンフィギュレーション キーが有効で、基になるテーブルのコンフィギュレーション キーが有効である場合、データ管理フレームワークはコンフィギュレーション キーをテーブルのフィールドで確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>If the configuration key for a field is disabled, that field will not be available in the data entity for functional use even if the corresponding data entity field has the configuration key enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドのコンフィギュレーション キーが無効である場合、対応するデータ エンティティ フィールドが有効なコンフィギュレーション キーを持っている場合でも、そのフィールドは使用する機能に対するデータ エンティティを使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>If the configuration key is enabled at all other levels, but the entity field configuration key is not enabled, then the field will not be available for use in the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のすべてのレベルでコンフィギュレーション キーが有効であっても、そのエンティティ フィールドのコンフィギュレーション キーが有効でない場合、フィールドはデータ エンティティで使用不可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>If an entity has another entity as a data source, then the above semantics are applied in a recursive manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティが、データ ソースとして別のエンティティを持っている場合、上記のセマンティクスが再帰的な方法で適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entity list refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>When the entity list is refreshed, the data management framework builds the configuration key metadata for runtime use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストが更新されると、データ管理フレームワークは、ランタイムに使用するコンフィギュレーション キー メタデータを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>This metadata is built using the logic described above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメタデータは上記で説明されたロジックを使用して構築されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>We strongly recommend that you wait for the entity list refresh to complete before using jobs and entities in the data management framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理フレームワークのジョブおよびエンティティを使用する前に、エンティティ リストの更新の完了を待機することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>If you don't wait, the configuration key metadata may not be up to date and could result in unexpected outcomes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">待機しない場合、コンフィギュレーション キー メタデータは最新でない場合があり、予期しない結果になる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>When the entity list is being refreshed, the following message is shown in the entity list page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストが更新される場合、エンティティ リストのページに、次のメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Entity list refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Data entity list page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ リストのページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>The data entity list page in the <bpt id="p1">**</bpt>Data management<ept id="p1">**</ept> workspace shows the configuration key settings for the entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ管理<ept id="p1">**</ept>ワークスペースのデータ エンティティ リストのページは、エンティティのコンフィギュレーション キー設定を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Start from this page to understand the impact of configuration keys on the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのコンフィギュレーション キーの影響を理解するには、このページから開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>This information is shown using the metadata that is built during entity refresh.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの更新中に構築されるメタデータを使用して、この情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The configuration key column shows the name of the configuration key that is associated with the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの列で、データ エンティティに関連付けられているコンフィギュレーション キーの名前が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If this column is blank it means that there is no configuration key associated with the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この列が空白の場合は、データ エンティティに関連付けられているコンフィギュレーション キーがないことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>The configuration key status column shows the state of the configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの状態列は、コンフィギュレーション キーの状態を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>If it has a checkmark, it means the key is enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チェックマークがある場合、キーが有効になっていることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>If it is blank, it means either the key is disabled or there is no key associated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空白の場合、キーが無効であるか、または関連付けられているキーが存在しないかのいずれかであることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Entity list page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストのページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Target fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>The next step is to drill into the data entity to view the impact of configuration keys on tables and fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順は、テーブルおよびフィールドのコンフィギュレーション キーの影響を確認するため、データ エンティティにドリルダウンすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>The target fields form for a data entity shows the configuration key and the key status information for the related tables and fields in the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのターゲット フィールド フォームは、データ エンティティで関連するテーブルおよびフィールドに対して、コンフィギュレーション キーおよびキーの状態情報を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>If the data entity itself has its configuration key disabled, a warning message is shown informing that the tables and fields in the target fields form for this entity will not be available, regardless of their configuration key status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ自体そのコンフィギュレーション キーが無効になっている場合、このエンティティに対するターゲット フィールド フォームで、テーブルおよびフィールドがコンフィギュレーション キーの状態に関係なく使用できないことを通知する、警告メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Target fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Child entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Certain entities have other entities as data sources, or are composite data entities: configuration key information for these entities is shown in the <bpt id="p1">**</bpt>Child entities<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のエンティティはデータ ソースとして他のエンティティを持っているか、複合データ エンティティです: <bpt id="p1">**</bpt>子エンティティ<ept id="p1">**</ept> フォームでこれらのエンティティに対するコンフィギュレーション キー情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Use this form in the similar way to the entities list page described above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のエンティティ リスト ページと同じ方法で、このフォームを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>The target fields form for the child entity also behaves like what is described above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子エンティティのターゲット フィールド フォームも、上記のように機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Target fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Run time validations for configuration keys</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの実行時間の検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Using the configuration key metadata built during entity refresh list, run time validations are performed in the following use cases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ更新リストの中で検構築されたコンフィギュレーション キー メタデータを使用して、次の使用ケースで実行時間の検証が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>When a data entity is added to a job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティをジョブに追加するとき。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>When user clicks <bpt id="p1">**</bpt>Validate<ept id="p1">**</ept> on the entity list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがエンティティ リストで <bpt id="p1">**</bpt>検証<ept id="p1">**</ept> をクリックしたとき。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>When the user loads a data package into a data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがデータ プロジェクトにデータ パッケージを読み込む場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>When the user loads a template into a data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがデータ プロジェクトにテンプレートを読み込む場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>When an existing data project is loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のデータ プロジェクトが読み込まれるとき。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>When a template is loaded into a data project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートがデータ プロジェクトに読み込まれたとき。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Before the export/import job is executed (batch, non-batch, recurring, OData).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート/インポート ジョブが実行される前 (バッチ、非バッチ、反復、OData)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>When the user generates mapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがマッピングを生成するとき。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>When the user maps fields in the mapping UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがマッピング UI のフィールドをマップする場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>When the user adds only 'importable fields'.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが 'インポート可能フィールド' のみを追加するとき。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Managing configuration key changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キー変更の管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Anytime that you update configuration keys at the entity, table, or field level, the entity list in the data management framework must be refreshed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ、テーブル、またはフィールド レベルでコンフィギュレーション キーを更新する時はいつでも、データ管理フレームワークのエンティティ リストを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>This process ensures that the framework picks up the latest configuration key settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスでは、フレームワークが、最新のコンフィギュレーション キー設定をピックアップすることが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Until the entity list is refreshed, the following warning will be shown in the entity list page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ リストが更新されるまで、エンティティ リストのページに、次の警告メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>The updated configuration key changes will take effect immediately after the entity list is refreshed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新されたコンフィギュレーション キーの変更は、エンティティ リストが更新されたすぐ後に、有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>We recommend that you validate existing data projects and jobs to make sure that they function as expected after the configuration keys changes are put in effect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーの変更が有効になった後、期待どおりに動作するかどうかを確認するため、既存のデータ プロジェクトおよびジョブを検証することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Target fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット フィールド</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>