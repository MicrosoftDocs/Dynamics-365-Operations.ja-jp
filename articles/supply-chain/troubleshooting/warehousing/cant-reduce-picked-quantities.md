---
title: ライセンス プレートとして管理されている場所に在庫を移動できません
description: 以前のバージョンでは、積荷のピッキング済数量を減少させることはできませんでした。 ただし、現在では、ライセンス プレートによって制御された場所にピッキング解除できるようになりました。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdb6ee2cff184c5dd53ce33133e4935d00caf3db
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476921"
---
# <a name="cant-move-inventory-to-a-location-that-is-license-plate-controlled"></a>ライセンス プレートとして管理されている場所に在庫を移動できません

## <a name="symptoms"></a>現象

積荷のピッキング済数量を減少させることはできません。

## <a name="resolution"></a>解決策

以前のバージョンでは、積荷のピッキング済数量を減少させることはできませんでした。 ただし、現在では、ライセンス プレートによって制御された場所にピッキング解除できるようになりました。 **ピッキング済数量の削減** ページでは、**場所** 値と **ライセンス プレート** 値の両方を積荷明細行に指定する必要があります。
