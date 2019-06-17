<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="POS-APIs.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>POS-APIs.fcd98e.092253de911b724945760facf422d966e742f561.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>092253de911b724945760facf422d966e742f561</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>33e5f728a70d0546975f91010148dc4c57bf3af3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/24/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\POS-APIs.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail POS APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic contains a list of available POS APIs and how to access them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail POS APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Retail POS APIs help you to easily build extensions or new features to the POS app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>you can consume APIs that will do the work for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを実現する API を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To do this, you need to simply call the APIs to do the work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、作業を実行する API を呼び出す必要があるだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The POS API simplifies the extension pattern and provides continuous support to build the extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張パターンは、要求/応答のパターンに従って <ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>)、POS、ハードウェア ステーション (HWS) 間で統合されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>All the POS APIs are exposed as request/response like CRT and HWS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is applicable for Dynamics 365 for Finance and Operations or Dynamics 365 for Retail with the latest hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Dynamics 365 for Finance and Operations または Dynamics 365 for Retail 最新修正プログラムが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>POS APIs are categorized into three different scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API は、3 つのさまざまなシナリオに分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Consume<ept id="p1">**</ept> – Consume public APIs in your extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>消費<ept id="p1">**</ept> - 拡張機能のパブリック API を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Extend<ept id="p1">**</ept> – Override public APIs to do some additional logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張<ept id="p1">**</ept> - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Create<ept id="p1">**</ept> – Create new APIs using the exposed POS interface, which can be used across extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成<ept id="p1">**</ept> - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Many APIs can be consumed in extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API の多くは、拡張機能で消費できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>A list of the all of the APIs is available in <bpt id="p1">**</bpt>Pos.Api.d.ts<ept id="p1">**</ept>, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての API の一覧は、<bpt id="p1">**</bpt>Pos.Api.d.ts<ept id="p1">**</ept> にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Extensions must consume only the exposed request and response from the POS.Api.d.ts and no modification is allowed to Pos.Api.d.ts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Extensions should not consume or update any POS APIs, properties, methods, or handlers directly from POS commerce or sessions objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>How to consume APIs in your extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能で API を使用する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Use the following steps to consume Retail APIs in your extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能で Retail API を利用するには、次の手順を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Import the API in your extension file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能ファイルで API をインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The pattern is import { api name } from "PosApi/Consume/Module name";</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターンは、"PosApi/Consume/Module name" からの {api name} のインポートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Import the client entities and proxy entities if required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Samples showing how to access APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API にアクセスする方法を示すサンプル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Get Current cart<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>現在の買い物カゴを取得<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Get Current customer added to cart<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>買い物カゴに追加された現在の顧客を取得<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Force void transaction<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>強制無効トランザクション<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Cart</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The following is a list of APIs exposed to perform cart-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>AddPreprocessedTenderLineToCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddPreprocessedTenderLineToCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>AddTenderLineToCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddTenderLineToCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>ConcludeTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ConcludeTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>GetCurrentCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCurrentCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>GetCurrentCartClientResponse</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCurrentCartClientResponse</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GetKeyedInPriceClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetKeyedInPriceClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>GetPickupDateClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPickupDateClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>GetReasonCodeLinesClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReasonCodeLinesClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>GetReceiptEmailAddressClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReceiptEmailAddressClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>GetShippingDateClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetShippingDateClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>RefreshCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RefreshCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>ResumeSuspendedCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ResumeSuspendedCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>SaveAttributesOnCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveAttributesOnCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>SaveAttributesOnCartLinesClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveAttributesOnCartLinesClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>SaveExtensionPropertiesOnCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveExtensionPropertiesOnCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>SaveExtensionPropertiesOnCartLinesClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveExtensionPropertiesOnCartLinesClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>SaveReasonCodeLinesOnCartClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveReasonCodeLinesOnCartClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>SaveReasonCodeLinesOnCartLinesClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveReasonCodeLinesOnCartLinesClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>SelectSalesLinesForPickUpClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectSalesLinesForPickUpClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>SetCartAttributesClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SetCartAttributesClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>ShowChangeDueClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowChangeDueClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>AddAffiliationOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddAffiliationOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>AddItemToCartOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddItemToCartOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>CalculateTotalOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CalculateTotalOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>ChangeCartLineUnitOfMeasureOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ChangeCartLineUnitOfMeasureOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>CreateCustomerOrderOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateCustomerOrderOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>CreateCustomerQuoteOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateCustomerQuoteOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>CustomerAccountDepositOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerAccountDepositOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>DepositOverrideOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DepositOverrideOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>EditCustomerOrderOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EditCustomerOrderOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>LineDiscountAmountOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LineDiscountAmountOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>LineDiscountPercentOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LineDiscountPercentOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>OverrideLineTaxFromListOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OverrideLineTaxFromListOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>OverrideLineTaxOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OverrideLineTaxOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>OverrideTransactionTaxOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OverrideTransactionTaxOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>PickupAllOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PickupAllOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>PriceOverrideOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PriceOverrideOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>SetCartLineCommentOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SetCartLineCommentOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>SetCartLineQuantityOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SetCartLineQuantityOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>SetCustomerOnCartOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SetCustomerOnCartOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>SetTransactionCommentOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SetTransactionCommentOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>SuspendCurrentCartOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SuspendCurrentCartOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>TotalDiscountAmountOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TotalDiscountAmountOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>TotalDiscountPercentOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TotalDiscountPercentOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>VoidCartLineOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VoidCartLineOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>VoidTenderLineOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VoidTenderLineOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>VoidTransactionOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VoidTransactionOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>CreateEmptyCartServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateEmptyCartServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>GetTaxOverridesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetTaxOverridesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>UpdateTenderLineSignatureServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UpdateTenderLineSignatureServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>CarryoutSelectedProductsOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CarryoutSelectedProductsOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>AddCouponsOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddCouponsOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>CreateNonSalesTransactionServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateNonSalesTransactionServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>ReturnTransactionOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReturnTransactionOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>AddLoyaltyCardToCartOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddLoyaltyCardToCartOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Payments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The following is a list of APIs exposed to perform payment-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、支払に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>GetGiftCardByIdServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetGiftCardByIdServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>GetPaymentCardTypeByBinRangeClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPaymentCardTypeByBinRangeClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Peripherals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">周辺機器</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The following is a list of APIs exposed to perform peripheral-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>CardPaymentAuthorizePaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentAuthorizePaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>CardPaymentBeginTransactionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentBeginTransactionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>CardPaymentCapturePaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentCapturePaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>CardPaymentEndTransactionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentEndTransactionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>CardPaymentEnquireGiftCardBalancePeripheralRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentEnquireGiftCardBalancePeripheralRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>CardPaymentExecuteTaskRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentExecuteTaskRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>CardPaymentRefundPaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentRefundPaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>CardPaymentVoidPaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CardPaymentVoidPaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>CashDrawerIsOpenRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CashDrawerIsOpenRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>HardwareStationDeviceActionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HardwareStationDeviceActionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>HardwareStationStatusRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HardwareStationStatusRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>LineDisplayDisplayLinesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LineDisplayDisplayLinesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>PaymentTerminalAuthorizePaymentActivityRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAuthorizePaymentActivityRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>PaymentTerminalAuthorizePaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalAuthorizePaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>PaymentTerminalBeginTransactionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalBeginTransactionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>PaymentTerminalCancelOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalCancelOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>PaymentTerminalCapturePaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalCapturePaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>PaymentTerminalEndTransactionRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalEndTransactionRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>PaymentTerminalEnquireGiftCardBalancePeripheralRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>PaymentTerminalExecuteTaskRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalExecuteTaskRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>PaymentTerminalRefundPaymentActivityRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalRefundPaymentActivityRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>PaymentTerminalRefundPaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalRefundPaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>PaymentTerminalUpdateLinesRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalUpdateLinesRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>PaymentTerminalVoidPaymentRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PaymentTerminalVoidPaymentRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>PrinterPrintRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrinterPrintRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>ScaleReadRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ScaleReadRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>ScanResults</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ScanResults</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The following is a list of APIs exposed to perform scan results-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>GetScanResultClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetScanResultClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>The following is a list of APIs exposed to perform customer-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、顧客に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>GetCustomerClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>CreateCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>UpdateCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UpdateCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>SelectCustomerClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectCustomerClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Authentication</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>The following is a list of APIs exposed to perform authentication-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、認証に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>LogOffOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LogOffOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>DataService</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataService</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The following is a list of APIs exposed to perform data service-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>DataServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Device</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The following is a list of APIs exposed to perform device-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>GetDeviceConfigurationClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetDeviceConfigurationClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>GetExtensionProfileClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetExtensionProfileClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>GetHardwareProfileClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetHardwareProfileClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>GetAuthenticationTokenClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetAuthenticationTokenClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>GetConnectionStatusClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetConnectionStatusClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>GetActiveHardwareStationClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetActiveHardwareStationClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>GetApplicationVersionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetApplicationVersionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>GetChannelConfigurationClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetChannelConfigurationClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">診断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The following is a list of APIs exposed to perform diagnostics-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、診断に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>GetSessionInfoClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSessionInfoClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Dialog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The following is a list of APIs exposed to perform dialog-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>ShowMessageDialogClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowMessageDialogClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>IAlphanumericInputDialogResult</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IAlphanumericInputDialogResult</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>ShowAlphanumericInputDialogClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowAlphanumericInputDialogClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>ShowNumericInputDialogClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowNumericInputDialogClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>ShowListInputDialogClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowListInputDialogClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>ShowTextInputDialogClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ShowTextInputDialogClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Employee</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従業員</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The following is a list of APIs exposed to perform employee-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、従業員に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>GetLoggedOnEmployeeClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetLoggedOnEmployeeClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Formatters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーマッター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>The following is a list of APIs exposed to perform formatter-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>IBooleanFormatter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IBooleanFormatter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>ICurrencyFormatter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ICurrencyFormatter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>IDateFormatter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IDateFormatter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>ITransactionTypeFormatter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ITransactionTypeFormatter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>IPurchaseTransferOrderTypeFormatter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPurchaseTransferOrderTypeFormatter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>OrgUnits</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrgUnits</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The following is a list of APIs exposed to perform org units-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>GetOrgUnitConfigurationClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOrgUnitConfigurationClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>GetOrgUnitTenderTypesClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOrgUnitTenderTypesClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>InventoryLookupOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventoryLookupOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Products</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>The following is a list of APIs exposed to perform products-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、製品に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>GetProductsByIdsClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetProductsByIdsClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>GetCurrentProductCatalogStoreClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCurrentProductCatalogStoreClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>SelectProductVariantClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectProductVariantClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>GetSerialNumberClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSerialNumberClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>GetRefinerValuesByTextServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetRefinerValuesByTextServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>SelectProductClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectProductClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>SalesOrders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SalesOrders</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>The following is a list of APIs exposed to perform sales orders-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>GetReceiptsClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetReceiptsClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>RegisterPrintReceiptCopyEventRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RegisterPrintReceiptCopyEventRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>GetSalesOrderDetailsByTransactionIdClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSalesOrderDetailsByTransactionIdClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>GetGiftReceiptsClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetGiftReceiptsClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>RegisterPrintReceiptCopyEventRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RegisterPrintReceiptCopyEventRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>MarkAsPickedServiceRequest</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">MarkAsPickedServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>PrintPackingSlipClientRequest</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">PrintPackingSlipClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>PickUpCustomerOrderLinesClientRequest</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">PickUpCustomerOrderLinesClientRequest</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Shifts</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">シフト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>The following is a list of APIs exposed to perform shifts-related functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">次に、シフトに関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>CloseShiftOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloseShiftOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>CloseShiftOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CloseShiftOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>StockCountJournals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StockCountJournals</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The following is a list of APIs exposed to perform stock count journals-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>SyncAllStockCountJournalsClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SyncAllStockCountJournalsClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>StoreOperations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StoreOperations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>The following is a list of APIs exposed to perform store operations-related functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>POS API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>DeclareStartingAmountClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DeclareStartingAmountClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>GetSalesOrdersWithNoFiscalTransactionsRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSalesOrdersWithNoFiscalTransactionsRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>RegisterCustomAuditEventClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RegisterCustomAuditEventClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>GetOfflinePendingTransactionCountClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOfflinePendingTransactionCountClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>SaveFiscalTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveFiscalTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>SafeDropOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SafeDropOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>TenderDeclarationOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TenderDeclarationOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>TenderRemovalOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TenderRemovalOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>CreateBankDropTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateBankDropTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>CreateFloatEntryTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateFloatEntryTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>CreateStartingAmountTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateStartingAmountTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>CreateTenderDeclarationTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateTenderDeclarationTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>CreateTenderRemovalTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateTenderRemovalTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>GetDenominationTotalsClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetDenominationTotalsClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>SelectZipCodeInfoClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectZipCodeInfoClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>CreateSafeDropTransactionClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreateSafeDropTransactionClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>GetTenderDetailsClientRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetTenderDetailsClientRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>LoyaltyCardPointsBalanceOperationRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LoyaltyCardPointsBalanceOperationRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>GetCommissionSalesGroupsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCommissionSalesGroupsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>GetCurrenciesServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCurrenciesServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>GetSrsReportDataSetServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetSrsReportDataSetServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>SearchCommissionSalesGroupsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SearchCommissionSalesGroupsServiceRequest</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>