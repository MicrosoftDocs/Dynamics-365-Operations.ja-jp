<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extend-retail-server-odata-controller.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extend-retail-server-odata-controller.6515e6.496ab6512cfb1478ed762eb165a760c872e7e222.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>496ab6512cfb1478ed762eb165a760c872e7e222</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\extend-retail-server-odata-controller.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend a Retail Server OData controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Server OData コントローラーの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides code that extends the CustomController class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、CustomController クラスを拡張するコードを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend a Retail Server OData controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Server OData コントローラーの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides code that extends the CustomersController class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、CustomersController クラスを拡張するコードを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>A controller is a mapping for a commerce entity that controls create, read, update, and delete (CRUD) behaviors and actions for a commerce entity type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーは、commerce エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールする commerce エンティティのマッピングです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Each commerce entity must have a corresponding controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各コマース エンティティには、対応するコントローラーが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can extend a controller that is included with Microsoft Dynamics 365 for Retail to add new business actions that meet your business requirement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail に含まれるコントローラーを拡張して、業務上の要件を満たすように新しい業務処理を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To extend an existing controller, you must define a new class that extends an existing controller class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコント ローラーを拡張するには、既存のコントローラー クラスを拡張する新しいクラスを定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When you create a new controller that extends an existing controller, the new controller can create new or override existing methods in the controller that is being extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコント ローラーを拡張する新しいコント ローラーを作成するときは、新しいコントローラーは拡張されるコントローラーで新しいメソッドを作成するか既存のメソッドをオーバーライドできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>All methods in the extended controller that have not been overridden will continue to function as before.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーライドされていない拡張コントローラー内のすべてのメソッドは、引き続き同じように機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In this example, the <bpt id="p1">**</bpt>ExtendedCustomersController<ept id="p1">**</ept> class extends the <bpt id="p2">**</bpt>CustomersController<ept id="p2">**</ept> class, and the <bpt id="p3">**</bpt>CustomersController<ept id="p3">**</ept> class is the controller for the <bpt id="p4">**</bpt>Customers<ept id="p4">**</ept> entity type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>ExtendedCustomersController<ept id="p1">**</ept> クラスは <bpt id="p2">**</bpt>CustomersController<ept id="p2">**</ept> クラスを拡張し、<bpt id="p3">**</bpt>CustomersController<ept id="p3">**</ept>クラスは <bpt id="p4">**</bpt>Customers<ept id="p4">**</ept> エンティティ タイプのコントローラーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You will need to update the <bpt id="p1">**</bpt>extensionComposition<ept id="p1">**</ept> section of the Retail Server Web.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー Web.config ファイルの <bpt id="p1">**</bpt>extensionComposition<ept id="p1">**</ept> セクションを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For more information, see the <bpt id="p1">**</bpt>How to call the new retail server API from MPOS/Cloud POS<ept id="p1">**</ept> section of <bpt id="p2">[</bpt>Commerce runtime (CRT) and Retail Server extensibility<ept id="p2">](commerce-runtime-extensibility.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p2">[</bpt>Commerce Runtime ((CRT) および Retail サーバー拡張機能<ept id="p2">](commerce-runtime-extensibility.md)</ept>の <bpt id="p1">**</bpt>MPOS/クラウド POS から新しい Retail サーバー API を呼び出す方法<ept id="p1">**</ept> セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You can find the sample code from this topic in the Retail software development kit (SDK).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>