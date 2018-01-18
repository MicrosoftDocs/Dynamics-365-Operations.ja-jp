---
title: "価格調整および割引"
description: "この記事では、Microsoft Dynamics 365 for Retail での価格調整と割引に関する情報を提供します。"
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9220cc12abf7134d425e088939d20ea03239a75a
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="price-adjustments-and-discounts"></a>価格調整および割引

[!include[banner](includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Retail での価格調整と割引に関する情報を提供します。

Dynamics 365 for Retail では、コール センターの販売注文またはオンライン注文について、製品の価格調整を行ったり、および明細行品目またはトランザクションに POS (販売時点管理) で適用される割引を設定できます。 価格調整と割引のどちらも、価格グループとリンクすることができます。 価格調整と割引の両方について、単一の開始日と終了日を指定するか、または期間コード、割引コード、その他の追加の属性を指定することができます。 価格調整と割引は、製品、バリアント、またはカテゴリーに適用できます。 複数の割引が製品に適用される場合、割引コンフィギュレーションの設定によって、顧客はいずれか 1 つの割引、または複合された割引を受け取ります。 Dynamics 365 for Retail では、割引または複合割引を、顧客に最適な価格となるように自動的に適用します。 価格調整または割引を設定する場合、価格グループが、割引が適用される正しいチャンネル、カタログ、所属、またはロイヤルティ プログラムに割り当てられていることを確認します。 また、割引 ID を自動的に生成するには、新しい割引または価格調整を定義する前に、**小売パラメーター** ページで番号順序を設定します。 **注記:** 価格調整または割引を削除できます。 ただし、統計情報は失われます。

### <a name="types-of-discounts"></a>割引タイプ

小売割引には次の 4 タイプがあります。

-   **単純割引** – 単一のパーセントまたは量。
-   **数量割引** – 複数の製品を購入するときに適用される割引。
-   **組み合わせ割引** – 顧客が特定の製品の組み合わせを購入した場合に提供される割引。
-   **しきい値割引** – トランザクションの合計が指定金額より大きいときに適用される割引。

価格調整と割引のどちらも、価格グループと関連付けることができます。 価格グループは、チャンネル、カタログ、加盟者およびロイヤルティ プログラムに関連付けることができます。




