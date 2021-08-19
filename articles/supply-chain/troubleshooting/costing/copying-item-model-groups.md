---
title: 品目モデル グループが別の法人にコピーされる場合のフィールド設定がありません
description: 品目モデル グループが別の法人にコピーされる場合のフィールド設定がありません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738846"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>品目モデル グループが別の法人にコピーされる場合のフィールド設定がありません

KB 番号: 4612800

## <a name="symptoms"></a>現象

*品目モデル グループ在庫ポリシー* エンティティを使用して品目モデル グループを別の法人 (会社) にコピーする場合、行先の法人の新しいモデル グループに一部のフィールド設定 (在庫モデルや説明) がありません。

## <a name="resolution"></a>解像度

品目モデル グループの完全なコピーを別の法人に作成するには、品目モデル グループの在庫ポリシー (`InventInventoryPolicyEntity`) と、品目モデル グループに関連付けられている原価フローの前提条件ポリシー (`InventCostFlowAssumptionPolicyEntity`) の両方を選択する必要があります。
