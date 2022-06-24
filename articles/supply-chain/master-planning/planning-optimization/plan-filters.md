---
title: 計画にフィルターを適用
description: この記事では、計画の最適化機能の使用する場合、計画でフィルターを使用する方法について説明します。
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c2df379be0876225bc7b0301d21f4e6660b04eb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875307"
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
