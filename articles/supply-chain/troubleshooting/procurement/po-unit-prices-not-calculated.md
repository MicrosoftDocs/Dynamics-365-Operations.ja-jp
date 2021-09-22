---
title: 発注書の単価が、単位換算に基づいて計算されない
description: 発注書の単価が、単位換算に基づいて計算されない
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476871"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>発注書の単価が、単位換算に基づいて計算されない

## <a name="symptoms"></a>現象

発注書の単位が変更された場合、売買契約価格は単位換算定義に従って再計算されません。

## <a name="cause"></a>原因

価格は常に売買契約 (または販売契約書や品目価格などのシステム内のその他の価格設定) から取得され、単位に対して設定されます。

注文明細行で単位が変更されると、システムは新しい単位の価格を検索し、その価格を適用します。 単位の価格が見つからない場合は、システムは価格を適用しません。 単位換算を使用して、価格を別の単位に再計算することはできません。 理論的には、10 個入りの 1 箱の価格は、1 箱の価格の 10 倍と等しくない場合があります。

## <a name="workaround"></a>回避策

この問題を回避する 1 つの方法は、品目の注文明細行で使用されると予想される単位の売買契約があることを確認することです。
