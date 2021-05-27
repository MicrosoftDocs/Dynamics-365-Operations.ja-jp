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
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026672"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="8a8ff-103">品目モデル グループが別の法人にコピーされる場合のフィールド設定がありません</span><span class="sxs-lookup"><span data-stu-id="8a8ff-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="8a8ff-104">KB 番号: 4612800</span><span class="sxs-lookup"><span data-stu-id="8a8ff-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="8a8ff-105">現象</span><span class="sxs-lookup"><span data-stu-id="8a8ff-105">Symptoms</span></span>

<span data-ttu-id="8a8ff-106">*品目モデル グループ在庫ポリシー* エンティティを使用して品目モデル グループを別の法人 (会社) にコピーする場合、行先の法人の新しいモデル グループに一部のフィールド設定 (在庫モデルや説明) がありません。</span><span class="sxs-lookup"><span data-stu-id="8a8ff-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="8a8ff-107">解像度</span><span class="sxs-lookup"><span data-stu-id="8a8ff-107">Resolution</span></span>

<span data-ttu-id="8a8ff-108">品目モデル グループの完全なコピーを別の法人に作成するには、品目モデル グループの在庫ポリシー (`InventInventoryPolicyEntity`) と、品目モデル グループに関連付けられている原価フローの前提条件ポリシー (`InventCostFlowAssumptionPolicyEntity`) の両方を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a8ff-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
