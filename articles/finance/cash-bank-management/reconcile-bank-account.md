---
title: 銀行口座の調整
description: このトピックでは、銀行口座を調整する方法について説明します。
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1abc86aa5c3863eba34f726b543792408a542383
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976369"
---
# <a name="reconcile-a-bank-account"></a><span data-ttu-id="29537-103">銀行口座の調整</span><span class="sxs-lookup"><span data-stu-id="29537-103">Reconcile a bank account</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29537-104">口座取引明細書を受け取ったら、口座取引明細書の取引と法人の銀行取引を定期的に調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29537-104">When you receive a bank statement, you should periodically reconcile legal entity bank transactions with the transactions on the bank statement.</span></span>

<span data-ttu-id="29537-105">明細書に記載されている小切手または預金伝票のいずれかの支払いの状態が現在 **保留中** の場合、銀行明細書は銀行口座で調整できません。</span><span class="sxs-lookup"><span data-stu-id="29537-105">You cannot reconcile a bank statement with a bank account if any of the checks or deposit slip payments that are listed on the statement currently have a status of **Pending cancellation**.</span></span> <span data-ttu-id="29537-106">レビュー担当者が小切手の取消または預金伝票の支払キャンセルを転記または拒否した後、ステータスは **取消の保留中** ではなくなり、銀行口座を照合できます。</span><span class="sxs-lookup"><span data-stu-id="29537-106">After a reviewer posts or rejects a check reversal or deposit slip payment cancellation, the status is no longer **Pending cancellation**, and you can reconcile the bank account.</span></span>

1.  <span data-ttu-id="29537-107">**現金および銀行管理** \> **銀行口座** \> **銀行口座** に移動します。</span><span class="sxs-lookup"><span data-stu-id="29537-107">Go to **Cash and bank management** \> **Bank Accounts** \> **Bank accounts**.</span></span> <span data-ttu-id="29537-108">口座取引明細書と調整する銀行口座を選択し、**調整** > **口座調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29537-108">Select the bank account to reconcile with the bank statement and select **Reconcile** > **Account reconciliation**.</span></span>

2.  <span data-ttu-id="29537-109">**口座取引明細書日付** と **口座取引明細書** フィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="29537-109">Enter information in the **Bank statement date** and **Bank statement** fields.</span></span> <span data-ttu-id="29537-110">**期末残高** フィールドには、口座取引明細書に表示される銀行口座の残高を入力できます。</span><span class="sxs-lookup"><span data-stu-id="29537-110">In the **Ending balance** field, you can enter the balance of the bank account as it appears on the bank statement.</span></span>

3.  <span data-ttu-id="29537-111">**トランザクション** を選択して、**口座調整** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="29537-111">Select **Transactions** to open the **Account reconciliation** page.</span></span>

4.  <span data-ttu-id="29537-112">口座取引明細書に含まれる取引ごとに、Dynamics 365 Finance の金額が口座取引明細書の金額に対応する場合、**精算済** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="29537-112">For each transaction that is included on the bank statement, select the **Cleared** check box if the amount in Dynamics 365 Finance corresponds to the amount on the bank statement.</span></span> <span data-ttu-id="29537-113">**銀行トランザクション タイプ** フィールドでは値の入力や変更もできます。</span><span class="sxs-lookup"><span data-stu-id="29537-113">You can also enter or modify the value in the **Bank transaction type** field.</span></span> <span data-ttu-id="29537-114">このフィールドの値は、銀行取引統計や一部のレポートで重要な情報です。</span><span class="sxs-lookup"><span data-stu-id="29537-114">This field value is important for bank transaction statistics and for some reports.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="29537-115">口座取引明細書にない取引については、<STRONG>精算済</STRONG>チェック ボックスを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="29537-115">Do not select the <STRONG>Cleared</STRONG> check box for transactions that are not on the bank statement.</span></span> <span data-ttu-id="29537-116">これらの取引は、後日、口座取引明細書と調整するまでこのページに表示され続けます。</span><span class="sxs-lookup"><span data-stu-id="29537-116">These transactions will continue to be displayed in on this page until they are reconciled with a future bank statement.</span></span></P>
    > <P><span data-ttu-id="29537-117">トランザクションのステータスが<STRONG>取消の保留中</STRONG>の場合、<STRONG>精算済</STRONG>チェック ボックスは使用できません。</span><span class="sxs-lookup"><span data-stu-id="29537-117">The <STRONG>Cleared</STRONG> check box is not available if the transaction has a status of <STRONG>Pending cancellation</STRONG>.</span></span> <span data-ttu-id="29537-118">転記の前、取り消しまたはキャンセルがレビューに送信されているように Finance で設定されている場合、取引はこの状態になっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="29537-118">Transactions might have this status if Finance is set up to require that reversals or cancellations be sent to review before they are posted.</span></span> <span data-ttu-id="29537-119">レビュー担当者が取消またはキャンセルの転記や拒否をした後、状態は<STRONG>取消の保留中</STRONG>ではなくなり、銀行口座を口座取引明細書と調整できます。</span><span class="sxs-lookup"><span data-stu-id="29537-119">After a reviewer posts or rejects the reversal or cancellation, the status is no longer <STRONG>Pending cancellation</STRONG>, and you can reconcile the bank account with the bank statement.</span></span></P>

    
    <span data-ttu-id="29537-120">口座取引明細書にすべてが表示されるチェックの間隔に対して **精算済** チェックボックスを選択するには、**小切手の期間にマーク** を選択し、間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="29537-120">To select the **Cleared** check box for an interval of checks that all are displayed on the bank statement, select **Mark check interval**, and then indicate the interval.</span></span>

5.  <span data-ttu-id="29537-121">銀行口座トランザクションの金額が口座取引明細書のトランザクションの金額と一致しない場合は、**訂正金額** フィールドに修正金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="29537-121">If the amount for a bank account transaction does not correspond to the amount for the transaction on the bank statement, enter the amount of the correction in the **Correction amount** field.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="29537-122">修正するトランザクションの会計年度期間が終了している場合、<STRONG>訂正金額</STRONG>フィールドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="29537-122">If the fiscal period of the transaction to be corrected is closed, the <STRONG>Correction amount</STRONG> field cannot be used.</span></span> <span data-ttu-id="29537-123">代わりに、訂正用のオープン会計期間内の取引日を指定した明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="29537-123">Instead, create a line that has a transaction date that is in an open fiscal period for the correction.</span></span> <span data-ttu-id="29537-124">この場合、元のトランザクションで使用した財務分析コードと、相手方主勘定を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29537-124">In this case, you must add the financial dimensions that were used on the original transaction, and also the offset main account.</span></span></P>



6.  <span data-ttu-id="29537-125">口座取引明細書には記載されていても Finance には記録されていない手数料や利息などの、エントリの取引を作成します。</span><span class="sxs-lookup"><span data-stu-id="29537-125">Create transactions for entries, such as fees and interest, that are on the bank statement but that are not recorded in Finance.</span></span> <span data-ttu-id="29537-126">**銀行トランザクション タイプ** と適切な財務分析コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="29537-126">Enter the **Bank transaction type** and appropriate financial dimensions.</span></span>

7.  <span data-ttu-id="29537-127">口座取引明細書のトランザクションは **精算済** としてマークされているため、変更するたびに再計算される **未調整** フィールドの金額がゼロに近づいていきます。</span><span class="sxs-lookup"><span data-stu-id="29537-127">As the transactions on the bank statement are marked as **Cleared**, the amount in the **Unreconciled** field, which is recalculated continuously as you make changes, approaches zero.</span></span> <span data-ttu-id="29537-128">金額がゼロになったら、**口座を調整** を選択して、調整、および作成したトランザクションと訂正を転記します。</span><span class="sxs-lookup"><span data-stu-id="29537-128">When it reaches zero, select **Reconcile account** to post the reconciliation, and the transactions and corrections that you have created.</span></span>
    
    <span data-ttu-id="29537-129">調整を転記すると、関連の取引は変更や訂正ができなくなり、それ以降の口座調整には表示されません。</span><span class="sxs-lookup"><span data-stu-id="29537-129">After the reconciliation is posted, the transactions that have been included cannot be modified or corrected, and they are not displayed for future account reconciliation.</span></span>

8.  <span data-ttu-id="29537-130">未調整の銀行トランザクションを表示するには、**未調整銀行トランザクション** レポートを使用します。</span><span class="sxs-lookup"><span data-stu-id="29537-130">To view bank transactions that have not yet been reconciled, use the **Unreconciled bank transactions** report.</span></span> <span data-ttu-id="29537-131">銀行口座の口座取引明細書を表示するには、**口座取引明細書** レポートを使用します。</span><span class="sxs-lookup"><span data-stu-id="29537-131">To view the bank statement for a bank account, use the **Bank statement** report.</span></span>

## <a name="cancel-bank-statement-reconciliation"></a><span data-ttu-id="29537-132">口座取引明細書調整のキャンセル</span><span class="sxs-lookup"><span data-stu-id="29537-132">Cancel bank statement reconciliation</span></span> 

<span data-ttu-id="29537-133">口座取引明細書調整のキャンセル機能を使用すると、口座取引明細書調整をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="29537-133">The Cancel bank statement reconciliation functionality enables you to cancel bank statement reconciliation.</span></span> <span data-ttu-id="29537-134">この機能を使用するには、**機能管理** ワークスペースで **口座取引明細書調整のキャンセル** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="29537-134">To use this feature, enable the **Cancel bank statement reconciliation** feature in the **Feature management** workspace.</span></span> <span data-ttu-id="29537-135">また、**口座取引明細書の編集を許可** パラメーターを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="29537-135">You also need to enable the **Allow bank statement edit** parameter.</span></span> <span data-ttu-id="29537-136">これを行うには、**現金および銀行管理 > 設定 > 現金および銀行管理パラメーター > 口座調整** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="29537-136">To do this, go to **Cash and bank management > Setup > Cash and bank management parameters > Bank reconciliation**.</span></span>
 
<span data-ttu-id="29537-137">口座取引明細書の調整は、入力された時系列でのみキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="29537-137">Bank statement reconciliations can only be canceled in the chronological order in which they were entered.</span></span> <span data-ttu-id="29537-138">口座取引明細書の調整がキャンセルされると、新しいトランザクションと修正が取り消され、他のすべてのトランザクションは未調整としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="29537-138">When a bank statement reconciliation is canceled, new transactions and corrections will be reversed and all other transactions will be marked as un-reconciled.</span></span>
 
<span data-ttu-id="29537-139">口座取引明細書の調整をキャンセルするには、口座取引明細書を選択し、**口座取引明細書 > 口座調整をキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29537-139">To cancel bank statement reconciliation, select the bank statement and select **Bank statement > Cancel bank reconciliation**.</span></span> <span data-ttu-id="29537-140">**口座調整をキャンセル** ページで、**理由コード**、**理由コメント**、および **取消日** を入力します。</span><span class="sxs-lookup"><span data-stu-id="29537-140">On the **Cancel bank reconciliation** page, provide the **Reason code**, **Reason comment**, and **Cancellation date**.</span></span> <span data-ttu-id="29537-141">**OK** を選択してキャンセルを開始します。</span><span class="sxs-lookup"><span data-stu-id="29537-141">Select **OK** to begin cancellation.</span></span> <span data-ttu-id="29537-142">なお、口座取引明細書の取消日は、口座取引明細書の日付以降である必要があります。</span><span class="sxs-lookup"><span data-stu-id="29537-142">Note, the bank statement cancellation date must be on or after the bank statement date.</span></span> <span data-ttu-id="29537-143">口座取引明細書の調整がキャンセルされた後、口座取引明細書の **取消日** フィールドは、指定された **取消日** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="29537-143">After the bank statement reconciliation has canceled, the **Cancellation date** field for the bank statement will be updated with the **Cancellation date** provided.</span></span> <span data-ttu-id="29537-144">**トランザクション** ボタンを選択して、調整がキャンセルされたトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="29537-144">Select the **Transactions** button to view the transactions for which the reconciliation was canceled.</span></span>
