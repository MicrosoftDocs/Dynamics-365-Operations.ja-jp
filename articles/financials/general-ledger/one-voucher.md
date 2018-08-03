---
title: "1 つの伝票"
description: "財務仕訳帳の 1 つの伝票 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクションを入力できます。"
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.translationtype: HT
ms.sourcegitcommit: fa342ba6746490f1738d4c944cff9687736df3ff
ms.openlocfilehash: a4be73a38d66ff20bf82c5838a59d2418f82c7ad
ms.contentlocale: ja-jp
ms.lasthandoff: 08/03/2018

---

# <a name="one-voucher"></a><span data-ttu-id="4a13b-103">1 つの伝票</span><span class="sxs-lookup"><span data-stu-id="4a13b-103">One voucher</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
>  <span data-ttu-id="4a13b-104">この機能は、2018 年春のリリースで提供される、Dynamics 365 for Finance and Operations バージョン 8.0 で利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-104">This functionality will be available in Dynamics 365 for Finance and Operations version 8.0, which will be available in the Spring '18 release.</span></span>   

<a name="what-is-one-voucher"></a><span data-ttu-id="4a13b-105">「1 つの伝票」とは</span><span class="sxs-lookup"><span data-stu-id="4a13b-105">What is "One voucher"?</span></span>
======================

<span data-ttu-id="4a13b-106">財務仕訳帳 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) の既存の機能を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-106">The existing functionality for financial journals (general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="4a13b-107">「1 つの伝票」としてこの機能を参照します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-107">We refer to this functionality as "One voucher."</span></span> <span data-ttu-id="4a13b-108">1 つの伝票は、次のいずれかの方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-108">You can create One voucher by using one of the following methods:</span></span>

-   <span data-ttu-id="4a13b-109">仕訳帳名を設定し ([一般会計] \> [仕訳帳の設定] \>[仕訳帳名]) [新しい伝票] フィールドを [1 つの伝票番号のみ] に設定します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-109">Set up the journal name (**General ledger** \> **Journal setup** \>**Journal names**) so that the **New voucher** field is set to **One voucher number only**.</span></span> <span data-ttu-id="4a13b-110">\* 仕訳帳に追加するすべての明細行が、同じ伝票に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-110">\* Every line that you add to the journal is now included on the same voucher.</span></span> <span data-ttu-id="4a13b-111">すべての明細行が同じ伝票に追加されるため、伝票は、複数行の伝票、同じ明細行の勘定/相手勘定、または組み合わせとして入力することができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-111">Because every line is added to the same voucher, the voucher can be entered as a multiline voucher, as an account/offset account on the same line, or as a combination.</span></span>

<span data-ttu-id="4a13b-112">[![単一明細行](./media/same-line.png)](./media/same-line.png)</span><span class="sxs-lookup"><span data-stu-id="4a13b-112">[![Single line](./media/same-line.png)](./media/same-line.png)</span></span>
 
> [!IMPORTANT] 
> *  <span data-ttu-id="4a13b-113">「1 つの伝票」の定義には **1 つの伝票番号** のみとして設定されている仕訳帳名が含まれていないこと、さらにユーザーは勘定科目タイプのみを含む伝票を入力することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4a13b-113">Note that the definition of ‘One voucher’ does NOT include journal names that are set up as **One voucher number** only and the user then enters a voucher which only includes Ledger account types.</span></span>  <span data-ttu-id="4a13b-114">このドキュメントでは、「1 つの伝票」は、複数の仕入先、顧客、銀行、固定資産、またはプロジェクトを含む 1 つの伝票があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-114">In this document, ‘One voucher’ means that there is one voucher that contains more than one vendor, customer, bank, fixed asset, or project.</span></span> 

-   <span data-ttu-id="4a13b-115">相手勘定が存在しない複数行の伝票を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-115">Enter a multiline voucher where there is no offset account.</span></span>

<span data-ttu-id="4a13b-116">[![複数行の伝票](./media/Multi-line.png)](./media/Multi-line.png)</span><span class="sxs-lookup"><span data-stu-id="4a13b-116">[![Multiline voucher](./media/Multi-line.png)](./media/Multi-line.png)</span></span>

-   <span data-ttu-id="4a13b-117">勘定と相手勘定の両方に、仕入先/仕入先、顧客/顧客、仕入先/顧客または銀行/銀行などの補助元帳勘定タイプが含まれる伝票を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-117">Enter a voucher where both the account and the offset account contain a subledger account type, such as vendor/vendor, Customer/customer, vendor/customer, or bank/bank.</span></span>

<span data-ttu-id="4a13b-118">[![補助元帳伝票](./media/subledger.png)](./media/subledger.png)</span><span class="sxs-lookup"><span data-stu-id="4a13b-118">[![Subledger voucher](./media/subledger.png)](./media/subledger.png)</span></span>

<a name="issues-with-one-voucher"></a><span data-ttu-id="4a13b-119">1 つの伝票に関する問題</span><span class="sxs-lookup"><span data-stu-id="4a13b-119">Issues with One voucher</span></span>
=======================

<span data-ttu-id="4a13b-120">1 つの伝票機能により、決済、税計算、補助元帳の一般会計への調整、財務報告などの間に問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-120">The One voucher functionality causes issues during settlement, tax calculation, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="4a13b-121">(たとえば、決済時に発生する可能性がある問題についての詳細については、[複数の顧客または仕入先レコードを持つ単一伝票](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records) を参照してください。) 正しく作業しレポートするために、これらのプロセスとレポートにはトランザクションの詳細が必要です。</span><span class="sxs-lookup"><span data-stu-id="4a13b-121">(For example, for more information about issues that can occur during settlement, see [Single voucher with multiple customer or vendor records](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) To work and report correctly, these processes and reports require transaction details.</span></span> <span data-ttu-id="4a13b-122">組織の設定に基づいて、いくつかのシナリオが正しく機能する場合もありますが、1 つの伝票に複数のトランザクションが入力された場合によく問題があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-122">Although some scenarios might still work correctly, based on your organization's setup, there are often issues when multiple transactions are entered in one voucher.</span></span>

<span data-ttu-id="4a13b-123">たとえば、次の複数行の伝票を転記します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-123">For example, you post the following multiline voucher.</span></span>

<span data-ttu-id="4a13b-124">[![例](./media/example.png)](./media/example.png)</span><span class="sxs-lookup"><span data-stu-id="4a13b-124">[![Example](./media/example.png)](./media/example.png)</span></span>

<span data-ttu-id="4a13b-125">そして、**財務インサイト** ワークスペースの **仕入先** レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-125">You then generate the **Expenses by vendor** report in the **Financial Insights** workspace.</span></span> <span data-ttu-id="4a13b-126">レポートは、仕入先グループと仕入先の経費勘定残高をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-126">The report groups expense account balances under vendor group and then vendor.</span></span> <span data-ttu-id="4a13b-127">レポートを生成する際、システムは 250.00 の費用を負担した仕入先グループ/仕入先の発生を特定できません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-127">When generating the report, the system can't determine which vendor groups/vendors incurred the expense of 250.00.</span></span> <span data-ttu-id="4a13b-128">トランザクションの詳細が欠落しているため、システムは、伝票で見つけた最初の仕入先によって 250.00 全体が発生したものと見なされます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-128">Because transaction details are missing, the system assumes the whole 250.00 was incurred by the first vendor found in the voucher.</span></span> <span data-ttu-id="4a13b-129">主勘定 600120 の残高に含まれている 250.00 は、仕入先グループ/仕入先の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-129">The 250.00, which is included in the balance for main account 600120, is then shown under that vendor group/vendor.</span></span> <span data-ttu-id="4a13b-130">仕入先の最初の仕入先が正しい仕入先でなく、レポートが間違っている可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-130">It’s very likely that the first vendor in the voucher was not the correct vendor, so the report is incorrect.</span></span>

<span data-ttu-id="4a13b-131">[![経費](./media/expenses.png)](./media/expenses.png)</span><span class="sxs-lookup"><span data-stu-id="4a13b-131">[![Expenses](./media/expenses.png)](./media/expenses.png)</span></span>

<a name="the-future-of-one-voucher"></a><span data-ttu-id="4a13b-132">1 つの伝票の今後</span><span class="sxs-lookup"><span data-stu-id="4a13b-132">The future of One voucher</span></span>
=========================

<span data-ttu-id="4a13b-133">前述の問題のため、1 つの伝票機能は、廃止されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-133">Because of the issues that were stated earlier, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="4a13b-134">ただし、この機能に依存する機能的なギャップがあるため、機能が一度に無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-134">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at once.</span></span> <span data-ttu-id="4a13b-135">代わりに、次のスケジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-135">Instead, we will use the following schedule:</span></span> 

- <span data-ttu-id="4a13b-136">**2018 年春リリース** – 機能は、既定で総勘定元帳のパラメーターによってオフになります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-136">**Spring 2018 release** – The functionality will be turned off by default through a General ledger parameter.</span></span> <span data-ttu-id="4a13b-137">ただし、組織がこのトピックの後半に記載されているビジネス シナリオ ギャップの範囲内にシナリオがある場合、機能をオンにできます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-137">However, you can turn the functionality on if your organization has a scenario that falls in the business scenario gaps that are listed later in this topic.</span></span>

  -   <span data-ttu-id="4a13b-138">顧客が 1 つの伝票を必要としないビジネス シナリオがある場合、機能をオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="4a13b-138">If a customer has a business scenario that doesn't require One voucher, don't turn the functionality on.</span></span> <span data-ttu-id="4a13b-139">別のソリューションが存在するにもかかわらずこの機能が使用されている場合は、このトピックで後から識別された領域の「バグ」は修正されません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-139">We won't fix "bugs" in the areas that were identified later in this topic if this functionality is used even though another solution exists.</span></span>

  -   <span data-ttu-id="4a13b-140">機能のギャップのいずれかに機能が必要でない限り、Microsoft Dynamics 365 Finance and Operations への統合に 1 つの伝票を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="4a13b-140">Stop using One voucher for integrations into Microsoft Dynamics 365 Finance and Operations, unless the functionality is required for one of the functional gaps.</span></span>

- <span data-ttu-id="4a13b-141">**2018 年秋およびそれ以降のリリース** – 機能的なギャップが埋まります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-141">**Fall 2018 and later releases** – The functional gaps will be filled.</span></span> <span data-ttu-id="4a13b-142">機能的なギャップが埋められた後、1 つの伝票の機能が完全にオフになります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-142">After the functional gaps are filled, the One voucher functionality will be permanently turned off.</span></span>

- > [!IMPORTANT]
  > <span data-ttu-id="4a13b-143">[**1 つの伝票番号のみ**] オプションは、仕訳帳名の設定から削除されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4a13b-143">Please note that the **One voucher number only** option has NOT been removed from the Journal name setup.</span></span>  <span data-ttu-id="4a13b-144">このオプションは、伝票に勘定科目タイプのみ含まれている場合でもサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-144">This option is still supported when the voucher only contains Ledger account types.</span></span>  <span data-ttu-id="4a13b-145">[**1 つの伝票番号のみ**] を使用しながら複数の顧客、仕入先、銀行、固定資産、またはプロジェクトを入力する場合、伝票には転記しないため、顧客がこの設定を使用する場合には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="4a13b-145">Customers must be careful when using this setting because the voucher will not post if they use **One voucher number only** but then enter more than one customer, vendor, bank, fixed asset, or project.</span></span>  <span data-ttu-id="4a13b-146">また、顧客は、仕入先/銀行の勘定タイプを含む単一伝票内の支払などの、補助元帳仕訳タイプの組み合わせを入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-146">Also, customers can still enter a mix of subledger account types, such as a payment within a single voucher that contains account types of Vendor/Bank.</span></span>  

<a name="why-use-one-voucher"></a><span data-ttu-id="4a13b-147">1 つの伝票を使用する理由</span><span class="sxs-lookup"><span data-stu-id="4a13b-147">Why use One voucher?</span></span>
====================

<span data-ttu-id="4a13b-148">顧客との通話内容に基づき、顧客が 1 つの伝票機能を使用するシナリオ、またはその使用理由の一覧を次にコンパイルしました。</span><span class="sxs-lookup"><span data-stu-id="4a13b-148">Based on conversations with customers, we have compiled the following list of scenarios where customers use the One voucher functionality or reasons why they use it.</span></span> <span data-ttu-id="4a13b-149">これらのビジネス要件のいくつかは、1 つの伝票を使用することによってのみ満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-149">Some of these business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="4a13b-150">ただし、多くのシナリオでは、代替の方法で同じ業務要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-150">However, for many scenarios, alternatives can meet the same business requirements.</span></span>

<a name="scenarios-that-require-one-voucher"></a><span data-ttu-id="4a13b-151">1 つの伝票を必要とするシナリオ</span><span class="sxs-lookup"><span data-stu-id="4a13b-151">Scenarios that require One voucher</span></span>
----------------------------------

<span data-ttu-id="4a13b-152">次のシナリオは、1 つの伝票機能を使用することによってのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-152">The following scenarios can be accomplished only by using the One voucher functionality.</span></span> <span data-ttu-id="4a13b-153">これらの機能のギャップは、2018 年秋以降にリリースされる他の機能によって解決されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-153">These functional gaps will be filled through other features in the Fall 2018 and later releases.</span></span>

-   <span data-ttu-id="4a13b-154">**銀行口座に要約形式で仕入先または顧客支払を転記**</span><span class="sxs-lookup"><span data-stu-id="4a13b-154">**Post vendor or customer payments in summary form to a bank account**</span></span>

    -   <span data-ttu-id="4a13b-155">組織は、仕入先と金額のリストを銀行に伝え、銀行は、このリストを使用して、組織の代わりに仕入先に支払います。</span><span class="sxs-lookup"><span data-stu-id="4a13b-155">An organization communicates a list of vendors and amounts to its bank, and the bank uses this list to pay the vendors on the organization's behalf.</span></span> <span data-ttu-id="4a13b-156">銀行は、支払いの合計を 1 回の引き落としとして銀行口座に転記します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-156">The bank posts the sum of the payments as a single withdrawal on the bank account.</span></span>

>   <span data-ttu-id="4a13b-157">仕入先支払の集計は、1 つの伝票でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-157">Summarization of vendor payments is supported only through One voucher.</span></span> <span data-ttu-id="4a13b-158">各仕入先は、買掛金勘定補助元帳での詳細を管理する個別の行として入力されますが、すべての支払の集計金額は銀行口座の単一明細行に相殺されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-158">Each vendor is entered as a separate line to maintain detail in the Accounts payable subledger, but the summarized amount for all the payments is offset to a single line for the bank account.</span></span> <span data-ttu-id="4a13b-159">したがって、払戻しは銀行補助元帳に単一の集計金額として示されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-159">Therefore, the withdrawal is shown as a single summarized amount in the bank subledger.</span></span>

-   <span data-ttu-id="4a13b-160">組織が顧客支払を預金するか、または銀行が組織の代わりに顧客支払を預金すると、その預金は、銀行口座の一括比例配分として表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-160">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

>   <span data-ttu-id="4a13b-161">顧客支払の集計は通常、預金機能でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-161">Summarization of customer payments is typically supported through the deposit functionality.</span></span> <span data-ttu-id="4a13b-162">ただし、支払方法に「つなぎ」を使用している場合、このシナリオは 1 つの伝票でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-162">However, if you're using "bridging" on the method of payment, this scenario is supported only through One voucher.</span></span> <span data-ttu-id="4a13b-163">顧客支払は、仕入先支払の集計と同じ方法で入力します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-163">The customer payments are entered in the same manner that is described for vendor payment summarization.</span></span>

-   <span data-ttu-id="4a13b-164">**ビジネス イベントからトランザクションをグループ化するメカニズム**</span><span class="sxs-lookup"><span data-stu-id="4a13b-164">**Mechanism to group transactions from a business event**</span></span>

    -   <span data-ttu-id="4a13b-165">組織には、複数のトランザクションをトリガーする 1 つのビジネス イベントがあります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-165">An organization has a single business event that triggers multiple transactions.</span></span> <span data-ttu-id="4a13b-166">ただし、経理部門は、監査性を高めるために勘定項目をまとめて表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-166">However, the Accounting department wants to view the accounting entries together for better auditability.</span></span>

>   <span data-ttu-id="4a13b-167">組織がビジネス イベントからまとめて勘定項目を表示する必要がある場合、1 つの伝票を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-167">If an organization must view the accounting entries from a business event together, it must use One voucher.</span></span> 

- <span data-ttu-id="4a13b-168">**国固有の機能**</span><span class="sxs-lookup"><span data-stu-id="4a13b-168">**Country-specific features**</span></span>

  -   <span data-ttu-id="4a13b-169">ポーランドの単一管理ドキュメント (SAD) 機能では、現在、単一の伝票を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-169">The Single Administrative Document (SAD) feature for Poland currently requires that a single voucher be used.</span></span> <span data-ttu-id="4a13b-170">この機能でグループ化オプションを使用できるようになるまで、引き続き 1 つの伝票機能を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-170">Until a grouping option is available for this feature, you must continue to use the One voucher functionality.</span></span> <span data-ttu-id="4a13b-171">1 つの伝票機能を必要とする、追加の国特有の機能が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-171">There may be additional country-specific features that require the One voucher functionality.</span></span>

- <span data-ttu-id="4a13b-172">**複数の「明細行」に課税される顧客の前払支払仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="4a13b-172">**Customer prepayment payment journal that has taxes on multiple "lines"**</span></span>

  -   <span data-ttu-id="4a13b-173">顧客が注文の前払をして、注文明細行には、前払のために記録する必要のある異なる税金があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-173">A customer makes a prepayment for an order, and the lines of the order have different taxes that must be recorded for the prepayment.</span></span> <span data-ttu-id="4a13b-174">前払の顧客支払は、注文の明細行をシミュレートする 1 つのトランザクションであるため、各明細行の金額に対して適切な税金を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-174">The prepayment customer payment is one transaction that simulates the lines of the order, so that the appropriate tax can be recorded for the amount on each line.</span></span>

<span data-ttu-id="4a13b-175">このシナリオでは、トランザクションが顧客注文をシミュレートするため、1 つの伝票内の顧客は同じ顧客です。</span><span class="sxs-lookup"><span data-stu-id="4a13b-175">In this scenario, the customers in the single voucher are the same customer, because the transaction simulates the lines of a customer order.</span></span> <span data-ttu-id="4a13b-176">前払いは 1 つの伝票に入力する必要があります。これは、税金の計算が、顧客が行った 1 つの支払の「明細行」で行われなければならないためです。</span><span class="sxs-lookup"><span data-stu-id="4a13b-176">The prepayment must be entered in a single voucher, because the tax calculation must be made on the "lines" of the single payment that the customer made.</span></span>

-   <span data-ttu-id="4a13b-177">**固定資産の保守: 減価償却の遡及、資産の分割、処分時の減価償却の計算**</span><span class="sxs-lookup"><span data-stu-id="4a13b-177">**Fixed asset maintenance: Catch-up depreciation, split asset, calculate depreciation on disposal**</span></span>

<span data-ttu-id="4a13b-178">以下の固定資産トランザクションでは、単一の伝票内に複数のトランザクションも作成されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-178">The following fixed asset transactions also create multiple transactions within a single voucher:</span></span>
-   <span data-ttu-id="4a13b-179">資産の追加取得が行われ、減価償却の「遡及」が計算されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-179">An additional acquisition is made on an asset and ‘catch-up’ depreciation is calculated.</span></span>
-   <span data-ttu-id="4a13b-180">資産が分割されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-180">An asset is split.</span></span>
-   <span data-ttu-id="4a13b-181">処分時の減価償却を計算するためのパラメーターは有効になり、資産が処分されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-181">A parameter to calculate depreciation on disposal is enabled and then the asset is disposed.</span></span>

<a name="scenarios-that-dont-require-one-voucher"></a><span data-ttu-id="4a13b-182">1 つの伝票を必要としないシナリオ</span><span class="sxs-lookup"><span data-stu-id="4a13b-182">Scenarios that don't require One voucher</span></span>
----------------------------------------

<span data-ttu-id="4a13b-183">次のシナリオでは他の方法で行うことができますが、1 つの伝票を使用することができません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-183">The following scenarios can be accomplished through other means and should not use One voucher.</span></span>

-   <span data-ttu-id="4a13b-184">**銀行口座に要約形式で顧客支払を転記**</span><span class="sxs-lookup"><span data-stu-id="4a13b-184">**Post customer payments in summary form to the bank account**</span></span>

<span data-ttu-id="4a13b-185">組織が顧客支払を預金するか、または銀行が組織の代わりに顧客支払を預金すると、その預金は、銀行口座の一括比例配分として表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-185">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="4a13b-186">顧客支払いの集計は、支払い方法につなぎが使用されていない場合に預金機能によってサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-186">Summarization of customer payments is supported through the deposit  functionality when bridging isn't used on the method of payment.</span></span>

-   <span data-ttu-id="4a13b-187">**相殺決済**</span><span class="sxs-lookup"><span data-stu-id="4a13b-187">**Netting**</span></span>

<span data-ttu-id="4a13b-188">相殺では、仕入先と顧客が同じ関係者であるため、仕入先および顧客に対する残高は相互に相殺されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-188">In netting, the balances for a vendor and customer are netted against each other because the vendor and customer are the same party.</span></span> <span data-ttu-id="4a13b-189">このアプローチは、組織および顧客/仕入先関係者間の金銭の交換を最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-189">This approach minimizes the exchange of money between an organization and the customer/vendor party.</span></span>

<span data-ttu-id="4a13b-190">別の伝票に増減を入力することによって相殺決済を完了でき、清算する勘定科目に相殺を転記します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-190">Netting can be accomplished by entering the increase and decrease in separate vouchers, and posting the offset to a clearing ledger account.</span></span>

-   <span data-ttu-id="4a13b-191">**総勘定元帳に要約で転記**</span><span class="sxs-lookup"><span data-stu-id="4a13b-191">**Post in summary to the general ledger**</span></span>

<span data-ttu-id="4a13b-192">多くの場合、組織はデータの量を最小限に抑えるため、一般会計の集計を転記することがあります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-192">Organizations often want to post to the general ledger in summary to minimize the amount of data.</span></span> <span data-ttu-id="4a13b-193">ただし、通常、組織はやはりトランザクションの詳細を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-193">However, the organizations typically still require that the transaction detail be maintained.</span></span> <span data-ttu-id="4a13b-194">1 つの伝票で転記が集計された場合、取引の詳細は不明であり、管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-194">When posting is done in summary through a single voucher, the transaction detail isn't known and can't be maintained.</span></span>

   -   <span data-ttu-id="4a13b-195">現在トランザクションの詳細を管理することはできないため、集計で転記するために 1 つの伝票を使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4a13b-195">Because the transaction detail currently can't be maintained, we recommend that One voucher not be used to post in summary.</span></span>
   -   <span data-ttu-id="4a13b-196">1 つの伝票のサポートが削除された後、元伝票と会計フレームワークを仕訳帳に実装することができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-196">After support for One voucher is removed, we can implement the Source document and Accounting frameworks into the journals.</span></span> <span data-ttu-id="4a13b-197">これらのフレームワークは、トランザクションの詳細を管理し、総勘定元帳に集計をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4a13b-197">These frameworks, will then maintain the transaction detail and support summarization into the general ledger.</span></span>

-   <span data-ttu-id="4a13b-198">**同じ請求書に転記されていない複数の支払を決済**</span><span class="sxs-lookup"><span data-stu-id="4a13b-198">**Settle multiple unposted payments to the same invoice**</span></span>

<span data-ttu-id="4a13b-199">このシナリオは通常、顧客が複数の支払い方法を使用して購入代金を支払うことができる小売企業にあります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-199">This scenario is typically found in retail organizations where customers can use multiple methods of payment to pay for purchases.</span></span> <span data-ttu-id="4a13b-200">このシナリオでは、組織は転記されていない複数の支払を記録し、顧客請求書に対して決済をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-200">In this scenario, the organization must be able to record multiple unposted payments and settle them against the customer invoice.</span></span>

<span data-ttu-id="4a13b-201">Microsoft Dynamics 365 for Operations バージョン 1611 (2016 年 11 月) に追加された新機能により、単一の請求書に対して転記されていない複数の支払が決済されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-201">A new feature that was added in Microsoft Dynamics 365 for Operations version 1611 (November 2016) enables multiple unposted payments to be settled against a single invoice.</span></span> <span data-ttu-id="4a13b-202">複数の顧客支払は、1 つの伝票で入力する必要はもうありません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-202">Multiple customer payments no longer have to be entered in a single voucher.</span></span>

-   <span data-ttu-id="4a13b-203">**口座取引明細書トランザクションのインポート**</span><span class="sxs-lookup"><span data-stu-id="4a13b-203">**Import bank statement transactions**</span></span>

<span data-ttu-id="4a13b-204">銀行は、しばしば組織に代わって支払を支払い、受入れるが、これらのトランザクションは、銀行から受け取ったファイルを介して Finance and Operations に記録されます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-204">Banks often pay and receive payments on an organization's behalf, and these transactions are recorded in Finance and Operations through a file that is received from the bank.</span></span> <span data-ttu-id="4a13b-205">多くの場合、組織はファイル内の口座取引明細書を使用して、これらのトランザクションをグループ化することがあります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-205">Organizations often want to group together those transactions by using the bank statement number in the file.</span></span> <span data-ttu-id="4a13b-206">各トランザクションが口座取引明細書に詳細に表示されているため、銀行補助元帳で集計は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-206">Because each transaction is shown in detail on the bank statement, no summarization is required in the bank subledger.</span></span>

<span data-ttu-id="4a13b-207">仕訳帳バッチ番号や伝票番号など、ジャーナルの他のフィールドを使用してトランザクションをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-207">Transactions can be grouped by using other fields on the journal, such as the journal batch number itself or the document number.</span></span>

-   <span data-ttu-id="4a13b-208">**転送残高**</span><span class="sxs-lookup"><span data-stu-id="4a13b-208">**Transfer balances**</span></span>

<span data-ttu-id="4a13b-209">間違いもしくは別の仕入先が負債を引き継いでいるため、組織は、1 つの仕入先から別の仕入先に残高を転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-209">An organization might have to transfer a balance from one vendor to another vendor, either because of a mistake or because another vendor has taken over the liability.</span></span> <span data-ttu-id="4a13b-210">このタイプの転送は、顧客や銀行口座などの勘定タイプに対しても発生します。</span><span class="sxs-lookup"><span data-stu-id="4a13b-210">Transfers of this type also occur for account types such as customers and bank accounts.</span></span>

<span data-ttu-id="4a13b-211">ある勘定 (仕入先、顧客、銀行勘定など) から別の勘定への残高の振替は、個別の伝票を介して行うことができ、相殺は、清算する勘定科目に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-211">Balance transfers from one account (vendor, customer, bank account, and so on) to another account can be done through separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

-   <span data-ttu-id="4a13b-212">**期首残高の入力**</span><span class="sxs-lookup"><span data-stu-id="4a13b-212">**Enter beginning balances**</span></span>

<span data-ttu-id="4a13b-213">多くの場合、組織は 1 つの伝票トランザクションとして補助元帳 (仕入先、顧客、固定資産など) の期首残高を入力することがあります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-213">Organizations often enter beginning balances for subledger accounts (vendors, customers, fixed assets, and so on) as one voucher transaction.</span></span> <span data-ttu-id="4a13b-214">各補助元帳勘定の期首残高は、別々の伝票に入力することができ、相殺は、清算する勘定科目に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="4a13b-214">Beginning balances for each subledger account can be entered as separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

-   <span data-ttu-id="4a13b-215">**転記済の顧客または仕入先ドキュメントの簿記入力を修正する**</span><span class="sxs-lookup"><span data-stu-id="4a13b-215">**Correct the accounting entry of a posted customer or vendor document**</span></span>

<span data-ttu-id="4a13b-216">組織は、転記済請求書の簿記入力のために、売掛金勘定または買掛金勘定の勘定科目を修正する必要がありますが、その請求書は、別のメカニズムを通じて取り消すことも修正することもできません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-216">An organization might have to correct the Accounts receivable or Accounts payable ledger account for an accounting entry of a posted invoice, but that invoice can't be reversed or corrected through another mechanism.</span></span>

<span data-ttu-id="4a13b-217">売掛金勘定または買掛金勘定の勘定科目で修正を行う必要がある場合、調整は勘定科目に対して直接実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-217">If a correction must be made to the accounts receivable or accounts payable ledger account, an adjustment must be made directly to the ledger account.</span></span> <span data-ttu-id="4a13b-218">仕入先または顧客への転記によって調整することはできません。</span><span class="sxs-lookup"><span data-stu-id="4a13b-218">The adjustment can't be made by posting through the vendor or customer.</span></span> <span data-ttu-id="4a13b-219">このアプローチでは、「停止時間」に調整を行う必要があるため、勘定科目で一時的に手動入力が可能になります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-219">This approach requires that the adjustment be made during a "down time," so that the ledger account can temporarily allow manual entry.</span></span>

-   <span data-ttu-id="4a13b-220">**「システムはそれを許可します」**</span><span class="sxs-lookup"><span data-stu-id="4a13b-220">**"The system allows it"**</span></span>

<span data-ttu-id="4a13b-221">組織は多くの場合、システムが影響を理解することなくそれらを使用できるようにするため、単なる 1 つのバウチャー機能を使用することがあります。</span><span class="sxs-lookup"><span data-stu-id="4a13b-221">Organizations often use the One voucher functionality merely because the system lets them use it, without understanding the implications.</span></span>

