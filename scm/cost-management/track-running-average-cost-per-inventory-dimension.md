---
title: "在庫分析コード当たりの移動平均原価の追跡"
description: "在庫分析コード グループは各在庫品目に割り当てられています。 したがって、品目の移動平均原価価格は、財務的に追跡されている在庫分析コードの選択に基づいて計算されます。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4f5ca047835fcbb2567f0b97347b356e1b594980
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>在庫分析コード当たりの移動平均原価の追跡

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


在庫分析コード グループは各在庫品目に割り当てられています。 したがって、品目の移動平均原価価格は、財務的に追跡されている在庫分析コードの選択に基づいて計算されます。

在庫分析コードは製品、保管、および追跡の 3 種類があります。 製品分析コードは、コンフィギュレーション、サイズ、および色が含まれます。 製品分析コードは常に財務的に追跡されます。 保管と追跡用分析コードは、サイト、倉庫、場所、在庫状態、ライセンス プレート、バッチ番号、シリアル番号を含みます。 どの保管と追跡用分析コードが財務的に追跡されるかを指定できます。 

**例 1** 

品目に添付されている保管分析コード グループが倉庫によって財務的に追跡されている場合、移動平均原価価格は倉庫ごとに計算されます。 次の購買注文が請求されています。

-   原価価格が USD 10.00 で数量が 2 の発注書が倉庫 GW に対して請求されています。
-   原価価格が USD 12.00 で数量が 3 の発注書が倉庫 GW に対して請求されています。
-   原価価格が USD 15.00 で数量が 5 の発注書が倉庫 MW に対して請求されています。

倉庫 GW の移動平均原価価格は USD 11.20 で、倉庫 MW の移動平均原価価格は USD 15.00 です。 販売注文請求書が倉庫 GW に対して転記されます。 在庫と売却済商品の原価の価値 (在庫決算が実行される前で、マークがない) は、USD 11.20 です。 別の販売注文が倉庫 MW に対して転記されます。 在庫と売却済商品の原価の価値 (在庫決算が実行される前で、マークがない) は、USD 15.00 です。 

**例 2** 品目に関連付けられている保管分析コード グループが倉庫によって財務的に追跡され、また追跡用分析コード グループがバッチ番号によって財務的に追跡されている場合、移動平均原価価格はバッチごとに計算されます。 

**注記:** すべての財務分析コードを追跡して、原価価格を常に表示することをお勧めします。 次の購買注文が請求されています。

-   原価価格が USD 10.00 で数量が 2 の発注書が倉庫 GW およびバッチ AAA に対して請求されています。
-   原価価格が USD 12.00 で数量が 3 の発注書が倉庫 GW およびバッチ AAA に対して請求されています。
-   原価価格が USD 15.00 で数量が 2 の発注書が倉庫 GW およびバッチ BBB に対して請求されています。

倉庫 GW とバッチ AAA の移動平均原価価格は USD 11.20 で、倉庫 GW とバッチ BBB の移動平均原価価格は USD 15.00 です。




