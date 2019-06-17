<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extend-metadata.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extend-metadata.401671.13436f9705f03a34992bbfd1cbb129a54a2f0621.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>13436f9705f03a34992bbfd1cbb129a54a2f0621</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\extend-metadata.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend the default Retail Server metadata controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の Retail Server メタデータ コントローラーの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article provides code to extend the CommerceModelFactory class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、CommerceModelFactory クラスを拡張するコードを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend the default Retail Server metadata controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の Retail Server メタデータ コントローラーの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article provides code to extend the CommerceModelFactory class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、CommerceModelFactory クラスを拡張するコードを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When you use OData together with Microsoft Dynamics 365 for Retail, metadata defines the contract between a client and server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OData を Microsoft Dynamics 365 for Retail と共に使用するとき、メタデータはクライアントとサーバー間の契約を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The metadata exposes entity definitions and action definitions, so that when you make a change on the server side, you can use a tool on the client side to generate proxy code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ はエンティティ定義とアクション定義を公開しているため、サーバー側で変更を加えると、クライアント側のツールを使用してプロキシ コードを生成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Therefore, the maintenance effort for developers is reduced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メンテナンスにかかる開発者の労力が軽減されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To consume new or changed entities and actions, you must extend the metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新規または変更されたエンティティおよびアクションを使用するには、メタデータを拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Retail Server has a default metadata controller that is named <bpt id="p1">**</bpt>CommerceModelFactory<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーには、<bpt id="p1">**</bpt>CommerceModelFactory<ept id="p1">**</ept> という既定メタデータ コントローラーがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To extend the default controller, you create a new class that uses the <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> attribute together with the <bpt id="p2">**</bpt>IEdmModelFactory<ept id="p2">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のコント ローラーを拡張するには、<bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> 属性と <bpt id="p2">**</bpt>IEdmModelFactory<ept id="p2">**</ept> インターフェイスを使用する新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can then add and override existing code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコードを追加してオーバーライドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>For example, you can add new entity sets, new actions, new complex types, or new exception types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、新しいエンティティ セット、新しいアクション、新しい複合型、または新しい例外タイプを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In the following example, the <bpt id="p1">**</bpt>ExtendedEdmModelFactory<ept id="p1">**</ept> class extends the <bpt id="p2">**</bpt>CommerceModelFactory<ept id="p2">**</ept> metadata controller and creates a new action that is named <bpt id="p3">**</bpt>NewAction<ept id="p3">**</ept> and a new entity set that is named <bpt id="p4">**</bpt>NewEntities<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>ExtendedEdmModelFactory<ept id="p1">**</ept> クラスは <bpt id="p2">**</bpt>CommerceModelFactory<ept id="p2">**</ept> メタデータ コントローラーを拡張して、<bpt id="p3">**</bpt>NewAction<ept id="p3">**</ept> という新しいアクションおよび <bpt id="p4">**</bpt>NewEntities<ept id="p4">**</ept> という新しいエンティティ セットを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You can find the sample code from this topic in the Retail software development kit (SDK).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>