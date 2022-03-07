---
title: Dynamics 365 支払データの使用
description: このトピックでは、Microsoft Dynamics 365 の支払コネクタによって管理されているデータの概要を示します。
author: BrianShook
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2018-11-06
ms.dyn365.ops.version: AX 8.1.2
ms.openlocfilehash: f8d183196540a0a1c604ae0ef86d81a767066962
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779759"
---
# <a name="dynamics-365-payment-data-use"></a>Dynamics 365 支払データの使用

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 の支払コネクタによって管理されているデータの概要を示します。

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| カードあり | *カードあり* という語は、販売時点管理 (POS) レジスターにおいてなど、物理的なカードが存在するトランザクションを処理するために支払コネクタを使用することを指します。 |
| カードなし | *カードなし* という語は、コール センターや E コマースにおいてなど、物理的なカードが存在しないトランザクションを処理するために支払コネクタを使用することを指します。 |

## <a name="overview"></a>概要

このトピックでは、支払コネクタによって管理されているデータに関して次の領域に関する特定の詳細情報を提供します。

- **[カードありシナリオで使用されるデータ](#data-used-in-card-present-scenarios)**: このセクションでは、カードありシナリオの支払コネクタに渡されるデータ フィールドの一覧および説明を示します。
- **[カードなしシナリオで使用されるデータ](#data-used-in-card-not-present-scenarios)**: このセクションでは、カードなしシナリオの支払コネクタに渡されるデータ フィールドの一覧および説明を示します。

## <a name="data-used-in-card-present-scenarios"></a>カードありシナリオで使用されるデータ

このセクションでは、カードありシナリオの支払コネクタに送信されるすべてのデータ ポイントについて説明します。 支払コネクタは、データを使用しないことがあります。

### <a name="payment-connector-request-specific-data"></a>支払コネクタ要求固有のデータ

#### <a name="begintransactionpaymentterminaldevicerequest"></a>BeginTransactionPaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| merchantInformation | Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。 |
| invoiceNumber | POS が販売トランザクションを追跡するために生成する一意の請求書番号。 |

#### <a name="updatelineitemspaymentterminaldevicerequest"></a>UpdateLineItemsPaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| totalAmount | 現在の販売トランザクションでの合計金額。 |
| taxAmount | 現在の販売トランザクションでの税金額。 | 
| discountAmount | 現在の販売トランザクションでの割引金額。 |
| subTotalAmount | 現在の販売トランザクションでの小計金額。 |
| 項目 | 製品名、数量、または計量単位など、製品に固有の詳細の一覧。 |

#### <a name="authorizepaymentterminaldevicerequest"></a>AuthorizePaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| 金額 | 承認する金額。 |
| 通貨 | 承認する金額の通貨。 |
| voiceAuthorization | 音声認証が必要な場合は、POS から送信される音声承認コード。 |

#### <a name="capturepaymentterminaldevicerequest"></a>CapturePaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| 金額 | 取得する金額。 |
| 通貨 | 取得する金額の通貨。 |
| paymentPropertiesXml | **AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。 詳細については、このトピックで後述する[支払 SDK データ](#payment-sdk-data) セクションを参照してください。 |

#### <a name="voidpaymentterminaldevicerequest"></a>VoidPaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| 金額 | 支払いが無効になる金額。 |
| 通貨 | 支払いが無効になる通貨。 |
| paymentPropertiesXml | **AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。 詳細については、このトピックで後述する[支払 SDK データ](#payment-sdk-data) セクションを参照してください。 |

#### <a name="refundpaymentterminaldevicerequest"></a>RefundPaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| 金額 | 払い戻す金額。 |
| 通貨 | 払い戻す金額の通貨。 |

#### <a name="activategiftcardpaymentterminalrequest"></a>ActivateGiftCardPaymentTerminalRequest

| フィールド | 説明 |
|---|---|
| 金額 | 有効化中にギフト カードに追加する初期金額。 |
| 通貨 | 有効化中にギフト カードに追加する初期金額の通貨。 |

#### <a name="addbalancetogiftcardpaymentterminalrequest"></a>AddBalanceToGiftCardPaymentTerminalRequest

| フィールド | 説明 |
|---|---|
| 金額 | ギフト カード残高に追加される金額。 |
| 通貨 | ギフト カード残高に追加する金額の通貨。 |

#### <a name="getgiftcardbalancepaymentterminalrequest"></a>GetGiftCardBalancePaymentTerminalRequest

| フィールド | 説明 |
|---|---|
| 通貨 | ギフト カード残高を取得するための通貨。 |

#### <a name="getprivatetenderpaymentterminaldevicerequest"></a>GetPrivateTenderPaymentTerminalDeviceRequest

| フィールド | 説明 |
|---|---|
| 金額 | POS に設定された金額。 (通常、この変数は、カード番号を取得したときに支払ターミナルの金額を表示するために使用されます。) |

### <a name="shared-data"></a>共有データ

#### <a name="payment-sdk-data"></a>支払 SDK データ

| フィールド | 説明 |
|---|---|
| ApprovedAmount | トランザクションに対して承認された金額。 |
| AvailableBalance | カードの使用可能な残高。 |
| ApprovalCode | トランザクションの承認コード。 |
| ProviderTransactionId | 支払いプロバイダーのトランザクション識別子。 |
| AuthorizationResult | 権限呼び出しの結果。 |
| ExternalReceipt | 支払プロバイダーからの外部レシート データ。 |
| TerminalId | 支払を処理した端末の一意の識別子。 |
 
## <a name="data-used-in-card-not-present-scenarios"></a>カードなしシナリオで使用されるデータ

このセクションでは、カードなしシナリオの支払コネクタに送信されるデータについて説明します。 各コネクタが処理する特定のデータはさまざまであるため、特定のコネクタが提供されたすべてのデータを使用しない可能性があります。

### <a name="payment-connector-methodspecific-data"></a>支払コネクタ方法固有のデータ

#### <a name="authorization"></a>認証

| 名前空間 | フィールド | 説明 |
|---|---|---|
| MerchantAccount | MerchantId | Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。 |
| PaymentCard | Last4Digits | 支払に使用するカードの末尾 4 桁。 | 
| PaymentCard | UniqueCardId | 支払に使用するカードのランダムな一意識別子。 |
| PaymentCard | ExpirationYear | 支払に使用するカードの有効期限年。 |
| PaymentCard | ExpirationMonth | 支払に使用するカードの有効期限月。 |
| PaymentCard | StreetAddress | 支払に使用されるカードに関連付けられている請求先住所の番地。 |
| PaymentCard | 市町村 | 支払に使用されるカードに関連付けられている請求先住所の市町村。 |
| PaymentCard | 行政単位 (区画) | 支払に使用されるカードに関連付けられている請求先住所の都道府県。 |
| PaymentCard | PostalCode | 支払に使用されるカードに関連付けられている請求先住所の郵便番号。 |
| TransactionData | IndustryType | 支払が発生したチャネルのタイプ (たとえば、**小売**、**ダイレクト マーケティング**、または **電子商取引**)。 |
| TransactionData | AllowPartialAuthorization | 部分的な承認がサポートされているかどうかを示す値。 |
| TransactionData | 量 | トランザクションの合計金額。 |
| TransactionData | CurrencyCode | トランザクションの通貨コード。 |
| TransactionData | TerminalId | トランザクションが発生した端末の一意の識別子。 |
| PurchaseLevelData | L2Data | "レベル 2" データの一覧。 詳細については、このトピックで後述する[L2 データ](#l2-data) セクションを参照してください。 |
| PurchaseLevelData | L3Data | "レベル 3" データの一覧。 詳細については、このトピックで後述する[L3 データ](#l3-data) セクションを参照してください。 |

#### <a name="capture"></a>キャプチャ

| 名前空間 | フィールド | 説明 |
|---|---|---|
| MerchantAccount | MerchantId | Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。 |
| TransactionData | 量 | トランザクションの合計金額。 |
| TransactionData | CurrencyCode | トランザクションの通貨コード。 |
| PurchaseLevelData | L2Data | "レベル 2" データの一覧。 詳細については、このトピックで後述する[L2 データ](#l2-data) セクションを参照してください。 |
| PurchaseLevelData | L3Data | "レベル 3" データの一覧。 詳細については、このトピックで後述する[L3 データ](#l3-data) セクションを参照してください。 |

#### <a name="void"></a>無効

| 名前空間 | フィールド | 説明 |
|---|---|---|
| MerchantAccount | MerchantId | Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。 |
| TransactionData | 量 | トランザクションの合計金額。 |
| TransactionData | CurrencyCode | トランザクションの通貨コード。 |

#### <a name="refund"></a>払戻

| 名前空間 | フィールド | 説明 |
|---|---|---|
| MerchantAccount | MerchantId | Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。 |
| PaymentCard | Last4Digits | 支払に使用するカードの末尾 4 桁。 | 
| PaymentCard | UniqueCardId | 支払に使用するカードのランダムな一意識別子。 |
| PaymentCard | ExpirationYear | 支払に使用するカードの有効期限年。 |
| PaymentCard | ExpirationMonth | 支払に使用するカードの有効期限月。 |
| PaymentCard | StreetAddress | 支払に使用されるカードに関連付けられている請求先住所の番地。 |
| PaymentCard | 市町村 | 支払に使用されるカードに関連付けられている請求先住所の市町村。 |
| PaymentCard | 行政単位 (区画) | 支払に使用されるカードに関連付けられている請求先住所の都道府県。 |
| PaymentCard | PostalCode | 支払に使用されるカードに関連付けられている請求先住所の郵便番号。 |
| TransactionData | IndustryType | 支払が発生したチャネルのタイプ (たとえば、**小売**、**ダイレクト マーケティング**、または **電子商取引**)。 |
| TransactionData | AllowPartialAuthorization | 部分的な承認がサポートされているかどうかを示す値。 |
| TransactionData | 量 | トランザクションの合計金額。 |
| TransactionData | CurrencyCode | トランザクションの通貨コード。 |
| TransactionData | TerminalId | トランザクションが発生した端末の一意の識別子。 |
| PurchaseLevelData | L2Data | "レベル 2" データの一覧。 詳細については、このトピックで後述する[L2 データ](#l2-data) セクションを参照してください。 |
| PurchaseLevelData | L3Data | "レベル 3" データの一覧。 詳細については、このトピックで後述する[L3 データ](#l3-data) セクションを参照してください。 |

#### <a name="getpaymentacceptpoint"></a>GetPaymentAcceptPoint 

| 名前空間 | フィールド | 説明 |
|---|---|---|
| MerchantAccount | MerchantId | Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。 |
| PaymentCard | 氏名 | カード所有者の名前。 |
| PaymentCard | StreetAddress | 支払に使用されるカードに関連付けられている請求先住所の番地。 |
| PaymentCard | 市町村 | 支払に使用されるカードに関連付けられている請求先住所の市町村。 |
| PaymentCard | 行政単位 (区画) | 支払に使用されるカードに関連付けられている請求先住所の都道府県。 |
| PaymentCard | PostalCode | 支払に使用されるカードに関連付けられている請求先住所の郵便番号。 |
| PaymentCard | 国 | 支払に使用されるカードに関連付けられている請求先住所の国または地域。 |
| PaymentCard | ShowSameAsShippingAddress | 請求先住所が出荷先住所と同じかどうかを識別する値。 |
| TransactionData | IndustryType | 支払が発生したチャネルのタイプ (たとえば、**小売**、**ダイレクト マーケティング**、または **電子商取引**)。 |
| TransactionData | AllowPartialAuthorization | 部分的な承認がサポートされているかどうかを示す値。 |
| TransactionData | CurrencyCode | トランザクションの通貨コード。 |
| TransactionData | TerminalId | トランザクションが発生した端末の一意の識別子。 |

### <a name="shared-data"></a>共有データ

#### <a name="l2-data"></a>L2 データ

> [!NOTE]
> この動作がコマース クライアント内の対応するコネクタ構成を通じて明示的に構成されている場合にのみ、L2 データがコネクタに送信されます。

| 名前空間 | フィールド | 説明 |
|---|---|---|
| L2Data | OrderDateTime | 注文が発生した日時。 |
| L2Data | OrderNumber | 注文に関連付けられている注文番号。 |
| L2Data | InvoiceDateTime | 注文が作成された日時。 |
| L2Data | InvoiceNumber | 注文の請求書番号。 |
| L2Data | OrderDescription | 注文の説明。 |
| L2Data | SummaryCommodityCode | 製品に関連付けられている商品コード。 |
| L2Data | MerchantContact | 販売者の連絡先情報。 |
| L2Data | MerchantTaxId | 販売者の一意の税 ID。 |
| L2Data | MerchantType | 支払プロセッサによって保持されている固有の販売者 ID。 |
| L2Data | PurchaserId | 購入者の一意の識別子。 |
| L2Data | PurchaserTaxId | 購入者の一意の税識別子。 |
| L2Data | ShipToCity | 出荷先住所の市町村。 |
| L2Data | ShipToCounty | 出荷先住所の市区郡。 |
| L2Data | ShipToState\_ProvinceCode | 出荷先住所の都道府県コード。 |
| L2Data | ShipToPostalCode | 出荷先住所の郵便番号。 |
| L2Data | ShipToCountryCode | 出荷先住所の国または地域コード。 |
| L2Data | ShipFromCity | 注文の出荷元の住所の市町村。 |
| L2Data | ShipFromCounty | 注文の出荷元の住所の市区郡。 |
| L2Data | ShipFromState\_ProvinceCode | 注文の出荷元の住所の都道府県コード。 |
| L2Data | ShipFromPostalCode | 注文の出荷元の住所の郵便番号。 |
| L2Data | ShipFromCountryCode | 注文の出荷元の住所の国または地域コード。 |
| L2Data | DiscountAmount | 注文の特定の明細行品目の部分に適用される割引金額。 |
| L2Data | MiscCharge | 注文の特定の明細行品目の部分に適用されるその他の変更。 | 
| L2Data | DutyAmount | 注文の特定の明細行品目の部分に適用される関税額。 |
| L2Data | FreightAmount | 注文の特定の明細行品目の部分に適用される配送料。 |
| L2Data | HandlingCharge | 注文の特定の明細行品目の部分に適用される取扱手数料。 |
| L2Data | IsTaxable | 注文の特定の明細行品目の部分が課税対象であるかどうかを識別する値。 |
| L2Data | TotalTaxAmount | 注文の特定の明細行品目の部分に適用される合計税額。 |
| L2Data | TotalTaxRate | 注文の特定の明細行品目の部分に適用される合計税率。 |
| L2Data | MerchantName | 販売者の名前。 |
| L2Data | MerchantCity | 販売者の住所の市町村。 |
| L2Data | MerchantState | 販売者の住所の都道府県。 |
| L2Data | MerchantCounty | 販売者の住所の市区郡。 |
| L2Data | MerchantCountryCode | 販売者の住所の国または地域コード。 |
| L2Data | MerchantZip | 販売者の住所の郵便番号。 |
| L2Data | TaxRate | 注文の特定の明細行品目の部分に適用される税率。 |
| L2Data | TaxAmount | 注文の特定の明細行品目の部分に適用される税額。 |
| L2Data | TaxDescription | 注文の特定の明細行品目の部分に適用される税の説明。 | 
| L2Data | TaxTypeIdentifier | 注文の特定の明細行品目の部分に適用される税のタイプ識別子。 |
| L2Data | RequesterName | 要求者の名前。 |
| L2Data | TotalAmount | 注文の特定の明細行品目の部分の合計税額。 |
| L2Data | PurchaseCardType | 購入者のカードの種類。 |
| L2Data | AmexLegacyDescription1 | 従来の American Express 説明フィールド 1。 |
| L2Data | AmexLegacyDescription2 | 従来の American Express 説明フィールド 2。 |
| L2Data | AmexLegacyDescription3 | 従来の American Express 説明フィールド 3。 |
| L2Data | AmexLegacyDescription4 | 従来の American Express 説明フィールド 4。 |
| L2Data | TaxDetails\[\].TaxRate | 注文の特定の明細行品目の部分に適用される個々の税率の一覧。 |
| L2Data | TaxDetails\[\].TaxDescription | 注文の特定の明細行品目の部分に適用される税の個々の説明の一覧。 |
| L2Data | TaxDetails\[\].TaxAmount | 注文の特定の明細行品目の部分に適用される個々の税額の一覧。 |
| L2Data | TaxDetails\[\].TaxTypeIdentifier | 注文の特定の明細行品目の部分に適用される税のタイプ識別子の一覧。 |
| L2Data | MiscellaneousCharges\[\].ChargeType | 注文の特定の明細行品目の部分に適用される請求タイプの一覧。 |
| L2Data | MiscellaneousCharges\[\].ChargeAmount | 注文の特定の明細行品目の部分に適用される請求金額の一覧。 |

#### <a name="l3-data"></a>L3 データ

> [!NOTE]
> この動作がコマース クライアント内の対応するコネクタ構成を通じて明示的に構成されている場合にのみ、L3 データがコネクタに送信されます。

| 名前空間 | フィールド | 説明 |
|---|---|---|
| L3Data | SequenceNumber | 注文の品目の順序番号。 |
| L3Data | CommodityCode | 製品に関連付けられている商品コード。 |
| L3Data | ProductCode | 製品の一意のコード。 | 
| L3Data | ProductName | 生産の名前。 |
| L3Data | ProductSKU | 製品の最小在庫管理単位 (SKU)。 |
| L3Data | Descriptor | 製品の説明。 |
| L3Data | UnitOfMeasure | 製品の測定単位。 |
| L3Data | UnitPrice | 製品の単価。 |
| L3Data | 割引 | 製品に適用される割引。 |
| L3Data | DiscountRate | 製品に適用される割引率。 |
| L3Data | 件数 | 製品の数量。 |
| L3Data | MiscCharge | 製品のその他の請求金額。 |
| L3Data | NetTotal | 製品の正味合計額。 |
| L3Data | TaxAmount | 製品の税額。 |
| L3Data | TaxRate | 製品の税率。 |
| L3Data | TotalAmount | 製品の合計金額。 |
| L3Data | CostCenter | 製品のコスト センター。 |
| L3Data | FreightAmount | 製品の配送料。 |
| L3Data | HandlingAmount | 製品の取扱手数料。 |
| L3Data | CarrierTrackingNumber | 出荷される製品の配送業者の追跡番号。 |
| L3Data | MerchantTaxID | 販売者の一意の税 ID。 |
| L3Data | MerchantCatalogNumber | 販売者のカタログ番号。 |
| L3Data | TaxCategoryApplied | 製品に適用される税カテゴリ。 |
| L3Data | PickupAddress | 集荷元住所の番地。 |
| L3Data | PickupCity | 集荷元住所の市町村。 |
| L3Data | PickupState | 集荷元住所の都道府県。 |
| L3Data | PickupCounty | 集荷元住所の市区郡。 |
| L3Data | PickupZip | 集荷元住所の郵便番号。 |
| L3Data | PickupCountry | 集荷元住所の国または地域。 |
| L3Data | PickupDateTime | 集荷の日時。 |
| L3Data | PickupRecordNumber | 集荷のレコード番号。 |
| L3Data | CarrierShipmentNumber | 配送業者の出荷番号。 |
| L3Data | UNSPSCCode | United Nations Standard Products and Services Code (UNSPSC)。 |
| L2Data | TaxDetails\[\].TaxRate | 注文の特定の明細行品目の部分に適用される個々の税率の一覧。 |
| L2Data | TaxDetails\[\].TaxDescription | 注文の特定の明細行品目の部分に適用される税の個々の説明の一覧。 |
| L2Data | TaxDetails\[\].TaxAmount | 注文の特定の明細行品目の部分に適用される個々の税額の一覧。 |
| L3Data | TaxDetails\[\].TaxTypeIdentifier | 注文の特定の明細行品目の部分に適用される税のタイプ識別子の一覧。 |
| L3Data | MiscellaneousCharges\[\].ChargeType | 注文の特定の明細行品目の部分に適用される請求タイプの一覧。 |
| L3Data | MiscellaneousCharges\[\].ChargeAmount | 注文の特定の明細行品目の部分に適用される請求金額の一覧。 |

## <a name="related-topics"></a>関連トピック

- **[支払端末のエンド ツー エンド支払統合の作成](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension)** – このトピックでは、カスタム支払コネクタを作成する方法について説明します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]