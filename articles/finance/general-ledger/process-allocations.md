---
title: 配賦の処理
description: この記事では、配賦、Microsoft Dynamics 365 Finance で配賦を処理するためのオプション、および予算計画でそれらを使用する方法についての情報を提供します。 配賦は、複数の勘定科目の組み合わせ全体で金額を配分するのに使用されます。 経費、または収益が正しい会計のオブジェクトに付けられることを保証します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 4676ea9646fa1a182103ecab93e78a69001f0b8d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/21/2020
ms.locfileid: "3612665"
---
# <a name="process-allocations"></a><span data-ttu-id="4f45e-105">配賦の処理</span><span class="sxs-lookup"><span data-stu-id="4f45e-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f45e-106">この記事では、配賦、配賦を処理するためのオプション、および予算計画でそれらを使用する方法についての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f45e-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="4f45e-107">配賦は、複数の勘定科目の組み合わせ全体で金額を配分するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="4f45e-108">経費、または収益が正しい会計のオブジェクトに付けられることを保証します。</span><span class="sxs-lookup"><span data-stu-id="4f45e-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="4f45e-109">このプロセスをサポートする機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4f45e-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="4f45e-110">勘定配布で分割アクションを使用する、またはドキュメントに財務分析コードの既定のテンプレートを適用することにより、トランザクション金額を手動で割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="4f45e-111">詳細については、[勘定配布](../accounts-payable/accounting-distributions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f45e-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="4f45e-112">個別の主勘定で定義された配賦条件に基づいてトランザクション金額を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="4f45e-113">配賦勘定項目は、勘定項目がソースの勘定科目に定義した条件を満たす場合に、割合と相手方の勘定科目に基づいて仕訳帳ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="4f45e-114">詳細については、[主勘定配賦条件](../general-ledger/main-account-allocation-terms.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f45e-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="4f45e-115">元帳配賦ルールに基づいて元帳残高または固定金額を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="4f45e-116">元帳配賦ルールは、配賦仕訳帳を使用して定期的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="4f45e-117">詳細については、[配賦ルール](../general-ledger/ledger-allocation-rules.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f45e-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="4f45e-118">予算計画での配賦</span><span class="sxs-lookup"><span data-stu-id="4f45e-118">Allocations in budget planning</span></span>

<span data-ttu-id="4f45e-119">元帳配賦ルールは、予算計画に使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="4f45e-120">予算計画で元帳配賦ルールを使用するとき、配賦ルールは元帳と同じ動作をしますが、データ ソースと相手方のデータは予算計画から取得されます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="4f45e-121">手動で予算計画に使用する元帳配賦ルールを選択できます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="4f45e-122">また、ワークフロー プロセスの一部として実行される配賦スケジュールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f45e-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="4f45e-123">会社間元帳配賦ルールは予算計画には使用できません。</span><span class="sxs-lookup"><span data-stu-id="4f45e-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

