---
title: 1 つの伝票
description: 財務仕訳帳の 1 つの伝票 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクションを入力できます。
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 68ec3cb028462865e914cbcb25ff28dbaf9a4f01
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3058020"
---
# <a name="one-voucher"></a><span data-ttu-id="afd8c-103">1 つの伝票</span><span class="sxs-lookup"><span data-stu-id="afd8c-103">One voucher</span></span>

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a><span data-ttu-id="afd8c-104">1 つの伝票とは？</span><span class="sxs-lookup"><span data-stu-id="afd8c-104">What is One voucher?</span></span>

<span data-ttu-id="afd8c-105">財務仕訳帳 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) の既存の機能を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクション (顧客、仕入先、固定資産、プロジェクト、および銀行) を入力できます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-105">The existing functionality for financial journals (the general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions (customer, vendor, fixed assets, project, and bank) in the context of a single voucher.</span></span> <span data-ttu-id="afd8c-106">Microsoft はこの機能を *1 つの伝票*として参照します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-106">Microsoft refers to this functionality as *One voucher*.</span></span> <span data-ttu-id="afd8c-107">1 つの伝票は、次のいずれかの方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-107">You can create a single voucher by using one of the following methods:</span></span>

- <span data-ttu-id="afd8c-108">仕訳帳名を設定し (**総勘定元帳** \> **仕訳帳の設定** \>**仕訳帳名**) **新しい伝票**フィールドを **1 つの伝票番号のみ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-108">Set up the journal name (**General ledger** \> **Journal setup** \> **Journal names**) so that the **New voucher** field is set to **One voucher number only**.</span></span> <span data-ttu-id="afd8c-109">仕訳帳に追加するすべての明細行が、同じ伝票に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-109">Every line that you add to the journal is now included in the same voucher.</span></span> <span data-ttu-id="afd8c-110">したがって、伝票は、複数行の伝票、同じ明細行の勘定/相手勘定、または組み合わせとして入力することができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-110">Therefore, the voucher can be entered as a multiline voucher, as an account/offset account on the same line, or as a combination.</span></span>

    <span data-ttu-id="afd8c-111">[![単一明細行](./media/same-line.png)](./media/same-line.png)</span><span class="sxs-lookup"><span data-stu-id="afd8c-111">[![Single line](./media/same-line.png)](./media/same-line.png)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="afd8c-112">1 つの伝票の定義は、仕訳帳名が**1 つの伝票番号のみ**として設定されている場合には対応**しません**。ユーザーは勘定タイプのみを含む伝票に入力します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-112">The definition of One voucher does **not** cover cases where journal names are set up as **One voucher number only**, but the user then enters a voucher that includes only ledger account types.</span></span> <span data-ttu-id="afd8c-113">このトピックでは、1 つの伝票は、複数の仕入先、顧客、銀行、固定資産、またはプロジェクトを含む 1 つの伝票があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-113">In this topic, One voucher means that there is a single voucher that contains more than one vendor, customer, bank, fixed asset, or project.</span></span>

- <span data-ttu-id="afd8c-114">相手勘定が存在しない複数行の伝票を入力します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-114">Enter a multiline voucher where there is no offset account.</span></span>

    <span data-ttu-id="afd8c-115">[![複数行の伝票](./media/Multi-line.png)](./media/Multi-line.png)</span><span class="sxs-lookup"><span data-stu-id="afd8c-115">[![Multiline voucher](./media/Multi-line.png)](./media/Multi-line.png)</span></span>

- <span data-ttu-id="afd8c-116">勘定と相手勘定の両方に、**仕入先**/**仕入先**、**顧客**/**顧客**、 **仕入先**/**顧客**、または**銀行**/**銀行**などの補助元帳勘定タイプが含まれる伝票を入力します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-116">Enter a voucher where both the account and the offset account contain a subledger account type, such as **Vendor**/**Vendor**, **Customer**/**Customer**, **Vendor**/**Customer**, or **Bank**/**Bank**.</span></span>

    <span data-ttu-id="afd8c-117">[![補助元帳伝票](./media/subledger.png)](./media/subledger.png)</span><span class="sxs-lookup"><span data-stu-id="afd8c-117">[![Subledger voucher](./media/subledger.png)](./media/subledger.png)</span></span>

## <a name="issues-with-one-voucher"></a><span data-ttu-id="afd8c-118">1 つの伝票に関する問題</span><span class="sxs-lookup"><span data-stu-id="afd8c-118">Issues with One voucher</span></span>

<span data-ttu-id="afd8c-119">1 つの伝票機能により、決済、税計算、トランザクションの取消、補助元帳の総勘定元帳への調整、財務報告などの間に問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-119">The One voucher functionality causes issues during settlement, tax calculation, transaction reversal, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="afd8c-120">たとえば、決済時に発生する可能性がある問題についての詳細については、[複数の顧客または仕入先レコードを持つ単一伝票](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records)を参照してください。 正しく作業しレポートするために、これらのプロセスとレポートにはトランザクションの詳細が必要です。</span><span class="sxs-lookup"><span data-stu-id="afd8c-120">(For more information about issues that can occur during settlement, see, for example, [Single voucher with multiple customer or vendor records](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records).) To work and report correctly, these processes and reports require transaction details.</span></span> <span data-ttu-id="afd8c-121">組織の設定に基づいて、いくつかのシナリオが正しく機能する場合もありますが、1 つの伝票に複数のトランザクションが入力された場合によく問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-121">Although some scenarios might still work correctly, depending on your organization's setup, there are often issues when multiple transactions are entered in one voucher.</span></span>

<span data-ttu-id="afd8c-122">たとえば、次の複数行の伝票を転記します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-122">For example, you post the following multiline voucher.</span></span>

<span data-ttu-id="afd8c-123">[![例](./media/example.png)](./media/example.png)</span><span class="sxs-lookup"><span data-stu-id="afd8c-123">[![Example](./media/example.png)](./media/example.png)</span></span>

<span data-ttu-id="afd8c-124">そして、**財務インサイト** ワークスペースの **仕入先** レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-124">You then generate the **Expenses by vendor** report in the **Financial Insights** workspace.</span></span> <span data-ttu-id="afd8c-125">このレポートでは、経費勘定残高が仕入先グループと仕入先別にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="afd8c-125">On this report, expense account balances are grouped by vendor group and then vendor.</span></span> <span data-ttu-id="afd8c-126">レポートを生成する際、システムは 250.00 の費用を負担した仕入先グループ/仕入先を特定できません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-126">When the report is generated, the system can't determine which vendor groups/vendors incurred the expense of 250.00.</span></span> <span data-ttu-id="afd8c-127">トランザクションの詳細が欠落しているため、システムは、伝票に記載された最初の仕入先によって 250.00 の費用が発生したものと見なします。</span><span class="sxs-lookup"><span data-stu-id="afd8c-127">Because transaction details are missing, the system assumes that the whole 250.00 expense was incurred by the first vendor that is found in the voucher.</span></span> <span data-ttu-id="afd8c-128">したがって、主勘定 600120 の残高に含まれている費用 250.00 は、仕入先グループ/仕入先の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-128">Therefore, the 250.00 expense, which is included in the balance for main account 600120, is shown under that vendor group/vendor.</span></span> <span data-ttu-id="afd8c-129">ただし、伝票の最初の仕入先が正しい仕入先ではない可能性が非常に高いです。</span><span class="sxs-lookup"><span data-stu-id="afd8c-129">However, it's very likely that the first vendor in the voucher isn't the correct vendor.</span></span> <span data-ttu-id="afd8c-130">したがって、レポートが正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-130">Therefore, the report is probably incorrect.</span></span>

<span data-ttu-id="afd8c-131">[![経費](./media/expenses.png)](./media/expenses.png)</span><span class="sxs-lookup"><span data-stu-id="afd8c-131">[![Expenses](./media/expenses.png)](./media/expenses.png)</span></span>

## <a name="the-future-of-one-voucher"></a><span data-ttu-id="afd8c-132">1 つの伝票の今後</span><span class="sxs-lookup"><span data-stu-id="afd8c-132">The future of One voucher</span></span>

<span data-ttu-id="afd8c-133">前述の問題のため、1 つの伝票機能は廃止されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-133">Because of the issues that were mentioned earlier, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="afd8c-134">ただし、この機能に依存する機能的なギャップがあるため、機能が一度に廃止になることはありません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-134">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at one time.</span></span> <span data-ttu-id="afd8c-135">代わりに、次のスケジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-135">Instead, the following schedule will be used:</span></span>

- <span data-ttu-id="afd8c-136">**2018 年春リリース** – 既定では、**総勘定元帳パラメーター** ページの**一般**タブの **1 つの伝票内で複数のトランザクションを許可する**パラメーターで、この機能は既定で無効になります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-136">**Spring 2018 release** – By default, the functionality will be turned off by default through the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="afd8c-137">ただし、組織にこのトピックの後半に記載されている機能的なギャップの 1 つに該当するシナリオがある場合、機能をオンにできます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-137">However, you can turn the functionality on if your organization has a scenario that falls into one of the functional gaps that are listed later in this topic.</span></span>

    - <span data-ttu-id="afd8c-138">顧客が 1 つの伝票を必要としないビジネス シナリオがある場合、機能をオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="afd8c-138">If customers have a business scenario that doesn't require One voucher, they shouldn't turn the functionality on.</span></span> <span data-ttu-id="afd8c-139">Microsoft は、別のソリューションが存在するにもかかわらずこの機能が使用されている場合、このトピックで後から識別された領域の「バグ」を修正しません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-139">Microsoft won't fix "bugs" in the areas that are identified later in this topic if this functionality is used even though another solution exists.</span></span>
    - <span data-ttu-id="afd8c-140">機能的なギャップのいずれかの機能が必要でない限り、 統合に 1 つの伝票を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="afd8c-140">Stop using One voucher for integrations, unless you need the functionality for one of the functional gaps.</span></span>

- <span data-ttu-id="afd8c-141">**以降のリリース** – すべての機能的なギャップが埋まります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-141">**Later releases** – All functional gaps will be filled.</span></span> <span data-ttu-id="afd8c-142">顧客および独立系ソフトウェア ベンダー (ISV) は、新機能に対応するのに十分な時間が必要なので、**機能的なギャップが埋まり新機能が提供された後に、 1 つの伝票が完全に無効になるまでには、少なくとも 1 年を要します**。</span><span class="sxs-lookup"><span data-stu-id="afd8c-142">**After the functional gaps are filled and new features are delivered, it will be at least one year before the One voucher functionality is permanently turned off**, because customers and independent software vendors (ISVs) must have enough time to react to the new functionality.</span></span> <span data-ttu-id="afd8c-143">たとえば、業務プロセス、エンティティ、統合を更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-143">For example, they might have to update their business processes, entities, and integrations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afd8c-144">**1 つの伝票番号のみ**オプションは、仕訳帳名の設定から削除されて**いません**。</span><span class="sxs-lookup"><span data-stu-id="afd8c-144">The **One voucher number only** option has **not** been removed from the Journal name setup.</span></span> <span data-ttu-id="afd8c-145">このオプションは、伝票に勘定科目タイプのみ含まれている場合でもサポートされます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-145">This option is still supported when the voucher contains only ledger account types.</span></span> <span data-ttu-id="afd8c-146">**1 つの伝票番号のみ**を使用しながら複数の顧客、仕入先、銀行、固定資産、またはプロジェクトを入力する場合、伝票は転記されないため、顧客がこの設定を使用する場合には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="afd8c-146">Customers must be careful when they use this setting, because the voucher won't be posted if they use the **One voucher number only** option but then enter more than one customer, vendor, bank, fixed asset, or project.</span></span> <span data-ttu-id="afd8c-147">また、顧客は、 **仕入先**/**銀行** の勘定タイプを含む単一伝票内の支払など、補助元帳仕訳タイプの組み合わせを入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-147">Additionally, customers can still enter a mix of subledger account types, such as a payment in a single voucher that contains the **Vendor**/**Bank** account types.</span></span>

## <a name="why-use-one-voucher"></a><span data-ttu-id="afd8c-148">1 つの伝票を使用する理由</span><span class="sxs-lookup"><span data-stu-id="afd8c-148">Why use One voucher?</span></span>

<span data-ttu-id="afd8c-149">顧客との通話内容に基づき、Microsoft は、顧客が 1 つの伝票機能を使用するシナリオ、またはその使用理由の一覧を次にコンパイルしました。</span><span class="sxs-lookup"><span data-stu-id="afd8c-149">Based on conversations with customers, Microsoft has compiled the following list of scenarios where customers use the One voucher functionality or reasons why they use it.</span></span> <span data-ttu-id="afd8c-150">これらのビジネス要件のいくつかは、1 つの伝票を使用することによってのみ満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-150">Some of these business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="afd8c-151">ただし、多くのシナリオでは、代替の方法で同じ業務要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-151">However, for many scenarios, alternatives can meet the same business requirements.</span></span>

### <a name="scenarios-that-require-one-voucher"></a><span data-ttu-id="afd8c-152">1 つの伝票を必要とするシナリオ</span><span class="sxs-lookup"><span data-stu-id="afd8c-152">Scenarios that require One voucher</span></span>

<span data-ttu-id="afd8c-153">次のシナリオは、1 つの伝票機能を使用することによってのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-153">The following scenarios can be accomplished only by using the One voucher functionality.</span></span> <span data-ttu-id="afd8c-154">組織にこれらのシナリオがある場合には、**総勘定元帳パラメーター** ページの、**1 つの伝票内で複数のトランザクションを許可する**パラメーターの設定を変更し、伝票に複数のトランザクションを入力できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-154">If your organization has any of these scenarios, you must enable multiple transactions to be entered in a voucher by changing the setting of the **Allow multiple transactions within one voucher** parameter on the **General ledger parameters** page.</span></span> <span data-ttu-id="afd8c-155">これらの機能のギャップは、以降にリリースされる他の機能によって解決されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-155">These functional gaps will be filled through other features in later releases.</span></span>

> [!Note]
> <span data-ttu-id="afd8c-156">[次の各シナリオでは、**一般会計パラメーター** ページの**一般**クイック タブで、バウチャー内の**1つの伝票内の複数のトランザクションを許可する**フィールドを はいに設定する必要があります。]</span><span class="sxs-lookup"><span data-stu-id="afd8c-156">[For each of the following scenarios the **Allow multiple transactions within one voucher** field must be set to Yes in the **General** FastTab on the **General ledger parameters** page.]</span></span>

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a><span data-ttu-id="afd8c-157">銀行口座に要約形式で仕入先または顧客支払を転記</span><span class="sxs-lookup"><span data-stu-id="afd8c-157">Post vendor or customer payments in summary form to a bank account</span></span>

<span data-ttu-id="afd8c-158">**シナリオ** 組織は仕入先と金額のリストを銀行に伝え、銀行は、このリストを使用して、組織の代わりに仕入先に支払います。</span><span class="sxs-lookup"><span data-stu-id="afd8c-158">**Scenario** An organization communicates a list of vendors and amounts to its bank, and the bank uses this list to pay the vendors on the organization's behalf.</span></span> <span data-ttu-id="afd8c-159">銀行は、支払いの合計を 1 回の引き落としとして銀行口座に転記します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-159">The bank posts the sum of the payments as a single withdrawal on the bank account.</span></span>

<span data-ttu-id="afd8c-160">仕入先支払の集計は、1 つの伝票でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-160">Summarization of vendor payments is supported only through One voucher.</span></span> <span data-ttu-id="afd8c-161">各仕入先は、買掛金勘定の補助元帳の詳細を維持するために別の行として入力されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-161">Each vendor is entered as a separate line to maintain details in the Accounts payable subledger.</span></span> <span data-ttu-id="afd8c-162">ただし、すべての支払の集計金額は、銀行口座の単一明細行に相殺されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-162">However, the summarized amount for all the payments is offset to a single line for the bank account.</span></span> <span data-ttu-id="afd8c-163">したがって、払戻しは銀行補助元帳に単一の集計金額として示されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-163">Therefore, the withdrawal is shown as a single summarized amount in the bank subledger.</span></span>

<span data-ttu-id="afd8c-164">**シナリオ** 組織が顧客支払を預金するか、または銀行が組織の代わりに顧客支払を預金すると、その預金は、銀行口座の一括比例配分として表示されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-164">**Scenario** An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="afd8c-165">顧客支払の集計は通常、預金機能でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-165">Summarization of customer payments is typically supported through the deposit functionality.</span></span> <span data-ttu-id="afd8c-166">ただし、支払方法に「つなぎ」を使用している場合、このシナリオは 1 つの伝票でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-166">However, if you're using "bridging" on the method of payment, this scenario is supported only through One voucher.</span></span> <span data-ttu-id="afd8c-167">顧客支払は、仕入先支払の集計と同じ方法で入力します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-167">The customer payments are entered in the same manner that is described for vendor payment summarization.</span></span>

### <a name="mechanism-to-group-transactions-from-a-business-event"></a><span data-ttu-id="afd8c-168">ビジネス イベントからトランザクションをグループ化するメカニズム</span><span class="sxs-lookup"><span data-stu-id="afd8c-168">Mechanism to group transactions from a business event</span></span>

<span data-ttu-id="afd8c-169">**シナリオ** 組織には、複数のトランザクションをトリガーする 1 つのビジネス イベントがあります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-169">**Scenario** An organization has a single business event that triggers multiple transactions.</span></span> <span data-ttu-id="afd8c-170">ただし、経理部門は、監査性を高めるために勘定項目をまとめて表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-170">However, the Accounting department wants to view the accounting entries together for better auditability.</span></span>

<span data-ttu-id="afd8c-171">組織がビジネス イベントからまとめて勘定項目を表示する必要がある場合、1 つの伝票を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-171">If an organization must view the accounting entries from a business event together, it must use One voucher.</span></span> 

### <a name="country-specific-features"></a><span data-ttu-id="afd8c-172">国固有の機能</span><span class="sxs-lookup"><span data-stu-id="afd8c-172">Country-specific features</span></span>

<span data-ttu-id="afd8c-173">**シナリオ** ポーランドの単一管理ドキュメント (SAD) 機能では、現在、単一の伝票を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-173">**Scenario** The Single Administrative Document (SAD) feature for Poland currently requires that a single voucher be used.</span></span> <span data-ttu-id="afd8c-174">この機能でグループ化オプションを使用できるようになるまで、引き続き 1 つの伝票機能を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-174">Until a grouping option is available for this feature, you must continue to use the One voucher functionality.</span></span> <span data-ttu-id="afd8c-175">1 つの伝票機能を必要とする、追加の国特有の機能が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-175">There may be additional country-specific features that require the One voucher functionality.</span></span>

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a><span data-ttu-id="afd8c-176">複数の「明細行」に課税される顧客の前払支払仕訳帳</span><span class="sxs-lookup"><span data-stu-id="afd8c-176">Customer prepayment payment journal that has taxes on multiple "lines"</span></span>

<span data-ttu-id="afd8c-177">このシナリオでは、トランザクションが顧客注文をシミュレートするため、1 つの伝票内の顧客は同じ顧客です。</span><span class="sxs-lookup"><span data-stu-id="afd8c-177">In this scenario, the customers in the single voucher are the same customer, because the transaction simulates the lines of a customer order.</span></span> <span data-ttu-id="afd8c-178">前払いは 1 つの伝票に入力する必要があります。これは、税金の計算が、顧客が行った 1 つの支払の「明細行」で行われなければならないためです。</span><span class="sxs-lookup"><span data-stu-id="afd8c-178">The prepayment must be entered in a single voucher, because the tax calculation must be made on the "lines" of the single payment that the customer made.</span></span>

### <a name="customer-reimbursement"></a><span data-ttu-id="afd8c-179">顧客払い戻し</span><span class="sxs-lookup"><span data-stu-id="afd8c-179">Customer reimbursement</span></span>

<span data-ttu-id="afd8c-180">**シナリオ** 顧客が注文の前払をする際、注文明細行には、前払のために記録する必要のある異なる税金が記載されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-180">**Scenario** A customer makes a prepayment for an order, and the lines of the order have different taxes that must be recorded for the prepayment.</span></span> <span data-ttu-id="afd8c-181">前払の顧客支払は、注文の明細行をシミュレートする 1 つのトランザクションであるため、各明細行の金額に対して適切な税金を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-181">The prepayment customer payment is one transaction that simulates the lines of the order, so that the appropriate tax can be recorded for the amount on each line.</span></span>

<span data-ttu-id="afd8c-182">売掛金勘定モジュールから払い戻し定期処理タスクを実行すると、顧客から仕入先に残高を移動するトランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-182">If the Reimbursement periodic task is run from the Accounts receivable module, it creates a transaction to move the balance from a customer to a vendor.</span></span> <span data-ttu-id="afd8c-183">このシナリオでは、顧客への払戻しに 1 つの伝票を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-183">For this scenario, One voucher must be used to reimburse the customer.</span></span>

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a><span data-ttu-id="afd8c-184">固定資産の保守: 減価償却の遡及、資産の分割、処分時の減価償却の計算</span><span class="sxs-lookup"><span data-stu-id="afd8c-184">Fixed asset maintenance: Catch-up depreciation, split asset, calculate depreciation on disposal</span></span>
<span data-ttu-id="afd8c-185">以下の固定資産トランザクションでは、単一の伝票内に複数のトランザクションも作成されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-185">The following fixed asset transactions also create multiple transactions in a single voucher:</span></span>

- <span data-ttu-id="afd8c-186">資産の追加取得が行われ、減価償却の「遡及」が計算されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-186">An additional acquisition is made on an asset, and "catch-up" depreciation is calculated.</span></span>
- <span data-ttu-id="afd8c-187">資産が分割されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-187">An asset is split.</span></span>
- <span data-ttu-id="afd8c-188">処分時の減価償却を計算するためのパラメーターは有効になり、資産が処分されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-188">A parameter to calculate depreciation on disposal is turned on, and then the asset is disposed of.</span></span>
- <span data-ttu-id="afd8c-189">資産利用開始日は、取得日付より前になります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-189">An asset's service date is before the acquisition date.</span></span> <span data-ttu-id="afd8c-190">したがって、減価償却調整額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-190">Therefore, a depreciation adjustment is posted.</span></span>

> [!Note]
> <span data-ttu-id="afd8c-191">トランザクションを入力するときは、すべてのトランザクションが同じ固定資産に適用されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-191">When you are entering transactions, be sure that all the transactions apply to the same fixed asset.</span></span> <span data-ttu-id="afd8c-192">**新しい伝票**フィールドが、一般会計の**仕訳帳名**ページでのみ 1 つの伝票番号に設定されている場合でも、複数の固定資産が含まれていると、伝票は転記されません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-192">The voucher won't be posted if it includes more than one fixed asset, even if the **New Voucher** field is set to One voucher number only on the **Journal names** page in General ledger.</span></span> <span data-ttu-id="afd8c-193">伝票に複数の固定資産を含めると、**1 つの伝票に対して指定できる固定資産トランザクションは 1 つのみです**というメッセージが表示され、伝票を転記することはできません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-193">If you include more than one fixed asset in the voucher, the message **There can only be one fixed asset transaction per voucher** will be displayed and you won't be able to post the voucher.</span></span>  

### <a name="bills-of-exchange-and-promissory-notes"></a><span data-ttu-id="afd8c-194">為替手形および約束手形</span><span class="sxs-lookup"><span data-stu-id="afd8c-194">Bills of exchange and promissory notes</span></span>
<span data-ttu-id="afd8c-195">支払の状態に基づいて、トランザクションは顧客または仕入先残高を 1 つの売掛金/買掛金元帳口座から別の口座に移動するために、為替手形および約束手形は、1 つの伝票を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-195">Bills of exchange and promissory notes require that One voucher be used, because the transactions move the customer or vendor balance from one Accounts receivable/Accounts payable ledger account to another, based on the state of the payment.</span></span>

## <a name="scenarios-that-dont-require-one-voucher"></a><span data-ttu-id="afd8c-196">1 つの伝票を必要としないシナリオ</span><span class="sxs-lookup"><span data-stu-id="afd8c-196">Scenarios that don't require One voucher</span></span>

<span data-ttu-id="afd8c-197">次のシナリオは、他の方法で実行することができますが、1 つの伝票機能を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-197">The following scenarios can be accomplished through other means and should not use the One voucher functionality.</span></span>

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a><span data-ttu-id="afd8c-198">銀行口座に要約形式で顧客支払を転記</span><span class="sxs-lookup"><span data-stu-id="afd8c-198">Post customer payments in summary form to the bank account</span></span>

<span data-ttu-id="afd8c-199">組織が顧客支払を預金するか、または銀行が組織の代わりに顧客支払を預金すると、その預金は、銀行口座の一括比例配分として表示されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-199">An organization deposits customer payments, or the bank deposits customer payments on the organization's behalf, and the deposit is shown as a lump sum on the bank account.</span></span>

<span data-ttu-id="afd8c-200">支払方法に「つなぎ」が使用されていない場合、顧客支払の集計は、預金機能でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-200">Summarization of customer payments is supported through the deposit functionality when "bridging" isn't used on the method of payment.</span></span>

### <a name="netting"></a><span data-ttu-id="afd8c-201">相殺決済</span><span class="sxs-lookup"><span data-stu-id="afd8c-201">Netting</span></span>

<span data-ttu-id="afd8c-202">相殺決済では、仕入先と顧客が同じ関係者であるため、仕入先および顧客に対する残高は相互に相殺されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-202">In netting, the balances for a vendor and customer are netted against each other, because the vendor and customer are the same party.</span></span> <span data-ttu-id="afd8c-203">このアプローチは、組織および顧客/仕入先関係者間の金銭の交換を最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-203">This approach minimizes the exchange of money between an organization and the customer/vendor party.</span></span>

<span data-ttu-id="afd8c-204">別の伝票に増減を入力することによって相殺決済を完了でき、清算する勘定科目に相殺を転記します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-204">Netting can be accomplished by entering the increase and decrease in separate vouchers, and then posting the offset to a clearing ledger account.</span></span>

### <a name="post-in-summary-to-the-general-ledger"></a><span data-ttu-id="afd8c-205">総勘定元帳に要約で転記</span><span class="sxs-lookup"><span data-stu-id="afd8c-205">Post in summary to the general ledger</span></span>

<span data-ttu-id="afd8c-206">多くの場合、組織はデータの量を最小限に抑えるため、要約形式で総勘定元帳に転記します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-206">Organizations often want to post to the general ledger in summary form to minimize the amount of data.</span></span> <span data-ttu-id="afd8c-207">ただし、通常、それらの組織はやはりトランザクションの詳細を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-207">However, those organizations typically still require that the transaction details be maintained.</span></span> <span data-ttu-id="afd8c-208">1 つの伝票を使用して要約形式で転記された場合、取引の詳細は不明であり、管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-208">When posting is done in summary form through a single voucher, the transaction details aren't known and can't be maintained.</span></span>

- <span data-ttu-id="afd8c-209">現在取引の詳細を維持することができないため、組織は要約形式で転記するために 1 つの伝票を使用**しない**ことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="afd8c-209">Because the transaction details currently can't be maintained, we recommend that organization **not** use One voucher to post in summary form.</span></span>
- <span data-ttu-id="afd8c-210">1 つの伝票のサポートが削除された後、元伝票と会計フレームワークを仕訳帳に実装することができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-210">After support for One voucher is removed, the Source document and Accounting frameworks can be implemented in the journals.</span></span> <span data-ttu-id="afd8c-211">これらのフレームワークは、トランザクションの詳細を管理し、総勘定元帳への集計をサポートします。</span><span class="sxs-lookup"><span data-stu-id="afd8c-211">These frameworks will then maintain the transaction details and support summarization into the general ledger.</span></span>


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a><span data-ttu-id="afd8c-212">同じ請求書に転記されていない複数の支払を決済</span><span class="sxs-lookup"><span data-stu-id="afd8c-212">Settle multiple unposted payments to the same invoice</span></span>

<span data-ttu-id="afd8c-213">このシナリオは通常、顧客が複数の支払い方法を使用して購入代金を支払うことができる企業にあります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-213">This scenario is typically found in organizations where customers can use multiple methods of payment to pay for purchases.</span></span> <span data-ttu-id="afd8c-214">このシナリオでは、組織は転記されていない複数の支払を記録し、顧客請求書に対して決済をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-214">In this scenario, the organization must be able to record multiple unposted payments and settle them against the customer invoice.</span></span>

<span data-ttu-id="afd8c-215">Microsoft Dynamics 365 for Operations バージョン 1611 (2016 年 11 月) に追加された新機能により、単一の請求書に対して転記されていない複数の支払が決済されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-215">A new feature that was added in Microsoft Dynamics 365 for Operations version 1611 (November 2016) enables multiple unposted payments to be settled against a single invoice.</span></span> <span data-ttu-id="afd8c-216">複数の顧客支払は、1 つの伝票で入力する必要はもうありません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-216">Multiple customer payments no longer have to be entered in a single voucher.</span></span>

### <a name="import-bank-statement-transactions"></a><span data-ttu-id="afd8c-217">口座取引明細書トランザクションのインポート</span><span class="sxs-lookup"><span data-stu-id="afd8c-217">Import bank statement transactions</span></span>

<span data-ttu-id="afd8c-218">銀行は、しばしば組織に代わって支払をしたり支払を受入れたりしますが、これらのトランザクションは、銀行から受け取ったファイルを介して財務に記録されます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-218">Banks often pay and receive payments on an organization's behalf, and those transactions are recorded in Finance through a file that is received from the bank.</span></span> <span data-ttu-id="afd8c-219">多くの場合、組織はファイル内の口座取引明細書を使用して、これらのトランザクションをグループ化することがあります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-219">Organizations often want to group together those transactions by using the bank statement number in the file.</span></span> <span data-ttu-id="afd8c-220">各トランザクションが口座取引明細書に詳細に表示されているため、銀行補助元帳で集計は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-220">Because each transaction is shown in detail on the bank statement, no summarization is required in the bank subledger.</span></span>

<span data-ttu-id="afd8c-221">仕訳帳バッチ番号や伝票番号など、ジャーナルの他のフィールドを使用してトランザクションをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-221">Transactions can be grouped by using other fields on the journal, such as the journal batch number itself or the document number.</span></span>


### <a name="transfer-balances"></a><span data-ttu-id="afd8c-222">転送残高</span><span class="sxs-lookup"><span data-stu-id="afd8c-222">Transfer balances</span></span>

<span data-ttu-id="afd8c-223">間違いもしくは別の仕入先が負債を引き継いでいるため、組織は、1 つの仕入先から別の仕入先に残高を転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-223">An organization might have to transfer a balance from one vendor to another vendor, either because of a mistake or because another vendor has taken over the liability.</span></span> <span data-ttu-id="afd8c-224">このタイプの転送は、**顧客**や**銀行**などの勘定タイプに対しても発生します。</span><span class="sxs-lookup"><span data-stu-id="afd8c-224">Transfers of this type also occur for account types such as **Customer** and **Bank**.</span></span>

<span data-ttu-id="afd8c-225">ある勘定 (仕入先、顧客、銀行など) から別の勘定への残高の振替は、個別の伝票を介して行うことができ、相殺は、清算する勘定科目に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-225">Balance transfers from one account (vendor, customer, bank, and so on) to another account can be done through separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

### <a name="enter-beginning-balances"></a><span data-ttu-id="afd8c-226">期首残高の入力</span><span class="sxs-lookup"><span data-stu-id="afd8c-226">Enter beginning balances</span></span>

<span data-ttu-id="afd8c-227">多くの場合、組織は 1 つの伝票トランザクションとして補助元帳 (仕入先、顧客、固定資産など) の期首残高を入力することがあります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-227">Organizations often enter beginning balances for subledger accounts (vendors, customers, fixed assets, and so on) as one voucher transaction.</span></span> <span data-ttu-id="afd8c-228">各補助元帳勘定の期首残高は、別々の伝票に入力することができ、相殺は、清算する勘定科目に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="afd8c-228">Beginning balances for each subledger account can be entered as separate vouchers, and the offset can be posted to a clearing ledger account.</span></span>

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a><span data-ttu-id="afd8c-229">転記済の顧客または仕入先ドキュメントの簿記入力を修正する</span><span class="sxs-lookup"><span data-stu-id="afd8c-229">Correct the accounting entry of a posted customer or vendor document</span></span>

<span data-ttu-id="afd8c-230">組織は、転記済請求書の簿記入力のために、売掛金勘定または買掛金勘定の勘定科目を修正する必要がありますが、その請求書は、別のメカニズムを通じて取り消すことも修正することもできません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-230">An organization might have to correct the Accounts receivable or Accounts payable ledger account for an accounting entry of a posted invoice, but that invoice can't be reversed or corrected through another mechanism.</span></span>

<span data-ttu-id="afd8c-231">売掛金勘定または買掛金勘定の勘定科目で修正を行う必要がある場合、調整は勘定科目に対して直接実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-231">If a correction must be made to the Accounts receivable or Accounts payable ledger account, an adjustment must be made directly to the ledger account.</span></span> <span data-ttu-id="afd8c-232">仕入先または顧客への転記によって調整することはできません。</span><span class="sxs-lookup"><span data-stu-id="afd8c-232">The adjustment can't be made by posting through the vendor or customer.</span></span> <span data-ttu-id="afd8c-233">このアプローチでは、「停止時間」に調整を行う必要があるため、勘定科目で一時的に手動入力が可能になります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-233">This approach requires that the adjustment be made during a "down time," so that the ledger account can temporarily allow manual entry.</span></span>

### <a name="the-system-allows-it"></a><span data-ttu-id="afd8c-234">システムはそれを許可します</span><span class="sxs-lookup"><span data-stu-id="afd8c-234">"The system allows it"</span></span>

<span data-ttu-id="afd8c-235">組織は多くの場合、システムが影響を理解することなくそれらを使用できるようにするため、単なる 1 つのバウチャー機能を使用することがあります。</span><span class="sxs-lookup"><span data-stu-id="afd8c-235">Organizations often use the One voucher functionality merely because the system lets them use it, without understanding the implications.</span></span>
