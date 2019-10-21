---
title: 連結会社の通貨再評価
description: このトピックでは、連結会社の通貨を再評価する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178621"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>連結会社の通貨再評価

[!include [banner](../includes/banner.md)]

1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。 最初にデータを連結する場合、**為替換算**タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。 新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。 未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。 次の例では、プロセス中に作成された勘定項目を示します。

## <a name="company-setup"></a>会社設定
-   **ソース / 営業会社 (USMF)** – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。
-   **連結会社 (CON)** – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。
    -   **実現利益** – 勘定科目 801500
    -   **実現損失** – 勘定科目 801600
    -   **未実現利益** – 勘定科目 801600
    -   **未実現損失** – 勘定科目 801400

## <a name="original-transactions"></a>元のトランザクション
### <a name="cash-receipt-transactions-in-usmf"></a>[USMF] の現金領収トランザクション

| 日       | 勘定科目               | 通貨 | 金額 |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 – 現金                | USD      | 500    |
| 10/11/2015 | 130100 – [売掛金勘定] | USD      | -500   |

## <a name="exchange-rates"></a>為替レート

| 開始通貨 | 終了通貨 | 開始日 | 為替レート |
|---------------|-------------|------------|---------------|
| EUR / EUR           | USD         | 10/1/2015  | 200           |
| EUR / EUR           | USD         | 11/1/2015  | 150           |
| EUR / EUR           | USD         | 12/1/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>2015 年 10 月の連結を実行
### <a name="balances-in-the-consolidation-company"></a>連結会社の残高

| 勘定科目 | 通貨 | 金額 | 計算    |
|----------------|----------|--------|----------------|
| 110110         | EUR / EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR / EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>2015 年 10 月1 日から 2015 年 11 月 30 日の勘定の通貨再評価を実行
### <a name="balances-in-the-consolidation-company"></a>連結会社の残高

| 勘定科目 | 通貨 | 金額  | 計算                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR / EUR      | 333.33  | 元の金額 500 × 66.6667%  |
| 130100         | EUR / EUR      | -333.33 | 元の金額 -500 × 66.6667% |
| 801400         | EUR / EUR      | 83.33   | 333.33 – 250                       |
| 801600         | EUR / EUR      | -83.33  | -333.33 – (-250)                   |

レポート通貨の金額に対する追加トランザクションが表示されます。

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>2015 年 10 月1 日から 2015 年 12 月 31 日の勘定の通貨再評価を実行
### <a name="balances-in-the-consolidation-company"></a>連結会社の残高

| 勘定科目 | 通貨 | 金額  | 計算                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR / EUR      | 500.00  | 元の金額 500 × 1                           |
| 130100         | EUR / EUR      | -500.00 | 元の金額 -500 × 1                          |
| 801400         | EUR / EUR      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | EUR / EUR      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |





