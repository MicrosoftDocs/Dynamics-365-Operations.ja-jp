<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="design-best-practices.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>design-best-practices.3cd2ca.6e4ff2a805b73a3036b6acd31f6fcf81e9b901c0.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6e4ff2a805b73a3036b6acd31f6fcf81e9b901c0</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\design-best-practices.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Design principles and best practices for data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティに関する設計原則とベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes design principles for data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、データ エンティティの設計原則について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It also includes guidelines for the names of data entities, fields, relation roles, roles, and OData EntityTypes and EntitySets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、データ エンティティ、フィールド、関係のロール、ロールの名前、OData EntityType および EntitySet のガイドラインも含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Design principles and best practices for data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティに関する設計原則とベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article describes design principles for data entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、データ エンティティの設計原則について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It also includes guidelines for the names of data entities, fields, relation roles, roles, and OData EntityTypes and EntitySets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、データ エンティティ、フィールド、関係のロール、ロールの名前、OData EntityType および EntitySet のガイドラインも含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Entity design principles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ デザインの原則</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A data entity should provide a holistic object that encapsulates the relevant business logic in a single consumable contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティは、1 つの消耗契約に関連するビジネス ロジックをカプセル化する総合的なオブジェクトを提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The contract is then exposed through application interfaces (APIs), such as OData, import and export, integration, and the programming model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">契約は、OData、インポートとエクスポート、統合、プログラミング モデルなどのアプリケーション インターフェイス (API) を通じて公開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Each data entity should be designed to meet the following goals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各データ エンティティでは、以下の目標を達成するように設計する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Encapsulation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カプセル化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Each entity should provide an abstraction between the physical data model and the consumer of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各エンティティは、物理データ モデルとエンティティのコンシューマー間の抽象化を提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The entity should encapsulate the underlying tables that, together, can define an object that has a specific purpose in the business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティは、ビジネスにおいて特定の目的を持つオブジェクトをまとめて定義できる、基になるテーブルをカプセル化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Consumers of the entity might be form clients, services, and integration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの消費者は、クライアント、サービス、および統合を形成する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Each entity should encapsulate multiple related tables to represent the domain object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各エンティティは、ドメイン オブジェクトを表す複数の関連するテーブルをカプセル化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In some situations, single table entities are acceptable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、1 つのテーブルのエンティティが許容されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>A single public contract</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのパブリック契約</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The public contract for an entity should be the same across all integration end points.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのパブリック契約は、すべての統合エンドポイントで同じである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, the customer entity must expose the same fields or API to both OData and import/export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客エンティティは、同じフィールドまたは OData およびインポート/エクスポートの両方への API を公開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This principle guarantees that the published schema for an entity is consistent, regardless of the mechanism for consumer interaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この原則は、エンティティの公開されたスキーマが、消費者のインタラクションの仕組みにかかわらず一貫していることを保証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>When an entity is consumed, the business logic that is executed within the entity during CRUD operations must not vary based on the type of consumer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティが使用されるとき、CRUD 操作時にエンティティ内で実行されるビジネス ロジックは消費者のタイプによって変化することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Simplicity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シンプルさ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The consumer of an entity should be able to interact with the entity based on the accepted industry or domain definitions of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのコンシューマーは、エンティティの受け入れられた業種またはドメイン定義に基づいてエンティティと対話することができる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The behavior details of the entity should be kept hidden and should be prevented from distorting the interaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの動作の詳細は、表示されないままにし、相互作用に影響しないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The consumer of an entity must be able to interact with the entity by using the natural key of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのコンシューマーは、エンティティのナチュラル キーを使用してエンティティと対話できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The consumer must not be required to use any keys that are implementation-specific, such as any surrogate key that it generates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンシューマーは、生成する代理キーなど、実装固有のキーを使用する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Naming guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付けのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Data entity names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Do</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Don’t</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行しない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Prefix the name with standard prefixes, because of the lack of namespaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前空間がないため、名前の先頭に標準の接頭語を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Don't include underscores in names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前にアンダースコアを含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Add the postfix "Entity" to the name to prevent conflicts with tables and classes that have the same prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前に接尾語「エンティティ」を追加して、同じ接頭語を持つテーブルとクラスとの競合を避けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Don't use abbreviations in conceptual names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概念の名前に省略形を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Give the entity a conceptual name that is aligned with the name in the en-us UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティに、en-us UI の名前と合致している概念の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For example, the conceptual name of the entity that exposes records from the InventTable table should be named <bpt id="p1">**</bpt>ReleasedProduct<ept id="p1">**</ept>, so that the full name of the entity will be <bpt id="p2">**</bpt>EcoResReleasedProductEntity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、InventTable テーブルからレコードを公開するエンティティ概念の名前は <bpt id="p1">**</bpt>ReleasedProduct<ept id="p1">**</ept> と呼ばれ、エンティティの正式名称は <bpt id="p2">**</bpt>EcoResReleasedProductEntity<ept id="p2">**</ept> となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Result:<ept id="p1">**</ept> <ph id="ph1">&amp;lt;</ph>prefix<ph id="ph2">&amp;gt;</ph><ph id="ph3">&amp;lt;</ph>ConceptualName<ph id="ph4">&amp;gt;</ph>Entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>結果:<ept id="p1">**</ept> <ph id="ph1">&amp;lt;</ph>接頭語<ph id="ph2">&amp;gt;</ph><ph id="ph3">&amp;lt;</ph>ConceptualName<ph id="ph4">&amp;gt;</ph>エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Data entity field names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ フィールド名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Do</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Don’t</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行しない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Give the field name a conceptual name that is aligned with the name in the en-us UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名に、en-us UI の名前と合致している概念の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For example, use <bpt id="p1">**</bpt>ItemNumber<ept id="p1">**</ept> instead of <bpt id="p2">**</bpt>ItemID<ept id="p2">**</ept> as the field name to align with the UI, where the label is <bpt id="p3">**</bpt>Item number<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p2">**</bpt>ItemID<ept id="p2">**</ept> の代わりに <bpt id="p1">**</bpt>ItemNumber<ept id="p1">**</ept> を UI に対応するフィールド名として使用し、ラベルは<bpt id="p3">**</bpt>品目番号<ept id="p3">**</ept>になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Don't include prefixes in field names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名に接頭語を含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>For example, a field should not be named <bpt id="p1">**</bpt>InventLocationId<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、フィールドには <bpt id="p1">**</bpt>InventLocationId<ept id="p1">**</ept> という名前を付ける必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Add the postfix "ID," "Number," and so on, to the name of a field that is part of foreign keys to prevent collision with the navigation properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部キーの一部であるフィールドの名前に接尾語「ID」、「番号」などを追加して、ナビゲーション プロパティとの競合を防ぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For example, use <bpt id="p1">**</bpt>WarehouseID<ept id="p1">**</ept> instead of <bpt id="p2">**</bpt>Warehouse<ept id="p2">**</ept> as a field name, because <bpt id="p3">**</bpt>Warehouse<ept id="p3">**</ept> is the navigation method to the <bpt id="p4">**</bpt>Warehouse<ept id="p4">**</ept> entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p2">**</bpt>倉庫<ept id="p2">**</ept>の代わりに <bpt id="p1">**</bpt>WarehouseID<ept id="p1">**</ept> をフィールド名として使用します。それは<bpt id="p3">**</bpt>倉庫<ept id="p3">**</ept>が、<bpt id="p4">**</bpt>倉庫<ept id="p4">**</ept>エンティティへのナビゲーション メソッドであるからです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Don't include country/region-specific postfixes in field names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名に国または地域固有の接尾語を含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>For example, a field should not be named <bpt id="p1">**</bpt>InventoryProfileID<ph id="ph1">\_</ph>RU<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、フィールドには <bpt id="p1">**</bpt>InventoryProfileID<ph id="ph1">\_</ph>RU<ept id="p1">**</ept> という名前を付ける必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Don't include underscores in field names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド名にアンダースコアを含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Don't use abbreviations in field names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの名前に省略形を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Data entity relation role names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ リレーションのロール名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Do</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Don’t</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行しない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Use the plural form when you name roles that have a cardinality that is higher than 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 より大きいカーディナリティを持つロールに名前を付けるときは、複数形を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For example, the foreign key on Customer to Party should have the role name of Customers, because the cardinality from Party to Customer is 0...N.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、関係者への顧客の外部キーには、顧客のロール名が必要で、それは顧客への関係者からの基数が 0...N であるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Don't include prefixes in relation role names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーション ロール名に接頭語を含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, don’t use the name <bpt id="p1">**</bpt>WMSWarehouseLocation<ept id="p1">**</ept>, even though the referenced entity includes the prefix "WMS."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、参照されるエンティティに接頭語「WMS」が含まれていても、<bpt id="p1">**</bpt>WMSWarehouseLocation<ept id="p1">**</ept> の名前は使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Use the singular form when you name roles that have a cardinality of 0 (zero) or 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カーディナリティが 0 (ゼロ) または 1 のロールに名前を付ける場合は、単数形を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>For example, the foreign key on Worker to Person should have the role name of Worker, because the cardinality from Person to Worker is 0..1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、個人への作業者の外部キーには、作業者のロール名が必要で、それは作業者への個人からの基数が 0..1 であるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Don't add the postfix "Entity" to relation role names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ロール名に接尾語「エンティティ」を追加しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For example, don’t use the role name <bpt id="p1">**</bpt>WarehouseEntity<ept id="p1">**</ept> in a relationship, even though the referenced entity includes the name "Entity."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、参照されるエンティティが「エンティティ」の名前を含んでいても、関係でロール名 <bpt id="p1">**</bpt>WarehouseEntity<ept id="p1">**</ept> を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Instead, use the name <bpt id="p1">**</bpt>Warehouse<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">**</bpt>倉庫<ept id="p1">**</ept>という名前を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Consider adding the role of the relationship as a prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係の役割を接頭語として追加することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>For example, to clearly describe the role of the relationship, name a relationship <bpt id="p1">**</bpt>BuyingLegalEntity<ept id="p1">**</ept> instead of <bpt id="p2">**</bpt>LegalEntity<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、関係のロールを明確に説明するには、<bpt id="p2">**</bpt>LegalEntity<ept id="p2">**</ept> の代わりに、関係の <bpt id="p1">**</bpt>BuyingLegalEntity<ept id="p1">**</ept> に名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Don't add country/region-specific postfixes to relation role names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">国または地域固有の接尾語を関係ロール名に追加しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For example, don’t use the role name <bpt id="p1">**</bpt>InventoryProfile<ph id="ph1">\_</ph>RU<ept id="p1">**</ept>, even though the relationship applies only in an RU country/region format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、RU 国/地域の形式にのみ関係が適用される場合でも、ロール名 <bpt id="p1">**</bpt>InventoryProfile<ph id="ph1">\_</ph>RU<ept id="p1">**</ept> を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Don't include underscores in relation role names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーション ロール名にアンダースコアを含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Data entity relation names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティのリレーション名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Do<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実行<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Give the relation name the same name as the related role name, in singular form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーション名に、単一のフォームで関連するロール名として同じ名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>For example, the relation that describes the foreign key from Customer to Party should be named <bpt id="p1">**</bpt>Party<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客から関係者への外部キーを説明する関係は、<bpt id="p1">**</bpt>関係者<ept id="p1">**</ept>と呼ばれる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>OData EntityType names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData EntityType 名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Do<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実行<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Give the EntityType a conceptual name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EntityType に概念の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The name should be the same as the conceptual name of the data entity, but without the prefix and without the "Entity" postfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前は、データ エンティティの概念の名前と同じでなければなりませんが、接頭語はなく、「エンティティ」接尾語はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>For example, <bpt id="p1">**</bpt>EcoResReleasedProductEntity<ept id="p1">**</ept> becomes <bpt id="p2">**</bpt>ReleasedProduct<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>EcoResReleasedProductEntity<ept id="p1">**</ept> は <bpt id="p2">**</bpt>ReleasedProduct<ept id="p2">**</ept> になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Name the EntityType in singular form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一フォームで EntityType の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>OData EntitySet (Entity Collection) names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData EntitySet (エンティティ コレクション) 名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Do<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実行<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Name the EntitySet in plural form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数フォームで EntitySet の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For example, the EntitySet for the <bpt id="p1">**</bpt>ReleasedProduct<ept id="p1">**</ept> EntityType is <bpt id="p2">**</bpt>ReleasedProducts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>ReleasedProduct<ept id="p1">**</ept> EntityType の EntitySet は <bpt id="p2">**</bpt>ReleasedProducts<ept id="p2">**</ept> です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>