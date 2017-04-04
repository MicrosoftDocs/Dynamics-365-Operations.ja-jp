---
title: "買掛金勘定の集中支払"
description: "複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。 したがって、同じ支払を複数の法人に入力する必要はありません。 この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e7cc68b1b40b6a0361d7c215af466ae5a17a2aaa
ms.lasthandoff: 03/31/2017


---

# <a name="centralized-payments-for-accounts-payable"></a>買掛金勘定の集中支払

複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。 したがって、同じ支払を複数の法人に入力する必要はありません。 この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。

複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。 したがって、同じ支払を複数の法人に入力する必要はありません。 また、組織では、支払プロセスが合理化されるため、時間を節約できます。

集中支払組織では、事業を行うために多くの法人があり、事業を行っている各法人がそれぞれの仕入先請求書を管理します。 事業を行っているすべての法人の支払は、支払の法人として知られている 1 つの法人から行われます。 決済プロセス中に、適切な借りトランザクションと貸しトランザクションが生成されます。 組織内のどの法人が実利益トランザクションと実損失トランザクションを受け取るか、また、会社間支払に関連する現金割引トランザクションの処理方法を指定できます。 

次の各例で、さまざまなシナリオにおける転記の処理方法を示します。 これらすべての例について、次の構成が想定されます。

-   法人は Fabrikam、Fabrikam East、および Fabrikam West です。 支払は、Fabrikam で構成されています。
-   [**会社間会計**] ページの [**現金割引の転記**] フィールドには**請求書の法人**が設定されます。
-   [**会社間会計**] ページの [**為替差益または差損の転記**] フィールドには**請求書の支払**が設定されます。
-   仕入先の Fourth Coffee は、各法人の仕入先として設定されています。 異なる法人の仕入先は同一のグローバル アドレス帳 ID を共有するため、同じ仕入先として識別されます。

| ディレクトリ ID | 仕入先 | 氏名          | 個法  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam East |
| 1050         | 3004           | Fourth Coffee | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>例 1 : 別の法人からの請求書の仕入先支払
Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。 Fabrikam は、支払を入力し、Fabrikam 仕入先 3004 の Fourth Coffee に転記します。 支払は、未処理請求書で決済されます。

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>仕入先 100 に対して Fabrikam East で転記される請求書

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 経費 (Fabrikam East)          | 600.00       |               |
| 買掛金 (Fabrikam East) |              | 600.00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>仕入先 3004 に対して Fabrikam で生成および転記される支払

| 勘定                     | 借方金額 | 貸方金額 |
|-----------------------------|--------------|---------------|
| 買掛金 (Fabrikam) | 600.00       |               |
| 現金 (Fabrikam)             |              | 600.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam East の請求書で決済される Fabrikam の支払

**Fabrikam posting**

| 勘定                           | 借方金額 | 貸方金額 |
|-----------------------------------|--------------|---------------|
| Fabrikam East 貸し (Fabrikam) | 600.00       |               |
| 買掛金 (Fabrikam)       |              | 600.00        |

**Fabrikam East posting**

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 買掛金 (Fabrikam East) | 600.00       |               |
| Fabrikam への貸し (Fabrikam East)  |              | 600.00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>例 2 : 現金割引のある別法人からの請求書の仕入先支払
Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。 請求書では、20.00 の現金割引を利用できます。 Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する 580.00 の支払を入力して転記します。 支払は、未処理の Fabrikam East 請求書で決済されます。 現金割引が請求書、Fabrikam East の法人に転記されます。

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 経費 (Fabrikam East)          | 600.00       |               |
| 買掛金 (Fabrikam East) |              | 600.00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払

| 勘定                     | 借方金額 | 貸方金額 |
|-----------------------------|--------------|---------------|
| 買掛金 (Fabrikam) | 580.00       |               |
| 現金 (Fabrikam)             |              | 580.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam East の請求書で決済される Fabrikam の支払

**Fabrikam posting**

| 勘定                           | 借方金額 | 貸方金額 |
|-----------------------------------|--------------|---------------|
| Fabrikam East 貸し (Fabrikam) | 580.00       |               |
| 買掛金 (Fabrikam)       |              | 580.00        |

**Fabrikam East posting**

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 買掛金 (Fabrikam East) | 580.00       |               |
| Fabrikam 借り (Fabrikam East)  |              | 580.00        |
| 買掛金 (Fabrikam East) | 20.00        |               |
| 現金割引 (Fabrikam East)    |              | 20.00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>例 3 : 実現為替差損のある別法人からの請求書の仕入先支払
Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。 Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を入力して転記します。 支払は、未処理の Fabrikam East の請求書で決済されます。 決済プロセスの間に、為替差損トランザクションが生成されます。

-   請求日時点でのユーロ (EUR) から米国ドル (USD) への為替レート : 1.2062
-   支払日時点での EUR から USD への為替レート : 1.2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書

| 勘定                          | 借方金額            | 貸方金額           |
|----------------------------------|-------------------------|-------------------------|
| 経費 (Fabrikam East)          | 600.00 EUR/723.72 USD)  |                         |
| 買掛金 (Fabrikam East) |                         | 600.00 EUR/723.72 USD)  |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払

| 勘定                     | 借方金額            | 貸方金額           |
|-----------------------------|-------------------------|-------------------------|
| 買掛金 (Fabrikam) | 600.00 EUR/736.62 USD)  |                         |
| 現金 (Fabrikam)             |                         | 600.00 EUR/736.62 USD)  |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam East の請求書で決済される Fabrikam の支払

**Fabrikam posting**

| 勘定                           | 借方金額            | 貸方金額           |
|-----------------------------------|-------------------------|-------------------------|
| Fabrikam East 貸し (Fabrikam) | 600.00 EUR/736.62 USD)  |                         |
| 買掛金 (Fabrikam)       |                         | 600.00 EUR/736.62 USD)  |
| 実現損失 (Fabrikam)          | 0.00 EUR/12.90 USD)     |                         |
| Fabrikam East 貸し (Fabrikam) |                         | 0.00 EUR/12.90 USD)     |

**Fabrikam East posting**

| 勘定                          | 借方金額            | 貸方金額           |
|----------------------------------|-------------------------|-------------------------|
| 買掛金 (Fabrikam East) | 600.00 EUR/736.62 USD)  |                         |
| Fabrikam 借り (Fabrikam East)  |                         | 600.00 EUR/736.62 USD)  |
| Fabrikam 借り (Fabrikam East)  | 0.00 EUR/12.90 USD)     |                         |
| 買掛金 (Fabrikam East) |                         | 0.00 EUR/12.90 USD)     |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>例 4 : 現金割引と実現為替差損のある別法人からの請求書の仕入先支払
Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。 請求書には現金割引があり、売上税トランザクションが生成されます。 Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を転記します。 支払は、未処理の Fabrikam East の請求書で決済されます。 決済プロセスの間に、為替差損トランザクションが生成されます。 現金割引が請求の法人 (Fabrikam East) に転記され、通貨為替差損が支払の法人 (Fabrikam) に転記されます。

-   請求日時点での EUR から USD への為替レート : 1.2062
-   支払日時点での USD に対する EUR の為替レート : 1.2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>仕入先 100 に対して Fabrikam East で転記される請求書および生成される税トランザクション

| 勘定                          | 借方金額            | 貸方金額           |
|----------------------------------|-------------------------|-------------------------|
| 経費 (Fabrikam East)          | 564.07 EUR/680.38 USD)  |                         |
| 売上税 (Fabrikam East)        | 35.93 EUR/43.34 USD)    |                         |
| 買掛金 (Fabrikam East) |                         | 600.00 EUR/723.72 USD)  |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>仕入先 3004 に対して Fabrikam で生成および転記される支払

| 勘定                     | 借方金額            | 貸方金額           |
|-----------------------------|-------------------------|-------------------------|
| 買掛金 (Fabrikam) | 588.72 EUR/722.77 USD)  |                         |
| 現金 (Fabrikam East)        |                         | 588.72 EUR/722.77 USD)  |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam East の請求書で決済される Fabrikam の支払

**Fabrikam posting**

| 勘定                           | 借方金額            | 貸方金額           |
|-----------------------------------|-------------------------|-------------------------|
| Fabrikam East 貸し (Fabrikam) | 588.72 EUR/722.77 USD)  |                         |
| 買掛金 (Fabrikam)       |                         | 588.72 EUR/722.77 USD)  |
| 実現損失 (Fabrikam)          | 0.00 EUR/12.66 USD)     |                         |
| Fabrikam East 貸し (Fabrikam) |                         | 0.00 EUR/12.66 USD)     |

**Fabrikam East posting**

| 勘定                          | 借方金額            | 貸方金額           |
|----------------------------------|-------------------------|-------------------------|
| 買掛金 (Fabrikam East) | 588.72 EUR/722.77 USD)  |                         |
| Fabrikam 借り (Fabrikam East)  |                         | 588.72 EUR/722.77 USD)  |
| Fabrikam 借り (Fabrikam East)   | 0.00 EUR/12.66 USD)     |                         |
| 買掛金 (Fabrikam East) |                         | 0.00 EUR/12.66 USD)     |
| 買掛金 (Fabrikam East) | 11.28 EUR/13.61 USD)    |                         |
| 現金割引 (Fabrikam East)    |                         | 11.28 EUR/13.61 USD)    |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>例 5 : 基本支払のある仕入先貸方票
Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。 支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。 支払はと**決済のトランザクション**ページの基本支払として選択されています。

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>仕入先 3004 に対して Fabrikam West で転記される請求書

| 口座                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 経費 (Fabrikam West)          | 100.00       |               |
| 買掛金 (Fabrikam West) |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>仕入先 100 に対して Fabrikam East に転記される貸方票

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 買掛金 (Fabrikam East) | 25.00        |               |
| 購買返品 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>仕入先 3004 に対して Fabrikam に転記される支払

| 勘定                     | 借方金額 | 貸方金額 |
|-----------------------------|--------------|---------------|
| 買掛金 (Fabrikam) | 75.00        |               |
| 現金 (Fabrikam)             |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払

**Fabrikam posting**

| 勘定                           | 借方金額 | 貸方金額 |
|-----------------------------------|--------------|---------------|
| 買掛金 (Fabrikam)       | 25.00        |               |
| Fabrikam East 借り (Fabrikam)   |              | 25.00         |
| Fabrikam West 貸し (Fabrikam) | 100.00       |               |
| 買掛金 (Fabrikam)       |              | 100.00        |

**Fabrikam East posting**

| 勘定                           | 借方金額 | 貸方金額 |
|-----------------------------------|--------------|---------------|
| Fabrikam 貸し (Fabrikam East) | 25.00        |               |
| 買掛金 (Fabrikam East)  |              | 25.00         |

**Fabrikam West posting**

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 買掛金 (Fabrikam West) | 100.00       |               |
| Fabrikam 借り (Fabrikam West)  |              | 100.00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>例 6 : 基本支払のない仕入先貸方票
Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。 支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。 支払は、**決済のトランザクション**ページで基本支払として選択されていません。

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>仕入先 3004 に対して Fabrikam West で転記される請求書

| 口座                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 経費 (Fabrikam West)          | 100.00       |               |
| 買掛金 (Fabrikam West) |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>仕入先 100 に対して Fabrikam East に転記される貸方票

| 勘定                          | 借方金額 | 貸方金額 |
|----------------------------------|--------------|---------------|
| 買掛金 (Fabrikam East) | 25.00        |               |
| 購買返品 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>仕入先 3004 に対して Fabrikam に転記される支払

| 勘定                     | 借方金額 | 貸方金額 |
|-----------------------------|--------------|---------------|
| 買掛金 (Fabrikam) | 75.00        |               |
| 現金 (Fabrikam)             |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払

**Fabrikam posting**

| 勘定                           | 借方金額 | 貸方金額 |
|-----------------------------------|--------------|---------------|
| Fabrikam West 貸し (Fabrikam) | 75.00        |               |
| 買掛金 (Fabrikam)       |              | 75.00         |

**Fabrikam East posting**

| 勘定                                | 借方金額 | 貸方金額 |
|----------------------------------------|--------------|---------------|
| Fabrikam West 貸し (Fabrikam East) | 25.00        |               |
| 買掛金 (Fabrikam East)       |              | 25.00         |

**Fabrikam West posting**

| 勘定                              | 借方金額 | 貸方金額 |
|--------------------------------------|--------------|---------------|
| 買掛金 (Fabrikam West)     | 75.00        |               |
| Fabrikam 借り (Fabrikam West)      |              | 75.00         |
| 買掛金 (Fabrikam West)     | 25.00        |               |
| Fabrikam East 借り (Fabrikam West) |              | 25.00         |




