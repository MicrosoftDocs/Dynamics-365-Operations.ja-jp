<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-services.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-services.513934.02e828baa43087e8768b0dda182637d02cab15e5.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>02e828baa43087e8768b0dda182637d02cab15e5</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\custom-services.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Custom service development</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム サービスの開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to create a custom service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、カスタム サービスの作成方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Custom service development</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客サービスの開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can develop custom services for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations に対してカスタム サービスを開発できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When a developer writes a custom service under a service group, the service group is always deployed on two endpoints:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が 1 つのサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは次の 2 つのエンドポイントに常に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>SOAP endpoint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SOAP エンドポイント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>JSON endpoint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JSON エンドポイント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>SOAP-based custom service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SOAP ベース顧客サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>SOAP-based services remain the same as they were in Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SOAP ベースのサービスは Dynamics AX 2012 のものと同じままです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Code examples for consuming custom services using SOAP are available in the <bpt id="p1">[</bpt>Microsoft Dynamics AX Integration GitHub repository<ept id="p1">](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SOAP を使用したカスタム サービスを使用するためのコード例は、<bpt id="p1">[</bpt>Microsoft Dynamics AX 統合 GitHub リポジトリ<ept id="p1">](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication)</ept>で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Key changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キーの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>All the service groups under the <bpt id="p1">**</bpt>AOTService group<ept id="p1">**</ept> node are automatically deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOTService グループ<ept id="p1">**</ept>ノードの下にあるすべてのサービス グループが自動的に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>All services that must be deployed must be part of a service group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置する必要があるすべてのサービスはサービス グループの一部である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Example endpoint for a dev environment<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開発環境でのエンドポイントの例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Example endpoint for a non-dev environment<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>非開発環境でのエンドポイントの例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information about custom services, see:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム サービスの詳細については、次を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">[</bpt>Using Custom Services <ph id="ph1">\[</ph>AX 2012<ph id="ph2">\]</ph> (TechNet)<ept id="p1">](https://technet.microsoft.com/library/hh509052.aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>カスタム サービスを使用する <ph id="ph1">\[</ph>AX 2012<ph id="ph2">\]</ph> (TechNet)<ept id="p1">](https://technet.microsoft.com/library/hh509052.aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">[</bpt>Walkthrough: Exposing an X++ Class as a Data Contract (TechNet)<ept id="p1">](https://technet.microsoft.com/library/gg844225.aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>チュートリアル: X++ クラスをデータ契約として公開する (TechNet)<ept id="p1">](https://technet.microsoft.com/library/gg844225.aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>JSON-based custom service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JSON ベース顧客サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This feature enables X++ classes to be consumed as JSON services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能により、X++ クラスを JSON サービスとして使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In other words, the return data set is in JSON format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、返り値のデータ セットは、JSON 形式でです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>JSON, which stands for JavaScript Object Notation, is a compact, lightweight format that is commonly used communicate data between the client and the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JavaScript Object Notation の略である JSON は、クライアントとサーバー間のデータ通信によく使用されるコンパクトで軽量なフォーマットです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The JSON Endpoint is at <ph id="ph1">`https://host_uri/api/services/service_group_name/service_group_service_name/operation_name`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JSON エンドポイントが <ph id="ph1">`https://host_uri/api/services/service_group_name/service_group_service_name/operation_name`</ph> にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Code examples for consuming JSON services are available in the <bpt id="p1">[</bpt>Microsoft Dynamics AX Integration GitHub repository<ept id="p1">](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JSON サービスを使用するためのコード例は、<bpt id="p1">[</bpt>Microsoft Dynamics AX 統合 GitHub リポジトリ<ept id="p1">](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication)</ept>で利用できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>