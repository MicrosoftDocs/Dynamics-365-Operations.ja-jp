<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trigger-example-blocking-transaction.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trigger-example-blocking-transaction.f820e3.5994755b11bc2268686bedc7664c7992ca3e6d79.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5994755b11bc2268686bedc7664c7992ca3e6d79</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\trigger-example-blocking-transaction.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Block transactions by using triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを使用してトランザクションをブロックする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic shows how you can use a trigger to block an invoice or credit transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、トリガーを使用して請求書またはクレジット取引をブロックする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Block transactions by using triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを使用してトランザクションをブロックする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic shows how you can use a trigger to block an invoice or credit transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、トリガーを使用して請求書またはクレジット取引をブロックする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic shows how you can block an invoice or credit transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、請求書またはクレジット取引をブロックする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Open Visual Studio as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を管理者としてオープンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Create a new Visual C<ph id="ph1">\#</ph> Class Library (Portable) project and name it CRTTriggerExtension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Visual C<ph id="ph1">\#</ph> クラス ライブラリ (ポータブル) プロジェクトを作成し、CRTTriggerExtension という名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you get a message that the selection makes this project incompatible with Visual Studio 2010, click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択内容によってこのプロジェクトが Visual Studio 2010 と互換性がなくなるというメッセージが表示される場合、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In Solution Explorer, rename default class1.cs to GetCustomersServiceRequestTrigger.cs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、既定の class1.cs を GetCustomersServiceRequestTrigger.cs に名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Right-click the <bpt id="p1">**</bpt>Reference<ept id="p1">**</ept> node in the project and add the following references.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトで <bpt id="p1">**</bpt>参照<ept id="p1">**</ept> ノードを右クリックし、次の参照を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The location of the references will depend on the deployment topology.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照の場所は、配置トポロジによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Microsoft.Dynamics.Commerce.Runtime.Entities.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Commerce.Runtime.Entities.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Microsoft.Dynamics.Commerce.Runtime.Framework.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Commerce.Runtime.Framework.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Microsoft.Dynamics.Commerce.Runtime.Services.Messages.dll</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft.Dynamics.Commerce.Runtime.Services.Messages.dll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Add the following <bpt id="p1">**</bpt>using<ept id="p1">**</ept> statement to the GetCustomersServiceRequestTrigger.cs file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomersServiceRequestTrigger.cs ファイルに、次の明細書を<bpt id="p1">**</bpt>使用して<ept id="p1">**</ept>追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Rename class1.cs in the code to GetCustomersServiceRequestTrigger and then add the IRequestTrigger interface declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの class1.cs の名前を GetCustomersServiceRequestTrigger に変更し、IRequestTrigger インターフェイス宣言を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Implement the IRequestTrigger interface trigger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IRequestTrigger インターフェイス トリガーを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Right-click the IRequestTrigger class, select <bpt id="p1">**</bpt>Quick Actions<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Implement Interface<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IRequestTrigger クラスを右クリックして、<bpt id="p1">**</bpt>クイック アクション<ept id="p1">**</ept> をクリックし、<bpt id="p2">**</bpt>インターフェイスの実装<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Visual Studio will implement the interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio はインターフェイスを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can also place the cursor on IRequestTrigger, press <bpt id="p1">**</bpt>Ctrl+<ept id="p1">**</ept>, and select <bpt id="p2">**</bpt>Implement Interface<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カーソルを IRequestTrigger の上に配置して、<bpt id="p1">**</bpt>Ctrl+<ept id="p1">**</ept> を押し、<bpt id="p2">**</bpt>インターフェイスの実装<ept id="p2">**</ept> を選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The empty interface members SupportedRequestTypes, OnExecuted, and OnExecuting methods are shown in the following code example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空のインターフェイス メンバー SupportedRequestTypes、OnExecuted、および OnExecuting メソッドを次のコード例に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Retail Server uses the GetCustomersServiceRequest object to get the customer details from Commerce Runtime (CRT) and uses the GetCustomersServiceRequest object to add the customer to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Server は、GetCustomersServiceRequest オブジェクトを使用して Commerce Runtime (CRT) から顧客詳細を取得し、GetCustomersServiceRequest オブジェクトを使用して顧客をトランザクションに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Before adding the customer to the transaction you need to check whether the customer is blocked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションに顧客を追加する前に、顧客がブロックされているかどうかを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To do this, implement a post trigger for this request and check whether the customer is blocked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、この要求の転記トリガーを実装し、顧客がブロックされているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>If the customer is blocked, then throw the exception to MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客がブロックされている場合、MPOS によって例外がスローされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the SupportedRequestTypes method tell the CRT that you are going to add the trigger for GetCustomersServiceRequest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SupportedRequestTypes メソッドで、GetCustomersServiceRequest のトリガーを追加することを CRT に通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following code example shows how to add GetCustomersServiceRequest as a supported type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、GetCustomersServiceRequest をサポートされている型として追加する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Check if the customer is blocked in the OnExecuted (post trigger) method with the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客が次のコードで OnExecuted (転記トリガー) メソッドでブロックされているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Finally, update the OnExecuting method with the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、次のコードで OnExecuting メソッドを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>