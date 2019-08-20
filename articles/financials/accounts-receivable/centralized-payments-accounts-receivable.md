---
title: 売掛金勘定の集中支払
description: 複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。 したがって、同じトランザクションを複数の法人に入力する必要はありません。 この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59942fadb0fb702c59c95f75359f1a3036e4668f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836895"
---
# <a name="centralized-payments-for-accounts-receivable"></a>売掛金勘定の集中支払

[!include [banner](../includes/banner.md)]

複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。 したがって、同じトランザクションを複数の法人に入力する必要はありません。 この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。

複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。 したがって、同じトランザクションを複数の法人に入力する必要はありません。 また、組織は、支払提案、決済、および集中支払用の未処理および決算済トランザクションを編集するプロセスが合理化されるため、時間を節約できます。 

集中支払組織では、事業を行うために多くの法人があり、事業を行っている各法人がそれぞれの請求書売掛金情報を管理します。 事業を行っているすべての法人の支払は、支払の法人として知られている 1 つの法人が受け取ります。 決済プロセス中に、適切な借りトランザクションと貸しトランザクションが生成されます。 組織内のどの法人が実利益トランザクションと実損失トランザクションを受け取るか、また、集中支払に関連する現金割引トランザクションの処理方法を指定できます。 集中支払仕訳明細行で、**勘定タイプ**は顧客 に設定する必要があります。 **相手勘定タイプ**は銀行または元帳に設定する必要があります。 銀行口座は現在の会社にあるはずです。 

次の各例で、さまざまなシナリオにおける転記の処理方法を示します。 これらすべての例について、次の構成が想定されます。

-   法人は Fabrikam、Fabrikam East、および Fabrikam West です。 顧客支払が Fabrikam に入力されます。
-   **会社間会計**ページの**現金割引の転記**フィールドには**請求書の法人**が設定されます。
-   **会社間会計**ページの**為替差益または差損の転記**フィールドには**請求書の支払**が設定されます。
-   顧客の Northwind Traders は、各法人の顧客として設定されます。 さまざまな法人の顧客は同一のグローバル アドレス帳 ID を共有するため、同じ顧客として識別されます。

| アドレス帳 ID | 顧客口座 | 氏名              | 個法  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam East |
| 4050            | 10000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>例 1: 別の法人からの請求書の顧客支払
Fabrikam は、Fabrikam 顧客 ID 4000 の Northwind Traders について 600.00 の支払を受け取ります。 支払は、Fabrikam East の顧客 ID 4000 に対する未処理請求書で決済されます。

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>顧客 4000 について請求書が Fabrikam East で転記される

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売掛金 (Fabrikam East) | 600.00       |               |
| 売上 (Fabrikam East)               |              | 600.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>顧客 4000 について支払が Fabrikam で受領および転記される

| アカウント                        | 借方金額 | 貸方金額 |
|--------------------------------|--------------|---------------|
| 現金 (Fabrikam)                | 600.00       |               |
| 売掛金 (Fabrikam) |              | 600.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam の支払が Fabrikam East の請求書で決済される

**Fabrikam の転記**

| アカウント                         | 借方金額 | 貸方金額 |
|---------------------------------|--------------|---------------|
| 売掛金 (Fabrikam)  | 600.00       |               |
| Fabrikam East への貸し (Fabrikam) |              | 600.00        |

**Fabrikam East の転記**

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| Fabrikam からの借り (Fabrikam East)   | 600.00       |               |
| 売掛金 (Fabrikam East) |              | 600.00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>例 2: 現金割引のある別の法人からの請求書の顧客支払
Fabrikam は、Fabrikam 顧客 4000 の Northwind Traders について 580.00 の支払を受け取ります。 Fabrikam East には、顧客 4000 の未処理請求書があります。 請求書には 20.00 の現金割引があります。 支払は、未処理の Fabrikam East 請求書で決済されます。 現金割引が請求書、Fabrikam East の法人に転記されます。

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Fabrikam East の顧客 4000 について請求書が Fabrikam East で転記される

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売掛金 (Fabrikam East) | 600.00       |               |
| 売上 (Fabrikam East)               |              | 600.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Fabrikam 顧客 4000 について支払が Fabrikam で受領および転記される

| アカウント                        | 借方金額 | 貸方金額 |
|--------------------------------|--------------|---------------|
| 現金 (Fabrikam)                | 600.00       |               |
| 売掛金 (Fabrikam) |              | 600.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam の支払が Fabrikam East の請求書で決済される

**Fabrikam の転記**

| アカウント                         | 借方金額 | 貸方金額 |
|---------------------------------|--------------|---------------|
| 売掛金 (Fabrikam)  | 580.00       |               |
| Fabrikam East への貸し (Fabrikam) |              | 580.00        |

**Fabrikam East の転記**

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| Fabrikam からの借り (Fabrikam East)   | 580.00       |               |
| 売掛金 (Fabrikam East) |              | 580.00        |
| 現金割引 (Fabrikam East)       | 20.00        |               |
| 売掛金 (Fabrikam East) |              | 20.00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>例 3: 実為替レート差益のある別の法人からの請求書の顧客支払
Fabrikam は、Fabrikam 顧客 4000 の Northwind Traders について 600.00 EUR の支払を受け取ります。 支払は、Fabrikam East の顧客 4000 に対する未処理請求書で決済されます。 決済プロセス時に、通貨為替差益トランザクションが生成されます。

-   請求日時点での EUR から米国ドル (USD) への為替レート : 1.2062
-   支払日時点での EUR から USD への為替レート : 1.2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Fabrikam East の顧客 4000 について請求書が Fabrikam East で転記される

| アカウント                             | 借方金額            | 貸方金額           |
|-------------------------------------|-------------------------|-------------------------|
| 売掛金 (Fabrikam East) | 600.00 EUR / 723.72 USD |                         |
| 売上 (Fabrikam East)               |                         | 600.00 EUR / 723.72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Fabrikam の顧客 4000 について支払が Fabrikam で受領および転記される

| アカウント                        | 借方金額            | 貸方金額           |
|--------------------------------|-------------------------|-------------------------|
| 現金 (Fabrikam)                | 600.00 EUR / 736.62 USD |                         |
| 売掛金 (Fabrikam) |                         | 600.00 EUR / 736.62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam の支払が Fabrikam East の請求書で決済される

**Fabrikam の転記**

| アカウント                         | 借方金額            | 貸方金額           |
|---------------------------------|-------------------------|-------------------------|
| 売掛金 (Fabrikam)  | 600.00 EUR / 736.62 USD |                         |
| Fabrikam East への貸し (Fabrikam) |                         | 600.00 EUR / 736.62 USD |
| Fabrikam East への貸し (Fabrikam) | 0.00 EUR / 12.90 USD    |                         |
| 実利益 (Fabrikam)        |                         | 0.00 EUR / 12.90 USD    |

**Fabrikam East の転記**

| アカウント                             | 借方金額            | 貸方金額           |
|-------------------------------------|-------------------------|-------------------------|
| Fabrikam からの借り (Fabrikam East)   | 600.00 EUR / 736.62 USD |                         |
| 売掛金 (Fabrikam East) |                         | 600.00 EUR / 736.62 USD |
| 売掛金 (Fabrikam East) | 0.00 EUR / 12.90 USD    |                         |
| Fabrikam からの借り (Fabrikam East)   |                         | 0.00 EUR / 12.90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>例 4: 現金割引と実為替レート差益のある別の法人からの請求書の顧客支払
Fabrikam は、Fabrikam 顧客 4000 の Northwind Traders について、Fabrikam East での未処理請求書の支払を転記します。 請求書には現金割引があり、売上税トランザクションが生成されます。 支払は、未処理の Fabrikam East 請求書で決済されます。 決済プロセス時に、通貨為替差益トランザクションが生成されます。 現金割引が請求の法人 (Fabrikam East) に転記され、通貨為替差益が支払の法人 (Fabrikam) に転記されます。

-   請求日時点での EUR から USD への為替レート : 1.2062
-   支払日時点での EUR から USD への為替レート : 1.2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>顧客 4000 について、Fabrikam East で自由書式の請求書が転記され、税金トランザクションが生成される

| アカウント                             | 借方金額            | 貸方金額           |
|-------------------------------------|-------------------------|-------------------------|
| 売掛金 (Fabrikam East) | 638.22 EUR / 769.82 USD |                         |
| 売上 (Fabrikam East)               |                         | 600.00 EUR / 723.72 USD |
| 売上税 (Fabrikam East)           |                         | 38.22 EUR / 46.10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>顧客 4000 について支払が Fabrikam で受領および転記される

| アカウント                        | 借方金額            | 貸方金額           |
|--------------------------------|-------------------------|-------------------------|
| 現金 (Fabrikam)                | 626.22 EUR / 768.81 USD |                         |
| 売掛金 (Fabrikam) |                         | 626.22 EUR / 768.81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam の支払が Fabrikam East の請求書で決済される

**Fabrikam の転記**

| アカウント                         | 借方金額            | 貸方金額           |
|---------------------------------|-------------------------|-------------------------|
| 売掛金 (Fabrikam)  | 626.22 EUR / 768.81 USD |                         |
| Fabrikam East への貸し (Fabrikam) |                         | 626.22 EUR / 768.81 USD |
| Fabrikam East への貸し (Fabrikam) | 0.00 EUR / 13.46 USD    |                         |
| 実利益 (Fabrikam)        |                         | 0.00 EUR / 13.46 USD    |

**Fabrikam East の転記**

| アカウント                             | 借方金額            | 貸方金額           |
|-------------------------------------|-------------------------|-------------------------|
| Fabrikam からの借り (Fabrikam East)   | 626.22 EUR / 768.81 USD |                         |
| 売掛金 (Fabrikam East) |                         | 626.22 EUR / 768.81 USD |
| 売掛金 (Fabrikam East)  | 0.00 EUR / 13.46 USD    |                         |
| Fabrikam からの借り (Fabrikam East)   |                         | 0.00 EUR / 13.46 USD    |
| 現金割引 (Fabrikam East)       | 12.00 EUR / 14.47 USD   |                         |
| 売掛金 (Fabrikam East) |                         | 12.00 EUR / 14.47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>例 5 : 基本支払のある顧客貸方票
Fabrikam は、顧客 4000 の Northwind Traders について 75.00 の支払を受け取ります。 支払は、Fabrikam West の顧客 10000 に対する未処理請求書および Fabrikam East の顧客 4000 に対する未処理の貸方票で決済されます。 支払は、**トランザクションの決済** ページで基本支払として選択されています。

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>顧客 10000 について請求書が Fabrikam West に転記される

| 口座                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売掛金 (Fabrikam West) | 100.00       |               |
| 売上 (Fabrikam West)               |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>顧客 4000 について貸方票が Fabrikam East に転記される

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売上返品 (Fabrikam East)       | 25.00        |               |
| 売掛金 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>顧客 4000 について支払が Fabrikam に転記される

| アカウント                        | 借方金額 | 貸方金額 |
|--------------------------------|--------------|---------------|
| 現金 (Fabrikam)                | 75.00        |               |
| 売掛金 (Fabrikam) |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam の支払が、Fabrikam West の請求書と Fabrikam East の貸方票で決済される

**Fabrikam の転記**

| アカウント                           | 借方金額 | 貸方金額 |
|-----------------------------------|--------------|---------------|
| Fabrikam East からの借り (Fabrikam) | 25.00        |               |
| 売掛金 (Fabrikam)    |              | 25.00         |
| 売掛金 (Fabrikam)    | 100.00       |               |
| Fabrikam West への貸し (Fabrikam)   |              | 100.00        |

**Fabrikam East の転記**

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売掛金 (Fabrikam East) | 25.00        |               |
| Fabrikam への貸し (Fabrikam East)     |              | 25.00         |

**Fabrikam West の転記**

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| Fabrikam からの借り (Fabrikam West)   | 100.00       |               |
| 売掛金 (Fabrikam West) |              | 100.00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>例 6 : 基本支払のない顧客貸方票
Fabrikam は、顧客 4000 の Northwind Traders について 75.00 の支払を受け取ります。 支払は、Fabrikam West の顧客 10000 に対する未処理請求書および Fabrikam East の顧客 4000 に対する未処理の貸方票で決済されます。 支払は、**トランザクションの決済** ページでは基本支払として選択されません。

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>顧客 10000 について請求書が Fabrikam West に転記される

| 口座                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売掛金 (Fabrikam West) | 100.00       |               |
| 売上 (Fabrikam West)               |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>顧客 4000 について貸方票が Fabrikam East に転記される

| アカウント                             | 借方金額 | 貸方金額 |
|-------------------------------------|--------------|---------------|
| 売上返品 (Fabrikam East)       | 25.00        |               |
| 売掛金 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>顧客 4000 について支払が Fabrikam に転記される

| アカウント                        | 借方金額 | 貸方金額 |
|--------------------------------|--------------|---------------|
| 現金 (Fabrikam)                | 75.00        |               |
| 売掛金 (Fabrikam) |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam の支払が、Fabrikam West の請求書と Fabrikam East の貸方票で決済される

**Fabrikam の転記**

| アカウント                         | 借方金額 | 貸方金額 |
|---------------------------------|--------------|---------------|
| 売掛金 (Fabrikam)  | 75.00        |               |
| Fabrikam West への貸し (Fabrikam) |              | 75.00         |

**Fabrikam East の転記**

| アカウント                              | 借方金額 | 貸方金額 |
|--------------------------------------|--------------|---------------|
| 売掛金 (Fabrikam East)  | 25.00        |               |
| Fabrikam West への貸し (Fabrikam East) |              | 25.00         |

**Fabrikam West の転記**

| アカウント                                | 借方金額 | 貸方金額 |
|----------------------------------------|--------------|---------------|
| Fabrikam からの借り (Fabrikam West)      | 75.00        |               |
| 売掛金 (Fabrikam West)    |              | 75.00         |
| Fabrikam East からの借り (Fabrikam West) | 25.00        |               |
| 売掛金 (Fabrikam West)    |              | 25.00         |
