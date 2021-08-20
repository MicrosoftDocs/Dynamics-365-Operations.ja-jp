---
title: CW 数量の分割時に公称数量ではなく最小数量が使用される
description: CW 数量をバッチに分割すると、[ピック数量] フィールドで、品目に対して設定されている公称数量ではなく最小数量が使用されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723458"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>CW 数量の分割時に公称数量ではなく最小数量が使用される

KB 番号: 4612073

## <a name="symptoms"></a>現象

CW 数量をバッチに分割すると、**ピック数量** フィールドで、品目に対して設定されている公称数量ではなく最小数量が使用されます。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 システムは、各品目の最小数量設定をピッキングに使用します。
