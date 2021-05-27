---
title: 年度末決算に期首残高が表示されない
description: このトピックでは、年度末決算時に期首残高が欠落している理由と、欠落している場合に、その残高を再構築する方法について説明します。
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028573"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="13c30-103">年度末決算に期首残高が表示されない</span><span class="sxs-lookup"><span data-stu-id="13c30-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13c30-104">このトピックでは、年度末決算時に期首残高が欠落している理由と、欠落している場合に、その残高を再構築する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13c30-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="13c30-105">現象</span><span class="sxs-lookup"><span data-stu-id="13c30-105">Symptom</span></span>

<span data-ttu-id="13c30-106">一般会計の年度末決算を実行した後で、期首残高がないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="13c30-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="13c30-107">解決策</span><span class="sxs-lookup"><span data-stu-id="13c30-107">Resolution</span></span>

<span data-ttu-id="13c30-108">一般会計で年度末決算を実行した場合に、次の会計年度の期首残高が表示されない試算表が生成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="13c30-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="13c30-109">**前の決算を元に戻す** フィールドが **はい** に設定されている場合は、同じ会計年度の実行された年度末決算が元に戻されます。</span><span class="sxs-lookup"><span data-stu-id="13c30-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="13c30-110">年度末決算を元に戻すプロセスを実行すると、決算残高と期首残高の両方のエントリが削除され、年度末決算が実行されていない状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="13c30-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="13c30-111">伝票も削除されます。</span><span class="sxs-lookup"><span data-stu-id="13c30-111">The vouchers are also deleted.</span></span> <span data-ttu-id="13c30-112">年度末決算プロセスは、自動的には再実行されません。</span><span class="sxs-lookup"><span data-stu-id="13c30-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="13c30-113">プロセスを再度開始する必要があります。その場合、**前の決算を元に戻す** オプションを **いいえ** に更新します。</span><span class="sxs-lookup"><span data-stu-id="13c30-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="13c30-114">このシナリオについては、年度末決算に関する FAQ トピックで取り上げられています。</span><span class="sxs-lookup"><span data-stu-id="13c30-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="13c30-115">詳細については、[年度末の活動に関するよく寄せられる質問](faq-year-end-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13c30-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="13c30-116">現象</span><span class="sxs-lookup"><span data-stu-id="13c30-116">Symptom</span></span>

<span data-ttu-id="13c30-117">**前の決算を元に戻す** オプションを **いいえ** に設定して年度末決算を実行しましたが、会計年度の期首残高が表示されません。</span><span class="sxs-lookup"><span data-stu-id="13c30-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="13c30-118">解決策</span><span class="sxs-lookup"><span data-stu-id="13c30-118">Resolution</span></span>

<span data-ttu-id="13c30-119">最初にバッチ ジョブの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="13c30-119">First check the status of the batch job.</span></span> <span data-ttu-id="13c30-120">年度末決算には複数の別々のタスクが含まれますが、最も重要なステップは、タスクの記述 **ステップ 5.0.0** のバッチ タスクです。</span><span class="sxs-lookup"><span data-stu-id="13c30-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="13c30-121">このステップで、開始トランザクションと、必要に応じて決算トランザクションを一般会計に転記します。</span><span class="sxs-lookup"><span data-stu-id="13c30-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="13c30-122">[![バッチ履歴リスト](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="13c30-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="13c30-123">このステップが正常に終了しても、**試算表の照会** ページ (**一般会計 > 照会とレポート > 試算表**) に期首残高が表示されない場合は、年度末決算バッチ ジョブの結果を確認し、残高の再構築ステップが正常に完了したどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="13c30-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="13c30-124">[![年度末決算バッチ ジョブの結果](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="13c30-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="13c30-125">何らかの理由でこのステップが失敗している場合は、開始 (およびオプションで決算) トランザクションが正常に転記されている可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="13c30-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="13c30-126">**伝票トランザクションの照会** ページ (**一般会計 > 照会とレポート > 伝票トランザクション**) を使用して、決算した年度の年度末決算ダイアログに表示される伝票番号と日付を指定することで、一般会計トランザクションが正常に転記されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="13c30-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="13c30-127">[![伝票トランザクションの照会](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="13c30-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="13c30-128">開始伝票 (および必要に応じて決算伝票) が存在する場合は、年度末決算を再度実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="13c30-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="13c30-129">代わりに、次に進む方法ついて次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="13c30-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="13c30-130">現象</span><span class="sxs-lookup"><span data-stu-id="13c30-130">Symptom</span></span>

<span data-ttu-id="13c30-131">"残高の再構築" ステップが失敗しました。年度末決算プロセス全体を再実行する必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="13c30-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="13c30-132">解決策</span><span class="sxs-lookup"><span data-stu-id="13c30-132">Resolution</span></span>

<span data-ttu-id="13c30-133">残高の再構築ステップでは、試算表の生成時に使用される一般会計残高が更新されます。</span><span class="sxs-lookup"><span data-stu-id="13c30-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="13c30-134">これは、年度末決算プロセスの最後のステップです。</span><span class="sxs-lookup"><span data-stu-id="13c30-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="13c30-135">このステップしか失敗していない場合は、一般会計トランザクションは正常に転記されています。</span><span class="sxs-lookup"><span data-stu-id="13c30-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="13c30-136">年度末決算を再実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="13c30-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="13c30-137">このプロセスを実行するには、**財務分析コード セット** ページ (**一般会計 > 勘定科目表 > 分析コード > 財務分析コード セット**) を使用して、残高を手動で再構築します。</span><span class="sxs-lookup"><span data-stu-id="13c30-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="13c30-138">[![[財務分析コード セット] ページの [残高の再構築] ボタン](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="13c30-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="13c30-139">このステップの処理に時間がかかる場合は、[財務分析コード セットの更新に関するベスト プラクティス](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets)で説明されている手順に従って、財務分析コード セットのベスト プラクティスを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="13c30-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

