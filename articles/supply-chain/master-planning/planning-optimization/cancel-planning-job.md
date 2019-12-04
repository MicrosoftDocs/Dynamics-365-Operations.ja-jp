---
title: 計画ジョブのキャンセル
description: このトピックでは、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774000"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a>計画ジョブのキャンセル

Microsoft Dynamics 365 Supply Chain Management では、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。

有効な計画ジョブをキャンセルするには、次の手順を実行します。

> [!NOTE]
> 有効なジョブのみキャンセルすることができます。

1. **マスタープラン \> 設定 \> 計画**に移動します。
2. 計画実行に適切な計画を選択します。
3. **履歴**を選択します。
4. キャンセルする計画ジョブの選択
5. **キャンセル**を選択します。

ジョブ状態は、計画の最適化サービスがジョブのキャンセルを確認するまで**キャンセル中**になります。 その後、状態は**キャンセル済**に変更されます。

> [!NOTE]
> 状態の変更を確認するには、**更新**ボタンを選択してページを更新する必要があります。

## <a name="related-resources"></a>関連するリソース

[計画の最適化の概要](planning-optimization-overview.md)

[計画の最適化を開始する](get-started.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[プランへのフィルターの適用](plan-filters.md)
