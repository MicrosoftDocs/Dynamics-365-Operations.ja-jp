<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-tables.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-tables.bab901.358ccdda7c16056afdcab11804bd3e7485d35b7f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>358ccdda7c16056afdcab11804bd3e7485d35b7f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extensible-tables.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Write extensible tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なテーブルの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to write extensible tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張可能テーブルを書き込む方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Write extensible tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なテーブルの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Tables have a rich extension model that lets extenders add fields, field groups, indexes, relations, methods, and more.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルには、拡張担当者がフィールド、フィールド グループ、インデックス、関係、メソッドなどを追加できる豊富な拡張モデルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Unique indexes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一意のインデックス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Unique indexes can't be changed by an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張により固有のインデックスを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Unique indexes define a table constraint, and they often also define the key of the rows in the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固有のインデックスは、テーブルの制約を定義し、多くの場合、テーブルにおける行のキーも定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You aren't allowed to change unique indexes, because such changes change the nature of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような変更はテーブルの内容を変更するため、固有のインデックスを変更することは許可されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Therefore, there is a high risk that the changes will cause logical conflicts with future versions of the solution that defines the table, or with other solutions that consume the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、テーブルを定義するソリューションの将来のバージョン、またはテーブルを消費する他のソリューションと論理競合が発生する可能性が高くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Avoid unique indexes that are likely to be changed either now or in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在または将来、変更されると考えられる固有のインデックスを避けてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For example, don't create a unique index on product dimensions such as color, size, style, and configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、色、サイズ、スタイル、およびコンフィギュレーションなど、製品分析コードに固有のインデックスを作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Instead, create a unique index on a distinct product variant, so that the index doesn't have to be changed if new product dimensions are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、新しい製品分析コードが追加された場合にインデックスを変更しなくてもかまわないように、特徴的製品バリアントに固有のインデックスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If you require an extensible uniqueness constraint on multiple columns, consider creating a hash of the column's values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の列で拡張可能な一意制約を必要とする場合、列の値のハッシュを作成することを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>For an example, see the NumberSequenceScope table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、NumberSequenceScope テーブルを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Data events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Tables have many predefined data events that are automatically raised.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルには、自動的に発生する多くの事前定義データ イベントがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Avoid calling <bpt id="p1">**</bpt>doInsert()<ept id="p1">**</ept>, <bpt id="p2">**</bpt>doUpdate()<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>doDelete()<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>doInsert()<ept id="p1">**</ept>、<bpt id="p2">**</bpt>doUpdate()<ept id="p2">**</ept>、<bpt id="p3">**</bpt>doDelete()<ept id="p3">**</ept> の呼び出しを回避してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These methods prevent the data events from being raised and make your table harder to extend.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは、データ イベントが発生することを防ぎ、テーブルの拡張が困難になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Instead, call <bpt id="p1">**</bpt>insert()<ept id="p1">**</ept>, <bpt id="p2">**</bpt>update()<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>delete()<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">**</bpt>insert()<ept id="p1">**</ept>、<bpt id="p2">**</bpt>update()<ept id="p2">**</ept>、<bpt id="p3">**</bpt>delete()<ept id="p3">**</ept> を呼び出してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Field groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Always use field groups to group related fields, and to build forms and reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ず、関連するフィールドをグループ化するため、フォームおよびレポートを構築するために、フィールド グループを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>By consistently using this approach, you enable the extension to surface additional fields in forms and on reports by extending the field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一貫してこの方法を使用することで、フィールド グループを拡張することによって、追加フィールドをフォームやレポートに表示する拡張を有効にします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>