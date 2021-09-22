---
title: 製造オーダーがある在庫に対して計画オーダーが生成される
description: 在庫および製造オーダーの品目が既に存在している場合でも、計画オーダーが生成されます
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476925"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>製造オーダーがある在庫に対して計画オーダーが生成される

## <a name="symptoms"></a>現象

在庫および製造オーダーの品目が既に存在している場合でも、計画オーダーが生成されます。

## <a name="resolution"></a>解決策

この問題を解決するには、**補充グループ** ページで該当するグループの **プラス在庫日数** の値を大きくします。 この変更により、需要に手持在庫を使用できるかどうかがシステムによって判断されます。 この場合、在庫のある品目に対して新しい計画オーダーは生成されません。
