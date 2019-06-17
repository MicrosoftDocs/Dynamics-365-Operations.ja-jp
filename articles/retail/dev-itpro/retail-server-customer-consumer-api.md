<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-server-customer-consumer-api.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-server-customer-consumer-api.61286b.d202ad2403eb93e6424e54be2d87cc7f45c36c8c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d202ad2403eb93e6424e54be2d87cc7f45c36c8c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-server-customer-consumer-api.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail Server customer and consumer APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーの顧客およびコンシューマー API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article provides an overview of the APIs that are available across various roles, and that can be used by various clients.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、さまざまな役割で利用可能であり、さまざまなクライアントで使用できる API の概要について説明します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>The focus is on customer-facing application clients and eCommerce clients.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Retail Server customer and consumer APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーの顧客およびコンシューマー API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article provides an overview of the APIs that are available across various roles, and that can be used by various clients.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、さまざまな役割で利用可能であり、さまざまなクライアントで使用できる API の概要について説明します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The focus is on customer-facing application clients and eCommerce clients.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Retail Server business data and operations are available to any connected device through the OData Web API, across both employee (point of sale) scenarios and customer (online store) scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーのビジネス データと操作は、従業員 (販売時点) シナリオと顧客 (オンライン ストア) シナリオの両方で、OData Web API を通じてすべての接続デバイスで使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The embedded commerce runtime (CRT) enables a unified omni-channel platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">埋め込み <ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) は、統一されたオムニチャネル プラットフォームを可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The application programming interfaces (APIs) are stateless and can process requests from many channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション プログラミング インターフェイス (API) はステートレスであり、多くのチャンネルからの要求を処理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The APIs have a linear scale-out model (“brick” scale-out).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API には、直線的なスケール アウト モデル ("ブリック" スケール アウト) があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You use a composition pattern for plug-and-play customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグアンドプレイのカスタマイズに対して、合成パターンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The APIs are built on the .NET stack by using C<ph id="ph1">\#</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API は、C<ph id="ph1">\#</ph> を使用して .NET スタックに組み込まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Roles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Every request to Retail Server (via retail proxy) operates under three main roles:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー (Retail プロキシ経由) へのすべての要求リクエストでは、主に 3 つの役割を果たします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>CommerceRole.Employee</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRole.Employee</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>CommerceRole.Anonymous</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRole.Anonymous</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>CommerceRole.Customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRole.Customer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The Anonymous and Customer roles apply to eCommerce (customer/consumer) scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">匿名および顧客ロールは、電子商取引 (顧客/消費者) シナリオに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The Anonymous role is used for requests that represent an eCommerce customer who hasn't signed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">匿名ロールは、サインインしていない電子商取引顧客を表す要求に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The Customer role is used for requests that represent an eCommerce customer who has been authenticated and has signed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客ロールは、認証済みでサインインしている電子商取引顧客を表す要求に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>A role filter is applied to every API that is exposed in Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロール フィルターは、Retail サーバーで公開されているすべての API に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For eCommerce scenarios, you can use only APIs that have either CommerceRole.Anonymous or CommerceRole.Customer associated with them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">eCommerce シナリオでは、関連する CommerceRole.Anonymous または CommerceRole.Customer のいずれかを持つ API のみを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>By default, Anonymous access is not enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、匿名アクセスは有効ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>To enable Anonymous access for your environment, contact <bpt id="p1">[</bpt>Support<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-support)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境の匿名アクセスを有効にするには、<bpt id="p1">[</bpt>サポート<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-support)</ept>に問い合わせてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>APIs that are available for an authenticated customer role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証された顧客ロールで有効な API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>CartManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CartManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Task<ph id="ph1">&amp;lt;</ph>SalesOrder<ph id="ph2">&amp;gt;</ph> CartManager.Checkout(String id, String receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, String receiptNumberSequence, IEnumerable<ph id="ph3">&amp;lt;</ph>CartTenderLine<ph id="ph4">&amp;gt;</ph> cartTenderLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>SalesOrder<ph id="ph2">&amp;gt;</ph> CartManager.Checkout(String id, String receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, String receiptNumberSequence, IEnumerable<ph id="ph3">&amp;lt;</ph>CartTenderLine<ph id="ph4">&amp;gt;</ph> cartTenderLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Copy(String id, Int32 targetCartType)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Copy(String id, Int32 targetCartType)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Task<ph id="ph1">&amp;lt;</ph>CartDeliveryPreferences<ph id="ph2">&amp;gt;</ph> CartManager.GetDeliveryPreferences(String id)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CartDeliveryPreferences<ph id="ph2">&amp;gt;</ph> CartManager.GetDeliveryPreferences(String id)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesLineDeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetLineDeliveryOptions(String id, IEnumerable<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> cartLineIds, Address shippingAddress, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesLineDeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetLineDeliveryOptions(String id, IEnumerable<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> cartLineIds, Address shippingAddress, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetDeliveryOptions(String id, Address shippingAddress, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetDeliveryOptions(String id, Address shippingAddress, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateLineDeliverySpecifications(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>LineDeliverySpecification<ph id="ph4">&amp;gt;</ph> lineDeliverySpecifications)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateLineDeliverySpecifications(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>LineDeliverySpecification<ph id="ph4">&amp;gt;</ph> lineDeliverySpecifications)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateDeliverySpecification(String id, DeliverySpecification deliverySpecification)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateDeliverySpecification(String id, DeliverySpecification deliverySpecification)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetProductsInCart(String id, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetProductsInCart(String id, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Task<ph id="ph1">&amp;lt;</ph>CartPromotions<ph id="ph2">&amp;gt;</ph> CartManager.GetPromotions(String id)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CartPromotions<ph id="ph2">&amp;gt;</ph> CartManager.GetPromotions(String id)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddDiscountCode(String id, String discountCode)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddDiscountCode(String id, String discountCode)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveDiscountCodes(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> discountCodes)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveDiscountCodes(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> discountCodes)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> cartLineIds)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> cartLineIds)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Cart<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.Search(CartSearchCriteria cartSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Cart<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.Search(CartSearchCriteria cartSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptPoint<ph id="ph2">&amp;gt;</ph> CartManager.GetCardPaymentAcceptPoint(String id, CardPaymentAcceptSettings cardPaymentAcceptSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptPoint<ph id="ph2">&amp;gt;</ph> CartManager.GetCardPaymentAcceptPoint(String id, CardPaymentAcceptSettings cardPaymentAcceptSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptResult<ph id="ph2">&amp;gt;</ph> CartManager.RetrieveCardPaymentAcceptResult(String resultAccessCode)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptResult<ph id="ph2">&amp;gt;</ph> CartManager.RetrieveCardPaymentAcceptResult(String resultAccessCode)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Read(String id, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Read(String id, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Update(Cart entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Update(Cart entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Create(Cart entity)CartsController.GetEntityByKey()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Create(Cart entity)CartsController.GetEntityByKey()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>ProductCatalogManager and CategoryManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductCatalogManager および CategoryManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductCatalog<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductCatalogManager.GetCatalogs(Int64 channelId, Boolean activeOnly, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductCatalog<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductCatalogManager.GetCatalogs(Int64 channelId, Boolean activeOnly, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.GetCategories(Int64 channelId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.GetCategories(Int64 channelId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>CommerceList and CommerceListManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceList および CommerceListManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CommerceList<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CommerceListManager.GetByCustomer(String customerId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CommerceList<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CommerceListManager.GetByCustomer(String customerId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.AddLines(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.AddLines(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.UpdateLines(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.UpdateLines(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.RemoveLines(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.RemoveLines(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.MoveLines(IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines, Int64 destinationId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.MoveLines(IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines, Int64 destinationId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.CopyLines(IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines, Int64 destinationId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.CopyLines(IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListLine<ph id="ph4">&amp;gt;</ph> commerceListLines, Int64 destinationId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.AddContributors(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListContributor<ph id="ph4">&amp;gt;</ph> commerceListContributors)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.AddContributors(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListContributor<ph id="ph4">&amp;gt;</ph> commerceListContributors)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.RemoveContributors(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListContributor<ph id="ph4">&amp;gt;</ph> commerceListContributors)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.RemoveContributors(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListContributor<ph id="ph4">&amp;gt;</ph> commerceListContributors)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.CreateInvitations(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListInvitation<ph id="ph4">&amp;gt;</ph> commerceListInvitations)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.CreateInvitations(Int64 id, IEnumerable<ph id="ph3">&amp;lt;</ph>CommerceListInvitation<ph id="ph4">&amp;gt;</ph> commerceListInvitations)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Task CommerceListManager.AcceptInvitation(String invitationToken, String customerId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク CommerceListManager.AcceptInvitation(String invitationToken、String customerId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.Read(Int64 id, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.Read(Int64 id, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.Create(CommerceList entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.Create(CommerceList entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.Update(CommerceList entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CommerceList<ph id="ph2">&amp;gt;</ph> CommerceListManager.Update(CommerceList entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Task CommerceListManager.Delete(CommerceList entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク CommerceListManager.Delete (CommerceList エンティティ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>CustomerManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerManager APIs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesOrder<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CustomerManager.GetOrderHistory(String accountNumber, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesOrder<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CustomerManager.GetOrderHistory(String accountNumber, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>PurchaseHistory<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CustomerManager.GetPurchaseHistory(String accountNumber, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>PurchaseHistory<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CustomerManager.GetPurchaseHistory(String accountNumber, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Task<ph id="ph1">&amp;lt;</ph>Customer<ph id="ph2">&amp;gt;</ph> CustomerManager.Read(String accountNumber, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Customer<ph id="ph2">&amp;gt;</ph> CustomerManager.Read(String accountNumber, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Task<ph id="ph1">&amp;lt;</ph>Customer<ph id="ph2">&amp;gt;</ph> CustomerManager.Update(Customer entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Customer<ph id="ph2">&amp;gt;</ph> CustomerManager.Update(Customer entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>StoreOperationsManager and OrgUnitManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StoreOperationsManager および OrgUnitManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CardTypeInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCardTypes(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CardTypeInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCardTypes(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>String<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetSupportedPaymentCardTypes(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>String<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetSupportedPaymentCardTypes(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CountryRegionInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCountryRegionsByLanguageId(String languageId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CountryRegionInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCountryRegionsByLanguageId(String languageId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetDeliveryOptions(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetDeliveryOptions(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Task<ph id="ph1">&amp;lt;</ph>GiftCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.GetGiftCard(String giftCardId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>GiftCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.GetGiftCard(String giftCardId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Task<ph id="ph1">&amp;lt;</ph>LinkToExistingCustomerResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.InitiateLinkToExistingCustomer(String email, String activationToken, String emailTemplateId, IEnumerable<ph id="ph3">&amp;lt;</ph>NameValuePair<ph id="ph4">&amp;gt;</ph> emailProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>LinkToExistingCustomerResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.InitiateLinkToExistingCustomer(String email, String activationToken, String emailTemplateId, IEnumerable<ph id="ph3">&amp;lt;</ph>NameValuePair<ph id="ph4">&amp;gt;</ph> emailProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Task StoreOperationsManager.UnlinkFromExistingCustomer()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク StoreOperationsManager.UnlinkFromExistingCustomer()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Task<ph id="ph1">&amp;lt;</ph>LoyaltyCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.IssueLoyaltyCard(LoyaltyCard loyaltyCard)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>LoyaltyCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.IssueLoyaltyCard(LoyaltyCard loyaltyCard)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Task<ph id="ph1">&amp;lt;</ph>LoyaltyCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.GetLoyaltyCard(String cardNumber)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>LoyaltyCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.GetLoyaltyCard(String cardNumber)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>LoyaltyCard<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCustomerLoyaltyCards(String accountNumber, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>LoyaltyCard<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCustomerLoyaltyCards(String accountNumber, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>LoyaltyCardTransaction<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetLoyaltyCardTransactions(String cardNumber, String rewardPointId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>LoyaltyCardTransaction<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetLoyaltyCardTransactions(String cardNumber, String rewardPointId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>StateProvinceInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetStateProvinces(String countryRegionId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>StateProvinceInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetStateProvinces(String countryRegionId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>TenderType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetTenderTypes(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>TenderType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetTenderTypes(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetOrgUnitLocationsByArea(SearchArea searchArea, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetOrgUnitLocationsByArea(SearchArea searchArea, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventory(String itemId, String variantId, String barcode, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventory(String itemId, String variantId, String barcode, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventoryNearby(IEnumerable<ph id="ph5">&amp;lt;</ph>ItemUnit<ph id="ph6">&amp;gt;</ph> itemIds, SearchArea searchArea, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventoryNearby(IEnumerable<ph id="ph5">&amp;lt;</ph>ItemUnit<ph id="ph6">&amp;gt;</ph> itemIds, SearchArea searchArea, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Task<ph id="ph1">&amp;lt;</ph>TillLayout<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetTillLayout()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>TillLayout<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetTillLayout()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Task<ph id="ph1">&amp;lt;</ph>ChannelConfiguration<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetOrgUnitConfiguration()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>ChannelConfiguration<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetOrgUnitConfiguration()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.Search(SearchStoreCriteria storeSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.Search(SearchStoreCriteria storeSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Task<ph id="ph1">&amp;lt;</ph>OrgUnit<ph id="ph2">&amp;gt;</ph> OrgUnitManager.Read(String orgUnitNumber, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>OrgUnit<ph id="ph2">&amp;gt;</ph> OrgUnitManager.Read(String orgUnitNumber, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>ProductManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.Search(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.Search(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Task<ph id="ph1">&amp;lt;</ph>SimpleProduct<ph id="ph2">&amp;gt;</ph> ProductManager.GetById(Int64 recordId, Int64 channelId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>SimpleProduct<ph id="ph2">&amp;gt;</ph> ProductManager.GetById(Int64 recordId, Int64 channelId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByText(Int64 channelId, Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByText(Int64 channelId, Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByCategory(Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByCategory(Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByText(Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByText(Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByCategory(Int64 catalogId, Int64 categoryId, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByCategory(Int64 catalogId, Int64 categoryId, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByText(Int64 catalogId, String searchText, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByText(Int64 catalogId, String searchText, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByText(Int64 channelId, Int64 catalogId, String searchText, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByText(Int64 channelId, Int64 catalogId, String searchText, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductDimensionValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDimensionValues(Int64 recordId, Int64 channelId, Int32 dimension, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductDimensionValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDimensionValues(Int64 recordId, Int64 channelId, Int32 dimension, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByDimensionValues(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByDimensionValues(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByComponentsInSlots(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ComponentInSlotRelation<ph id="ph6">&amp;gt;</ph> matchingSlotToComponentRelationship, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByComponentsInSlots(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ComponentInSlotRelation<ph id="ph6">&amp;gt;</ph> matchingSlotToComponentRelationship, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDefaultComponents(Int64 recordId, Int64 channelId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDefaultComponents(Int64 recordId, Int64 channelId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetSlotComponents(Int64 recordId, Int64 channelId, Int64 slotId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetSlotComponents(Int64 recordId, Int64 channelId, Int64 slotId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>AttributeValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetAttributeValues(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>AttributeValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetAttributeValues(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRelationType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelationTypes(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRelationType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelationTypes(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelatedProducts(Int64 recordId, Int64 channelId, Int64 catalogId, Int64 relationTypeId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelatedProducts(Int64 recordId, Int64 channelId, Int64 catalogId, Int64 relationTypeId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefiners(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefiners(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductAvailableQuantity<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetProductAvailabilities(IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> itemIds, Int64 channelId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductAvailableQuantity<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetProductAvailabilities(IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> itemIds, Int64 channelId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductPrice<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetActivePrices(ProjectionDomain projectDomain, IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> productIds, DateTimeOffset activeDate, String customerId, IEnumerable<ph id="ph7">&amp;lt;</ph>AffiliationLoyaltyTier<ph id="ph8">&amp;gt;</ph> affiliationLoyaltyTiers, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductPrice<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetActivePrices(ProjectionDomain projectDomain, IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> productIds, DateTimeOffset activeDate, String customerId, IEnumerable<ph id="ph7">&amp;lt;</ph>AffiliationLoyaltyTier<ph id="ph8">&amp;gt;</ph> affiliationLoyaltyTiers, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaLocations(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaLocations(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaBlob<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaBlobs(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaBlob<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaBlobs(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>SalesOrderManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SalesOrderManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesOrder<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> SalesOrderManager.Search(SalesOrderSearchCriteria salesOrderSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesOrder<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> SalesOrderManager.Search(SalesOrderSearchCriteria salesOrderSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>APIs that are available for an anonymous role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">匿名ロールで有効な API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>CartManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CartManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Task<ph id="ph1">&amp;lt;</ph>SalesOrder<ph id="ph2">&amp;gt;</ph> CartManager.Checkout(String id, String receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, String receiptNumberSequence, IEnumerable<ph id="ph3">&amp;lt;</ph>CartTenderLine<ph id="ph4">&amp;gt;</ph> cartTenderLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>SalesOrder<ph id="ph2">&amp;gt;</ph> CartManager.Checkout(String id, String receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, String receiptNumberSequence, IEnumerable<ph id="ph3">&amp;lt;</ph>CartTenderLine<ph id="ph4">&amp;gt;</ph> cartTenderLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Copy(String id, Int32 targetCartType)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Copy(String id, Int32 targetCartType)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>CartLine<ph id="ph4">&amp;gt;</ph> cartLines)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Task<ph id="ph1">&amp;lt;</ph>CartDeliveryPreferences<ph id="ph2">&amp;gt;</ph> CartManager.GetDeliveryPreferences(String id)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CartDeliveryPreferences<ph id="ph2">&amp;gt;</ph> CartManager.GetDeliveryPreferences(String id)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesLineDeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetLineDeliveryOptions(String id, IEnumerable<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> cartLineIds, Address shippingAddress, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SalesLineDeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetLineDeliveryOptions(String id, IEnumerable<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> cartLineIds, Address shippingAddress, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetDeliveryOptions(String id, Address shippingAddress, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetDeliveryOptions(String id, Address shippingAddress, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateLineDeliverySpecifications(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>LineDeliverySpecification<ph id="ph4">&amp;gt;</ph> lineDeliverySpecifications)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateLineDeliverySpecifications(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>LineDeliverySpecification<ph id="ph4">&amp;gt;</ph> lineDeliverySpecifications)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateDeliverySpecification(String id, DeliverySpecification deliverySpecification)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.UpdateDeliverySpecification(String id, DeliverySpecification deliverySpecification)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetProductsInCart(String id, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Product<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CartManager.GetProductsInCart(String id, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Task<ph id="ph1">&amp;lt;</ph>CartPromotions<ph id="ph2">&amp;gt;</ph> CartManager.GetPromotions(String id)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CartPromotions<ph id="ph2">&amp;gt;</ph> CartManager.GetPromotions(String id)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddDiscountCode(String id, String discountCode)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.AddDiscountCode(String id, String discountCode)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveDiscountCodes(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> discountCodes)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveDiscountCodes(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> discountCodes)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> cartLineIds)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.RemoveCartLines(String id, IEnumerable<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> cartLineIds)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptPoint<ph id="ph2">&amp;gt;</ph> CartManager.GetCardPaymentAcceptPoint(String id, CardPaymentAcceptSettings cardPaymentAcceptSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptPoint<ph id="ph2">&amp;gt;</ph> CartManager.GetCardPaymentAcceptPoint(String id, CardPaymentAcceptSettings cardPaymentAcceptSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptResult<ph id="ph2">&amp;gt;</ph> CartManager.RetrieveCardPaymentAcceptResult(String resultAccessCode)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>CardPaymentAcceptResult<ph id="ph2">&amp;gt;</ph> CartManager.RetrieveCardPaymentAcceptResult(String resultAccessCode)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Read(String id, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Read(String id, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Update(Cart entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Update(Cart entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Create(Cart entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Cart<ph id="ph2">&amp;gt;</ph> CartManager.Create(Cart entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>CatalogManager and ProductCatalogManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CatalogManager および ProductCatalogManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductCatalog<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductCatalogManager.GetCatalogs(Int64 channelId, Boolean activeOnly, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductCatalog<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductCatalogManager.GetCatalogs(Int64 channelId, Boolean activeOnly, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.GetCategories(Int64 channelId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.GetCategories(Int64 channelId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.GetChildren(Int64 channelId, Int64 categoryId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>Category<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> CategoryManager.GetChildren(Int64 channelId, Int64 categoryId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>StoreOperationsManager and OrgUnitManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StoreOperationsManager および OrgUnitManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CardTypeInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCardTypes(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CardTypeInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCardTypes(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>String<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetSupportedPaymentCardTypes(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>String<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetSupportedPaymentCardTypes(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CountryRegionInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCountryRegionsByLanguageId(String languageId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>CountryRegionInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetCountryRegionsByLanguageId(String languageId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetDeliveryOptions(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>DeliveryOption<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetDeliveryOptions(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Task<ph id="ph1">&amp;lt;</ph>GiftCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.GetGiftCard(String giftCardId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>GiftCard<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.GetGiftCard(String giftCardId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Task<ph id="ph1">&amp;lt;</ph>LinkToExistingCustomerResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.InitiateLinkToExistingCustomer(String email, String activationToken, String emailTemplateId, IEnumerable<ph id="ph3">&amp;lt;</ph>NameValuePair<ph id="ph4">&amp;gt;</ph> emailProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>LinkToExistingCustomerResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.InitiateLinkToExistingCustomer(String email, String activationToken, String emailTemplateId, IEnumerable<ph id="ph3">&amp;lt;</ph>NameValuePair<ph id="ph4">&amp;gt;</ph> emailProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Task<ph id="ph1">&amp;lt;</ph>LinkToExistingCustomerResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.FinalizeLinkToExistingCustomer(String email, String activationToken)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>LinkToExistingCustomerResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.FinalizeLinkToExistingCustomer(String email, String activationToken)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Task<ph id="ph1">&amp;lt;</ph>ValidateHardwareStationTokenResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.ValidateHardwareStationToken(String deviceNumber, String hardwareStationToken)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>ValidateHardwareStationTokenResult<ph id="ph2">&amp;gt;</ph> StoreOperationsManager.ValidateHardwareStationToken(String deviceNumber, String hardwareStationToken)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>StateProvinceInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetStateProvinces(String countryRegionId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>StateProvinceInfo<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetStateProvinces(String countryRegionId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>TenderType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetTenderTypes(QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>TenderType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> StoreOperationsManager.GetTenderTypes(QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.ReadAll(QueryResultSettings queryResultSettings, ICollection<ph id="ph5">&amp;lt;</ph>String<ph id="ph6">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetOrgUnitLocationsByArea(SearchArea searchArea, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetOrgUnitLocationsByArea(SearchArea searchArea, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventory(String itemId, String variantId, String barcode, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventory(String itemId, String variantId, String barcode, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventoryNearby(IEnumerable<ph id="ph5">&amp;lt;</ph>ItemUnit<ph id="ph6">&amp;gt;</ph> itemIds, SearchArea searchArea, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnitAvailability<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.GetAvailableInventoryNearby(IEnumerable<ph id="ph5">&amp;lt;</ph>ItemUnit<ph id="ph6">&amp;gt;</ph> itemIds, SearchArea searchArea, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Task<ph id="ph1">&amp;lt;</ph>TillLayout<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetTillLayout()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>TillLayout<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetTillLayout()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Task<ph id="ph1">&amp;lt;</ph>ChannelConfiguration<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetOrgUnitConfiguration()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>ChannelConfiguration<ph id="ph2">&amp;gt;</ph> OrgUnitManager.GetOrgUnitConfiguration()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.Search(SearchStoreCriteria storeSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>OrgUnit<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> OrgUnitManager.Search(SearchStoreCriteria storeSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Task<ph id="ph1">&amp;lt;</ph>OrgUnit<ph id="ph2">&amp;gt;</ph> OrgUnitManager.Read(String orgUnitNumber, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>OrgUnit<ph id="ph2">&amp;gt;</ph> OrgUnitManager.Read(String orgUnitNumber, ICollection<ph id="ph3">&amp;lt;</ph>String<ph id="ph4">&amp;gt;</ph> expandProperties)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>CustomerManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerManager APIs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Task<ph id="ph1">&amp;lt;</ph>Customer<ph id="ph2">&amp;gt;</ph> CustomerManager.Create(Customer entity)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>Customer<ph id="ph2">&amp;gt;</ph> CustomerManager.Create(Customer entity)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>ProductManager APIs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductManager API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByText(Int64 channelId, Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.SearchByText(Int64 channelId, Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByCategory(Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByCategory(Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByText(Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinersByText(Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByCategory(Int64 catalogId, Int64 categoryId, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByCategory(Int64 catalogId, Int64 categoryId, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByText(Int64 catalogId, String searchText, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefinerValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefinerValuesByText(Int64 catalogId, String searchText, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByText(Int64 channelId, Int64 catalogId, String searchText, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.RefineSearchByText(Int64 channelId, Int64 catalogId, String searchText, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductRefinerValue<ph id="ph6">&amp;gt;</ph> refinementCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductDimensionValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDimensionValues(Int64 recordId, Int64 channelId, Int32 dimension, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductDimensionValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDimensionValues(Int64 recordId, Int64 channelId, Int32 dimension, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByDimensionValues(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByDimensionValues(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ProductDimensionValue<ph id="ph6">&amp;gt;</ph> matchingDimensionValues, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByComponentsInSlots(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ComponentInSlotRelation<ph id="ph6">&amp;gt;</ph> matchingSlotToComponentRelationship, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>SimpleProduct<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetVariantsByComponentsInSlots(Int64 recordId, Int64 channelId, IEnumerable<ph id="ph5">&amp;lt;</ph>ComponentInSlotRelation<ph id="ph6">&amp;gt;</ph> matchingSlotToComponentRelationship, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDefaultComponents(Int64 recordId, Int64 channelId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetDefaultComponents(Int64 recordId, Int64 channelId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetSlotComponents(Int64 recordId, Int64 channelId, Int64 slotId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductComponent<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetSlotComponents(Int64 recordId, Int64 channelId, Int64 slotId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>AttributeValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetAttributeValues(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>AttributeValue<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetAttributeValues(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRelationType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelationTypes(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRelationType<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelationTypes(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelatedProducts(Int64 recordId, Int64 channelId, Int64 catalogId, Int64 relationTypeId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductSearchResult<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRelatedProducts(Int64 recordId, Int64 channelId, Int64 catalogId, Int64 relationTypeId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefiners(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductRefiner<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetRefiners(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductAvailableQuantity<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetProductAvailabilities(IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> itemIds, Int64 channelId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductAvailableQuantity<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetProductAvailabilities(IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> itemIds, Int64 channelId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductPrice<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetActivePrices(ProjectionDomain projectDomain, IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> productIds, DateTimeOffset activeDate, String customerId, IEnumerable<ph id="ph7">&amp;lt;</ph>AffiliationLoyaltyTier<ph id="ph8">&amp;gt;</ph> affiliationLoyaltyTiers, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>ProductPrice<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetActivePrices(ProjectionDomain projectDomain, IEnumerable<ph id="ph5">&amp;lt;</ph>Int64<ph id="ph6">&amp;gt;</ph> productIds, DateTimeOffset activeDate, String customerId, IEnumerable<ph id="ph7">&amp;lt;</ph>AffiliationLoyaltyTier<ph id="ph8">&amp;gt;</ph> affiliationLoyaltyTiers, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaLocations(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaLocation<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaLocations(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaBlob<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaBlobs(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Task<ph id="ph1">&amp;lt;</ph>PagedResult<ph id="ph2">&amp;lt;</ph>MediaBlob<ph id="ph3">&amp;gt;</ph><ph id="ph4">&amp;gt;</ph> ProductManager.GetMediaBlobs(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>