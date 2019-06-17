<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="maps-with-versioning.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>maps-with-versioning.f3ad5b.d44391c1d630c5aea686e65a016fc33137edeb26.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d44391c1d630c5aea686e65a016fc33137edeb26</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\maps-with-versioning.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend table maps that are used for versioning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン管理で使用されるテーブル マップの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to extend table maps that can be used for versioning.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、バージョン管理に使用できるテーブル マップを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend table maps that are used for versioning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン管理で使用されるテーブル マップの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic applies to Dynamics 365 for Finance and Operations, Enterprise edition 7.3 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Finance and Operations, Enterprise edition 7.3 およびそれ以降に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>PurchLineMap table map logic</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PurchLineMap テーブル マップ ロジック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When new fields are added to the <bpt id="p1">**</bpt>PurchLine<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PurchLineHistory<ept id="p2">**</ept> tables using table extensions, the new fields must be copied between the tables when a purchase order is versioned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル拡張機能を使用して新しいフィールドが <bpt id="p1">**</bpt>PurchLine<ept id="p1">**</ept> および <bpt id="p2">**</bpt>PurchLineHistory<ept id="p2">**</ept> テーブルに追加された場合、発注書のバージョンが更新されるときに、新しいフィールドをテーブル間でコピーする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The <bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> table map specifies the fields that must be copied between the <bpt id="p2">**</bpt>PurchLine<ept id="p2">**</ept> table and the <bpt id="p3">**</bpt>PurchLineHistory<ept id="p3">**</ept> table when a new purchase order version is created or edited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> テーブル マップは、新しい購買注文バージョンが作成または編集されたときに <bpt id="p2">**</bpt>PurchLine<ept id="p2">**</ept> テーブルおよび <bpt id="p3">**</bpt>PurchLineHistory<ept id="p3">**</ept> テーブルの間でコピーする必要があるフィールドを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To accomplish this, extend the <bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> map table to include the additional fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うためには、<bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> マップ テーブルを拡張してフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Additionally, the <bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> is used by the <bpt id="p2">**</bpt>VersioningPurchaseOrder<ept id="p2">**</ept> class when archiving purchase order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> は、購買注文明細行をアーカイブするとき、<bpt id="p2">**</bpt>VersioningPurchaseOrder<ept id="p2">**</ept> によって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The model is shown in the following diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このモデルを次の図に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>VersioningPurchaseOrder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VersioningPurchaseOrder</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To be able to specify new fields to be copied, the <bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept> table map logic and its usage have been refactored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーする新しいフィールドを指定できるようにするため、<bpt id="p1">**</bpt>PurchLineMap<ept id="p1">**</ept>テーブル マップ ロジックとその使用がリファクタリングされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The copy logic has been moved to the <bpt id="p1">**</bpt>PurchLineVersioning<ept id="p1">**</ept> class, so the <bpt id="p2">**</bpt>VersioningPurchaseOrder<ept id="p2">**</ept> class references the <bpt id="p3">**</bpt>PurchLineVersioning<ept id="p3">**</ept> class instead of the <bpt id="p4">**</bpt>PurchLineMap<ept id="p4">**</ept> table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピー ロジックが <bpt id="p1">**</bpt>PurchLineVersioning<ept id="p1">**</ept> 移動されているため、<bpt id="p2">**</bpt>VersioningPurchaseOrder<ept id="p2">**</ept> クラスは<bpt id="p4">**</bpt>PurchLineMap<ept id="p4">**</ept> テーブルマップの代わりに、<bpt id="p3">**</bpt>PurchLineVersioning<ept id="p3">**</ept> を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>PurchLineVersioning<ept id="p1">**</ept> class delegates the logic to copy the fields and the logic to determine whether a confirmation is required from the classes that implement the <bpt id="p2">**</bpt>PurchLineIVersioningFieldSet<ept id="p2">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchLineVersioning<ept id="p1">**</ept> クラスは、フィールドをコピーするロジックや、<bpt id="p2">**</bpt>PurchLineIVersioningFieldSet<ept id="p2">**</ept>インターフェイス を実行するクラスからの確認が必須かどうかを決定するロジックを委任します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Each class that implements the interface is associated with a table map that specifies the fields to copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターフェイスを実装する各クラスは、コピーするフィールドを指定するテーブル マップに関連付けられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The <bpt id="p1">**</bpt>PurchLineDictVersioning<ept id="p1">**</ept> class instantiates the <bpt id="p2">**</bpt>PurchLineIVersioningFieldSet<ept id="p2">**</ept> object using reflection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchLineDictVersioning<ept id="p1">**</ept> クラスは、リフレクションを使用して <bpt id="p2">**</bpt>PurchLineIVersioningFieldSet<ept id="p2">**</ept> オブジェクトをインスタンス化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>PurchLineDictVersioning<ept id="p1">**</ept> class collects the entire set of fields which need to be copied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchLineDictVersioning<ept id="p1">**</ept> クラスは、コピーする必要があるフィールドのセット全体を収集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The field data is collected based on all the table maps associated with a class that implements <bpt id="p1">**</bpt>PurchLineIVersioningFieldSet<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドデータは、<bpt id="p1">**</bpt>PurchLineIVersioningFieldSet<ept id="p1">**</ept> を実装するクラスに関連付けられているすべてのテーブル マップに基づいて収集されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following diagram displays the new classes and their dependencies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、新しいクラスとその依存関係を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>How to extend PurchLine and PurchLineHistory tables with new fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフィールドで PurchLine および PurchLineHistory テーブルを拡張する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Suppose that you want the ISVModule2 model to extend the <bpt id="p1">**</bpt>PurchLine<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PurchLineHistory<ept id="p2">**</ept> tables with new fields that must be copied when creating a new version of a purchase order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書の新しいバージョンを作成するときにコピーする必要がある新しいフィールドを持つ <bpt id="p1">**</bpt>PurchLine<ept id="p1">**</ept> および <bpt id="p2">**</bpt>PurchLineHistory<ept id="p2">**</ept> テーブルを拡張するために、ISVModule2 モデルが必要であるとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>You must have developer access to the ISVModule2 model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISVModule2 モデルに開発者がアクセスできる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To complete this task, you must perform the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクを完了するには、次の手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Add fields by using table extensions to the <bpt id="p1">**</bpt>PurchLine<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PurchLineHistory<ept id="p2">**</ept> tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchLine<ept id="p1">**</ept> と <bpt id="p2">**</bpt>PurchLineHistory<ept id="p2">**</ept> テーブルへのテーブル拡張機能を使用して、フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create a new table map containing the fields that must be copied, and implement the new table map on the two new table extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーする必要があるフィールドを含む新しいテーブル マップを作成し、2 つの新しいテーブル拡張で新しいテーブル マップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Create a new class to implement the <bpt id="p1">**</bpt>PurchLineIVersioningFieldSet<ept id="p1">**</ept> interface and implement the following required methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスを作成して <bpt id="p1">**</bpt>PurchLineIVersioningFieldSet<ept id="p1">**</ept> インターフェースを実装し、以下の必須メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>copyVersion<ept id="p1">**</ept> method - Copies data between two records of the new table map type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>copyVersion<ept id="p1">**</ept> メソッド - 新しいテーブル マップの 2 つのレコード間でデータをコピーをします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>fieldSetTableMapId<ept id="p1">**</ept> method - Returns the ID of the new table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>fieldSetTableMapId<ept id="p1">**</ept> メソッド - は新しいテーブルマップの ID を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>isChangeConfirmationRequired<ept id="p1">**</ept> method - Returns true or false based on whether the change to the newly added field values requires a confirmation to be created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>isChangeConfirmationRequired<ept id="p1">**</ept> メソッド - 新しく追加されたフィールド値が必要とする作成された確認への変更に基づいて、true または false を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The classes, interfaces, and extensions described in these steps are shown in the following diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順で説明するクラス、インターフェイス、および拡張機能を次の図に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>MapClassExtensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MapClassExtensions</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>