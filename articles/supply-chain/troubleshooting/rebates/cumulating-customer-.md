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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026667"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>品目リベート グループが使用された場合の顧客リベートの集計が失敗する

KB 番号: 4611372

## <a name="symptoms"></a>現象

品目リベート グループと組み合わせて (*金額* タイプの) 顧客リベート契約を使用すると、リベートが計算されますが、集計は失敗します。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 品目グループでは、同じしきい値条件を持つ品目のみをグループ化します。 リベートの条件 (しきい値) は、品目グループ内の品目の合計金額ではなく、各品目の金額に対して設定されます。
