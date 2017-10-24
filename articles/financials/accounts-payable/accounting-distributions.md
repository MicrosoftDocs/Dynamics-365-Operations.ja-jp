---
title: "勘定配布"
description: "この記事は、勘定配布についての情報を提供し、それらを処理するために使用できるオプションについて説明します。 勘定配布は特定の勘定科目に元伝票の金額を割り当てるのに使用されます。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bbf23d9cab01e8cdbae776c9310fbd19b429443d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="accounting-distributions"></a><span data-ttu-id="40602-104">勘定配布</span><span class="sxs-lookup"><span data-stu-id="40602-104">Accounting distributions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="40602-105">この記事は、勘定配布についての情報を提供し、それらを処理するために使用できるオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="40602-105">This article provides information about accounting distributions and describes the options that are available for processing them.</span></span> <span data-ttu-id="40602-106">勘定配布は特定の勘定科目に元伝票の金額を割り当てるのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="40602-106">Accounting distributions are used to allocate monetary amounts for a source document to specific ledger accounts.</span></span> 

<span data-ttu-id="40602-107">勘定配布は、発注書、仕入先請求書、経費精算書および自由書式の請求書などの各元伝票によって、使用され、拡張されるプログラム全体にわたる機能です。</span><span class="sxs-lookup"><span data-stu-id="40602-107">Accounting distributions are a program-wide capability that is used and extended by each source document, such as a purchase order, vendor invoice, expense report, and free text invoice.</span></span> <span data-ttu-id="40602-108">既定では、既定の勘定配布は、各元伝票明細行と金額に対して生成され、条件付きで変更が有効になります。</span><span class="sxs-lookup"><span data-stu-id="40602-108">By default, a default accounting distribution is generated for each source document line and monetary amount, and is conditionally enabled for modification.</span></span> 

> [!Note] 
> <span data-ttu-id="40602-109">一部のドキュメントでは、注文と請求書の請求などのヘッダー ドキュメントの金額もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="40602-109">Some documents also support header document monetary amounts, such as charges for orders and invoices.</span></span> 

<span data-ttu-id="40602-110">一般的な勘定配布機能では、勘定配布を処理するため次のオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="40602-110">The generic accounting distribution capabilities provide the following options for processing accounting distributions:</span></span>

-   <span data-ttu-id="40602-111">[**金額の配分**] – 個別のドキュメント ヘッダーおよび税または請求金額などの明細行と子行の、勘定配布を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="40602-111">**Distribute amounts** – View and modify the accounting distributions for an individual document header or line and any child lines, such as taxes or charges.</span></span>
    -   <span data-ttu-id="40602-112">上位の金額配分 (親配分) では、主勘定と財務分析コードは、グリッド内のセグメント化エントリ コントロールで直接編集できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="40602-112">For the top monetary amount distributions (parent distributions), the main account and financial dimensions might be editable directly in the segmented entry control in the grid.</span></span> <span data-ttu-id="40602-113">拡張価格は、親配分の一般的な例です。</span><span class="sxs-lookup"><span data-stu-id="40602-113">The extended price is a typical example of such a parent distribution.</span></span>
    -   <span data-ttu-id="40602-114">配分金額はドキュメントの通貨条件に基づいています。</span><span class="sxs-lookup"><span data-stu-id="40602-114">The distributions amounts are based on the term currency for the document.</span></span> <span data-ttu-id="40602-115">通常、この通貨は、トランザクション通貨です。</span><span class="sxs-lookup"><span data-stu-id="40602-115">Typically, this currency is the transaction currency.</span></span> <span data-ttu-id="40602-116">会計通貨金額とレポート通貨金額は、補助元帳の一部として生成されます。</span><span class="sxs-lookup"><span data-stu-id="40602-116">Accounting and reporting currency amounts are generated as part of subledger accounting.</span></span>
    -   <span data-ttu-id="40602-117">配分には、会計日および会計イベントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="40602-117">The distributions display the accounting date and accounting event.</span></span> <span data-ttu-id="40602-118">通常、会計イベントはドキュメントが転記/仕訳入力されるまで [**なし**] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="40602-118">Typically, the accounting event is set to **None** until the document is posted/journalized.</span></span> <span data-ttu-id="40602-119">その時点で、会計イベントは**元**になります。</span><span class="sxs-lookup"><span data-stu-id="40602-119">At that point, the accounting event becomes **Original**.</span></span> <span data-ttu-id="40602-120">配分が転記された後は、配分を変更できません。</span><span class="sxs-lookup"><span data-stu-id="40602-120">After the distributions have been posted, you can't modify the distributions.</span></span>
    -   <span data-ttu-id="40602-121">[**分割**] ボタンにより、親配分が有効になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="40602-121">**Split** button might be enabled for parent distributions.</span></span> <span data-ttu-id="40602-122">[**分割**] は、新しい勘定配布を生成します。また、分割は、割合、金額、または数量に基づくことができます。</span><span class="sxs-lookup"><span data-stu-id="40602-122">**Split** generates new accounting distributions, and the split can be based on percentage, amount, or quantity.</span></span>
    -   <span data-ttu-id="40602-123">[**均等な配分**] ボタンを [**分割**] ボタンと共に使用することにより、すべての配分に均等に金額を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="40602-123">The **Distribute equally** button can be used in combination with **Split** to automatically allocate the amount equally across all distributions.</span></span>
    -   <span data-ttu-id="40602-124">[**リセット**] ボタンは、複数の配分が存在する場合は親配分を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="40602-124">**Reset** button might be enabled for parent distributions when more than one distributions exists.</span></span> <span data-ttu-id="40602-125">[**リセット**] は、すべての既存の配分を削除し、既定の配分を再生成することにより、配分への手動の変更を取り消します。</span><span class="sxs-lookup"><span data-stu-id="40602-125">**Reset** reverses any manual modification to the distribution by deleting all existing distributions and re-generating the default distributions.</span></span>
    -   <span data-ttu-id="40602-126">割引、請求金額、売上税などのすべての子配分は、親配分に常に従います。</span><span class="sxs-lookup"><span data-stu-id="40602-126">Any child distribution, such as discount, charge, and sales tax, always follows the parent distribution.</span></span> <span data-ttu-id="40602-127">[**参照**] &gt; [**親情報**] で、親/子関係を表示できます。</span><span class="sxs-lookup"><span data-stu-id="40602-127">You can view the parent/child relation at **Reference** &gt; **Parent information**.</span></span>
    -   <span data-ttu-id="40602-128">主勘定と財務分析コードは、子も編集できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="40602-128">The main account and financial dimension might be editable for children too.</span></span>
    -   <span data-ttu-id="40602-129">勘定配布の財務分析コードは、ドキュメントを拡張できる既定パターンに従います。</span><span class="sxs-lookup"><span data-stu-id="40602-129">The financial dimensions on the accounting distributions follow a defaulting pattern that a document can extended.</span></span> <span data-ttu-id="40602-130">詳細については、関連する記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40602-130">For more details, see the related articles.</span></span>
    -   <span data-ttu-id="40602-131">差異の配分は、仕入先請求書と発注書間のマッチングなどのマッチング シナリオで生成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="40602-131">Variance distributions might be generated in matching scenarios, such as matching between a vendor invoice and a purchase order.</span></span> <span data-ttu-id="40602-132">[**参照**] &gt; [**ドキュメント情報**] で、勘定配布間のマッチング関係を表示できます。</span><span class="sxs-lookup"><span data-stu-id="40602-132">You can view the matching relations between accounting distribution at **Reference** &gt; **Document information**.</span></span>
    -   <span data-ttu-id="40602-133">[**修正**] ボタンは、修正をサポートするドキュメントに対して表示され、有効になります。</span><span class="sxs-lookup"><span data-stu-id="40602-133">**Correct** button appears and is enabled for documents that support corrections.</span></span> <span data-ttu-id="40602-134">[**修正**] で新しい配分を作成します。</span><span class="sxs-lookup"><span data-stu-id="40602-134">**Correct** creates new distributions.</span></span> <span data-ttu-id="40602-135">最初に、元の配分を取り消す配分が作成されます。</span><span class="sxs-lookup"><span data-stu-id="40602-135">First, distributions are created that reverse the original distributions.</span></span> <span data-ttu-id="40602-136">これらの配分を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="40602-136">These distributions can't be modified.</span></span> <span data-ttu-id="40602-137">次に、新しく正しい勘定配布が作成されます。</span><span class="sxs-lookup"><span data-stu-id="40602-137">Next, new correct accounting distributions are created.</span></span> <span data-ttu-id="40602-138">これらの配分は、元の配分を変更できる場合、変更できます。</span><span class="sxs-lookup"><span data-stu-id="40602-138">These distributions can be modified if the original distributions could be modified.</span></span>
    -   <span data-ttu-id="40602-139">[**プロジェクトの詳細**] ボタンは、明細行がプロジェクトに関連付けられる場合に機能拡張として有効になります。</span><span class="sxs-lookup"><span data-stu-id="40602-139">The **Project details** button is enabled as an extension when a line is related to a project.</span></span> <span data-ttu-id="40602-140">プロジェクトの勘定配布により、資金調達ソースおよび明細行プロパティなどの詳細を変更できます。</span><span class="sxs-lookup"><span data-stu-id="40602-140">Project accounting distributions let you modify details such as the funding source and line property.</span></span>
    -   <span data-ttu-id="40602-141">[**参照**] で現在のドキュメントの口座の状態を表示できます。</span><span class="sxs-lookup"><span data-stu-id="40602-141">You can view the current document accounting status in **Reference**.</span></span> <span data-ttu-id="40602-142">状態は、ドキュメント全体に対してドキュメントが処理中または完了しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="40602-142">The status is for the entire document, and indicates whether the document is in process or completed.</span></span>
-   <span data-ttu-id="40602-143">[** 配分の表示**] – ドキュメントのすべての明細行と金額の勘定配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="40602-143">** View distributions** – View the accounting distributions for the all lines and monetary amounts on the document.</span></span> <span data-ttu-id="40602-144">このビューでは、勘定配布は変更できません。</span><span class="sxs-lookup"><span data-stu-id="40602-144">You can't modify the accounting distributions from this view.</span></span>


<span data-ttu-id="40602-145">詳細については、「[自由書式の請求書の勘定配布と補助元帳仕訳](accounting-distributions-subledger-journal-entries-vendor-invoices.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40602-145">For more information, see [Accounting distributions and subledger journal entries for free text invoices](accounting-distributions-subledger-journal-entries-vendor-invoices.md).</span></span>



