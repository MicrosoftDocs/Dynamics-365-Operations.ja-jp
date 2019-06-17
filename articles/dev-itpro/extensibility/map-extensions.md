<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="map-extensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>map-extensions.ffc0d8.eda53f7df22f1aa2bdfcfee6d0dd991d5f7f8044.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>eda53f7df22f1aa2bdfcfee6d0dd991d5f7f8044</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\map-extensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Table map extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップ拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>To extend table maps, we have refactored table maps into a model, which allows you to extend a solution with additional fields and methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Table map extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップ拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic applies to Dynamics 365 for Finance and Operations, Enterprise edition 7.3 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Finance and Operations, Enterprise edition 7.3 およびそれ以降に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To extend table maps, we have refactored table maps into a model, which allows you to extend a solution with additional fields and methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic discusses why you need a model to extend a table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、テーブルのマップを拡張するためのモデルが必要な理由を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Adding a field to an existing table map through extension can present some challenges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して既存のテーブル マップにフィールドを追加すると、いくつかの問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If these issues are not addressed during the implementation, there can be runtime errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装時にこれらの問題に対処しない場合は、ランタイム エラーになる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The errors occur because the developer cannot modify all the tables that are involved in implementing the table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーは、開発者がテーブル マップの実装に関連するすべてのテーブルを変更できないために発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The same is true for adding a method to a table map if the method is called directly as an instance method on the table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドがテーブル マップ上でインスタンス メソッドとして直接呼び出された場合、メソッドをテーブル マップに追加する場合も同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>There is no way to enforce how fields on table maps must be mapped to fields on all tables that implement the table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップのフィールドがどのようにテーブル マップを実装するすべてのテーブルのフィールドにマップされる必要があるかを、強制する方法はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Similarly, there is no way to enforce how methods on table maps must be also be methods on all tables that implement the table map.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、テーブル マップのメソッドがどのようにテーブル マップを実装するすべてのテーブルのメソッドにマップされる必要があるかを、強制する方法はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following diagram shows the <bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> table map, which is implemented by the <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept>, <bpt id="p3">**</bpt>PurchTable<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>SalesBasket<ept id="p4">**</ept> tables in the <bpt id="p5">**</bpt>ApplicationSuite<ept id="p5">**</ept> model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、<bpt id="p1">**</bpt>SalesPurchTable<ept id="p1">**</ept> テーブル マップを示しています。これは、<bpt id="p2">**</bpt>ApplicationSuite<ept id="p2">**</ept> モデルの <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept>、<bpt id="p4">**</bpt>PurchTable<ept id="p4">**</ept>、および <bpt id="p5">**</bpt>SalesBasket<ept id="p5">**</ept> テーブルによって実装されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In addition, the <bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> table implements the <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> table map, but <bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept> is part of an <bpt id="p4">**</bpt>ISVModule1<ept id="p4">**</ept> model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、<bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> テーブルは <bpt id="p2">**</bpt>SalesPurchTable<ept id="p2">**</ept> テーブル マップを実装しますが、<bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept> は <bpt id="p4">**</bpt>ISVModule1<ept id="p4">**</ept> モデルの一部です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>MapExtensionsProblem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MapExtensionsProblem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For example, if a new field named <bpt id="p1">**</bpt>AccountingGroupId<ept id="p1">**</ept> and a new method named <bpt id="p2">**</bpt>validateAccountingGroup<ept id="p2">**</ept> are added to the table map in the <bpt id="p3">**</bpt>ApplicationSuite<ept id="p3">**</ept> model, then the tables that you implement the table map can be updated to include the field and method added as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>AccountingGroupId<ept id="p1">**</ept> という名前の新しいフィールドおよび <bpt id="p2">**</bpt>validateAccountingGroup<ept id="p2">**</ept> という名前の新しいメソッドが <bpt id="p3">**</bpt>ApplicationSuite<ept id="p3">**</ept> モデルでテーブル マップに追加されます。それから、そのテーブル マップを実装するテーブルは、フィールドおよび追加されるメソッドも含むよう更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> table in the <bpt id="p2">**</bpt>ISVModule1<ept id="p2">**</ept> model is, however, outside of the control of the developer making the changes to the <bpt id="p3">**</bpt>ApplicationSuite<ept id="p3">**</ept> model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p2">**</bpt>ISVModule1<ept id="p2">**</ept> モデルの <bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> テーブルは、開発者が <bpt id="p3">**</bpt>ApplicationSuite<ept id="p3">**</ept> モデルに変更を加えるコントロールの外にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>MapExtensionsProblem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MapExtensionsProblem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If you add business logic to the <bpt id="p1">**</bpt>ApplicationSuite<ept id="p1">**</ept> model, and that logic queries the new <bpt id="p2">**</bpt>AccountingGroupId<ept id="p2">**</ept> field and the table map record is of type <bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept>, a runtime error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックを <bpt id="p1">**</bpt>ApplicationSuite<ept id="p1">**</ept> モデルに追加する場合、そのロジックは新しい <bpt id="p2">**</bpt>AccountingGroupId<ept id="p2">**</ept> フィールドをクエリし、テーブル マップ レコードのタイプが <bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept> である場合、ランタイム エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Similarly, if you add business logic to the <bpt id="p1">**</bpt>ApplicationSuite<ept id="p1">**</ept> model, and that logic queries <bpt id="p2">**</bpt>validateAccountingGroup<ept id="p2">**</ept>, then a runtime error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、ビジネス ロジックを <bpt id="p1">**</bpt>ApplicationSuite<ept id="p1">**</ept> モデルに追加する場合、およびそのロジックが <bpt id="p2">**</bpt>validateAccountingGroup<ept id="p2">**</ept> を照会する場合、ランタイム エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>As a result, the solution is broken, unless you add mapping to the new field and add the new method to the <bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、新しいフィールドにマッピングを追加して新しいメソッドを <bpt id="p1">**</bpt>ISV1Header<ept id="p1">**</ept> テーブルに追加しない限り、ソリューションは破損します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The conflict is not resolved if the ability to add fields or methods is added to table maps through extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドまたはメソッドを追加する機能が拡張機能を介してテーブル マップに追加された場合は、競合は解決されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>This is illustrated in the following diagram, where <bpt id="p1">**</bpt>ISVModule2<ept id="p1">**</ept> includes extensions of the table map and the implementing tables in the <bpt id="p2">**</bpt>ApplicationSuite<ept id="p2">**</ept> model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、<bpt id="p1">**</bpt>ISVModule2<ept id="p1">**</ept> に <bpt id="p2">**</bpt>ApplicationSuite<ept id="p2">**</ept> モデルのテーブル マップと実装テーブルの拡張が含まれている次の図に示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The developer implementing <bpt id="p1">**</bpt>ISVModule2<ept id="p1">**</ept> has no control over the <bpt id="p2">**</bpt>ISV1Header<ept id="p2">**</ept> table in the <bpt id="p3">**</bpt>ISVModule1<ept id="p3">**</ept> model, so the <bpt id="p4">**</bpt>ISV1Header<ept id="p4">**</ept> table lacks a mapping of the <bpt id="p5">**</bpt>AccountingGroupId<ept id="p5">**</ept> field and implementation of the <bpt id="p6">**</bpt>validateAccountingGroup<ept id="p6">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISVModule2<ept id="p1">**</ept> を実装する開発者は、<bpt id="p2">**</bpt>ISVModule1<ept id="p2">**</ept> モデルの <bpt id="p3">**</bpt>ISV1Header<ept id="p3">**</ept> テーブルを制御できません。<bpt id="p4">**</bpt>ISV1Header<ept id="p4">**</ept> テーブルには、<bpt id="p5">**</bpt>AccountingGroupId<ept id="p5">**</ept> フィールドのマッピングと <bpt id="p6">**</bpt>validateAccountingGroup<ept id="p6">**</ept> メソッドの実装がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>MapExtensionsProblem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MapExtensionsProblem</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Even if the the compiler enforced that all fields and methods on a table map must be mapped to all tables implementing the table map, the conflict would not be resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラがテーブル マップのすべてのフィールドとメソッドを、テーブル マップを実装するすべてのテーブルにマップする必要がある場合でも、競合は解決されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Instead of receiving runtime errors, adding a field or a method would clear a breaking change, as tables not having a new field mapped or a new method implemented would compile when the model containing the added field/method is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マップされた新しいフィールドまたは実装された新しいメソッドがないテーブルは、追加されたフィールド/メソッドを含むモデルが適用されるときにコンパイルするため、ランタイム エラーを受け取る代わりに、フィールドまたはメソッドを追加することで重大な変更をクリアします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>To extend table maps, we have refactored table maps into a model, which allows you to extend a solution with additional fields and methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>