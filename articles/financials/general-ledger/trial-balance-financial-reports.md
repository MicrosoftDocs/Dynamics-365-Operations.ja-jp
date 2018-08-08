---
title: "試算表の財務諸表"
description: "この記事では、試算表の既定のレポートについて説明します。 さらに、これらのレポートに関連付けられる構成要素について、また業務要件を満たすようにレポートを変更する方法についても説明します。"
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c9e8c16724364df4dd62150056299e818470aa63
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="8f1d3-104">試算表の財務諸表</span><span class="sxs-lookup"><span data-stu-id="8f1d3-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f1d3-105">この記事では、試算表の既定のレポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="8f1d3-106">さらに、これらのレポートに関連付けられる構成要素について、また業務要件を満たすようにレポートを変更する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="8f1d3-107">既定の試算表のレポート</span><span class="sxs-lookup"><span data-stu-id="8f1d3-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="8f1d3-108">Microsoft Dynamics 365 for Finance and Operations の財務報告では、3 つの試算表のレポートが使用できます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="8f1d3-109">既定のレポート</span><span class="sxs-lookup"><span data-stu-id="8f1d3-109">Default report</span></span>                                 | <span data-ttu-id="8f1d3-110">目的</span><span class="sxs-lookup"><span data-stu-id="8f1d3-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1d3-111">詳細な試算表 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="8f1d3-112">すべての勘定の残高情報を提供します。これには借方と貸方残高、これらの正味金額、トランザクションの日付、伝票、仕訳帳の説明が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="8f1d3-113">試算表の集計 – 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="8f1d3-114">すべての勘定の残高情報を提供します。これには、開始残高および決算残高、借方と貸方残高、およびそれらの正味差額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="8f1d3-115">年次試算表の集計 – 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="8f1d3-116">すべての勘定の残高情報を提供します。これには、開始残高および決算残高、借方と貸方残高、およびそれらの今年度および昨年度の正味差額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="8f1d3-117">構成要素</span><span class="sxs-lookup"><span data-stu-id="8f1d3-117">Building blocks</span></span>
<span data-ttu-id="8f1d3-118">試算表の財務レポートは、次の構成要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="8f1d3-119">既定のレポート</span><span class="sxs-lookup"><span data-stu-id="8f1d3-119">Default report</span></span>                                 | <span data-ttu-id="8f1d3-120">行の定義</span><span class="sxs-lookup"><span data-stu-id="8f1d3-120">Row definition</span></span>          | <span data-ttu-id="8f1d3-121">列の定義</span><span class="sxs-lookup"><span data-stu-id="8f1d3-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="8f1d3-122">詳細な試算表 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="8f1d3-123">試算表 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-123">Trial Balance - Default</span></span> | <span data-ttu-id="8f1d3-124">詳細な試算表 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="8f1d3-125">試算表の集計 – 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="8f1d3-126">試算表 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-126">Trial Balance - Default</span></span> | <span data-ttu-id="8f1d3-127">試算表の集計 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="8f1d3-128">年次試算表の集計 – 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="8f1d3-129">試算表 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-129">Trial Balance - Default</span></span> | <span data-ttu-id="8f1d3-130">年次試算表の集計 - 既定</span><span class="sxs-lookup"><span data-stu-id="8f1d3-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="8f1d3-131">行の定義</span><span class="sxs-lookup"><span data-stu-id="8f1d3-131">Row definition</span></span>

<span data-ttu-id="8f1d3-132">試算表 - 既定という行定義には、すべての主勘定を取込む 1 つの行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="8f1d3-133">したがって、ユーザーは変更しないでレポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="8f1d3-134">レポートを表示すると、各勘定に関する詳細を表示する 1 行を表示できます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="8f1d3-135">行定義を変更することにより、さらに詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="8f1d3-136">試算表 - 既定の行定義を変更して、すべての勘定に対する行を含むようにするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="8f1d3-137">**編集** をクリックし、次に **分析コードからの行の挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="8f1d3-138">**分析コードからの行の挿入** コマンドを使用すると、自分の行定義に含める分析コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="8f1d3-139">この行定義で、**主勘定** を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="8f1d3-140">**主勘定** がすべてのアンパサンド (&) を含むことを確認し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="8f1d3-141">今回の行定義には、既定の法人の主勘定すべてが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="8f1d3-142">列の定義</span><span class="sxs-lookup"><span data-stu-id="8f1d3-142">Column definition</span></span>

<span data-ttu-id="8f1d3-143">各試算表レポートは別の列定義を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="8f1d3-144">これらの列の定義には、さまざまな詳細なレベルと財務データを提供する列のさまざまなタイプが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f1d3-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="8f1d3-145">**詳細な試算表 – 既定の列のタイプ:**</span><span class="sxs-lookup"><span data-stu-id="8f1d3-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="8f1d3-146">**DESC** – 行定義の説明</span><span class="sxs-lookup"><span data-stu-id="8f1d3-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8f1d3-147">**ACCT** – アカウント コード</span><span class="sxs-lookup"><span data-stu-id="8f1d3-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="8f1d3-148">**ATTR (3)** – 属性:</span><span class="sxs-lookup"><span data-stu-id="8f1d3-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="8f1d3-149">トランザクション日付</span><span class="sxs-lookup"><span data-stu-id="8f1d3-149">Transaction Date</span></span>
        -   <span data-ttu-id="8f1d3-150">伝票番号</span><span class="sxs-lookup"><span data-stu-id="8f1d3-150">Voucher</span></span>
        -   <span data-ttu-id="8f1d3-151">仕訳帳の説明</span><span class="sxs-lookup"><span data-stu-id="8f1d3-151">Journal Description</span></span>
    -   <span data-ttu-id="8f1d3-152">**FD** – 借方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="8f1d3-153">**FD** – 貸方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="8f1d3-154">**CALC** – 正味差額</span><span class="sxs-lookup"><span data-stu-id="8f1d3-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="8f1d3-155">**試算表の集計 – 既定の列のタイプ:**</span><span class="sxs-lookup"><span data-stu-id="8f1d3-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="8f1d3-156">**ACCT** – アカウント コード</span><span class="sxs-lookup"><span data-stu-id="8f1d3-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="8f1d3-157">**DESC** – 行定義の説明</span><span class="sxs-lookup"><span data-stu-id="8f1d3-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8f1d3-158">**ATTR** – 属性の 1 つ:</span><span class="sxs-lookup"><span data-stu-id="8f1d3-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="8f1d3-159">伝票番号</span><span class="sxs-lookup"><span data-stu-id="8f1d3-159">Voucher</span></span>
    -   <span data-ttu-id="8f1d3-160">**FD** – 期首残高の財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="8f1d3-161">**FD** – 借方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="8f1d3-162">**FD** – 貸方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="8f1d3-163">**CALC** – 正味差額</span><span class="sxs-lookup"><span data-stu-id="8f1d3-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="8f1d3-164">**CALC** – 決算残高</span><span class="sxs-lookup"><span data-stu-id="8f1d3-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="8f1d3-165">**年次試算表の集計 - 既定:**</span><span class="sxs-lookup"><span data-stu-id="8f1d3-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="8f1d3-166">**ACCT** – アカウント コード</span><span class="sxs-lookup"><span data-stu-id="8f1d3-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="8f1d3-167">**DESC** – 行定義の説明</span><span class="sxs-lookup"><span data-stu-id="8f1d3-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8f1d3-168">**ATTR** – 属性の 1 つ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="8f1d3-169">伝票番号</span><span class="sxs-lookup"><span data-stu-id="8f1d3-169">Voucher</span></span>
    -   <span data-ttu-id="8f1d3-170">**FD** – 今年度の期首残高の財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="8f1d3-171">**FD** - 今年度の借方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="8f1d3-172">**FD** – 今年度の貸方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="8f1d3-173">**CALC** – 正味差額</span><span class="sxs-lookup"><span data-stu-id="8f1d3-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="8f1d3-174">**CALC** – 決算残高</span><span class="sxs-lookup"><span data-stu-id="8f1d3-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="8f1d3-175">**FD** – 昨年度の借方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="8f1d3-176">**FD** – 昨年度の貸方のみを含む財務データ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="8f1d3-177">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="8f1d3-177">Additional resources</span></span>
--------

[<span data-ttu-id="8f1d3-178">財務報告</span><span class="sxs-lookup"><span data-stu-id="8f1d3-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="8f1d3-179">財務諸表の表示</span><span class="sxs-lookup"><span data-stu-id="8f1d3-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="8f1d3-180">Dynamics Financial Reporting ブログ</span><span class="sxs-lookup"><span data-stu-id="8f1d3-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




