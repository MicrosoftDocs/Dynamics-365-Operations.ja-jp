--- 
title: "督促状の処理"
description: "この手順では、督促状の作成、印刷、および転記の方法を示します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="c556d-103">督促状の処理</span><span class="sxs-lookup"><span data-stu-id="c556d-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c556d-104">この手順では、督促状の作成、印刷、および転記の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c556d-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="c556d-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="c556d-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="c556d-106">転記プロファイルでの督促状シーケンスの設定</span><span class="sxs-lookup"><span data-stu-id="c556d-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="c556d-107">[貸方転記および取立] > [設定] > [顧客転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c556d-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="c556d-108">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-108">Click Edit.</span></span>
    * <span data-ttu-id="c556d-109">ドロップダウン リストから督促状の順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="c556d-110">この転記プロファイルを使用するトランザクションで督促状を生成したくないなら、フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="c556d-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="c556d-111">テーブル制限タブで、督促状の処理方法を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c556d-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="c556d-112">このフィールドが [はい] に設定されているなら、督促状はこの転記プロファイルに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="c556d-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="c556d-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c556d-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="c556d-114">督促状の作成</span><span class="sxs-lookup"><span data-stu-id="c556d-114">Create collection letters</span></span>
1. <span data-ttu-id="c556d-115">[貸方転記および取立] > [督促状] > [督促状の作成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c556d-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="c556d-116">レターを収集するトランザクション タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c556d-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="c556d-117">これらのタイプのすべての未処理トランザクションがこの計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="c556d-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="c556d-118">[督促状] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="c556d-119">督促状の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c556d-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="c556d-120">2 つの転記プロファイルのオプションがあります: [口座] – 各利子計算書の顧客 ID に割り当てられた転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c556d-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="c556d-121">選択 – [転記プロファイル] フィールドで選択した転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c556d-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="c556d-122">[使用する転記プロファイル] で [選択] に変更した場合、転記プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="c556d-123">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c556d-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="c556d-124">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-124">Click Filter.</span></span>
6. <span data-ttu-id="c556d-125">[基準] フィールドで、[基準] フィールドで、[顧客 ID] を入力します。</span><span class="sxs-lookup"><span data-stu-id="c556d-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="c556d-126">たとえば、「US-001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c556d-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="c556d-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-127">Click OK.</span></span>
8. <span data-ttu-id="c556d-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="c556d-129">督促状の印刷</span><span class="sxs-lookup"><span data-stu-id="c556d-129">Print collection letters</span></span>
1. <span data-ttu-id="c556d-130">[貸方転記および取立] > [督促状] > [督促状の確認と処理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c556d-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="c556d-131">[ステータス] フィールドで [作成済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="c556d-132">[印刷済] フィールドで、「印刷せず」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="c556d-133">[印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-133">Click Print.</span></span>
5. <span data-ttu-id="c556d-134">[督促状の注記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="c556d-135">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c556d-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c556d-136">転記の締日を入力します。</span><span class="sxs-lookup"><span data-stu-id="c556d-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="c556d-137">督促状を印刷するために [OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="c556d-138">督促状の転記</span><span class="sxs-lookup"><span data-stu-id="c556d-138">Post the collection letter</span></span>
1. <span data-ttu-id="c556d-139">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-139">Click Post.</span></span>
2. <span data-ttu-id="c556d-140">督促状の転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c556d-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="c556d-141">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c556d-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="c556d-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c556d-142">Click OK.</span></span>
5. <span data-ttu-id="c556d-143">[ステータス] フィールドで [転記済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="c556d-144">[印刷済] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c556d-144">In the Printed field, select an option.</span></span>


