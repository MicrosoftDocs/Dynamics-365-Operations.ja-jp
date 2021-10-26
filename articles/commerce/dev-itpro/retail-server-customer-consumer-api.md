---
title: Commerce Scale Unit の顧客およびコンシューマー API
description: このトピックでは、さまざまな役割で利用可能であり、さまざまなクライアントが使用できる API の概要について説明します
author: mugunthanm
ms.date: 06/02/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0cf9b1c26f3408fb3f17006a809e0b48b6ae4e98
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559401"
---
# <a name="commerce-scale-unit-customer-and-consumer-apis"></a>Commerce Scale Unit の顧客およびコンシューマー API

[!include [banner](../includes/banner.md)]

このトピックでは、さまざまな役割で利用可能であり、さまざまなクライアントが使用できる API の概要について説明します 中心は、顧客フェーシング アプリケーション クライアントと e コマース クライアントについてです。

- Cloud Scale Unit のビジネス データと操作は、従業員 (販売時点管理) シナリオと顧客 (オンライン ストア) シナリオの両方で、OData Web API を通じてすべての接続デバイスで使用できます。
- 埋め込み CRT は、統一されたオムニチャネル プラットフォームを可能にします。
- アプリケーション プログラミング インターフェイス (API) はステートレスであり、多くのチャンネルからの要求を処理できます。
- API には、直線的なスケール アウト モデル ("ブリック" スケール アウト) があります。
- プラグアンドプレイのカスタマイズに対して、合成パターンを使用します。
- API は、C\# を使用して .NET スタックに組み込まれています。

## <a name="roles"></a>ロール

Cloud Scale Unit (Commerce プロキシ経由) へのすべての要求は、主にこれらの役割を果たします。

- CommerceRole.Employee
- CommerceRole.Anonymous
- CommerceRole.Customer
- CommerceRoleアプリケーション

匿名および顧客ロールは、電子商取引 (顧客/消費者) シナリオに適用されます。 匿名ロールは、サインインしていない電子商取引顧客を表す要求に使用されます。 顧客ロールは、認証済みでサインインしている電子商取引顧客を表す要求に使用されます。 ロール フィルターは、Commerce Scale Unit で公開されているすべての API に適用されます。 eCommerce シナリオでは、関連する CommerceRole.Anonymous または CommerceRole.Customer のいずれかを持つ API のみを使用することができます。

> [!NOTE]
> 既定では、匿名アクセスは有効ではありません。 環境の匿名アクセスを有効にするには、[サポート](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-support)に問い合わせてください。

## <a name="customer-controller"></a>顧客のコントロール

| API | パラメーター | 戻り値 | 対応している商取引上の役割 | 説明                |
|-----|-----------|--------------|--------------------------|----------------------------|
| GetOrderShipmentsHistory    | accountNumber  string型、QueryResultSettings queryResultSettings | PageResult\<OrderShipments\>       | 従業員、顧客、アプリケーション | 顧客からの注文の出荷履歴を取得します。  |
| CreateEntity | 顧客 | 顧客 |従業員、匿名、アプリケーション | 顧客を作成します。|
| UpdateEntity | 文字列キー、顧客の更新 | 顧客 |従業員、顧客、アプリケーション | 顧客を更新します。|
| GetOrderHistory             | accountNumber  string型、QueryResultSettings queryResultSettings           | PageResult\<SalesOrder\>           | 従業員、顧客、アプリケーション | 一群の販売注文を返します。                           |
| 検索                      | CustomerSearchCriteria customerSearchCriteria, QueryResultSettings queryResultSettings    | PageResult\<GlobalCustomer\>       | 従業員、アプリケーション         | 顧客を検索します                                        |
| GetPurchaseHistory          | accountNumber  string型、QueryResultSettings queryResultSettings      | PageResult\<PurchaseHistory\>      | 従業員、顧客、アプリケーション | 顧客の購入履歴を取得します。                           |
| GetByAccountNumbers         | IEnumerable\<string\> accountNumbers, int searchLocationValue, QueryResultSettings queryResultSettings | IEnumerable\<Customer\>     | 従業員、顧客、アプリケーション | 顧客のアカウント番号一覧から顧客リストを取得します。     |
| GetCustomerSearchFields     | queryResultSettings    | IEnumerable\<CustomerSearchField\> | 従業員、顧客、アプリケーション | 本社の店舗セットが使用する顧客検索フィールドを取得します。 |
| SearchByFields              | 顧客エンティティ                                                                                            | PageResult\<GlobalCustomer\>       | 従業員、顧客、アプリケーション | 指定したフィールドで顧客を検索します。           |
| PostNonTransactionalActivityLoyaltyPoints | loyaltyCardNumber string型, channelId Long型, affiliationId Long型, activityTypeId string型                        | 無効                                   | 従業員、顧客、アプリケーション | 非トランザクション処理後のロイヤリティポイント                    |

## <a name="sales-order-controller"></a>販売注文のコントロール

| API                                                    | パラメーター              | 戻り値                   | 対応している商取引上の役割 | 説明     |
|-------------|-----------------------------------------------------------------------------------------|------------------------------|--------------------------|---------------------------------------------------------------------|
| GetReceipts                                            | id string型, ReceiptRetrievalCriteria receiptRetrievalCriteria, QueryResultSettings queryResultSettings                                              | PageResult\<Receipt\>      | 従業員                 | 印刷用のフォームタイプに基づいて一連のレシートを取得します。                                             |
| GetGiftReceipts                                        | string id, IEnumerable\<decimal\> salesLineNumbers, ReceiptRetrievalCriteria receiptRetrievalCriteria, QueryResultSettings queryResultSettings | PageResult\<Receipt\>      | 従業員                 | 贈答品の受領を取得します。                                                                                  |
| GetByReceiptId                                         | receiptId string型, orderStoreNumber string型, orderTerminalId string型, QueryResultSettings queryResultSettings                                         | PageResult\<SalesOrder\>   | 従業員                 | レシートIDから販売注文を取得します。                                                             |
| SearchSalesTransactionsBy- ReceiptId                     | receiptId string型, QueryResultSettings queryResultSettings                                                                                          | PageResult\<SalesOrder\>   | 従業員                 | レシートIDから販売取引を取得します。                                                      |
| 検索                                                 | SalesOrderSearchCriteria salesOrderSearchCriteria, QueryResultSettings queryResultSettings                                                         | PageResult\<SalesOrder\>   | 従業員、顧客        | 指定された検索条件に一致する注文を検索します。                                              |
| SearchOrders                                           | OrderSearchCriteria orderSearchCriteria, QueryResultSettings queryResultSettings                                                                   | PageResult\<SalesOrder\>   | 従業員、顧客        | 指定された検索条件に一致する注文を検索します。                                                 |
| GetInvoicesBySalesId                                   | salesId string型, QueryResultSettings queryResultSettings                                                                                            | PageResult\<SalesInvoice\> | 従業員                 | 渡された販売IDに関連付けられている売上請求書を取得します。                                      |
| GetOrderInvoices                                       | customerAccount string型, QueryResultSettings queryResultSettings                                                                                    | PageResult\<OrderInvoice\> | 従業員                 | 与えられた顧客IDに関連付けられている顧客に結びつく未処理の注文請求書を取得します。 |
| GetInvoices                                            | InvoiceSearchCriteria invoiceSearchCriteria, QueryResultSettings queryResultSettings                                                               | PageResult\<OrderInvoice\> | 従業員                 | 検索条件に結びつく未処理の請求書を取得します。                                              |
| GetInvoicedSalesLinesBy- SalesIds                        | IEnumerable\<string\> salesIds, QueryResultSettings queryResultSettings                                                                        | PageResult\<SalesLine\>    | 従業員                 | 販売注文IDごとの請求済販売明細行の一覧を取得します。                                        |
| CreatePickingList [廃止(かわりにCreatePickingListForItemsを使用)]  | salesId string型                                                                                                                                     | 無効                           | 従業員                 | 販売注文のピッキングリストを作成します。                                                                |
| CreatePickingListForItems                              | string salesId, IEnumerable- \<PickAndPackSalesLineParameter\> pickAndPackSalesLineParameters                                                    | 文字列                         | 従業員                 | 販売注文の選択された行のピッキング リストを作成する。                                               |
| GetPickingLists                                        | salesId string型, QueryResultSettings queryResultSettings                                                                                            | PageResult\<PickingList\>  | 従業員                 | Headquarters からの受注のピッキング リストを取得します。                                           |
| CreatePackingSlip                                      |                                                                                                                                                    | 無効                           | 従業員                 | パッキングスリップを作成する                                                                                  |
| GetSalesOrderDetailsBy- TransactionId                    | transactionId string型, searchLocationValue int型                                                                                                      | 販売注文                     | 従業員、顧客        | 取引IDごとの販売注文の詳細を取得します。                                                         |
| GetSalesOrderDetailsBy- SalesId                          | salesId string型                                                                                                                                     | 販売注文                     | 従業員、顧客        | 販売IDごとの販売注文の詳細を取得します。                                                               |
| GetSalesOrderDetailsBy- QuotationId                      | quotationId string型                                                                                                                                 | 販売注文                     | 従業員、顧客        | 見積書IDごとの販売注文の詳細を取得します。                                                           |
| GetEntityByKey                     | 文字列 transactionId                                                                                                                                | 販売注文                     | 従業員        | トランザクション識別子と一致する販売注文を取得します。                                                          |
| CreateEntity                      | SalesOrder エンティティ                                                                                                                                 | 販売注文                     | 従業員、アプリケーション        | 支払/入金明細行を含む予約された販売注文をアップロードします。                                                          |
| CheckInForOrderPickup                      | long channelId、文字列 packingSlipId、文字列 channelReferenceId、IEnumerable\<CommerceProperty\> extensionProperties                                                                                                                                | CheckInForOrderPickupConfirmation                     | 匿名、顧客        | 注文集荷のチェックイン操作。                                                           |
| GetInvoiceDetails                      | InvoiceDetailsSearchCriteria invoiceDetailsSearchCriteria                                                                                                                                | SalesInvoice                     | 従業員、顧客、アプリケーション        | 請求書の検索条件によって請求書の詳細 (明細行、請求、税金) を取得します。                                                          |
| SearchSalesTransactionsByReceiptId                      | 文字列 receiptId、QueryResultSettings settings                                                                                                                                | PagedResult\<SalesOrder\>                     | 従業員        | レシート識別子から販売トランザクションを検索します。                                                           |
| SendReceipt                      | SearchReceiptCriteria searchReceiptCriteria、IEnumerable\<ElectronicAddress\> recipientAddresses                                                                                                                               | NullResponse                    | 従業員        | 指定された条件を満たす取引レシートを最大 3 つの指定された電子アドレスに送信します。
  | GetOrderByChannelReferenceLookupCriteria                      | ChannelReferenceLookupCriteria channelReferenceLookupCriteria                                                                                                                               | 販売注文                    | 従業員、顧客、アプリケーション、匿名       | 特定のチャンネル参照 ID と追加のルックアップ基準に対する販売注文を取得します。   |

## <a name="cart-controller"></a>カートのコントロール

| API                                              | パラメーター                                                                                                                                                                     | 戻り値                              | 対応している商取引上の役割 | 説明                                                                                                                                                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| チェックアウト                                         | string id, string receiptEmail, TokenizedPaymentCard tokenizedPaymentCard, string receiptNumberSequence, IEnumerable\<CartTenderLine\> cartTenderLines, long? cartVersion | 販売注文                                | 従業員、顧客、匿名、アプリケーション               | 買い物カゴの品目を精算します。                                                                                                                                                                                                  |
| AddCartLines                                     | string id, System.Collections.Generic.- IEnumerable\<CartLine\> cartLines, long? cartVersion                                                                                | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートにカートの行を追加します。                                                                                                                                                                                      |
| VoidCartLines                                    | string id, System.Collections.Generic.- IEnumerable\<CartLine\> cartLines                                                                                                   | カート                                      | 従業員                 | カート内のカート行を無効にします。                                                                                                                                                                                   |
| UpdateCartLines                                  | string id, System.Collections.Generic.- IEnumerable\<CartLine\> cartLines                                                                                                   | カート                                      | 従業員、顧客、匿名、アプリケーション               | カート内のカート行を更新します。                                                                                                                                                                                 |
| RefillGiftCard                                   | id string型, giftCardId string型, amount decimal型, currencyCode string型, lineDescription string型)                                                                                    | カート                                      | 従業員                | ギフトカードに残額を加算                                                                                                                                                                                           |
| IssueGiftCard                                    | id string型, giftCardId string型, amount decimal型, currencyCode string型, lineDescription string型, tenderTypeId string型                                                                | カート                                      | 従業員                | ギフト カードを発行する。                                                                                                                                                                                                   |
| CashOutGiftCard                                  | id string型, giftCardId string型, amount decimal型, currencyCode string型, lineDescription string型                                                                                     | カート                                      | 従業員                | ギフト カードを現金化する                                                                                                                                                                                               |
| AddTenderLine                                    | id string型, CartTenderLine cartTenderLine, cartVersion long型                                                                                                                   | カート                                      | 従業員                | カートの入金明細行を追加します。                                                                                                                                                                                          |
| AddPreprocessed- TenderLine                        | id string型, TenderLine preprocessedTenderLine, cartVersion long型                                                                                                               | カート                                      | 従業員                | 事前処理済の入金明細を追加します。                                                                                                                                                                                 |
| ValidateTender- LineForAdd                         | id string型, TenderLine tenderLine                                                                                                                                              | 無効                                      | 従業員                 | カートの入金明細行を確認します。                                                                                                                                                                                          |
| UpdateTenderLine- Signature                        | id string型, tenderLineId string型, signatureData string型                                                                                                                          | カート                                      | 従業員                | カートの入金明細行の署名を更新します。                                                                                                                                                                             |
| VoidTenderLine                                   | string id, string tenderLineId, System.Collections.Generic.- IEnumerable\<ReasonCodeLine\> reasonCodeLines, bool? isPreprocessed = false, bool? forceVoid = false           | カート                                      | 従業員                | カートの入金明細行を無効にします。                                                                                                                                                                                         |
| SuspendWithJournal                               | id string型, journalCartId string型, receiptNumberSequence string型                                                                                                                 | カート                                      | 従業員                | カートを中断して仕訳入力を行います。                                                                                                                                                                            |
| 経歴                                           | id string型                                                                                                                                                                     | カート                                      | 従業員                | 保留中のカートを再開します。                                                                                                                                                                                           |
| ResumeFromReceiptId                              | receiptId string型                                                                                                                                                              | カート                                      | 従業員                | レシートIDに基づいて中断しているカートを再開します。                                                                                                                                                                       |
| RecallOrder                                      | string transactionId, string salesId                                                                                                                                           | カート                                      | 従業員                | 顧客の注文を取り消します。                                                                                                                                                                                           |
| AddInvoicedSales- LinesToCart                      | string transactionId, IEnumerable\<long\> invoicedLineIds                                                                                                                 | カート                                      | 従業員                | 請求済の販売明細をカートに追加します。                                                                                                                                                                                   |
| RecallQuote                                      | transactionId string型, string quoteId                                                                                                                                          | カート                                      | 従業員                | 見積を取り消します。                                                                                                                                                                                                    |
| RecallSalesInvoice                               | transactionId string型, invoiceId string型                                                                                                                                        | カート                                      | 従業員                 | 渡された請求書IDに関連付けられた請求書を示すカートを取得します。                                                                                                                            |
| AddOrderInvoice                                  | id string型, invoiceId string型, lineDescription string型                                                                                                                           | カート                                      | 従業員                 | 渡された請求書IDに関連付けられた請求書をカートに追加します。                                                                                                                                         |
| AddInvoices                                      | string key, IEnumerable\<string\> invoiceIds                                                                                                                              | カート                                      | 従業員                 | 請求書をカートに追加します。                                                                                                                                                                                               |
| RecalculateOrder                                 | id string型                                                                                                                                                                     | カート                                      | 従業員                 | 顧客注文の再計算をします。                                                                                                                                                                                      |
| UpdateCommission- SalesGroup                       | transactionId string型, cartLineId string型, commissionSalesGroup string型, isUserInitiated bool型                                                                                    | カート                                      | 従業員                 | 明細または取引のコミッション販売グループを更新します。                                                                                                                                                          |
| CartDeliveryPreferences                          | id string型                                                                                                                                                                     | CartDeliveryPreferences                   | 従業員、顧客、匿名、アプリケーション               | カート内のアイテムに基づいて、適用可能な配送設定タイプを取得します。                                                                                                                                       |
| GetLineDeliveryOptions                           | string id, IEnumerable- \<LineShippingAddress\> lineShippingAddresses, QueryResultSettings queryResultSettings                                                              | PageResult- \<SalesLineDeliveryOption\> | 従業員、顧客、匿名、アプリケーション               | カートの配送明細オプションを取得します。                                                                                                                                                                          |
| GetLineDeliveryOptionsBy- ChannelId                | string id, IEnumerable- \<LineShippingAddress\> lineShippingAddresses, long channelId, QueryResultSettings queryResultSettings                                              | PageResult- \<SalesLineDeliveryOption\> | 従業員、顧客、匿名、アプリケーション               | チャンネルIDごとのカートの配送明細オプションを取得します。                                                                                                                                                |
| GetPaymentsHistory                               | id string型, QueryResultSettings queryResultSettings                                                                                                                            | PageResult\<TenderLine\>              | 従業員                 | カートIDを指定して支払履歴を取得します。                                                                                                                                                                |
| GetDeliveryOptions                               | string string型, Address shippingAddress, QueryResultSettings queryResultSettings                                                                                                   | PageResult- \<DeliveryOption\>          | 従業員、顧客、匿名、アプリケーション               | カートの配送オプションを取得します。                                                                                                                                                                             |
| UpdateLineDelivery- Specifications                 | string id, System.Collections.Generic.- IEnumerable- \<LineDeliverySpecification\> lineDeliverySpecifications                                                                 | カート                                      | 従業員、顧客、匿名、アプリケーション               | カート明細ごとに配送仕様を更新します。                                                                                                                                                                  |
| AddCharge                                        | cartId string型, moduleTypeValue int型, chargeCode string型, calculatedAmount decimal型                                                                                               | カート                                      | 従業員、アプリケーション               | 買い物カゴに請求金額を追加します。                                                                                                                                                                                           |
| OverrideCharge                                   | string cartId, string chargeLineId, decimal amount, IEnumerable\<ReasonCodeLine\> reasonCodeLines                                                                         | カート                                      | 従業員、アプリケーション               | カート内の手数料金額を上書きします。                                                                                                                                                                        |
| AddCartLineCharge                                | cartId string型, cartLineId string型, moduleTypeValue int型, string chargeCode string型, calculatedAmount decimal型                                                                            | カート                                      | 従業員、アプリケーション               | カート明細に手数料を追加します。                                                                                                                                                                                      |
| OverrideCartLineCharge                           | string cartId, string cartLineId, string chargeLineId, decimal amount, IEnumerable\<ReasonCodeLine\> reasonCodeLines                                                      | カート                                      | 従業員、アプリケーション               | カート内の明細手数料の金額を上書きします。                                                                                                                                                                          |
| UpdateDelivery- Specification                      | string string型, DeliverySpecification deliverySpecification                                                                                                                        | カート                                      | 従業員、顧客、匿名、アプリケーション               | カート ヘッダーの配送仕様を更新します。                                                                                                                                                                 |
| OverrideCartLinePrice                            | string string型, string cartLineId, decimal price                                                                                                                                   | カート                                      | 従業員                 | カートIDとバーコードスキャン情報を送信して、バーコードのワークフローを処理します。                                                                                                                      |
| GetPromotions                                    | id string型                                                                                                                                                                     | CartPromotions                            | 従業員、顧客、匿名、アプリケーション               | 買い物カゴの宣伝商品を取得します。                                                                                                                                                                                       |
| AddDiscountCode                                  | string string型, string discountCode                                                                                                                                                | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートに割引コードを追加します。                                                                                                                                                                                          |
| RemoveDiscountCodes                              | string id, IEnumerable\<string\> discountCodes                                                                                                                            | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートから割引コードを削除します。                                                                                                                                                                                     |
| RemoveCartLines                                  | string id, System.Collections.Generic.- IEnumerable\<string\> cartLineIds                                                                                                   | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートの明細行を削除します。                                                                                                                                                                                             |
| 検索                                           | CartSearchCriteria cartSearchCriteria, QueryResultSettings queryResultSettings                                                                                                | PageResult\<Cart\>                    | 顧客                 | カートを顧客別に取得します。                                                                                                                                                                                         |
| GetCardPayment- AcceptPoint                        | string string型, CardPaymentAcceptSettings cardPaymentAcceptSettings                                                                                                                | CardPaymentAcceptPoint                    | 従業員、顧客、匿名、アプリケーション               | Webページなど、カード支払いの受付ポイントを取得します。                                                                                                                                                          |
| RetrieveCardPayment- AcceptResult                  | resultAccessCode string型                                                                                                                                                       | CardPayment- AcceptResult                   | 従業員、顧客、匿名、アプリケーション               | 支払承認、カード トークンなど、カード支払の受理結果を取得します。                                                                                                                             |
| AddCoupons                                       | string id, IEnumerable\<string\> couponCodes, bool? isLegacyDiscountCode = false                                                                                          | カート                                      | 従業員、顧客、匿名、アプリケーション               | クーポンをカートに追加します。                                                                                                                                                                                            |
| RemoveCoupons                                    | string id, IEnumerable\<string\> couponCodes                                                                                                                              | カート                                      | 従業員、顧客、匿名、アプリケーション               | カートからクーポンコードを削除します。                                                                                                                                                                                  |
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
| GetNotifications         | IEnumerable\<int\> subscribedOperations, QueryResultSettings queryResultSettings | ICollection\<NotificationItem\> | 従業員                 | 通知を取得します。    |
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
| GetSearchSuggestions   | SearchSuggestionCriteria suggestionCriteria, QueryResultSettings 設定 | PageResult\<SearchSuggestion\> | 従業員、顧客、匿名、アプリケーション               | 検索候補を取得します。                            |
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
| GetByIds                          | long channelId, IEnumerable\<long\> productIds, QueryResultSettings queryResultSettings                                                                                                                                                                                 | PageResult\<SimpleProduct\>            | 従業員、顧客、匿名、アプリケーション               | チャンネルIDとレコードIDに基づいて製品群を取得します。                                                          |
| GetRecommendedProducts            | IEnumerable\<long\> productIds, string customerAccountNumber, QueryResultSettings queryResultSettings                                                                                                                                                                   | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション              | 一群のプロダクトIDが指定して、推奨されたSimpleProduct群を取得します。                    |
| 比較                           | long channelId, long catalogId, IEnumerable\<long\> productIds, QueryResultSettings queryResultSettings                                                                                                                                                                 | PageResult- \<ProductComparisonLine\>    | 従業員、顧客、匿名、アプリケーション              | 製品を比較します。                                                                                                                        |
| SearchByCategory                  | channelId long型, catalogId long型, categoryId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                    | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション              | カテゴリに属している製品を直接、またはその子カテゴリを介して検索します。                                                     |
| SearchByText                      | channelId long型, catalogId long型, searchText string型, QueryResultSettings queryResultSettings                                                                                                                                                                                  | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション               | 指定した検索テキストに関連付けられた製品を検索します。                                                                       |
| GetSearchSuggestions              | channelId long型, catalogId long型, searchText string型, hitPrefix string型, hitSuffix string型, QueryResultSettings queryResultSettings                                                                                                                                              | PageResult- \<SearchSuggestion\>         | 従業員、顧客、匿名、アプリケーション               | (部分的な) 検索テキストに基づいて推奨される検索語句を取得します。                                                                         |
| GetRefinersByCategory             | catalogId long型, categoryId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                                    | PageResult- \<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | 指定されたカテゴリ製品で使用できる製品の絞り込み条件を取得します。                                                                  |
| GetRefinersByText                 | catalogId long型, searchText string型, QueryResultSettings queryResultSettings                                                                                                                                                                                                  | PageResult- \<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | 指定されたテキストを検索した結果、製品で使用可能なプロダクトリファイナーを取得します。                                             |
| GetProductSearchRefiners          | ProductSearchCriteria searchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                               | PageResult- \<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | 使用されている絞り込み条件と検索テキスト/カテゴリIDの組み合わせから得られる結果から、製品で使用できる製品の絞り込み条件を取得します。 |
| GetRefinerValuesByCategory        | catalogId long型, categoryId long型, refinerId long型, refinerSourceValue int型, QueryResultSettings queryResultSettings                                                                                                                                                            | PageResult- \<ProductRefinerValue\>      | 従業員、顧客、匿名、アプリケーション              | 指定されたカテゴリ製品で使用できる製品の絞り込み条件を取得します。                                                            |
| GetRefinerValuesByText            | catalogId long型, searchText string型, refinerId long型, refinerSourceValue int型, QueryResultSettings queryResultSettings                                                                                                                                                          | PageResult- \<ProductRefinerValue\>      | 従業員、顧客、匿名、アプリケーション               | 指定されたテキストを検索した結果、製品で使用可能なプロダクトリファイナーの値を取得します。                                       |
| RefineSearchByCategory            | long channelId, long catalogId, long categoryId, IEnumerable- \<ProductRefinerValue\> refinementCriteria, QueryResultSettings queryResultSettings                                                                                                                         | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション              | カテゴリに属している製品を直接、またはその子カテゴリを介して検索します。                                    |
| RefineSearchByText                | long channelId, long catalogId, string searchText, IEnumerable- \<ProductRefinerValue\> refinementCriteria, QueryResultSettings queryResultSettings                                                                                                                       | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション               | 指定された検索テキストに関連する製品に対して実行される検索を絞り込みます。                                                      |
| GetDimensionValues                | long recordId, long channelId, int dimension, IEnumerable\<ProductDimension\> matchingDimensionValues, QueryResultSettings queryResultSettings                                                                                                                          | PageResult- \<ProductDimensionValue\>    | 従業員、顧客、匿名、アプリケーション               | 指定された要件に基づいて製品のディメンション値を取得します。                                                              |
| GetVariantsBy- DimensionValues      | long recordId, long channelId, IEnumerable\<ProductDimension\> matchingDimensionValues, QueryResultSettings queryResultSettings                                                                                                                                         | PageResult\<SimpleProduct\>            | 従業員、顧客、匿名、アプリケーション               | 指定した要件に基づいて製品のバリエーションを取得します。                                                                     |
| GetVariantsBy- ComponentsInSlots    | long recordId, long channelId, IEnumerable- \<ComponentInSlotRelation\> matchingSlotTo- ComponentRelationship, QueryResultSettings queryResultSettings                                                                                                                      | PageResult\<SimpleProduct\>            | 従業員、顧客、匿名、アプリケーション               | 指定したスロットの組み合わせのコンポーネントに基づいて、製品のバリエーションを取得します。                                                    |
| GetDefaultComponents              | recordId long型, channelId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                                      | PageResult- \<ProductComponent\>         | 従業員、顧客、匿名、アプリケーション               | 指定したプロダクトを構成する既定の個々のパーツを取得します。                                                                  |
| GetComponentByProduct- SlotRelation | channelId long型, ComponentInSlotRelation componentRelation                                                                                                                                                                                                                   | ProductComponent                           | 従業員、顧客、匿名、アプリケーション               | 指定されたComponentIn-SlotRelationに基づいて特定の製品コンポーネントを取得します                                                  |
| GetSlotComponents                 | recordId long型, channelId long型, slotId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                         | PageResult- \<ProductComponent\>         | 従業員、顧客、匿名、アプリケーション               | プロダクトの構成を完了するためにプロダクトのスロットに適合する既定のの個別パーツを取得します。                                     |
| GetFiltered- SlotComponents         | long recordId, long channelId, long slotId, IEnumerable- \<ComponentInSlotRelation\> selectedComponents, QueryResultSettings queryResultSettings                                                                                                                          | PageResult- \<ProductComponent\>         | 従業員、顧客、匿名、アプリケーション               | 以前に選択した一連のコンポーネントで選択可能な製品コンポーネントを取得します。                                           |
| GetAttributeValues                | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult\<AttributeValue\>           | 従業員、顧客、匿名、アプリケーション              | 指定された製品の属性値を取得します。                                                                                       |
| GetRelationTypes                  | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult- \<ProductRelationType\>      | 従業員、顧客、匿名、アプリケーション               | 指定した製品と他の製品との関係の種別を取得します。                                                            |
| GetRelatedProducts                | recordId long型, channelId long型, catalogId long型, relationTypeId long型, QueryResultSettings queryResultSettings                                                                                                                                                                 | PageResult- \<ProductSearchResult\>      | 従業員、顧客、匿名、アプリケーション               | 指定した関係によって指定した製品に関連付けられている製品を検索します。                                         |
| GetRefiners                       | ProductSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                        | PageResult\<ProductRefiner\>           | 従業員、顧客、匿名、アプリケーション               | ODataクエリを使用して製品リファイナーを検索します。                                                                                          |
| 変更                           | ChangedProductsSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                | IEnumerable\<Product\>                 | 従業員、店舗                | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| ReadChangedProducts               | ChangedProductsSearchCriteria productSearchCriteria, QueryResultSettings queryResultSettings                                                                                                                                                                                | PageResult\<Product\>                  | 応募              | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| GetDeletedListings                | catalogId long型, skip long型, top long型                                                                                                                                                                                                                                         | DeletedListingsResult                      | 応募              | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| GetDeletedCatalogs                | QueryResultSettings queryResultSettings                                                                                                                                                                                                                                     | IEnumerable\<long\>                    | 応募              | 削除されたカタログを取得します。                                                                                                                    |
| GetDeletedLanguages               | QueryResultSettings queryResultSettings                                                                                                                                                                                                                                     | IEnumerable\<string\>                  | 応募              | 削除された言語を取得します。                                                                                                                   |
| DeleteListingsBy- Catalogs          | IEnumerable\<long\> catalogIds                                                                                                                                                                                                                                          | 無効                                       | 応募              | カタログごとの一覧を削除します。                                                                                                             |
| DeleteListingsBy- Languages         | IEnumerable\<string\> languages                                                                                                                                                                                                                                         | 無効                                       | 応募              | 言語別の一覧を削除します。                                                                                                            |
| BeginRead- ChangedProducts          | ChangedProductsSearchCriteria changedProductSearchCriteria                                                                                                                                                                                                                  | ReadChanged- ProductsSession                 | 応募              | 変更された製品を読み取るセッションを開始します。                                                                                                  |
| EndReadChangedProducts            | ReadChangedProductsSession セッション                                                                                                                                                                                                                                          | 無効                                       | 応募              | 変更された製品を読み取るセッションを終了します。                                                                                                    |
| UpdateListing- PublishingStatus     | IEnumerable\<ListingPublishStatus\> publishingStatuses                                                                                                                                                                                                                  | 無効                                       | 応募              | 指定されたクエリ条件で、変更された製品を検索して取得します。                                                               |
| GetProductAvailabilities          | IEnumerable\<long\> itemIds, long channelId, QueryResultSettings queryResultSettings                                                                                                                                                                                    | PageResult- \<ProductAvailableQuantity\> | 従業員、顧客、匿名、アプリケーション               | 指定したチャネルおよび顧客の指定した品目リストの有効な在庫を取得します。                                                           |
| GetPrices                         | itemId string型, inventoryDimensionId string型, barcode string型, customerAccountNumber string型, unitOfMeasureSymbol string型, quantity decimal型, QueryResultSettings queryResultSettings                                                                                             | PageResult\<ProductPrice\>             | 従業員                 | 現在の顧客に関連する品目の価格を取得します。                                                                             |
| GetPrice                          | recordId long型, customerAccountNumber string型, unitOfMeasureSymbol string型                                                                                                                                                                                                     | ProductPrice                               | 従業員、顧客、匿名、アプリケーション               | 現在の顧客に関連する製品の価格を取得します。                                                                           |
| CalculateProductPrice             | long recordId, string customerAccountNumber, string unitOfMeasureSymbol, string loyaltyCardId, IEnumerable\<AffiliationLoyaltyTier\> affiliationLoyaltyTiers                                                                                                            | ProductPrice                               | 従業員、顧客、匿名、アプリケーション               | 価格を取得します。                                                                                                                           |
| GetActivePrices                   | ProjectionDomain projectDomain, IEnumerable\<long\> productIds, DateTimeOffset activeDate, string customerId, IEnumerable\<AffiliationLoyaltyTier\> affiliationLoyaltyTiers, bool? includeSimpleDiscountsIn- ContextualPrice, QueryResultSettings queryResultSettings | PageResult\<ProductPrice\>             | 従業員、顧客、匿名、アプリケーション               | 価格を取得します。                                                                                                                           |
| GetMediaLocations                 | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult\<MediaLocation\>            | 従業員、顧客、匿名、アプリケーション               | 指定した製品のメディアの場所を取得します。                                                                                       |
| GetMediaBlobs                     | recordId long型, channelId long型, catalogId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                      | PageResult\<MediaBlob\>                | 従業員、顧客、匿名、アプリケーション               | 指定された製品のメディアブロブを取得します。                                                                                           |
| GetUnitsOfMeasure                 | recordId long型, QueryResultSettings queryResultSettings                                                                                                                                                                                                                      | PageResult\<UnitOfMeasure\>            | 従業員、顧客、匿名、アプリケーション               | 指定した製品の測定単位を取得します。                                                                                    |
| GetChannel- ProductAttributes       | QueryResultSettings queryResultSettings                                                                                                                                                                                                                                     | PageResult\<AttributeProduct\>         | 従業員、顧客、匿名、アプリケーション               | チャネル製品属性を取得します。                                                                                                      |
| GetProductRatings                 | IEnumerable\<long\> productIds, QueryResultSettings 設定                                                                                                                                                                                                            | PageResult\<ProductRating\>            | 従業員、顧客、匿名、アプリケーション              | 製品識別子に基づく製品評価を取得します。                                                                        |
| GetEstimatedAvailability                            | InventoryAvailabilitySearchCriteria searchCriteria                                                                                                                                                                                        | ProductWarehouseInventoryInformation  | 従業員、顧客、匿名、アプリケーション               | 検索基準に基づいて、製品の在庫状況を予測します。                                                                                               |
| GetEstimatedProductWarehouseAvailability                            | InventoryAvailabilitySearchCriteria searchCriteria                                                                                                                                                                                        | IEnumerable\<ProductWarehouse\>                 | 従業員、顧客、匿名、アプリケーション               | 特定の製品倉庫のペアに対して、予想される製品の在庫状況を取得します。                                                                                               |

## <a name="product-lists-controller"></a>製品リストのコントローラー

| API                        | パラメーター                               | 戻り値                             | 対応している商取引上の役割 | 説明                                   |
|----------------------------|-----------------------------------------|------------------------------------------|--------------------------|-----------------------------------------------|
| 検索     | ProductListSearchCriteria productListSearchCriteria、QueryResultSettings queryResultSettings               | PagedResult\<ProductList\>                          | 従業員、顧客、匿名                 | 検索基準でフィルター処理された製品リストを取得します。                  |
| AddProductListLines | 文字列 productListId、IEnumerable\<ProductListLine\> productListLines | PagedResult\<ProductListLine\> | 従業員、顧客、匿名                 | 製品リストの製品リスト明細行を作成します。 |
| UpdateProductListLines | 文字列 productListId、IEnumerable\<ProductListLine\> productListLines | PageResult\<ProductListLine\> | 従業員、顧客、匿名                 | 製品リスト明細行を更新します。 |
| GetProductListLines | 文字列 productListId,、文字列 searchText、QueryResultSettings queryResultSettings | PagedResult\<ProductListLine\> | 従業員、顧客、匿名            | 製品リスト明細行を取得します。 |
| RemoveProductListLines | 文字列 productListId、IEnumerable\<ProductListLine\> 明細行| NullResponse | 従業員、顧客、匿名                 | 製品リストから明細行を削除します。 |
| CopyCartToProductList | 文字列 cartId、文字列 destinationProductListId、bool isRewrite、bool isQuantityAggregate | ProductList | 従業員、顧客                 | 製品リスト明細行にカートの内容をコピーします。 |
| GetEntityByKey | 文字列 productListId    | ProductList  | 従業員、顧客                 | ID 別の 1 つの製品リストを取得します。 |
| CreateEntity   | ProductList productList | ProductList  | 従業員、顧客                 | 製品リストを作成します。 |
| PatchEntity    | ProductList productList | ProductList  | 従業員、顧客                 | 製品リストプロパティを更新します。 部分的な更新に使用されます。|
| UpdateEntity   | ProductList productList | ProductList  | 従業員、顧客                 | 製品リストプロパティを更新します。 部分的な更新に使用されます。 |
| DeleteEntity   | 文字列 productListId    | NullResponse | 従業員、顧客                | 製品リストを削除します。 |

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
| GetFulfillmentPickingLists     | IEnumerable\<FulfillmentLineParameter\> pickingListFulfillmentLines, string hardwareProfileId, QueryResultSettings queryResultSettings | IEnumerable\<Receipt\>         | 従業員                 | ピッキング リストを取得する。                                                    |
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

## <a name="transfer-order-controller"></a>オーダーコントローラーの転送

| API                      | パラメーター                                                                                                        | 戻り値                           | 対応している商取引上の役割 | 説明                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------|----------------------------------------|--------------------------|-------------------------------------------------------------------|
| 取得                      | QueryResultSettings queryResultSettings                                                                          | PageResult&lt;transferorder&gt;        | 従業員                 | 店舗のオープン移動オーダーを取得します。                          |
| 確定                   | 文字列 orderId                                                                                                   | 無効                                   | 従業員                 | 移動オーダーのコミット                                         |
| GetTransferOrderJournals | 文字列 orderId, QueryResultSettings queryResultSettings                                                          | PageResult&lt;TransferOrderJournal&gt; | 従業員                 | 指定された移動オーダーの移動オーダー帳を取得します。 |
| GetTransferOrderLines    | 文字列 orderId, QueryResultSettings queryResultSettings                                                          | PageResult&lt;TransferOrderLine&gt;    | 従業員                 | 移動オーダーの明細行を取得します。                                    |
| CreateTransferOrderLines | 文字列 orderId、IEnumerable&lt;TransferOrderLine&gt; transferOrderLines、QueryResultSettings queryResultSettings | PageResult&lt;TransferOrderLine&gt;    | 従業員                 | 移動オーダーの明細行を作成します。                                 |
| UpdateTransferOrderLines | 文字列 orderId、IEnumerable&lt;TransferOrderLine&gt; transferOrderLines、QueryResultSettings queryResultSettings | PageResult&lt;TransferOrderLine&gt;    | 従業員                 | 移動オーダーの明細行を転記します。                                 |
| DeleteTransferOrderLines | 文字列 orderId、IEnumerable&lt;TransferOrderLine&gt; transferOrderLines、QueryResultSettings queryResultSettings | PageResult&lt;TransferOrderLine&gt;    | 従業員                 | 移動オーダーの明細行を削除します。                                 |
| GetTransferOrderComments | 文字列 orderId, QueryResultSettings queryResultSettings                                                          | PageResult&lt;Comment&gt;              | 従業員                 | 指定された移動オーダーのコメントを取得します。                |
| AddTransferOrderComment  | 文字列 orderId、文字列 commentedBy、文字列 comment                                                               | コメント                                | 従業員                 | 指定された移動オーダーのコメントを取得します。                |
| GetTransferPackingSlip   | 文字列 orderId、文字列 voucherId、ReceiptRetrievalCriteria 基準、QueryResultSettings queryResultSettings     | PageResult&lt;Receipt&gt;              | 従業員                 | 指定の移動オーダー帳の梱包明細を取得します。   |
| PatchEntity              | TransferOrder エンティティ                                                                                             | TransferOrder                          | 従業員                 | ローカルデータベースに移動オーダーを保存します。                     |
| GetEntityByKey           | 文字列 orderId                                                                                                   | TransferOrder                          | 従業員                 | オーダー識別子で移動オーダーを取得します。                        |
| DeleteEntity             | TransferOrder エンティティ                                                                                             | 無効                                   | 従業員                 | 指定の移動オーダーを削除します。                             |
| CreateEntity             | TransferOrder エンティティ                                                                                             | TransferOrder                          | 従業員                 | 移動オーダーを作成します。                                           |

## <a name="purchase-order-controller"></a>オーダー コントローラーの購入

| API            | パラメーター                               | 戻り値                    | 対応している商取引上の役割 | 説明                                   |
|----------------|-----------------------------------------|---------------------------------|--------------------------|-----------------------------------------------|
| 取得            | QueryResultSettings queryResultSettings | PageResult&lt;PurchaseOrder&gt; | 従業員                 | 店舗のオープンな発注書を取得します。      |
| 確定         | 文字列 orderId                          | 無効                            | 従業員                 | 発注書をコミットします。                                         |
| PatchEntity    | PurchaseOrder エンティティ                    | PurchaseOrder                   | 従業員                 | ローカルデータベースに発注書を保存します。 |
| GetEntityByKey | 文字列 orderId                          | PurchaseOrder                   | 従業員                 | オーダー識別子で発注書を取得します。     |

## <a name="org-units-controller"></a>組織単位コントローラー

| API                                | パラメーター                                                                                                                                                                         | 戻り値                          | 対応している商取引上の役割                  | 説明                                                                                             |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------|
| 取得                                | QueryResultSettings queryResultSettings                                                                                                                                           | PageResult&lt;OrgUnit&gt;             | アプリケーション、従業員、顧客、匿名 | 組織を IQueryable として取得します。                                                                    |
| GetOrgUnitLocationsByArea          | SearchArea searchArea、QueryResultSettings queryResultSettings                                                                                                                    | PageResult&lt;OrgUnitLocation&gt;     | アプリケーション、従業員、顧客、匿名 | 定義された領域で店舗を検索します。                                                                         |
| SearchOrgUnitLocations             | OrgUnitLocationSearchCriteria orgUnitLocationSearchCriteria、QueryResultSettings queryResultSettings                                                                              | PageResult&lt;OrgUnitLocation&gt;     | アプリケーション、従業員、顧客、匿名 | 現在のフルフィルメントグループ内に指定されたフィルタ基準を持つ店舗を検索します。                          |
| GetAvailableInventory              | 文字列 itemId、文字列のバリエーション、文字列 barcode、QueryResultSettings queryResultSettings                                                                                          | PageResult&lt;OrgUnitAvailability&gt; | アプリケーション、従業員、顧客、匿名 | 品目 ID またはバーコードのすべての店舗で利用可能な在庫を取得します。                            |
| GetProductAvailability             | productId long型、QueryResultSettings queryResultSettings                                                                                                                           | PageResult&lt;OrgUnitAvailability&gt; | アプリケーション、従業員、顧客、匿名 | 製品のすべての店舗で利用可能な在庫を取得します。                                                |
| SearchProductAvailability          | productId long型、OrgUnitAvailabilitySearchCriteria orgUnitAvailabilitySearchCriteria、QueryResultSettings queryResultSettings                                                      | PageResult&lt;OrgUnitAvailability&gt; | アプリケーション、従業員、顧客、匿名 | 製品のすべての店舗で利用可能な在庫を検索します。                                             |
| GetAvailableInventoryNearby        | IEnumerable&lt;ItemUnit&gt; itemIds、SearchArea searchArea、QueryResultSettings queryResultSettings                                                                               | PageResult&lt;OrgUnitAvailability&gt; | アプリケーション、従業員、顧客、匿名 | 定義された検索領域で指定された品目の一覧に対して、利用可能な隣接する店舗の在庫を取得します。               |
| GetTillLayout                      | int? height, int? width                                                                                                                                                           | TillLayout                            | アプリケーション、従業員、顧客、匿名 | 単一のレジレイアウトを取得します。                                                                              |
| GetOrgUnitConfiguration            |                                                                                                                                                                                   | ChannelConfiguration                  | アプリケーション、従業員、顧客、匿名 | 現在の組織単位の構成を取得します。                                               |
| 検索                             | SearchStoreCriteria storeSearchCriteria、QueryResultSettings queryResultSettings                                                                                                  | PageResult&lt;OrgUnit&gt;             | アプリケーション、従業員、顧客、匿名 | 指定された検索クエリによって組織単位を検索します。                                               |
| GetTerminalInfo                    | 文字列 orgUnitNumber、int deviceType、QueryResultSettings queryResultSettings                                                                                                     | PageResult&lt;TerminalInfo&gt;        | Employee                                 | 店舗のターミナルおよびデバイスの関連情報データを復元します。                                |
| GetProductAvailabilityByDimensions | IEnumerable&lt;文字列&gt; inventLocationIds、productId long型、IEnumerable&lt;ProductDimensionCombination&gt; productDimensionCombinations、QueryResultSettings queryResultSettings | PageResult&lt;OrgUnitAvailability&gt; | アプリケーション、従業員、顧客、匿名 | 指定された各在庫場所で、指定された製品分析コードに基づいて、orgUnitの使用可能性を取得します。 |
| GetStoreHours                      | 文字列 storeNumber                                                                                                                                                                | StoreHours                            | アプリケーション、従業員、顧客、匿名 | 特定の店舗番号の店舗時間を復元します。                                                      |
| GetEntityByKey                     | 文字列 orgUnitNumber                                                                                                                                                              | OrgUnit                               | アプリケーション、従業員、顧客、匿名 | キーを使って組織エンティティを取得します。                                                                        |

## <a name="catalogs-controller"></a>カタログコントローラ

| API         | パラメーター                                                                | 戻り値                     | 対応している商取引上の役割                  | 説明                   |
|-------------|--------------------------------------------------------------------------|----------------------------------|-------------------------------------------|-------------------------------|
| GetCatalogs | channelId long型、bool activeOnly、QueryResultSettings queryResultSettings | PageResult&lt;ProductCatalog&gt; | アプリケーション、従業員、顧客、匿名 | OData クエリでカタログを取得します。 |

## <a name="categories-controller"></a>カテゴリコントローラ

| API           | パラメーター                                                                | 戻り値                        | 対応している商取引上の役割                  | 説明                                             |
|---------------|--------------------------------------------------------------------------|-------------------------------------|-------------------------------------------|---------------------------------------------------------|
| GetCategories | productId long型、QueryResultSettings queryResultSettings                  | PageResult&lt;カテゴリ&gt;          | アプリケーション、従業員、顧客、匿名 | OData クエリでカテゴリを取得します。                         |
| GetChildren   | channelId long型, categoryId long型, QueryResultSettings queryResultSettings | PageResult&lt;カテゴリ&gt;          | アプリケーション、従業員、匿名          | 指定されたチャネル ID およびカテゴリ ID でサブカテゴリを取得します。 |
| GetAttributes | categoryId long型、QueryResultSettings queryResultSettings                 | PageResult&lt;AttributeCategory&gt; | 応募                               | OData クエリでカテゴリの属性を取得します。             |
| 取得           | QueryResultSettings queryResultSettings                                  | PageResult&lt;カテゴリ&gt;          | アプリケーション、従業員、匿名          | カテゴリの完全なリストを IQueryable として取得します。             |

## <a name="appinfo-controller"></a>AppInfo コントローラ

| API                      | パラメーター         | 戻り値 | 対応している商取引上の役割 | 説明                                           |
|--------------------------|-------------------|--------------|--------------------------|-------------------------------------------------------|
| UpdateApplicationVersion | 文字列 appVersion | 無効         | 従業員                 | POS デバイスの現在のアプリケーションバージョンを更新します。 |

## <a name="attribute-controller"></a>属性コントローラ

| API                     | パラメーター                                                                                        | 戻り値                          | 対応している商取引上の役割 | 説明                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------|--------------------------|------------------------------------------------------------------|
| GetAttributeDefinitions | AttributeDefinitionCriteria attributeDefinitionCriteria、QueryResultSettings queryResultSettings | PageResult&lt;attributedefinition&gt; | 従業員                 | 属性グループ ID を使って属性定義を取得します。 |

## <a name="attribute-group-controller"></a>属性グループコントローラ

| API                          | パラメーター                                                                                                  | 戻り値                               | 対応している商取引上の役割 | 説明                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------|--------------------------|------------------------------------------------------------------------------------|
| GetAttributeGroupDefinitions | AttributeGroupDefinitionCriteria attributeGroupDefinitionCriteria、QueryResultSettings queryResultSettings | PageResult&lt;AttributeGroupDefinition&gt; | 従業員                 | 属性グループ ID のコレクションを使って属性グループ定義を取得します。 |

## <a name="audit-event-controller"></a>監査イベントコントローラ

| API                      | パラメーター             | 戻り値 | 対応している商取引上の役割                           | 説明                                |
|--------------------------|-----------------------|--------------|----------------------------------------------------|--------------------------------------------|
| RegisterAuditEvent       | AuditEvent auditEvent | 無効         | 従業員                                           | 監査イベントの保存操作を実行します。 |
| RegisterAndGetAuditEvent | AuditEvent auditEvent | AuditEvent   | 匿名、顧客、デバイス、従業員、アプリケーション | 監査イベントの保存操作を実行します。 |

## <a name="shifts-controller"></a>コントローラーのシフト

| API                         | パラメーター                                                                              | 戻り値                    | 対応している商取引上の役割 | 説明                                                |
|-----------------------------|----------------------------------------------------------------------------------------|---------------------------------|--------------------------|------------------------------------------------------------|
| GetShift                    | shiftId long型、文字列 terminalId                                                        | シフト                           | 従業員                 | シフト ID とターミナル ID でシフトを取得します。                |
| GetByStatus                 | int statusValue、QueryResultSettings queryResultSettings                               | PageResult&lt;シフト&gt;         | 従業員                 | ステータスによるシフトを取得します。                                 |
| GetByStatusFilterByUserRole | Int statusValue、bool filterByUserRole、QueryResultSettings queryResultSettings        | PageResult&lt;シフト&gt;         | 従業員                 | ステータスによるシフトを取得します。                                 |
| GetByRetrievalCriteria      | ShiftRetrievalCriteria shiftRetrievalCriteria、QueryResultSettings queryResultSettings | PageResult&lt;シフト&gt;         | 従業員                 | 取得条件によるシフトを取得します。                     |
| UpsertAndValidateShifts     | shiftId long型?、文字列 terminalId、IEnumerable&lt;シフト&gt; シフト                      | ブール                            | 従業員                 | 指定したシフトを挿入または更新し、それらを検証します。          |
| DeleteShifts                |                                                                                        | ブール                            | 従業員                 | シフトの削除はオンラインコンテキストではサポートされません。      |
| 営業時間                        |                                                                                        | シフト                           | 従業員                 | 新しいシフトを開きます。                                         |
| 精算                       | shiftId long型、文字列 terminalId、文字列 transactionId、bool forceClose                 | シフト                           | 従業員                 | 指定されたターミナルのシフトを閉じます。                   |
| BlindClose                  | shiftId long型、文字列 terminalId、文字列 transactionId、bool forceClose                 | シフト                           | 従業員                 | ブラインドがシフトをクローズします。                                      |
| ForceDelete                 | shiftId long型、文字列 terminalId、文字列 transactionId                                  | 無効                            | 従業員                 | Forcefully はシフトを削除します。 無効なシフトを削除するために使用します。 |
| 経歴                      | shiftId long型、文字列 terminalId、文字列 cashDrawer                                     | シフト                           | 従業員                 | シフトを再開します。                                           |
| 使用                         | shiftId long型、文字列 terminalId                                                        | シフト                           | 従業員                 | 既存のシフトを使用します。                                    |
| 中断                     | shiftId long型、文字列 terminalId、文字列 transactionId                                  | シフト                           | 従業員                 | シフトを中断します。                                          |
| PostShift                   | シフト シフト                                                                            | HttpResponseMessage             | 従業員                 | 新しいシフトを作成するPOST要求を処理します。                |
| PatchShift                  | shiftId long型、文字列 terminalId、Delta&lt;シフト&gt; delta                              | シフト                           | 従業員                 | 既存のシフトを更新するパッチ要求を処理します。          |
| GetXReport                  | shiftId long型、文字列 terminalId、文字列 transactionId、文字列 hardwareProfileId        | 受信                         | 従業員                 | X レポートの受領書を取得します。                                 |
| GetZReport                  | 文字列 transactionId、文字列 hardwareProfileId                                         | 受信                         | 従業員                 | Z レポートの受領書を取得します。                                 |
| ValidateCashDrawerLimit     | 文字列 shiftTerminalId、shiftId long 型                                                   | 無効                            | 従業員                 | 指定されたシフトのすべての中断中のカートを取得します。                  |
| GetSuspendedCartsByShift    | 文字列 shiftTerminalId、shiftId long型、QueryResultSettings queryResultSettings          | PageResult&lt;SuspendedCart&gt; | 従業員                 | 指定されたシフトの中断中のトランザクションを無効にします。          |
| VoidSuspendedCarts          | shiftId long型、文字列 shiftTerminalId                                                   | 無効                            | 従業員                 | 指定されたシフトの中断中のトランザクションを無効にします。          |

## <a name="async-service-controller"></a>Async サービスコントローラー

| API                        | パラメーター                                                     | 戻り値                      | 対応している商取引上の役割 | 説明                     |
|----------------------------|---------------------------------------------------------------|-----------------------------------|--------------------------|---------------------------------|
| GetDownloadInterval        | 文字列 dataStoreName                                          | 文字列                            | デバイス                   | ダウンロードの間隔を取得します。         |
| GetUploadInterval          | GetUploadInterval                                             | 文字列                            | デバイス                   | アップロードの間隔を取得します。           |
| GetTerminalDataStoreName   | 文字列 terminalId                                             | 文字列                            | デバイス                   | データストア名を取得します。           |
| GetDownloadLink            | 文字列 dataStoreName、downloadSessionId long型                  | 文字列                            | デバイス                   | ダウンロードリンクを取得します。             |
| GetDownloadSessions        | 文字列 dataStoreName、QueryResultSettings queryResultSettings | PageResult&lt;DownloadSession&gt; | デバイス                   | ダウンロード セッションを取得します。     |
| GetInitialDownloadSessions | 文字列 dataStoreName、QueryResultSettings queryResultSettings | PageResult&lt;DownloadSession&gt; | デバイス                   | 初期のダウンロード セッションを取得します。 |
| GetUploadJobDefinitions    | 文字列 dataStoreName、QueryResultSettings queryResultSettings | IEnumerable&lt;string型&gt;         | デバイス                   | ダウンロード セッションを取得します。     |
| UpdateDownloadSession      | DownloadSession downloadSession                               | ブール                              | デバイス                   | ダウンロード セッション状態を更新します。 |
| PostOfflineTransactions    | IEnumerable&lt;文字列&gt; offlineTransactionForMPOS           | ブール                              | デバイス                   | オフライン トランザクションを転記します。     |

## <a name="card-type-controller"></a>カードタイプ コントローラー

| API                          | パラメーター                               | 戻り値                   | 対応している商取引上の役割                  | 説明                                                           |
|------------------------------|-----------------------------------------|--------------------------------|-------------------------------------------|-----------------------------------------------------------------------|
| GetCardTypes                 | QueryResultSettings queryResultSettings | PageResult&lt;CardTypeInfo&gt; | アプリケーション、従業員、顧客、匿名 | カードタイプの一覧を返します。                                       |
| GetSupportedPaymentCardTypes | QueryResultSettings queryResultSettings | PageResult&lt;文字列&gt;       | アプリケーション、顧客、匿名                                 | 支払コネクタでサポートされている支払カードの一覧を返します。 |

## <a name="commission-sales-group-controller"></a>コミッション売上グループのコントローラー

| API                         | パラメーター                                                  | 戻り値                           | 対応している商取引上の役割 | 説明                                                                       |
|-----------------------------|------------------------------------------------------------|----------------------------------------|--------------------------|-----------------------------------------------------------------------------------|
| GetCommissionSalesGroups    | QueryResultSettings queryResultSettings                    | PageResult&lt;CommissionSalesGroup&gt; | 従業員                 | チャネルのコミッション売上グループのコレクションを取得します。                       |
| SearchCommissionSalesGroups | searchText string型, QueryResultSettings queryResultSettings | PageResult&lt;CommissionSalesGroup&gt; | 従業員                 | 指定された検索テキストについて、チャネルのコミッション売上グループを検索します。 |

## <a name="environment-configuration-controller"></a>環境の構成コントローラー

| API                         | パラメーター | 戻り値             | 対応している商取引上の役割         | 説明                                                                                                     |
|-----------------------------|-----------|--------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| GetEnvironmentConfiguration |           | EnvironmentConfiguration | 匿名、従業員、アプリケーション | 単体の環境構成を取得します。                                                                        |
| GetExtensionProfile         |           | ExtensionProfile         | 匿名、従業員、アプリケーション | 拡張機能パッケージをダウンロードし、Micro-Services と通信するために使用できる拡張機能プロファイルを取得します。 |

## <a name="extension-package-definition-controller"></a>拡張機能パッケージ定義コントローラ

| API                            | パラメーター                               | 戻り値                                  | 対応している商取引上の役割      | 説明                                        |
|--------------------------------|-----------------------------------------|-----------------------------------------------|-------------------------------|----------------------------------------------------|
| GetExtensionPackageDefinitions | QueryResultSettings queryResultSettings | IEnumerable&lt;ExtensionPackageDefinition&gt; | デバイス、従業員、アプリケーション | 構成されている拡張機能パッケージ定義を取得します。 |

## <a name="extensible-enumeration-package-definition-controller"></a>拡張可能な列挙型パッケージ定義コントローラ

| API                       | パラメーター                               | 戻り値                                      | 対応している商取引上の役割                                       | 説明                              |
|---------------------------|-----------------------------------------|---------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| GetExtensibleEnumerations | QueryResultSettings queryResultSettings | IEnumerable&lt;ExtensibleEnumerationContainer&gt; | デバイス、従業員、アプリケーション、匿名、顧客、店舗 | すべての拡張可能な列挙クラスを取得します。 |

## <a name="loyalty-card-controller"></a>ロイヤルティ カード コントローラー

| API                                                   | パラメーター                                                                                          | 戻り値                                 | 対応している商取引上の役割 | 説明                                                                       |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------|----------------------------------------------|--------------------------|-----------------------------------------------------------------------------------|
| IssueLoyaltyCard                                      | LoyaltyCard loyaltyCard                                                                            | LoyaltyCard                                  | 従業員、顧客       | 新しいロイヤルティ カードを発行します。                                                        |
| GetLoyaltyCard                                        | 文字列 cardNumber                                                                                  | LoyaltyCard                                  | 従業員、顧客       | ロイヤルティ カードを取得します。                                                              |
| GetCustomerLoyaltyCards                               | accountNumber  string型、QueryResultSettings queryResultSettings                                      | PageResult&lt;LoyaltyCard&gt;                | 従業員、顧客       | 顧客のロイヤルティカードを取得します。                                                  |
| GetLoyaltyCardTransactions                            | 文字列 cardNumber、文字列 rewardPointId、QueryResultSettings queryResultSettings                   | PageResult&lt;LoyaltyCardTransaction&gt;     | 従業員、顧客       | ロイヤルティ カード トランザクションを取得します。                                               |
| GetLoyaltyRewardPointActivityTimeline                 | 文字列 cardNumber、文字列 rewardPointId、QueryResultSettings queryResultSettings                   | PageResult&lt;LoyaltyRewardPointActivity&gt; | 従業員、顧客       | ロイヤルティカードの特典ポイントのタイムライン活動を取得します。                |
| GetLoyaltyRewardPointActivityTimelineForExpiredPoints | 文字列 cardNumber、文字列 rewardPointId、QueryResultSettings queryResultSettings                   | PageResult&lt;LoyaltyRewardPointActivity&gt; | 従業員、顧客       | ロイヤルティカードの特典ポイントの期限切れポイントのタイムライン活動を取得します。 |
| GetLoyaltyRewardPointsExpiringSoon                    | 文字列 cardNumber、文字列 rewardPointId、int daysToExpiry、QueryResultSettings queryResultSettings | PageResult&lt;LoyaltyRewardPointActivity&gt; | 従業員、顧客       | 有効期限が近づいたロイヤルティカードの特典ポイントを取得します。                |

## <a name="non-sales-transaction-tender-operations-controller"></a>販売以外のトランザクションの支払/入金操作コントローラ

| API                       | パラメーター                                                                                                    | 戻り値                          | 対応している商取引上の役割 | 説明                                                                                         |
|---------------------------|--------------------------------------------------------------------------------------------------------------|---------------------------------------|--------------------------|-----------------------------------------------------------------------------------------------------|
| GetNonSalesTransactions   | 文字列 shiftId、文字列 shiftTerminalId、int nonSalesTenderTypeValue、QueryResultSettings queryResultSettings | PageResult&lt;NonSalesTransaction&gt; | 従業員                 | 非販売の支払/入金操作の集計金額を取得します。                                           |
| CreateNonSalesTransaction | NonSalesTransaction nonSalesTransaction                                                                      | NonSalesTransaction                   | 従業員                 | 開始金額の申告、支払 / 入金の削除 / 釣銭入力などの工程のドロワータイプの保存を実行します。 |
| GetAffiliations           | QueryResultSettings queryResultSettings                                                                      | PageResult&lt;Affiliation&gt;         | 従業員                 | 所属を取得。                                                                                  |

## <a name="operations-controller"></a>工程コントローラー

| API                            | パラメーター                                                                                          | 戻り値                                  | 対応している商取引上の役割 | 説明                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------|-----------------------------------------------|--------------------------|------------------------------------------------------------------------------|
| GetOperationPermissionById     | Int operationId                                                                                    | OperationPermission                           | 従業員                 | 操作の ID を使用して、工程のアクセス許可を取得します。                     |
| GetOperationPermissions        | QueryResultSettings queryResultSettings                                                            | PageResult&lt;OperationPermission&gt;         | 従業員                 | 操作のアクセス許可のコレクションを返します。                               |
| SearchJournalTransactions      | TransactionSearchCriteria searchCriteria、QueryResultSettings queryResultSettings                  | PageResult&lt;Transaction&gt;                 | 従業員                 | 指定された検索条件に一致するトランザクションのコレクションを返します。 |
| GetInventoryAvailableToPromise | long productId、文字列 itemId、文字列 inventoryLocationId、QueryResultSettings queryResultSettings | PageResult&lt;InventoryAvailableToPromise&gt; | 従業員                 | 製品のすべての店舗で利用可能な在庫を取得します。                     |
| VoidSuspendedTransactions      | IEnumerable&lt;文字列&gt; suspendedCartIds                                                         | 無効                                          | 従業員                 | 特定のカート ID で指定された中断されたトランザクションを無効にします。                 |

## <a name="shift-reconciliation-lines-controller"></a>調整行コントローラーのシフト

| API                         | パラメーター                                                                                                                  | 戻り値                              | 対応している商取引上の役割 | 説明                                                                             |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|--------------------------|-----------------------------------------------------------------------------------------|
| GetShiftReconciliationLines | ShiftReconciliationLineRetrievalCriteria shiftReconciliationLineRetrievalCriteria、QueryResultSettings queryResultSettings | PageResult&lt;ShiftReconciliationLine&gt; | 従業員                 | ダウンロードの間隔を取得します。                                                                 |
| ReconcileLines              | IEnumerable&lt;ShiftReconciliationLine&gt; 行、文字列の説明                                                       | 無効                                      | 従業員                 | 行を調整します。                                                                   |
| UndoReconciliation          | IEnumerable&lt;ShiftReconciliationLine&gt; 行                                                                           | 無効                                      | 従業員                 | 渡された明細行で、いずれかのグループの一部になっているすべての明細行の整合性を解除します。 |

## <a name="stock-count-journal-controller"></a>在庫数履歴のコントローラ

| API                                | パラメーター                                                                                                         | 戻り値                                   | 対応している商取引上の役割 | 説明                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------|--------------------------|-----------------------------------------------------------------------------------------------------------|
| 取得                                | QueryResultSettings queryResultSettings                                                                           | PageResult&lt;StockCountJournal&gt;            | 従業員                 | StockCountJournal エンティティを IQueryable として取得します。                                                            |
| 同期                               | QueryResultSettings queryResultSettings                                                                           | PageResult&lt;StockCountJournal&gt;            | 従業員                 | AX からの在庫数仕訳帳を RetailServer DB へと同期して、DB から SC 履歴の現在のリストを取得します。 |
| SyncTransactions                   | 文字列 journalId、QueryResultSettings queryResultSettings                                                         | PageResult&lt;StockCountJournalTransaction&gt; | 従業員                 | AX からの在庫数仕訳帳を RetailServer へと同期して、履歴取引の現在のリストを取得します。  |
| RemoveJournal                      | 文字列 journalId                                                                                                  | 無効                                           | 従業員                 | 在庫数棚卸仕訳帳をローカルから削除します。                                                              |
| RemoveTransaction                  | 文字列 journalId、文字列 itemId、文字列 inventSizeId、文字列 inventColorId、文字列 inventStyleId、文字列 configId | 無効                                           | 従業員                 | 在庫数仕訳帳をローカルから削除します。                                                   |
| RemoveStockCountLineByLineId       | 文字列 journalId、stockCountLineId long型                                                                           | 無効                                           | 従業員                 | 在庫数明細行 ID によって、ローカルから在庫数仕訳帳トランザクションから削除します。                    |
| RemoveStockCountLineByProductRecId | 文字列 journalId、productRecId long型                                                                               | 無効                                           | 従業員                 | 製品 ID によって、ローカルから在庫数仕訳帳トランザクションから削除します。                             |
| 確定                             | 文字列 journalId                                                                                                  | 無効                                           | 従業員                 | 在庫仕訳帳トランザクションの一覧をに AX にコミットします。                                                     |
| GetEntityByKey                     | 文字列 journalId                                                                                                  | StockCountJournal                              | 従業員                 | 仕訳帳エンティティを作成します。                                                                                   |
| UpdateEntity                       | StockCountJournal エンティティ                                                                                          | StockCountJournal                              | 従業員                 | 仕訳帳エンティティを更新します。                                                                                   |
| PatchEntity                        | StockCountJournal エンティティ                                                                                          | StockCountJournal                              | 従業員                 | 仕訳帳エンティティを部分的に更新します。                                                                         |

## <a name="scan-result-controller"></a>結果コントローラのスキャン

| API            | パラメーター          | 戻り値 | 対応している商取引上の役割 | 説明                        |
|----------------|--------------------|--------------|--------------------------|------------------------------------|
| GetEntityByKey | 文字列 scannedText | ScanResult   | 従業員                 | キーにより ScanResult エンティティを取得します。 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
