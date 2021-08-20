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
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741959"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>製造オーダーがバッチ ジョブを介してリセットされる場合、後で選択することはできません

KB 番号: 4614634

## <a name="symptoms"></a>現象

繰り返し実行されるバッチ ジョブを使用して製造オーダーの状態をリセットする場合、後で選択することはできません。

## <a name="resolution"></a>解像度

現在のデザインでは、*リセットの状態* プロセスのために後で選択することはサポートされていません。
