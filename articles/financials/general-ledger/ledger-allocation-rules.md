---
title: "元帳配賦ルール"
description: "この記事は、元帳配賦ルールに関する情報を提供します。 これらの配賦ルールのさまざまなコンポーネントと使用できる配賦方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63562cde3f2813fdcfc9df7ccbfc623aa2fbe9b1
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="905fb-104">元帳配賦ルール</span><span class="sxs-lookup"><span data-stu-id="905fb-104">Ledger allocation rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="905fb-105">この記事は、元帳配賦ルールに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="905fb-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="905fb-106">これらの配賦ルールのさまざまなコンポーネントと使用できる配賦方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="905fb-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="905fb-107">元帳配賦ルールを使用すると、自動的に配賦仕訳帳と勘定項目の計算と生成を行い、元帳残高や固定金額を配賦できます。</span><span class="sxs-lookup"><span data-stu-id="905fb-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="905fb-108">配賦方法には、変動的または固定があります。</span><span class="sxs-lookup"><span data-stu-id="905fb-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="905fb-109">次の配賦方法が、元帳配賦ルールに使用できます。</span><span class="sxs-lookup"><span data-stu-id="905fb-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="905fb-110">**基準** – これは変動方式で、配賦方法がフィルター条件に基づいて実際の元帳残高に依存する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="905fb-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="905fb-111">たとえば、広告費を、全部門の合計売上に対する各部門の売上の割合に基づいて配賦することができます。</span><span class="sxs-lookup"><span data-stu-id="905fb-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="905fb-112">**固定割合**と**加重固定値** – これらの方式では、配賦率や配賦比重のルールを直接定義できます。</span><span class="sxs-lookup"><span data-stu-id="905fb-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="905fb-113">たとえば、部門 A が広告費の 70 パーセントを受け取り、部門 B が 30 パーセントを受け取るように広告費を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="905fb-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="905fb-114">**均等** – この方式は、個々に定義した配賦先に均等に金額を配分します。</span><span class="sxs-lookup"><span data-stu-id="905fb-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="905fb-115">たとえば、配賦先として部門 A と部門 B が定義されている場合、部門 A と部門 B の双方が 50 パーセントずつの広告費を受け取るように割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="905fb-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="905fb-116">配賦ルールの配賦方法が [基準] である場合は、元帳配賦基準ルールも別途定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="905fb-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="905fb-117">「配賦要求の処理」プロセスでは、ユーザーが元帳配賦ルールを処理し、配賦仕訳帳入力の結果をプレビューしてから、計算された配賦を転記または削除できます。</span><span class="sxs-lookup"><span data-stu-id="905fb-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="905fb-118">元帳配賦ルールのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="905fb-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="905fb-119">各配賦ルールには、一般、入力元、出力先、および相殺の 4 つのコンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="905fb-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="905fb-120">配賦方法として [基準] を使用する場合、追加のコンポーネントである元帳配賦基準ルールが必要になります。</span><span class="sxs-lookup"><span data-stu-id="905fb-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="905fb-121">各コンポーネントは、配賦の処理に要求される重要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="905fb-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="905fb-122">**一般** – このコンポーネントでは、ユーザーが配賦方法、会社間ルール設定、ルールが有効かどうかなどのオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="905fb-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="905fb-123">**ソース** – このコンポーネントでは、ユーザーが配賦の入力元データを指定します。</span><span class="sxs-lookup"><span data-stu-id="905fb-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="905fb-124">配賦は、元帳残高 (**データ ソース** = **元帳**) または固定金額 (**データ ソース** = **固定値**) に基づきます。</span><span class="sxs-lookup"><span data-stu-id="905fb-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="905fb-125">**データ ソース**が**元帳**に設定されている場合、ソースのフィルタ条件は、元帳配賦ルールに対して定義する必要があります (たとえば、広告費)。</span><span class="sxs-lookup"><span data-stu-id="905fb-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="905fb-126">**出力先** – このコンポーネントでは、配賦計算の結果を配賦先明細行に配分し計上する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="905fb-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="905fb-127">たとえば、各部門には、配賦先明細行が 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="905fb-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="905fb-128">**相殺** – このコンポーネントでは、主勘定および分析コードが配賦先入力の収支を合わせるための相殺仕訳に決定される方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="905fb-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="905fb-129">ユーザー定義のオプションは通常、ソースに基づく勘定および分析コードの代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="905fb-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="905fb-130">**データ ソース**に**固定値**が設定されている場合、**ソース**は選択肢として使用できません。</span><span class="sxs-lookup"><span data-stu-id="905fb-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="905fb-131">**元帳配賦基準ルール** – これらのルールは、独自のソース基準を使用して、元帳残高を配賦に使用するかを決定します (たとえば、部門ごとの収益)。</span><span class="sxs-lookup"><span data-stu-id="905fb-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="905fb-132">各配賦基準ルールは、複数の配賦ルールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="905fb-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





