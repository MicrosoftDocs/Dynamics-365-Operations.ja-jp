<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="crt-services.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>crt-services.363669.35182afafd3649b9669564b289cdfc5a39975e20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>35182afafd3649b9669564b289cdfc5a39975e20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\crt-services.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Commerce runtime (CRT) services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) のサービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the Commerce runtime (CRT) services, which are a collection of portable .NET libraries that contain the core business logic for the retail channel and pricing functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、小売チャネルおよび価格設定機能のコア ビジネス ロジックを含むポータブル .NET ライブラリの集合である Commerce runtime (CRT) サービスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Commerce runtime (CRT) services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) のサービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Commerce runtime (CRT) is a collection of portable .NET libraries that contain the core business logic for the retail channel and pricing functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce runtime (CRT) は、小売チャネルおよび価格設定機能のコア ビジネス ロジックを含む、ポータブル .NET ライブラリの集合です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To add or modify any business logic, you should customize CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Retail Modern POS or Cloud POS calls CRT to request that it perform business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS またはクラウド POS は CRT を呼び出して、ビジネス ロジックの実行を要求します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>CRT processes the request and then sends the response back to retail point of sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT は要求を処理し、小売販売時点管理に応答を送り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Retail point of sale is like a thin client, all the business logic should be done in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売販売時点管理はシン クライアントのようで、すべてのビジネス ロジックを CRT で実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A CRT service is a group of requests/responses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT サービスは、要求/応答のグループです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Any time that you do something in POS, POS sends a request to Retail server, and Retail server calls CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で作業する際はいつでも、POSは Retail サーバーに要求を送り、Retail サーバーは CRT を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>CRT processes the request and sends back the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT は要求を処理し、応答を送り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This topic shows some important requests/responses that you can customize for your business scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ビジネス シナリオにカスタマイズ可能な重要な要求/応答の一部を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>There are three main layers in CRT:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT には、次の 3 つの主要なレイヤーがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Data Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>All CRT customization for business logic can be done in Services, Workflow or Data Access layers, other core layers that are required for CRT to work are runtime, authentication, and data access managers and you should avoid any customization on these layers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックのすべての CRT カスタマイズがワークフローまたはデータ アクセス レイヤーのサービスで実行可能で、CRT が作業するに必要な他のコア レイヤーは、ランタイム、認証、およびデータ アクセスのマネージャーであり、これらのレイヤーのカスタマイズは避ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Overall flow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的な流れ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The overall flow looks like this:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なフローは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>CRT service request <ph id="ph1">\&lt;</ph> <ph id="ph2">\&gt;</ph> Zero or more workflow requests <ph id="ph3">\&lt;</ph> <ph id="ph4">\&gt;</ph> Zero or more data access requests</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT サービス要求<ph id="ph1">\&lt;</ph><ph id="ph2">\&gt;</ph> 1 つ以上のワークフロー要求<ph id="ph3">\&lt;</ph><ph id="ph4">\&gt;</ph> 1 つ以上のデータ アクセス要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For example, multiple workflow and data access requests are called to perform the <bpt id="p1">**</bpt>Create sales order<ept id="p1">**</ept> service request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、複数のワークフローおよびデータ アクセス要求が呼び出されて<bpt id="p1">**</bpt>販売注文の作成<ept id="p1">**</ept>サービス要求が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>CRT services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Each CRT service contains one or more requests/responses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 CRT サービスには、1 つ以上の要求または応答が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>For example, the Customer service in CRT contains all the customer-related requests/responses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、CRT の顧客サービスには、顧客関連のすべての要求/応答が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Each request/response is run in a different flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各要求または応答は、さまざまなフローで実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Default CRT services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の CRT サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Many services in CRT support the functionality of the retail channel and store operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT の多くのサービスは、小売チャンネルおよび店舗運営の機能をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You can add your own services or extend the existing services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">独自のサービスを追加したり、既存のサービスを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The following table describes some of the services that you might customize for various business services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表では、さまざまなビジネス サービス用にカスタマイズする可能性があるサービスの一部について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For more information about each service, see the CRT request/response document in the Retail software development kit (SDK), at …<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Code<ph id="ph3">\\</ph>Documents<ph id="ph4">\\</ph>CommerceRuntimeMessages.chm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各サービスの詳細については、以下のRetail ソフトウェア開発キット (SDK) の CRT 要求/応答 ドキュメントを参照してください。 …<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Code<ph id="ph3">\\</ph>Documents<ph id="ph4">\\</ph>CommerceRuntimeMessages.chm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>AddressService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddressService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>This service verifies addresses and gets location information, such as cities, counties, or states.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、住所を確認し、市町村、市区郡、都道府県などの場所情報を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>BarcodeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BarcodeService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This service processes the barcode that was scanned, based on the mask and barcode types, and calculates the quantity and price from the barcode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、マスクとバーコード タイプに基づいて、スキャンしたバーコードを処理し、バーコードから数量と価格を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>CartService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CartService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This service gets the cart from the transaction and sales transaction service from the transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、トランザクションからカートを取得し、トランザクション テーブルから販売トランザクション サービスを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>ChargeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ChargeService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This service implements logic that calculates automatic charges, price charges, and shipping charges for transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、自動請求、諸費用価格、およびトランザクションの出荷費用を計算するロジックを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>CouponService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CouponService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This service validates and updates coupon-related requests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、検証およびクーポン関連の要求を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>CurrencyService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CurrencyService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>This service converts currencies, based on exchange rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、為替レートに基づいて通貨を変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>CustomerService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>This service contains customer related operations such as Save cusotomer, purchase history, get customer and customer balance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスには顧客の保存、購買履歴、顧客の取得および顧客残高などの、顧客に関連する操作が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>EmployeeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従業員サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This service gets employee-related information and employees by store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、従業員関連の情報と店舗別の従業員を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>FormattingService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FormattingService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This service implements logic for the format of numbers, currencies, and dates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、数字、通貨、および日付の形式のロジックを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>GiftCardService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GiftCardService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This service provides information about internal activities that are related to gift cards, such as issuing the gift card, getting the balance, and adding value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、ギフト カードの発行、残高の取得、値の付加などのギフト カードに関連する内部の活動に関する情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>LoyaltyService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LoyaltyService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This service implements a program that rewards repeat customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、リピート顧客に報酬を与えるプログラムを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>NotificationService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NotificationService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>This service maintains the POS notification service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、POS 通知サービスを管理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>PaymentService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>This service lets you connect your online store to a payment service to provide credit card authorization and use preconfigured payment processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスでは、オンライン ストアから支払サービスに接続し、クレジット カード認証を提供し、コンフィギュレーション済の支払処理を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can also extend the payment service to add additional third-party payment processors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、支払いサービスを拡張して、サード パーティの支払いプロセッサを追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>ProductService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This service gets product-related and variant-related information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、製品関連およびバリアントに関連する情報を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>ProductsService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductsService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>This service gets information that is related to products and variants.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、製品およびバリアントに関連する情報を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>PricingService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PricingService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This service gets the price of an item in real time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、リアル タイムで品目の価格を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The price is adjusted, based on the base price and any applicable discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準価格および任意の利用可能な割引に基づいて、価格が調整されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Discounts can be customized for each retailer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各小売業者の割引をカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>ProductAvailabilityService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductAvailabilityService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This service calculates the quantities of products that are available to sell.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、販売可能な製品の数量を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>ReasonCodeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReasonCodeService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>This service calculates and gets the required reason code for POS operations or any workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、POS 操作またはワークフローに対して必要な理由コードを取得し計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>ReceiptService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReceiptService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>This service gets and formats the receipt details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは入庫の詳細を取得し、フォーマットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>RoundingService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RoundingService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>This service rounds the tender amount, based on the tender type and store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、支払/入金タイプおよび店舗に基づいて、支払/入金金額を丸めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>SalesOrderService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SalesOrderService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This service creates a sales order, based on a customer shopping cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、顧客のショッピング カートに基づいて、販売注文を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>SearchProductsService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SearchProductsService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This service searches products, based on the input text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、入力テキストに基づいて、製品を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>ShippingService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShippingService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This service calculates shipping costs and determines shipping options for the current order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、送料を計算し、現在の注文の出荷オプションを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>StockCountService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StockCountService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This service creates, commits, and synchronizes stock journals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは在庫仕訳帳を作成し、コミット、および同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>StoreOperationService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StoreOperationService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>This service maintains store-related operation services, such as Save and Drop, Tender declaration, and Search journal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、保存と削除、支払/入金申告、および仕訳帳の検索など店舗関連の工程のサービスを管理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>TaxService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>This service calculates the sales tax for the current order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、現在の注文に対する売上税を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You can use sales tax information from Microsoft Dynamics 365 for Finance and Operations, or from a third-party sales tax service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations からの売上税情報を、またはサード パーティ売上税サービスからの売上税情報を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>TotalingService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TotalingService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>This service calculates the totals on the sales transactions and sales lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサービスは、販売トランザクションおよび販売明細行の合計を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For extension scenarios, you can override any of the requests in the service class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張シナリオでは、サービス クラス内の要求のいずれかを上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>For example, to change the customer search flow, extend the <bpt id="p1">**</bpt>CustomersSearchServiceRequest<ept id="p1">**</ept> request from the <bpt id="p2">**</bpt>CustomerService<ept id="p2">**</ept> service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客の検索フローを変更するには、<bpt id="p2">**</bpt>CustomerService<ept id="p2">**</ept> サービスから、<bpt id="p1">**</bpt>CustomersSearchServiceRequest<ept id="p1">**</ept> リクエストを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>You don't customize the service class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス クラスをカスタマイズしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Instead, you extend the request/response in the service class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、サービス クラス内の要求/応答を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>By itself, the service class doesn't have any logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ自体では、サービス クラスにはロジックがありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>It just routes the call to the correct request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しい要求への呼び出しをルーティングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Sample service class implementation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス クラス実装の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Extension pattern for CRT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT 拡張パターン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Create a new service class, and implement one or more requests/responses<ept id="p1">**</ept> – Use this approach to create a new feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいサービス クラスを作成し、1 つまたは複数の要求 / 応答を実装<ept id="p1">**</ept> – このアプローチを使用して、新しい機能を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Override the core request/response<ept id="p1">**</ept> – Use this approach to modify the standard workflow or business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コア要求/応答のオーバーライド<ept id="p1">**</ept> – このアプローチを使用して、標準ワークフローまたはビジネス ロジックを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Add a pre-trigger or post-trigger for any request/response<ept id="p1">**</ept> – Use this approach to add business logic or add custom fields, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>応答/要求のプレ トリガーまたはポスト トリガーの追加<ept id="p1">**</ept> – このアプローチを使用して、ビジネス ロジックまたはカスタム フィールドなどを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>It doesn't matter whether you create a data access request, a workflow request, or a service request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アクセス要求、ワークフロー要求、またはサービス要求を作成するかどうかは重要ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Everything in CRT is a request/response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT のすべての内容は、要求または応答です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You write the logic that is required in the request/response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求/応答に必要なロジックを記述します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Although the requests are classified into different types for logical reasons, everything is the same from the framework perspective.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求が論理上の理由から異なるタイプに分類されても、全て同じフレームワーク観点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The following three classes will be implemented in all our requests/responses:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の 3 つのクラスは、すべての要求/応答で実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>Request class<ept id="p1">**</ept> – This class is POS/Retail server/E-commerce/CRT workflow class that is the request to do something.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラスのリクエスト<ept id="p1">**</ept> – このクラスは、POS/Retail サーバー/E コマース/CRT ワークフロー クラスの作業の要求を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Response class<ept id="p1">**</ept> – This class returns the response, based on the request to the caller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>応答クラス<ept id="p1">**</ept> – このクラスは、呼び出し元の要求に基づいて、応答を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><bpt id="p1">**</bpt>Handler class<ept id="p1">**</ept> – This class contains the core logic for the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ハンドラー クラス<ept id="p1">**</ept> – このクラスには、要求のコア ロジックが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>In the handler class, you can call other requests, do custom logic, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラー クラスで、他の要求を呼び出して、カスタム ロジックなどを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Request class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスのリクエスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Response class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">応答クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Handler class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラー クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>AddressService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddressService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The Address service supports the following requests/responses for various extension scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">住所サービスでは、さまざまな拡張シナリオに対する次の要求/応答をサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>GetCountryRegionsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCountryRegionsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>This request gets the list of countries and regions that are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、サポートされている国および地域の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>GetStateProvincesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetStateProvincesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>This request gets the list of states or provinces that are supported for the country or region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、国または地域でサポートされている都道府県の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>GetCitiesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCitiesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>This request gets the list of cities that are supported for the state or region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、州または地域でサポートされている市町村の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>GetDistrictServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetDistrictServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This request gets the list of districts that are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、サポートされている地域の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>GetZipCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetZipCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>This request gets the list of ZIP Codes that are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、サポートされている郵便番号の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>GetFromZipPostalCodeServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetFromZipPostalCodeServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>This request gets the list of postal codes supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、サポートされている郵便番号の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>GetAddressFormattingServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetAddressFormattingServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This request gets the address format for the specified country or region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、指定した国または地域の住所書式を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>BarcodeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BarcodeService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>ProcessMaskSegmentsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProcessMaskSegmentsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>This request processes the barcode, based on the barcode mask configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、バーコード マスクのコンフィギュレーションに基づいて、バーコードを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>GetBarcodeTypeServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetBarcodeTypeServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>This request gets the types of barcodes that are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、サポートされているバーコードのタイプを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>CalculateQuantityFromPriceServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateQuantityFromPriceServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>This request calculates the price and quantity, based on the barcode that is scanned or entered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、価格と数量はスキャンまたは入力されたバーコードに基づいて計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>CartService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CartService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>GetSalesTransactionsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSalesTransactionsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>This request gets the sales transaction from Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、小売用バックオフィスから販売トランザクションを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>GetCartServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCartServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This request gets the cart from the sales transaction table by using the cart ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カート ID を使用して、販売トランザクション テーブルからカートを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>CalculateSalesTransactionServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateSalesTransactionServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>This request calculates the various sales transaction totals, based on the specified calculation mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、指定した計算モードに基づいて、各種販売トランザクションの合計が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>CalculateEstimatedShippingAuthorizationAmountServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateEstimatedShippingAuthorizationAmountServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>This request calculates the estimated shipping authorization amount on the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、トランザクションでの見積配送承認金額が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>ConvertSalesTransactionToCartServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ConvertSalesTransactionToCartServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>This request converts the sales transaction to a cart transaction, based on transaction ID that is passed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、渡されるトランザクション ID に基づいて、販売トランザクションがカート トランザクションに変換されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>CouponService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CouponService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>UpdateCouponCodesOnCartServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UpdateCouponCodesOnCartServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This request updates the coupon codes status in Retail headquarters, based on the coupons that are used in the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カートで使用されているクーポンに基づいて、小売用バックオフィス内のクーポン コードの状態を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>ValidateCouponCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateCouponCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>This request validates the coupon code that is entered in the transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、トランザクションに入力されたクーポン コードを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>UpdateCouponUsageServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UpdateCouponUsageServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This request updates coupon usage for the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、トランザクションのクーポンの使用状況を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>CustomerService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>SaveCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>This request is called when you save a customer from the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS から顧客を保存する場合に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>GetCustomersServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomersServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>This request gets the selected customer details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、選択した顧客の詳細を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>CustomersSearchServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomersSearchServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>This request is run when you search for a customer from the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS から顧客の検索を行う場合に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>GetCustomerGroupsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerGroupsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>This request gets the customer group details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客グループの詳細を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>InitiateLinkToExistingCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InitiateLinkToExistingCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>This request is an internal request for backward compatibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、下位互換性のための内部要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>FinalizeLinkToExistingCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinalizeLinkToExistingCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>This request is an internal request for backward compatibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、下位互換性のための内部要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>UnlinkFromExistingCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UnlinkFromExistingCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>This request is an internal request for backward compatibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、下位互換性のための内部要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>GetCustomerBalanceServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerBalanceServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>This request gets the balance of the customer's account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客の勘定の残高を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>GetOrderHistoryServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOrderHistoryServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>This request gets the customer's order history.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客の注文履歴を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>GetPurchaseHistoryServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPurchaseHistoryServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>This request gets the history of the customer's recent purchases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客の最近の購入履歴を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>CustomerSearchByFieldsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSearchByFieldsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This request is run when you search customer by using fields such as name, phone number etc. (hint search).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、名前、電話番号などのフィールドを使用して顧客を検索するときに実行されます (ヒント検索)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>GetCustomerSearchFieldsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerSearchFieldsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This request gets the list of customer search fields (hint fields).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>PricingService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PricingService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>CalculatePricesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculatePricesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>This request calculates the price for each item that is added to the cart and on the search screen.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、カートと検索画面に追加される各品目の価格が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>CalculateDiscountsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateDiscountsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>This request calculates the discount for each item that is added to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、カートに追加する各品目の割引が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>GetIndependentPriceDiscountServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetIndependentPriceDiscountServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>This request calculates the price for each item on the price check screen and in other non-transaction-related flows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、価格チェック画面の各品目とその他の非トランザクション関連のフローの価格が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>ValidateDiscountsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateDiscountsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>This request validates the discount that is entered, based on the employee.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は従業員に基づいて、入力された割引を検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>GetAllPeriodicDiscountsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetAllPeriodicDiscountsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>This request gets all the periodic discounts that are configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、コンフィギュレーションされたすべての期間割引を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>GetDiscountCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetDiscountCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>This request gets all the discount codes that are configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、コンフィギュレーションされたすべての割引コードを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>ProductService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>ProductSearchServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductSearchServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>This request gets the product list, based on the search text from the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS からの検索テキストに基づいて、製品リストを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>(This is an old request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(これは以前の要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For customization, use the new <bpt id="p1">**</bpt>SearchProductsServiceRequest<ept id="p1">**</ept> request instead.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズでは、新しい <bpt id="p1">**</bpt>SearchProductsServiceRequest<ept id="p1">**</ept> 要求を代わりに使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>GetProductServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetProductServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>This request gets the product, based on the product ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、製品 ID に基づいて製品を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>GetProductRefinersRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetProductRefinersRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>This request retrieves the product refiner values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、製品のリファイナーの値を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>ProductsService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductsService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>GetProductsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetProductsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>This request gets the products, based on the products IDs that are provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は用意されている製品の ID に基づいて、製品を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>GetVariantProductsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetVariantProductsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>This request gets specific variations of master type products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、マスター タイプ製品の特定のバリエーションを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>ReasonCodeService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReasonCodeService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>GetReasonCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReasonCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>This request gets the required reason code for the workflow or POS operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、ワークフローまたは POS 操作に対して必要な理由コードを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>CalculateRequiredReasonCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateRequiredReasonCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>This request calculates the required reason code for the workflow or POS operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、ワークフローまたは POS 操作に対して必要な理由コードが計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>CalculateCartRequiredReasonCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateCartRequiredReasonCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>This request calculates the required reason code for the cart workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、カート ワークフローに必要な理由コードが計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>CalculateDropAndDeclareTransactionRequiredReasonCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateDropAndDeclareTransactionRequiredReasonCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>This request calculates the required reason code for the drop and tender declaration transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、ドロップおよび支払/入金申告トランザクションに必要な理由コードが計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>CalculateNonSalesTransactionRequiredReasonCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateNonSalesTransactionRequiredReasonCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>This request calculates the required reason code for the non-sales transaction, such as tender declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、支払/入金申告などの販売以外のトランザクションに必要な理由コードが計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>GetReturnOrderReasonCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReturnOrderReasonCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This request gets the required reason code for the return transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、返品トランザクションに対して必要な理由コードを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>ValidateReasonCodeLineForUpdateServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateReasonCodeLineForUpdateServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>This request validates the reason code lines that are added during the save cart request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カート要求の保存中に追加された理由コード行を検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>ReceiptService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReceiptService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>GetReceiptServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReceiptServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>This request gets the receipt type and generates the receipt data, based on the receipt type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求はレシート タイプに基づいて、レシート タイプを取得しレシート データを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>GetCustomReceiptFieldServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomReceiptFieldServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Override this request, and add custom logic for your custom fields that are added in the receipt.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求を上書きし、受領書に追加されるカスタムフィールドのカスタム ロジックを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>GetEmailReceiptServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetEmailReceiptServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>This request gets the formatted receipts that will be used for print and email scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、印刷と電子メールのシナリオで使用される書式設定された領収書を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>PopulateTaxSummaryIndiaServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PopulateTaxSummaryIndiaServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>This request populates the tax summary for India transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、インドのトランザクションの税集計を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>SearchProductsService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SearchProductsService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>SearchProductsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SearchProductsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>This request is run when you search for a product from the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS から製品の検索を行う場合に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>TaxService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TaxService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>CalculateTaxServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateTaxServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>This request calculates taxes on the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、トランザクションの税額が計算されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>AssignTaxCodesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AssignTaxCodesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>This request assigns tax codes on the transaction's taxable items before the tax calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、税計算前にトランザクションの課税対象の品目に対して税コードが割り当てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>The default tax calculation handler of the <bpt id="p1">**</bpt>CalculateTaxServiceRequest<ept id="p1">**</ept> request uses this message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CalculateTaxServiceRequest<ept id="p1">**</ept> 要求の既定の税計算ハンドラーはこのメッセージを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>PopulateTaxRatesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PopulateTaxRatesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>This request populates tax rates for the recalled transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、取り消されたトランザクションの税率を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>No tax percentage information is persisted for tax lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">税明細行に対する税率情報は永続化されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>This message handler restores the information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメッセージ ハンドラーは、情報を復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Workflow layer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー レイヤー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>On top of the Services layer is the Workflow layer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス レイヤーの上は、ワークフロー レイヤーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>A workflow is a collection of services and business logic that together define business processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローは、サービスとビジネス ロジックを共に業務プロセスを定義するコレクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>For example, when a customer adds an item to the cart, you can use a workflow to get the price, do validation, check the inventory quantity, calculate shipping, calculate tax, and calculate discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客がカートに品目を追加すると、価格の取得、検証の実行、在庫数量の確認、出荷費用の計算、税計算、および割引計算をするためワークフローを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>You can customize the existing workflows, or you can create new workflows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のワークフローをカスタマイズすることも、新しいワークフローを作成することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>You can even use a workflow to connect to a third-party system as part of your business processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローを使用して、業務プロセスの一部としてサードパーティ製システムに接続することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Just like services, workflows use the request/response pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスと同じように、ワークフローは要求/応答パターンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>The request object inherited from the base CRT <bpt id="p1">[</bpt>Request<ept id="p1">](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.request.aspx)</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本 CRT <bpt id="p1">[</bpt>要求<ept id="p1">](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.request.aspx)</ept> クラスから継承された要求オブジェクト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>The response object inherited from the base CRT <bpt id="p1">[</bpt>Response<ept id="p1">](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.response.aspx)</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本 CRT <bpt id="p1">[</bpt>応答<ept id="p1">](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.response.aspx)</ept> クラスから継承された応答オブジェクト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>A workflow also has a request handler class that extends the <bpt id="p1">[</bpt>WorkflowRequestHandler&lt;TRequest, TResponse&gt;<ept id="p1">](https://technet.microsoft.com/en-us/library/jj764791.aspx)</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローには、<bpt id="p1">[</bpt>WorkflowRequestHandler&lt;TRequest, TResponse&gt;<ept id="p1">](https://technet.microsoft.com/en-us/library/jj764791.aspx)</ept> クラスを拡張する要求ハンドラー クラスもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>To create a workflow, you create a request class and a response class, and you then create a request handler class that contains the business logic for the workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローを作成するには、要求クラスおよび応答クラスを作成し、ワークフローのビジネス ロジックが含まれる要求ハンドラー クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>For example, when you create a cash-and-carry transaction or a customer order, many different steps or workflows are completed before the order is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、現金払いトランザクションまたは顧客からの注文を作成する場合、注文が作成される前に、多くの異なるステップやワークフローが完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>One of the workflow steps in the order process is the Save cart request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文プロセスでのワークフロー ステップの 1 つは、カート要求の保存です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>The Save cart request workflow is responsible for saving any changes that are made to the cart from the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カート要求ワークフローの保存は、POS からカートに加えられる変更の保存を担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>For example, when you add an item to the cart, change the quantity, and so on, anything that you do in the POS will cause a call to the SaveCart to save the changes to the POS and database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、買い物カゴに品目を追加したり、数量を変更するなど POS で行う行為は、SaveCart を呼び出して POS とデータベースに変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>The following three classes will be implemented in the Save cart request workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の 3 つのクラスは、カート要求ワークフローの保存で実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Request class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスのリクエスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Response class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">応答クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Handler class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラー クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>All your workflow classes will follow the same pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのワークフロー クラスは、同じパターンに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Default workflows and handlers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のワークフローとハンドラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>The following table lists the default workflow requests and response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表では、既定のワークフローの要求と応答の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>CRT services call the workflows request and response based on the operation you perform in retail point of sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT サービスは、ワークフロー要求を呼び出し、小売販売時点管理で実行する操作に基づいて応答します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>You can customize any of these workflows request and response according to your business scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス シナリオに従って、これらのワークフローの要求と応答のいずれかをカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Handler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>AddOrderInvoiceToCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddOrderInvoiceToCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>AddOrderInvoiceToCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddOrderInvoiceToCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>This request adds the invoice to the cart as a cart line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、請求書はカート行としてのカートに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>AddOrRemoveDiscountCodesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddOrRemoveDiscountCodesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>AddOrRemoveDiscountCodesRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddOrRemoveDiscountCodesRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>This request adds discount codes to the cart or removes them from the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、割引コードはカートに追加またはカートから削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>CancelOrderRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CancelOrderRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>CancelOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CancelOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>This request is triggered when you cancel an order from the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS から注文をキャンセルすると、この要求が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>CopyCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CopyCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>CopyCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CopyCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>This request creates an identical shopping cart that has the specified cart type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、指定されたカート タイプを含む同一のショッピング カートを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>GetAddressRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetAddressRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>GetAddressRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetAddressRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>This request gets the address from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、リストから住所を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>GetCardPaymentAcceptPointRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCardPaymentAcceptPointRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>GetCardPaymentAcceptPointRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCardPaymentAcceptPointRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>This request shows the accepting page for card payment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カード支払の受諾ページを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>GetCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>GetCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>This request gets the shopping cart, based on the cart search criteria.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求はカート検索基準に基づいて、ショッピング カートを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>GetDiscountCodesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetDiscountCodesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>GetDiscountCodesRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetDiscountCodesRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>This request gets the discount codes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、割引コードを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>GetOrdersRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOrdersRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>GetOrdersRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOrdersRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>This request gets sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、販売注文を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>GetPromotionsRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPromotionsRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>GetPromotionsRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPromotionsRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>This request gets the shopping cart together with promotion lines for the cart and the cart items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カートおよびカートの品目のプロモーション ラインと共にショッピング カートを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>GetScanResultRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetScanResultRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>GetScanResultRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetScanResultRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>This request gets the entity details, based on the details that are scanned or typed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、スキャンまたは入力した情報に基づいて、エンティティの詳細を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>GetSupportedCardTypesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSupportedCardTypesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>GetSupportedCardTypesRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSupportedCardTypesRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>This request retrieves the cart types that are supported for the specified currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、指定された通貨に対してサポートされているカートのタイプを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>IssueOrAddToGiftCardRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IssueOrAddToGiftCardRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>IssueOrAddToGiftCardRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IssueOrAddToGiftCardRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>This request issues a gift card or adds to a gift card's balance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、ギフト カードを発行またはギフト カードの残高に加算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>PickAndPackOrderRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PickAndPackOrderRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>PickAndPackOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PickAndPackOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>This request represents a request for picking list creation and packing slip creation for a customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客注文に対するピッキング リストの作成および梱包明細の作成の要求を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>PickupAtStoreRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PickupAtStoreRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>PickupAtStoreRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PickupAtStoreRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>This request represents a request for pick-up at the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、店舗での集荷の要求を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>RecalculateOrderRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecalculateOrderRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>RecalculateOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecalculateOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>This request represents a request for the recalculate order workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、注文ワークフローを再計算するための要求を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>RecallCustomerOrderRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecallCustomerOrderRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>RecallCustomerOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecallCustomerOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>This request gets sales orders and converts them into a cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、販売注文を取得し、カートに変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>RecallSalesInvoiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecallSalesInvoiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>RecallSalesInvoiceRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RecallSalesInvoiceRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>This request gets invoices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、請求書を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>ResumeCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ResumeCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>ResumeCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ResumeCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>This request represents a request to resume a cart that was suspended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、中断されたカートを再開するための要求を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>SaveCartLinesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCartLinesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>SaveCartLinesRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCartLinesRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>This request represents a request for create, update, delete, or void operations on the cart line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カート行での作成、更新、削除、または無効操作の要求を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>SaveCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>SaveCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>This request is triggered when you make any changes in that POS that affect the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カートに影響を与える変更を POS で行うときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>SaveCustomerOrderRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCustomerOrderRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>SaveCustomerOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCustomerOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>This request initiates a request to save the customer order, based on the specified cart identifier and payment card information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求では、指定されたカート ID と支払カードの情報に基づいて、顧客注文を保存するための要求が開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>SaveReasonCodeLineRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveReasonCodeLineRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>SaveReasonCodeLineRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveReasonCodeLineRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>This request adds or updates a reason code on the cart line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、理由コードはカート行で追加または更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>SaveTenderLineRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveTenderLineRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>SaveTenderLineRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveTenderLineRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>This request adds, removes, or updates a tender line for the given shopping cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、指定されたショッピング カートに対して支払/入金の明細行が追加、削除、または更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>SaveVoidTransactionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveVoidTransactionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>SaveVoidTransactionRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveVoidTransactionRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>This request voids a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、トランザクションを無効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>SubmitSalesTransactionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SubmitSalesTransactionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>SubmitOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SubmitOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>This request initiates a request to submit the sales transaction, based on the specified cart identifier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求では、指定されたカート ID に基づいて、販売トランザクションを送信するための要求が開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>SuspendCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SuspendCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>SuspendCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SuspendCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>This request represents a request to suspend the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、カートを中断するための要求を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>TransferCartRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransferCartRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>TransferCartRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransferCartRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>This request transfers the specified shopping cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、指定されたショッピング カートを転送します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>UpdateCommissionSalesGroupRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UpdateCommissionSalesGroupRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>UpdateCommissionSalesGroupHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UpdateCommissionSalesGroupHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>This request encapsulates a request for updating the sales representative on the cart or the cart line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求により、カートまたはカート行の販売担当者を更新するための要求がカプセル化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>UploadOrderRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UploadOrderRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>UploadOrderRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UploadOrderRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>This request uploads the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、販売注文をアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>ValidateCartForCheckoutRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateCartForCheckoutRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>ValidateCartForCheckoutRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ValidateCartForCheckoutRequestHandler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>This request validates the cart for checkout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、チェックアウトのカートを検証します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>