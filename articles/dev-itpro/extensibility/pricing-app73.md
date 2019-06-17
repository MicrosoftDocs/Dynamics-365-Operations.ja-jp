<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pricing-app73.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pricing-app73.140f72.d2f46e9f2bbcfbd5e566107405af202efcea104f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d2f46e9f2bbcfbd5e566107405af202efcea104f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\pricing-app73.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Price and discount extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格と割引の拡張性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to extend pricing functionality in Microsoft Dynamics 365 for Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは Microsoft Dynamics 365 for Finance and Operations の価格設定機能を展開する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Price and discount extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格と割引の拡張性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 and later, the pricing area is extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 以降では、価格設定の領域が拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some common customizations for price and discounts include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格と割引のいくつかの一般的なカスタマイズは次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Adding new price group types and the corresponding price types (enum values for <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept>), in addition to adding search mechanisms for the new price types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい価格タイプの検索メカニズムに加えて、新しい価格グループ タイプと対応する価格タイプ (<bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> と <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> の列挙値) を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Modifying the price and discount search, including passing in any additional parameters to the <bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のパラメーターを <bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> クラスに渡すことを含め、価格と割引の検索を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>PriceType and PriceGroupType enums</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PriceType および PriceGroupType 列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Typically, adding a new type of price discount search starts with adding a new enum value in the two enums: <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、新しいタイプの価格割引検索を追加すると、<bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> と <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> の 2 つの列挙型へ新しい列挙型値が追加されて開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To support extensibility, <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> enum values are now encapsulated in the class hierarchies <bpt id="p3">**</bpt>PriceGroupTypeTradeAgreementMapping<ept id="p3">**</ept> and <bpt id="p4">**</bpt>PriceTypeTradeAgreementMapping<ept id="p4">**</ept>, respectively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能をサポートするために、<bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> と <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> の列挙型の値は、クラス階層 <bpt id="p3">**</bpt>PriceGroupTypeTradeAgreementMapping<ept id="p3">**</ept> と <bpt id="p4">**</bpt>PriceTypeTradeAgreementMapping<ept id="p4">**</ept> にそれぞれカプセル化されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>These can be extended for any new <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> extended enum values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、新しい <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> および <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> 拡張列挙値に対して拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The mapping of fields on the <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Vendor<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>InventTable<ept id="p3">**</ept> tables that  correspond to the price types is defined in <bpt id="p4">**</bpt>PriceTypeTradeAgreementMapping<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Customer<ept id="p1">**</ept>、<bpt id="p2">**</bpt>Vendor<ept id="p2">**</ept>、および <bpt id="p3">**</bpt>InventTable<ept id="p3">**</ept> テーブルの価格タイプに対応するフィールドのマッピングは、<bpt id="p4">**</bpt>PriceTypeTradeAgreementMapping<ept id="p4">**</ept> で定義されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following diagram highlights the implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、実装を強調表示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Note that the methods show only one of the sub-classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドはサブクラスを 1 つだけ示すことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The implementation needs to be on each sub-class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装は、各サブクラスにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>PriceGroupTypeTradeAgreementMapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PriceGroupTypeTradeAgreementMapping</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>PriceDisc class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PriceDisc クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The <bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> class is the search engine for price and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> クラスは、価格と割引の検索エンジンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This class uses a <bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> object as a member for passing in the parameters that are used in the price and discount search.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、<bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> オブジェクトを、価格および割引検索で使用されるパラメーターを渡すメンバとして使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This enables you to pass in the additional search parameters for the specific solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、特定のソリューションの追加の検索パラメーターを渡すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Only the parameters for a given <bpt id="p1">**</bpt>PriceGroupType<ept id="p1">**</ept> search are passed through the corresponding find methods on the <bpt id="p2">**</bpt>PriceDisc<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の <bpt id="p1">**</bpt>PriceGroupType<ept id="p1">**</ept> 検索のパラメータのみ、<bpt id="p2">**</bpt>PriceDisc<ept id="p2">**</ept> クラスの対応する find メソッドを使用して渡されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The ability to wrap and modify the instantiation of the <bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> class is enabled for all price and discount search calls made throughout AppSuite.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> クラスのインスタンス化をラップし、変更する機能は、AppSuite 全体で実行されたすべての価格と割引の検索呼び出しで有効になっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In the following diagram, you can see how the <bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> class can be extended to modify existing searches or to add new search methods that correspond to the extended <bpt id="p2">**</bpt>PriceType<ept id="p2">**</ept> enum values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図では、どのように <bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> クラスを拡張して、既存の検索を変更したり、拡張された <bpt id="p2">**</bpt>PriceType<ept id="p2">**</ept> 列挙値に対応する新しい検索メソッドを追加したりできるかを確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>PriceDiscClass</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PriceDiscClass</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Add a new price search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい価格検索の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In this scenario, you have extended the <bpt id="p1">**</bpt>PriceGroupType<ept id="p1">**</ept> enum with a new value <bpt id="p2">**</bpt>PriceGroupTypeISVExtension<ept id="p2">**</ept>, and two corresponding <bpt id="p3">**</bpt>PriceType<ept id="p3">**</ept> enum values - <bpt id="p4">**</bpt>ISVPurchPriceType<ept id="p4">**</ept> and <bpt id="p5">**</bpt>ISVSalesPriceType<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、<bpt id="p1">**</bpt>PriceGroupType<ept id="p1">**</ept> 列挙を新しい値 <bpt id="p2">**</bpt>PriceGroupTypeISVExtension<ept id="p2">**</ept>、および 2 つの対応する <bpt id="p3">**</bpt>PriceType<ept id="p3">**</ept> 列挙値である <bpt id="p4">**</bpt>ISVPurchPriceType<ept id="p4">**</ept> と <bpt id="p5">**</bpt>ISVSalesPriceType<ept id="p5">**</ept> で拡張しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>WalkThrough1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WalkThrough1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The following diagram illustrates how a new price search can be added for the <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、<bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> 値および <bpt id="p2">**</bpt>PriceGroupType<ept id="p2">**</ept> 値に対して新しい価格検索を追加する方法を示しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>WalkThrough2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WalkThrough2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This example shows the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For the newly created <bpt id="p1">**</bpt>PriceGroupType<ept id="p1">**</ept> value, a <bpt id="p2">**</bpt>PriceGroupTypeTradeAgreementMappingISVPriceGroupType<ept id="p2">**</ept> class decorated with the attribute <bpt id="p3">**</bpt>ISVPriceGroupType<ept id="p3">**</ept> defines the behavior of the price group type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく作成された <bpt id="p1">**</bpt>PriceGroupType<ept id="p1">**</ept> 値については、属性 <bpt id="p3">**</bpt>ISVPriceGroupType<ept id="p3">**</ept> で修飾された <bpt id="p2">**</bpt>PriceGroupTypeTradeAgreementMappingISVPriceGroupType<ept id="p2">**</ept> クラスは、価格グループ タイプの動作を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For the newly created <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> value, the <bpt id="p2">**</bpt>PriceTypeTradeAgreementMappingISVPurchPriceType<ept id="p2">**</ept> and <bpt id="p3">**</bpt>PriceTypeTradeAgreementMappingISVSalesPriceType<ept id="p3">**</ept> classes correspond to Purchase and Sales.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく作成された <bpt id="p1">**</bpt>PriceType<ept id="p1">**</ept> 値については、<bpt id="p2">**</bpt>PriceTypeTradeAgreementMappingISVPurchPriceType<ept id="p2">**</ept> および <bpt id="p3">**</bpt>PriceTypeTradeAgreementMappingISVSalesPriceType<ept id="p3">**</ept> クラスは、購買および販売に対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Augmenting the <bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> class to add any generic parameters for the price discount search.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> クラスを拡張して価格割引検索の汎用パラメータを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Augmenting the <bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> class to create the new price discount search methods for the new price types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PriceDisc<ept id="p1">**</ept> クラスを拡張して新しい価格タイプの新しい価格割引検索メソッドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The <bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> is accessible from all classes related to price and discount search and these could be augmented, based on the requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PriceDiscParameters<ept id="p1">**</ept> には、価格と割引の検索に関連するすべてのクラスからアクセスでき、これらは要件に基づいて拡張できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>