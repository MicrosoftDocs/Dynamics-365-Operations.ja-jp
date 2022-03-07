---
title: 計画最適化の拡張機能
description: このトピックでは、計画の最適化でサポートされている機能性のシナリオについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Developer
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aaa7d6c4411da04fa9191f96a102c07a2bf90440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983531"
---
# <a name="planning-optimization-extensibility"></a>計画最適化の拡張機能

[!include [banner](../../includes/banner.md)]

このトピックでは、マスター プランに関連し、計画の最適化でサポートされている拡張性のシナリオについて説明します。 これらの機能は、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.13 以降で使用できます。

## <a name="custom-processing-when-master-planning-is-completed"></a>マスター プランが完了したときのカスタム処理

計画の最適化における最も一般的な機能性のシナリオでは、計画が更新された後にカスタム処理を実行します。 たとえば、計画オーダー テーブル (`ReqPO`) に列を追加したり、生成された計画から統計情報を派生することができます。 これらのシナリオを可能にする主要な機能性ポイントは、`MpsMasterPlanningEvents` クラス内の `jobCompletedSuccessfully` メソッドです 。

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

ここでは、計画オーダーのカスタム `CstmOrderPriority` フィールドを設定する拡張機能の例を示し ます。

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

カスタム ロジックを追加する場合は、次の制約とベスト プラクティスを考慮してください。

- この `jobCompletedSuccessfully` メソッドは、トランザクション スコープ外で呼び出されます。 したがって、カスタム ロジックの実行を開始したときに、ユーザーには既にプランが表示されています。 計画オーダーの追加のフィールドをカスタマイズしている場合、これらのフィールドの値が最終的に一貫性を持つようになることをユーザーに通知することが重要です (つまり、計画ジョブが完了した直後にその値が期限切れになる可能性があります)。
- 別のマスター プラン ジョブを、`jobCompletedSuccessfully` メソッドが呼び出されたときに開始できます。 新しいジョブは、計画の全体または一部に影響を与える可能性があります。 新しいジョブでは、`jobCompletedSuccessfully` で処理された計画ジョブの一部として作成または更新された、同じ計画オーダーまたは要求トランザクションを更新または削除することができます。 更新の競合の例外は、このイベントが拡張されたときに処理する必要があります。
- このメソッドを拡張する場合は、単一のトランザクション スコープを使用しないでください。 単一のマスター プランの実行で、数百万の要求トランザクションと数十万の計画オーダーを生成することができます。 これらのすべてのトランザクションと計画オーダーが単一のトランザクションのスコープで処理されると、多くの SQL ロックが発生し、その他の計画プロセスがブロックされます。 さらに、トランザクションが長期間保持されている場合は、SQL データベースに「ゴースト レコード」が作成されます。 ゴースト レコードは、システム内のすべてのプロセスに悪影響を与えます。
