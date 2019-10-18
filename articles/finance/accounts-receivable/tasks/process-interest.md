---
title: 利息の処理
description: この手順では、利子計算書の作成、印刷、および転記の方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188766"
---
# <a name="process-interest"></a><span data-ttu-id="b53c1-103">利息の処理</span><span class="sxs-lookup"><span data-stu-id="b53c1-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b53c1-104">この手順では、利子計算書の作成、印刷、および転記の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="b53c1-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="b53c1-106">転記プロファイルの利息を設定します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="b53c1-107">**ナビゲーション ウィンドウ**で、**モジュール > 貸方転記および取立 > 設定 > 顧客転記プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="b53c1-108">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-108">Click **Edit**.</span></span>
3. <span data-ttu-id="b53c1-109">**設定クイック タブ**の、**利息コード** フィールドで、ドロップダウン リストから利息コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="b53c1-110">この転記プロファイルを使用してトランザクションの利息を計算したくない場合、フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="b53c1-111">**テーブル制限**クイック タブで利息の処理方法を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="b53c1-112">このフィールドが [はい] に設定されている場合、利息はこの転記プロファイルに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="b53c1-113">利息の計算</span><span class="sxs-lookup"><span data-stu-id="b53c1-113">Calculate interest</span></span>
1. <span data-ttu-id="b53c1-114">**ナビゲーション ウィンドウ**で、**モジュール > 貸方転記および取立 > 利息 > 利子計算書の作成**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="b53c1-115">利息を計算するためのトランザクション タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b53c1-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="b53c1-116">これらのタイプのすべての未処理トランザクションがこの計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="b53c1-117">**利息**を 'はい' に設定すると、利子の利息が計算されます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="b53c1-118">これらのトランザクションを含める前に、利子の利息計算を規定する法令を確認できます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="b53c1-119">**開始日**フィールドに、この利息計算が始まる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="b53c1-120">**開始日**を特定しない場合、すべての未転記の利子計算書はキャンセルされ、利息はトランザクションの日付から再度計算されます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="b53c1-121">**終了日**フィールドに、この利息計算が終わる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="b53c1-122">**使用する転記プロファイル** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="b53c1-123">3 つの転記プロファイル オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b53c1-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="b53c1-124">勘定科目 – 各利子計算書の顧客勘定に割り当てられた転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="b53c1-125">選択 – [転記プロファイル] フィールドで選択した転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="b53c1-126">[トランザクション] 利子計算書ごとに利息が計算されるトランザクションから個々の転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="b53c1-127">割り当てられた転記プロファイルのないトランザクションでは、[買掛金勘定パラメータ] フォーム上の [元帳と売上税] エリアで指定された転記プロファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="b53c1-128">**対象に含めるレコード** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="b53c1-129">**フィルター**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-129">Click **Filter**.</span></span>
9. <span data-ttu-id="b53c1-130">**基準**フィールドに、顧客 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="b53c1-131">たとえば、「US-001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="b53c1-132">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-132">Click **OK**.</span></span>
7. <span data-ttu-id="b53c1-133">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="b53c1-134">利子計算書の印刷</span><span class="sxs-lookup"><span data-stu-id="b53c1-134">Print interest notes</span></span>
1. <span data-ttu-id="b53c1-135">**ナビゲーション ウィンドウ**で、**モジュール > 貸方転記および取立 > 利息 > 利子計算書の確認と処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="b53c1-136">**ステータス** フィールドで '作成済' を選択します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="b53c1-137">**印刷済**フィールドで、'印刷せず' を選択します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="b53c1-138">**印刷** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-138">Click **Print**.</span></span>
5. <span data-ttu-id="b53c1-139">**対象に含めるレコード** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="b53c1-140">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-140">Click **OK**.</span></span>
7. <span data-ttu-id="b53c1-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="b53c1-142">利子計算書の転記</span><span class="sxs-lookup"><span data-stu-id="b53c1-142">Post the interest note</span></span>
1. <span data-ttu-id="b53c1-143">転記の準備が整った利子計算書を選択します (ステータスは作成済)。</span><span class="sxs-lookup"><span data-stu-id="b53c1-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="b53c1-144">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-144">Click **Post**.</span></span>
3. <span data-ttu-id="b53c1-145">利子計算書の転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="b53c1-146">利子計算書ごとに総勘定元帳トランザクションを作成する場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="b53c1-147">「はい」を選択しない場合、顧客に対するすべての利子計算書の利子が累計され、1 つのトランザクションで総勘定元帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="b53c1-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="b53c1-148">**対象に含めるレコード** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="b53c1-149">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b53c1-149">Click **OK**.</span></span>
6. <span data-ttu-id="b53c1-150">**ステータス** フィールドで '転記済' を選択します。</span><span class="sxs-lookup"><span data-stu-id="b53c1-150">In the **Status** field, select 'Posted'.</span></span>

