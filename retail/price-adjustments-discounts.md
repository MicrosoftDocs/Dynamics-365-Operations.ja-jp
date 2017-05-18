---
title: "価格調整および割引"
description: "この記事は、Microsoft Dynamics 365 for Operations での小売りとコマースの価格調整と割引に関する情報を提供します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: cb4f189b1f51788dea84702e4410cfaf8f570865
ms.contentlocale: ja-jp
ms.lasthandoff: 04/26/2017


---

# <a name="price-adjustments-and-discounts"></a>価格調整および割引

[!include[banner](includes/banner.md)]


この記事は、Microsoft Dynamics 365 for Operations での小売りとコマースの価格調整と割引に関する情報を提供します。

Dynamics 365 for Operations - Retail の小売りとコマースでは、コール センターの販売注文またはオンライン注文について、製品の価格調整を行ったり、明細行品目またはトランザクションに販売の時点 (POS) で適用される割引を設定できます。 価格調整と割引のどちらも、価格グループとリンクすることができます。 価格調整と割引の両方について、単一の開始日と終了日を指定するか、または期間コード、割引コード、その他の追加の属性を指定することができます。 価格調整と割引は、製品、バリアント、またはカテゴリーに適用できます。 複数の割引が製品に適用される場合、割引コンフィギュレーションの設定によって、顧客はいずれか 1 つの割引、または複合された割引を受け取ります。 Dynamics 365 for Operations の小売とコマースでは、割引または複合割引を、顧客に最適な価格となるように自動的に適用します。 価格調整または割引を設定する場合、価格グループが、割引が適用される正しいチャンネル、カタログ、所属、またはロイヤルティ プログラムに割り当てられていることを確認します。 また、割引 ID を自動的に生成するには、新しい割引または価格調整を定義する前に、**小売パラメーター** ページで番号順序を設定します。 **注記:** 価格調整または割引を削除できます。 ただし、統計情報は失われます。

### <a name="types-of-discounts"></a>割引タイプ

小売割引には次の 4 タイプがあります。

-   **単純割引** – 単一のパーセントまたは量。
-   **数量割引** – 複数の製品を購入するときに適用される割引。
-   **組み合わせ割引** – 顧客が特定の製品の組み合わせを購入した場合に提供される割引。
-   **しきい値割引** – トランザクションの合計が指定金額より大きいときに適用される割引。

価格調整と割引のどちらも、価格グループと関連付けることができます。 価格グループは、チャンネル、カタログ、加盟者およびロイヤルティ プログラムに関連付けることができます。




