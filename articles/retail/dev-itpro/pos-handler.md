<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-handler.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-handler.96ac3b.88fc67499f14dd34cc23b47b837fe875821e4d09.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>88fc67499f14dd34cc23b47b837fe875821e4d09</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>33e5f728a70d0546975f91010148dc4c57bf3af3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/24/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\pos-handler.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Override POS request handler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 要求ハンドラーのオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can extend Commerce Data Exchange - Real-time service by adding extension methods to the RetailTransactionServiceEx class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>Real-time service enables retail clients to interact with retail functionality in real time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Override POS request handler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 要求ハンドラーのオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic explains how to override POS request handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、POS 要求ハンドラーをオーバーライドする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>We've introduced an extension pattern for overriding the POS business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ビジネス ロジックをオーバーライドするための拡張パターンを導入しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If you have a scenario where you want to modify/add some business logic to the core POS business flow, then you can follow this pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コア POS ビジネス フローにビジネス ロジックを変更/追加するシナリオがある場合、このパターンに従うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, when you sell a serial item, POS will display a dialog box where you can enter the serial number for that item after the scan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、シリアル品目を販売する場合、スキャン後、POS にはその品目のシリアル番号を入力するダイアログ ボックスが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you want to automate the serial number process by entering the serial number through code, then you can override this serial number request handler and use custom business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを使用してシリアル番号を入力することでシリアル番号プロセスを自動化する場合、このシリアル番号要求ハンドラーをオーバーライドしてカスタム ビジネス ロジックを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Most of the business logic in POS is implemented in request handler, however, you can override the relevant request handler and return the response according to your business flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS のビジネス ロジックのほとんどは、要求ハンドラーで実装されます。ただし、関連する要求ハンドラーをオーバーライドして、ビジネス フローに従って応答を返すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Not all request handler logic is exposed for customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての要求ハンドラー ロジックがカスタマイズ用に公開されるわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If you want to customize any business logic and if that request handler is not overridable, then create a support ticket or log a request in the LCS extensibility tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックをカスタマイズする場合で、その要求ハンドラーがオーバーライド可能でない場合、サポート チケットを作成するか、LCS 機能拡張ツールでリクエストを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>** POS request handler logic exposed for overriding **</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">**オーバーライドするために公開される POS 要求ハンドラー ロジック**</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This is list is based on <bpt id="p1">[</bpt>Microsoft Dynamics 365 for Finance and Operations - Version 7.3.5.<ept id="p1">](https://fix.lcs.dynamics.com/Issue/Details?kb=4456209&amp;bugId=235124&amp;qc=9fef9e411bd4f715508205b6c65b16afdc4096cea0f15e1535c3d8e3f13716c1)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、<bpt id="p1">[</bpt>Microsoft Dynamics 365 for Finance and Operations - バージョン 7.3.5<ept id="p1">](https://fix.lcs.dynamics.com/Issue/Details?kb=4456209&amp;bugId=235124&amp;qc=9fef9e411bd4f715508205b6c65b16afdc4096cea0f15e1535c3d8e3f13716c1)</ept> の一覧に基づいています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In each monthly update we will be adding additional extension points, so check the Pos.api.d.ts file in the Retail SDK for the full list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">毎月の更新プログラムのたびに、拡張ポイントが追加されるため、完全な一覧については Retail SDK で Pos.api.d.ts ファイルをチェックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>Cart extension handlers<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>買い物カゴ拡張ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Request name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要求名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>AddTenderLineToCartClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddTenderLineToCartClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This handler is executed when you add tender (payment) line to cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このハンドラーは、カートに支払/入金方法 (支払) 明細行を追加するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>GetKeyedInPriceClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetKeyedInPriceClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This handler is executed when you add an item that has a configuration key in price during sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このハンドラーは、販売時に、価格内にコンフィギュレーション キーを持つ品目を追加するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>GetPickupDateClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPickupDateClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Executed when you select a pickup date during a customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文時に集荷日を選択するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>GetShippingDateClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetShippingDateClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Executed when you select a shipping date during a customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文時に出荷日を選択するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>ShowChangeDueClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowChangeDueClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Executed when the change due dialog box is shown at the end of transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの終了時に期日の変更ダイアログ ボックスが表示されるときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>GetReceiptEmailAddressClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReceiptEmailAddressClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Executed when you get a receipt email address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">受信者のメール アドレスを取得するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>DepositOverrideOperationRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DepositOverrideOperationRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Executed when you override a deposit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">預金をオーバーライドするときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>GetShippingChargeClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetShippingChargeClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Executed when get shipping charge workflow initiated during customer order flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文フロー中に開始された出荷費用ワークフローを取得するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>Payment extension handler:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払拡張機能ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Request name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要求名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>説明<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>GetGiftCardByIdServiceRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetGiftCardByIdServiceRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>This handler is executed when you receive the gift card ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このハンドラーは、ギフト カード ID を受け取ると実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>GetPaymentCardTypeByBinRangeClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPaymentCardTypeByBinRangeClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This handler is executed when POS gets the card type, such as Visa or Master Card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このハンドラーは、Visa や Master Card などのカード タイプを POS が取得するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This is based on the HQ configuration during the card tender line processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、カード支払/入金の明細行の処理中の HQ コンフィギュレーションに基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Peripherals request handler<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>周辺機器要求ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Request name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>CardPaymentAuthorizePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentAuthorizePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Executed when a card payment is authorized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カード支払が承認されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>CardPaymentCapturePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentCapturePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Executed when a card payment is captured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カード支払が取得されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>CardPaymentExecuteTaskRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentExecuteTaskRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Used to execute any custom task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム タスクを実行するために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This handler is mainly for extensions for custom functionality with payment connector, which is not supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このハンドラーは、主に、サポートされていない支払コネクタを使用するカスタム機能の拡張機能用です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>CardPaymentRefundPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentRefundPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Executed when a card payment is refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カード支払が払戻しされたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>CardPaymentVoidPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentVoidPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Executed when a card payment is voided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カード支払が無効化されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>CardPaymentBeginTransactionRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentBeginTransactionRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Executed when a card payment is initiated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カード支払が開始されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>CardPaymentEndTransactionRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentEndTransactionRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Executed when a card payment is ended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カード支払が終了したときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>CardPaymentEnquireGiftCardBalancePeripheralRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentEnquireGiftCardBalancePeripheralRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Executed when a gift card balance inquiry is made.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードの残高照会が行われるときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>PaymentTerminalAuthorizePaymentActivityRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAuthorizePaymentActivityRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Executed when a card payment is authorized using a payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払が承認されたときに実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>PaymentTerminalAuthorizePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAuthorizePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Executed when a card payment is authorized using a payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払が承認されたときに実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>PaymentTerminalEnquireGiftCardBalancePeripheralRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalEnquireGiftCardBalancePeripheralRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Executed when a gift card balance inquiry is made using a payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してギフト カードの残高照会が行われるときに実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>PaymentTerminalExecuteTaskRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalExecuteTaskRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Used to execute any custom task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム タスクを実行するために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This handler is mainly for extensions for custom functionality with payment terminal/device, which is not supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このハンドラーは、主に、サポートされていない支払ターミナル/デバイスを使用するカスタム機能の拡張機能用です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>PaymentTerminalRefundPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalRefundPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Executed when a card payment is refunded using a payment terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払が払戻しされたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>PaymentTerminalUpdateLinesRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalUpdateLinesRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Executed when POS sends line item details to a payment device for display purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS が表示目的で明細行品目の詳細を支払デバイスに送信するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>PaymentTerminalVoidPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalVoidPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Executed when a card payment is voided using a payment terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払が無効化されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>PaymentTerminalBeginTransactionRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalBeginTransactionRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Executed when a card payment is initiated using a payment terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払が開始されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>PaymentTerminalCancelOperationRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalCancelOperationRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Executed when a card payment is cancelled using a payment terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払がキャンセルされたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>PaymentTerminalEndTransactionRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalEndTransactionRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Executed when a card payment is ended using a payment terminal/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル/デバイスを使用してカード支払が終了したときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>CashDrawerOpenRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CashDrawerOpenRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Executed when a cash drawer open request is initiated by POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ ドロワー オープン要求が POS によって開始されるときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>PaymentTerminalActivateGiftCardPeripheralRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalActivateGiftCardPeripheralRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Executed when activate gift card request is initiated by POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS により開始されたギフト カード要求をアクティブにしたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>PaymentTerminalAddBalanceToGiftCardPeripheralRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAddBalanceToGiftCardPeripheralRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Executed when add balance to gift card request is initiated by POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS により開始されたギフト カード要求に残高を追加したときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Scan request handler<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スキャン要求ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Request name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>GetScanResultClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetScanResultClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Executed when you scan or key in a POS transaction screen Numpad.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキャンするか、POS トランザクション画面テンキーで入力するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">**</bpt>Store fulfillment request handler<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>店舗フルフィルメント要求ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Request name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>PrintPackingSlipClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrintPackingSlipClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Executed when you print a packing slip from the store fulfillment view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗フルフィルメント ビューから梱包明細を印刷するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>MarkAsPickedServiceRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MarkAsPickedServiceRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Executed when you mark a sales line as picked from the store fulfillment view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗フルフィルメント ビューからピッキングされた販売注文明細行をマークするときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Store operations request handler<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>店舗運営要求ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Request name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>CreateTenderRemovalTransactionClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateTenderRemovalTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Executed when you do a tender removal operation in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で支払/入金の削除操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>CreateFloatEntryTransactionClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateFloatEntryTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Executed when you do a float entry operation in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で釣銭入力操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>SelectZipCodeInfoClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectZipCodeInfoClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Executed when you key in zip code in address add/edit view in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で住所の追加/編集ビューで郵便番号を入力するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>CreateStartingAmountTransactionClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateStartingAmountTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Executed when you do a start amount declaration in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で開始金額申告を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>LoyaltyCardPointsBalanceOperationRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LoyaltyCardPointsBalanceOperationRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Executed when you do a loyalty card balance operation in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS でロイヤルティ カード残高操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>GetReportParametersClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReportParametersClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Executed when you do a report parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート パラメーターを行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>If your POS report need input parameter this dialog will get executed to capture the parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS レポートに入力パラメーターが必要な場合は、このダイアログが実行されてパラメーターを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">**</bpt>Tender counting request handler<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払/入金計算要求ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Request name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>CreateSafeDropTransactionClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateSafeDropTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Executed when you do a safe drop operation in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で金庫保管操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>GetTenderDetailsClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetTenderDetailsClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Executed when you get tender declaration details in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で支払/入金申告の詳細を取得するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>CreateBankDropTransactionClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateBankDropTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Executed when you do a bank drop operation in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で銀行入金操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>CreateTenderDeclarationTransactionClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateTenderDeclarationTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Executed when you do a tender declaration operation in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で支払/入金申告操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>GetCountedTenderDetailAmountClientRequestHandler</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GetCountedTenderDetailAmountClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Executed when you do a tendercount detail in POS.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">POS で入札件数の詳細を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>CreateBankDropTransactionClientRequestHandler</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">CreateBankDropTransactionClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Executed when you do a bank drop operation in POS.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">POS で銀行入金操作を行うときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">**</bpt>Sales orders request handlers<ept id="p1">**</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>販売注文の要求ハンドラー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Request name</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">要求名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>GetGiftReceiptsClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetGiftReceiptsClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Executed when you print a gift receipt in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS でギフト レシートを印刷するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>SelectCustomerOrderTypeClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectCustomerOrderTypeClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Executed when you get a dialog box with options to choose between customer order or quote.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文または見積のどちらかを選択するオプションがあるダイアログ ボックスを取得するときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>GetCancellationChargeClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCancellationChargeClientRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Executed when you get a dialog box to enter the cancellation shipping charge during the customer order workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客注文ワークフロー中にキャンセル出荷費用を入力するダイアログ ボックスが表示されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">**</bpt>How to override a handler in POS<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS でハンドラーをオーバーライドする方法<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If you want to override any of the above POS request handler logic, you to need to use the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の POS 要求ハンドラー ロジックのいずれかをオーバーライドすると、次の手順を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Create a new class and extend it from the corresponding handler class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラスを作成し、対応するハンドラー クラスから拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>For example, if you are overriding GetSerialNumberClientRequestHandler, then extend your class from GetSerialNumberClientRequestHandler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、GetSerialNumberClientRequestHandler をオーバーライドする場合、クラスを GetSerialNumberClientRequestHandler から拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Implement the executeAsync method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">executeAsync メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Either call the default handler or do your custom logic inside the executeAsync method and return the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のハンドラーを呼び出すか、executeAsync メソッド内でカスタム ロジックを実行して、応答を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">**</bpt>Step by step instructions<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ バイ ステップの手順<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The following example shows how to override the GetSerialNumberClientRequestHandler to automate the serial number entry in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、GetSerialNumberClientRequestHandler をオーバーライドして POS でシリアル番号の入力を自動化する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>By default, POS will display a dialog box to enter the serial number if the item is configured to ask for serial number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、POS には、シリアル番号を要求するよう品目がコンフィギュレーションされている場合は、シリアル番号を入力するダイアログ ボックスが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>We want to avoid showing this dialog box and enter serial number through code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このダイアログ ボックスが表示されないようにし、コードを使用してシリアル番号を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Open Visual Studio 2015 in administrator mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者モードで Visual Studio 2015 を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Open ModernPOS solution from …<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModernPOS ソリューションを …<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS から開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Under the POS.Extensions project, create a new folder called POSRequestHandlerExtension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS.Extensions プロジェクトで、POSRequestHandlerExtension という名前の新しいフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Under the POSRequestHandlerExtension folder, create new folder called Handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POSRequestHandlerExtension フォルダーに、Handlers という名前の新しいフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>In the Handlers folder, add a new .ts (typescript) file and name it GetSerialNumberClientRequestHandlerExt.ts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handlers フォルダーに、新しい .ts (typescript) ファイルを追加し、GetSerialNumberClientRequestHandlerExt.ts と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Add the following import statement to import the relevant entities and context in the GetSerialNumberClientRequestHandlerExt.ts file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の import ステートメントを追加して、GetSerialNumberClientRequestHandlerExt.ts ファイルに関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>In the GetSerialNumberClientRequestHandlerExt.ts file, create a new class called GetSerialNumberClientRequestHandlerExtend and extend it from GetSerialNumberClientRequestHandler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSerialNumberClientRequestHandlerExt.ts ファイルで、GetSerialNumberClientRequestHandlerExtend という新しいクラスを作成し、GetSerialNumberClientRequestHandler から拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler { }</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler { }</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Implement the executeAsync method inside the GetSerialNumberClientRequestHandlerExt class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSerialNumberClientRequestHandlerExt クラス内に executeAsync メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>In the executeAsync method, you can write your custom logic and return the response or call the default handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">executeAsync メソッドでは、カスタム ロジックを書き込んで、応答を返すか、既定のハンドラーを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>When POS sells the serial item, it will look for executeAsync to execute the logic for the serial number, however because we are overriding it, POS will now execute this overridden executeAsync method instead of the standard method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS は、シリアル品目を販売するとき、シリアル番号のロジックを実行する executeAsync を探しますが、オーバーライドされるため、POS は標準メソッドの代わりにこのオーバーライドされた executeAsync メソッドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">**</bpt>Sample implementation of how to override the executeAsync method<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>executeAsync メソッドをオーバーライドする方法のサンプル実装<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Full sample code:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なサンプル コード:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Create a new json file under the POSRequestHandlerExtension folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POSRequestHandlerExtension フォルダーの下に新しい json ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Name it manifest.json.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">manifest.json という名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>In the manifest.json file, copy and paste the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">manifest.json ファイルに、次のコードをコピーして貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Be sure to delete the default generated code before copying this code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードをコピーする前に、既定で生成されたコードを削除してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Open the extensions.json file under the POS.Extensions project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS.Extensions プロジェクトにある extensions.json ファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Update it with POSRequestHandlerExtension samples, so that POS during runtime will include this extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時の POS にこの拡張が含まれるように、POSRequestHandlerExtension サンプルで更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>The extension.json file should always contain two extensions folder names, so be sure to keep the SampleExtensions folder name or your custom extension folder name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">extension.json ファイルには、常に 2 つの拡張フォルダー名が含まれている必要があるため、必ず SampleExtensions フォルダー名またはカスタム拡張フォルダー名を保持してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>For production, don’t use the sample extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産には、サンプル拡張を使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>You should add your own extension folders and remove all the samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">独自の拡張フォルダーを追加し、すべてのサンプルを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Open the tsconfig.json file to comment out the extension package folders from the exclude list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tsconfig.json ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>POS will use this file to include or exclude the extension for compilation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、このファイルを使用して、コンパイル用に拡張機能を追加または除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>By default, the list contains all the excluded extensions list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、リストに除外されたすべての拡張リストが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>If you want to compile any extension part of the POS, then you need to add the extension folder name and comment the extension from the extension list, as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS の拡張部分をコンパイルする場合は、拡張フォルダー名を追加し、以下のように拡張リストから拡張をコメント アウトする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Compile and rebuild the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source><bpt id="p1">**</bpt>How to test your extension<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張機能をテストする方法<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Press F5 and deploy the POS to test your customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 キーを押し、POS を展開してカスタマイズをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>After POS launches, sign in to POS and add a serial item to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS が開始されたら、POS にサインインし、トランザクションへシリアル品目を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Place a break point in the extension code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張コードにブレークポイントを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>When you add the serial item you should be able to debug the extension code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シリアル品目を追加するとき、拡張コードをデバッグできるはずです。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>