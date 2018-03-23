---
title: "経費精算書の転記"
description: "このトピックでは、一般会計への経費精算書を転記する方法について説明します。"
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: cc3aae061038202ec4f314654d9149c31e2575bb
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="post-an-expense-report"></a><span data-ttu-id="d964c-103">経費精算書の転記</span><span class="sxs-lookup"><span data-stu-id="d964c-103">Post an expense report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d964c-104">経費精算書は、承認されて一般仕訳帳に転送された後、一般会計に転記できます。</span><span class="sxs-lookup"><span data-stu-id="d964c-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="d964c-105">経費精算書を転記すると、付加価値税 (VAT) の還付に適用できる経費が特定されます。</span><span class="sxs-lookup"><span data-stu-id="d964c-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="d964c-106">VAT の支払の確認および還付タスクは、経費精算書の確認を担当する従業員に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d964c-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="d964c-107">経費精算書の経費が従業員の採用会社以外の会社に請求される場合は、経費の支払先会社と経費の支払元会社を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d964c-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="d964c-108">たとえば、経費精算書を送信した従業員は DAT 社に勤務しているが、DIR 社への経費を請求されたとします。</span><span class="sxs-lookup"><span data-stu-id="d964c-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="d964c-109">この場合、DAT は経費の支払先会社、DIR は経費の支払元会社です。</span><span class="sxs-lookup"><span data-stu-id="d964c-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="d964c-110">これらの仕訳帳明細行を確認した後は、経費明細行を一般会計に転記できます。</span><span class="sxs-lookup"><span data-stu-id="d964c-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="d964c-111">経費精算書を転記するには、[承認された経費精算書] ページで経費精算書を選択し、アクション ウィンドウで [転記] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d964c-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="d964c-112">同時にリストですべての経費精算書を転記することもできます。</span><span class="sxs-lookup"><span data-stu-id="d964c-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="d964c-113">すべての経費精算書を選択し、[転記] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d964c-113">Select all the expense reports, and then select **Post**.</span></span>

