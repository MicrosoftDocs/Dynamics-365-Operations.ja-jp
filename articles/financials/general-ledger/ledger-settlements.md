---
title: 元帳決済
description: このトピックでは、元帳決済 ページを使用して元帳トランザクションを決済する、および決済を取り消す方法について説明します。
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b02a1a066913c9959e9a55e78789e5ff1a175c56
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554693"
---
# <a name="ledger-settlements"></a><span data-ttu-id="bfd47-103">元帳決済</span><span class="sxs-lookup"><span data-stu-id="bfd47-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfd47-104">元帳決済では、一般会計の借方および貸方トランザクションを照合し、決済済としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="bfd47-105">この方法で、関連するトランザクションがクリアされていることを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="bfd47-106">誤って行われた決済を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="bfd47-107">詳細な元帳決済の有効化</span><span class="sxs-lookup"><span data-stu-id="bfd47-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="bfd47-108">詳細な元帳決済ページでは、トランザクションをフィルター処理および選択するための追加機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="bfd47-109">詳細な元帳決済ページを有効にするには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="bfd47-110">**一般会計** \> **元帳の設定** \> **一般会計パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="bfd47-111">**元帳決済**タブで、**詳細な元帳決済**オプションを**はい**に設定して、詳細な元帳決済機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bfd47-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="bfd47-112">**定期処理のタスク**で**元帳決済**を選択すると、詳細な**元帳決済**ページが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="bfd47-113">各勘定科目表の元帳決済に使用する勘定の一覧を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfd47-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="bfd47-114">このリストは、**元帳決済**ページに表示されるトランザクションの一覧をフィルターするために使用します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="bfd47-115">**勘定科目表**の一覧で、勘定科目表を選択し、**新規**を選択して一覧に新しい勘定を追加します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="bfd47-116">詳細な元帳決済のページを使用してトランザクションを決済する</span><span class="sxs-lookup"><span data-stu-id="bfd47-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="bfd47-117">元帳トランザクションを決済するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bfd47-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="bfd47-118">**一般会計** \> **定期処理のタスク** \> **元帳決済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="bfd47-119">ページの上部にあるフィルターを設定します:</span><span class="sxs-lookup"><span data-stu-id="bfd47-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="bfd47-120">日付範囲を選択、または**日付範囲コード**を日付範囲に自動的に入力するように選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="bfd47-121">必要に応じて転記階層を変更します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="bfd47-122">勘定科目および分析コードを個別に表示するためには、財務分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="bfd47-123">**トランザクションを表示**を選択すると、設定したフィルターと一致するすべてのトランザクションと、前のセクションで勘定科目表の設定時に指定した勘定の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="bfd47-124">フィルターまたは分析コード セットのいずれかを変更する場合は、**トランザクションを表示**を再度選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfd47-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="bfd47-125">決済用に検討している 1 つまたは複数の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="bfd47-126">ページの上部にある**選択済金額**フィールドの値は、選択した明細行の合計金額によって増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="bfd47-127">トランザクションの選択が完了したら、**選択済のマーク**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="bfd47-128">選択した各トランザクションの**マーク済**列にチェック マークが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="bfd47-129">また、グリッドの上にある**マークされた金額**フィールドの値は、マークした明細行の合計金額によって増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="bfd47-130">**マークされた金額**の値が **0** (ゼロ) の場合は、**マークされたトランザクションの決済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="bfd47-131">マークされたトランザクションのステータスは**決済済**に更新されます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="bfd47-132">トランザクションを見つけやすくする</span><span class="sxs-lookup"><span data-stu-id="bfd47-132">Make transactions easier to find</span></span>

<span data-ttu-id="bfd47-133">**元帳決済**ページには、決済に必要なトランザクションを表示しやすくする機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bfd47-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="bfd47-134">**選択項目のマークを解除する**ボタンは選択されているすべての明細行の**マーク済**フィールドをクリアします。</span><span class="sxs-lookup"><span data-stu-id="bfd47-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="bfd47-135">**マーク済**フィルターを使用すると、**マーク済**フィールドが選択されているか、またはクリアされているかに基づいてトランザクションをフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="bfd47-136">**ステータス**フィルターを使用すると、ステータスが**決済済**か、または**未決済**かに基づいてトランザクションをフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="bfd47-137">**絶対金額で並べ替え**ボタンを使用すると、金額を絶対値で並べ替えることができ、同じ金額の借方と貸方をグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="bfd47-138">決済を取り消す</span><span class="sxs-lookup"><span data-stu-id="bfd47-138">Reverse a settlement</span></span>

<span data-ttu-id="bfd47-139">誤って行われた決済を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="bfd47-140">「詳細な元帳決済のページを使用してトランザクションを決済する」のセクションの手順 1 から 3 に従って、探しているトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="bfd47-141">**ステータス**フィルターで**決済済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="bfd47-142">取消を検討している 1 つまたは複数の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="bfd47-143">ページの上部にある**選択済金額**フィールドの値は、選択した明細行の合計金額によって増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="bfd47-144">トランザクションの選択が完了したら、**選択済のマーク**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="bfd47-145">選択した各トランザクションの**マーク済**列にチェック マークが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="bfd47-146">また、ページの上部にある**マークされた金額**フィールドの値は、マークした明細行の合計金額によって増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="bfd47-147">**マークされた金額**の値が **0** (ゼロ) の場合は、**マークされたトランザクションの取消**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="bfd47-148">マークされたトランザクションのステータスは**未決済**に更新されます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="bfd47-149">トランザクションの一覧に含まれる勘定の一覧を更新します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="bfd47-150">**元帳決済勘定**を選択して、トランザクションの一覧に含まれる勘定を編集するダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="bfd47-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="bfd47-151">**新規**をクリックして、新しい勘定を一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="bfd47-152">このリストは、**元帳決済**ページに表示されるトランザクションの一覧をフィルターするために使用します。</span><span class="sxs-lookup"><span data-stu-id="bfd47-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>
