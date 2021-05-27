---
title: 製造オーダーがバッチ ジョブを介してリセットされる場合、後で選択することはできません
description: 繰り返し実行されるバッチ ジョブを使用して製造オーダーの状態をリセットする場合、後で選択することはできません。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026671"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>製造オーダーがバッチ ジョブを介してリセットされる場合、後で選択することはできません

KB 番号: 4614634

## <a name="symptoms"></a>現象

繰り返し実行されるバッチ ジョブを使用して製造オーダーの状態をリセットする場合、後で選択することはできません。

## <a name="resolution"></a>解像度

現在のデザインでは、*リセットの状態* プロセスのために後で選択することはサポートされていません。
