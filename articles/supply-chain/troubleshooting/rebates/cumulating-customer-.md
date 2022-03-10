---
title: 品目リベート グループが使用された場合の顧客リベートの集計が失敗する
description: 品目リベート グループと組み合わせて顧客リベート契約を使用すると、リベートが計算されますが、集計は失敗します。
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760373"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>品目リベート グループが使用された場合の顧客リベートの集計が失敗する

KB 番号: 4611372

## <a name="symptoms"></a>現象

品目リベート グループと組み合わせて (*金額* タイプの) 顧客リベート契約を使用すると、リベートが計算されますが、集計は失敗します。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 品目グループでは、同じしきい値条件を持つ品目のみをグループ化します。 リベートの条件 (しきい値) は、品目グループ内の品目の合計金額ではなく、各品目の金額に対して設定されます。
