---
title: "転記の定義"
description: "この記事では、転記の定義に関する情報と、それらを定義およびリンクする方法について説明します。 サポートされている転記タイプと文書については、転記プロファイルの代わりに転記の定義を使用して、勘定項目の主勘定および財務分析コードを分類できます。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa80976e539e88af8b157257d043d410ede49e8d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="posting-definitions"></a><span data-ttu-id="6309c-104">転記の定義</span><span class="sxs-lookup"><span data-stu-id="6309c-104">Posting definitions</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6309c-105">この記事では、転記の定義に関する情報と、それらを定義およびリンクする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6309c-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="6309c-106">サポートされている転記タイプと文書については、転記プロファイルの代わりに転記の定義を使用して、勘定項目の主勘定および財務分析コードを分類できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="6309c-107">サポートされている転記タイプと文書については、転記プロファイルの代わりに転記の定義を使用して、勘定項目の主勘定および財務分析コードを分類できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="6309c-108">サポートされる文書および転記タイプは、**トランザクションの転記の定義**ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="6309c-109">転記の定義の使用を開始するには、**総勘定元帳パラメーター** ページで**転記の定義の使用**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6309c-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="6309c-110">転記の定義を使用する場合でも、元のエントリの転記プロファイルと、サポートされない転記タイプとドキュメントを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6309c-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="6309c-111">転記の定義は、発注書の債務会計および購買要求の債務会計をサポートするために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6309c-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="6309c-112">転記定義の定義</span><span class="sxs-lookup"><span data-stu-id="6309c-112">Defining posting definitions</span></span>
<span data-ttu-id="6309c-113">**転記の定義**ページを使用すると、照合基準を指定し、一致が発生したときに生成するエントリを定義できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="6309c-114">照合基準は、勘定配布として元のエントリに対して評価されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="6309c-115">**転記の定義**ページで、優先順位番号をエントリ行に割り当てて、行の評価順序を制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="6309c-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="6309c-116">最も優先順位の低い番号を持つ行が最初に評価されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="6309c-117">たとえば、優先順位が 1 であるすべての明細行が評価され、次に優先順位が 2 の行が評価されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="6309c-118">一致が見つかった場合、他の基準は無視されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="6309c-119">また、発生元トランザクションに一致するグループの基準のみで生成されたエントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="6309c-120">**転記の定義のテスト** ウィザードを使用すると、転記の定義を検証できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="6309c-121">転記の定義に対するサンプルの元のエントリを定義すると、生成されたエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="6309c-122">転記の定義のバージョンは、有効日と併用することができます。</span><span class="sxs-lookup"><span data-stu-id="6309c-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="6309c-123">たとえば、転記の定義の将来のバージョンを作成して、新しい会計年度の別の勘定科目に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="6309c-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="6309c-124">**トランザクションの転記の定義**ページを使用すると、転記の定義をトランザクション タイプに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6309c-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="6309c-125">転記の定義のリンク</span><span class="sxs-lookup"><span data-stu-id="6309c-125">Linking posting definitions</span></span>
<span data-ttu-id="6309c-126">転記の定義を作成すると、1 つの転記の定義から別の転記の定義にリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="6309c-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="6309c-127">リンクした定義の基準が現在の転記の定義の基準に追加されたと見なされます。</span><span class="sxs-lookup"><span data-stu-id="6309c-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="6309c-128">別の定義に対して基準の行を既に入力した場合には、これにより、**転記の定義**ページの**エントリ** クイック タブに基準を再入力する必要がなくなるため、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="6309c-129">図やテーブルに、使用する可能性があるリンクを含めます。</span><span class="sxs-lookup"><span data-stu-id="6309c-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="6309c-130">現在の転記の定義との競合を回避するために、リンク先の転記の定義の行がすべて一意であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6309c-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="6309c-131">転記の定義でリンクを作成するときに、次の制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6309c-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="6309c-132">転記の定義は、他の転記にリンクするか、別の転記の定義からにリンクされるかのいずれかにすることができますが、両方のリンクを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="6309c-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="6309c-133">ただし、転記の定義は、複数の転記の定義にリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="6309c-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="6309c-134">同じモジュールにある転記の定義の間でのみリンクを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6309c-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="6309c-135">転記の定義をトランザクション タイプに割り当てることができますが、トランザクション タイプは転記の定義と同じモジュールになければなりません。</span><span class="sxs-lookup"><span data-stu-id="6309c-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="6309c-136">**トランザクションの転記の定義**ページを使用して、トランザクション タイプがどのモジュールにあるのかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6309c-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="6309c-137">詳細については、「[転記の定義例](example-posting-definitions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6309c-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



