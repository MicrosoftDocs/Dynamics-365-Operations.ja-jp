---
title: 請求金額送信機能を使用して別の店舗から注文を出荷
description: このトピックでは、請求金額の送信機能について説明します。
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800474"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>請求金額送信機能を使用して別の店舗から注文を出荷

[!include [banner](includes/banner.md)]

Commerce の請求金額送信機能で、顧客注文を 1 つの店舗で受けて、別の店舗から出荷することができます。

小売販売時点管理 (POS) クライアントでの顧客注文は、複数の調達オプションをサポートします。 調達のためのオプションの例を示します。

- 別の日付に、同じ店舗から集荷します。
- 同じ日付または異なる日付に、別の店から集荷します。
- その店舗に割り当てられている既定の出荷倉庫から出荷し、特定の日付に配送します。

請求金額送信機能は次の POS 操作を使用しています。すべての製品を出荷および選択した製品を出荷します。 これにより、店舗担当者は注文または注文明細行を充当する「出荷元」の場所を選択できます。 既定では、「出荷元」の場所は、店舗に関連付けられている出荷倉庫です。 ただし、店舗担当者は、この場所を変更し、店舗に割り当てられた店舗ロケーター グループで定義されている店舗を選択することができます。

「出荷先」アドレスを選択する機能は変わりません。

注文明細行を処理するために使用できる出荷方法は、製品と住所の有効な荷渡方法の設定に基づいています。 荷渡方法の有効性に関するルールは、本社 (HQ) でのみ維持されるため、POS クライアントは出荷明細行の有効な荷渡方法を取得するためにリアルタイムの呼び出しを行います。


[!INCLUDE[footer-include](../includes/footer-banner.md)]