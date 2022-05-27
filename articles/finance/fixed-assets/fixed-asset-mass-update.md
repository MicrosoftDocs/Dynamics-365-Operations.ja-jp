---
title: 固定資産の一括更新
description: 帳簿を使用した場合、同じ減価償却簿の一部である資産グループの減価償却方法を変更できます。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b70fa13aea2b4acb10cbe5a917f5cf0f266bbf0
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719850"
---
# <a name="fixed-asset-mass-update"></a>固定資産の一括更新

[!include [banner](../includes/banner.md)]

帳簿を使用した場合、同じ減価償却簿の一部である資産グループの減価償却方法を変更できます。

たとえば、米国でその年の第 4 四半期に供用された資産が 40% を超える場合、四半期の期中の減価償却方法を使用する必要があります。 一括更新プロセスを使用して、新しい減価償却方法が必要な資産すべてを変更することができます。 

資産の減価償却方法を更新した場合、これらの資産に存在するすべての減価償却トランザクションは削除されます。 また、これらの資産の減価償却調整トランザクション、特別償却トランザクション、および特別減価償却トランザクションもすべて削除します。 

既に処理された資産の減価償却方法を更新するには、既存の処分トランザクションを最初に削除する必要があります。 また、処分プロセスにより生成されたすべてのトランザクションも削除する必要があります。 

資産の減価償却方法を更新した後、資産ごとに減価償却および特別減価償却の処理を行うことができます。 調整が必要な場合は、手動で減価償却調整を行うこともできます。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
