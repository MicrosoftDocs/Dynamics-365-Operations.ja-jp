<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="orderexchanges.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>orderexchanges.ba78aa.43571099727830e81c41416b6fe250dba398b3f8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>43571099727830e81c41416b6fe250dba398b3f8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\orderexchanges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品注文に対する交換のコンフィギュレーションとプロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure an exchange on a return in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail で返品に対する交換のコンフィギュレーションを行う方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品注文に対する交換のコンフィギュレーションとプロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail の以前のバージョンでは、Retail Headquarters で返品注文ドキュメントを使用することにより、顧客注文に対する返品が処理されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, the return order document can be used to process only products that are being returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、返品注文ドキュメントを使用できるのは、返品されている製品の処理のみです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The returned products are indicated by a negative quantity on the return order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品された製品は、返品注文明細行の数量が負の数になっていることでわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>By contrast, sales are indicated by a positive quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これに対して、売上は、数量が正の数になっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>However, the return order document doesn't support positive quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、返品注文ドキュメントでは、負の数量はサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限があるため、以前のバージョンの Retail では、返品注文ドキュメントを使用して製品の交換を行うシナリオはサポートされていませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, functionality has been added to support scenarios where exchanges are done on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しかし、返品注文で交換を行うシナリオをサポートする機能が追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Retail now uses the sales order document instead of the return order document to process these types of transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在の Retail では、返品注文ドキュメントではなく、販売注文ドキュメントを使用してこれらのタイプのトランザクションを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Configure Retail to support exchanges on return orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品注文での交換をサポートするように Retail を構成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to configure the system to support exchanges on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品注文での交換をサポートするようにシステムを構成するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">\&gt;</ph> 本社の設定 <ph id="ph2">\&gt;</ph> パラメーター <ph id="ph3">\&gt;</ph> 小売パラメーター<ept id="p1">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>On the <bpt id="p1">**</bpt>Customer orders<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Process return orders as sales orders<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客注文<ept id="p1">**</ept> クイック タブで、<bpt id="p2">**</bpt>返品注文を販売注文として処理する<ept id="p2">**</ept> オプションで <bpt id="p3">**</bpt>はい<ept id="p3">**</ept> を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Run the <bpt id="p1">**</bpt>Global configuration distribution schedule<ept id="p1">**</ept> job (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>グローバル構成配送スケジュール<ept id="p1">**</ept> ジョブ (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>) を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make an exchange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">交換を行う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションの記載に従ってシステムを構成した後、販売時点管理 (POS) のユーザーは、販売注文または販売請求書を選択して返品の処理を行います。これは、以前のバージョンの Retail と同様です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、返品品目がカートに追加された後、ユーザーは新しい販売明細行をカートに追加できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの新しい販売明細行については、顧客注文明細行を処理するために必要なすべての属性をユーザーが定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These attributes include the delivery method and fulfillment location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの属性には、配送方法やフルフィルメント場所が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The payment that is due for the transaction will be a net of the return order lines and sales order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">取引に対する支払額は、返品注文明細行と販売注文明細行の正味金額になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">取引に対して支払が行われると、Retail Headquarters で、返品注文が販売注文ドキュメントとして転記され、システムにより即座に返品明細行の請求処理が行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カートのさまざまな金額をわかりやすくするため、新しく 3 つの金額フィールドがカートに追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can use the screen designer to make these new fields available in the POS user interface (UI).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面デザイナーを使用することで、これらの新しいフィールドを POS のユーザー インターフェイス (UI) で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Deposit applied<ept id="p1">**</ept> – The deposit amount that is applied on a transaction when the user does a customer order pickup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>充当済預金<ept id="p1">**</ept> – ユーザーが顧客注文の集荷を行う場合に、取引に適用される預金額です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">預金の上書きがなく、10% の預金率が構成されている場合、このフィールドの金額は、顧客注文の合計額の 90% になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Carry out amount<ept id="p1">**</ept> – The total amount for lines where the delivery mode was set to <bpt id="p2">**</bpt>Carry out<ept id="p2">**</ept> when the customer order was created or edited, or during a customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>金額の実行<ept id="p1">**</ept> – 顧客注文の作成時または編集時、あるいは顧客注文の交換中に、配送モードが <bpt id="p2">**</bpt>実行<ept id="p2">**</ept> に設定されていた明細行の合計額です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドの金額には、税金および諸費用が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Return amount<ept id="p1">**</ept> – The total amount for lines that have negative quantities during the customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>返品金額<ept id="p1">**</ept> – 顧客注文の交換中の数量が負の値の明細行の合計金額です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドの金額には、税金および諸費用が含まれます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>