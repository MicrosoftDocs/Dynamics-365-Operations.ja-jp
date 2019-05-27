---
title: Retail サーバーの顧客およびコンシューマー API
description: この記事では、さまざまな役割で利用可能であり、さまざまなクライアントで使用できる API の概要について説明します 中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 84383
ms.assetid: c60de19f-06e5-4e57-8956-7fd17c460e52
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 825c5770a71ab2126ce48a6987c209915956730e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537523"
---
# <a name="retail-server-customer-and-consumer-apis"></a>Retail サーバーの顧客およびコンシューマー API

[!include [banner](../includes/banner.md)]

この記事では、さまざまな役割で利用可能であり、さまざまなクライアントで使用できる API の概要について説明します 中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。

<a name="overview"></a>概要
--------

-   Retail サーバーのビジネス データと操作は、従業員 (販売時点) シナリオと顧客 (オンライン ストア) シナリオの両方で、OData Web API を通じてすべての接続デバイスで使用できます。
-   埋め込み Commerce Runtime (CRT) は、統一されたオムニチャネル プラットフォームを可能にします。
-   アプリケーション プログラミング インターフェイス (API) はステートレスであり、多くのチャンネルからの要求を処理できます。
-   API には、直線的なスケール アウト モデル ("ブリック" スケール アウト) があります。
-   プラグアンドプレイのカスタマイズに対して、合成パターンを使用します。
-   API は、C\# を使用して .NET スタックに組み込まれています。

## <a name="roles"></a>ロール
Retail サーバー (Retail プロキシ経由) へのすべての要求リクエストでは、主に 3 つの役割を果たします。

-   CommerceRole.Employee
-   CommerceRole.Anonymous
-   CommerceRole.Customer

匿名および顧客ロールは、電子商取引 (顧客/消費者) シナリオに適用されます。 匿名ロールは、サインインしていない電子商取引顧客を表す要求に使用されます。 顧客ロールは、認証済みでサインインしている電子商取引顧客を表す要求に使用されます。 ロール フィルターは、Retail サーバーで公開されているすべての API に適用されます。 eCommerce シナリオでは、関連する CommerceRole.Anonymous または CommerceRole.Customer のいずれかを持つ API のみを使用することができます。

> [!NOTE]
> 既定では、匿名アクセスは有効ではありません。 環境の匿名アクセスを有効にするには、[サポート](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-support)に問い合わせてください。

### <a name="apis-that-are-available-for-an-authenticated-customer-role"></a>認証された顧客ロールで有効な API

#### <a name="cartmanager-apis"></a>CartManager API

-   Task&lt;SalesOrder&gt; CartManager.Checkout(String id, String receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, String receiptNumberSequence, IEnumerable&lt;CartTenderLine&gt; cartTenderLines)
-   Task&lt;Cart&gt; CartManager.Copy(String id, Int32 targetCartType)
-   Task&lt;Cart&gt; CartManager.AddCartLines(String id, IEnumerable&lt;CartLine&gt; cartLines)
-   Task&lt;Cart&gt; CartManager.UpdateCartLines(String id, IEnumerable&lt;CartLine&gt; cartLines)
-   Task&lt;CartDeliveryPreferences&gt; CartManager.GetDeliveryPreferences(String id)
-   Task&lt;PagedResult&lt;SalesLineDeliveryOption&gt;&gt; CartManager.GetLineDeliveryOptions(String id, IEnumerable&lt;String&gt; cartLineIds, Address shippingAddress, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;DeliveryOption&gt;&gt; CartManager.GetDeliveryOptions(String id, Address shippingAddress, QueryResultSettings queryResultSettings)
-   Task&lt;Cart&gt; CartManager.UpdateLineDeliverySpecifications(String id, IEnumerable&lt;LineDeliverySpecification&gt; lineDeliverySpecifications)
-   Task&lt;Cart&gt; CartManager.UpdateDeliverySpecification(String id, DeliverySpecification deliverySpecification)
-   Task&lt;PagedResult&lt;Product&gt;&gt; CartManager.GetProductsInCart(String id, QueryResultSettings queryResultSettings)
-   Task&lt;CartPromotions&gt; CartManager.GetPromotions(String id)
-   Task&lt;Cart&gt; CartManager.AddDiscountCode(String id, String discountCode)
-   Task&lt;Cart&gt; CartManager.RemoveDiscountCodes(String id, IEnumerable&lt;String&gt; discountCodes)
-   Task&lt;Cart&gt; CartManager.RemoveCartLines(String id, IEnumerable&lt;String&gt; cartLineIds)
-   Task&lt;PagedResult&lt;Cart&gt;&gt; CartManager.Search(CartSearchCriteria cartSearchCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;CardPaymentAcceptPoint&gt; CartManager.GetCardPaymentAcceptPoint(String id, CardPaymentAcceptSettings cardPaymentAcceptSettings)
-   Task&lt;CardPaymentAcceptResult&gt; CartManager.RetrieveCardPaymentAcceptResult(String resultAccessCode)
-   Task&lt;Cart&gt; CartManager.Read(String id, ICollection&lt;String&gt; expandProperties)
-   Task&lt;Cart&gt; CartManager.Update(Cart entity)
-   Task&lt;Cart&gt; CartManager.Create(Cart entity)CartsController.GetEntityByKey()

#### <a name="productcatalogmanager-and-categorymanager-apis"></a>ProductCatalogManager および CategoryManager API

-   Task&lt;PagedResult&lt;ProductCatalog&gt;&gt; ProductCatalogManager.GetCatalogs(Int64 channelId, Boolean activeOnly, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;Category&gt;&gt; CategoryManager.GetCategories(Int64 channelId, QueryResultSettings queryResultSettings)

#### <a name="commercelist-and-commercelistmanager-apis"></a>CommerceList および CommerceListManager API

-   Task&lt;PagedResult&lt;CommerceList&gt;&gt; CommerceListManager.GetByCustomer(String customerId, QueryResultSettings queryResultSettings)
-   Task&lt;CommerceList&gt; CommerceListManager.AddLines(Int64 id, IEnumerable&lt;CommerceListLine&gt; commerceListLines)
-   Task&lt;CommerceList&gt; CommerceListManager.UpdateLines(Int64 id, IEnumerable&lt;CommerceListLine&gt; commerceListLines)
-   Task&lt;CommerceList&gt; CommerceListManager.RemoveLines(Int64 id, IEnumerable&lt;CommerceListLine&gt; commerceListLines)
-   Task&lt;CommerceList&gt; CommerceListManager.MoveLines(IEnumerable&lt;CommerceListLine&gt; commerceListLines, Int64 destinationId)
-   Task&lt;CommerceList&gt; CommerceListManager.CopyLines(IEnumerable&lt;CommerceListLine&gt; commerceListLines, Int64 destinationId)
-   Task&lt;CommerceList&gt; CommerceListManager.AddContributors(Int64 id, IEnumerable&lt;CommerceListContributor&gt; commerceListContributors)
-   Task&lt;CommerceList&gt; CommerceListManager.RemoveContributors(Int64 id, IEnumerable&lt;CommerceListContributor&gt; commerceListContributors)
-   Task&lt;CommerceList&gt; CommerceListManager.CreateInvitations(Int64 id, IEnumerable&lt;CommerceListInvitation&gt; commerceListInvitations)
-   タスク CommerceListManager.AcceptInvitation(String invitationToken、String customerId)
-   Task&lt;CommerceList&gt; CommerceListManager.Read(Int64 id, ICollection&lt;String&gt; expandProperties)
-   Task&lt;CommerceList&gt; CommerceListManager.Create(CommerceList entity)
-   Task&lt;CommerceList&gt; CommerceListManager.Update(CommerceList entity)
-   タスク CommerceListManager.Delete (CommerceList エンティティ)

#### <a name="customermanager-apis"></a>CustomerManager APIs

-   Task&lt;PagedResult&lt;SalesOrder&gt;&gt; CustomerManager.GetOrderHistory(String accountNumber, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;PurchaseHistory&gt;&gt; CustomerManager.GetPurchaseHistory(String accountNumber, QueryResultSettings queryResultSettings)
-   Task&lt;Customer&gt; CustomerManager.Read(String accountNumber, ICollection&lt;String&gt; expandProperties)
-   Task&lt;Customer&gt; CustomerManager.Update(Customer entity)

#### <a name="storeoperationsmanager-and-orgunitmanager-apis"></a>StoreOperationsManager および OrgUnitManager API

-   Task&lt;PagedResult&lt;CardTypeInfo&gt;&gt; StoreOperationsManager.GetCardTypes(QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;String&gt;&gt; StoreOperationsManager.GetSupportedPaymentCardTypes(QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;CountryRegionInfo&gt;&gt; StoreOperationsManager.GetCountryRegionsByLanguageId(String languageId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;DeliveryOption&gt;&gt; StoreOperationsManager.GetDeliveryOptions(QueryResultSettings queryResultSettings)
-   Task&lt;GiftCard&gt; StoreOperationsManager.GetGiftCard(String giftCardId)
-   Task&lt;LinkToExistingCustomerResult&gt; StoreOperationsManager.InitiateLinkToExistingCustomer(String email, String activationToken, String emailTemplateId, IEnumerable&lt;NameValuePair&gt; emailProperties)
-   タスク StoreOperationsManager.UnlinkFromExistingCustomer()
-   Task&lt;LoyaltyCard&gt; StoreOperationsManager.IssueLoyaltyCard(LoyaltyCard loyaltyCard)
-   Task&lt;LoyaltyCard&gt; StoreOperationsManager.GetLoyaltyCard(String cardNumber)
-   Task&lt;PagedResult&lt;LoyaltyCard&gt;&gt; StoreOperationsManager.GetCustomerLoyaltyCards(String accountNumber, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;LoyaltyCardTransaction&gt;&gt; StoreOperationsManager.GetLoyaltyCardTransactions(String cardNumber, String rewardPointId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;StateProvinceInfo&gt;&gt; StoreOperationsManager.GetStateProvinces(String countryRegionId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;TenderType&gt;&gt; StoreOperationsManager.GetTenderTypes(QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;OrgUnit&gt;&gt; OrgUnitManager.ReadAll(QueryResultSettings queryResultSettings, ICollection&lt;String&gt; expandProperties)
-   Task&lt;PagedResult&lt;OrgUnitLocation&gt;&gt; OrgUnitManager.GetOrgUnitLocationsByArea(SearchArea searchArea, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;OrgUnitAvailability&gt;&gt; OrgUnitManager.GetAvailableInventory(String itemId, String variantId, String barcode, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;OrgUnitAvailability&gt;&gt; OrgUnitManager.GetAvailableInventoryNearby(IEnumerable&lt;ItemUnit&gt; itemIds, SearchArea searchArea, QueryResultSettings queryResultSettings)
-   Task&lt;TillLayout&gt; OrgUnitManager.GetTillLayout()
-   Task&lt;ChannelConfiguration&gt; OrgUnitManager.GetOrgUnitConfiguration()
-   Task&lt;PagedResult&lt;OrgUnit&gt;&gt; OrgUnitManager.Search(SearchStoreCriteria storeSearchCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;OrgUnit&gt; OrgUnitManager.Read(String orgUnitNumber, ICollection&lt;String&gt; expandProperties)

#### <a name="productmanager-apis"></a>ProductManager API

-   Task&lt;PagedResult&lt;Product&gt;&gt; ProductManager.ReadAll(QueryResultSettings queryResultSettings, ICollection&lt;String&gt; expandProperties)
-   Task&lt;PagedResult&lt;Product&gt;&gt; ProductManager.Search(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;SimpleProduct&gt; ProductManager.GetById(Int64 recordId, Int64 channelId)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.SearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.SearchByText(Int64 channelId, Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefiner&gt;&gt; ProductManager.GetRefinersByCategory(Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefiner&gt;&gt; ProductManager.GetRefinersByText(Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefinerValue&gt;&gt; ProductManager.GetRefinerValuesByCategory(Int64 catalogId, Int64 categoryId, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefinerValue&gt;&gt; ProductManager.GetRefinerValuesByText(Int64 catalogId, String searchText, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.RefineSearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, IEnumerable&lt;ProductRefinerValue&gt; refinementCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.RefineSearchByText(Int64 channelId, Int64 catalogId, String searchText, IEnumerable&lt;ProductRefinerValue&gt; refinementCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductDimensionValue&gt;&gt; ProductManager.GetDimensionValues(Int64 recordId, Int64 channelId, Int32 dimension, IEnumerable&lt;ProductDimensionValue&gt; matchingDimensionValues, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;SimpleProduct&gt;&gt; ProductManager.GetVariantsByDimensionValues(Int64 recordId, Int64 channelId, IEnumerable&lt;ProductDimensionValue&gt; matchingDimensionValues, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;SimpleProduct&gt;&gt; ProductManager.GetVariantsByComponentsInSlots(Int64 recordId, Int64 channelId, IEnumerable&lt;ComponentInSlotRelation&gt; matchingSlotToComponentRelationship, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductComponent&gt;&gt; ProductManager.GetDefaultComponents(Int64 recordId, Int64 channelId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductComponent&gt;&gt; ProductManager.GetSlotComponents(Int64 recordId, Int64 channelId, Int64 slotId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;AttributeValue&gt;&gt; ProductManager.GetAttributeValues(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRelationType&gt;&gt; ProductManager.GetRelationTypes(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.GetRelatedProducts(Int64 recordId, Int64 channelId, Int64 catalogId, Int64 relationTypeId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefiner&gt;&gt; ProductManager.GetRefiners(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductAvailableQuantity&gt;&gt; ProductManager.GetProductAvailabilities(IEnumerable&lt;Int64&gt; itemIds, Int64 channelId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductPrice&gt;&gt; ProductManager.GetActivePrices(ProjectionDomain projectDomain, IEnumerable&lt;Int64&gt; productIds, DateTimeOffset activeDate, String customerId, IEnumerable&lt;AffiliationLoyaltyTier&gt; affiliationLoyaltyTiers, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;MediaLocation&gt;&gt; ProductManager.GetMediaLocations(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;MediaBlob&gt;&gt; ProductManager.GetMediaBlobs(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)

#### <a name="salesordermanager-apis"></a>SalesOrderManager API

-   Task&lt;PagedResult&lt;SalesOrder&gt;&gt; SalesOrderManager.Search(SalesOrderSearchCriteria salesOrderSearchCriteria, QueryResultSettings queryResultSettings)

### <a name="apis-that-are-available-for-an-anonymous-role"></a>匿名ロールで有効な API

#### <a name="cartmanager-apis"></a>CartManager API

-   Task&lt;SalesOrder&gt; CartManager.Checkout(String id, String receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, String receiptNumberSequence, IEnumerable&lt;CartTenderLine&gt; cartTenderLines)
-   Task&lt;Cart&gt; CartManager.Copy(String id, Int32 targetCartType)
-   Task&lt;Cart&gt; CartManager.AddCartLines(String id, IEnumerable&lt;CartLine&gt; cartLines)
-   Task&lt;Cart&gt; CartManager.UpdateCartLines(String id, IEnumerable&lt;CartLine&gt; cartLines)
-   Task&lt;CartDeliveryPreferences&gt; CartManager.GetDeliveryPreferences(String id)
-   Task&lt;PagedResult&lt;SalesLineDeliveryOption&gt;&gt; CartManager.GetLineDeliveryOptions(String id, IEnumerable&lt;String&gt; cartLineIds, Address shippingAddress, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;DeliveryOption&gt;&gt; CartManager.GetDeliveryOptions(String id, Address shippingAddress, QueryResultSettings queryResultSettings)
-   Task&lt;Cart&gt; CartManager.UpdateLineDeliverySpecifications(String id, IEnumerable&lt;LineDeliverySpecification&gt; lineDeliverySpecifications)
-   Task&lt;Cart&gt; CartManager.UpdateDeliverySpecification(String id, DeliverySpecification deliverySpecification)
-   Task&lt;PagedResult&lt;Product&gt;&gt; CartManager.GetProductsInCart(String id, QueryResultSettings queryResultSettings)
-   Task&lt;CartPromotions&gt; CartManager.GetPromotions(String id)
-   Task&lt;Cart&gt; CartManager.AddDiscountCode(String id, String discountCode)
-   Task&lt;Cart&gt; CartManager.RemoveDiscountCodes(String id, IEnumerable&lt;String&gt; discountCodes)
-   Task&lt;Cart&gt; CartManager.RemoveCartLines(String id, IEnumerable&lt;String&gt; cartLineIds)
-   Task&lt;CardPaymentAcceptPoint&gt; CartManager.GetCardPaymentAcceptPoint(String id, CardPaymentAcceptSettings cardPaymentAcceptSettings)
-   Task&lt;CardPaymentAcceptResult&gt; CartManager.RetrieveCardPaymentAcceptResult(String resultAccessCode)
-   Task&lt;Cart&gt; CartManager.Read(String id, ICollection&lt;String&gt; expandProperties)
-   Task&lt;Cart&gt; CartManager.Update(Cart entity)
-   Task&lt;Cart&gt; CartManager.Create(Cart entity)

#### <a name="catalogmanager-and-productcatalogmanager-apis"></a>CatalogManager および ProductCatalogManager API

-   Task&lt;PagedResult&lt;ProductCatalog&gt;&gt; ProductCatalogManager.GetCatalogs(Int64 channelId, Boolean activeOnly, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;Category&gt;&gt; CategoryManager.ReadAll(QueryResultSettings queryResultSettings, ICollection&lt;String&gt; expandProperties)
-   Task&lt;PagedResult&lt;Category&gt;&gt; CategoryManager.GetCategories(Int64 channelId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;Category&gt;&gt; CategoryManager.GetChildren(Int64 channelId, Int64 categoryId, QueryResultSettings queryResultSettings)

#### <a name="storeoperationsmanager-and-orgunitmanager-apis"></a>StoreOperationsManager および OrgUnitManager API

-   Task&lt;PagedResult&lt;CardTypeInfo&gt;&gt; StoreOperationsManager.GetCardTypes(QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;String&gt;&gt; StoreOperationsManager.GetSupportedPaymentCardTypes(QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;CountryRegionInfo&gt;&gt; StoreOperationsManager.GetCountryRegionsByLanguageId(String languageId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;DeliveryOption&gt;&gt; StoreOperationsManager.GetDeliveryOptions(QueryResultSettings queryResultSettings)
-   Task&lt;GiftCard&gt; StoreOperationsManager.GetGiftCard(String giftCardId)
-   Task&lt;LinkToExistingCustomerResult&gt; StoreOperationsManager.InitiateLinkToExistingCustomer(String email, String activationToken, String emailTemplateId, IEnumerable&lt;NameValuePair&gt; emailProperties)
-   Task&lt;LinkToExistingCustomerResult&gt; StoreOperationsManager.FinalizeLinkToExistingCustomer(String email, String activationToken)
-   Task&lt;ValidateHardwareStationTokenResult&gt; StoreOperationsManager.ValidateHardwareStationToken(String deviceNumber, String hardwareStationToken)
-   Task&lt;PagedResult&lt;StateProvinceInfo&gt;&gt; StoreOperationsManager.GetStateProvinces(String countryRegionId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;TenderType&gt;&gt; StoreOperationsManager.GetTenderTypes(QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;OrgUnit&gt;&gt; OrgUnitManager.ReadAll(QueryResultSettings queryResultSettings, ICollection&lt;String&gt; expandProperties)
-   Task&lt;PagedResult&lt;OrgUnitLocation&gt;&gt; OrgUnitManager.GetOrgUnitLocationsByArea(SearchArea searchArea, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;OrgUnitAvailability&gt;&gt; OrgUnitManager.GetAvailableInventory(String itemId, String variantId, String barcode, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;OrgUnitAvailability&gt;&gt; OrgUnitManager.GetAvailableInventoryNearby(IEnumerable&lt;ItemUnit&gt; itemIds, SearchArea searchArea, QueryResultSettings queryResultSettings)
-   Task&lt;TillLayout&gt; OrgUnitManager.GetTillLayout()
-   Task&lt;ChannelConfiguration&gt; OrgUnitManager.GetOrgUnitConfiguration()
-   Task&lt;PagedResult&lt;OrgUnit&gt;&gt; OrgUnitManager.Search(SearchStoreCriteria storeSearchCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;OrgUnit&gt; OrgUnitManager.Read(String orgUnitNumber, ICollection&lt;String&gt; expandProperties)

#### <a name="customermanager-apis"></a>CustomerManager APIs

-   Task&lt;Customer&gt; CustomerManager.Create(Customer entity)

#### <a name="productmanager-apis"></a>ProductManager API

-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.SearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.SearchByText(Int64 channelId, Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefiner&gt;&gt; ProductManager.GetRefinersByCategory(Int64 catalogId, Int64 categoryId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefiner&gt;&gt; ProductManager.GetRefinersByText(Int64 catalogId, String searchText, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefinerValue&gt;&gt; ProductManager.GetRefinerValuesByCategory(Int64 catalogId, Int64 categoryId, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefinerValue&gt;&gt; ProductManager.GetRefinerValuesByText(Int64 catalogId, String searchText, Int64 refinerId, Int32 refinerSourceValue, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.RefineSearchByCategory(Int64 channelId, Int64 catalogId, Int64 categoryId, IEnumerable&lt;ProductRefinerValue&gt; refinementCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.RefineSearchByText(Int64 channelId, Int64 catalogId, String searchText, IEnumerable&lt;ProductRefinerValue&gt; refinementCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductDimensionValue&gt;&gt; ProductManager.GetDimensionValues(Int64 recordId, Int64 channelId, Int32 dimension, IEnumerable&lt;ProductDimensionValue&gt; matchingDimensionValues, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;SimpleProduct&gt;&gt; ProductManager.GetVariantsByDimensionValues(Int64 recordId, Int64 channelId, IEnumerable&lt;ProductDimensionValue&gt; matchingDimensionValues, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;SimpleProduct&gt;&gt; ProductManager.GetVariantsByComponentsInSlots(Int64 recordId, Int64 channelId, IEnumerable&lt;ComponentInSlotRelation&gt; matchingSlotToComponentRelationship, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductComponent&gt;&gt; ProductManager.GetDefaultComponents(Int64 recordId, Int64 channelId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductComponent&gt;&gt; ProductManager.GetSlotComponents(Int64 recordId, Int64 channelId, Int64 slotId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;AttributeValue&gt;&gt; ProductManager.GetAttributeValues(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRelationType&gt;&gt; ProductManager.GetRelationTypes(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductSearchResult&gt;&gt; ProductManager.GetRelatedProducts(Int64 recordId, Int64 channelId, Int64 catalogId, Int64 relationTypeId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductRefiner&gt;&gt; ProductManager.GetRefiners(ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductAvailableQuantity&gt;&gt; ProductManager.GetProductAvailabilities(IEnumerable&lt;Int64&gt; itemIds, Int64 channelId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;ProductPrice&gt;&gt; ProductManager.GetActivePrices(ProjectionDomain projectDomain, IEnumerable&lt;Int64&gt; productIds, DateTimeOffset activeDate, String customerId, IEnumerable&lt;AffiliationLoyaltyTier&gt; affiliationLoyaltyTiers, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;MediaLocation&gt;&gt; ProductManager.GetMediaLocations(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)
-   Task&lt;PagedResult&lt;MediaBlob&gt;&gt; ProductManager.GetMediaBlobs(Int64 recordId, Int64 channelId, Int64 catalogId, QueryResultSettings queryResultSettings)




