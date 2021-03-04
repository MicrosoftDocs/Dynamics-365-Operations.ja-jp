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
# <a name="planning-optimization-extensibility"></a><span data-ttu-id="c150d-103">計画最適化の拡張機能</span><span class="sxs-lookup"><span data-stu-id="c150d-103">Planning Optimization extensibility</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c150d-104">このトピックでは、マスター プランに関連し、計画の最適化でサポートされている拡張性のシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c150d-104">This topic describes the extensibility scenarios that are related to master planning and supported in Planning Optimization.</span></span> <span data-ttu-id="c150d-105">これらの機能は、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.13 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="c150d-105">These capabilities are available starting in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span>

## <a name="custom-processing-when-master-planning-is-completed"></a><span data-ttu-id="c150d-106">マスター プランが完了したときのカスタム処理</span><span class="sxs-lookup"><span data-stu-id="c150d-106">Custom processing when master planning is completed</span></span>

<span data-ttu-id="c150d-107">計画の最適化における最も一般的な機能性のシナリオでは、計画が更新された後にカスタム処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="c150d-107">In the most common extensibility scenario in Planning Optimization, custom processing is done after the plan has been updated.</span></span> <span data-ttu-id="c150d-108">たとえば、計画オーダー テーブル (`ReqPO`) に列を追加したり、生成された計画から統計情報を派生することができます。</span><span class="sxs-lookup"><span data-stu-id="c150d-108">For example, you might add a column to the planned orders table (`ReqPO`), or you might want to derive some statistical information from the generated plan.</span></span> <span data-ttu-id="c150d-109">これらのシナリオを可能にする主要な機能性ポイントは、`MpsMasterPlanningEvents` クラス内の `jobCompletedSuccessfully` メソッドです 。</span><span class="sxs-lookup"><span data-stu-id="c150d-109">The main extensibility point that enables these scenarios is the `jobCompletedSuccessfully` method in the `MpsMasterPlanningEvents` class.</span></span>

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

<span data-ttu-id="c150d-110">ここでは、計画オーダーのカスタム `CstmOrderPriority` フィールドを設定する拡張機能の例を示し ます。</span><span class="sxs-lookup"><span data-stu-id="c150d-110">Here is an example of an extension that sets a custom `CstmOrderPriority` field on the planned order.</span></span>

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

<span data-ttu-id="c150d-111">カスタム ロジックを追加する場合は、次の制約とベスト プラクティスを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="c150d-111">When you add custom logic, consider the following constraints and best practices:</span></span>

- <span data-ttu-id="c150d-112">この `jobCompletedSuccessfully` メソッドは、トランザクション スコープ外で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c150d-112">The `jobCompletedSuccessfully` method is called outside the transaction scope.</span></span> <span data-ttu-id="c150d-113">したがって、カスタム ロジックの実行を開始したときに、ユーザーには既にプランが表示されています。</span><span class="sxs-lookup"><span data-stu-id="c150d-113">Therefore, the plan is already visible to the user when the custom logic starts to run.</span></span> <span data-ttu-id="c150d-114">計画オーダーの追加のフィールドをカスタマイズしている場合、これらのフィールドの値が最終的に一貫性を持つようになることをユーザーに通知することが重要です (つまり、計画ジョブが完了した直後にその値が期限切れになる可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="c150d-114">If your customization sets additional fields on planned orders, it's important that you let users know that the values of those fields will eventually be consistent (in other words, they might be out of date immediately after a planning job is completed).</span></span>
- <span data-ttu-id="c150d-115">別のマスター プラン ジョブを、`jobCompletedSuccessfully` メソッドが呼び出されたときに開始できます。</span><span class="sxs-lookup"><span data-stu-id="c150d-115">Another master planning job can start when the `jobCompletedSuccessfully` method is called.</span></span> <span data-ttu-id="c150d-116">新しいジョブは、計画の全体または一部に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c150d-116">The new job might affect the full plan or part of the plan.</span></span> <span data-ttu-id="c150d-117">新しいジョブでは、`jobCompletedSuccessfully` で処理された計画ジョブの一部として作成または更新された、同じ計画オーダーまたは要求トランザクションを更新または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="c150d-117">The new job might update or delete the same planned orders or requirement transactions that were created or updated as part of the planning job that was handled in `jobCompletedSuccessfully`.</span></span> <span data-ttu-id="c150d-118">更新の競合の例外は、このイベントが拡張されたときに処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c150d-118">Update conflict exceptions must be handled when this event is extended.</span></span>
- <span data-ttu-id="c150d-119">このメソッドを拡張する場合は、単一のトランザクション スコープを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="c150d-119">Avoid using single transaction scope when you extend this method.</span></span> <span data-ttu-id="c150d-120">単一のマスター プランの実行で、数百万の要求トランザクションと数十万の計画オーダーを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="c150d-120">A single master planning run can produce millions of requirement transactions and hundreds of thousands of planned orders.</span></span> <span data-ttu-id="c150d-121">これらのすべてのトランザクションと計画オーダーが単一のトランザクションのスコープで処理されると、多くの SQL ロックが発生し、その他の計画プロセスがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="c150d-121">If all these transactions and planned orders are processed in the scope of a single transaction, many SQL locks will occur and block other planning processes.</span></span> <span data-ttu-id="c150d-122">さらに、トランザクションが長期間保持されている場合は、SQL データベースに「ゴースト レコード」が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c150d-122">Additionally, if the transaction is held for a long time, "ghost records" will be created in the SQL database.</span></span> <span data-ttu-id="c150d-123">ゴースト レコードは、システム内のすべてのプロセスに悪影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="c150d-123">Ghost records will negatively affect every process in the system.</span></span>
