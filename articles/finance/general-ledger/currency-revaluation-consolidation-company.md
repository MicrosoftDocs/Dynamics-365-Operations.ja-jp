---
title: 連結会社の通貨再評価
description: この記事では、連結会社の通貨を再評価する方法について説明します。
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779665"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>連結会社の通貨再評価

[!include [banner](../includes/banner.md)]

1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。 最初にデータを連結する場合、**為替換算** タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。 新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。 未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。 次の例では、プロセス中に作成された勘定項目を示します。

## <a name="company-setup"></a>会社設定
-   **ソース / 営業会社 (USMF)** – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。
-   **連結会社 (CON)** – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。
    -   **実現利益** – 勘定科目 801500
    -   **実現損失** – 勘定科目 801600
    -   **未実現利益** – 勘定科目 801600
    -   **未実現損失** – 勘定科目 801400

## <a name="original-transactions"></a>元のトランザクション
### <a name="cash-receipt-transactions-in-usmf"></a>[USMF] の現金領収トランザクション

| 日       | 勘定科目               | 通貨 | 数量 |
|------------|------------------------------|----------|--------|
| 10/11/2020 | 110110 – 現金                | USD      | 500    |
| 10/11/2020 | 130100 – [売掛金勘定] | USD      | -500   |

## <a name="exchange-rates"></a>為替レート

| 交換前通貨 | 交換後通貨 | 開始日 | 為替レート |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2020  | 200           |
| EUR           | USD         | 11/1/2020  | 150           |
| EUR           | USD         | 12/1/2017  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>2020 年 10 月の連結を実行
### <a name="balances-in-the-consolidation-company"></a>連結会社の残高

| 勘定科目 | 通貨 | 金額 | 計算    |
|----------------|----------|--------|----------------|
| 110110         | EUR / EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR / EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>2020 年 10 月1 日から 2020 年 11 月 30 日の勘定の通貨再評価を実行
### <a name="balances-in-the-consolidation-company"></a>連結会社の残高

| 勘定科目 | 通貨 | 金額  | 計算                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR / EUR      | 333.33  | 元の金額 500 × 66.6667%  |
| 130100         | EUR / EUR      | -333.33 | 元の金額 -500 × 66.6667% |
| 801400         | EUR / EUR      | 83.33   | 333.33 – 250                       |
| 801600         | EUR / EUR      | -83.33  | -333.33 – (-250)                   |

レポート通貨の金額に対する追加トランザクションが表示されます。

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>2020 年 10 月1 日から 2020 年 12 月 31 日の勘定の通貨再評価を実行
### <a name="balances-in-the-consolidation-company"></a>連結会社の残高

| 勘定科目 | 通貨 | 金額  | 計算                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR / EUR      | 500.00  | 元の金額 500 × 1                           |
| 130100         | EUR / EUR      | -500.00 | 元の金額 -500 × 1                          |
| 801400         | EUR / EUR      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | EUR / EUR      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
