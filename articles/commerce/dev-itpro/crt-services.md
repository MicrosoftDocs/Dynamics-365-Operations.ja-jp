---
title: Commerce Runtime (CRT) のサービス
description: このトピックでは、コマース チャネルおよび価格設定機能のコア ビジネス ロジックを含むライブラリである Commerce Runtime (CRT) サービスについて説明します。
author: mugunthanm
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-05-18
ms.dyn365.ops.version: AX 8.0, Retail July 2017 update
ms.openlocfilehash: 76ab8d8ac8e21ae90e79ba7f8f87d8e90f1b7f07
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937106"
---
# <a name="commerce-runtime-crt-services"></a>Commerce Runtime (CRT) のサービス

[!include [banner](../../includes/banner.md)]

Commerce Runtime (CRT) は、コマース チャネルおよび価格設定機能のコア ビジネス ロジックを含む、ポータブル .NET ライブラリの集合です。 ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。 Retail Modern POS またはクラウド POS は CRT を呼び出して、ビジネス ロジックの実行を要求します。 CRT は要求を処理し、販売時点管理に応答を送り返します。 POS はシン クライアントのようで、すべてのビジネス ロジックを CRT で実行する必要があります。

CRT サービスは、要求/応答のグループです。 POS で作業する際はいつでも、POS は Commerce Scale Unit に要求を送り、Commerce Scale Unit は CRT を呼び出します。 CRT は要求を処理し、応答を送り返します。

このトピックでは、ビジネス シナリオにカスタマイズ可能な重要な要求/応答の一部を示します。

CRT には、次の 3 つの主要なレイヤーがあります。

- サービス
- ワークフロー
- データ アクセス

ビジネス ロジックのすべての CRT カスタマイズがワークフローまたはデータ アクセス レイヤーのサービスで実行可能で、CRT が作業するに必要な他のコア レイヤーは、ランタイム、認証、およびデータ アクセスのマネージャーであり、これらのレイヤーのカスタマイズは避ける必要があります。

> [!NOTE]
> CRT のすべてのクラスの詳細情報は、RetailSDK\Documents\CommerceRuntimeMessages.chm にある Retail SDK を参照してください。

## <a name="overall-flow"></a>全体的な流れ

全体的なフローは次のようになります。

CRT サービス要求 \< \> 0 以上のワークフロー要求 \< \> 0 以上のデータ アクセス要求

たとえば、複数のワークフローおよびデータ アクセス要求が呼び出されて **販売注文の作成** サービス要求が実行されます。

## <a name="crt-services"></a>CRT サービス

各 CRT サービスには、1 つ以上の要求または応答が含まれています。 たとえば、CRT の顧客サービスには、顧客関連のすべての要求/応答が含まれています。 各要求または応答は、さまざまなフローで実行されます。

### <a name="default-crt-services"></a>既定の CRT サービス

CRT の多くのサービスは、チャネルおよび店舗運営の機能をサポートします。 独自のサービスを追加したり、既存のサービスを拡張することができます。 次の表では、さまざまなビジネス サービス用にカスタマイズする可能性があるサービスの一部について説明します。

各サービスの詳細については、以下のRetail ソフトウェア開発キット (SDK) の CRT 要求/応答 ドキュメントを参照してください。 …\\RetailSDK\\Code\\Documents\\CommerceRuntimeMessages.chm.

| サービス                    | 説明 |
|----------------------------|-------------|
| AddressService             | このサービスは、住所を確認し、市町村、市区郡、都道府県などの場所情報を取得します。 |
| BarcodeService             | このサービスは、マスクとバーコード タイプに基づいて、スキャンしたバーコードを処理し、バーコードから数量と価格を計算します。 |
| CartService                | このサービスは、トランザクションからカートを取得し、トランザクション テーブルから販売トランザクション サービスを取得します。 |
| ChargeService              | このサービスは、自動請求、諸費用価格、およびトランザクションの出荷費用を計算するロジックを実装します。 |
| CouponService              | このサービスは、検証およびクーポン関連の要求を更新します。 |
| CurrencyService            | このサービスは、為替レートに基づいて通貨を変換します。 |
| CustomerService            | このサービスには顧客の保存、購買履歴、顧客の取得および顧客残高などの、顧客に関連する操作が含まれています。 |
| 従業員サービス            | このサービスは、従業員関連の情報と店舗別の従業員を取得します。 |
| FormattingService          | このサービスは、数字、通貨、および日付の形式のロジックを実装します。 |
| GiftCardService            | このサービスは、ギフト カードの発行、残高の取得、値の付加などのギフト カードに関連する内部の活動に関する情報を提供します。 |
| LoyaltyService             | このサービスは、リピート顧客に報酬を与えるプログラムを実装します。 |
| NotificationService        | このサービスは、POS 通知サービスを管理します。 |
| PaymentService             | このサービスでは、オンライン ストアから支払サービスに接続し、クレジット カード認証を提供し、コンフィギュレーション済の支払処理を使用することができます。 また、支払いサービスを拡張して、サード パーティの支払いプロセッサを追加することもできます。 |
| ProductService             | このサービスは、製品関連およびバリアントに関連する情報を取得します。 |
| ProductsService            | このサービスは、製品およびバリアントに関連する情報を取得します。 |
| PricingService             | このサービスは、リアル タイムで品目の価格を取得します。 基準価格および任意の利用可能な割引に基づいて、価格が調整されます。 各小売業者の割引をカスタマイズすることができます。 |
| ProductAvailabilityService | このサービスは、販売可能な製品の数量を計算します。 |
| ReasonCodeService          | このサービスは、POS 操作またはワークフローに対して必要な理由コードを取得し計算します。 |
| ReceiptService             | このサービスは入庫の詳細を取得し、フォーマットします。 |
| RoundingService            | このサービスは、支払/入金タイプおよび店舗に基づいて、支払/入金金額を丸めます。 |
| SalesOrderService          | このサービスは、顧客のショッピング カートに基づいて、販売注文を作成します。 |
| SearchProductsService      | このサービスは、入力テキストに基づいて、製品を検索します。 |
| ShippingService            | このサービスは、送料を計算し、現在の注文の出荷オプションを決定します。 |
| StockCountService          | このサービスは在庫仕訳帳を作成し、コミット、および同期します。 |
| StoreOperationService      | このサービスは、保存と削除、支払/入金申告、および仕訳帳の検索など店舗関連の工程のサービスを管理します。 |
| TaxService                 | このサービスは、現在の注文に対する売上税を計算します。 提供された売上情報、またはサード パーティ売上税サービスからの売上税情報を使用できます。 |
| TotalingService            | このサービスは、販売トランザクションおよび販売明細行の合計を計算します。 |

拡張シナリオでは、CRT トリガーの追加、新しいサービスの作成、サービス クラス内の要求の上書きを行えます。 CRT 拡張パターンの拡張と理解する方法の詳細については [Commerce Runtime (CRT) の拡張機能](commerce-runtime-extensibility.md) を参照してください。

> [!NOTE]
> CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (Runtime.Workflow、Runtime.Services、Runtime.DataServices のクラスなど) を参照したり使用したりすることはできません。 これらのクラスには、下位互換性がありません。アップグレード中に拡張機能が無効になる可能性があります。 拡張では、Runtime.*.Messages、Runtime.Framework、Runtime.Data、Runtime.Entities の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。

### <a name="addressservice"></a>AddressService

住所サービスでは、さまざまな拡張シナリオに対する次の要求/応答をサポートしています。

| 要求                            | 目的                                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------------------|
| GetCountryRegionsServiceRequest    | この要求は、サポートされている国および地域の一覧を取得します。                         |
| GetStateProvincesServiceRequest    | この要求は、国または地域でサポートされている都道府県の一覧を取得します。 |
| GetCitiesServiceRequest            | この要求は、州または地域でサポートされている市町村の一覧を取得します。                |
| GetDistrictServiceRequest          | この要求は、サポートされている地域の一覧を取得します。                                     |
| GetZipCodesServiceRequest          | この要求は、サポートされている郵便番号の一覧を取得します。                                     |
| GetFromZipPostalCodeServiceRequest | この要求は、サポートされている郵便番号の一覧を取得します。                                           |
| GetAddressFormattingServiceRequest | この要求は、指定した国または地域の住所書式を取得します。                       |

### <a name="barcodeservice"></a>BarcodeService

| 要求                                  | 目的                                                                                          |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| ProcessMaskSegmentsServiceRequest        | この要求は、バーコード マスクのコンフィギュレーションに基づいて、バーコードを処理します。                     |
| GetBarcodeTypeServiceRequest             | この要求は、サポートされているバーコードのタイプを取得します。                                      |
| CalculateQuantityFromPriceServiceRequest | この要求により、価格と数量はスキャンまたは入力されたバーコードに基づいて計算されます。 |

### <a name="cartservice"></a>CartService

| 要求                                                     | 目的                                                                                                    |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| GetSalesTransactionsServiceRequest                          | この要求は、バックオフィスから販売トランザクションを取得します。                                          |
| GetCartServiceRequest                                       | この要求は、カート ID を使用して、販売トランザクション テーブルからカートを取得します。                          |
| CalculateSalesTransactionServiceRequest                     | この要求により、指定した計算モードに基づいて、各種販売トランザクションの合計が計算されます。     |
| CalculateEstimatedShippingAuthorizationAmountServiceRequest | この要求により、トランザクションでの見積配送承認金額が計算されます。                    |
| ConvertSalesTransactionToCartServiceRequest                 | この要求により、渡されるトランザクション ID に基づいて、販売トランザクションがカート トランザクションに変換されます。 |

### <a name="couponservice"></a>CouponService

| 要求                               | 目的                                                                                                              |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| UpdateCouponCodesOnCartServiceRequest | この要求は、カートで使用されているクーポンに基づいて、バックオフィス内のクーポン コードの状態を更新します。 |
| ValidateCouponCodesServiceRequest     | この要求は、トランザクションに入力されたクーポン コードを検証します。                                          |
| UpdateCouponUsageServiceRequest       | この要求は、トランザクションのクーポンの使用状況を更新します。                                                               |

### <a name="customerservice"></a>CustomerService

| 要求                                      | 目的                                                                  |
|----------------------------------------------|--------------------------------------------------------------------------|
| SaveCustomerServiceRequest                   | この要求は、POS から顧客を保存する場合に呼び出されます。            |
| GetCustomersServiceRequest                   | この要求は、選択した顧客の詳細を取得します。                         |
| CustomersSearchServiceRequest                | この要求は、POS から顧客の検索を行う場合に実行されます。         |
| GetCustomerGroupsServiceRequest              | この要求は、顧客グループの詳細を取得します。                            |
| InitiateLinkToExistingCustomerServiceRequest | この要求は、下位互換性のための内部要求です。          |
| FinalizeLinkToExistingCustomerServiceRequest | この要求は、下位互換性のための内部要求です。          |
| UnlinkFromExistingCustomerServiceRequest     | この要求は、下位互換性のための内部要求です。          |
| GetCustomerBalanceServiceRequest             | この要求は、顧客の勘定の残高を取得します。                 |
| GetOrderHistoryServiceRequest                | この要求は、顧客の注文履歴を取得します。                          |
| GetPurchaseHistoryServiceRequest             | この要求は、顧客の最近の購入履歴を取得します。        |
| CustomerSearchByFieldsServiceRequest         | この要求は、名前、電話番号などのフィールドを使用して顧客を検索するときに実行されます (ヒント検索)。 |
| GetCustomerSearchFieldsServiceRequest        | この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。      |

### <a name="pricingservice"></a>PricingService

| 要求                                   | 目的                                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| CalculatePricesServiceRequest             | この要求により、カートと検索画面に追加される各品目の価格が計算されます。                   |
| CalculateDiscountsServiceRequest          | この要求により、カートに追加する各品目の割引が計算されます。                                         |
| GetIndependentPriceDiscountServiceRequest | この要求により、価格チェック画面の各品目とその他の非トランザクション関連のフローの価格が計算されます。 |
| ValidateDiscountsServiceRequest           | この要求は従業員に基づいて、入力された割引を検証します。                                           |
| GetAllPeriodicDiscountsServiceRequest     | この要求は、コンフィギュレーションされたすべての期間割引を取得します。                                                     |
| GetDiscountCodesServiceRequest            | この要求は、コンフィギュレーションされたすべての割引コードを取得します。                                                         |

### <a name="productservice"></a>ProductService

| 要求                     | 目的                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProductSearchServiceRequest | この要求は、POS からの検索テキストに基づいて、製品リストを取得します。 (これは以前の要求です。 カスタマイズでは、新しい **SearchProductsServiceRequest** 要求を代わりに使用します。 |
| GetProductServiceRequest    | この要求は、製品 ID に基づいて製品を取得します。                                                                                                                               |
| GetProductRefinersRequest   | この要求は、製品のリファイナーの値を取得します。                                                                                                                                    |

### <a name="productsservice"></a>ProductsService

| 要求                          | 目的                                                                      |
|----------------------------------|------------------------------------------------------------------------------|
| GetProductsServiceRequest        | この要求は用意されている製品の ID に基づいて、製品を取得します。 |
| GetVariantProductsServiceRequest | この要求は、マスター タイプ製品の特定のバリエーションを取得します。               |

### <a name="reasoncodeservice"></a>ReasonCodeService

| 要求                                                             | 目的                                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| GetReasonCodesServiceRequest                                        | この要求は、ワークフローまたは POS 操作に対して必要な理由コードを取得します。                               |
| CalculateRequiredReasonCodesServiceRequest                          | この要求により、ワークフローまたは POS 操作に対して必要な理由コードが計算されます。                         |
| CalculateCartRequiredReasonCodesServiceRequest                      | この要求により、カート ワークフローに必要な理由コードが計算されます。                                     |
| CalculateDropAndDeclareTransactionRequiredReasonCodesServiceRequest | この要求により、ドロップおよび支払/入金申告トランザクションに必要な理由コードが計算されます。           |
| CalculateNonSalesTransactionRequiredReasonCodesServiceRequest       | この要求により、支払/入金申告などの販売以外のトランザクションに必要な理由コードが計算されます。 |
| GetReturnOrderReasonCodesServiceRequest                             | この要求は、返品トランザクションに対して必要な理由コードを取得します。                                      |
| ValidateReasonCodeLineForUpdateServiceRequest                       | この要求は、カート要求の保存中に追加された理由コード行を検証します。                   |

### <a name="receiptservice"></a>ReceiptService

| 要求                               | 目的                                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------------------|
| GetReceiptServiceRequest              | この要求はレシート タイプに基づいて、レシート タイプを取得しレシート データを生成します。     |
| GetCustomReceiptFieldServiceRequest   | この要求を上書きし、受領書に追加されるカスタムフィールドのカスタム ロジックを追加します。 |
| GetEmailReceiptServiceRequest         | この要求は、印刷と電子メールのシナリオで使用される書式設定された領収書を取得します。         |
| PopulateTaxSummaryIndiaServiceRequest | この要求は、インドのトランザクションの税集計を設定します。                                     |

### <a name="searchproductsservice"></a>SearchProductsService

| 要求                      | 目的                                                         |
|------------------------------|-----------------------------------------------------------------|
| SearchProductsServiceRequest | この要求は、POS から製品の検索を行う場合に実行されます。 |

### <a name="taxservice"></a>TaxService

| 要求                      | 目的                                                                                                                                                                                            |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CalculateTaxServiceRequest   | この要求により、トランザクションの税額が計算されます。                                                                                                                                                  |
| AssignTaxCodesServiceRequest | この要求により、税計算前にトランザクションの課税対象の品目に対して税コードが割り当てられます。 **CalculateTaxServiceRequest** 要求の既定の税計算ハンドラーはこのメッセージを使用します。 |
| PopulateTaxRatesRequest      | この要求は、取り消されたトランザクションの税率を設定します。 税明細行に対する税率情報は永続化されません。 このメッセージ ハンドラーは、情報を復元します。                            |

## <a name="workflow-layer"></a>ワークフロー レイヤー

サービス レイヤーの上は、ワークフロー レイヤーです。 ワークフローは、サービスとビジネス ロジックを共に業務プロセスを定義するコレクションです。 たとえば、顧客がカートに品目を追加すると、価格の取得、検証の実行、在庫数量の確認、出荷費用の計算、税計算、および割引計算をするためワークフローを使用できます。 既存のワークフローをカスタマイズすることも、新しいワークフローを作成することもできます。 ワークフローを使用して、業務プロセスの一部としてサードパーティ製システムに接続することもできます。

サービスと同じように、ワークフローは要求/応答パターンを使用します。 基本 CRT [要求](/dynamicsax-2012/appuser-itpro/request-class-microsoft-dynamics-commerce-runtime-messages) クラスから継承された要求オブジェクト。 基本 CRT [応答](/dynamicsax-2012/appuser-itpro/response-class-microsoft-dynamics-commerce-runtime-messages) クラスから継承された応答オブジェクト。 ワークフローには、[WorkflowRequestHandler<TRequest, TResponse>](/dynamicsax-2012/appuser-itpro/workflowrequesthandler-trequest-tresponse-class-microsoft-dynamics-commerce-runtime-workflow) クラスを拡張する要求ハンドラー クラスもあります。 ワークフローを作成するには、要求クラスおよび応答クラスを作成し、ワークフローのビジネス ロジックが含まれる要求ハンドラー クラスを作成します。

たとえば、現金払いトランザクションまたは顧客からの注文を作成する場合、注文が作成される前に、多くの異なるステップやワークフローが完了します。 注文プロセスでのワークフロー ステップの 1 つは、カート要求の保存です。 カート要求ワークフローの保存は、POS からカートに加えられる変更の保存を担当します。 たとえば、買い物カゴに品目を追加したり、数量を変更するなど POS で行う行為は、SaveCart を呼び出して POS とデータベースに変更を保存します。

### <a name="default-workflows-and-handlers"></a>既定のワークフローとハンドラー

次の表では、既定のワークフローの要求と応答の一覧を示します。 CRT サービスは、ワークフロー要求を呼び出し、POS で実行する操作に基づいて応答します。 ビジネス シナリオに従って、これらのワークフローの要求と応答のいずれかをカスタマイズできます。 

| 要求                           | ハンドラー                                 | 目的                                                                                                                    |
|-----------------------------------|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| AddOrderInvoiceToCartRequest      | AddOrderInvoiceToCartRequestHandler     | この要求により、請求書はカート行としてのカートに追加されます。                                                                  |
| AddOrRemoveDiscountCodesRequest   | AddOrRemoveDiscountCodesRequestHandler  | この要求により、割引コードはカートに追加またはカートから削除されます。                                                |
| CancelOrderRequest                | CancelOrderRequestHandler               | POS から注文をキャンセルすると、この要求が発生します。                                                           |
| CopyCartRequest                   | CopyCartRequestHandler                  | この要求は、指定されたカート タイプを含む同一のショッピング カートを作成します。                                          |
| GetAddressRequest                 | GetAddressRequestHandler                | この要求は、リストから住所を取得します。                                                                               |
| GetCardPaymentAcceptPointRequest  | GetCardPaymentAcceptPointRequestHandler | この要求は、カード支払の受諾ページを表示します。                                                                     |
| GetCartRequest                    | GetCartRequestHandler                   | この要求はカート検索基準に基づいて、ショッピング カートを取得します。                                                    |
| GetDiscountCodesRequest           | GetDiscountCodesRequestHandler          | この要求は、割引コードを取得します。                                                                                      |
| GetOrdersRequest                  | GetOrdersRequestHandler                 | この要求は、販売注文を取得します。                                                                                            |
| GetPromotionsRequest              | GetPromotionsRequestHandler             | この要求は、カートおよびカートの品目のプロモーション ラインと共にショッピング カートを取得します。                         |
| GetScanResultRequest              | GetScanResultRequestHandler             | この要求は、スキャンまたは入力した情報に基づいて、エンティティの詳細を取得します。                                      |
| GetSupportedCardTypesRequest      | GetSupportedCardTypesRequestHandler     | この要求は、指定された通貨に対してサポートされているカートのタイプを取得します。                                       |
| IssueOrAddToGiftCardRequest       | IssueOrAddToGiftCardRequestHandler      | この要求は、ギフト カードを発行またはギフト カードの残高に加算します。                                                          |
| PickAndPackOrderRequest           | PickAndPackOrderRequestHandler          | この要求は、顧客注文に対するピッキング リストの作成および梱包明細の作成の要求を表します。                |
| PickupAtStoreRequest              | PickupAtStoreRequestHandler             | この要求は、店舗での集荷の要求を表します。                                                                |
| RecalculateOrderRequest           | RecalculateOrderRequestHandler          | この要求は、注文ワークフローを再計算するための要求を表します。                                                      |
| RecallCustomerOrderRequest        | RecallCustomerOrderRequestHandler       | この要求は、販売注文を取得し、カートに変換します。                                                              |
| RecallSalesInvoiceRequest         | RecallSalesInvoiceRequestHandler        | この要求は、請求書を取得します。                                                                                                |
| ResumeCartRequest                 | ResumeCartRequestHandler                | この要求は、中断されたカートを再開するための要求を表します。                                                     |
| SaveCartLinesRequest              | SaveCartLinesRequestHandler             | この要求は、カート行での作成、更新、削除、または無効操作の要求を表します。                         |
| SaveCartRequest                   | SaveCartRequestHandler                  | この要求は、カートに影響を与える変更を POS で行うときに発生します。                                      |
| SaveCustomerOrderRequest          | SaveCustomerOrderRequestHandler         | この要求では、指定されたカート ID と支払カードの情報に基づいて、顧客注文を保存するための要求が開始されます。 |
| SaveReasonCodeLineRequest         | SaveReasonCodeLineRequestHandler        | この要求により、理由コードはカート行で追加または更新されます。                                                                           |
| SaveTenderLineRequest             | SaveTenderLineRequestHandler            | この要求により、指定されたショッピング カートに対して支払/入金の明細行が追加、削除、または更新されます。                                          |
| SaveVoidTransactionRequest        | SaveVoidTransactionRequestHandler       | この要求は、トランザクションを無効にします。                                                                                          |
| SubmitSalesTransactionRequest     | SubmitOrderRequestHandler               | この要求では、指定されたカート ID に基づいて、販売トランザクションを送信するための要求が開始されます。                         |
| SuspendCartRequest                | SuspendCartRequestHandler               | この要求は、カートを中断するための要求を表します。                                                                     |
| TransferCartRequest               | TransferCartRequestHandler              | この要求は、指定されたショッピング カートを転送します。                                                                        |
| UpdateCommissionSalesGroupRequest | UpdateCommissionSalesGroupHandler       | この要求により、カートまたはカート行の販売担当者を更新するための要求がカプセル化されます。                    |
| UploadOrderRequest                | UploadOrderRequestHandler               | この要求は、販売注文をアップロードします。                                                                                      |
| ValidateCartForCheckoutRequest    | ValidateCartForCheckoutRequestHandler   | この要求は、チェックアウトのカートを検証します。                                                                              |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]