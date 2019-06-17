<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="NamingGuidelines.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>NamingGuidelines.8eb8b7.acc8d70394c41cba51f8a7cebb75b8750ea72651.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>acc8d70394c41cba51f8a7cebb75b8750ea72651</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\NamingGuidelines.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Naming guidelines for extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の名前付けのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the naming guidelines for extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張機能の名前付けガイドラインについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Naming guidelines for extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の名前付けのガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Naming model elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル要素に名前を付ける</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Any element in a model must be given a name, which is unique across all models at installation time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル内の要素には、インストール時にすべてのモデルで一意の名前を付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Given that all potential models, that your model will be installed together with, are unknown at implementation time, then every element name should include a prefix, which is specific to your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての潜在的なモデルの場合、実装時に共にインストールされるモデルは不明であり、すべての要素名にはソリューション固有の接頭辞が含まれる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If a model contains multiple solutions, then each solution within the model can be identified by different prefixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルに複数のソリューションが含まれている場合は、さまざまな接頭語によって、モデルでは、各ソリューションを識別できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The prefix must be carefully chosen to minimize the risk that other models from other parties have chosen the same prefix for their elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接頭語の選択は、他の関係者からの他のモデルの要素に同じ接頭語が選択されるというリスクを最小限に抑えるように慎重に行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>By including the prefix when naming elements in your model, then you have significantly lowered the risk of naming conflicts, when your model is later installed alongside other models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルに要素の名前を付けるときに接頭語を含めると、モデルが他のモデルと一緒に後でインストールされるときに名前の競合のリスクが大幅に引き下げられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>When you extend functionality in other models, then elements being extended already contains a prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のモデル内の機能を拡張するとき、拡張される要素には接頭語がすでに含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Instead of adding your prefix to the extension elements resulting in multiple prefixes after each other, then you should rather include your prefix or another term or abbreviation as an infix when naming the extension element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接頭語を拡張要素に追加し、それぞれの後に複数の接頭語を続けずに、拡張要素に名前を付けるときに接頭語やその他の語句、省略形をインフィックスとして含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Here are details about the specific naming of extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の特定の名前付けに関する詳細を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Naming Extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能に名前を付ける</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>An extension element, i.e. table extension, view extension, form extension, etc.,  must be given a unique name, that minimizes the risk of conflicts with extensions in other models; both now and in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張要素、すなわちテーブル拡張子、ビュー拡張子、フォーム拡張子など、他のモデルの拡張子と競合のリスクを最小限にする一意の名前を付ける必要があります。現在と将来の両方で行なえます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To minimize the risk of conflicts, the name should therefore include a term, abbreviation or infix, that distinguishes the extension from other extension to the same element in other models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">競合のリスクを最小限に抑えるために、名前には、拡張機能を他のモデル内の同じ要素の他の拡張機能と区別するための用語、省略形、または接中辞が含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> include either the name of the model in which the extension element resides, or the prefix the extension is associated with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必ず<ept id="p1">**</ept>拡張要素が存在するモデルの名前、または拡張子が関連付けられている接頭辞のいずれかを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>An extension of the HCMWorker table by a Warehousing module using the WHS prefix to name all other elements, could be named HCMWorker.WHSExtension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WHS 接頭語を使用してその他すべての要素の名前を付ける HCMWorker テーブルの拡張クラスは、ウェアハウジング モジュールにより HCMWorker.WHSExtension という名前を付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The prefix used to name other elements in the module, is inserted as an infix in the name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール内の他の要素に名前を付けるために使用される接頭語は、接中辞として挿入されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>An extension of the ContactPerson table in the ApplicationSuite could be named ContactPerson.ApplicationSuiteExtension, if the extension is meant to contain all extensions to the ContactPerson table from the ApplicationSuite model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ApplicationSuite の ContactPerson テーブルの拡張子は、ApplicationSuite モデルから ContactPerson テーブルへすべての拡張機能を含む拡張子である場合、ContactPerson.ApplicationSuiteExtension という名前を付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> suffix the name with the term Extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必ず<ept id="p1">**</ept>末尾に Extension という用語を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>An extension of the InventLocation table should follow the following pattern InventLocation.<ph id="ph1">&lt;Model&gt;</ph>Extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventLocation テーブルの拡張は、次のパターン InventLocation に従う必要があります。<ph id="ph1">&lt;Model&gt;</ph>拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> NOT name the extension simply as <ph id="ph1">&lt;ElementBeingExtended&gt;</ph>.Extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子に <ph id="ph1">&lt;ElementBeingExtended&gt;</ph>.Extension のような簡単な名前を<bpt id="p1">**</bpt>つけないで<ept id="p1">**</ept>ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>An extension of the InventLocation table must not be named InventLocation.Extension, as the risk of conflicts is too high.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">競合のリスクが高すぎるため、InventLocation テーブルの拡張子は InventLocation.Extension という名前を付けることができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Naming Extension classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスの名前を付ける</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Extension classes used to augment logic on tables, classes, or other elements which can be extended through augmentation, need to be given a name which is unique across all types in all models; both now and in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">強化を介して拡張可能なテーブル、クラス、または他の要素ロジックを拡張するために使用される拡張子クラスには、すべてのモデルのすべてのタイプで一意の名前を付ける必要が今後もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>It is preferable that the extension class includes the name of the type being extended, but at the same time, the name must also include a term, abbreviation or prefix, that distinguishes the class from other types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスに拡張されている型の名前を含めることは望ましいですが、同時に、その名前にその他の型とクラスを区別する用語、省略形または接頭語も含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> start the name of the extension class with the name of the type being augmented, and end it with the term _Extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必ず<ept id="p1">**</ept>拡張クラスの名前を強化された型の名前で開始し、_Extension という用語で終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>An extension class augmenting the ContactPerson table should start with the name ContactPerson, and end with _Extension, e.g. ContactPersonWHS_Extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ContactPerson テーブルを増補する拡張クラスは、ContactPerson という名前で開始し、_Extension、および ContactPersonWHS_Extension などで終了する必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> include either the name of the model in which the extension element resides, or the prefix the extension is associated with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必ず<ept id="p1">**</ept>拡張要素が存在するモデルの名前、または拡張子が関連付けられている接頭辞のいずれかを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>An extension class augmenting the ContactPerson table by a Warehousing module using the WHS prefix to name all other elements, could be named ContactPersonWHS_Extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WHS 接頭語を使用してその他すべての要素の名前を付ける ContactPerson テーブルを拡張する拡張クラスは、ウェアハウジング モジュールにより ContactPersonWHS_Extension という名前付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The prefix used to name other elements in the module, is inserted as an infix in the name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール内の他の要素に名前を付けるために使用される接頭語は、接中辞として挿入されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>An extension class augmenting the ContactPerson table in the ApplicationSuite model could be named ContactPersonApplicationSuite_Extension, if the extension class is meant to contain all extension to the ContactPerson table in the ApplicationSuite model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ApplicationSuite モデルの ContactPerson テーブル を増補する拡張クラスは、拡張クラス ApplicationSuite の ContactPerson テーブルへすべての拡張機能を含む拡張をしている場合、ContactPersonApplicationSuite 拡張子という名前にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>DO NOT<ept id="p1">**</ept> name the extension simply as <ph id="ph1">&lt;ElementBeingExtended&gt;</ph>_Extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子に <ph id="ph1">&lt;ElementBeingExtended&gt;</ph>_Extension のような簡単な名前を<bpt id="p1">**</bpt>つけないでください<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>An extension class augmenting the InventLocation table must not be named InventLocation_Extension, as the risk of conflicts is too high.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">競合のリスクが高すぎるため、InventLocation テーブルを増補する拡張クラスは InventLocation_Extension という名前を付けることができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Naming Fields, Field groups, Indexes, Relations and other metadata nodes in Extension elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張要素のフィールド、フィールド グループ、インデックス、関係およびその他のメタデータ ノードに名前を付ける</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Fields, indexes, relations and other metadata elements on extension elements also need be unique across both the element being extended as well as other extension elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張要素のフィールド、インデックス、関係、およびその他のメタデータ要素は、その他の拡張要素と同じように、拡張されている両方の要素間で一意である必要もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>These metadata nodes therefore also need to include a term, abbreviation or prefix, that limits the risk of conflicts across models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらのメタデータ ノードには、モデル間の競合のリスクを制限する用語、省略形または接頭辞も含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> include a prefix, term, or abbreviation in the beginning of the metadata node name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必ず<ept id="p1">**</ept>メタデータ ノードの名前の先頭に接頭語、用語、または省略形を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>An approving worker foreign key field added to as part of a table extension could be named WHSApprovingWorker, assuming WHS is one of prefixes dedicated to other elements in the hosting model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">承認する作業者の外部キー フィールドは、テーブルの拡張機能の一部として追加され、WHS がホスティング モデル内の他の要素の専用接頭語の 1 つとして想定した場合 WHSApprovingWorker という名前を付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Naming members in extension classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラス内のメンバーの名前を付ける</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Class level variables, and methods on extension classes must be provided a name that is unique across the type being augmented, and all other extension classes augmenting the same type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス レベルの変数、および拡張クラスのメソッドには、拡張される型全体で一意の名前と、同じタイプを拡張する他のすべての拡張クラスを指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>DO<ept id="p1">**</ept> include a prefix, term, or abbreviation in the beginning of the member name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必ず<ept id="p1">**</ept>メンバー名の先頭に接頭辞、用語、または省略形を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>An approving worker class level variable could be named WHSApprovingWorker, if WHS is one of the prefixes used by other element in the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WHS がモデル内の他の要素で使用される接頭語の 1 つである場合、承認する作業者クラス レベルの変数に WHSApprovingWorker という名前を付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>An approveWork method could be named WHSApproveWork, if WHS is one of the prefixes used by other elements in the hosting model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WHS がホスティング モデルの他の要素で使用される接頭語の 1 つである場合、approveWork メソッドは WHSApproveWork という名前を付けることができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>