---
title: 減価償却計算の丸め金額
description: このトピックでは、帳簿設定ページの [減価償却の丸め] フィールドについて説明します。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3df48fc7bb092b0257c4652a8c67d1d740dbcfe
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674336"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>減価償却計算の丸め金額

[!include [banner](../includes/banner.md)]

このトピックでは、**帳簿設定** ページにある **減価償却の丸め** フィールドについて説明します。

減価償却の丸め金額は各帳簿で設定されます。 減価償却の丸め金額は、固定資産の将来の減価償却と価値を示す固定資産減価償却プロファイルで使用されます。 この帳簿で許可される減価償却の最小金額を入力します。 

丸め設定に関係なく、最後の減価償却期間の減価償却金額の丸めはおこなわれません。 最後の償却期間の最後に、固定資産の金額は 0 (ゼロ) になるか、または仕損価格を使用する場合は仕損価格となる必要があります。

### <a name="example"></a>例

丸めを使用しない減価償却は、2,444.44 として計算されます。 次の表に示すように、丸めの設定に応じてさまざまな金額が提示されます。

| 丸め方法 | 算出償却額 |
|-----------------|---------------------|
| 0.1 の丸め    | 2,444.40            |
| 1.00 の丸め   | 2,444.00            |
| 10.00 の丸め  | 2,440.00            |
| 100.00 の丸め | 2,400.00            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
