---
title: "配賦の処理"
description: "この記事では、配賦を Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションで処理するオプション、および予算の計画で使用する方法に関する情報を提供します。 配賦は、複数の勘定科目の組み合わせ全体で金額を配分するのに使用されます。 経費、または収益が正しい会計のオブジェクトに付けられることを保証します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb12e24fcb8e8c91f90b91e2fdb3039dd1735ca3
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="process-allocations"></a><span data-ttu-id="de671-105">配賦の処理</span><span class="sxs-lookup"><span data-stu-id="de671-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="de671-106">この記事では、配賦を Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションで処理するオプション、および予算の計画で使用する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="de671-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and how they can be used in budget planning.</span></span> <span data-ttu-id="de671-107">配賦は、複数の勘定科目の組み合わせ全体で金額を配分するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de671-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="de671-108">経費、または収益が正しい会計のオブジェクトに付けられることを保証します。</span><span class="sxs-lookup"><span data-stu-id="de671-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="de671-109">Microsoft Dynamics 365 for Finance and Operations では、このプロセスをサポートするために、次の機能を提供します:</span><span class="sxs-lookup"><span data-stu-id="de671-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="de671-110">勘定配布で分割アクションを使用する、またはドキュメントに財務分析コードの既定のテンプレートを適用することにより、トランザクション金額を手動で割り当てます。</span><span class="sxs-lookup"><span data-stu-id="de671-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="de671-111">詳細については、「[勘定配布](../accounts-payable/accounting-distributions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de671-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="de671-112">個別の主勘定で定義された配賦条件に基づいてトランザクション金額を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="de671-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="de671-113">配賦勘定項目は、勘定項目がソースの勘定科目に定義した条件を満たす場合に、割合と相手方の勘定科目に基づいて仕訳帳ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="de671-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="de671-114">元帳配賦ルールに基づいて元帳残高または固定金額を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="de671-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="de671-115">元帳配賦ルールは、配賦仕訳帳を使用して定期的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="de671-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="de671-116">予算計画での配賦</span><span class="sxs-lookup"><span data-stu-id="de671-116">Allocations in budget planning</span></span>

<span data-ttu-id="de671-117">元帳配賦ルールは、予算計画に使用できます。</span><span class="sxs-lookup"><span data-stu-id="de671-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="de671-118">予算計画で元帳配賦ルールを使用するとき、配賦ルールは元帳と同じ動作をしますが、データ ソースと相手方のデータは予算計画から取得されます。</span><span class="sxs-lookup"><span data-stu-id="de671-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="de671-119">手動で予算計画に使用する元帳配賦ルールを選択できます。</span><span class="sxs-lookup"><span data-stu-id="de671-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="de671-120">また、ワークフロー プロセスの一部として実行される配賦スケジュールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="de671-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="de671-121">会社間元帳配賦ルールは予算計画には使用できません。</span><span class="sxs-lookup"><span data-stu-id="de671-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






