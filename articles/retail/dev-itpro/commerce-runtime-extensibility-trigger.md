<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="commerce-runtime-extensibility-trigger.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>commerce-runtime-extensibility-trigger.3234d9.23998cfead02ad1dd514c373e4d7ec42d0327b3c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>23998cfead02ad1dd514c373e4d7ec42d0327b3c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\commerce-runtime-extensibility-trigger.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Commerce runtime (CRT) extensibility and triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Rumtime (CRT) の拡張機能とトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains trigger support for the Microsoft Dynamics AX commerce runtime (CRT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics AX commerce ランタイム (CRT) のトリガー サポートについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>CRT supports pre-triggers and post-triggers for every request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRTは、すべての要求に対してプレトリガーおよびポストトリガーをサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Commerce runtime (CRT) extensibility and triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Rumtime (CRT) の拡張機能とトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article explains trigger support for the Dynamics 365 for Retail commerce runtime (CRT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Dynamics 365 for Retail commerce ランタイム (CRT) のトリガー サポートについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>CRT supports pre-triggers and post-triggers for every request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRTは、すべての要求に対してプレトリガーおよびポストトリガーをサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>CRT trigger overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT トリガーの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Commerce runtime (CRT) triggers give you a way to extend the CRT workflow, and let you add business logic before and after every CRT request is executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Commerce Runtime</ph> (CRT) トリガーによって CRT のワークフローを拡張でき、全ての <ph id="4">CRT</ph> リクエストが実行される前後に、ビジネス ロジックに追加できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The following two methods are used:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の 2 つの方法が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>OnExecuting<ept id="p1">**</ept> – This method is invoked before a request has been processed by a corresponding <bpt id="p2">**</bpt>IRequestHandler<ept id="p2">**</ept> implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OnExecuting<ept id="p1">**</ept> – このメソッドは、要求が対応する <bpt id="p2">**</bpt>IRequestHandler<ept id="p2">**</ept> 実装によって処理される前に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>OnExecuted<ept id="p1">**</ept> – This method is invoked after the request has been processed by a corresponding <bpt id="p2">**</bpt>IRequestHandler<ept id="p2">**</ept> implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OnExecuted<ept id="p1">**</ept> – このメソッドは、要求が対応する <bpt id="p2">**</bpt>IRequestHandler<ept id="p2">**</ept> 実装によって処理された後に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>CRT trigger interface</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT トリガー インターフェイス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To implement a trigger, you must complete these tasks, as shown in the code example that follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを実装するには、次のコード例に示すように、これらのタスクを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Implement <bpt id="p1">**</bpt>IRequestTrigger<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IRequestTrigger<ept id="p1">**</ept> を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Specify <bpt id="p1">**</bpt>SupportedRequestTypes<ept id="p1">**</ept> to define the request types that the trigger must be executed for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SupportedRequestTypes<ept id="p1">**</ept> を指定して、トリガーを実行する必要のある要求のタイプを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Write a trigger implementation in the <bpt id="p1">**</bpt>OnExecuting<ept id="p1">**</ept> method if business logic must be run before the request is addressed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求の解決前にビジネス ロジックを実行する必要がある場合、トリガーの実装を <bpt id="p1">**</bpt>OnExecuting<ept id="p1">**</ept> メソッドに記述します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Write a trigger implementation in the <bpt id="p1">**</bpt>OnExecuted<ept id="p1">**</ept> method if business logic must be run after the request is addressed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求の解決後にビジネス ロジックを実行する必要がある場合、トリガーの実装を <bpt id="p1">**</bpt>OnExecuted<ept id="p1">**</ept> メソッドに記述します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Trigger CommerceRunTime.config updates for 7.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.0 の CommerceRunTime.config 更新プログラムをトリガーする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When you extend the CRT, you must write your extension in your own assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT を拡張するときは、ユーザー独自のアセンブリ内で拡張機能を記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>After you write the trigger extension in your assembly, you must copy the extension library to the Retail server bin folder and add an entry in the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section of the commerceRuntime.config file for the CRT, so that the trigger is loaded at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガー拡張子をアセンブリに書き込んだ後、Retail サーバー bin フォルダーに拡張子ライブラリをコピーし、実行時にトリガーがロードされるように、CRT の commerceRuntime.config ファイルの<bpt id="p1">**</bpt>合成<ept id="p1">**</ept>セクションに入力を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following example shows a .config file that includes an entry for a trigger implementation in the <bpt id="p1">**</bpt>CRTExtensionTrigger<ept id="p1">**</ept> assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>CRTExtensionTrigger<ept id="p1">**</ept> アセンブリ内のトリガー実装のエントリを含む .config ファイルを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CRTExtensionTrigger<ept id="p1">](./media/crtextensiontrigger-1024x489.png)](./media/crtextensiontrigger.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CRTExtensionTrigger<ept id="p1">](./media/crtextensiontrigger-1024x489.png)](./media/crtextensiontrigger.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For the CRT extension to work in offline mode update <bpt id="p1">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\CommerceRuntime.MPOSOffline.config<ept id="p1">**</ept> with the extension library information under the composition section and copy and paste the extension library to <bpt id="p2">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードで作業する CRT 拡張機能については、合成セクションの拡張ライブラリ情報で <bpt id="p1">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\CommerceRuntime.MPOSOffline.config<ept id="p1">**</ept> を更新し、その拡張ライブラリをコピーして <bpt id="p2">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker<ept id="p2">**</ept> に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Trigger CommerceRunTime.config updates for 7.1 (with May 2017 monthly update), 7.2 and 7.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.1 (2017 年 5 月の月次更新)、7.2 および 7.3 の CommerceRunTime.config 更新プログラムのトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Copy and paste the extension library to <bpt id="p1">**</bpt>...\RetailServer\webroot\bin\ext folder<ept id="p1">**</ept> and update the <bpt id="p2">**</bpt>commerceRuntime.ext.config<ept id="p2">**</ept> file with the custom extension library information under composition section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張ライブラリを <bpt id="p1">**</bpt>...\RetailServer\webroot\bin\ext フォルダー<ept id="p1">**</ept>にコピーして貼り付け、構成セクションのカスタム拡張ライブラリ情報を含む <bpt id="p2">**</bpt>commerceRuntime.ext.config<ept id="p2">**</ept> ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In this example, <bpt id="p1">**</bpt>Contoso.Commerce.Runtime.Services<ept id="p1">**</ept> is the  custom extension name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>Contoso.Commerce.Runtime.Services<ept id="p1">**</ept> はカスタムの拡張機能名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For the CRT extension to work in offline mode update <bpt id="p1">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\extCommerceRuntime.MPOSOffline.ext.config<ept id="p1">**</ept> with the extension library information under the composition section and copy and paste the extension library to <bpt id="p2">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードで作業する CRT 拡張機能については、合成セクションの拡張ライブラリ情報で <bpt id="p1">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\extCommerceRuntime.MPOSOffline.ext.config<ept id="p1">**</ept> を更新し、その拡張ライブラリをコピーして <bpt id="p2">**</bpt>...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext<ept id="p2">**</ept> に貼り付けます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>