---
title: "経費のワークフローの設定"
description: "旅費経費のドキュメントを確認および承認するために使用されるワークフロー プロセスを設定できます。"
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: fb729a56919eb50cdff8318138986152bb65a083
ms.contentlocale: ja-jp
ms.lasthandoff: 01/19/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="7e3c5-103">経費のワークフローの設定</span><span class="sxs-lookup"><span data-stu-id="7e3c5-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="7e3c5-104"> 旅費経費のドキュメントを確認および承認するために使用されるワークフロー プロセスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="7e3c5-105">ワークフローを定義できるドキュメントには、経費レポート、出張費要求、および現金前貸し要求が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="7e3c5-106">1 つのワークフローは 1 つの業務プロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-106">A workflow represents a business process.</span></span> <span data-ttu-id="7e3c5-107">ここでは、ドキュメントの処理および承認に携わるべきユーザーを示すことによって、システムにおけるドキュメントの流れを定義します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="7e3c5-108">組織でワークフロー システムを使用することにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="7e3c5-109">**一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントの承認プロセスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="7e3c5-110">ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="7e3c5-111">プロセスの可視性 - 特定のワークフロー インスタンスのステータス、履歴およびパフォーマンス測定方法を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="7e3c5-112">これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="7e3c5-113">集中化された作業一覧 - ユーザーは、集中化された作業一覧を表示して、自分に割り当てられているワークフローのタスクおよび承認を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="7e3c5-114">**ワークフローのタイプを作成することができる**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="7e3c5-115">次の表に、**経費**で作成できるワークフローのタイプの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="7e3c5-116">**タイプ**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-116">**Type**</span></span>                           | <span data-ttu-id="7e3c5-117">**このタイプは次の目的で使用します。**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="7e3c5-118">**経費精算書**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-118">**Expense report**</span></span>                 | <span data-ttu-id="7e3c5-119">経費レポートの承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="7e3c5-120">**経費精算書の自動転記**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="7e3c5-121">経費レポートの自動転記のワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="7e3c5-122">**経費明細行品目**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-122">**Expense line item**</span></span>              | <span data-ttu-id="7e3c5-123">経費レポートの行項目の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="7e3c5-124">**経費明細行品目の自動転記**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="7e3c5-125">経費レポートの行項目の自動転記のワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="7e3c5-126">**出張費要求**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-126">**Travel requisition**</span></span>             | <span data-ttu-id="7e3c5-127">旅費要求の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="7e3c5-128">**現金前貸し要求**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-128">**Cash advance request**</span></span>           | <span data-ttu-id="7e3c5-129">現金前貸し要求の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="7e3c5-130">**VAT 過誤納税の還付**</span><span class="sxs-lookup"><span data-stu-id="7e3c5-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="7e3c5-131">付加価値税 (VAT) の還付の承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e3c5-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

