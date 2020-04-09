---
title: 会計年度末のプロジェクト予算の転送
description: この記事では、予算残高金額を将来の年に振り替え、予算登録の詳細を作成する方法についての情報を提供します。
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172333"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="3b23e-103">会計年度末のプロジェクト予算の転送</span><span class="sxs-lookup"><span data-stu-id="3b23e-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b23e-104">複数年のプロジェクトで作業している場合は、会計年度の終わりに予算が残っていることがあります。</span><span class="sxs-lookup"><span data-stu-id="3b23e-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="3b23e-105">残り予算の残高を将来の年に転送し、関連する一般会計勘定でその金額に対して予算登録の詳細を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="3b23e-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="3b23e-106">残余額を繰り越す前に、予算残高を確認および分析します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="3b23e-107">予算残高の確認および分析</span><span class="sxs-lookup"><span data-stu-id="3b23e-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="3b23e-108">プロジェクトの期末の予算金額を確認したいが、金額を繰り越さない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="3b23e-109">**プロジェクト管理と会計** > **定期** > **予算** > **繰り越し予算** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="3b23e-110">**プロジェクト予算の繰り越しプロセス** ページの **期末オプション** タブで、**残りのプロジェクト予算金額を繰り越し** が有効になっていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="3b23e-111">**パラメータ** タブの **プロジェクト予算の年度** フィールドで、予算残高額を表示したい会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="3b23e-112">**開始会計年度** フィールドで、予算残高額を表示する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="3b23e-113">**開始予測モデル** フィールドで、**予算残高** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="3b23e-114">選択した基準に一致し、予算残高がないプロジェクトを含めるには、**ゼロ残高の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="3b23e-115">**予算の選択** タブで、**すべての予算を取得** を選択して、選択した基準に一致するすべての予算を読み込み、**処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="3b23e-116">ウィンドウに特定の一連の予算を読み込むデータベースのクエリをデザインする場合は、**選択した予算を取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="3b23e-117">ウィンドウの特定明細行に関する詳細については、その明細行を選択して、**予算の詳細** または **勘定の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="3b23e-118">予算残金の繰越し</span><span class="sxs-lookup"><span data-stu-id="3b23e-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="3b23e-119">予算残高を処理するときに、繰り越すの金額のトランザクションを一般会計で作成するかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="3b23e-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="3b23e-120">一般会計トランザクションを作成するには、[予算残高を繰り越し、一般会計トランザクションを作成する](#carry-forward) セクションにある手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="3b23e-121">繰り越された予算金額は、**予測モデル** ページで繰越予測モデルとして選択された予測モデルに転送されます。</span><span class="sxs-lookup"><span data-stu-id="3b23e-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="3b23e-122">予算金額の繰り越しおよび一般会計トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="3b23e-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="3b23e-123">**プロジェクト管理と会計** > **定期** > **予算** > **繰越予算** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="3b23e-124">**プロジェクト予算の繰り越しプロセス** ページで、**年度末** を選択し、**プロジェクトの予算残高の繰り越し** と **一般会計で予算登録エントリを作成する** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="3b23e-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="3b23e-125">**パラメータ** タブの、**プロジェクト パラメータ** フィールド グループで、次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="3b23e-126">**プロジェクト予算年** : 予算残高を表示する会計年度の期首を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="3b23e-127">**損益計算書** : 一般会計で損益トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="3b23e-128">**仕掛品** : 進行中の作業 (仕掛品) トランザクションを一般会計で作成します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="3b23e-129">**給与**: 一般会計で給与配賦トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="3b23e-130">**一般会計** フィールド グループに、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="3b23e-131">**開始会計年度** フィールドで、プロジェクトの予算残高を転送する会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="3b23e-132">既定値は、**プロジェクトの予算年度** フィールドの 1 年後の値です。</span><span class="sxs-lookup"><span data-stu-id="3b23e-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="3b23e-133">**繰り越し期間** フィールドで、一般会計に予算登録の詳細を作成する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="3b23e-134">これは通常、開始会計年度の最初の期間です。</span><span class="sxs-lookup"><span data-stu-id="3b23e-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="3b23e-135">**コピー元 / コピー先** フィールド グループに、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="3b23e-136">**開始予測モデル** フィールドで、プロジェクトで転送する予算残高に関連付けられているプロジェクト予算の予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="3b23e-137">**終了元帳予算モデル** フィールドで、一般会計に転送する予算残高に関連付けられている元帳予算モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="3b23e-138">プロジェクトの予算金額を転送するときに作成される一般会計トランザクションに対するプロジェクトの販売通貨を使用するには、**販売通過の転送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="3b23e-139">このオプションが選択されていない場合、トランザクションは会計通貨を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="3b23e-140">下ウィンドウに表示されているプロジェクトの中で、予算残高はないが、選択した他の基準を満たすプロジェクトを含める場合は、**ゼロ残高の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="3b23e-141">**予算の選択** タブで、**すべての予算の取得** を選択して、選択した基準に一致するすべての予算を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="3b23e-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="3b23e-142">ウィンドウに特定の一連のプロジェクト予算を読み込むデータベースのクエリをデザインしたい場合は、**選択した予算を取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="3b23e-143">処理するプロジェクトごとに、プロジェクトの明細行の先頭にあるオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="3b23e-144">すべてまたはほとんどのプロジェクトを選択するには、左上隅にあるチェックマークをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3b23e-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="3b23e-145">プロジェクトの処理を除外するには、そのプロジェクトのチェックマークを外します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="3b23e-146">選択したプロジェクトの予算残高を、選択した会計年度に転送し、一般会計で予算登録の詳細を作成するには、**プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="3b23e-147">一般会計トランザクションは作成せずに予算金額を繰り越す</span><span class="sxs-lookup"><span data-stu-id="3b23e-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="3b23e-148">**プロジェクト管理と会計** > **定期** > **予算** > **繰り越し予算** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="3b23e-149">**プロジェクト予算の繰り越しプロセス** ページの **期末オプション** フィールドで、**プロジェクト予算残高の繰越** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="3b23e-150">**パラメータ** グループの、**プロジェクト予算年** フィールドで、予算残高額を表示したい会計年度を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="3b23e-151">**コピー元 / コピー先** グループで、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="3b23e-152">**開始予測モデル** フィールドで、プロジェクトで転送する予算残高に関連付けられているプロジェクト予算の予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="3b23e-153">選択したその他の基準に一致し、予算残高がないプロジェクトを含めるには、**ゼロ残高の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="3b23e-154">**予算の選択** グループで、**すべての予算の取得** を選択して、選択した基準に一致するすべての予算を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="3b23e-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="3b23e-155">ウィンドウに特定の一連のプロジェクト予算を読み込むデータベースのクエリをデザインする場合は、**選択した予算を取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="3b23e-156">処理するプロジェクトごとに、プロジェクトの明細行の先頭にあるオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="3b23e-157">**プロセス** を選択して、選択したプロジェクトの予算残高を選択した会計年度に転送します。</span><span class="sxs-lookup"><span data-stu-id="3b23e-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

