---
title: 進捗状況に基づいた請求書のアドバンス契約の作成
description: このトピックではプロジェクト契約を作成して、完了した作業の割合に基づいて顧客に請求書を生成できるようにする方法について説明します。
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282835"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="74ccd-103">進捗状況に基づいた請求書のアドバンス契約の作成</span><span class="sxs-lookup"><span data-stu-id="74ccd-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="74ccd-104">このトピックではプロジェクト契約を作成して、完了した作業の割合に基づいて顧客に請求書を生成できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="74ccd-105">プロジェクトに対して設定される作業の予算カテゴリの請求書の金額が自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="74ccd-106">請求のタイミングは、顧客とのプロジェクト契約交渉の際に設定されます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="74ccd-107">契約、関連付けられたプロジェクト、およびプロジェクトに対して設定される作業の予算カテゴリの請求書を計算するために使用される計算ルールを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="74ccd-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="74ccd-108">契約とプロジェクトを作成すると、プロジェクトの詳細を設定できます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="74ccd-109">たとえば、活動を定義し、プロジェクトに作業者を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="74ccd-110">例</span><span class="sxs-lookup"><span data-stu-id="74ccd-110">Example</span></span>

<span data-ttu-id="74ccd-111">組織はソフトウェア開発会社です。</span><span class="sxs-lookup"><span data-stu-id="74ccd-111">Your organization is a software development firm.</span></span> <span data-ttu-id="74ccd-112">合計費用 20,000 米ドル (USD) で顧客の給与会計パッケージを開発することに合意します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="74ccd-113">組織は、プロジェクトで指定された割合が完了したときに顧客に請求書を送付することに合意します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="74ccd-114">その作業に対して次のプロジェクト カテゴリを設定し、それらのカテゴリを次の請求プロセスで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="74ccd-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="74ccd-115">コンサルティング</span><span class="sxs-lookup"><span data-stu-id="74ccd-115">Consulting</span></span>
- <span data-ttu-id="74ccd-116">設計</span><span class="sxs-lookup"><span data-stu-id="74ccd-116">Design</span></span>
- <span data-ttu-id="74ccd-117">インストール</span><span class="sxs-lookup"><span data-stu-id="74ccd-117">Installation</span></span>

<span data-ttu-id="74ccd-118">各カテゴリにおいて完了したプロジェクト作業の割合に対して、自動的に請求金額を計算する請求ルールも設定します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="74ccd-119">予算マネージャは、プロジェクト カテゴリの予算を作成します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="74ccd-120">完了した作業の金額は、予算金額と比較した実際の作業の割合として自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="74ccd-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="74ccd-121">Prerequisites</span></span>

<span data-ttu-id="74ccd-122">請求ルールを使用するプロジェクトを作成する前に、請求ルールの番号シーケンスと、分割請求の転記に使用される手数料仕訳帳を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74ccd-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="74ccd-123">**プロジェクト管理および会計** \> **設定** \> **プロジェクト管理および会計のパラメータ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="74ccd-124">**番号シーケンス** タブの **プロジェクト管理および会計のパラメータ** ページで、請求ルールを作成するときに使用する番号シーケンスを設定します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="74ccd-125">**プロジェクト管理および会計** \> **仕訳帳** \> **費用** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="74ccd-126">**費用仕訳帳** ページで、**新規** を選択し、仕訳帳名を入力します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="74ccd-127">分割請求の契約を作成する</span><span class="sxs-lookup"><span data-stu-id="74ccd-127">Create a contract for progress billings</span></span>

<span data-ttu-id="74ccd-128">固定価格プロジェクトのプロジェクト契約を作成するには、この手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="74ccd-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="74ccd-129">プロジェクトで完了した作業が指定した割合に到達したときにプロジェクト請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="74ccd-130">**プロジェクト管理および会計** \> **プロジェクト** \> **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="74ccd-131">**プロジェクト契約** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="74ccd-132">**新規プロジェクト契約** ダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="74ccd-133">**氏名**</span><span class="sxs-lookup"><span data-stu-id="74ccd-133">**Name**</span></span>
    - <span data-ttu-id="74ccd-134">**資金調達タイプ**</span><span class="sxs-lookup"><span data-stu-id="74ccd-134">**Funding type**</span></span>
    - <span data-ttu-id="74ccd-135">**資金調達元**</span><span class="sxs-lookup"><span data-stu-id="74ccd-135">**Funding source**</span></span>
    - <span data-ttu-id="74ccd-136">**販売通過** – 既定では、この通貨が、プロジェクト契約に関連付けられる顧客請求書に使用されます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="74ccd-137">ただし、特定の顧客請求書で販売通貨を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="74ccd-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-138">Select **OK**.</span></span> <span data-ttu-id="74ccd-139">この情報は、**プロジェクト契約** ページのヘッダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="74ccd-140">**プロジェクト契約** ページで、プロジェクトに必要な残りの情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="74ccd-141">分割請求のプロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="74ccd-141">Create a project for progress billings</span></span>

<span data-ttu-id="74ccd-142">このステップに従って、プロジェクト契約に関連付けられているプロジェクトとサブプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="74ccd-143">**プロジェクト管理および会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="74ccd-144">**すべてのプロジェクト** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="74ccd-145">**新しいプロジェクト** ダイアログ ボックスで、**プロジェクト タイプ** フィールドで **時間と材料** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="74ccd-146">プロジェクト グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-146">Select a project group.</span></span> <span data-ttu-id="74ccd-147">プロジェクト グループは、グループに割り当てられるそのプロジェクトの転記情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="74ccd-148">**プロジェクトの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-148">Select **Create project**.</span></span>
6. <span data-ttu-id="74ccd-149">プロジェクトを作成した後、プロジェクトのステージを **進行中** に設定します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="74ccd-150">プロジェクトの予算を作成する</span><span class="sxs-lookup"><span data-stu-id="74ccd-150">Create a budget for a project</span></span>

<span data-ttu-id="74ccd-151">予算カテゴリは、自動的に各カテゴリで完了した作業の割合で請求する金額を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="74ccd-152">見積原価の予算カテゴリを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="74ccd-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="74ccd-153">**プロジェクト管理および会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="74ccd-154">**すべてのプロジェクト** ページで、目的のプロジェクトを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="74ccd-155">**プロジェクト** ページの、アクション ウィンドウの、**設定** タブにある、**予算** グループで、**プロジェクト予算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="74ccd-156">**プロジェクト予算** ページで、プロジェクトの各カテゴリに対して見積原価を入力します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="74ccd-157">分割請求の計算ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="74ccd-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="74ccd-158">**プロジェクト管理および会計** \> **プロジェクト** \> **プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="74ccd-159">**プロジェクト契約** ページで、プロジェクト契約を選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="74ccd-160">プロジェクト契約ページで、**請求ルール** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="74ccd-161">**請求ルール** ページの **行タイプ** フィールドで、**進捗状況** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="74ccd-162">**請求ルールの明細行の詳細** のクイック タブで、**契約金額** フィールドに、契約の合計金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="74ccd-163">[**カテゴリ**] のフィールドで、手数料トランザクションを転記するカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="74ccd-164">[**プロジェクト**] フィールドで、この計算ルールを使用するプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="74ccd-165">オプション: 追加のプロジェクトに請求ルールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="74ccd-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="74ccd-166">**プロジェクト** クイック タブの、**使用可能なプロジェクト** セクションでプロジェクトを選択し、右矢印ボタンをクリックして、**選択したプロジェクト** セクションにプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="74ccd-167">オプション: 顧客が請求書の支払から差し引く割合の金額を計算します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="74ccd-168">**支払い留保期間** クイック タブで、資金調達ソースを選択してから、**留保期間** フィールドに留保率を入力します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="74ccd-169">プロジェクト契約の追加の請求ルールを作成するには、このステップを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="74ccd-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
