---
title: バッチ上の品目に対して手持在庫が考慮されない
description: 一部のスロット テンプレートでは、バッチ上の品目に対して現在の手持在庫が考慮されません。 バッチ番号またはシリアル番号は、需要オーダーで指定する必要があります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476876"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>スロット テンプレートでは、バッチ上の品目に対して手持在庫が考慮されない

## <a name="symptoms"></a>現象

*オンハンドで考慮* のスロット基準を持つスロット テンプレートでは、*バッチ-上* 品目の現在のオンハンド在庫は考慮されません。 販売注文書でバッチ番号が指定されている場合にのみ考慮されます。

ただし、*バッチ-下* 品目を使用する場合、現在の手持在庫は予定と見なされます。

詳細については、[倉庫スロッティング](/dynamics365/supply-chain/warehousing/warehouse-slotting) を参照してください。

## <a name="resolution"></a>解決策

スロット テンプレート ヘッダーは、*注文済*、*予約済*、または *リリース済* の需要戦略に対して定義できます。 *注文済み* の需要戦略では、倉庫プロセスの予約またはリリースに適用される同じ在庫予約階層の要件が適用されます。 したがって、*バッチ-上* および *シリアル-下* の予約階層を持つ品目については、需要注文 (販売または移動) にバッチ番号またはシリアル番号を指定 する必要があります。

または、倉庫のスロットへ需要が生成される前に、*予約済* 需要戦略を使用してバッチ番号またはシリアル番号 を選択できます。
