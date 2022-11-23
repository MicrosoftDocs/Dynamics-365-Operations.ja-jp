---
title: 仕入先支払の計算済の割引よりも大幅な割引を行う
description: この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。 このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd74c6677f80a9075449908411350f1c81b95b02
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778360"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>仕入先支払の計算済の割引よりも大幅な割引を行う

[!include [banner](../includes/banner.md)]

この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。 このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。 

請求書が 7 日以内に支払われた場合に、仕入先 3051 が Fabrikam に 4 パーセントの現金割引を提供します。 6 月 29 日に、April は 1,000.00 ドルの請求書を入力します。 仕入先は、April が請求書に対して既定の 40.00 ドルの割引の代わりに 60.00 ドルの割引を受けるようにします。 April は、買掛金勘定支払仕訳帳を使用して 1 回限りの支払を記録します。 彼女は支払の仕入先を入力し、**トランザクションの決済** ページを開きます。 さらに、請求書にマークしたり、**現金割引金額** フィールドの値を **-60.00** に変更したりします。

| マーク     | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨の金額 | 通貨 | 決済金額 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 選択済 | 標準            | Inv-10040 | 3051    | 2020/6/29 | 2020/7/29 | 10040   | 1,000.00                       | USD      | 940.00           |

割引の情報は **トランザクションの決済** ページの下部に表示されます。

| フィールド                        | 値     |
|------------------------------|-----------|
| 現金割引日           | 2020/7/12 |
| 現金割引金額         | 60.00     |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 0.00      |
| 適用する現金割引金額 | 60.00     |

April は支払仕訳帳を転記します。 940.00 ドルの支払と 60.00 ドルの割引で請求書を完済します。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
