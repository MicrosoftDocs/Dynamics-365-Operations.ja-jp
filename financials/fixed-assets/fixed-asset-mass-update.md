---
title: "固定資産の一括更新"
description: "帳簿を使用した場合、同じ減価償却簿の一部である資産グループの減価償却方法を変更できます。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a16bae8f13dd53b5bbe380f03f6ca399bd6dbd9a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-mass-update"></a>固定資産の一括更新

[!include[banner](../includes/banner.md)]


帳簿を使用した場合、同じ減価償却簿の一部である資産グループの減価償却方法を変更できます。

たとえば、米国でその年の第 4 四半期に供用された資産が 40% を超える場合、四半期の期中の減価償却方法を使用する必要があります。 一括更新プロセスを使用して、新しい減価償却方法が必要な資産すべてを変更することができます。 

資産の減価償却方法を更新した場合、これらの資産に存在するすべての減価償却トランザクションは削除されます。 また、これらの資産の減価償却調整トランザクション、特別償却トランザクション、および特別減価償却トランザクションもすべて削除します。 

既に処理された資産の減価償却方法を更新するには、既存の処分トランザクションを最初に削除する必要があります。 また、処分プロセスにより生成されたすべてのトランザクションも削除する必要があります。 

資産の減価償却方法を更新した後、資産ごとに減価償却および特別減価償却の処理を行うことができます。 調整が必要な場合は、手動で減価償却調整を行うこともできます。






