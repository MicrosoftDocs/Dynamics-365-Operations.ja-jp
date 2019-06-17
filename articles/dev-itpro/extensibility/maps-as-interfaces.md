<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="maps-as-interfaces.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>maps-as-interfaces.531bfd.c8b71fe1e49c5c1db148e9710a1c64730c5d3a7e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c8b71fe1e49c5c1db148e9710a1c64730c5d3a7e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\maps-as-interfaces.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend table maps that are used as interfaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターフェイスとして使用されるテーブル マップの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to extend table maps that are used as interfaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、インターフェイスとして使用されるテーブル マップを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend table maps that are used as interfaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターフェイスとして使用されるテーブル マップの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The <bpt id="p1">**</bpt>SalesPurchLine<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> table maps expose a set of common fields and methods that are used by a variety of product features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesPurchLine<ept id="p1">**</ept> および <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> テーブル マップは、さまざまな製品機能により使用される一般的なフィールドおよびメソッドのセットを公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The mapping of fields and the implementation of methods have been refactored into a class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドのマッピングとメソッドの実装は、クラス階層にリファクタリングされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Some of these changes include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更の一部は以下のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Methods on the table maps have been moved to the class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップのメソッドは、クラス階層に移動されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Fields are exposed through parm-methods on the class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドは、クラス階層で parm メソッドを通して公開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The table map still exists and tables still implement the mapping to the table map, but the fields on the table map have been made obsolete, and field mapping has been removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップは引き続き存在し、テーブル マップへのマッピングも引き続き実装されていますが、テーブル マップのフィールドは廃止され、フィールド マッピングは削除されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The methods on the table map have been made obsolete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップ上のメソッドは廃止されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>SalesPurchTableInterface hierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SalesPurchTableInterface 階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The new <bpt id="p1">**</bpt>SalesPurchTableInterface<ept id="p1">**</ept> class is the abstract base class for the ApplicationSuite functionality that has been introduced by the refactoring of the <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい <bpt id="p1">**</bpt>SalesPurchTableInterface<ept id="p1">**</ept> クラスは、<bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> テーブル マップのリファクタリングによって導入された ApplicationSuite 機能の抽象基本クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The class contains abstract methods for fields and methods, which must exist for each table implementing the interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスにはフィールドとメソッドの抽象メソッドが含まれています。これらはインターフェイスを実装する各テーブルに存在している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It also contains the default logic in methods, which is common across all implementations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、メソッドに既定のロジックを含めることができ、すべての実装においてよく用いられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Each table that implements the <bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> table map must be represented as a derived class in the <bpt id="p2">**</bpt>SalesPurchTableInterface<ept id="p2">**</ept> class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> テーブル マップを実装する各テーブルは、<bpt id="p2">**</bpt>SalesPurchTableInterface<ept id="p2">**</ept> クラスの階層の派生クラスとして表す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Each derived class must be decorated with a <bpt id="p1">**</bpt>SalesPurchTableInterfaceFactory<ept id="p1">**</ept> attribute class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各派生クラスは、<bpt id="p1">**</bpt>SalesPurchTableInterfaceFactory<ept id="p1">**</ept> 属性クラスで修飾される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The attribute is used to associate the derived class with the table, so that it is possible to instantiate a class of the correct type depending on a <bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性を使用して派生クラスをテーブルに関連付けます。これで、<bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> レコードに応じて、適切なタイプのクラスのインスタンスを作成できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>MapsAsInterfaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MapsAsInterfaces</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Even though the table map methods have been made obsolete, the corresponding methods still exist on the implementing tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップ メソッドが廃止されたにもかかわらず、対応するメソッドはまだ実装テーブルに存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The logic in these methods have been refactored from delegating calls to the method on the table map, to the corresponding method on the base class of the hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドのロジックは、テーブル マップのメソッドへの呼び出しを階層の基本クラスの対応するメソッドにデリゲートすることからリファクタリングされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Extension scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In this example, if you want your ISVModule2 model to extend the interface class hierarchy and the tables implementing the <bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> table map, you must perform the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、ISVModule2 モデルによってインターフェイス クラス階層と <bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> テーブル マップを実装しているテーブルを拡張させる場合、次の手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Add the fields and methods through table extension to the necessary tables implementing the <bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> テーブル マップを実装する必要なテーブルに、テーブル拡張機能を使用してフィールドとメソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Create a new interface class hierarchy, which exposes the new fields as parm-methods and other additional methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新規のインターフェイス クラス階層を作成し、新しいフィールドを parm メソッドやその他の追加メソッドとして公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The base class of the class hierarchy must be concrete and not abstract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス階層構造の基本クラスは、具体的であり、抽象的ではない必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create derived classes for each table that has been extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張された各テーブルの派生クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Decorate each derived class with the <bpt id="p1">**</bpt>SalesPurchTableInterfaceFactory<ept id="p1">**</ept> attribute class to associate the class with the correct table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各派生クラスを <bpt id="p1">**</bpt>SalesPurchTableInterfaceFactory<ept id="p1">**</ept> 属性クラスで修飾し、クラスを正しいテーブルに関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Create a static factory method on the base class of the new class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラス階層の基本クラスに静的ファクトリ メソッドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The factory method should instantiate the proper derived class that leverages the <bpt id="p1">**</bpt>SalesPurchTableInterfaceFactory<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドは、<bpt id="p1">**</bpt>SalesPurchTableInterfaceFactory<ept id="p1">**</ept> 属性を利用する適切な派生クラスをインスタンス化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If no derived class can be found, then an instance of the base class must be returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">派生クラスが見つからない場合は、基本クラスのインスタンスを戻す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Create an extension class of the <bpt id="p1">**</bpt>SalesPurchTableInterface<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesPurchTableInterface<ept id="p1">**</ept> クラスの拡張クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The class augments the <bpt id="p1">**</bpt>SalesPurchTableInterface<ept id="p1">**</ept> class with a method that creates an instance from the new class hierarchy by calling the factory method on the new class hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、<bpt id="p1">**</bpt>SalesPurchTableInterface<ept id="p1">**</ept> クラスを、新しいクラス階層のファクトリ メソッドを呼び出して新しいクラス階層からインスタンスを作成するメソッドで補強します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The class and extensions described above are shown in the following diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のクラスと拡張機能は、次の図に示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>MapsAsInterfacesWalkThrough</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MapsAsInterfacesWalkThrough</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The diagram contains an ISVModule1 model, which includes the <bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> table that implements the <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> table map and contains its own <bpt id="p3">**</bpt>SalesPurchTableInterface<ept id="p3">**</ept> derived class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この図には、<bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> を実装する <bpt id="p2">**</bpt>ISV1Header<ept id="p2">**</ept> テーブルを含み、独自の <bpt id="p3">**</bpt>SalesPurchTableInterface<ept id="p3">**</ept> 派生クラスを含む ISVModule1 モデルが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The model is independent of the ISVModule2, so when logic in the ISVModule2 creates an instance from the <bpt id="p1">**</bpt>ISV2SalesPurchTableInterface<ept id="p1">**</ept> class hierarchy, then an instance of the base class will be returned when the <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> record is of type <bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このモデルは ISVModule2 から独立しているため、ISVModule2 のロジックが、<bpt id="p1">**</bpt>ISV2SalesPurchTableInterface<ept id="p1">**</ept> クラス階層からインスタンスを作成すると、<bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> レコードが <bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept> タイプの場合に基本クラスのインスタンスが返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If the methods on the base class return a reasonable result for unknown tables, then the two ISV models will co-exist within the same installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラスのメソッドが、未知のテーブルに対して適切な結果を返す場合、同じインストール内で 2 つの ISV モデルが共存します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>