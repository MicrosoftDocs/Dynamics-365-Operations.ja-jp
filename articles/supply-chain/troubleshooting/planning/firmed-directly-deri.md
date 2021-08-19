---
title: 直接派生した会社注文は、レビュー中のワークフローによって処理されます
description: 直接派生した会社注文は、レビュー中のワークフローによって処理されます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721178"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>直接派生した会社注文は、レビュー中のワークフローによって処理されます

KB 番号: 4612450

## <a name="symptoms"></a>現象

直接派生した会社注文は、*レビュー中* のワークフローによって処理されます。

## <a name="resolution"></a>解像度

変更追跡が有効な場合、確定した派生オーダー (外注発注書) は、案件変更のトラッキングが有効になっている場合は、状態が *レビュー中* と表示されます。 したがって、派生した発注書 (外注発注書) は、ワークフローにのみ送信されます。 発注書が固定された計画発注書の場合、発注書のステータスが *ドラフト* の間、計画エンジンが新しい計画オーダーを作成しない場合は、自動的に承認されます。
