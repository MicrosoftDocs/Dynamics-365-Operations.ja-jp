---
title: 督促状の処理
description: このトピックでは、督促状の作成、印刷、および転記の方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 2b8ce102086535a5462d3fa0e8ac76e9ec3dd15c
ms.sourcegitcommit: 8fad5a8c7ea5d0d0037669e61e2313f684bcae23
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2020
ms.locfileid: "3106862"
---
# <a name="process-collection-letters"></a><span data-ttu-id="ad832-103">督促状の処理</span><span class="sxs-lookup"><span data-stu-id="ad832-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad832-104">このトピックでは、督促状の作成、印刷、および転記の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ad832-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="ad832-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="ad832-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="ad832-106">転記プロファイルでの督促状シーケンスの設定</span><span class="sxs-lookup"><span data-stu-id="ad832-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="ad832-107">**ナビゲーション ウィンドウ > モジュール > 貸方転記および取立 > 設定 > 顧客転記プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad832-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="ad832-108">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad832-108">Click **Edit**.</span></span>
3. <span data-ttu-id="ad832-109">ドロップダウン リストから督促状の順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="ad832-110">この転記プロファイルを使用するトランザクションで督促状を生成したくない場合、フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="ad832-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="ad832-111">**テーブル制限**タブを展開し、督促状の処理方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="ad832-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="ad832-112">このフィールドが**はい**に設定されているなら、督促状はこの転記プロファイルに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="ad832-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="ad832-113">督促状の作成</span><span class="sxs-lookup"><span data-stu-id="ad832-113">Create collection letters</span></span>
1. <span data-ttu-id="ad832-114">**ナビゲーション ウィンドウ > モジュール > 貸方転記および取立 > 督促状 > 督促状の作成**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad832-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="ad832-115">レターを収集するトランザクション タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="ad832-116">これらのタイプのすべての未処理トランザクションがこの計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad832-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="ad832-117">**督促状**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="ad832-118">**督促状の日付**フィールドに、督促状の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad832-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="ad832-119">**使用する転記プロファイル**で**選択**に変更した場合、転記プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="ad832-120">2 つの転記プロファイルのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ad832-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="ad832-121">**勘定科目** – 各利子計算書の顧客勘定に割り当てられた転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad832-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="ad832-122">**選択** – **転記プロファイル** フィールドで選択した転記プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad832-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="ad832-123">**対象に含めるレコード** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ad832-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="ad832-124">**フィルター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-124">Select **Filter**.</span></span>
8. <span data-ttu-id="ad832-125">**基準**フィールドに、顧客 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad832-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="ad832-126">たとえば、「US-001」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ad832-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="ad832-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-127">Select **OK**.</span></span>
10. <span data-ttu-id="ad832-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="ad832-129">督促状の印刷</span><span class="sxs-lookup"><span data-stu-id="ad832-129">Print collection letters</span></span>
1. <span data-ttu-id="ad832-130">**ナビゲーション ウィンドウ > モジュール > 貸方転記および取立 > 督促状 > 督促状の確認と処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad832-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="ad832-131">**ステータス** フィールドで**作成済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="ad832-132">**印刷済**フィールドで、**印刷せず**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="ad832-133">**印刷**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-133">Select **Print**.</span></span>
5. <span data-ttu-id="ad832-134">**督促状の注記**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="ad832-135">**パラメーター** セクションで、転記の締日を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad832-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="ad832-136">**対象に含めるレコード** セクションを展開し、督促状の注記の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad832-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="ad832-137">督促状を印刷するために **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="ad832-138">督促状を転記します。</span><span class="sxs-lookup"><span data-stu-id="ad832-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="ad832-139">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-139">Select **Post**.</span></span>
    1. <span data-ttu-id="ad832-140">督促状の転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad832-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="ad832-141">**対象に含めるレコード** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ad832-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="ad832-142">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-142">Select **OK**.</span></span>
    1. <span data-ttu-id="ad832-143">**ステータス** フィールドで、**転記済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="ad832-144">**印刷済**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="ad832-145">顧客レベルで督促状の管理する</span><span class="sxs-lookup"><span data-stu-id="ad832-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="ad832-146">督促状がトランザクション レベルで設定されている場合、トランザクションのエイジングに基づき、顧客に対して複数の文字が生成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="ad832-146">If collection letters are set up at the transaction level, multiple letters might be generated for a customer, based on transaction aging.</span></span> <span data-ttu-id="ad832-147">トランザクションが異なる督促状順序で表示される場合、顧客の各期限切れトランザクション グループに対して、個別の督促状が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ad832-147">If transactions appear in different letter sequences, separate collection letters will be generated for each group of overdue transactions for the customer.</span></span> <span data-ttu-id="ad832-148">したがって、個々の顧客は、たとえば期限超過日数が 60 日のトランザクションに対して 1 つの督促状、また 90 日のトランザクションに対しては別の督促状を受け取ることがあります。</span><span class="sxs-lookup"><span data-stu-id="ad832-148">Therefore, an individual customer might receive, for example, one collection letter for transactions that are 60 days overdue and another collection letter for transactions that are 90 days overdue.</span></span> 

<span data-ttu-id="ad832-149">各督促状は、督促状コードにも関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="ad832-149">Each collection letter is also associated with a collection letter code.</span></span> <span data-ttu-id="ad832-150">督促状コードは個々のトランザクションに関連付けられていて、いつ次の督促状を各トランザクションに対して生成するかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad832-150">The collection letter code is associated with individual transactions and is used to determine when the next collection letter should be generated for each transaction.</span></span> <span data-ttu-id="ad832-151">たとえば、トランザクションの期限切れ日数が 30 日を超えている時、督促状コードによって、それまでに支払が行われなかった場合、トランザクションの期限切れ日数が 60 日になった時に次の督促状が送信されるよう決定されます。</span><span class="sxs-lookup"><span data-stu-id="ad832-151">For example, if a transaction is more than 30 days overdue, the collection letter code determines that the next collection letter will be sent when the transaction becomes 60 days overdue, if it isn't paid before then.</span></span> 

<span data-ttu-id="ad832-152">督促状は、顧客レベルで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ad832-152">Collection letters can also be set up at the customer level.</span></span> <span data-ttu-id="ad832-153">この場合、各トランザクションの督促状コードは追跡されますが、督促状の処理は顧客に保存されている単一の督促状レベルに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="ad832-153">In this case, the collection letter code for each transaction is tracked, but collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="ad832-154">単一の督促状には、期限切れの顧客トランザクションすべてが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad832-154">The single collection letter will contain all the transactions that are overdue for the customer.</span></span> <span data-ttu-id="ad832-155">支払猶予日数が顧客レベルで追跡されるようになったため、最後の督促状の送信後にトランザクションが期限切れになっても、順序内の次の督促状に対して支払猶予日数が経過するまで督促状は送信されません。</span><span class="sxs-lookup"><span data-stu-id="ad832-155">Because the grace days are now tracked at the customer level, the next collection letter won't be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions became overdue after the last collection letter was sent.</span></span> <span data-ttu-id="ad832-156">このオプションにより、各顧客に送信する督促状の数を削減することができます。</span><span class="sxs-lookup"><span data-stu-id="ad832-156">This option helps reduce the number of collection letters that you must send to each customer.</span></span>

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="ad832-157">顧客レベルで督促状を管理するように顧客を設定する</span><span class="sxs-lookup"><span data-stu-id="ad832-157">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="ad832-158">**ナビゲーション ウィンドウ > モジュール > 貸方転記および取立 > 設定 > 売掛金勘定パラメーター**の順に移動し、**回収**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad832-158">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="ad832-159">**次の単位別に督促状を作成**の値を**顧客**に変更します。</span><span class="sxs-lookup"><span data-stu-id="ad832-159">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="ad832-160">**ナビゲーション ウィンドウ > モジュール > 貸方転記および取立 > 督促状 > 督促状の確認と処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad832-160">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="ad832-161">期限切れのすべてのトランザクションを持つ顧客に対して督促状が 1 つだけ生成されます。</span><span class="sxs-lookup"><span data-stu-id="ad832-161">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="ad832-162">督促状コードの計算する時に、支払およびクレジット メモを無視する</span><span class="sxs-lookup"><span data-stu-id="ad832-162">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="ad832-163">督促状に記載されるトランザクションの支払とクレジット メモを含める場合、督促状をトリガーする支払またはクレジット メモがある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ad832-163">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="ad832-164">**督促状コードを計算する時に支払とクレジット メモを無視する**パラメーターの値を変更することで、支払とクレジット メモが督促状コードを制御する方法をコントロールできます。</span><span class="sxs-lookup"><span data-stu-id="ad832-164">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="ad832-165">督促状コードを計算する時に支払とクレジット メモを無視するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ad832-165">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="ad832-166">**ナビゲーション ウィンドウ > モジュール > 貸方転記および取立 > 設定 > 売掛金勘定パラメーター**の順に移動し、**回収**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad832-166">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="ad832-167">Change the value of **督促状コードを計算する時に支払とクレジット メモを無視する**の値を**はい**に変更します。</span><span class="sxs-lookup"><span data-stu-id="ad832-167">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
