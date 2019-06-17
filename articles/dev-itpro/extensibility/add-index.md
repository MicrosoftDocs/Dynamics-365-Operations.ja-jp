<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="add-index.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>add-index.1fe9a0.3dab4107711edd95859b694c22085d4464811914.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3dab4107711edd95859b694c22085d4464811914</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\add-index.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add indexes to tables through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用してテーブルにインデックスを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to add an index to a table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、テーブルにインデックスを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add indexes to tables through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用してテーブルにインデックスを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Often, you extend tables so that you can store additional data for later but also quickly access the data that is based on the new fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Therefore, it's often beneficial to have a dedicated index that speeds up the database search.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can add a new index to an existing table through extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To add an index to an existing table, you extend the selected table and then create an index just as you would create an index on a new table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You can add both new and existing fields so that they are part of the new index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>You can create new indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいインデックスを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, you can't modify existing indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、既存のインデックスを変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the following illustration, an InventTable extension is used to define an index for a new field on the InventTable table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>New index</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいインデックス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You should not use this approach to create unique indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固有のインデックスを作成するのに、この手法は用いないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This change is an intrusive change that might break the solutions of other independent software vendors (ISVs) if those solutions are deployed in the same environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This capability will be removed in future platform releases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、将来のプラットフォーム リリースでは削除されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>