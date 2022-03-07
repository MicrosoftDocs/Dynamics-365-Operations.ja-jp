---
title: プランへのフィルターの適用
description: このトピックでは、計画の最適化機能の使用する場合、計画でフィルターを使用する方法について説明します。
author: ChristianRytt
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3612dd45a3f4b8c3597c81962a66c21ed14fb206
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729030"
---
# <a name="apply-filters-to-a-plan"></a>プランへのフィルターの適用

[!include [banner](../../includes/banner.md)]

計画の最適化機能を使用する場合、計画にフィルターを適用できます。 **計画フィルター** は、常にマスター プランの実行中に適用されます。 **計画フィルター** は、計画を特定の品目のグループに制限し、結果のマスター プランの一部としてその他の品目が含まれないようにするのに役立ちます。

**計画フィルター** が適用され、マスター プランの実行中にランタイム フィルターも適用される場合、計画の実行には 2 つのフィルターの共通部分のみが含まれます。

計画の最適化が使用されている場合、**計画フィルター** は **マスター プラン** からアクセスできます。

## <a name="example-scenario"></a>シナリオ例

計画フィルターには品目 A、B、および C が含まれるよう設定されています。その後マスター プランの実行は同じ計画に対して実行されますが、異なるランタイム フィルターが適用されます。

- **品目 D を含むランタイム フィルター:** 計画フィルターおよびランタイム フィルター間に共通部分がないため、品目は計画されていません。
- **品目 A および D を含むランタイム フィルター:** 品目 D は計画フィルターの一部ではないため、プランの実行では品目 A のみが含まれます。
- **品目 B を含むランタイム フィルター:** プランの実行には品目 B のみが含まれ、品目 A の以前の計画出力が保持されます。
- **すべての品目を含むランタイム フィルター (空白フィルター):** プランの実行には項目 A、B、および C が含まれており、品目 A および B の計画出力は上書きされます。

> [!NOTE]
> **マスター プラン パラメーター** ページで **現在の動的マスター プラン** として選択した計画に計画フィルターを設定した場合、動的マスター プランの機能はフィルター処理された品目に限定されます。 たとえば、計画フィルターの一部でない品目に対して正味必要量が更新されると、結果は生成されません。

## <a name="related-resources"></a>関連するリソース

[計画の最適化の概要](planning-optimization-overview.md)

[計画の最適化を開始する](get-started.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[計画ジョブのキャンセル](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
