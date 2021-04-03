---
title: 移動平均フォールバック コスト シーケンス
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Managementで移動平均を計算するためのフォールバック コスト シーケンスについて説明します。
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 1f5b1307f039bb9e921d50aed411b3dc603ada65
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263617"
---
# <a name="moving-average-fallback-cost-sequence"></a>移動平均フォールバック コスト シーケンス

在庫の原価を計算する 1 つの方法は、_移動平均_ を使用することです。 各在庫品目には、最大 3 つの原価価値を関連付けることができます。

- **最終払出** – 在庫がマイナスになる前に割り当てられた最終払出原価
- **有効な原価** – 原価計算バージョンで有効化された最新の原価
- **品目価格** – リリース済み製品に対して指定されている原価

これらの原価価値のうちどれを移動平均の計算に使用するかを決定するために、システムでは _フォールバック コスト シーケンス_ を使用して、値の優先順位を決定します。 優先原価価値が使用できない場合、システムは次に優先される値を使用します。

以前のバージョンのMicrosoft Dynamics 365 Supply Chain Management では、システムは固定のフォールバック コスト シーケンス (_最終払出 – 有効な原価 – 品目価格_) を使用していました。 バージョン 10.0.11 では、このシーケンスは依然として既定のシーケンスです。 ただし、使用可能な 3 つのフォールバック コスト シーケンスから選択できる機能を有効にすることもできます。 この機能は、マイナス在庫値を定期的に使用する組織で特に役立ちます。

フォールバック コスト シーケンスのセレクターを使用できるようにするには、ユーザー (または管理者) は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、_移動平均フォールバック コスト シーケンス_ という名前の機能を有効にする必要があります。

移動平均の計算に使用するフォールバック コスト シーケンスを選択するには、次の手順に従います。

1. **パラメーター** ページを開きます。
2. **在庫会計** タブの **移動平均** セクションで、**フォールバック コスト シーケンス** フィールドを次のいずれかの値に設定します:

    - **最終払出 – 有効な原価 – 品目価格** – このシーケンスは、既定のシーケンスです。 _移動平均フォールバック コスト シーケンス_ 機能が有効になっていない場合に使用されるシーケンスと同じです。
    - **有効な原価 – 最終払出**
    - **有効な原価 – 品目価格** – 在庫が定期的にマイナスになり、同時に、トランザクション量が高い業務プロセスを使用している場合、組織でパフォーマンスの問題が発生する可能性があります。 この設定は、これらのパフォーマンスの問題を軽減するのに役立ちます。

![在庫会計パラメーター](media/inventory-accounting-parameters.png "在庫会計パラメーター")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]