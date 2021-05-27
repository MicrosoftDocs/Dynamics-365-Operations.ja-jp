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
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026686"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>CW 数量の分割時に公称数量ではなく最小数量が使用される

KB 番号: 4612073

## <a name="symptoms"></a>現象

CW 数量をバッチに分割すると、**ピック数量** フィールドで、品目に対して設定されている公称数量ではなく最小数量が使用されます。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 システムは、各品目の最小数量設定をピッキングに使用します。
