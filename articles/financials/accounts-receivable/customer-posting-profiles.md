---
title: 顧客転記プロファイル
description: 顧客転記プロファイルは、顧客トランザクションから総勘定元帳への転記を制御します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 956dca24c2cfa7e22d718ff84b338bc4ba030394
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "322355"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="f7066-103">顧客転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="f7066-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7066-104">顧客転記プロファイルは、顧客トランザクションから総勘定元帳への転記を制御します。</span><span class="sxs-lookup"><span data-stu-id="f7066-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="f7066-105">顧客転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="f7066-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="f7066-106">顧客転記プロファイルでは、すべての顧客、顧客グループまたは単一の顧客に総勘定元帳勘定とドキュメント設定を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f7066-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="f7066-107">これらの設定は、販売注文、自由書式の請求書、現金による支払、督促状、利子計算書を作成するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="f7066-108">トランザクションに、このページでトランザクション用に設定された転記プロファイルとは異なる転記プロファイルを選択し、優先して使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7066-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="f7066-109">既定の転記プロファイルは、[売掛金勘定パラメーター] ページの [元帳] と [売上税] クイック タブで定義されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="f7066-110">既定の転記プロファイルは、必要に応じて別のプロファイルに変更できる新しいドキュメントのヘッダーに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="f7066-111">[トランザクションの転記の定義] ページでトランザクションの転記タイプと転記の定義を関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="f7066-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="f7066-112">転記の定義は、顧客トランザクションの総勘定元帳への転記を転記プロファイルの代わりに制御します。</span><span class="sxs-lookup"><span data-stu-id="f7066-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="f7066-113">転記プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="f7066-113">Creating a posting profile</span></span>
<span data-ttu-id="f7066-114">選択した転記プロファイルを使用するトランザクションを転記する際に使用される勘定科目を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7066-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="f7066-115">選択した転記プロファイルについて、アカウント コードおよび (可能な場合) アカウント番号またはグループ番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="f7066-116">転記プロセスでは、次の優先順位に従って特定のアカウント コード、アカウント番号、グループ番号の組み合わせを検索することにより、各トランザクションの最も適切な転記プロファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="f7066-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="f7066-117">**アカウント コード** フィールド値</span><span class="sxs-lookup"><span data-stu-id="f7066-117">**Account code** field value</span></span> | <span data-ttu-id="f7066-118">**アカウント/グループ番号**フィールド値</span><span class="sxs-lookup"><span data-stu-id="f7066-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="f7066-119">検索の優先順位</span><span class="sxs-lookup"><span data-stu-id="f7066-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="f7066-120">**テーブル**</span><span class="sxs-lookup"><span data-stu-id="f7066-120">**Table**</span></span>                    | <span data-ttu-id="f7066-121">特定の顧客 ID</span><span class="sxs-lookup"><span data-stu-id="f7066-121">Specific customer account</span></span>                       | <span data-ttu-id="f7066-122">1</span><span class="sxs-lookup"><span data-stu-id="f7066-122">1</span></span>               |
| <span data-ttu-id="f7066-123">**グループ**</span><span class="sxs-lookup"><span data-stu-id="f7066-123">**Group**</span></span>                    | <span data-ttu-id="f7066-124">顧客に割り当てられた顧客グループ</span><span class="sxs-lookup"><span data-stu-id="f7066-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="f7066-125">2</span><span class="sxs-lookup"><span data-stu-id="f7066-125">2</span></span>               |
| <span data-ttu-id="f7066-126">**すべて**</span><span class="sxs-lookup"><span data-stu-id="f7066-126">**All**</span></span>                      | <span data-ttu-id="f7066-127">空白</span><span class="sxs-lookup"><span data-stu-id="f7066-127">Blank</span></span>                                           | <span data-ttu-id="f7066-128">3</span><span class="sxs-lookup"><span data-stu-id="f7066-128">3</span></span>               |

<span data-ttu-id="f7066-129">すべての顧客トランザクションに同じ転記プロファイルを割り当てる場合は、[アカウント コード] フィールドを [すべて] に設定して、単一の転記プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7066-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="f7066-130">転記プロファイルを設定するには、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7066-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f7066-131">フィールド</span><span class="sxs-lookup"><span data-stu-id="f7066-131">Field</span></span></th>
<th><span data-ttu-id="f7066-132">説明</span><span class="sxs-lookup"><span data-stu-id="f7066-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7066-133"><strong>転記プロファイル</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="f7066-134">転記プロファイルのコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f7066-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="f7066-135">たとえば、転記プロファイルを 2 つ作成して、国内通貨で表した顧客残高と外国通貨で表した顧客残高の勘定を 1 つずつ取得できます。</span><span class="sxs-lookup"><span data-stu-id="f7066-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="f7066-136">一方の勘定には「国内」、もう一方の勘定には「外国」という名前を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7066-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7066-137"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="f7066-138">転記プロファイルの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7066-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="f7066-139">転記プロファイルをこのページで表示する場合に、よりよく識別するためにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7066-140"><strong>アカウント コード</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="f7066-141">転記プロファイルを単一の顧客に適用するか、複数の顧客に適用するか、またはすべての顧客に適用するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7066-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="f7066-142"><strong>テーブル</strong> – 単一の顧客に転記ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="f7066-143">[アカウント/グループ番号] フィールドで顧客 ID を選択してください。</span><span class="sxs-lookup"><span data-stu-id="f7066-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="f7066-144"><strong>グループ</strong> – 顧客グループに転記ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="f7066-145">[アカウント/グループ番号] フィールドで顧客グループを選択してください。</span><span class="sxs-lookup"><span data-stu-id="f7066-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="f7066-146"><strong>全て</strong> – 全ての顧客に転記ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="f7066-147">[アカウント/グループ番号] フィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="f7066-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7066-148"><strong>アカウント/グループ番号</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="f7066-149">[アカウント コード] フィールドで [テーブル] を選択した場合は、転記プロファイルに関連付けられた顧客の ID 番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="f7066-150">[グループ] を選択した場合は、顧客グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="f7066-151">[すべて] を選択した場合、このフィールドには何も入力しません。</span><span class="sxs-lookup"><span data-stu-id="f7066-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7066-152"><strong>集計勘定</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="f7066-153">転記プロファイルに関連付けられている顧客の集計勘定として使用する勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7066-154"><strong>決済勘定</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="f7066-155">キャッシュ フロー予測に使用する流動性勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="f7066-156">このフィールドは、キャッシュ フロー予測が有効になっている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7066-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7066-157"><strong>売上税の前払</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="f7066-158">前払で受領する売上税の勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="注記" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="f7066-160"><strong>注記</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7066-161">支払が前払としてマークされている場合に使用する転記プロファイルを指定する場合、[売掛金勘定パラメーター] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7066-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7066-162"><strong>割引勘定負債</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="f7066-163">割引負債の勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7066-164"><strong>督促状順序</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="f7066-165">転記プロファイルが割り当てられている顧客に使用する督促状順序の ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7066-166"><strong>利息コード</strong></span><span class="sxs-lookup"><span data-stu-id="f7066-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="f7066-167">転記プロファイルが割り当てられている顧客の利息の計算に使用する利息コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="f7066-168">**テーブルの制限**</span><span class="sxs-lookup"><span data-stu-id="f7066-168">**Table restrictions**</span></span>

<span data-ttu-id="f7066-169">選択した転記プロファイルを持つトランザクションで、トランザクションが自動的に決済するかどうか、利息が計算されるかどうか、督促状が発行されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7066-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="f7066-170">選択した転記プロファイルを持つトランザクションの決済されると、使用する勘定も選択できます。</span><span class="sxs-lookup"><span data-stu-id="f7066-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="f7066-171">転記プロファイルを設定するには、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7066-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="f7066-172">フィールド</span><span class="sxs-lookup"><span data-stu-id="f7066-172">Field</span></span>                 | <span data-ttu-id="f7066-173">説明</span><span class="sxs-lookup"><span data-stu-id="f7066-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7066-174">**決済**</span><span class="sxs-lookup"><span data-stu-id="f7066-174">**Settlement**</span></span>        | <span data-ttu-id="f7066-175">この転記プロファイルを持つトランザクションの自動決済を有効にする場合は、この切り替えを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="f7066-176">この切り替えがオフの場合、[未処理トランザクションの決済] ページまたは [顧客支払の入力] ページを使用してトランザクションを手動で決済する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7066-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="f7066-177">**関心事項**</span><span class="sxs-lookup"><span data-stu-id="f7066-177">**Interest**</span></span>          | <span data-ttu-id="f7066-178">このプロファイルを使用する顧客の未払残高の利息を計算するには、この切り替えを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="f7066-179">この切り替えをオフにした場合、この顧客の利息は計算されません。</span><span class="sxs-lookup"><span data-stu-id="f7066-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="f7066-180">**督促状**</span><span class="sxs-lookup"><span data-stu-id="f7066-180">**Collection letter**</span></span> | <span data-ttu-id="f7066-181">このプロファイルを使用する顧客の督促状を生成するには、この切り替えを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="f7066-182">この切り替えをオフにした場合、この顧客の督促状は生成されません。</span><span class="sxs-lookup"><span data-stu-id="f7066-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="f7066-183">**閉じる**</span><span class="sxs-lookup"><span data-stu-id="f7066-183">**Close**</span></span>             | <span data-ttu-id="f7066-184">この転記プロファイルを設定したトランザクションを締めるときに切り替える転記プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7066-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="f7066-185">トランザクションは、完全に決済されるとクローズ済と見なされます。</span><span class="sxs-lookup"><span data-stu-id="f7066-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="f7066-186">詳細については、「[顧客支払の概要](../cash-bank-management/tasks/customer-payment-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7066-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

