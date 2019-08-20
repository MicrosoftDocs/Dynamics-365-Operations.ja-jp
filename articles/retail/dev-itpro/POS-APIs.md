---
title: Retail POS API
description: このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。
author: mugunthanm
manager: AnnBe
ms.date: 05/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-29-10
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 1977c824fb71e5ceb2ec7d43ee2f19edccd82bc6
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833103"
---
# <a name="retail-pos-apis"></a>Retail POS API
[!include [banner](../includes/banner.md)]

Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。 たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。 これを実現する API を使用できます。 これを行うには、作業を実行する API を呼び出す必要があるだけです。 POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。

拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。 すべての POS API は、CRT や HWS のような要求/応答として公開されます。 このトピックでは、Dynamics 365 for Finance and Operations または Dynamics 365 for Retail 最新修正プログラムが適用されます。 

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
```Typescript
 import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
```

2.  必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。

```Typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
```
3.  API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。

```Typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
```

 たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。
```Typescript
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
```
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```
**買い物カゴに追加された現在の顧客を取得**
```
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
```
 // Force void tarnsaction.
```Typescript
 let forceVoidTransactionRequest: VoidTransactionOperationRequest<VoidTransactionOperationResponse> =

 new VoidTransactionOperationRequest<VoidTransactionOperationResponse>(false, this.context.logger.getNewCorrelationId());

 this.context.runtime.executeAsync(forceVoidTransactionRequest).then((value: ICancelableDataResult<VoidTransactionOperationResponse>) => {

 this.currentCart(JSON.stringify(value.data.cart));

 }).catch((err: any) => {

 this.currentCart(JSON.stringify(err));

 });
```

### <a name="cart"></a>カート

次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。

| POS API                                         |
|-------------------------------------------------|
| AddPreprocessedTenderLineToCartClientRequest    |
| AddTenderLineToCartClientRequest                |
| ConcludeTransactionClientRequest                |
| GetCurrentCartClientRequest                     |
| GetCurrentCartClientResponse                    |
| GetKeyedInPriceClientRequest                    |
| GetPickupDateClientRequest                      |
| GetReasonCodeLinesClientRequest                 |
| GetReceiptEmailAddressClientRequest             |
| GetShippingDateClientRequest                    |
| RefreshCartClientRequest                        |
| ResumeSuspendedCartClientRequest                |
| SaveAttributesOnCartClientRequest               |
| SaveAttributesOnCartLinesClientRequest          |
| SaveExtensionPropertiesOnCartClientRequest      |
| SaveExtensionPropertiesOnCartLinesClientRequest |
| SaveReasonCodeLinesOnCartClientRequest          |
| SaveReasonCodeLinesOnCartLinesClientRequest     |
| SelectSalesLinesForPickUpClientRequest          |
| SetCartAttributesClientRequest                  |
| ShowChangeDueClientRequest                      |
| AddAffiliationOperationRequest                  |
| AddItemToCartOperationRequest                   |
| CalculateTotalOperationRequest                  |
| ChangeCartLineUnitOfMeasureOperationRequest     |
| CreateCustomerOrderOperationRequest             |
| CreateCustomerQuoteOperationRequest             |
| CustomerAccountDepositOperationRequest          |
| DepositOverrideOperationRequest                 |
| EditCustomerOrderOperationRequest               |
| LineDiscountAmountOperationRequest              |
| LineDiscountPercentOperationRequest             |
| OverrideLineTaxFromListOperationRequest         |
| OverrideLineTaxOperationRequest                 |
| OverrideTransactionTaxOperationRequest          |
| PickupAllOperationRequest                       |
| PriceOverrideOperationRequest                   |
| SetCartLineCommentOperationRequest              |
| SetCartLineQuantityOperationRequest             |
| SetCustomerOnCartOperationRequest               |
| SetTransactionCommentOperationRequest           |
| SuspendCurrentCartOperationRequest              |
| TotalDiscountAmountOperationRequest             |
| TotalDiscountPercentOperationRequest            |
| VoidCartLineOperationRequest                    |
| VoidTenderLineOperationRequest                  |
| VoidTransactionOperationRequest                 |
| CreateEmptyCartServiceRequest                   |
| GetTaxOverridesServiceRequest                   |
| UpdateTenderLineSignatureServiceRequest         |
| CarryoutSelectedProductsOperationRequest |
| AddCouponsOperationRequest |
| CreateNonSalesTransactionServiceRequest |
| ReturnTransactionOperationRequest |
| AddLoyaltyCardToCartOperationRequest |

### <a name="payments"></a>支払

次に、支払に関連する機能を実行する公開されている API の一覧を示します。

| POS API                                   |
|-------------------------------------------|
| GetGiftCardByIdServiceRequest             |
| GetPaymentCardTypeByBinRangeClientRequest |

### <a name="peripherals"></a>周辺機器

次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。

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
| PrinterPrintRequest                                    |
| ScaleReadRequest                                       |

### <a name="scanresults"></a>ScanResults

次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。

| POS API                    |
|----------------------------|
| GetScanResultClientRequest |

### <a name="customer"></a>顧客

次に、顧客に関連する機能を実行する公開されている API の一覧を示します。

| POS API                  |
|--------------------------|
| GetCustomerClientRequest |
|CreateCustomerServiceRequest |
|UpdateCustomerServiceRequest |
|SelectCustomerClientRequest |


### <a name="authentication"></a>認証

次に、認証に関連する機能を実行する公開されている API の一覧を示します。

| POS API                |
|------------------------|
| LogOffOperationRequest |

### <a name="dataservice"></a>DataService

次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。

| POS API            |
|--------------------|
| DataServiceRequest |

### <a name="device"></a>デバイス

次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。

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

次に、診断に関連する機能を実行する公開されている API の一覧を示します。

| POS API                     |
|-----------------------------|
| GetSessionInfoClientRequest |

### <a name="dialog"></a>ダイアログ

次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。

| POS API                                  |
|------------------------------------------|
| ShowMessageDialogClientRequest           |
| IAlphanumericInputDialogResult           |
| ShowAlphanumericInputDialogClientRequest |
| ShowNumericInputDialogClientRequest      |
| ShowListInputDialogClientRequest         |
| ShowTextInputDialogClientRequest         |

### <a name="employee"></a>従業員

次に、従業員に関連する機能を実行する公開されている API の一覧を示します。

| POS API                          |
|----------------------------------|
| GetLoggedOnEmployeeClientRequest |

### <a name="formatters"></a>フォーマッター

次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。

| POS API                             |
|-------------------------------------|
| IBooleanFormatter                   |
| ICurrencyFormatter                  |
| IDateFormatter                      |
| ITransactionTypeFormatter           |
| IPurchaseTransferOrderTypeFormatter |

### <a name="orgunits"></a>OrgUnits

次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。

| POS API                              |
|--------------------------------------|
| GetOrgUnitConfigurationClientRequest |
| GetOrgUnitTenderTypesClientRequest   |
| InventoryLookupOperationRequest      |

### <a name="products"></a>製品

次に、製品に関連する機能を実行する公開されている API の一覧を示します。

| POS API                                    |
|--------------------------------------------|
| GetProductsByIdsClientRequest              |
| GetCurrentProductCatalogStoreClientRequest |
| SelectProductVariantClientRequest          |
| GetSerialNumberClientRequest               |
| GetRefinerValuesByTextServiceRequest       |
| SelectProductClientRequest |

### <a name="salesorders"></a>SalesOrders

次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。

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

次に、シフトに関連する機能を実行する公開されている API の一覧を示します。

| POS API                    |
|----------------------------|
| CloseShiftOperationRequest |
| CloseShiftOperationRequest |

### <a name="stockcountjournals"></a>StockCountJournals

次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。

| POS API                                |
|----------------------------------------|
| SyncAllStockCountJournalsClientRequest |

### <a name="storeoperations"></a>StoreOperations

次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。

| POS API                                         |
|-------------------------------------------------|
| DeclareStartingAmountClientRequest              |
| GetSalesOrdersWithNoFiscalTransactionsRequest   |
| RegisterCustomAuditEventClientRequest           |
| GetOfflinePendingTransactionCountClientRequest  |
| SaveFiscalTransactionClientRequest              |
| SafeDropOperationRequest                        |
| TenderDeclarationOperationRequest               |
| TenderRemovalOperationRequest                   |
| CreateBankDropTransactionClientRequest          |
| CreateFloatEntryTransactionClientRequest        |
| CreateStartingAmountTransactionClientRequest    |
| CreateTenderDeclarationTransactionClientRequest |
| CreateTenderRemovalTransactionClientRequest     |
| GetDenominationTotalsClientRequest              |
| SelectZipCodeInfoClientRequest                  |
| CreateSafeDropTransactionClientRequest          |
| GetTenderDetailsClientRequest                   |
| LoyaltyCardPointsBalanceOperationRequest        |
| GetCommissionSalesGroupsServiceRequest          |
| GetCurrenciesServiceRequest                     |
| GetSrsReportDataSetServiceRequest               |
| SearchCommissionSalesGroupsServiceRequest       |
| IssueLoyaltyCardOperationRequest                |
| GetPickingAndReceivingOrdersClientRequest       |


