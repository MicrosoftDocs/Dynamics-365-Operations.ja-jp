---
title: 遅延許容範囲 (マイナス在庫日数)
description: このトピックでは、遅延許容範囲の計算、および計画の最適化における計画オーダーの作成への影響に関する情報を提供します。
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306466"
---
# <a name="delay-tolerance-negative-days"></a>遅延許容範囲 (マイナス在庫日数)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

遅延許容範囲機能を使用すると、計画の最適化により、補償グループに設定されている **マイナス在庫日数** の値を考慮できます。 これは、マスター プランの際に適用される遅延許容範囲の期間を拡張するために使用されます。 このようにして、既存の供給が短期間の遅延後に需要を満たすことができる場合は、新しい供給注文の作成を回避できます。 この機能の目的は、特定の需要に対して新しい供給注文を作成する意味があるかどうかを決定することです。

## <a name="turn-on-the-feature-in-your-system"></a>システムで機能を有効化する

遅延許容範囲機能をシステムで使用するには、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*計画最適化のマイナス在庫日数* 機能を有効にします。

## <a name="delay-tolerance-in-planning-optimization"></a>計画の最適化の遅延許容範囲

遅延許容範囲は、既存の供給が既に計画されているときに新しい補充を注文するまでに待機するリード タイムを超えた日数を表します。 遅延許容範囲は、営業日ではなくカレンダー日を使用して定義します。

マスター プランの時点で、システムにより遅延許容範囲が計算されるときに **マイナス在庫日数** 設定が考慮されます。 **補充グループ** ページまたは **品目補充** ページで **マイナス在庫日数** の値を設定できます。

システムにより、*最も早い補充日* に遅延許容範囲の計算がリンクされ、これは今日の日付にリード タイムを加えた日付です。 遅延許容範囲は、次の式を使用して計算され、*max()* は 2 つの値の大きい方を検出します。

*max(最も早い補充日、需要期日)* – *需要期日* + *マイナス在庫日数*

この式により、製品リード タイム中に十分な供給があるときは、マスター プランによって新しい供給注文が作成されないようにします。

> [!NOTE]
> 計画の最適化における遅延許容範囲の計算では、組み込みのマスター プランからの動的マイナス在庫日数計算が常に使用されます。 **マスター プラン パラメーター** ページの **動的マイナス在庫日数を使用** の設定は、この動作には影響しません。

既存の供給によって計算された遅延許容範囲以下の需要遅延が意味される場合、計画の最適化によって、既存の供給が需要と共に関連付けられます。 場合によっては、過剰な供給よりも需要を遅延することをお勧めします。

次のサブセクションでは、遅延許容範囲が計画最適化での計画オーダーの作成にどのような影響を及ぼすかを示す例を提供します。

### <a name="example-1"></a>例 1

製品のコンフィギュレーションは次のとおりです:

- **リード タイム:** *10*
- **マイナス在庫日数:** *2*

次の供給と需要は製品に対して存在します。

- **今日の需要:** 数量が 10 の販売注文
- **12 日以内の供給:** 数量が 10 の発注書

既存の供給で、12 日以内の需要をカバーでき、その期間は遅延許容範囲と等しくなります。 したがって、マスター プランを実行すると、計画オーダーは作成されません。

### <a name="example-2"></a>例 2

製品のコンフィギュレーションは次のとおりです:

- **リード タイム:** *10*
- **マイナス在庫日数:** *0*

次の供給と需要は製品に対して存在します。

- **今日の需要:** 数量が 10 の販売注文
- **12 日以内の供給:** 数量が 10 の発注書

既存の供給で需要をカバーできるのは 12 日後のみです。 ただし、遅延許容範囲は 10 日です。 したがって、マスター プランを実行すると、数量が 10 の計画オーダーが作成されます。

### <a name="example-3"></a>例 3

製品のコンフィギュレーションは次のとおりです:

- **リード タイム:** *10*
- **マイナス在庫日数:** *2*

次の供給と需要は製品に対して存在します。

- **11 日以内の需要:** 数量が 10 の販売注文
- **14 日以内の供給:** 数量が 10 の発注書

既存の供給で需要をカバーできるのは 3 日後のみです。 ただし、遅延許容範囲は 2 日です。 (この場合、遅延許容範囲にはマイナス在庫日数 2 日のみが含まれます。 需要の日付は製品のリード タイムの後なので含まれません。) したがって、マスター プランを実行すると、数量が 10 の計画オーダーが作成されます。