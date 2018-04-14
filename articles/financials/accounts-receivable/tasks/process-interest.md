--- 
title: "利息の処理"
description: "この手順では、利子計算書の作成、印刷、および転記の方法を示します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 214e12132557c12d19575f04ce69101b7457f37a
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="process-interest"></a><span data-ttu-id="b0f4d-103">利息の処理</span><span class="sxs-lookup"><span data-stu-id="b0f4d-103">Process interest</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0f4d-104">この手順では、利子計算書の作成、印刷、および転記の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="b0f4d-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="b0f4d-106">転記プロファイルの利息を設定します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="b0f4d-107">[貸方転記および取立] > [設定] > [顧客転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="b0f4d-108">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-108">Click Edit.</span></span>
    * <span data-ttu-id="b0f4d-109">ドロップダウン リストから利息コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="b0f4d-110">この転記プロファイルを使用してトランザクションの利息を計算したくない場合、フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="b0f4d-111">テーブル制限タブで利息の処理方法を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="b0f4d-112">このフィールドが [はい] に設定されている場合、利息はこの転記プロファイルに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="b0f4d-113">利息の計算</span><span class="sxs-lookup"><span data-stu-id="b0f4d-113">Calculate interest</span></span>
1. <span data-ttu-id="b0f4d-114">[貸方転記および取立] > [利息] > [利子計算書の作成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="b0f4d-115">利息を計算するためのトランザクション タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="b0f4d-116">これらのタイプのすべての未処理トランザクションがこの計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="b0f4d-117">利息を選択すると、利子の利息を計算します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="b0f4d-118">これらのトランザクションを含める前に、利子の利息計算を規定する法令を確認できます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="b0f4d-119">この日付から「終了日」までの利子が計算されます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="b0f4d-120">「開始日」を特定しない場合、すべての未転記の利子計算書はキャンセルされ、利息はトランザクションの日付から再度計算されます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="b0f4d-121">利子計算書の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="b0f4d-122">3 つの転記プロファイルのオプションがあります: [口座] – 各利子計算書の顧客 ID に割り当てられた転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="b0f4d-123">選択 – [転記プロファイル] フィールドで選択した転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="b0f4d-124">[トランザクション] 利子計算書ごとに利息が計算されるトランザクションから個々の転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="b0f4d-125">割り当てられた転記プロファイルのないトランザクションでは、[買掛金勘定パラメータ] フォーム上の [元帳と売上税] エリアで指定された転記プロファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="b0f4d-126">[転記プロファイルの使用] を [選択] に変更した場合、転記プロファイルをここで選択します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="b0f4d-127">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="b0f4d-128">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-128">Click Filter.</span></span>
5. <span data-ttu-id="b0f4d-129">[基準] フィールドに、顧客 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="b0f4d-130">たとえば、「US-001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="b0f4d-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-131">Click OK.</span></span>
7. <span data-ttu-id="b0f4d-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="b0f4d-133">利子計算書の印刷</span><span class="sxs-lookup"><span data-stu-id="b0f4d-133">Print interest notes</span></span>
1. <span data-ttu-id="b0f4d-134">[貸方転記および取立] > [利息] > [利子計算書の確認と処理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="b0f4d-135">[ステータス] フィールドで [作成済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="b0f4d-136">[印刷済] フィールドで、「印刷せず」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="b0f4d-137">[印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-137">Click Print.</span></span>
5. <span data-ttu-id="b0f4d-138">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="b0f4d-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-139">Click OK.</span></span>
7. <span data-ttu-id="b0f4d-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="b0f4d-141">利子計算書の転記</span><span class="sxs-lookup"><span data-stu-id="b0f4d-141">Post the interest note</span></span>
1. <span data-ttu-id="b0f4d-142">転記の準備が整った利子計算書を選択します (ステータスは作成済)。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="b0f4d-143">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-143">Click Post.</span></span>
3. <span data-ttu-id="b0f4d-144">利子計算書の転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="b0f4d-145">利子計算書ごとに総勘定元帳トランザクションを作成する場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="b0f4d-146">「はい」を選択しない場合、顧客に対するすべての利子計算書の利子が累計され、1 つのトランザクションで総勘定元帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="b0f4d-147">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="b0f4d-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-148">Click OK.</span></span>
6. <span data-ttu-id="b0f4d-149">[ステータス] フィールドで [転記済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0f4d-149">In the Status field, select 'Posted'.</span></span>


