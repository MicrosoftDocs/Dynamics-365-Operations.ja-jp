---
title: 計画オーダーを再スケジューリングする場合、遅延値は更新されません
description: 計画オーダーを再スケジューリングする場合、遅延値は更新されません
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
ms.openlocfilehash: 566702913774cf002ab38e367f690a479d968657
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476899"
---
# <a name="the-delay-value-isnt-updated-when-you-reschedule-a-planned-order"></a>計画オーダーを再スケジューリングする場合、遅延値は更新されません

## <a name="symptoms"></a>現象

計画オーダーを再スケジューリングする場合、遅延値は更新されません。

## <a name="resolution"></a>解決策

計画オーダーの遅延を更新するには、計画オーダーの **再スケジュール** ダイアログ ボックスを開きます。 **展開** クイック タブで、**再スケジュール後に展開を実行する** オプションが *はい* に設定されていることを確認します。
