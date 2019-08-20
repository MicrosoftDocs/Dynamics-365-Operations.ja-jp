---
title: 督促状の処理
description: この手順では、督促状の作成、印刷、および転記の方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8db80b184d565f71f62f99051c7378c4e6e45fb9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834418"
---
# <a name="process-collection-letters"></a><span data-ttu-id="fd265-103">督促状の処理</span><span class="sxs-lookup"><span data-stu-id="fd265-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd265-104">この手順では、督促状の作成、印刷、および転記の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fd265-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="fd265-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd265-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="fd265-106">転記プロファイルでの督促状シーケンスの設定</span><span class="sxs-lookup"><span data-stu-id="fd265-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="fd265-107">**貸方転記および取立 > 設定 > 顧客転記プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd265-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="fd265-108">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-108">Click **Edit**.</span></span>
3. <span data-ttu-id="fd265-109">ドロップダウン リストから督促状の順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="fd265-110">この転記プロファイルを使用するトランザクションで督促状を生成したくない場合、フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="fd265-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="fd265-111">テーブル制限タブを展開し、督促状の処理方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="fd265-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="fd265-112">このフィールドが**はい**に設定されているなら、督促状はこの転記プロファイルに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="fd265-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="fd265-113">督促状の作成</span><span class="sxs-lookup"><span data-stu-id="fd265-113">Create collection letters</span></span>
1. <span data-ttu-id="fd265-114">**貸方転記および取立 > 督促状 > 督促状の作成**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd265-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="fd265-115">レターを収集するトランザクション タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="fd265-116">これらのタイプのすべての未処理トランザクションがこの計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd265-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="fd265-117">**督促状**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="fd265-118">督促状の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd265-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="fd265-119">**使用する転記プロファイル**で**選択**に変更した場合、転記プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="fd265-120">2 つの転記プロファイルのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="fd265-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="fd265-121">**勘定科目** – 各利子計算書の顧客勘定に割り当てられた転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fd265-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="fd265-122">**選択** – **転記プロファイル** フィールドで選択した転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fd265-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="fd265-123">**対象に含めるレコード** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd265-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="fd265-124">**フィルター**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-124">Click **Filter**.</span></span>
7. <span data-ttu-id="fd265-125">**基準**フィールドに、顧客 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd265-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="fd265-126">たとえば、「US-001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd265-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="fd265-127">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-127">Click **OK**.</span></span>
9. <span data-ttu-id="fd265-128">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="fd265-129">督促状の印刷</span><span class="sxs-lookup"><span data-stu-id="fd265-129">Print collection letters</span></span>
1. <span data-ttu-id="fd265-130">**貸方転記および取立 > 督促状 > 督促状の確認と処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd265-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="fd265-131">**ステータス** フィールドで**作成済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="fd265-132">**印刷済**フィールドで、**印刷せず**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="fd265-133">**印刷** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-133">Click **Print**.</span></span>
5. <span data-ttu-id="fd265-134">**督促状の注記**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="fd265-135">**対象に含めるレコード** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd265-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="fd265-136">転記の締日を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd265-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="fd265-137">督促状を印刷するために **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="fd265-138">督促状を転記します。</span><span class="sxs-lookup"><span data-stu-id="fd265-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="fd265-139">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-139">Click **Post**.</span></span>
   2. <span data-ttu-id="fd265-140">督促状の転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd265-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="fd265-141">**対象に含めるレコード** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd265-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="fd265-142">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-142">Click **OK**.</span></span>
   5. <span data-ttu-id="fd265-143">**ステータス** フィールドで、**転記済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="fd265-144">**印刷済**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd265-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="fd265-145">顧客レベルで督促状の管理する</span><span class="sxs-lookup"><span data-stu-id="fd265-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="fd265-146">各トランザクションの督促状コードが追跡されるように、顧客レベルで督促状を設定することもできます。ただし督促状の処理は、顧客用に保管されている 1 つの督促状レベルに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="fd265-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="fd265-147">1 つの督促状には、顧客の期限を過ぎているすべてのトランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd265-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="fd265-148">支払猶予日数は、顧客レベルで追跡されるようになったため、最後の督促状の送信後にトランザクションが期限切れになっても、順序内の次の督促状に対して支払猶予日数が経過するまで督促状は送信されません。</span><span class="sxs-lookup"><span data-stu-id="fd265-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="fd265-149">このオプションは、顧客ごとに送信する督促状の数を削減します。</span><span class="sxs-lookup"><span data-stu-id="fd265-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="fd265-150">顧客レベルで督促状を管理するように顧客を設定する</span><span class="sxs-lookup"><span data-stu-id="fd265-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="fd265-151">**貸方転記および取立 > 設定 > 売掛金勘定パラメーター**に移動し、**回収**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="fd265-152">**次の単位別に督促状を作成**の値を**顧客**に変更します。</span><span class="sxs-lookup"><span data-stu-id="fd265-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="fd265-153">**貸方転記および取立 > 督促状 > 督促状の確認と処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd265-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="fd265-154">期限切れのすべてのトランザクションを持つ顧客に対して督促状が 1 つだけ生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd265-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="fd265-155">督促状コードの計算する時に、支払およびクレジット メモを無視する</span><span class="sxs-lookup"><span data-stu-id="fd265-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="fd265-156">督促状に記載されるトランザクションの支払とクレジット メモを含める場合、督促状をトリガーする支払またはクレジット メモがある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd265-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="fd265-157">**督促状コードを計算する時に支払とクレジット メモを無視する**パラメーターの値を変更することで、支払とクレジット メモが督促状コードを制御する方法をコントロールできます。</span><span class="sxs-lookup"><span data-stu-id="fd265-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="fd265-158">督促状コードを計算する時に支払とクレジット メモを無視するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="fd265-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="fd265-159">**貸方転記および取立 > 設定 > 売掛金勘定パラメーター**に移動し、**回収**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd265-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="fd265-160">Change the value of **督促状コードを計算する時に支払とクレジット メモを無視する**の値を**はい**に変更します。</span><span class="sxs-lookup"><span data-stu-id="fd265-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
