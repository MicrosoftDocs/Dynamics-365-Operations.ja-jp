---
title: 一部の仕入先支払の決済、および割引日より前の全額最終支払
description: この記事は、仕入先請求書に対して一部支払が作成され、現金割引が提供されるシナリオについて説明します。
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: angelading
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5af6b47c816686a31015f07c8c81544481fc4433
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715913"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>一部の仕入先支払の決済、および割引日より前の全額最終支払

[!include [banner](../includes/banner.md)]

この記事は、仕入先請求書に対して一部支払が作成され、現金割引が提供されるシナリオについて説明します。

Fabrikam は、仕入先 3064 からの商品を購入します。 請求書が 14 日以内に支払われた場合に、仕入先は Fabrikam に 1 パーセントの現金割引を提供します。 請求書は 30 日以内に支払う必要があります。 仕入先は、Fabrikam が一部支払に対する現金割引を選べるようにすることもできます。 決済のパラメーターは **買掛金勘定パラメーター** ページにあります。 6 月 25 日に、April は、仕入先 3064 に対して 1,000.00 ドルの請求書を入力します。

## <a name="vendor-invoice-on-june-25"></a>6 月 25 日の仕入先請求書
6 月 25 日に、April は仕入先 3064 に対して 1,000.00 ドルの請求書を入力して転記します。 エイプリルはこのトランザクションを **仕入先トランザクション** ページで表示できます。

| 伝票番号   | 日      | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 残高   | 通貨 |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 2015 年 6 月 25 日 | 10010   |                                      | 1,000.00                              | -1,000.00 | USD      |

エイプリルは **仕入先** ページから **トランザクションの決済** ページを開きます。 さらに、現金割引の日付と金額を表示するのに **トランザクションの決済** ページを使用することもできます。 期日は 7 月 25 日で、請求書が 7 月 9 日までに支払われた場合に、-10.00 ドルの現金割引が使用できます。

| マーク | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨の金額 | 通貨 | 決済金額 |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | 標準            | Inv-10010 | 3064    | 2015 年 6 月 25 日 | 2015 年 7 月 25 日 | 10010   | 1,000.00                       | USD      | 990.00           |

割引の情報は **未処理トランザクションの決済** ページの下部に表示されます。

|       &nbsp;                 | &nbsp;    |
|------------------------------|-----------|
| 現金割引日           | 2015/7/9 |
| 現金割引金額         | -10.00    |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 0.00      |
| 適用する現金割引金額 | -10.00    |

エイプリルは **現金割引** タブをクリックし、割引金額を表示します。

| 現金割引日 | 現金割引金額 | トランザクション通貨の金額 |
|--------------------|----------------------|--------------------------------|
| 2015 年 7 月 9 日           | 10.00                | 990.00                         |
| 2015 年 7 月 25 日          | 0.00                 | 1,000.00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>7 月 1 日に [トランザクションの決済] ページを使用して行われる一部支払
エイプリルは、買掛金勘定 **支払仕訳帳** ページを開くことで、この支払のための支払仕訳帳を作成できます。 彼女は、新しい仕訳帳を作成し、仕入先 3064 の行を入力します。 彼女は、請求書を決済のためにマークできるように、**トランザクションの決済** ページを開きます。 さらに、請求書にマークしたり、**決済金額** フィールドの値を **-500.00** に変更したりします。 **現金割引金額** フィールドの値が全請求書に対して **-10.00** であり、**適用する現金割引金額** フィールドの値が **-5.05** であることを確認します。 したがって、April はこの請求書の -505.05 ドルを決済します。

| マーク     | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨の金額 | 通貨 | 決済金額 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 選択済 | 標準            | FTI-10010 | 4028    | 2015 年 6 月 25 日 | 2015 年 7 月 25 日 | 10010   | 1,000.00                       | USD      | -500.00          |

割引の情報は **未処理トランザクションの決済** ページの下部に表示されます。

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| 現金割引日           | 2015/7/9 |
| 現金割引金額         | -10.00    |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 0.00      |
| 適用する現金割引金額 | -5.05     |

エイプリルは請求書の半分を決済するとします。 したがって、請求書にマークしたり、**決済金額** フィールドの値を **-495.00** に変更したりします。 決済合計金額は 500.00 です。 この金額には、-5.00 ドルの現金割引が含まれます。

| マーク     | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨の金額 | 通貨 | 決済金額 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 選択済 | 標準            | FTI-10010 | 4028    | 2015 年 6 月 25 日 | 2015 年 7 月 25 日 | 10010   | 1,000.00                       | USD      | -495.00          |

割引の情報は **未処理トランザクションの決済** ページの下部に表示されます。

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| 現金割引日           | 2015/7/9 |
| 現金割引金額         | -10.00    |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 0.00      |
| 適用する現金割引金額 | -5.00     |

エイプリルは **トランザクションの決済** ページを閉じます。 495.00 ドルの支払明細行が仕訳帳に作成され、April は仕訳帳を転記します。 April は仕入先トランザクションを **仕入先トランザクション** ページで確認できます。 彼女は請求書に -500.00 ドルの残高があることを確認します。 また、495.00 ドルの支払で、5.00 ドルの現金割引があることも確認できます。

| 伝票番号    | トランザクション タイプ | 日      | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 残高 | 通貨 |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | 請求書          | 2015 年 6 月 25 日 | 10010   |                                      | 1,000.00                              | -500.00 | USD      |
| APP-10010  | 支払          | 2015/7/1  |         | 495.00                               |                                       | 0.00    | USD      |
| DISC-10010 | 現金割引    | 2015/7/1  |         | 5.00                                 |                                       | 0.00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>残りの金額が 7 月 8 日に支払われる
April は仕入先 3064 の請求書の残高を現金割引期間の 7 月 8日に支払います。 April は 7 月 8 日に支払仕訳帳を作成し、決済のトランザクションにマークします。 エイプリルは決済する必要がある金額が 495.00 ドルであることを確認します。 5.00 ドルの割引が前に実行されたため、**見積現金割引** フィールドの値は **-5.00** です。

|  &nbsp;                 |  &nbsp; |
|-------------------------|--------|
| マーク済合計            | 495.00 |
| 見積現金割引 | -5.00  |

マークしたトランザクションに関する情報が **未処理トランザクションの決済** ページのグリッドに表示されます。

| マーク     | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨の金額 | 通貨 | 決済金額 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 選択済 | 標準            | FTI-10010 | 4028    | 2015 年 6 月 25 日 | 2015 年 7 月 25 日 | 10010   | 1,000.00                       | USD      | 495.00           |

割引の情報は **未処理トランザクションの決済** ページの下部に表示されます。

|  &nbsp;                      | &nbsp;    |
|------------------------------|-----------|
| 現金割引日           | 2015/7/9 |
| 現金割引金額         | 10.00     |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 5.00      |
| 適用する現金割引金額 | 5.00      |

エイプリルは支払仕訳帳を転記し、仕入先トランザクションを **仕入先トランザクション** ページで確認します。 請求書の残高は 0.00 ドルになり、Apirl は 2 回の支払と 2 種類の現金割引を確認できます。

| 伝票番号    | トランザクション タイプ | 日      | 請求書 | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 残高 | 通貨 |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | 請求書          | 2015 年 6 月 25 日 | 10010   |                                      | 1,000.00                              | 0.00    | USD      |
| APP-10010  |  支払         | 2015/7/1  |         | 495.00                               |                                       | 0.00    | USD      |
| DISC-10010 | 現金割引    | 2015/7/1  |         | 5.00                                 |                                       | 0.00    | USD      |
| APP-10011  | 支払          | 2015/7/8  |         | 495.00                               |                                       | 0.00    | USD      |
| DISC-10011 | 現金割引    | 2015/7/8  |         | 5.00                                 |                                       | 0.00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
