<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="parse-incoming-electronic-documents.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>parse-incoming-electronic-documents.d83e4f.1b16f463b5f4b1c779105dea32dbd1e581f1f219.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1b16f463b5f4b1c779105dea32dbd1e581f1f219</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\parse-incoming-electronic-documents.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Parse incoming documents to update application data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションのデータを更新するために受信したドキュメントを解析する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to set up Electronic reporting (ER) formats that can be used to parse incoming documents and then apply selected content to update application data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、受信したドキュメントを解析し、選択したコンテンツをアプリケーション データに適用して更新できるように電子報告 (ER) 形式を設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Parse incoming documents to update application data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションのデータを更新するために受信したドキュメントを解析する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can design Electronic reporting (ER) formats and run them in Microsoft Dynamics 365 for Finance and Operations, to parse incoming electronic documents and then use their content to update application data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告 (ER) 書式をデザインして Microsoft Dynamics 365 for Finance and Operations 内で実行し、受信した電子ドキュメントを解析し、その内容を使用してアプリケーション データを更新することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following new ER functionality that has been introduced improves the parsing of incoming electronic documents in XML format:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">導入された次の新しい ER 機能は、XML 形式の受信する電子ドキュメンの解析を改善します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The <bpt id="p1">**</bpt>CASE<ept id="p1">**</ept> format element can be used as a root element of the ER format that is configured to parse incoming electronic documents in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CASE<ept id="p1">**</ept> 形式要素は、XML 形式の受信電子ドキュメントを解析するように構成された ER 形式のルート要素として使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The <bpt id="p1">**</bpt>FILE<ept id="p1">**</ept> format element is supported as a nested element of the <bpt id="p2">**</bpt>CASE<ept id="p2">**</ept> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FILE<ept id="p1">**</ept> 形式要素は、<bpt id="p2">**</bpt>CASE<ept id="p2">**</ept> 要素の入れ子になった要素としてサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Therefore, you can configure a single ER format to parse incoming electronic documents that might contain different root XML elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、1 つの ER フォーマットを設定して、異なるルート XML 要素を含む可能性のある受信電子ドキュメントを解析することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A <bpt id="p1">**</bpt>Parsing order of nested elements<ept id="p1">**</ept> attribute has been introduced for XML format elements in ER formats.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>入れ子になった要素の順序を解析<ept id="p1">**</ept>属性が ER 形式の XML 形式要素に導入されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can use this attribute to define a single XML element that is expected in the incoming file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この属性を使用すると、読み込まれるファイルで予期される 1 つの XML 要素を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>There are two valid sequences of the nested elements:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネストされた要素には 2 つの有効なシーケンスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>As in format<ept id="p1">**</ept> – The incoming file is valid when the sequence of nested elements in the file is the same as the order that is described in the ER format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>形式どおり<ept id="p1">**</ept> - 受信ファイルは、ファイル内の入れ子になった要素の順序は、ER 形式に記載されている順序と同じ場合に有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Any<ept id="p1">**</ept> – The incoming file is valid when all nested elements in the ER format are present in the parsing file, regardless of their sequence in that file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>任意<ept id="p1">**</ept> - 着信ファイルは、そのファイル内の順番に関係なく、ER 形式のすべての入れ子になった要素が解析ファイルに存在する場合に有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To become more familiar with the details of this feature, play the task guide, ER - Parse incoming documents to update application data (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能の詳細をよく理解するためには、タスク ガイド、\[ER - 受信ドキュメントを解析してアプリケーション データを更新する\] (「7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発」(10677) ビジネス プロセスの一部) を再生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This task guide shows how the responses from a web service can be parsed by using an ER format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスク ガイドは、Web サービスからの応答を ER 形式を使用して解析する方法を説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>To complete some steps of the task guide, you must download the following files:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク ガイドのいくつかの手順を完了するには、次のファイルをダウンロードする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Content description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテンツの説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>ER data model configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ER データ モデル構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">[</bpt>EFSTAmodel.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>EFSTAmodel.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>ER format configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ER フォーマット構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">[</bpt>EFSTAformat.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>EFSTAformat.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Web service response sample 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サービス応答サンプル 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">[</bpt>Response1.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Response1.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Web service response sample 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サービス応答サンプル 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt>Response2.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Response2.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Web service response sample 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サービス応答サンプル 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt>Response3.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Response3.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Web service response sample 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サービス応答サンプル 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">[</bpt>Response4.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Response4.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>