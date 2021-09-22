---
title: 未終了の補充作業によってブロックされたピッキング作業
description: ピッキング作業は、依存する補充作業のためブロックされる可能性があります。 補充作業を完了し、ピッキング作業を処理します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476922"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>ピッキング作業は、未終了の補充作業のためブロックされません

## <a name="symptoms"></a>現象

サイクル需要補充を使用する場合、依存補充作業のためにピッキング作業をブロックすることができます。 ソース注文需要を満たすためにピッキング場所を補充する必要がある場合は、補充作業とピッキング作業の両方がシステムによって作成されます。 ただし、補充作業が完了して次のエラー メッセージが表示されるまでは、ピッキング作業がブロックされます。

> 作業 %1 は、未完了の補充作業が含まれるために、ブロックを解除できません。

## <a name="resolution"></a>解決策

補充作業が完了していない場合、ピッキング場所に十分な在庫がないので、この動作は意図的です。 補充作業を完了し、ピッキング作業を処理します。
