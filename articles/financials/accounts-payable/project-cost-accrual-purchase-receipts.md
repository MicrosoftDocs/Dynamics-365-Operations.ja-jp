---
title: "購買入庫におけるプロジェクト費用の発生"
description: "このトピックでは、購買入庫での未収プロジェクト費用を、Microsoft Dynamics 365 for Finance and Operations で追跡する方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9a74b684e955376b9c3036954f4a6e6628c468f0
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="2e6e5-103">購買入庫におけるプロジェクト費用の発生</span><span class="sxs-lookup"><span data-stu-id="2e6e5-103">Project cost accrual on purchase receipts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e6e5-104">このトピックでは、購買入庫での未収プロジェクト費用を、Microsoft Dynamics 365 for Finance and Operations で追跡する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="2e6e5-105">プロジェクトの請求書は、商品やサービスが提供された後に到着することが多く、プロジェクトの主要業績評価指標 (KPIs) に重大な影響を及ぼす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="2e6e5-106">財務およびプロジェクト レポート両方におけるトランザクションを追跡できるのは重要なことです。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="2e6e5-107">次のシナリオはこのような例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="2e6e5-108">Contoso コンサルティングは新しいクラウド配置プロジェクトを開始しました。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="2e6e5-109">プロジェクトのためのコンピューターを購入するために発注書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="2e6e5-110">コンピューターは 1500 ドル、インストール サービスは 150 ドルかかります。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="2e6e5-111">仕入先からコンピュータが届き、インストールしましたが、請求書がまだ Contoso コンサルティングに届いていません。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="2e6e5-112">プロジェクト マネージャーは、請求書が送信される前にプロジェクト費用が 1650 ドルであることを期待しています。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="2e6e5-113">この原価は会社の月末財務諸表にも反映される必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="2e6e5-114">未払費用は、報告目的のために財務レベルとプロジェクトレベルの両方に記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="2e6e5-115">Finance and Operations では、製品入庫における財務更新は品目および調達カテゴリに対して追跡できます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="2e6e5-116">品目に対して、[買掛金勘定パラメーター] ページで、[製品入庫を元帳に転記] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="2e6e5-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="2e6e5-118">調達カテゴリに対して、[カテゴリのポリシー ルール] ページで、[購入] ポリシーを選択し、各調達カテゴリに対して [入庫時の未収購買経費] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="2e6e5-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="2e6e5-120">[転記設定] の [購買支出、未請求] と [購買見越計上] 勘定は、製品の入庫に関連付けられている伝票が転記されるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="2e6e5-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="2e6e5-122">この同じシナリオを使用して、製品入庫の転記が、総勘定元帳とプロジェクト情報へどのような影響を与えるかを見てみます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="2e6e5-123">**ステップ 1:** プロジェクトの新規発注書を作成して確認し、購入したコンピューターを 1500 ドル、インストール サービスを 150 ドルで記録します。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="2e6e5-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="2e6e5-125">発注書が確定されると、確定済費用のトランザクションが、プロジェクトに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="2e6e5-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="2e6e5-127">確定済費用のトランザクションには、[発注書] に対して設定された [トランザクションの発生元] フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="2e6e5-128">発注書を登録し、確認しても、プロジェクトのトランザクションは登録されません。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="2e6e5-129">**ステップ 2:** 商品とサービスが提供され、製品入庫が登録されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="2e6e5-130">製品入庫を転記すると、元帳に伝票が生成され、転記されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="2e6e5-131">伝票により、購買支出、未請求済発注の勘定、貸方額勘定は借方転記されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="2e6e5-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2e6e5-133">製品入庫が転記されると、プロジェクト カテゴリに対して、転記設定が使用されるのではなく、調達カテゴリおよび製品に対して転記設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="2e6e5-134">購買見越しの財務的影響を正確に反映させるためには、この設定を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="2e6e5-135">調達カテゴリを [調達カテゴリ ページ] のプロジェクト カテゴリにマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="2e6e5-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="2e6e5-137">**ステップ 3:** 仕入先請求書の下書きを作成します。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="2e6e5-138">Finance and Operations では、製品入庫を転記すると、プロジェクト情報には影響しません。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="2e6e5-139">回避手段として、購買入庫の転記の直後に仕入先請求書の下書きを生成できます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="2e6e5-140">[発注書] ページ &gt; [請求書のタブ] &gt; [生成] &gt; [請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="2e6e5-141">これにより、プロジェクト情報を更新する保留中の請求書ドキュメントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="2e6e5-142">仕入先請求書の草案を作成すると、保留中のプロジェクト トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="2e6e5-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="2e6e5-144">[確定済費用] ページでは、ステップ 1 で作成されたレコードが閉まり、保留中の仕入先請求書から取得される費用の約定を反映する新しいレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="2e6e5-145">確定済費用の [トランザクションの発生元] フィールドは [仕入先請求書] に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="2e6e5-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="2e6e5-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="2e6e5-147">仕入先請求書は、実際の仕入先請求書が到着するまで保留中のステータスとして保持されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e5-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>




