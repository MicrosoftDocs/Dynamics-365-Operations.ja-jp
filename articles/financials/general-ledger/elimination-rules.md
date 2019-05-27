---
title: 削除ルール
description: このトピックでは、消去ルールと、消去に関するレポートのさまざまなオプションについて説明します。
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0736d63c9a582948d197dc267f9941cbbd3e3c6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564719"
---
# <a name="elimination-rules"></a><span data-ttu-id="6b0ec-103">削除ルール</span><span class="sxs-lookup"><span data-stu-id="6b0ec-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b0ec-104">このトピックでは、消去ルールと、消去に関するレポートのさまざまなオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="6b0ec-105">親法人が 1 つ以上の関連法人とビジネスを行い、連結財務報告を使用するときは、削除トランザクションが必要です。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="6b0ec-106">連結財務報告は、連結された組織とその組織の外部にある他のエンティティの間で発生するトランザクションのみを含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="6b0ec-107">したがって、同じ組織内の法人間のトランザクションは、財務諸表に表示されないように、一般会計から消去または削除される必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="6b0ec-108">削除について報告する方法は複数あります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="6b0ec-109">連結会社または削除会社で削除ルールを作成し、処理します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="6b0ec-110">財務報告を使用して、特定の行または列で、削除の勘定および分析コードを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="6b0ec-111">別の法人を使用して、手動トランザクション エントリを転記して削除を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="6b0ec-112">このトピックでは、連結または削除会社で処理する削除ルールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="6b0ec-113">削除の相手方法人として指定されている法人内で削除トランザクションを作成するための削除ルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="6b0ec-114">相手方法人は削除法人と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="6b0ec-115">連結プロセス中に、または削除仕訳帳提案を使用することによってのいずれかで、削除仕訳帳を生成できます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="6b0ec-116">削除ルールを設定する前に、次の用語をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="6b0ec-117">**ソース法人** – 削除される金額が転記された法人。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="6b0ec-118">**相手方法人** – 削除ルールが転記される法人。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="6b0ec-119">**削除の法人** – 削除の相手方の法人として指定される法人。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="6b0ec-120">**連結法人** – 法人グループの財務結果を報告するために作成された法人。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="6b0ec-121">グループ法人からの財務データはこの法人に連結され、連結されたデータを使用することによって財務レポートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="6b0ec-122">次の表に、削除する必要がある可能性のあるトランザクション タイプを示します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b0ec-123">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="6b0ec-123">Transaction type</span></span></th>
<th><span data-ttu-id="6b0ec-124">例</span><span class="sxs-lookup"><span data-stu-id="6b0ec-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b0ec-125">販売注文入力および請求 (集中処理)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="6b0ec-126">組織の別の法人に代わって顧客に製品を販売します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0ec-127">販売注文入力 (会社間/会社内) および請求</span><span class="sxs-lookup"><span data-stu-id="6b0ec-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="6b0ec-128">組織の法人間で製品を販売します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0ec-129">発注書 (集中処理)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="6b0ec-130">組織の別の法人に代わって仕入先から在庫品、供給品、サービス、固定資産、およびその他の製品を購入します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0ec-131">在庫管理 (会社間/会社内)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="6b0ec-132">組織の別の法人の固定資産に 1 つの法人の在庫を移動します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="6b0ec-133">組織の別の法人の在庫に 1 つの法人の在庫を移動します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0ec-134">輸送中在庫追跡</span><span class="sxs-lookup"><span data-stu-id="6b0ec-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="6b0ec-135">同じ、法人の異なる地理的な場所にある倉庫間で品目を移動します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0ec-136">買掛金勘定集中請求処理</span><span class="sxs-lookup"><span data-stu-id="6b0ec-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="6b0ec-137">組織の別の法人に代わって請求書を記録します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0ec-138">買掛金勘定集中支払処理</span><span class="sxs-lookup"><span data-stu-id="6b0ec-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="6b0ec-139">組織の別の法人に代わって請求書の支払いを行います。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0ec-140">現金管理および資金 (集中処理)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="6b0ec-141">税金の支払、税金の払戻、利子、ローン、前払、配当金支払、および前払ロイヤリティまたはコミッションを処理します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="6b0ec-142">組織の別の法人に代わって経費の支払いを行います。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="6b0ec-143">請求書は、相手先法人の帳簿に入力され、法人間で相互決済する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="6b0ec-144">たとえば、1 つの法人が別の法人の従業員の経費レポートの支払を行います。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="6b0ec-145">この場合、従業員の経費レポートには別の法人に関連する経費があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="6b0ec-146">1 つの法人から組織の別の法人に現金を移動します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0ec-147">売掛金勘定 (集中処理)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="6b0ec-148">別の法人の顧客請求書の現金を受け取り、その法人の銀行口座に小切手で預金します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0ec-149">給与 (集中処理、会社間/会社内)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="6b0ec-150">別の法人の給与を支払います。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="6b0ec-151">たとえば、ある法人が従業員に自社の給与を支払いながら、その給与対象期間中に従業員が別の法人のために行った作業を請求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="6b0ec-152">または、従業員は法人 A で半分働き、法人 B でも半分働いているが、福利厚生はすべての支払が対象になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="6b0ec-153">このような場合、従業員の支払には両方の法人からの支払が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="6b0ec-154">給与が転記されるだけでなく、給与に対する税金、福利厚生、控除、および見越計上も転記されます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="6b0ec-155">部門間または事業部間で労働力を移動します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0ec-156">固定資産 (会社間/会社内)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="6b0ec-157">別の法人の固定資産または在庫に固定資産を転送します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0ec-158">配賦 (会社間/会社内)</span><span class="sxs-lookup"><span data-stu-id="6b0ec-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="6b0ec-159">会社の配賦を処理します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-159">You process corporate allocations.</span></span> <span data-ttu-id="6b0ec-160">配賦は、生成元のモジュールには関係のない、配賦される勘定に対する活動です。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="6b0ec-161">例</span><span class="sxs-lookup"><span data-stu-id="6b0ec-161">Example</span></span>
<span data-ttu-id="6b0ec-162">自分の法人、法人 A は、組織内の別の法人、法人 B に製品を販売します。次の例では、2 つの法人の間で発生するトランザクションをどのように削除する必要があるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="6b0ec-163">法人 A は、コスト 10.00 の製品を法人 B に 10.00 で販売します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="6b0ec-164">法人 A は、コスト 10.00 の製品を法人 B に 10.00で販売し、さらに、実際の送料 2.00 をプラスします。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="6b0ec-165">法人 A は、コスト 10.00 の製品を法人 B に 15.00 で販売し、販売の利益幅を認識します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="6b0ec-166">法人 A は、コスト 10.00 の製品を法人 B に 15.00 で販売し、販売の利益幅の半分を認識します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="6b0ec-167">法人 B は、販売の利益幅の残りの半分を認識します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="6b0ec-168">したがって、収益は分割されます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="6b0ec-169">分割収益では、外部組織からの代わりに、組織の別の法人の注文にインセンティブが提供されます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="6b0ec-170">これらすべてのトランザクションで、貸し勘定および借り勘定に転記されている会社間のトランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="6b0ec-171">さらに、これらのトランザクションには、会社間の販売の量が販売された商品販売コストと等しくない場合に、値上げ金額および値下げ金額が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="6b0ec-172">削除ルールの設定</span><span class="sxs-lookup"><span data-stu-id="6b0ec-172">Set up elimination rules</span></span>
<span data-ttu-id="6b0ec-173">Microsoft Dynamics 365 for Finance and Operations で消去ルールを設定するとき、消去目的の財務分析コードを具体的に作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="6b0ec-174">ほとんどの顧客は、「取引相手」のような名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="6b0ec-175">財務分析コードを使用しない決定をする場合、会社間トランザクション固有の主勘定を作成してください。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="6b0ec-176">消去の設定は [連結] モジュールの [設定] 領域にあります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="6b0ec-177">ルールの説明を入力した後、消去仕訳帳が転記する会社を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="6b0ec-178">これは、法人の設定で**財務消去プロセスで使用**が選択された会社である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="6b0ec-179">消去ルールを有効にする日付と、期限切れの日付を必要に応じて設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="6b0ec-180">消去提案プロセスで使用できるようにする場合、**有効**を**はい**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="6b0ec-181">**消去**のタイプがある仕訳帳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="6b0ec-182">基本を定義した後、**明細行**をクリックして実際の処理ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="6b0ec-183">消去には、正味金額の変更の消去、または固定金額の定義の 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="6b0ec-184">ソースの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-184">Select your source account.</span></span> <span data-ttu-id="6b0ec-185">アスタリスク (\*) をワイルド カードとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="6b0ec-186">たとえば、1\* は配賦のデータのソースとして 1 から始まるすべての勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="6b0ec-187">ソースの勘定を選択すると、**勘定仕様**で使用される相手方の会社から勘定が決まります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="6b0ec-188">**ソース**の勘定で定義された同じ主勘定を使用する場合、**ソース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="6b0ec-189">**ユーザー定義**を選択する場合、相手方の勘定を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="6b0ec-190">分析コードの仕様は、同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="6b0ec-191">**ソース**を選択すると、ソースの会社として相手方の会社の同じ分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="6b0ec-192">**ユーザー定義**を選択すると、**相手方の分析コード**のメニュー項目をクリックして相手方の会社で分析コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="6b0ec-193">消去のソースとして使用されるソース分析コード、財務分析コード、値を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="6b0ec-194">削除トランザクションの処理</span><span class="sxs-lookup"><span data-stu-id="6b0ec-194">Process elimination transactions</span></span>
<span data-ttu-id="6b0ec-195">連結オンライン プロセス時、または消去仕訳帳の作成と消去提案プロセスの実行による消去トランザクションを処理する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="6b0ec-196">このセクションでは、仕訳帳の作成と消去プロセスの実行を中心とします。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="6b0ec-197">消去会社として定義されている会社の連結モジュールで**消去仕訳帳**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="6b0ec-198">仕訳帳名を選択したら、**明細行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="6b0ec-199">**提案**メニューを選択して**消去提案**を選択すると、提案を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="6b0ec-200">連結されたデータのソースである会社を選択してから、処理するルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="6b0ec-201">削除額の検索を開始する開始日と、削除額の検索を終了する終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="6b0ec-202">**GL転記日付**フィールドは、仕訳帳から総勘定元帳への転記に使用される日付です。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="6b0ec-203">**OK** をクリックすると、勘定の確認と仕訳帳の転記ができます。</span><span class="sxs-lookup"><span data-stu-id="6b0ec-203">After you click **OK**, you can review the amounts and post the journal.</span></span>



