---
title: Retail サーバーの顧客およびコンシューマー API
description: この記事では、さまざまな役割で利用可能であり、さまざまなクライアントで使用できる API の概要について説明します 中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。
author: mugunthanm
manager: AnnBe
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 84383
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 890b472950eab43f51a6f9ca216792d91a5df4da
ms.sourcegitcommit: 9712ff2a4eb6a436ca8c65aece2bcecdf8d61706
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703650"
---
# <a name="retail-server-customer-and-consumer-apis"></a>Retail サーバーの顧客およびコンシューマー API

[!include [banner](../includes/banner.md)]

この記事では、さまざまな役割で利用可能であり、さまざまなクライアントで使用できる API の概要について説明します 中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。

<a name="overview"></a>概要
--------

- Retail サーバーのビジネス データと操作は、従業員 (販売時点) シナリオと顧客 (オンライン ストア) シナリオの両方で、OData Web API を通じてすべての接続デバイスで使用できます。
- 埋め込み CRT は、統一されたオムニチャネル プラットフォームを可能にします。
- アプリケーション プログラミング インターフェイス (API) はステートレスであり、多くのチャンネルからの要求を処理できます。
- API には、直線的なスケール アウト モデル ("ブリック" スケール アウト) があります。
- プラグアンドプレイのカスタマイズに対して、合成パターンを使用します。
- API は、C\# を使用して .NET スタックに組み込まれています。

## <a name="roles"></a>ロール
Retail サーバー (Retail プロキシ経由) へのすべての要求リクエストでは、主にこれらの役割を果たします。

- CommerceRole.Employee
- CommerceRole.Anonymous
- CommerceRole.Customer
- CommerceRoleアプリケーション

匿名および顧客ロールは、電子商取引 (顧客/消費者) シナリオに適用されます。 匿名ロールは、サインインしていない電子商取引顧客を表す要求に使用されます。 顧客ロールは、認証済みでサインインしている電子商取引顧客を表す要求に使用されます。 ロール フィルターは、Retail サーバーで公開されているすべての API に適用されます。 eCommerce シナリオでは、関連する CommerceRole.Anonymous または CommerceRole.Customer のいずれかを持つ API のみを使用することができます。

> [!NOTE]
> 既定では、匿名アクセスは有効ではありません。 環境の匿名アクセスを有効にするには、[サポート](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-support)に問い合わせてください。


## <a name="customer-controller"></a>顧客のコントロール

| API | パラメーター | 戻り値 | 対応している商取引上の役割 | 説明                |
|-----|-----------|--------------|--------------------------|----------------------------|
| GetOrderShipmentsHistory    | accountNumber  string型、QueryResultSettings queryResultSettings | PageResult\<OrderShipments\>       | 従業員、顧客、アプリケーション | 顧客からの注文の出荷履歴を取得します。  |
| GetOrderHistory             | accountNumber  string型、QueryResultSettings queryResultSettings           | PageResult\<SalesOrder\>           | 従業員、顧客、アプリケーション | 一群の販売注文を返します。                           |
| 検索                      | CustomerSearchCriteria customerSearchCriteria, QueryResultSettings queryResultSettings    | PageResult\<GlobalCustomer\>       | 従業員、アプリケーション         | 顧客を検索します                                        |
| GetPurchaseHistory          | accountNumber  string型、QueryResultSettings queryResultSettings      | PageResult\<PurchaseHistory\>      | 従業員、顧客、アプリケーション | 顧客の購入履歴を取得します。                           |
| GetByAccountNumbers         | IEnumerable\<string型\> accountNumbers, searchLocationValue int型, QueryResultSettings queryResultSettings | IEnumerable\<Customer\>     | 従業員、顧客、アプリケーション | 顧客のアカウント番号一覧から顧客リストを取得します。     |
| GetCustomerSearchFields     | queryResultSettings    | IEnumerable\<CustomerSearchField\> | 従業員、顧客、アプリケーション | 本社の店舗セットが使用する顧客検索フィールドを取得します。 |
| SearchByFields              | 顧客エンティティ                                                                                            | PageResult\<GlobalCustomer\>       | 従業員、顧客、アプリケーション | 指定したフィールドで顧客を検索します。           |
| PostNonTransactionalActivityLoyaltyPoints | loyaltyCardNumber string型, channelId Long型, affiliationId Long型, activityTypeId string型                        | 無効                                   | 従業員、顧客、アプリケーション | 非トランザクション処理後のロイヤリティポイント                    |

## <a name="sales-order-controller"></a>販売注文のコントロール

| API                                                    | パラメーター              | 戻り値                   | 対応している商取引上の役割 | 説明     |
|-------------|-----------------------------------------------------------------------------------------|------------------------------|--------------------------|---------------------------------------------------------------------|
| GetReceipts                                            | id string型, ReceiptRetrievalCriteria receiptRetrievalCriteria, QueryResultSettings queryResultSettings                                              | PageResult\<Receipt\>      | 従業員                 | 印刷用のフォームタイプに基づいて一連のレシートを取得します。                                             |
| GetGiftReceipts                                        | id string型, IEnumerable\<decimal型\> salesLineNumbers, ReceiptRetrievalCriteria receiptRetrievalCriteria, QueryResultSettings queryResultSettings | PageResult\<Receipt\>      | 従業員                 | 贈答品の受領を取得します。                                                                                  |
| GetByReceiptId                                         | receiptId string型, orderStoreNumber string型, orderTerminalId string型, QueryResultSettings queryResultSettings                                         | PageResult\<SalesOrder\>   | 従業員                 | レシートIDから販売注文を取得します。                                                             |
| SearchSalesTransactionsBy- ReceiptId                     | receiptId string型, QueryResultSettings queryResultSettings                                                                                          | PageResult\<SalesOrder\>   | 従業員                 | レシートIDから販売取引を取得します。                                                      |
| 検索                                                 | SalesOrderSearchCriteria salesOrderSearchCriteria, QueryResultSettings queryResultSettings                                                         | PageResult\<SalesOrder\>   | 従業員、顧客        | 指定された検索条件に一致する注文を検索します。                                              |
| SearchOrders                                           | OrderSearchCriteria orderSearchCriteria, QueryResultSettings queryResultSettings                                                                   | PageResult\<SalesOrder\>   | 従業員、顧客        | 指定された検索条件に一致する注文を検索します。                                                 |
| GetInvoicesBySalesId                                   | salesId string型, QueryResultSettings queryResultSettings                                                                                            | PageResult\<SalesInvoice\> | 従業員                 | 渡された販売IDに関連付けられている売上請求書を取得します。                                      |
| GetOrderInvoices                                       | customerAccount string型, QueryResultSettings queryResultSettings                                                                                    | PageResult\<OrderInvoice\> | 従業員                 | 与えられた顧客IDに関連付けられている顧客に結びつく未処理の注文請求書を取得します。 |
| GetInvoices                                            | InvoiceSearchCriteria invoiceSearchCriteria, QueryResultSettings queryResultSettings                                                               | PageResult\<OrderInvoice\> | 従業員                 | 検索条件に結びつく未処理の請求書を取得します。                                              |
| GetInvoicedSalesLinesBy- SalesIds                        | IEnumerable\<string型\> salesIds, QueryResultSettings queryResultSettings                                                                        | PageResult\<SalesLine\>    | 従業員                 | 販売注文IDごとの請求済販売明細行の一覧を取得します。                                        |
| CreatePickingList [廃止(かわりにCreatePickingListForItemsを使用)]  | salesId string型                                                                                                                                     | 無効                           | 従業員                 | 販売注文のピッキングリストを作成します。                                                                |
| CreatePickingListForItems                              | salesId string型, IEnumerable- \<PickAndPackSalesLineParameter\> pickAndPackSalesLineParameters                                                    | string                         | 従業員                 | 販売注文の選択された行のピッキング リストを作成する。                                               |
| GetPickingLists                                        | salesId string型, QueryResultSettings queryResultSettings                                                                                            | PageResult\<PickingList\>  | 従業員                 | Retail headquarters からの受注のピッキング・リストを取得します。                                           |
| CreatePackingSlip                                      |                                                                                                                                                    | 無効                           | 従業員                 | パッキングスリップを作成する                                                                                  |
| GetSalesOrderDetailsBy- TransactionId                    | transactionId string型, searchLocationValue int型                                                                                                      | 販売注文                     | 従業員、顧客        | 取引IDごとの販売注文の詳細を取得します。                                                         |
| GetSalesOrderDetailsBy- SalesId                          | salesId string型                                                                                                                                     | 販売注文                     | 従業員、顧客        | 販売IDごとの販売注文の詳細を取得します。                                                               |
| GetSalesOrderDetailsBy- QuotationId                      | quotationId string型                                                                                                                                 | 販売注文                     | 従業員、顧客        | 見積書IDごとの販売注文の詳細を取得します。                                                           |

## <a name="cart-controller"></a>カートのコントロール

| API                                              | パラメーター                                                                                                                                                                     | 戻り値                              | 対応している商取引上の役割 | 説明                                                                                                                                                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| チェックアウト                                         | id string型, receiptEmail string型, TokenizedPaymentCard tokenizedPaymentCard, receiptNumberSequence string型, IEnumerable\<CartTenderLine\> cartTenderLines, cartVersion long型 | 販売注文                                | 従業員、顧客、匿名、アプリケーション               | 買い物カゴの品目を精算します。                                                                                                                                                                                                  |
| AddCartLines                                     | id string型, System.Collections.Generic.- IEnumerable\<CartLine\> cartLines, cartVersion long型                                                                                | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートにカートの行を追加します。                                                                                                                                                                                      |
| VoidCartLines                                    | id string型, System.Collections.Generic.- IEnumerable\<CartLine\> cartLines                                                                                                   | カート                                      | 従業員                 | カート内のカート行を無効にします。                                                                                                                                                                                   |
| UpdateCartLines                                  | id string型, System.Collections.Generic.- IEnumerable\<CartLine\> cartLines                                                                                                   | カート                                      | 従業員、顧客、匿名、アプリケーション               | カート内のカート行を更新します。                                                                                                                                                                                 |
| RefillGiftCard                                   | id string型, giftCardId string型, amount decimal型, currencyCode string型, lineDescription string型)                                                                                    | カート                                      | 従業員                | ギフトカードに残額を加算                                                                                                                                                                                           |
| IssueGiftCard                                    | id string型, giftCardId string型, amount decimal型, currencyCode string型, lineDescription string型, tenderTypeId string型                                                                | カート                                      | 従業員                | ギフト カードを発行する。                                                                                                                                                                                                   |
| CashOutGiftCard                                  | id string型, giftCardId string型, amount decimal型, currencyCode string型, lineDescription string型                                                                                     | カート                                      | 従業員                | ギフト カードを現金化する                                                                                                                                                                                               |
| AddTenderLine                                    | id string型, CartTenderLine cartTenderLine, cartVersion long型                                                                                                                   | カート                                      | 従業員                | カートの入金明細行を追加します。                                                                                                                                                                                          |
| AddPreprocessed- TenderLine                        | id string型, TenderLine preprocessedTenderLine, cartVersion long型                                                                                                               | カート                                      | 従業員                | 事前処理済の入金明細を追加します。                                                                                                                                                                                 |
| ValidateTender- LineForAdd                         | id string型, TenderLine tenderLine                                                                                                                                              | 無効                                      | 従業員                 | カートの入金明細行を確認します。                                                                                                                                                                                          |
| UpdateTenderLine- Signature                        | id string型, tenderLineId string型, signatureData string型                                                                                                                          | カート                                      | 従業員                | カートの入金明細行の署名を更新します。                                                                                                                                                                             |
| VoidTenderLine                                   | id string型, tenderLineId string型, System.Collections.Generic.- IEnumerable\<ReasonCodeLine\> reasonCodeLines, bool? isPreprocessed = false, bool? forceVoid = false           | カート                                      | 従業員                | カートの入金明細行を無効にします。                                                                                                                                                                                         |
| SuspendWithJournal                               | id string型, journalCartId string型, receiptNumberSequence string型                                                                                                                 | カート                                      | 従業員                | カートを中断して仕訳入力を行います。                                                                                                                                                                            |
| 経歴                                           | id string型                                                                                                                                                                     | カート                                      | 従業員                | 保留中のカートを再開します。                                                                                                                                                                                           |
| ResumeFromReceiptId                              | receiptId string型                                                                                                                                                              | カート                                      | 従業員                | レシートIDに基づいて中断しているカートを再開します。                                                                                                                                                                       |
| RecallOrder                                      | transactionId string型, salesId string型                                                                                                                                           | カート                                      | 従業員                | 顧客の注文を取り消します。                                                                                                                                                                                           |
| AddInvoicedSales- LinesToCart                      | transactionId string型, IEnumerable\<long型\> invoicedLineIds                                                                                                                 | カート                                      | 従業員                | 請求済の販売明細をカートに追加します。                                                                                                                                                                                   |
| RecallQuote                                      | transactionId string型, string quoteId                                                                                                                                          | カート                                      | 従業員                | 見積を取り消します。                                                                                                                                                                                                    |
| RecallSalesInvoice                               | transactionId string型, invoiceId string型                                                                                                                                        | カート                                      | 従業員                 | 渡された請求書IDに関連付けられた請求書を示すカートを取得します。                                                                                                                            |
| AddOrderInvoice                                  | id string型, invoiceId string型, lineDescription string型                                                                                                                           | カート                                      | 従業員                 | 渡された請求書IDに関連付けられた請求書をカートに追加します。                                                                                                                                         |
| AddInvoices                                      | key string型, IEnumerable\<string型\> invoiceIds                                                                                                                              | カート                                      | 従業員                 | 請求書をカートに追加します。                                                                                                                                                                                               |
| RecalculateOrder                                 | id string型                                                                                                                                                                     | カート                                      | 従業員                 | 顧客注文の再計算をします。                                                                                                                                                                                      |
| UpdateCommission- SalesGroup                       | transactionId string型, cartLineId string型, commissionSalesGroup string型, isUserInitiated bool型                                                                                    | カート                                      | 従業員                 | 明細または取引のコミッション販売グループを更新します。                                                                                                                                                          |
| CartDeliveryPreferences                          | id string型                                                                                                                                                                     | CartDeliveryPreferences                   | 従業員、顧客、匿名、アプリケーション               | カート内のアイテムに基づいて、適用可能な配送設定タイプを取得します。                                                                                                                                       |
| GetLineDeliveryOptions                           | id string型, IEnumerable- \<LineShippingAddress\> lineShippingAddresses, QueryResultSettings queryResultSettings                                                              | PageResult- \<SalesLineDeliveryOption\> | 従業員、顧客、匿名、アプリケーション               | カートの配送明細オプションを取得します。                                                                                                                                                                          |
| GetLineDeliveryOptionsBy- ChannelId                | id string型, IEnumerable- \<LineShippingAddress\> lineShippingAddresses, channelId long型, QueryResultSettings queryResultSettings                                              | PageResult- \<SalesLineDeliveryOption\> | 従業員、顧客、匿名、アプリケーション               | チャンネルIDごとのカートの配送明細オプションを取得します。                                                                                                                                                |
| GetPaymentsHistory                               | id string型, QueryResultSettings queryResultSettings                                                                                                                            | PageResult\<TenderLine\>              | 従業員                 | カートIDを指定して支払履歴を取得します。                                                                                                                                                                |
| GetDeliveryOptions                               | string string型, Address shippingAddress, QueryResultSettings queryResultSettings                                                                                                   | PageResult- \<DeliveryOption\>          | 従業員、顧客、匿名、アプリケーション               | カートの配送オプションを取得します。                                                                                                                                                                             |
| UpdateLineDelivery- Specifications                 | string string型, System.Collections.Generic.- IEnumerable- \<LineDeliverySpecification\> lineDeliverySpecifications                                                                 | カート                                      | 従業員、顧客、匿名、アプリケーション               | カート明細ごとに配送仕様を更新します。                                                                                                                                                                  |
| AddCharge                                        | cartId string型, moduleTypeValue int型, chargeCode string型, calculatedAmount decimal型                                                                                               | カート                                      | 従業員、アプリケーション               | 買い物カゴに請求金額を追加します。                                                                                                                                                                                           |
| OverrideCharge                                   | cartId string型, chargeLineId string型, amount decimal型, IEnumerable\<ReasonCodeLine\> reasonCodeLines                                                                         | カート                                      | 従業員、アプリケーション               | カート内の手数料金額を上書きします。                                                                                                                                                                        |
| AddCartLineCharge                                | cartId string型, cartLineId string型, moduleTypeValue int型, string chargeCode string型, calculatedAmount decimal型                                                                            | カート                                      | 従業員、アプリケーション               | カート明細に手数料を追加します。                                                                                                                                                                                      |
| OverrideCartLineCharge                           | cartId string型, cartLineId string型, chargeLineId string型, amount decimal型, IEnumerable\<ReasonCodeLine\> reasonCodeLines                                                      | カート                                      | 従業員、アプリケーション               | カート内の明細手数料の金額を上書きします。                                                                                                                                                                          |
| UpdateDelivery- Specification                      | string string型, DeliverySpecification deliverySpecification                                                                                                                        | カート                                      | 従業員、顧客、匿名、アプリケーション               | カート ヘッダーの配送仕様を更新します。                                                                                                                                                                 |
| OverrideCartLinePrice                            | string string型, string cartLineId, decimal price                                                                                                                                   | カート                                      | 従業員                 | カートIDとバーコードスキャン情報を送信して、バーコードのワークフローを処理します。                                                                                                                      |
| GetPromotions                                    | id string型                                                                                                                                                                     | CartPromotions                            | 従業員、顧客、匿名、アプリケーション               | 買い物カゴの宣伝商品を取得します。                                                                                                                                                                                       |
| AddDiscountCode                                  | string string型, string discountCode                                                                                                                                                | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートに割引コードを追加します。                                                                                                                                                                                          |
| RemoveDiscountCodes                              | string string型, IEnumerable\<string型\> discountCodes                                                                                                                            | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートから割引コードを削除します。                                                                                                                                                                                     |
| RemoveCartLines                                  | string string型, System.Collections.Generic.- IEnumerable\<string型\> cartLineIds                                                                                                   | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートの明細行を削除します。                                                                                                                                                                                             |
| 検索                                           | CartSearchCriteria cartSearchCriteria, QueryResultSettings queryResultSettings                                                                                                | PageResult\<Cart\>                    | 顧客                 | カートを顧客別に取得します。                                                                                                                                                                                         |
| GetCardPayment- AcceptPoint                        | string string型, CardPaymentAcceptSettings cardPaymentAcceptSettings                                                                                                                | CardPaymentAcceptPoint                    | 従業員、顧客、匿名、アプリケーション               | Webページなど、カード支払いの受付ポイントを取得します。                                                                                                                                                          |
| RetrieveCardPayment- AcceptResult                  | resultAccessCode string型                                                                                                                                                       | CardPayment- AcceptResult                   | 従業員、顧客、匿名、アプリケーション               | 支払承認、カード トークンなど、カード支払の受理結果を取得します。                                                                                                                             |
| AddCoupons                                       | string string型, IEnumerable\<string型\> couponCodes, bool? isLegacyDiscountCode = false                                                                                          | カート                                      | 従業員、顧客、匿名、アプリケーション               | クーポンをカートに追加します。                                                                                                                                                                                            |
| RemoveCoupons                                    | string string型, IEnumerable\<string型\> couponCodes                                                                                                                              | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートからクーポンコードを削除します。                                                                                                                                                                                  |
| GetChargeCodes                                   | QueryResultSettings 設定                                                                                                                                                  | PageResult\<ChargeCode\>              | 従業員、アプリケーション               | すべての料金コードを取得します。                                                                                                                                                                                          |
| GetMaxLoyaltyPointsTo- RedeemFor- TransactionBalance | cartId string型, loyaltyCardNumber string型, redeemCurrency string型    | LoyaltyPoint- RedemptionEstimate            | 従業員、顧客                  | ロイヤリティ カードが取引残高に適用できる最大通貨額と、その最大通貨額を生成するために使用されるポイント報酬額を含むLoyaltyPoint-RedemptionEstimateオブジェクトを取得します。 |
| GetDeclinedOrVoided- CardReceipts                  | cartId string型, TenderLine preprocessedTenderLine, ReceiptRetrievalCriteria criteria, QueryResultSettings queryResultSettings                                                  | PageResult\<Receipt\>                 | 従業員                 | カードの支払/入金が行われなかった明細行のギフトレシート群を取得します。                                                                                                                                   |
| ResetAllCharges                                  | id string型                                                                                                                                                                     | カート                                      | 従業員、アプリケーション               | カートの手数料(手動で追加および上書きされたすべての手数料の削除を含む)を再計算します。                                                                                                                   |

## <a name="address-controller"></a>アドレスのコントロール

| API                | パラメーター                               | 戻り値                     | 対応している商取引上の役割 | 説明               |
|--------------------|-----------------------------------------|----------------------------------|--------------------------|---------------------------|
| GetAddressPurposes | QueryResultSettings queryResultSettings | PageResult\<AddressPurpose\> | 従業員、顧客、匿名、アプリケーション               | 住所の目的を取得します。 |

## <a name="barcode-controller"></a>バーコードのコントロール

| API            | パラメーター        | 戻り値 | 対応している商取引上の役割 | 説明                 |
|----------------|------------------|--------------|--------------------------|-----------------------------|
| GetBarcodeById | barcodeId string型 | バーコード      | 従業員                 | IDごとのバーコードを取得します。 |

## <a name="cash-declaration-controller"></a>現金申告のコントロール

| API                 | パラメーター                               | 戻り値                      | 対応している商取引上の役割 | 説明                 |
|---------------------|-----------------------------------------|-----------------------------------|--------------------------|-----------------------------|
| GetCashDeclarations | QueryResultSettings queryResultSettings | PageResult\<CashDeclaration\> | 従業員                 | IDごとのバーコードを取得します。 |

## <a name="cities-controller"></a>市区町村のコントロール

| API       | パラメーター                                                                                                | 戻り値               | 対応している商取引上の役割 | 説明                                                               |
|-----------|----------------------------------------------------------------------------------------------------------|----------------------------|--------------------------|---------------------------------------------------------------------------|
| GetCities | countryRegionId string型, stateProvinceId string型, countyId string型, QueryResultSettings queryResultSettings | PageResult\<CityInfo\> | 従業員                 | すべての都市を国/地域、州、郡でフィルタリングします。 |

## <a name="counties-controller"></a>群のコントロール

| API         | パラメーター                                                                               | 戻り値                 | 対応している商取引上の役割 | 説明                                                         |
|-------------|-----------------------------------------------------------------------------------------|------------------------------|--------------------------|---------------------------------------------------------------------|
| GetCounties | countryRegionId string型, stateProvinceId string型, QueryResultSettings queryResultSettings | PageResult\<CountyInfo\> | 従業員                 | 国/地域および州によってフィルタされたすべての郡を取得します。 |

## <a name="country-region-controller"></a>国/地域のコントロール

| API         | パラメーター                                                                               | 戻り値                 | 対応している商取引上の役割 | 説明                                                         |
|-------------------------------|------------------------------------------------------------|-------------------------------------|--------------------------|-----------------------------------------------------------------------------------------------|
| GetCountryRegionsFor- Shipping  | QueryResultSettings queryResultSettings   PageResult\<CountryRegionInfo\> | | 従業員、顧客、匿名、アプリケーション    | 現在のチャネルに設定されている出荷モードで翻訳された国/地域を取得します。 |
| GetCountryRegionsBy- LanguageId | languageId string型, QueryResultSettings queryResultSettings | PageResult\<CountryRegionInfo\> | 従業員、顧客、匿名、アプリケーション               | 言語IDでフィルタされたすべての国/地域を取得します。                                          |
| GetCountryRegions             | QueryResultSettings queryResultSettings                    | PageResult\<CountryRegionInfo\> | 従業員                 | すべての国/地域を取得します。                                                                |

## <a name="credit-memo-controller"></a>クレジット メモのコントロール

| API               | パラメーター           | 戻り値 | 対応している商取引上の役割 | 説明                    |
|-------------------|---------------------|--------------|--------------------------|--------------------------------|
| GetCreditMemoById | creditMemoId string型 | CreditMemo   | 従業員                 | IDを使ってクレジット メモを取得します。 |

## <a name="delivery-options-controller"></a>配送オプションのコントロール

| API                | パラメーター             | 戻り値                     | 対応している商取引上の役割 | 説明                               |
|--------------------|-----------------------------------------------------------------------------|----------------------------------|--------------------------|-------------------------------------------|
| GetDeliveryOptions | string string型, Address shippingAddress, QueryResultSettings queryResultSettings | PageResult\<DeliveryOption\> | 従業員、顧客、匿名、アプリケーション               | チャネルの配送オプションを取得します。 |

## <a name="customer-group-controller"></a>顧客グループのコントロール

| API               | パラメーター                               | 戻り値                    | 対応している商取引上の役割 | 説明                        |
|-------------------|-----------------------------------------|---------------------------------|--------------------------|------------------------------------|
| GetCustomerGroups | QueryResultSettings queryResultSettings | PageResult\<CustomerGroup\> | 従業員、顧客、匿名、アプリケーション               | 顧客グループ群を取得します。 |

## <a name="currency-controller"></a>通貨のコントロール

| API         | パラメーター                                                                               | 戻り値                 | 対応している商取引上の役割 | 説明                                                         |
|------------------------------|--------------------------------------------------------------------------------|----------------------------------|--------------------------|---------------------------------------|
| GetCurrenciesAmount          | currencyCode string型, amount decimal型, QueryResultSettings queryResultSettings   | PageResult\<CurrencyAmount\> | 従業員                 | 通貨金額を取得します。           |
| CalculateTotalCurrencyAmount | System.Collections.Generic.IEnumerable \<CurrencyRequest\> currenciesAmount | CurrencyAmount                   | 従業員                 | 通貨の合計金額を計算します。 |

## <a name="customer-balance-controller"></a>顧客残高のコントロール

| API                | パラメーター                                         | 戻り値     | 対応している商取引上の役割 | 説明                |
|--------------------|---------------------------------------------------|------------------|--------------------------|----------------------------|
| GetCustomerBalance | accountNumber string型, invoiceAccountNumber string型 | CustomerBalances | 従業員                 | 顧客残高を取得します。 |

## <a name="device-configuration-controller"></a>デバイス構成のコントロール

| API                    | パラメーター | 戻り値        | 対応している商取引上の役割 | 説明                         |
|------------------------|-----------|---------------------|--------------------------|-------------------------------------|
| GetDeviceConfiguration |           | DeviceConfiguration | 従業員                 | 単体のデバイス構成を取得します。 |

## <a name="district-controller"></a>地域 のコントロール

| API          | パラメーター                                                                                                                 | 戻り値                   | 対応している商取引上の役割 | 説明                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------|--------------------------|-------------------------------------------------------------------------------------|
| GetDistricts | countryRegionId string型, stateProvinceId string型, countyId string型, cityName string型, QueryResultSettings queryResultSettings | PageResult\<DistrictInfo\> | 従業員                 | 国/地域、州、郡、市でフィルタされたすべての地区情報を取得します。 |

## <a name="state-province-controller"></a>州 地域 のコントロール

| API               | パラメーター                                                       | 戻り値                        | 対応している商取引上の役割 | 説明                                                 |
|-------------------|-----------------------------------------------------------------|-------------------------------------|--------------------------|-------------------------------------------------------------|
| GetStateProvinces | countryRegionId string型, QueryResultSettings queryResultSettings | PageResult\<StateProvinceInfo\> | 従業員、顧客、匿名、アプリケーション               | 国/地域でフィルタされたすべての州または地域を取得します。 |

## <a name="discount-controller"></a>割引のコントロール

| API                       | パラメーター                                                                          | 戻り値                   | 対応している商取引上の役割 | 説明                                                     |
|---------------------------|------------------------------------------------------------------------------------|--------------------------------|--------------------------|-----------------------------------------------------------------|
| GetDiscountCodes          | QueryResultSettings queryResultSettings                                            | PageResult\<DiscountCode\> | 従業員                 | 一連の割引コードを取得します。                              |
| GetDiscountCodesByOfferId | offerId string型, QueryResultSettings queryResultSettings                            | PageResult\<DiscountCode\> | 従業員                 | オファーIDでフィルタされた割引コード群を取得します。 |
| GetDiscountCodesByKeyword | keyword string型, DateTimeOffset activeDate, QueryResultSettings queryResultSettings | PageResult\<DiscountCode\> | 従業員                 | 割引コードを検索します。                                    |
| GetDiscountCode           | discountCode string型                                                                | DiscountCode                   | 従業員                 | 割引コードを取得します。                                         |

## <a name="zipcodes-controller"></a>郵便番号のコントロール

| API                   | パラメーター                                                                                                                                  | 戻り値                  | 対応している商取引上の役割 | 説明                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|--------------------------|----------------------------------------------------------------------------------------------|
| GetZipCodes           | countryRegionId string型, stateProvinceId string型, countyId string型, cityName string型, district string型, QueryResultSettings queryResultSettings | PageResult\<ZipCodeInfo\> | 従業員                 | 国/地域、州、郡、市、地区でフィルタされたすべての郵便番号を取得します。 |
| GetAddressFromZipCode | countryRegionId string型, zipPostalCode string型, QueryResultSettings queryResultSettings                                                      | PageResult\<ZipCodeInfo\> | 従業員、顧客、匿名、アプリケーション               | 国/地域別にフィルタされた郵便番号に関連付けられた住所の詳細を取得します。                |

## <a name="suspended-cart-controller"></a>中断されたカートのコントロール

| API                  | パラメーター                               | 戻り値                    | 対応している商取引上の役割 | 説明               |
|----------------------|-----------------------------------------|---------------------------------|--------------------------|---------------------------|
| GetAllSuspendedCarts | QueryResultSettings queryResultSettings | PageResult\<SuspendedCart\> | 従業員                 | すべての保留中のカートを取得します。 |

## <a name="tender-types-controller"></a>支払/入金タイプのコントロール

| API                     | パラメーター                               | 戻り値                 | 対応している商取引上の役割 | 説明                  |
|-------------------------|-----------------------------------------|------------------------------|--------------------------|------------------------------|
| GetTenderTypes          | QueryResultSettings queryResultSettings | PageResult\<TenderType\> | 従業員、顧客、匿名、アプリケーション               | 支払/入金タイプを取得する           |
| RoundAmountByTenderType | amount decimal型, tenderTypeId string型     | decimal                      | 従業員                 | 支払/入金タイプ別の丸め金額。 |

## <a name="publishing-controller"></a>公開処理のコントロール

| API                           | パラメーター                                            | 戻り値 | 対応している商取引上の役割 | 説明                               |
|-------------------------------|------------------------------------------------------|--------------|--------------------------|-------------------------------------------|
| SetOnlineChannelPublishStatus | publishingStatus int型, publishingStatusMessage string型 | 無効         | 応募              | オンライン チャネルの公開ステータスを更新します。 |

## <a name="language-controller"></a>言語のコントロール

| API          | パラメーター                               | 戻り値                        | 対応している商取引上の役割 | 説明                             |
|--------------|-----------------------------------------|-------------------------------------|--------------------------|-----------------------------------------|
| GetLanguages | QueryResultSettings queryResultSettings | PageResult\<SupportedLanguage\> | 従業員                 | 対応している言語群を取得します。 |

## <a name="localized-string-controller"></a>ローカライズされた文字列のコントロール

| API                 | パラメーター                                                               | 戻り値                      | 対応している商取引上の役割 | 説明                                                                  |
|---------------------|-------------------------------------------------------------------------|-----------------------------------|--------------------------|------------------------------------------------------------------------------|
| GetLocalizedStrings | languageId string型, textId int型, QueryResultSettings queryResultSettings | PageResult\<LocalizedString\> | 従業員                 | 言語ID、テキストIDでフィルタされたすべてのローカライズされた文字列を取得します。 |

## <a name="notification-controller"></a>通知のコントロール

| API                      | パラメーター                                                                            | 戻り値                        | 対応している商取引上の役割 | 説明                |
|--------------------------|--------------------------------------------------------------------------------------|-------------------------------------|--------------------------|----------------------------|
| GetNotifications         | IEnumerable\<int型\> subscribedOperations, QueryResultSettings queryResultSettings | ICollection\<NotificationItem\> | 従業員                 | 通知を取得します。    |
| AcknowledgeNotifications | DateTimeOffset lastPullDateTime                                                      | 無効                                | 従業員                 | 通知を確認します。 |

## <a name="number-sequence-controller"></a>番号シーケンスのコントロール

| API                     | パラメーター                               | 戻り値                      | 対応している商取引上の役割 | 説明                                             |
|-------------------------|-----------------------------------------|-----------------------------------|--------------------------|---------------------------------------------------------|
| GetLatestNumberSequence | QueryResultSettings queryResultSettings | PageResult\<LocalizedString\> | 従業員                 | 現在の端子の次の番号シーケンスを取得します。 |

## <a name="reasoncodes-controller"></a>ReasonCodesのコントロール

| API                       | パラメーター                                                         | 戻り値                 | 対応している商取引上の役割 | 説明                                          |
|---------------------------|-------------------------------------------------------------------|------------------------------|--------------------------|------------------------------------------------------|
| GetReasonCodes            | QueryResultSettings queryResultSettings                           | PageResult\<ReasonCode\> | 従業員                 | 理由コードを取得します。                               |
| GetReturnOrderReasonCodes | QueryResultSettings queryResultSettings                           | PageResult\<ReasonCode\> | 従業員                 | 返品注文の理由コードを取得します。                      |
| GetReasonCodesById        | reasonCodeGroupId string型, QueryResultSettings queryResultSettings | PageResult\<ReasonCode\> | 従業員                 | グループまたは単一のIDごとに理由コードを取得します。 |

## <a name="receipt-controller"></a>レシートのコントロール

| API                             | パラメーター                                                            | 戻り値                  | 対応している商取引上の役割 | 説明                                                                     |
|---------------------------------|----------------------------------------------------------------------|-------------------------------|--------------------------|---------------------------------------------------------------------------------|
| GetReceiptMasks                 | receiptTransactionType int型, QueryResultSettings queryResultSettings | PageResult\<ReceiptMask\> | 従業員                 | 受領マスクを取得します。                                                        |
| ValidatePrintReceiptCopyAllowed | SalesOrder salesOrderToPrint                                         | 無効                          | 従業員                 | 受領コピーの印刷操作が許可されているかどうかを検証します。 |

## <a name="report-datasets-controller"></a>レポートデータセットのコントロール

| API                  | パラメーター                                                            | 戻り値  | 対応している商取引上の役割 | 説明                                                                           |
|----------------------|----------------------------------------------------------------------|---------------|--------------------------|---------------------------------------------------------------------------------------|
| SearchReportDataSet  | receiptTransactionType int型, QueryResultSettings queryResultSettings | ReportDataSet | 従業員                 | レポートID、パラメータ、場所でフィルタされたすべてのレポートデータセットを検索します。 |
| GetReportDataSetById | SalesOrder salesOrderToPrint                                         | ReportDataSet | 従業員                 | IDでレポートデータセットを取得します。                                                           |
| GetSrsReportDataSet  |                                                                      | ReportDataSet | 従業員                 | SSRSレポートデータセットを取得します。                                                            |

## <a name="search-controller"></a>検索処理のコントロール

| API                    | パラメーター                                                                 | 戻り値                       | 対応している商取引上の役割 | 説明                                         |
|------------------------|---------------------------------------------------------------------------|------------------------------------|--------------------------|-----------------------------------------------------|
| GetSearchSuggestions   | SearchSuggestionCriteria suggestionCriteria, QueryResultSettings 設定 | PageResult\<searchsuggestion\> | 従業員、顧客、匿名、アプリケーション               | 検索候補を取得します。                            |
| GetSearchConfiguration |                                                                           | SearchConfiguration                | 従業員、顧客、匿名、アプリケーション               | Azure Searchからチャネル検索設定を取得 |

## <a name="tax-controller"></a>税金処理のコントロール

| API               | パラメーター                                                                 | 戻り値                    | 対応している商取引上の役割 | 説明                                                        |
|-------------------|---------------------------------------------------------------------------|---------------------------------|--------------------------|--------------------------------------------------------------------|
| GetTaxOverrides   | SearchSuggestionCriteria suggestionCriteria, QueryResultSettings 設定 | PageResult\<TaxOverride\>   | 従業員                 | 指定した検索条件に一致する税金の上書きを検索します。 |
| GetSalesTaxGroups |                                                                           | PageResult\<SalesTaxGroup\> | 従業員                 | 売上税のグループを取得します。                                         |

## <a name="tender-drop-and-declare-operation-controller"></a>支払/入金のドロップおよびオペレーション宣言のコントロール

| API                             | パラメーター                                           | 戻り値              | 対応している商取引上の役割 | 説明                                               |
|---------------------------------|-----------------------------------------------------|---------------------------|--------------------------|-----------------------------------------------------------|
| CreateDropAndDeclareTransaction | DropAndDeclareTransaction dropAndDeclareTransaction | DropAndDeclareTransaction | 従業員                 | 支払/入金の保存と、店舗の申告操作を実行します。 |

## <a name="unit-of-measure-controller"></a>測定単位のコントロール

| API               | パラメーター                               | 戻り値                    | 対応している商取引上の役割 | 説明                                          |
|-------------------|-----------------------------------------|---------------------------------|--------------------------|------------------------------------------------------|
| GetUnitsOfMeasure | QueryResultSettings queryResultSettings | PageResult\<UnitOfMeasure\> | 従業員                 | 店舗で対応しているすべての測定単位を取得します。 |

## <a name="income-expense-accounts-controller"></a>収入/経費勘定のコントロール

| API                      | パラメーター                                                             | 戻り値                           | 対応している商取引上の役割 | 説明                          |
|--------------------------|-----------------------------------------------------------------------|----------------------------------------|--------------------------|--------------------------------------|
| GetIncomeExpenseAccounts | incomeExpenseAccountType int型, QueryResultSettings queryResultSettings | PageResult\<IncomeExpenseAccount\> | 従業員                 | 収入勘定または経費勘定科目を取得します。 |

## <a name="products-controller"></a>製品のコントロール

| API                               | パラメーター                                                                                                                                                                                                                                                                   | 戻り値                               | 対応している商取引上の役割 | 説明                                                                                                                               |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 検索                            | ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                        | IEnumerable\<Product\>                 | 従業員、顧客、匿名、アプリケーション               | ODataクエリを使用して製品を検索します。                                                                                               |
| GetById                           | recordId long型, channelId long型                                                                                                                                                                                                                                               | SimpleProduct                              | 従業員、顧客、匿名、アプリケーション              | レコードIDによってSimpleProductを取得します。                                                                                            |
| 取得                               |                                                                                                                                                                                                                                                                             | PageResult\<Product\>                  | 従業員, 顧客, 店舗                | 製品を検索します。                                                                                                                 |
| GetByIds                          | channelId long型, IEnumerable\<long型\> productIds, QueryResultSettings queryResultSettings                                                                                                                                                                                 | PageResult\<SimpleProduct\>            | 従業員、顧客、匿名、アプリケーション               | チャンネルIDとレコードIDに基づいて製品群を取得します。                                                          |
| GetRecommendedProducts            | IEnumerable\<long型\> productIds, customerAccountNumber string型, QueryResultSettings queryResultSettings                                                                                                                                                                   | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション              | 一群のプロダクトIDが指定して、推奨されたSimpleProduct群を取得します。                    |
| 比較                           | channelId long型, catalogId long型, IEnumerable\<long型\> productIds, QueryResultSettings queryResultSettings                                                                                                                                                                 | PageResult- \<ProductComparisonLine\>    | 従業員、顧客、匿名、アプリケーション              | 製品を比較します。                                                                                                                        |
| SearchByCategory                  | channelId long型, catalogId long型, categoryId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                    | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション              | カテゴリに属している製品を直接、またはその子カテゴリを介して検索します。                                                     |
| SearchByText                      | channelId long型, catalogId long型, searchText string型, QueryResultSettings queryResultSettings                                                                                                                                                                                  | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション               | 指定した検索テキストに関連付けられた製品を検索します。                                                                       |
| GetSearchSuggestions              | channelId long型, catalogId long型, searchText string型, hitPrefix string型, hitSuffix string型, QueryResultSettings queryResultSettings                                                                                                                                              | PageResult- \<SearchSuggestion\>         | 従業員、顧客、匿名、アプリケーション               | (部分的な) 検索テキストに基づいて推奨される検索語句を取得します。                                                                         |
| GetRefinersByCategory             | catalogId long型, categoryId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                                    | PageResult- \<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | 指定されたカテゴリ製品で使用できる製品の絞り込み条件を取得します。                                                                  |
| GetRefinersByText                 | catalogId long型, searchText string型, QueryResultSettings queryResultSettings                                                                                                                                                                                                  | PageResult- \<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | 指定されたテキストを検索した結果、製品で使用可能なプロダクトリファイナーを取得します。                                             |
| GetProductSearchRefiners          | ProductSearchCriteria searchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                               | PageResult- \<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | 使用されている絞り込み条件と検索テキスト/カテゴリIDの組み合わせから得られる結果から、製品で使用できる製品の絞り込み条件を取得します。 |
| GetRefinerValuesByCategory        | catalogId long型, categoryId long型, refinerId long型, refinerSourceValue int型, QueryResultSettings queryResultSettings                                                                                                                                                            | PageResult- \<ProductRefinerValue\>      | 従業員、顧客、匿名、アプリケーション              | 指定されたカテゴリ製品で使用できる製品の絞り込み条件を取得します。                                                            |
| GetRefinerValuesByText            | catalogId long型, searchText string型, refinerId long型, refinerSourceValue int型, QueryResultSettings queryResultSettings                                                                                                                                                          | PageResult- \<ProductRefinerValue\>      | 従業員、顧客、匿名、アプリケーション               | 指定されたテキストを検索した結果、製品で使用可能なプロダクトリファイナーの値を取得します。                                       |
| RefineSearchByCategory            | channelId long型, catalogId long型, categoryId long型, IEnumerable- \<ProductRefinerValue\> refinementCriteria, QueryResultSettings queryResultSettings                                                                                                                         | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション              | カテゴリに属している製品を直接、またはその子カテゴリを介して検索します。                                    |
| RefineSearchByText                | channelId long型, catalogId long型, searchText string型, IEnumerable- \<ProductRefinerValue\> refinementCriteria, QueryResultSettings queryResultSettings                                                                                                                       | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション               | 指定された検索テキストに関連する製品に対して実行される検索を絞り込みます。                                                      |
| GetDimensionValues                | recordId long型, channelId long型, dimension int型, IEnumerable\<ProductDimension\> matchingDimensionValues, QueryResultSettings queryResultSettings                                                                                                                          | PageResult- \<ProductDimensionValue\>    | 従業員、顧客、匿名、アプリケーション               | 指定された要件に基づいて製品のディメンション値を取得します。                                                              |
| GetVariantsBy- DimensionValues      | recordId long型, channelId long型, IEnumerable\<ProductDimension\> matchingDimensionValues, QueryResultSettings queryResultSettings                                                                                                                                         | PageResult\<SimpleProduct\>            | 従業員、顧客、匿名、アプリケーション               | 指定した要件に基づいて製品のバリエーションを取得します。                                                                     |
| GetVariantsBy- ComponentsInSlots    | recordId long型, channelId long型, IEnumerable- \<ComponentInSlotRelation\> matchingSlotTo- ComponentRelationship, QueryResultSettings queryResultSettings                                                                                                                      | PageResult\<SimpleProduct\>            | 従業員、顧客、匿名、アプリケーション               | 指定したスロットの組み合わせのコンポーネントに基づいて、製品のバリエーションを取得します。                                                    |
| GetDefaultComponents              | recordId long型, channelId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                                      | PageResult- \<productcomponent\>         | 従業員、顧客、匿名、アプリケーション               | 指定したプロダクトを構成する既定の個々のパーツを取得します。                                                                  |
| GetComponentByProduct- SlotRelation | channelId long型, ComponentInSlotRelation componentRelation                                                                                                                                                                                                                   | ProductComponent                           | 従業員、顧客、匿名、アプリケーション               | 指定されたComponentIn-SlotRelationに基づいて特定の製品コンポーネントを取得します                                                  |
| GetSlotComponents                 | recordId long型, channelId long型, slotId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                         | PageResult- \<productcomponent\>         | 従業員、顧客、匿名、アプリケーション               | プロダクトの構成を完了するためにプロダクトのスロットに適合する既定のの個別パーツを取得します。                                     |
| GetFiltered- SlotComponents         | recordId long型, channelId long型, long slotId, IEnumerable- \<ComponentInSlotRelation\> selectedComponents, QueryResultSettings queryResultSettings                                                                                                                          | PageResult- \<productcomponent\>         | 従業員、顧客、匿名、アプリケーション               | 以前に選択した一連のコンポーネントで選択可能な製品コンポーネントを取得します。                                           |
| GetAttributeValues                | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult\<AttributeValue\>           | 従業員、顧客、匿名、アプリケーション              | 指定された製品の属性値を取得します。                                                                                       |
| GetRelationTypes                  | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult- \<ProductRelationType\>      | 従業員、顧客、匿名、アプリケーション               | 指定した製品と他の製品との関係の種別を取得します。                                                            |
| GetRelatedProducts                | recordId long型, channelId long型, catalogId long型, relationTypeId long型, QueryResultSettings queryResultSettings                                                                                                                                                                 | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション               | 指定した関係によって指定した製品に関連付けられている製品を検索します。                                         |
| GetRefiners                       | ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                        | PageResult\<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | ODataクエリを使用して製品リファイナーを検索します。                                                                                          |
| 変更                           | ChangedProductsSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                | IEnumerable\<Product\>                 | 従業員、店舗                | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| ReadChangedProducts               | ChangedProductsSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                | PageResult\<Product\>                  | 応募              | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| GetDeletedListings                | catalogId long型, skip long型, top long型                                                                                                                                                                                                                                         | DeletedListingsResult                      | 応募              | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| GetDeletedCatalogs                | QueryResultSettings queryResultSettings                                                                                                                                                                                                                                     | IEnumerable\<long型\>                    | 応募              | 削除されたカタログを取得します。                                                                                                                    |
| GetDeletedLanguages               | QueryResultSettings queryResultSettings                                                                                                                                                                                                                                     | IEnumerable\<string型\>                  | 応募              | 削除された言語を取得します。                                                                                                                   |
| DeleteListingsBy- Catalogs          | IEnumerable\<long型\> catalogIds                                                                                                                                                                                                                                          | 無効                                       | 応募              | カタログごとの一覧を削除します。                                                                                                             |
| DeleteListingsBy- Languages         | IEnumerable\<string型\> languages                                                                                                                                                                                                                                         | 無効                                       | 応募              | 言語別の一覧を削除します。                                                                                                            |
| BeginRead- ChangedProducts          | ChangedProductsSearchCriteria changedProductSearchCriteria                                                                                                                                                                                                                  | ReadChanged- ProductsSession                 | 応募              | 変更された製品を読み取るセッションを開始します。                                                                                                  |
| EndReadChangedProducts            | ReadChangedProductsSession セッション                                                                                                                                                                                                                                          | 無効                                       | 応募              | 変更された製品を読み取るセッションを終了します。                                                                                                    |
| UpdateListing- PublishingStatus     | IEnumerable\<ListingPublishStatus\> publishingStatuses                                                                                                                                                                                                                  | 無効                                       | 応募              | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| GetProductAvailabilities          | IEnumerable\<long型\> itemIds, channelId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                    | PageResult- \<ProductAvailableQuantity\> | 従業員、顧客、匿名、アプリケーション               | 指定したチャネルおよび顧客の指定した品目リストの有効な在庫を取得します。                                                           |
| GetPrices                         | itemId string型, inventoryDimensionId string型, barcode string型, customerAccountNumber string型, unitOfMeasureSymbol string型, quantity decimal型, QueryResultSettings queryResultSettings                                                                                             | PageResult\<ProductPrice\>             | 従業員                 | 現在の顧客に関連する品目の価格を取得します。                                                                             |
| GetPrice                          | recordId long型, customerAccountNumber string型, unitOfMeasureSymbol string型                                                                                                                                                                                                     | ProductPrice                               | 従業員、顧客、匿名、アプリケーション               | 現在の顧客に関連する製品の価格を取得します。                                                                           |
| CalculateProductPrice             | recordId long型, customerAccountNumber string型, unitOfMeasureSymbol string型, loyaltyCardId string型, IEnumerable\<AffiliationLoyaltyTier\> affiliationLoyaltyTiers                                                                                                            | ProductPrice                               | 従業員、顧客、匿名、アプリケーション               | 価格を取得します。                                                                                                                           |
| GetActivePrices                   | ProjectionDomain projectDomain, IEnumerable\<long型\> productIds, DateTimeOffset activeDate, string customerId, IEnumerable\<AffiliationLoyaltyTier\> affiliationLoyaltyTiers, bool? includeSimpleDiscountsIn- ContextualPrice, QueryResultSettings queryResultSettings | PageResult\<ProductPrice\>             | 従業員、顧客、匿名、アプリケーション               | 価格を取得します。                                                                                                                           |
| GetMediaLocations                 | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult\<MediaLocation\>            | 従業員、顧客、匿名、アプリケーション               | 指定した製品のメディアの場所を取得します。                                                                                       |
| GetMediaBlobs                     | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult\<MediaBlob\>                | 従業員、顧客、匿名、アプリケーション               | 指定された製品のメディアブロブを取得します。                                                                                           |
| GetUnitsOfMeasure                 | recordId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                                                      | PageResult\<UnitOfMeasure\>            | 従業員、顧客、匿名、アプリケーション               | 指定した製品の測定単位を取得します。                                                                                    |
| GetChannel- ProductAttributes       | QueryResultSettings queryResultSettings                                                                                                                                                                                                                                     | PageResult\<AttributeProduct\>         | 従業員、顧客、匿名、アプリケーション               | チャネル製品属性を取得します。                                                                                                      |
| GetProductRatings                 | IEnumerable\<long型\> productIds, QueryResultSettings 設定                                                                                                                                                                                                            | PageResult\<ProductRating\>            | 従業員、顧客、匿名、アプリケーション              | 製品識別子に基づく製品評価を取得します。                                                                        |

## <a name="sales-orders-fulfillment-controller"></a>販売注文履行 コントロール

| API                            | パラメーター                                                                                                                                  | 戻り値                       | 対応している商取引上の役割 | 説明                                                                |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|--------------------------|----------------------------------------------------------------------------|
| ShipFulfillmentLines           | IEnumerable\<ShipFulfillmentLine\> fulfillmentLines                                                                                    | 無効                               | 従業員                 | 履行明細を出荷します。 AX の請求書。                                |
| AcceptFulfillmentLines         | IEnumerable\<FulfillmentLineParameter\> fulfillmentLines                                                                               | 無効                               | 従業員                 | 履行明細のステータスを 受入済 に更新します。                   |
| PickFulfillmentLines           | IEnumerable\<FulfillmentLineParameter\> fulfillmentLines, IEnumerable\<FulfillmentLineParameter\> fulfillmentLines                                                                                | 無効                               | 従業員                 | 履行明細のステータスを ピッキング に更新します。                    |
| MarkAsPicked                   | IEnumerable\<FulfillmentLineParameter\> fulfillmentLines                                                                               | 無効                               | 従業員                 | 履行明細のステータスを ピック済 に更新します。                     |
| PackFulfillmentLines           | IEnumerable\<FulfillmentLineParameter\> fulfillmentLines                                                                               | 無効                               | 従業員                 | 履行明細のステータスを 梱包済 または 一部梱包済 に更新します。 |
| MarkFulfillmentLinesAsPacked   | IEnumerable\<FulfillmentLineParameter\> fulfillmentLines                                                                               | 文字列                             | 従業員                 | 履行明細のステータスを 梱包済 または 一部梱包済 に更新します。 |
| GetFulfillmentLines            | FulfillmentLineSearchCriteria 検索条件, QueryResultSettings 設定                                                                       | IEnumerable\<FulfillmentLine\> | 従業員                 | 履行明細を取得します。                                                |
| GetFulfillmentPackingSlips     |                                                                                                                                            | IEnumerable\<Receipt\>         | 従業員                 | パッキングスリップを取得します。                                                    |
| GetFulfillmentPackingSlipsById | salesId string型, packingSlipId string型, hardwareProfileId string型                                                                             | IEnumerable\<Receipt\>         | 従業員                 | パッキングスリップIDおよび売上IDでパッキングスリップを取得します。                    |
| GetFulfillmentPickingLists     | IEnumerable\<FulfillmentLineParameter\> pickingListFulfillmentLines, hardwareProfileId string型, QueryResultSettings queryResultSettings | IEnumerable\<Receipt\>         | 従業員                 | ピッキング リストを取得する。                                                    |
| RejectFulfillmentLines         | IEnumerable\<RejectFulfillmentLine\> fulfillmentLines                                                                                  | 無効                               | 従業員                 | 履行明細のステータスを 否認 に更新します                   |
| GetPackingSlipsData            | salesId string型                                                                                                                             | IEnumerable\<PackingSlipData\> | 従業員                 | 売上IDを指定して、パッキングリスト データのリストを取得します。               |

## <a name="hardware-profiles-controller"></a>ハードウェア プロファイル コントロール

| API                        | パラメーター                               | 戻り値                             | 対応している商取引上の役割 | 説明                                   |
|----------------------------|-----------------------------------------|------------------------------------------|--------------------------|-----------------------------------------------|
| GetHardwareProfileById     | hardwareProfileId string型                | HardwareProfile                          | 従業員                 | IDからハードウェアプロファイルを取得します。                  |
| GetHardwareStationProfiles | QueryResultSettings queryResultSettings | PageResult\<HardwareStationProfile\> | 従業員                 | ハードウェアプロファイルを取得します。 |

## <a name="income-expense-account-controller"></a>収入/経費勘定のコントロール

| API                      | パラメーター                                                             | 戻り値                           | 対応している商取引上の役割 | 説明                          |
|--------------------------|-----------------------------------------------------------------------|----------------------------------------|--------------------------|--------------------------------------|
| GetIncomeExpenseAccounts | incomeExpenseAccountType int型, QueryResultSettings queryResultSettings | PageResult\<IncomeExpenseAccount\> | 従業員                 | 収入勘定または経費勘定科目を取得します。 |

## <a name="kits-controller"></a>キットのコントロール

| API                        | パラメーター                     | 戻り値   | 対応している商取引上の役割 | 説明                                        |
|----------------------------|-------------------------------|----------------|--------------------------|----------------------------------------------------|
| DisassembleKitTransactions | KitTransaction | KitTransaction | 従業員                 | キット(分解)トランザクション操作を実行します。 |

## <a name="gift-card-controller"></a>ギフト カード コントロール

| API                | パラメーター         | 戻り値 | 対応している商取引上の役割 | 説明                                              |
|--------------------|-------------------|--------------|--------------------------|----------------------------------------------------------|
| GetGiftCardInquiry | giftCardId string型 | GiftCard     | 従業員、顧客、匿名、アプリケーション              | IDごとの追加情報が記載されたギフトカードを入手します。 |

## <a name="image-controller"></a>イメージのコントロール

| API          | パラメーター    | 戻り値 | 対応している商取引上の役割 | 説明                          |
|--------------|--------------|--------------|--------------------------|--------------------------------------|
| GetImageBlob | imageId long型 | MediaBlob    | 従業員、顧客、匿名、アプリケーション               | イメージIDごとのイメージBLOBを取得します。 |

## <a name="store-safe-controller"></a>店舗の金庫 コントロール

| API           | パラメーター                    | 戻り値                | 対応している商取引上の役割 | 説明          |
|---------------|------------------------------|-----------------------------|--------------------------|----------------------|
| GetStoreSafes | QueryResultSettings 設定 | PageResult\<StoreSafe\> | Employee                | 店舗の金庫リストを取得します。 |


## <a name="warehouse-controller"></a>ウェアハウスのコントロール

| API              | パラメーター                                                                         | 戻り値                        | 対応している商取引上の役割       | 説明                                                                                         |
|------------------|-----------------------------------------------------------------------------------|-------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------|
| GetWarehouseById | inventLocation string型                                                             | PageResult\<StoreSafe\>         | 従業員、顧客             | レコードIDでウェアハウスを取得します。                                                          |
| SearchWarehouses | searchText string型, QueryResultSettings queryResultSettings                        | PageResult\<Warehouse\>         | アプリケーション、従業員、顧客 | 指定された検索テキストに一致するウェアハウスのリストを取得します。                                  |
| GetLocations     | inventLocation string型, QueryResultSettings queryResultSettings                    | PageResult\<WarehouseLocation\> | アプリケーション、従業員、顧客 | 指定されたウェアハウスの場所を取得します。                                            |
| SearchLocations  | inventLocation string型, searchText string型, QueryResultSettings queryResultSettings | PageResult\<WarehouseLocation\> | アプリケーション、従業員、顧客 | 指定された検索テキストと一致する、指定された倉庫の場所の一覧を取得します。 |

## <a name="recommendation-controller"></a>推奨のコントロール

| API         | パラメーター                                                                               | 戻り値                          | 対応している商取引上の役割                  | 説明                                                                                          |
|-------------|-----------------------------------------------------------------------------------------|---------------------------------------|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| 取得         |                                                                                         | PageResult\<Recommendation\>      | アプリケーション、従業員、顧客、匿名 | 推奨の一覧を取得します。                                                                    |
| GetElements | listId string型, RecommendationCriteria criteria, QueryResultSettings queryResultSettings | PagedResult\<RecommendedElement\> | アプリケーション、従業員、顧客、匿名 | 検索条件として指定されたコンテキスト情報 (省略可能) から推奨エレメントを取得します。 |


