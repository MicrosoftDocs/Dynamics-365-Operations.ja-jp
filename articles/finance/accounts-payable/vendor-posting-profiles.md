---
title: 仕入先転記プロファイル
description: 仕入先転記プロファイルは、仕入先トランザクションの総勘定元帳への転記を制御します。
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37fb7d2623451313475a6c234e820c7c6295be40
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835487"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="181f7-103">仕入先転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="181f7-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="181f7-104">仕入先転記プロファイルは、仕入先トランザクションの総勘定元帳への転記を制御します。</span><span class="sxs-lookup"><span data-stu-id="181f7-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="181f7-105">仕入先転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="181f7-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="181f7-106">仕入先転記プロファイルでは、すべての仕入先、仕入先グループ、または単一の仕入先に総勘定元帳勘定とドキュメント設定を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="181f7-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="181f7-107">これらの設定は、発注書、仕入先請求書、および現金による支払を作成するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="181f7-108">トランザクションに、このページ上でトランザクション用に設定された転記プロファイルとは異なる転記プロファイルを選択し、優先して使用できます。</span><span class="sxs-lookup"><span data-stu-id="181f7-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="181f7-109">既定の転記プロファイルは、**買掛金勘定パラメーター** ページの **元帳と売上税** クイック タブで定義されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="181f7-110">既定の転記プロファイルは、必要に応じて、別のプロファイルに変更できる新しいドキュメントのヘッダーに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="181f7-111">**トランザクションの転記の定義** ページ上でトランザクションの転記タイプと転記の定義を関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="181f7-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="181f7-112">転記の定義は、仕入先トランザクションの総勘定元帳への転記を転記プロファイルの代わりに制御します。</span><span class="sxs-lookup"><span data-stu-id="181f7-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="181f7-113">転記プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="181f7-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="181f7-114">**設定**</span><span class="sxs-lookup"><span data-stu-id="181f7-114">**Setup**</span></span>

<span data-ttu-id="181f7-115">選択した転記プロファイルを使用するトランザクションを転記する際に使用される勘定科目を指定します。</span><span class="sxs-lookup"><span data-stu-id="181f7-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="181f7-116">選択した転記プロファイルについて、アカウント コードおよび (可能な場合) アカウント番号またはグループ番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="181f7-117">転記プロセスでは、次の優先順位に従って特定のアカウント コード、アカウント番号、グループ番号の組み合わせを検索することにより、各トランザクションの最も適切な転記プロファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="181f7-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="181f7-118">**アカウント コード** フィールド値</span><span class="sxs-lookup"><span data-stu-id="181f7-118">**Account code** field value</span></span> | <span data-ttu-id="181f7-119">**アカウント/グループ番号** フィールド値</span><span class="sxs-lookup"><span data-stu-id="181f7-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="181f7-120">検索の優先順位</span><span class="sxs-lookup"><span data-stu-id="181f7-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="181f7-121">**テーブル**</span><span class="sxs-lookup"><span data-stu-id="181f7-121">**Table**</span></span>                    | <span data-ttu-id="181f7-122">特定の仕入先</span><span class="sxs-lookup"><span data-stu-id="181f7-122">Specific vendor account</span></span>                     | <span data-ttu-id="181f7-123">1</span><span class="sxs-lookup"><span data-stu-id="181f7-123">1</span></span>               |
| <span data-ttu-id="181f7-124">**グループ化**</span><span class="sxs-lookup"><span data-stu-id="181f7-124">**Group**</span></span>                    | <span data-ttu-id="181f7-125">仕入先に割り当てられている仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="181f7-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="181f7-126">2</span><span class="sxs-lookup"><span data-stu-id="181f7-126">2</span></span>               |
| <span data-ttu-id="181f7-127">**すべて**</span><span class="sxs-lookup"><span data-stu-id="181f7-127">**All**</span></span>                      | <span data-ttu-id="181f7-128">空白</span><span class="sxs-lookup"><span data-stu-id="181f7-128">Blank</span></span>                                       | <span data-ttu-id="181f7-129">3</span><span class="sxs-lookup"><span data-stu-id="181f7-129">3</span></span>               |

<span data-ttu-id="181f7-130">すべての仕入先トランザクションに同じ転記プロファイルを割り当てる場合は、**アカウント コード** フィールドを **すべて** に設定して、単一の転記プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="181f7-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="181f7-131">転記プロファイルを設定するには、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="181f7-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="181f7-132">フィールド</span><span class="sxs-lookup"><span data-stu-id="181f7-132">Field</span></span></th>
<th><span data-ttu-id="181f7-133">説明</span><span class="sxs-lookup"><span data-stu-id="181f7-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="181f7-134"><strong>転記プロファイル</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="181f7-135">転記プロファイルのコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="181f7-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="181f7-136">たとえば、転記プロファイルを 2 つ作成して、国内通貨で表した仕入先残高と外国通貨で表した仕入先残高の勘定を 1 つずつ取得できます。</span><span class="sxs-lookup"><span data-stu-id="181f7-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="181f7-137">一方の勘定には「国内」、もう一方の勘定には「外国」という名前を設定できます。</span><span class="sxs-lookup"><span data-stu-id="181f7-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="181f7-138"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="181f7-139">転記プロファイルの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="181f7-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="181f7-140"><strong>アカウント コード</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="181f7-141">転記プロファイルの適用先を、特定の仕入先、仕入先グループ、またはすべての仕入先のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="181f7-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="181f7-142"><strong>テーブル</strong> – 単一の仕入先に転記ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="181f7-143"><strong>アカウント/グループ番号</strong>フィールドで仕入先 ID を選択してください。</span><span class="sxs-lookup"><span data-stu-id="181f7-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="181f7-144"><strong>グループ</strong> – 仕入先グループに転記ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="181f7-145"><strong>アカウント/グループ番号</strong>フィールドで仕入先グループを選択してください。</span><span class="sxs-lookup"><span data-stu-id="181f7-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="181f7-146"><strong>すべて</strong> – すべての仕入先に転記ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="181f7-147"><strong>アカウント/グループ番号</strong>フィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="181f7-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="181f7-148"><strong>アカウント/グループ番号</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="181f7-149"><strong>アカウント コード</strong> フィールドで<strong>テーブル</strong>を選択した場合は、転記プロファイルに関連付けられた仕入先の ID 番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="181f7-150"><strong>グループ</strong>が選択されている場合、仕入先グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="181f7-151"><strong>すべて</strong>を選択した場合、このフィールドには何も入力しません。</span><span class="sxs-lookup"><span data-stu-id="181f7-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="181f7-152"><strong>集計勘定</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="181f7-153">転記プロファイルが関連付けられている仕入先の集計勘定として使用する勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="181f7-154">この主勘定に対する<strong>手動入力を許可しない</strong>パラメーターはマークされます。</span><span class="sxs-lookup"><span data-stu-id="181f7-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="181f7-155">その後、転記プロファイルからこの勘定を削除する場合、<strong>主勘定</strong>ページの<strong>手動入力を許可しない</strong>の設定を検証します。</span><span class="sxs-lookup"><span data-stu-id="181f7-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="181f7-156"><strong>メモ:</strong> <strong>転記の定義の使用</strong>オプションが<strong>総勘定元帳のパラメーター</strong> ページで選択されている場合、仕入先請求書のトランザクションの転記の定義が集計勘定の代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="181f7-157"><strong>決済勘定</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="181f7-158">キャッシュ フロー予測に使用する流動性勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="181f7-159">このフィールドは、キャッシュ フロー予測が有効な場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="181f7-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="181f7-160"><strong>売上税の前払</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="181f7-161">前払で受領する売上税支払を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="181f7-162"><strong>メモ:</strong> <strong>買掛金管理パラメーター</strong> ページの<strong>元帳と売上税</strong>領域の<strong>前払仕訳伝票</strong>フィールドを持つ<strong>転記</strong>プロファイルで、前払としてマークされた支払が選択されている場合に使用される転記プロファイル。</span><span class="sxs-lookup"><span data-stu-id="181f7-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="181f7-163"><strong>着荷</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="181f7-164">未承認の仕入先請求書に関する情報が転記される勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="181f7-165">この情報は仕入帳仕訳帳に入力されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="181f7-166">たとえば、仕入先請求書を仕入帳に記入する際には、仕入先請求書に関するごく基本的な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="181f7-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="181f7-167">仕入帳が転記されると、ここで入力する勘定と<strong>相手勘定</strong>フィールドに入力される勘定にトランザクションが転記されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="181f7-168">請求書が承認されると、着荷勘定から仕入先の集計勘定に債務が転送されます。</span><span class="sxs-lookup"><span data-stu-id="181f7-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="181f7-169"><strong>相手勘定</strong></span><span class="sxs-lookup"><span data-stu-id="181f7-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="181f7-170">仕入帳を使用して更新された未承認の仕入先請求書を相殺するために使用する勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="181f7-171">相手勘定は、着荷勘定に転記されたトランザクションの相手勘定として機能します。</span><span class="sxs-lookup"><span data-stu-id="181f7-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="181f7-172">したがって、まだ承認されていない仕入先の購買が勘定に含まれます。</span><span class="sxs-lookup"><span data-stu-id="181f7-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="181f7-173">**テーブルの制限**</span><span class="sxs-lookup"><span data-stu-id="181f7-173">**Table restrictions**</span></span>

<span data-ttu-id="181f7-174">選択した転記プロファイルを持つトランザクションで、トランザクションが自動的に決済するかどうか、利息が計算されるかどうか、督促状が発行されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="181f7-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="181f7-175">選択した転記プロファイルを持つトランザクションの決済されると、使用する勘定も選択できます。</span><span class="sxs-lookup"><span data-stu-id="181f7-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="181f7-176">次の値を指定し、転記プロファイルを設定します</span><span class="sxs-lookup"><span data-stu-id="181f7-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="181f7-177">フィールド</span><span class="sxs-lookup"><span data-stu-id="181f7-177">Field</span></span>          | <span data-ttu-id="181f7-178">説明</span><span class="sxs-lookup"><span data-stu-id="181f7-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="181f7-179">**決算**</span><span class="sxs-lookup"><span data-stu-id="181f7-179">**Settlement**</span></span> | <span data-ttu-id="181f7-180">この転記プロファイルを持つトランザクションの自動決済を有効にする場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="181f7-181">このオプションがオフの場合、**未処理トランザクションの決済** ページを使用してトランザクションを手動で決済する必要があります。</span><span class="sxs-lookup"><span data-stu-id="181f7-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="181f7-182">**キャンセル**</span><span class="sxs-lookup"><span data-stu-id="181f7-182">**Cancel**</span></span>     | <span data-ttu-id="181f7-183">この転記プロファイルを持つトランザクションのキャンセルを可能にするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="181f7-184">**閉じる**</span><span class="sxs-lookup"><span data-stu-id="181f7-184">**Close**</span></span>      | <span data-ttu-id="181f7-185">この転記プロファイルを設定したトランザクションを締めるときに切り替える転記プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="181f7-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="181f7-186">トランザクションは、完全に決済されるとクローズ済と見なされます。</span><span class="sxs-lookup"><span data-stu-id="181f7-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]