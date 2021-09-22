---
title: 計画オーダーの更新に長い時間がかかる
description: 計画オーダーの要求数量または出荷日、あるいはその両方を更新する場合、更新を保存するために、通常はオーダーあたり少なくとも 30 秒かかります
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
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476889"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>計画オーダーの更新に長い時間がかかる

## <a name="symptoms"></a>現象

計画オーダーの要求数量または出荷日、あるいはその両方を更新する場合、更新を保存するために、通常はオーダーあたり少なくとも 30 秒かかります。

## <a name="resolution"></a>解決策

これは、組み込みのマスター プラン エンジンに関する既知の問題です。 編集中に BOM 構造を通じた基になる自動展開によって発生します。 この問題は、計画の最適化で修正されます。計画の最適化では、プランナーが関連するオーダーを更新および承認し、必要に応じて計画実行をトリガーして基になる BOM 構造の計画オーダーを更新できます。

組み込みのマスター プラン エンジンを使用してパフォーマンスを向上させる方法の 1 つは、次の手順を実行することです:

1. **マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。
1. プランを選択します。
1. **タイム フェンス (日)** クイックタブを展開します。
1. **展開** を *はい* に設定し、この設定の下にあるフィールドを 0 (ゼロ) に設定します。

> [!NOTE]
> これにより、このマスター プランに対して実行される展開の期間が 1 日に制限されます。
