---
title: 二重書き込みの見込顧客を現金化
description: このトピックでは、二重書き込みの見込顧客を現金化に関する情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 6fe42f43277448dc5918597ed8bb1b68f2266b6a
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829215"
---
# <a name="prospect-to-cash-in-dual-write"></a>二重書き込みの見込顧客を現金化

[!include [banner](../../includes/banner.md)]



ほとんどの企業にとって重要な目標は、見込顧客を顧客に変換し、その顧客との継続的な取引関係を維持することです。 Microsoft Dynamics 365 アプリでは、見込顧客を現金化のプロセスが見積または注文処理のワークフローで行われ、財務の調整と認識が行われます。 二重書き込みによる見込顧客を現金化の統合により、見積と、Dynamics 365 Sales または Dynamics 365 Supply Chain Management のいずれかの方法で発生した注文を取得し、両方のアプリで見積と注文を使用できるようにするワークフローが作成されます。

アプリ インターフェイスでは、処理のステータスおよび請求書情報にリアル タイムでアクセスできます。 したがって、見積と注文を再作成することなく、Supply Chain Management の製品在庫、在庫処理、およびフルフィルメントなどの機能をより簡単に管理することができます。

![見込顧客を現金化への二重書き込みデータフロー](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

販売見積を同期するためには、次の設定を更新する必要があります。

### <a name="setup-in-sales"></a>Sales での設定

Sales で、**設定 \> 管理 \> システム設定 \> 販売**の順にクリックし、次の設定が使用されていることを確認してください。

- **システム プライジング計算の使用**システム オプションが、**はい**に設定されています。
- **割引の計算方法** フィールドが、**明細行品目** に設定されている。

### <a name="sites-and-warehouses"></a>サイトと倉庫

Supply Chain Management では、見積明細行と注文明細行に対して**サイト**と**倉庫**フィールドが必要です。 サイトと倉庫を既定の注文設定に設定した場合、これらのフィールドは、見積明細行または注文明細行に製品を追加したときに自動的に設定されます。 

### <a name="number-sequences-for-quotations-and-orders"></a>見積と注文の番号順序

Sales および Supply Chain Management で見積と注文が作成され同期されている場合、Supply Chain Management と販売の番号順序は接続されていません。 Sales で作成された販売注文が Supply Chain Management に同期されている場合は、Supply Chain Management の販売注文番号も同じになります。 販売注文番号が重複しないようにするには、2 つのアプリで別の番号順序システムを使用する必要があります。

たとえば、Supply Chain Management の番号順序は **1、2、3、4、5** となり、売上の番号順序は **100、99、98、...** となります。Sales で 100 の販売注文を作成する場合は、最終的に、Supply Chain Management に既に存在する注文番号が生成されます。 つまり、2 つの番号順序は、Supply Chain Management および Sales で販売注文が作成されるときに、最終的に重複します。 代わりに、Supply Chain Management で **F1、F2、F3、...** などの番号順序や Sales で **C1、C2、C3、...** などの番号順序を使用することができます。 これらの番号順序では重複する販売注文番号が作成されることはありません。

## <a name="sales-quotations"></a>販売見積

販売見積が Sales または Supply Chain Management で作成されます。 Sales で見積を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。 同様に、Supply Chain Management で見積を作成すると、その見積がリアル タイムで Sales に同期されます。 次のポイントに注意します。

+ 見積の製品に割引を追加できます。 この場合、割引は Supply Chain Management に同期されます。 **割引**、**請求**、および **税** フィールドは、ヘッダーで Supply Chain Management の設定によって制御されます。 この設定では、統合マッピングはサポートされていません。 代わりに、**価格**、**割引**、**請求金額**、および**税**の各フィールドは、Supply Chain Management で管理および処理されます。
+ 販売見積ヘッダーの読み取り専用フィールドの**割引 %**、**割引**、**貨物量**。
+ **運賃条件**、**配送条件**、**送付方法**、および**配送モード** フィールドは、既定のマッピングの一部ではありません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

また、Field Service ソリューションも使用している場合は、**見積明細行の簡易作成** パラメータを再度有効にする必要があります。 このパラメータを再度有効にすると、簡易作成機能を使用して、見積明細行の作成を続行することができます。
1. Dynamics 365 Sales アプリケーションに移動します。
2. ナビゲーション バー上部の設定アイコンを選択します。
3. **詳細設定** を選択します。
4. **システムのカスタマイズ** オプションを選択します。
5. **見積明細行** のメニュー項目を選択します。
6. **データ サービス** セクションに移動し、**簡易作成を許可する** チェックボックスをオンにします。

## <a name="sales-orders"></a>販売注文

販売注文が Sales または Supply Chain Management のいずれかで作成されます。 Sales で販売注文を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。 同様に、Supply Chain Management で販売注文を作成すると、その見積もりがリアル タイムで Sales に同期されます。 次のポイントに注意します。

+ Dynamics 365 Sales でリスト外製品は、Dynamics 365 Supply Chain Management では製品カテゴリとして表示されます。
+ 割引計算と丸め:

    - Sales での割引計算モデルは、Supply Chain Management の割引計算モデルとは異なります。 Supply Chain Management では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。 この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。 ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。 Supply Chain Management の販売明細行からの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。 したがって、Sales で割引の計算方法を**明細行品目**として定義する必要があります。
    - 販売注文行が Sales から Supply Chain Management に同期される場合、明細行全体の割引額が使用されます。 Supply Chain Management には、明細行の完全な割引金額を格納できるフィールドがないため、金額は数量で除算されて、**行割引**フィールドに格納されます。 この区分中に発生する丸めは、販売明細行の**販売費用**フィールドに保管されます。

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>例: Sales から Supply Chain Management への同期

次の販売注文があります。

+ **Sales:** 数量 = 3、行あたりの割引 = 10.00 USD
+ **Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01

Supply Chain Management から Sales に同期すると、次の結果が得られます。

+ **Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01
+ **Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD

## <a name="dual-write-solution-for-sales"></a>Sales のための二重書き込みソリューション

新しいフィールドが**注文**エンティティに追加され、ページに表示されます。 これらのフィールドのほとんどは、Sales の**統合**タブに表示されます。 状態フィールドがどのようにマッピングされるかについての詳細については、[販売注文の状態フィールドのマッピングを設定する](https://review.docs.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/sales-status-map?branch=robin-dw-status-map)に記載のトピックを参照してください

+ **販売注文**ページに**請求書作成**または**注文のキャンセル** ボタンは Sales に表示されません。
+ **販売注文状態**は**有効**のままにすると、Supply Chain Management からの変更が Sales の販売注文に流れるようにします。 この動作を管理するためには、既定の**ステイトコード \[ステータス\]** 値を**有効**に設定します。

## <a name="invoices"></a>請求書

売上請求書が Supply Chain Management で作成され、Sales に同期されます。 次のポイントに注意します。

+ **請求書番号**フィールドが**請求書**エンティティに追加され、ページに表示されます。
+ 請求書が Supply Chain Management で作成され、Sales に同期されるため、**販売注文**ページの**請求書の作成**ボタンは非表示になります。 請求書が Supply Chain Management から同期されるため、**請求書**ページは編集できません。
+ Supply Chain Management からの関連請求書が Sales に同期されると、**販売注文状態**値は自動的に**請求済**に変更されます。 さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。 したがって、販売注文書の所有者は、請求書を表示することができます。
+ **運賃条件**、**配送条件**、および**荷渡方法**フィールドは既定のマッピングには含まれていません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

## <a name="templates"></a>テンプレート

次の表に示されているように、見込顧客を現金化するには、データ操作中に連携して動作するコア エンティティ マップのコレクションが含まれています。

| Finance and Operations アプリ | Dynamics 365 のモデル駆動型アプリ | 説明 |
|-----------------------------|-----------------------------------|-------------|
| 売上請求書ヘッダー V2    | 請求書                          |             |
| 売上請求書明細行 V2      | invoicedetails                    |             |
| CDS 販売注文ヘッダー     | 販売注文                       |             |
| CDS 販売注文明細行       | 販売注文詳細                 |             |
| 販売注文元コード    | msdyn\_販売注文元          |             |
| CDS 販売見積ヘッダー  | 見積                            |             |
| CDS 販売見積明細行   | 見積詳細                      |             |

見込顧客の現金化に関連するコア エンティティ マップは次のとおりです。

+ [顧客 V3 を アカウントへ](customer-mapping.md#customers-v3-to-accounts)
+ [CDS 連絡先 V2 を連絡先へ](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [顧客 V3 を連絡先へ](customer-mapping.md#customers-v3-to-contacts)
+ [リリース済製品 V2 を msdyn_sharedproductdetails へ](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [すべての製品を msdyn_globalproducts へ](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [価格表](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
