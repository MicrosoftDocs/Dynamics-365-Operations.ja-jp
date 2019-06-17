<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-payment-extension.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-payment-extension.fcb175.9e08f0a11d50e60270aab2009c4efd67b7d2f5f9.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>9e08f0a11d50e60270aab2009c4efd67b7d2f5f9</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\pos-payment-extension.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Point of sale (POS) payment extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) 支払拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>You can implement the core payment logic in the payment device or payment connector using the Hardware station APIs by using the extension points in POS to support payment extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払いの拡張性をサポートするために POS で拡張点を使用すると、ハードウェア ステーション API を使用する支払デバイスまたは支払コネクタに主要な支払いロジックを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Point of sale (POS) payment extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) 支払拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>With the extension points in point of sale (POS) to support payment extensibility, you can implement the core payment logic in the payment device or payment connector using the Hardware station APIs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払いの拡張性をサポートするために販売時点管理 (POS) の拡張点を使用すると、ハードウェア ステーション API を使用する支払デバイスまたは支払コネクタに主要な支払いロジックを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some scenarios where you might want to do this are:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うことがあるいくつかのシナリオは次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You need to pass additional information such as extension properties to your connector/device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能のプロパティなどの追加情報をコネクター/デバイスに渡す必要がある場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You want to show custom messages in between the payment flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払フロー間に、カスタム メッセージを表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You need input from the cashier to complete the flow and send an intermediate response back to the payment device/connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フローを完了して支払デバイス/コネクタの中間的な応答を送信するレジ担当者からの入力が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, you might need the customer ID validation status or voice authorization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客 ID の検証状態または音声認証を必要とする場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You want to show processing dialog messages, such as waiting for the customer pin input.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客 PIN 入力待ちなどの、処理ダイアログ メッセージを表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can override POS payment requests to implement these scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 支払い要求をオーバーライドしてこれらのシナリオを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You can override the following request handlers from the POS side to customize the payment flow:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 側から以下の要求ハンドラーをオーバーライドして、支払いフローをカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>PaymentTerminalAuthorizePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAuthorizePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>PaymentTerminalCapturePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalCapturePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>PaymentTerminalExecuteTaskRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalExecuteTaskRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>PaymentTerminalRefundPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalRefundPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>PaymentTerminalVoidPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalVoidPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The POS runtime checks the extension manifest to see if there are any extensions for these request handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ランタイムは、これらの要求ハンドラーに拡張機能があるかどうかを確認するために拡張子マニフェストをチェックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If there are extensions, then the runtime loads the extended requests and executes the overridden requests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能がある場合は、ランタイムは拡張要求をロードし、オーバーライドされた要求を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In the extension project, you can override these requests, add your own implementation to call the custom payment providers, and then update the response based on the status that is returned by your providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロジェクトでは、これらの要求をオーバーライドし、カスタム支払プロバイダーを呼び出す独自の実装を追加して、プロバイダーによって返されるステータスに基づいて応答を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>When you override a request, you are overriding only the core logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求を上書きするときは、コア ロジックのみを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>After all your custom logic has run, you send the updated response that you received from Hardware station (payment device/connector) to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのカスタム ロジックの実行後、ハードウェア ステーション (支払デバイス/コネクタ) から受信した更新済の応答を POS に送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>All the standard workflow is handled by the POS, so that you do not need to worry about how to add, void, or decline the payment line and conclude the transaction based on the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての標準ワークフローは POS によって処理されるため、支払ラインの追加、無効、拒否、および応答に基づいたトランザクションの完結の方法を心配する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>PaymentTerminalAuthorizePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAuthorizePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>PaymentTerminalAuthorizePaymentRequestHandler<ept id="p1">**</ept>, the authorization request, is the core payment request from POS that initiates and authorizes a card payment request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PaymentTerminalAuthorizePaymentRequestHandler<ept id="p1">**</ept>、承認要求は、カード支払要求を開始し許可する POS からのコア支払要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You can override this request if you want to change the authorize workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">承認ワークフローを変更する場合は、この要求をオーバーライドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>To override the request, you need to extend the <bpt id="p1">**</bpt>PaymentTerminalAuthorizePaymentRequestHandler<ept id="p1">**</ept> in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リクエストをオーバーライドにするには、POS の <bpt id="p1">**</bpt>PaymentTerminalAuthorizePaymentRequestHandler<ept id="p1">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You need to make these changes in PaymentHandlerHelper.ts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentHandlerHelper.ts にこれらの変更を加える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>After implementing the request logic, you need to update manifest.json with the extension information so that POS loads the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The full code sample, including how to pass extension properties, is available in Retail SDK app update 3 in the RetailSDK\Code\POS\Extensions\PaymentSample folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを渡す方法を含む、完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラム 3 で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>If you check in the above code sample, only the calling portion has been overridden, and not the core logic on how to complete the payment or add payment line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のコード サンプルをチェックインした場合、支払いの完了や支払明細行の追加方法における主要なロジックではなく、呼び出し部分のみがオーバーライドされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The POS workflow manages that.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ワークフローがこれを管理しきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>PaymentTerminalCapturePaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalCapturePaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>PaymentTerminalCapturePaymentRequestHandler<ept id="p1">**</ept>, the payment request, is a payment request from POS that initiates and captures the card payment request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PaymentTerminalCapturePaymentRequestHandler<ept id="p1">**</ept>、支払要求は、カード支払要求を開始し取得する POS からの支払要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Override this request if you want to change the capture workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプチャ ワークフローを変更する場合は、この要求をオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>To override the request, you need to extend the <bpt id="p1">**</bpt>PaymentTerminalCapturePaymentRequestHandler<ept id="p1">**</ept> in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リクエストをオーバーライドにするには、POS の <bpt id="p1">**</bpt>PaymentTerminalCapturePaymentRequestHandler<ept id="p1">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>After implementing the request logic, you need to update the manifest.json with the extension information so that POS loads the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Any requests that you override are specified in the manifest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上書きする要求はすべてマニフェストで指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If you didn’t override any of the standard requests, then you do not need to specify anything in the manifest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準要求のいずれかを上書きしなかった場合は、マニフェストに何も指定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The example of the manifest shows two overriden requests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マニフェストの例では、2 つの上書きされた要求が示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The full code sample, with how to pass extension properties, is available in Retail SDK app update in the RetailSDK\Code\POS\Extensions\PaymentSample folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを渡す方法に関する完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラムで利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>PaymentTerminalExecuteTaskRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalExecuteTaskRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>PaymentTerminalExecuteTaskRequestHandler<ept id="p1">**</ept>, the execution request, is used from POS to initiate any custom payment device/connector operation from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PaymentTerminalExecuteTaskRequestHandler<ept id="p1">**</ept>、POS からの任意のカスタム支払デバイス/コネクタ操作を開始するために POS から使用される実行要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You might use this to do a health check of the payment device from POS, to do batch processing, or for an end-of-day request to the payment device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS から支払デバイスの正常性チェックを行うため、バッチ処理を行うため、または支払デバイスへ営業終了要求のためには、これを使用する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can override this request if you want to do a custom operation other than the standard authorize, capture, void, and refund.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準の承認、キャプチャ、無効化、および払戻以外のカスタム オプションを実行する場合、この要求をオーバーライドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To override the request, you need to extend the <bpt id="p1">**</bpt>PaymentTerminalExecuteTaskRequestHandler<ept id="p1">**</ept> in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リクエストをオーバーライドにするには、POS の <bpt id="p1">**</bpt>PaymentTerminalExecuteTaskRequestHandler<ept id="p1">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>After implementing the request logic, you need to update the manifest.json with the extension information so that POS loads the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The full code sample, with how to pass extension properties, is available in Retail SDK app update 3 in the RetailSDK\Code\POS\Extensions\PaymentSample folder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを渡す方法に関する完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラム 3 で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>PaymentTerminalRefundPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalRefundPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">**</bpt>PaymentTerminalRefundPaymentRequestHandler<ept id="p1">**</ept>, the refund request, is a payment request from POS that initiates a refund or return of the card payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PaymentTerminalRefundPaymentRequestHandler<ept id="p1">**</ept>、カード要求の払戻または返金を開始する POS からの払戻要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You override this request if you want to change the refund workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">払戻ワークフローを変更する場合は、この要求をオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>To override the request, you need to extend the <bpt id="p1">**</bpt>PaymentTerminalRefundPaymentRequestHandler<ept id="p1">**</ept> in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リクエストをオーバーライドにするには、POS の <bpt id="p1">**</bpt>PaymentTerminalRefundPaymentRequestHandler<ept id="p1">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>PaymentTerminalVoidPaymentRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalVoidPaymentRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>PaymentTerminalVoidPaymentRequestHandler<ept id="p1">**</ept>, the void request, is a payment request from POS that initiates the void card payment request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PaymentTerminalVoidPaymentRequestHandler<ept id="p1">**</ept>、無効化要求、無効化カード支払要求を開始する POS からの支払要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>You override this request if you want to change the void workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なワークフローを変更する場合は、この要求をオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To override the request, you need to extend the <bpt id="p1">**</bpt>PaymentTerminalVoidPaymentRequestHandler<ept id="p1">**</ept> in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リクエストをオーバーライドにするには、POS の <bpt id="p1">**</bpt>PaymentTerminalVoidPaymentRequestHandler<ept id="p1">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Extending the void and refund request code pattern is same as the authorize and capture request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効および払い戻し要求コード パターンを拡張することは、承認および取得要求と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The full code sample for the void and refund payment request, with how to pass extension properties, is available in Retail SDK app update 3 in the RetailSDK\Code\POS\Extensions\PaymentSample folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを渡す方法とともに、無効および払い戻し支払要求の完全なコードサンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション 3 で利用できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>