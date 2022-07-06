---
title: 販売時点管理 (POS) API
description: この記事では、使用可能な POS API の一覧とそれらにアクセスする方法を示します。
author: mugunthanm
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-10-29
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: b85a783330b529843ef43abe230546171c74c170
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861897"
---
# <a name="point-of-sale-pos-apis"></a>販売時点管理 (POS) API
[!include [banner](../includes/banner.md)]

Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。 たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。 これを実現する API を使用できます。 これを行うには、作業を実行する API を呼び出す必要があります。 POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。

拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。 すべての POS API は、CRT や HWS のような要求/応答として公開されます。 

POS API は、3 つのさまざまなシナリオに分類されます。

- **消費** - 拡張機能のパブリック API を使用します。

- **拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。

- **作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。

API の多くは、拡張機能で消費できます。 たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。 消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。

> [!NOTE]
> すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。 拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。 拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。 

## <a name="how-to-consume-apis-in-your-extension"></a>拡張機能で API を使用する方法

拡張機能で Retail API を利用するには、次の手順を使用します。

1.  拡張機能ファイルで API をインポートします。

    たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。

    パターンは、"PosApi/Consume/Module name" からの {api name} のインポートです。
 
    ```typescript
    import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
    ```

2.  必要に応じて、クライアントのエンティティとプロキシ エンティティをインポートします。

    ```typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
    ```
3.  API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。

    ```typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
    ```
    
    たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。
 
    ```typescript
    let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

     attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

     attributeValue.TextValue = "Yes";

     let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

     let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

    new SaveAttributesOnCartClientRequest(attributeValues);

    result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
    ```

### <a name="samples-showing-how-to-access-apis"></a>API にアクセスする方法を示すサンプル

**現在の買い物カゴを取得**
```typescript
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```

**買い物カゴに追加された現在の顧客を取得**
```typescript
 // Gets the current customer.

 let result: Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>>;

 if (!ObjectExtensions.isNullOrUndefined(currentCart) && !ObjectExtensions.isNullOrUndefined(currentCart.CustomerId)) {

 let getCurrentCustomerClientRequest: GetCustomerClientRequest<GetCustomerClientResponse> =

 new GetCustomerClientRequest(currentCart.CustomerId);

 result = this.context.runtime.executeAsync<GetCustomerClientResponse>(getCurrentCustomerClientRequest);

 } else {

 result = Promise.resolve({ canceled: true, data: new GetCustomerClientResponse(null) });

}
```

**強制無効トランザクション**
```typescript
 // Force void tarnsaction.
 let forceVoidTransactionRequest: VoidTransactionOperationRequest<VoidTransactionOperationResponse> =

 new VoidTransactionOperationRequest<VoidTransactionOperationResponse>(false, this.context.logger.getNewCorrelationId());

 this.context.runtime.executeAsync(forceVoidTransactionRequest).then((value: ICancelableDataResult<VoidTransactionOperationResponse>) => {

 this.currentCart(JSON.stringify(value.data.cart));

 }).catch((err: any) => {

 this.currentCart(JSON.stringify(err));

 });
```

### <a name="cart"></a>カート

次の表に、買い物カゴに関連する機能を実行する公開済みの API の一覧を示します。

| POS API                                   | 説明                            | リリース                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| AddPreprocessedTenderLineToCartClientRequest    | 事前処理済の入金明細行を買い物カゴに追加します。   | 10.0.14  |
| AddTenderLineToCartClientRequest                | 入金明細行を買い物カゴに追加します。  | 10.0.14  |
| ConcludeTransactionClientRequest                | トランザクションを終了します。    | 10.0.14  |
| GetCurrentCartClientRequest                     | 現在の買い物カゴを取得します。   | 10.0.14  |
| GetKeyedInPriceClientRequest                    |  キー入力価格を取得します。                                      | 10.0.14  |
| GetPickupDateClientRequest                      |  集荷日を取得します。                                      | 10.0.14  |
| GetReasonCodeLinesClientRequest                 |  理由コードを取得します。                                      | 10.0.14  |
| GetReceiptEmailAddressClientRequest             |  受信電子メール アドレスを取得します。                                     | 10.0.14  |
| GetShippingDateClientRequest                    |  出荷日を取得します。                                      | 10.0.14  |
| RefreshCartClientRequest                        |  サーバーの買い物カゴ データを使用して、現在の買い物カゴを更新します。                                      | 10.0.14  |
| ResumeSuspendedCartClientRequest                | 渡された ID に基づいて中断されたトランザクションを再開します。                                       | 10.0.14  |
| SaveAttributesOnCartClientRequest               | 買い物カゴの属性を保存します。                                       | 10.0.14  |
| SaveAttributesOnCartLinesClientRequest          | 買い物カゴ内の明細行の属性を保存します。                                       | 10.0.14  |
| SaveExtensionPropertiesOnCartClientRequest      | 買い物カゴの拡張機能プロパティを保存します。                                        | 10.0.14  |
| SaveExtensionPropertiesOnCartLinesClientRequest | 買い物カゴ内の明細行の拡張機能プロパティを保存します。                                       | 10.0.14  |
| SaveReasonCodeLinesOnCartClientRequest          | 買い物カゴに理由コードの明細行を保存します。                                       | 10.0.14  |
| SaveReasonCodeLinesOnCartLinesClientRequest     |  買い物カゴの明細行に理由コードの明細行を保存します。                                      | 10.0.14  |
| SelectSalesLinesForPickUpClientRequest          |  出荷の販売明細行を選択します。                                      | 10.0.14  |
| SetCartAttributesClientRequest                  |   買い物カゴの属性を設定します。                                     | 10.0.14  |
| ShowChangeDueClientRequest                      |  期日の変更ダイアログを表示します。                                      | 10.0.14  |
| AddAffiliationOperationRequest                  |  買い物カゴへ所属を追加します。                                      | 10.0.14  |
| AddItemToCartOperationRequest                   |  買い物カゴへ品目を追加します。                                      | 10.0.14  |
| CalculateTotalOperationRequest                  |  買い物カゴの合計を計算します。                                      | 10.0.14  |
| ChangeCartLineUnitOfMeasureOperationRequest     |  買い物カゴ明細行の測定単位を変更します。                                      | 10.0.14  |
| CreateCustomerOrderOperationRequest             |   顧客注文を作成します。                                     | 10.0.14  |
| CreateCustomerQuoteOperationRequest             |   顧客見積を作成します。                                     | 10.0.14  |
| CustomerAccountDepositOperationRequest          |                                        | 10.0.14  |
| DepositOverrideOperationRequest                 |  預金額を上書きします。                                      | 10.0.14  |
| EditCustomerOrderOperationRequest               |   顧客注文を編集します。                                     | 10.0.14  |
| LineDiscountAmountOperationRequest              |  明細行割引金額を買い物カゴ明細行に追加します。                                      | 10.0.14  |
| LineDiscountPercentOperationRequest             |  明細行割引率を買い物カゴ明細行に追加します。                                      | 10.0.14  |
| OverrideLineTaxFromListOperationRequest         |  一覧から買い物カゴ明細行の税を上書きします。                                      | 10.0.14  |
| OverrideLineTaxOperationRequest                 |   買い物カゴ明細行の税を上書きします。                                     | 10.0.14  |
| OverrideTransactionTaxOperationRequest          |    取引税を上書きします。                                       | 10.0.14  |
| PickupAllOperationRequest                       |   注文をピックアップします。                                     | 10.0.14  |
| PriceOverrideOperationRequest                   | 買い物カゴ明細行の価格を上書きします。                                       | 10.0.14  |
| SetCartLineCommentOperationRequest              |  買い物カゴ明細行のコメントを設定します。                                      | 10.0.14  |
| SetCartLineQuantityOperationRequest             |   買い物カゴ明細行の数量を設定します。                                     | 10.0.14  |
| SetCustomerOnCartOperationRequest               |   買い物カゴの顧客を設定します。                                     | 10.0.14  |
| SetTransactionCommentOperationRequest           |   トランザクションのコメントを設定します。                                     | 10.0.14  |
| SuspendCurrentCartOperationRequest              | 現在のトランザクションを中断します。                                       | 10.0.14  |
| TotalDiscountAmountOperationRequest             |   トランザクションへ合計割引金額を追加します。                                     | 10.0.14  |
| TotalDiscountPercentOperationRequest            |  トランザクションへ合計割引率を追加します。                                         | 10.0.14  |
| VoidCartLineOperationRequest                    |  買い物カゴ明細行を無効にします。                                      | 10.0.14  |
| VoidTenderLineOperationRequest                  | 入金明細行を無効にします。                                       | 10.0.14  |
| VoidTransactionOperationRequest                 |  トランザクションを無効にします。                                      | 10.0.14  |
| CreateEmptyCartServiceRequest                   |  空の買い物カゴを作成します。                                      | 10.0.14  |
| GetTaxOverridesServiceRequest                   |  税の上書きの一覧を取得します。                                      | 10.0.14  |
| UpdateTenderLineSignatureServiceRequest         |  入金明細行の署名データを更新します。                                      | 10.0.14  |
| CarryoutSelectedProductsOperationRequest |   選択した明細行を実行としてマークします。                                            | 10.0.14  |
| AddCouponsOperationRequest |    トランザクションにクーポンを追加します。                                                         | 10.0.14  |
| CreateNonSalesTransactionServiceRequest | 販売以外のトランザクションの買い物カゴを作成します。                                               | 10.0.14  |
| ReturnTransactionOperationRequest |  トランザクションを返します。                                                    | 10.0.14  |
| AddLoyaltyCardToCartOperationRequest | ロイヤルティ カードをトランザクションに追加します。                                                  | 10.0.14  |
| ReturnCartLineOperationRequest |   買い物カゴ明細行を返します。                                                      | 10.0.14  |
| ReturnItemOperationRequest |  品目を返します。                                                           | 10.0.14  |
| AddExpenseAccountLineToCartOperationRequest | 経費勘定明細行を買い物カゴに追加します。                                           | 10.0.14  |
| ShipAllCartLinesOperationRequest |   買い物カゴのすべての明細行を出荷します。                                                    | 10.0.14  |
| ShipSelectedCartLinesOperationRequest |    買い物カゴの選択した明細行を出荷します。                                              | 10.0.14  |
|PickupSelectedOperationRequest | 含められた明細行を出荷対象としてマークする                      |  10.0.16 |


### <a name="payments"></a>支払利息

次の表に、支払に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                                   | 説明                            | リリース                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| GetGiftCardByIdServiceRequest             | ギフト カード ID を取得します。     |   10.0.12   |
| GetPaymentCardTypeByBinRangeClientRequest | カード タイプの BIN 範囲を取得します。  |  10.0.12     |
| GetSignatureClientRequest                 | 署名のキャプチャ ダイアログを POS で表示するか、またはコンフィギュレーションに基づいてメッセージを署名キャプチャ デバイスに送信します。 | 10.0.15 |

### <a name="peripherals"></a>周辺機器

次の表に、周辺機器に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                                                |
|--------------------------------------------------------|
| CardPaymentAuthorizePaymentRequest                     |
| CardPaymentBeginTransactionRequest                     |
| CardPaymentCapturePaymentRequest                       |
| CardPaymentEndTransactionRequest                       |
| CardPaymentEnquireGiftCardBalancePeripheralRequest     |
| CardPaymentExecuteTaskRequest                          |
| CardPaymentRefundPaymentRequest                        |
| CardPaymentVoidPaymentRequest                          |
| CardPaymentAuthorizeCardTokenPeripheralRequest                          |
| CashDrawerIsOpenRequest                                |
| HardwareStationDeviceActionRequest                     |
| HardwareStationStatusRequest                           |
| LineDisplayDisplayLinesRequest                         |
| PaymentTerminalAuthorizePaymentActivityRequest         |
| PaymentTerminalAuthorizePaymentRequest                 |
| PaymentTerminalBeginTransactionRequest                 |
| PaymentTerminalCancelOperationRequest                  |
| PaymentTerminalCapturePaymentRequest                   |
| PaymentTerminalEndTransactionRequest                   |
| PaymentTerminalEnquireGiftCardBalancePeripheralRequest |
| PaymentTerminalExecuteTaskRequest                      |
| PaymentTerminalRefundPaymentActivityRequest            |
| PaymentTerminalRefundPaymentRequest                    |
| PaymentTerminalUpdateLinesRequest                      |
| PaymentTerminalVoidPaymentRequest                      |
| PaymentTerminalFetchTokenPeripheralRequest             |
| PrinterPrintRequest                                    |
| ScaleReadRequest                                       |

### <a name="scanresults"></a>ScanResults

次の表に、スキャン結果に関連する機能を実行する公開済みの API の一覧を示します。

| POS API                    |
|----------------------------|
| GetScanResultClientRequest |

### <a name="customer"></a>顧客

次の表に、顧客に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                  |
|--------------------------|
| GetCustomerClientRequest |
|CreateCustomerServiceRequest |
|UpdateCustomerServiceRequest |
|SelectCustomerClientRequest |


### <a name="authentication"></a>認証

次の表に、承認に関連する機能を実行する公開済みの API の一覧を示します。

| POS API                |
|------------------------|
| LogOffOperationRequest |
| LockRegisterOperationRequest |

### <a name="dataservice"></a>DataService

次の表に、データ サービスに関連する機能を実行する公開済みの API の一覧を示します。

| POS API            |
|--------------------|
| DataServiceRequest |

### <a name="device"></a>デバイス

次の表に、デバイスに関連する機能を実行する公開済みの API の一覧を示します。

| POS API                               |
|---------------------------------------|
| GetDeviceConfigurationClientRequest   |
| GetExtensionProfileClientRequest      |
| GetHardwareProfileClientRequest       |
| GetAuthenticationTokenClientRequest   |
| GetConnectionStatusClientRequest      |
| GetActiveHardwareStationClientRequest |
| GetApplicationVersionClientRequest    |
| GetChannelConfigurationClientRequest  |

### <a name="diagnostics"></a>診断 

次の表に、診断に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                     |
|-----------------------------|
| GetSessionInfoClientRequest |

### <a name="dialog"></a>ダイアログ

次の表に、ダイアログに関連する機能を実行する公開済みの API の一覧を示します。

| POS API                                  |
|------------------------------------------|
| ShowMessageDialogClientRequest           |
| IAlphanumericInputDialogResult           |
| ShowAlphanumericInputDialogClientRequest |
| ShowNumericInputDialogClientRequest      |
| ShowListInputDialogClientRequest         |
| ShowTextInputDialogClientRequest         |

### <a name="employee"></a>従業員

次の表に、従業員に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                                   | 説明                            | リリース                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| GetLoggedOnEmployeeClientRequest |  現在 POS にログインしている従業員の詳細を取得します。      | 10.0.14      |
| SelectStoreEmployeeClientRequest | 現在の店舗の選択可能な従業員の一覧を取得します。 | 10.0.16 |

### <a name="formatters"></a>フォーマッター

次の表に、フォーマッターに関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                             |
|-------------------------------------|
| IBooleanFormatter                   |
| ICurrencyFormatter                  |
| IDateFormatter                      |
| ITransactionTypeFormatter           |
| IPurchaseTransferOrderTypeFormatter |

### <a name="orgunits"></a>OrgUnits

次の表に、組織単位に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                              |
|--------------------------------------|
| GetOrgUnitConfigurationClientRequest |
| GetOrgUnitTenderTypesClientRequest   |
| InventoryLookupOperationRequest      |

### <a name="products"></a>製品

次の表に、製品に関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                                    |
|--------------------------------------------|
| GetProductsByIdsClientRequest              |
| GetCurrentProductCatalogStoreClientRequest |
| SelectProductVariantClientRequest          |
| GetSerialNumberClientRequest               |
| GetRefinerValuesByTextServiceRequest       |
| SelectProductClientRequest |
| SelectProductVariantClientRequest |
| GetActivePricesServiceRequest |

### <a name="categories"></a>カテゴリ

次の表に、カテゴリに関連する機能を実行できる公開済みの API の一覧を示します。

| POS API                                    |
|--------------------------------------------|
| GetCategoriesServiceRequest              |


### <a name="salesorders"></a>SalesOrders

次の表に、販売注文に関連する機能を実行する公開済みの API の一覧を示します。

| POS API                                          |
|--------------------------------------------------|
| GetReceiptsClientRequest                         |
| RegisterPrintReceiptCopyEventRequest             |
| GetSalesOrderDetailsByTransactionIdClientRequest |
| GetGiftReceiptsClientRequest                     |
| RegisterPrintReceiptCopyEventRequest             |
| MarkAsPickedServiceRequest                       |
| PrintPackingSlipClientRequest                    |
| PickUpCustomerOrderLinesClientRequest            |


### <a name="shifts"></a>シフト

次の表に、シフトに関連する機能を実行する公開済みの API の一覧を示します。

| POS API                    |
|----------------------------|
| CloseShiftOperationRequest |
| CloseShiftOperationRequest |

### <a name="stockcountjournals"></a>StockCountJournals

次の表に、在庫数仕訳帳に関連する機能を実行する公開済みの API の一覧を示します。

| POS API                                |
|----------------------------------------|
| SyncAllStockCountJournalsClientRequest |

### <a name="storeoperations"></a>StoreOperations

次の表に、店舗運営に関連する機能を実行する公開済みの API の一覧を示します。

| POS API                                   | 説明                            | リリース                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| DeclareStartingAmountClientRequest              | この要求を使用して開始金額を申告します。 | 10.0.14        |
| GetSalesOrdersWithNoFiscalTransactionsRequest   | 会計トランザクション要求のない販売注文を取得します。  |   10.0.14        |
| RegisterCustomAuditEventClientRequest           | カスタム監査イベント要求を登録します。   |  10.0.14        |
| GetOfflinePendingTransactionCountClientRequest  | オフラインで保留中のトランザクション カウントを取得します。  | 10.0.14        |
| SaveFiscalTransactionClientRequest              | 会計トランザクション要求を保存します。   |   10.0.14        |
| SafeDropOperationRequest                        | 金庫保管操作要求。  |  10.0.14        |
| TenderDeclarationOperationRequest               | 入金申告操作要求。      |   10.0.14        |
| TenderRemovalOperationRequest                   | 入金削除操作要求。  |  10.0.14        |
| CreateBankDropTransactionClientRequest          | 銀行入金トランザクション要求。    | 10.0.14        |
| CreateFloatEntryTransactionClientRequest        | 釣銭入力トランザクション要求。 |  10.0.14        |
| CreateStartingAmountTransactionClientRequest    | 開始金額トランザクション要求を作成します。       |   10.0.14        |
| CreateTenderDeclarationTransactionClientRequest | 入金申告トランザクション要求を作成します。     |   10.0.14        |
| CreateTenderRemovalTransactionClientRequest     | 入金申告トランザクション要求を削除します。       |  10.0.14        |
| GetDenominationTotalsClientRequest              | 単位合計要求を取得します。        | 10.0.14        |
| SelectZipCodeInfoClientRequest                  | 郵便番号情報の要求を選択します。    | 10.0.14        |
| CreateSafeDropTransactionClientRequest          | 金庫保管トランザクション要求を作成します。                                       |  10.0.14        |
| GetTenderDetailsClientRequest                   | 入金の詳細を取得します。    | 10.0.14        |
| LoyaltyCardPointsBalanceOperationRequest        | ロイヤルティ カードの残高を取得します。  | 10.0.14        |
| GetCommissionSalesGroupsServiceRequest          | コミッション売上グループを取得します。  |  10.0.14        |
| GetCurrenciesServiceRequest                     | 店舗の通貨を取得します。 | 10.0.14        |
| GetSrsReportDataSetServiceRequest               | SRS レポート データを取得します。  |  10.0.14        |
| SearchCommissionSalesGroupsServiceRequest       |  コミッション売上グループの要求を検索します。   | 10.0.14        |
| IssueLoyaltyCardOperationRequest                |  ロイヤルティ カードを発行します。  |  10.0.14        |
| GetPickingAndReceivingOrdersClientRequest       |  ピッキングと入荷の注文リストを取得します。  |    10.0.14        |
| BankDropOperationRequest                 |  銀行入金要求。   |        10.0.14        |
| DeclareStartAmountOperationRequest        |   開始金額申告要求。       |          10.0.14        |
| GetAllDiscountsServiceRequest        | 現在の買い物カゴに適用できる割引を取得します。  | 10.0.16 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]