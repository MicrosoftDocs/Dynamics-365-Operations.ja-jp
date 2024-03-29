---
title: 複数の割引期間にまたがる複数の請求書決済に、1 回の支払いを使用する
description: この記事では、各請求書に現金割引の資格がある場合に、複数の請求書の支払方法を示します。 この記事のシナリオでは、支払いのタイミングによって実行される現金の割引がどのように変化するかを重点的に解説します。
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bf321a5b0511295f2500f10cdffa9ff6f043bff
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780542"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>複数の割引期間にまたがる複数の請求書決済に、1 回の支払いを使用する

[!include [banner](../includes/banner.md)]

この記事では、各請求書に現金割引の資格がある場合に、複数の請求書の支払方法を示します。 この記事のシナリオでは、支払いのタイミングによって実行される現金の割引がどのように変化するかを重点的に解説します。

Fabrikam は顧客 4032 に商品を販売します。 Fabrikam は、請求書の支払が 14 日以内に行われた場合に、1 パーセントの現金割引を提供します。 Fabrikam は、一部支払に対する現金割引も提供します。 決済のパラメーターは **売掛金勘定パラメーター** ページにあります。

## <a name="invoices"></a>請求書
顧客 4032 は合計が 3,000.00 になる 3 つの請求書があります:

-   1,000.00 ドルの請求書 FTI-10040 は 5 月 15 日に入力されました。 この請求書は、14 日以内に支払われた場合には、1% の現金割引の適用対象となります。
-   1,000.00 ドルの請求書 FTI-10041 は 6 月 25 日に入力されました。 この請求書は、14 日以内に支払われた場合には、1% の現金割引の適用対象となります。
-   1,000.00 ドルの請求書 FTI-10042 は 6 月 25 日に入力されました。 この請求書は、5 日以内に支払われた場合には 2% の、14 日以内に支払われた場合には 1% の現金割引の適用対象となります。

## <a name="settle-all-invoices-on-june-29"></a>6 月 29 日にすべての請求書を決済
これらの請求書を 6 月 29 日に全額決済する支払仕訳帳をアーニーが作成した場合、支払は 2,970.00 ドルとなります。 すべての割引金額の合計は 30.00 ドルになります。 アーニーは、顧客 4032 の支払を作成し、**トランザクションの決済** ページを開きます。 **トランザクションの決済** ページで、アーニーは決済する 3 つの請求明細行をすべてマークします:

-   請求書 FTI-10040 の支払は 1,000.00 になります。 現金割引は適用されません。
-   請求書 FTI-10041 の支払は 990.00 になります。 1% の現金割引、つまり 10.00 が取得されます。
-   請求書 FTI-10042 の支払は 980.00 になります。 2% の現金割引、つまり 20.00 が取得されます。

| マーク | 現金割引の使用 | 伝票番号   | 口座 | 日   | 期日  | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 通貨 | 決済金額 |
|------|----------|-----------|---------|-----------|-----------|---------|---------------------|---------------------|----------|------------------|
| 選択済     | 標準      | FTI-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00  |                    | USD      | 1,000.00         |
| 選択済     | 標準      | FTI-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00  |                    | USD      | 990.00           |
| 選択済みかつ強調表示 | 標準      | FTI-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00    |              | USD      | 980.00           |

支払の転記後に、顧客残高は 0.00 になります。

## <a name="settle-all-invoices-on-july-1"></a>7 月 1 日にすべての請求書を決済
これらの請求書を 7 月 1 日に全額決済する支払仕訳帳をアーニーが作成した場合、支払は 2,980.00 ドルとなります。 アーニーは、顧客 4032 の支払を作成し、**トランザクションの決済** ページを開きます。 **トランザクションの決済** ページで、アーニーは決済する 3 つの請求明細行をすべてマークします:

-   請求書 FTI-10040 の支払は 1,000.00 になります。 現金割引は適用されません。
-   請求書 FTI-10041 の支払は 990.00 になります。 1% の現金割引、つまり 10.00 が取得されます。
-   請求書 FTI-10042 の支払は 990.00 になります。 1% の現金割引、つまり 10.00 が取得されます。 7 月 1 日は 2% の割引期間の適用が終了していますが、まだ 1% の割引の適用期間内にあります。

| マーク                     | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 通貨 | 決済金額 |
|----------|---------|-----------|---------|-----------|-----------|---------|--------------------|------------------|----------|------------------|
| 選択済         | 標準            | FTI-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00         |                | USD      | 1,000.00         |
| 選択済                 | 標準            | FTI-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00  |               | USD      | 990.00           |
| 選択済みかつ強調表示 | 標準            | FTI-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00  |             | USD      | 990.00           |

## <a name="partial-settlement-on-june-29"></a>6 月 29 日に部分決済
顧客 4032 は、各請求書の金額の半分など、一部金額を支払うことができます。 アーニーは、顧客 4032 の支払を作成し、**トランザクションの決済** ページを開きます。 **トランザクションの決済** ページで、アーニーは決済する 3 つの請求明細行をすべてマークします。 各行で、アーニーが指定した注文に基づいて、決済する金額を入力します。 アーニーは明細行を選択して、その明細行の割引金額と適用される現金割引金額を確認します。 顧客が請求書の金額の半分を支払うので、アーニーは FTI-10042 の **現金割引金額** フィールドの値が **20.00** ドル、**適用される現金割引** フィールドの値が **10.00** ドルであるのを確認します。 支払額は 1,485.00 ドルとなります。

| マーク   | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 通貨 | 決済金額 |
|-------------|-------------------|-----------|---------|-----------|-----------|---------|-----------|------------------|----------|------------------|
| 選択済   | 標準       | FTI-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00        |               | USD      | 500.00           |
| 選択済                 | 標準            | FTI-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00     |     | USD      | 495.00           |
| 選択済みかつ強調表示 | 標準            | FTI-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00     |         | USD      | 490.00           |

アーニーはまた、**トランザクションの決済** ページを開く前に、手動で 1,485.00 の支払額を入力します。 もしアーニーが手動で支払金額の入力と、3 つのトランザクションすべてのマークは行い、各トランザクションの **決済金額** フィールドの値の調整は行っていない場合は、ページを閉じる時に次のメッセージが表示されます。

> マークされたトランザクションの合計金額は仕訳帳金額とは異なります。  仕訳帳金額を変更しますか?

アーニーが支払額を 1,485.00 ドルだけにする必要がある場合は、**なし** をクリックしてから仕訳帳を転記します。 トランザクションは次のように決済されます。

1.  請求書 FTI-10040 は 5 月 15 日に入力された最も古い請求書なので、1,000.00 ドルで全額決済されます。 現金割引は適用されません。 支払トランザクションの残高は 485.00 ドルです。
2.  請求書 FTI-10041 はまったく決済されません。 請求書 FTI-10041 と FTI-10042 は同じ日付で入力されました。 ただし、請求書 FTI-10041 は 1% の割引を、請求書 FTI-10042 は 2% の割引を利用できます。 請求書 FTI-10042 ではより良い割引を利用できるので、残りの 485.00 ドルは FTI-10042 請求書で決済されます。
3.  請求書 FTI-10042 は、残りの 485.00 ドルで決済されます。 Fabrikam は部分割引を提供します。 この場合、割引は 9.90 です (= 485.00 ÷ 0.98 × 0.02)。 2% の割引があり、顧客は請求書の 98% を支払うことになるので、金額 (485.00) は 0.98 で割ることによって求められます。 結果に割引率 (2%) が乗じられます。 485.00 ドルの支払に 9.90 ドルの割引を加算すると 494.90 ドルとなります。 元の請求金額は 1,000.00 ドルでした。 従って、トランザクションの残高は、505.10 ドルとなります (= 1,000.00 – 494.90)。

アーニーはこの情報を **顧客トランザクション** ページで表示できます。

| 伝票番号    | トランザクション タイプ | 日      | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 残高  | 通貨 |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | 請求書          | 5/15/2020 | 10040   | 1,000.00                             |                                       | 0.00     | USD      |
| FTI-10041  | 請求書          | 6/25/2020 | 10041   | 1,000.00                             |                                       | 1,000.00 | USD      |
| FTI-10042  | 請求書          | 6/25/2020 | 10042   | 1,000.00                             |                                       | 505.10   | USD      |
| ARP-10040  | 支払          | 6/29/2020 |         |                                      | 1,485.00                              | 0.00     | USD      |
| DISC-10040 | 現金割引    | 6/29/2020 |         |                                      | 9.90                                  | 0.00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
