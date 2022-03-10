---
title: '[品目価格] ページの [有効な価格] タブに [開始日] の値がない'
description: '[品目価格] ページの [有効な価格] タブに [開始日] の値がありません。'
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730133"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>[品目価格] ページの [有効な価格] タブに [開始日] の値がない

KB 番号: 4613548

## <a name="symptoms"></a>現象

**品目価格** ページの **有効な価格** タブに **開始日** の値がありません。

## <a name="resolution"></a>解像度

保留中の価格で設定されている **開始日** の値 (有効日) は、有効な価格に転送されません。

品目の原価レコードを初期入力すると、*保留中* ステータスであり、発効日が設定されています。 品目の原価レコードを有効にすると、ステータスは *有効* に更新され、発効日は有効化した日に更新されます。 したがって、有効な価格の有効化日付は、常に有効化の実際の日付です。

詳細については、[原価計算バージョンの概要](../../cost-management/costing-versions.md)を参照してください。
