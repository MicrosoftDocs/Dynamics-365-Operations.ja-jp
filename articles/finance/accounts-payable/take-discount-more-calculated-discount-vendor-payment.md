---
title: 仕入先支払の計算済の割引よりも大幅な割引を行う
description: この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。 このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ee74bad071d546724f6ffe336bbe3bdf47e2a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971906"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>仕入先支払の計算済の割引よりも大幅な割引を行う

[!include [banner](../includes/banner.md)]

この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。 このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。 

請求書が 7 日以内に支払われた場合に、仕入先 3051 が Fabrikam に 4 パーセントの現金割引を提供します。 6 月 29 日に、April は 1,000.00 ドルの請求書を入力します。 仕入先は、April が請求書に対して既定の 40.00 ドルの割引の代わりに 60.00 ドルの割引を受けるようにします。 April は、買掛金勘定支払仕訳帳を使用して 1 回限りの支払を記録します。 彼女は支払の仕入先を入力し、**トランザクションの決済** ページを開きます。 さらに、請求書にマークしたり、**現金割引金額** フィールドの値を **-60.00** に変更したりします。

| マーク     | 現金割引の使用 | 伝票番号   | 口座 | 日      | 期日  | 請求書 | トランザクション通貨の金額 | 通貨 | 決済金額 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 選択済 | 標準            | Inv-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1,000.00                       | USD      | 940.00           |

割引の情報は **トランザクションの決済** ページの下部に表示されます。

|                              |           |
|------------------------------|-----------|
| 現金割引日           | 7/12/2015 |
| 現金割引金額         | 60.00     |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 0.00      |
| 適用する現金割引金額 | 60.00     |

April は支払仕訳帳を転記します。 940.00 ドルの支払と 60.00 ドルの割引で請求書を完済します。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]