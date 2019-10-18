---
title: 会計年度の決算
description: この手順では、残高を新しい会計年度に振り替える年度末決算処理について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c12f0842f6e8edf3b51d12d0e008eb09acf8c374
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178602"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="d8a00-103">会計年度の決算</span><span class="sxs-lookup"><span data-stu-id="d8a00-103">Close the fiscal year</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8a00-104">この手順では、残高を新しい会計年度に振り替える年度末決算処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="d8a00-105">年度末決算のパラメーターを検証します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="d8a00-106">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 元帳の設定 > 一般会計パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="d8a00-107">**会計年度末決算**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="d8a00-108">**振替時に決算トランザクションを削除する**オプションで、「はい」または「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="d8a00-109">会計年度が既に決済され、年度末決算が再度実行されている場合、この設定が重要です。</span><span class="sxs-lookup"><span data-stu-id="d8a00-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="d8a00-110">[はい] と設定されている場合、以前の年度末決算の伝票が削除されると、新しい伝票がすべての勘定の開始残高に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="d8a00-111">[いいえ] と設定されている場合、以前の伝票が保持され、新しい伝票が最後の年度末決算の転記後に調整エントリに対してのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="d8a00-112">**振替時に決算トランザクションを作成する**オプションで、「はい」または「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="d8a00-113">[はい] と設定している場合、2 つのトランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="d8a00-114">終了した会計年度に 1 番目の伝票が P&L 勘定科目の残高をゼロにするために引き下げるために作成され、2 番目の伝票は、次の会計年度に期首残高のために作成されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="d8a00-115">[いいえ] と設定している場合、期首残高のために次の会計年度に、1 つの伝票が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="d8a00-116">**会計年度の状態を完全に終了する**オプションで、「はい」または「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="d8a00-117">[はい] と設定している場合、会計年度のステータスは [完全に閉じる] と設定されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="d8a00-118">完全に終了した年度は再度開くことができないため、このオプションは [いいえ] に設定することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="d8a00-119">**伝票番号を年度末決算時に転記する必要がある**オプションで、「はい」または「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="d8a00-120">[はい] と設定している場合、年度末決算処理中に、伝票番号を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a00-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="d8a00-121">番号の順序は、この伝票番号の生成には使用されません。</span><span class="sxs-lookup"><span data-stu-id="d8a00-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="d8a00-122">この推奨設定は [はい] です。</span><span class="sxs-lookup"><span data-stu-id="d8a00-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="d8a00-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-123">Close the page.</span></span>
8. <span data-ttu-id="d8a00-124">**一般会計 > 期間の締め > 年度末決算**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="d8a00-125">**新規**をクリックして、年度末決算テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="d8a00-126">テンプレートは年度末決算を実行する法人グループ用に作成できます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="d8a00-127">このテンプレートは次年度にも再利用できます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="d8a00-128">**グループ名**フィールドで、年度末決算テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="d8a00-129">**会計カレンダー** フィールドで、テンプレートを作成する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="d8a00-130">同じ会計年度を使用する法人のみを、年度末決算テンプレートにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="d8a00-131">これは、期末決算が日付ではなく、会計年度の選択によって実行されるためです。</span><span class="sxs-lookup"><span data-stu-id="d8a00-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="d8a00-132">**アクション ウィンドウ**で、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8a00-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="d8a00-133">**法人**セクションで、**追加**をクリックして、このテンプレートの法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="d8a00-134">法人を選択するか、または組織階層を選択することにより、法人を追加できます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="d8a00-135">選択された同じ会計カレンダーを使用する組織階層の法人のみが追加されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="d8a00-136">法人または組織階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="d8a00-137">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8a00-137">Click **OK**.</span></span>
16. <span data-ttu-id="d8a00-138">**貸借対照表の分析コードを転送**で、「はい」または「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="d8a00-139">貸借対照表勘定の場合は、このオプションをはいに設定するのが最善です。</span><span class="sxs-lookup"><span data-stu-id="d8a00-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="d8a00-140">これは、貸借対照表勘定の開始残高を作成するときに転記されたトランザクションの財務分析コードを管理します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="d8a00-141">損益勘定の場合、残高が利益剰余金に移動した場合に財務分析コード (すべて閉じる) を維持するように選択するか、または異なる分析コード値 (1 つ閉じる) を使用して財務分析コードを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="d8a00-142">[1 つ閉じる] を選択した場合は、各分析コードに特定の分析コード値を定義するか、またはそれを空のままにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="d8a00-143">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8a00-143">Click **Save**.</span></span>
18. <span data-ttu-id="d8a00-144">**アクション ウィンドウ**の**期末決算の実行**の選択によって年度末決算を開始します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="d8a00-145">年度末決算が選択されたテンプレートに対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="d8a00-146">テンプレートから年度末決算を実行する法人グループのすべてまたはサブセットを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="d8a00-147">年度末決算を最初に実行する場合、開始残高を取得するために、ほとんどの組織は、テンプレート内のすべての法人の年度末決算を実行することを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="d8a00-148">調整エントリがその後に行われた場合、調整がある法人のみに対して、年度末決算を実行することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d8a00-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="d8a00-149">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8a00-149">Click **OK**.</span></span>
21. <span data-ttu-id="d8a00-150">年度末決算を実行する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="d8a00-151">**伝票フィールド**に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="d8a00-152">作成された年度末決算伝票を検索しやすいように、伝票番号に会計年度を含めることを推奨します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="d8a00-153">バッチで実行する年度末決算の既定値。</span><span class="sxs-lookup"><span data-stu-id="d8a00-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="d8a00-154">処理時間が長いプロセスはバッチ モードで処理することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="d8a00-155">これが、既定ではバッチ モードを使用する理由となる、典型的な処理の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="d8a00-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="d8a00-156">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8a00-156">Click **OK**.</span></span>
