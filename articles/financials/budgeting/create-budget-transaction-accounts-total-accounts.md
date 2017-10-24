---
title: "トランザクション勘定と合計勘定からの予算作成"
description: "この記事は、勘定合計に基づいて予算を作成するプロセスの概要を提供します。 予算管理が必要な場合に、勘定合計の予算管理を有効にする方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fd6dc5173fd37f0257c98c1a41f3e6ce40b5b680
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="7d5fe-104">トランザクション勘定と合計勘定からの予算作成</span><span class="sxs-lookup"><span data-stu-id="7d5fe-104">Create a budget from transaction accounts and total accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7d5fe-105">この記事は、勘定合計に基づいて予算を作成するプロセスの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="7d5fe-106">予算管理が必要な場合に、勘定合計の予算管理を有効にする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="7d5fe-107">予算計画および予算登録エントリの文書の両方が、**合計**タイプの主勘定を持つ主勘定での予算作成に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="7d5fe-108">実績は、トランザクション用の主勘定にのみ転記できます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="7d5fe-109">**一般会計から予算計画を生成**の定期プロセスについて、**ソース** タブで、**合計**の主勘定タイプを基準として指定できます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="7d5fe-110">この場合、各合計の主勘定がターゲット予算計画に含まれ、金額は選択範囲の主勘定の合計金額と一致します。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="7d5fe-111">**合計**タイプの主勘定の予算管理を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="7d5fe-112">この機能は、予算グループの使用でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="7d5fe-113">各合計の主勘定について、予算グループに対して管理される予算は、**予算管理コンフィギュレーション **ページで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="7d5fe-114">指定する基準には、合計の主勘定と勘定範囲を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="7d5fe-115">予算グループの作成プロセスの処理速度を上げるために、予算管理グループのデータ エンティティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="7d5fe-116">予算を財務諸表などのレポートで使用する場合、合計勘定の予算合計は、次の金額で構成されます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="7d5fe-117">勘定合計の期間内に各トランザクション勘定科目から作成される予算</span><span class="sxs-lookup"><span data-stu-id="7d5fe-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="7d5fe-118">勘定合計に直接入力された予算金額</span><span class="sxs-lookup"><span data-stu-id="7d5fe-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="7d5fe-119">これにより、勘定合計の期間内の最重要トランザクション勘定に個別の予算を作成することも、利用可能な予算額を勘定合計に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d5fe-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




