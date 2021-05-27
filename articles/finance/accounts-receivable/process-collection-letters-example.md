---
title: 督促状の処理の例
description: このトピックでは、督促状の作成、印刷、および転記の処理を示す例について説明します。
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fb2651644efd2cadfccb91e48c34dfddc8383e1f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021419"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="dbb25-103">督促状の処理の例</span><span class="sxs-lookup"><span data-stu-id="dbb25-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbb25-104">このトピックでは、督促状の作成、印刷、および転記の処理を示す例について説明します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="dbb25-105">この例は、貸方転記および取立の **督促状コードを計算する時に支払とクレジット メモを無視する** オプションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="dbb25-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="dbb25-106">USMF デモ会社と新しい顧客である US-045 のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="dbb25-107">始めに、**売掛金勘定 \> 顧客 \> すべての顧客** に移動し、**新規** を選択して、顧客 US-045 を作成するために必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="dbb25-108">完了したら、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="dbb25-109">**貸方転記および取立 \> 督促状 \> 督促状の順序の設定** に移動して、顧客転記プロファイルに割り当てられている次の表に示すように督促状の順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="dbb25-110">督促状 コード</span><span class="sxs-lookup"><span data-stu-id="dbb25-110">Collection   letter code</span></span>      |     <span data-ttu-id="dbb25-111">説明</span><span class="sxs-lookup"><span data-stu-id="dbb25-111">Description</span></span>                           |     <span data-ttu-id="dbb25-112">通貨</span><span class="sxs-lookup"><span data-stu-id="dbb25-112">Currency</span></span>      |     <span data-ttu-id="dbb25-113">主勘定</span><span class="sxs-lookup"><span data-stu-id="dbb25-113">Main   account</span></span>        |     <span data-ttu-id="dbb25-114">通貨での 手数料</span><span class="sxs-lookup"><span data-stu-id="dbb25-114">Fee   in currency</span></span>     |     <span data-ttu-id="dbb25-115">最小 超過</span><span class="sxs-lookup"><span data-stu-id="dbb25-115">Minimum   over</span></span>        |     <span data-ttu-id="dbb25-116">日数 ブロック</span><span class="sxs-lookup"><span data-stu-id="dbb25-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="dbb25-117">督促状 1</span><span class="sxs-lookup"><span data-stu-id="dbb25-117">Collection   letter 1</span></span>         |     <span data-ttu-id="dbb25-118">手数料を含む 2 番目の通知</span><span class="sxs-lookup"><span data-stu-id="dbb25-118">Second   notification with fee</span></span>        |     <span data-ttu-id="dbb25-119">USD</span><span class="sxs-lookup"><span data-stu-id="dbb25-119">USD</span></span>           |                           |     <span data-ttu-id="dbb25-120">0.00</span><span class="sxs-lookup"><span data-stu-id="dbb25-120">0.00</span></span>                  |     <span data-ttu-id="dbb25-121">0.00</span><span class="sxs-lookup"><span data-stu-id="dbb25-121">0.00</span></span>                  |     <span data-ttu-id="dbb25-122">2</span><span class="sxs-lookup"><span data-stu-id="dbb25-122">2</span></span>                 |
|     <span data-ttu-id="dbb25-123">督促状 2</span><span class="sxs-lookup"><span data-stu-id="dbb25-123">Collection   letter 2</span></span>         |     <span data-ttu-id="dbb25-124">手数料を含む 2 番目の通知</span><span class="sxs-lookup"><span data-stu-id="dbb25-124">Second   notification with fee</span></span>        |     <span data-ttu-id="dbb25-125">USC</span><span class="sxs-lookup"><span data-stu-id="dbb25-125">USC</span></span>           |     <span data-ttu-id="dbb25-126">403150</span><span class="sxs-lookup"><span data-stu-id="dbb25-126">403150</span></span>                |     <span data-ttu-id="dbb25-127">20.00</span><span class="sxs-lookup"><span data-stu-id="dbb25-127">20.00</span></span>                 |     <span data-ttu-id="dbb25-128">10.00</span><span class="sxs-lookup"><span data-stu-id="dbb25-128">10.00</span></span>                 |     <span data-ttu-id="dbb25-129">3</span><span class="sxs-lookup"><span data-stu-id="dbb25-129">3</span></span>                 |
|     <span data-ttu-id="dbb25-130">取立</span><span class="sxs-lookup"><span data-stu-id="dbb25-130">Collection</span></span>                    |     <span data-ttu-id="dbb25-131">手数料を含む 最終通知</span><span class="sxs-lookup"><span data-stu-id="dbb25-131">Final   notification with fee</span></span>         |     <span data-ttu-id="dbb25-132">USD</span><span class="sxs-lookup"><span data-stu-id="dbb25-132">USD</span></span>           |     <span data-ttu-id="dbb25-133">403150</span><span class="sxs-lookup"><span data-stu-id="dbb25-133">403150</span></span>                |     <span data-ttu-id="dbb25-134">50.00</span><span class="sxs-lookup"><span data-stu-id="dbb25-134">50.00</span></span>                 |     <span data-ttu-id="dbb25-135">100.00</span><span class="sxs-lookup"><span data-stu-id="dbb25-135">100.00</span></span>                |     <span data-ttu-id="dbb25-136">15</span><span class="sxs-lookup"><span data-stu-id="dbb25-136">15</span></span>                |

<span data-ttu-id="dbb25-137">次の図は、**督促状** ページに表示される表の情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="dbb25-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="dbb25-138">[![督促状の順序の設定](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="dbb25-139">この例で必要な 2 つのパラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="dbb25-140">**貸方転記および取立 \> 設定 \> 売掛金勘定パラメーター** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-141">**回収** タブで、**督促状コードを計算する時に支払とクレジット メモを無視する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="dbb25-142">**次の単位別に督促状を作成** フィールドが **顧客** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="dbb25-143">[![貸方転記取立の売掛金勘定パラメーターの設定](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="dbb25-144">**売掛金勘定 \> 請求書 \> すべての自由書式の請求書** に移動し、**新規** を選択して、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-145">**顧客口座** フィールドで、**US-045** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="dbb25-146">**請求日** フィールドに **1/15/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="dbb25-147">**期日** フィールドに **1/16/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="dbb25-148">**請求明細行** クイック タブの **主勘定** フィールドに **401100** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="dbb25-149">**単価フィールド** に **500.00** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="dbb25-150">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-150">Select **Post**.</span></span>

    <span data-ttu-id="dbb25-151">ここで、顧客に対して 2 つの訂正票を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="dbb25-152">**新規** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-153">**顧客口座** フィールドで、**US-045** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="dbb25-154">**請求日** フィールドに **1/15/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="dbb25-155">**期日** フィールドに **1/16/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="dbb25-156">**請求明細行** クイック タブの **主勘定** フィールドに **401100** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="dbb25-157">**単価** フィールドに **-100.00** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="dbb25-158">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-158">Select **Post**.</span></span>

5. <span data-ttu-id="dbb25-159">手順 4 を繰り返しますが、**単価** フィールドに **-200.00** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="dbb25-160">**売掛金勘定 \> 顧客 \> すべての顧客** に移動し、顧客 **US-045** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="dbb25-161">その後、アクション ウィンドウで **トランザクション \> トランザクション** を選択して、先ほど転記した顧客トランザクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="dbb25-162">[![転記済の顧客トランザクションの確認](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="dbb25-163">ここで、顧客 US-045 の督促状を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="dbb25-164">**貸方転記および取立 \> 督促状 \> 督促状の作成** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-165">**請求書** および **訂正票** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="dbb25-166">既定で、**督促状** フィールドを **顧客別取立** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="dbb25-167">**督促状の日付** フィールドに **1/19/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="dbb25-168">**対象に含めるレコード** クイック タブで、**フィルター** を選択して、**顧客アカウント** フィールドに、顧客 **US-045** を追加します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="dbb25-169">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-169">Select **OK**.</span></span>
    5. <span data-ttu-id="dbb25-170">**OK** を選択して督促状を作成します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="dbb25-171">**貸方転記および取立 \> 督促状 \> 督促状の確認と処理** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-172">この督促状は順序内の最初の督促状であるため、ヘッダーとトランザクション明細行の督促状コードが **督促状 1** になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="dbb25-173">(トランザクション明細行を表示するために、**トランザクション** クイック タブの選択が必要な場合があります。)</span><span class="sxs-lookup"><span data-stu-id="dbb25-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="dbb25-174">[![ヘッダーと明細行に同じ督促状コードが表示されていることを確認する](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="dbb25-175">アクション ペインで、**転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="dbb25-176">**転記日付** フィールドに **1/19/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="dbb25-177">ここで、顧客 US-045 の督促状を再度作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="dbb25-178">**貸方転記および取立 \> 督促状 \> 督促状の作成** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-179">**請求書** および **訂正票** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="dbb25-180">既定で、**督促状** フィールドを **顧客別取立** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="dbb25-181">**督促状の日付** フィールドに **1/23/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="dbb25-182">**対象に含めるレコード** クイック タブで、**フィルター** を選択して、**顧客アカウント** フィールドに、顧客 **US-045** を追加します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="dbb25-183">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-183">Select **OK**.</span></span>
    5. <span data-ttu-id="dbb25-184">**OK** を選択して督促状を作成します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="dbb25-185">**貸方転記および取立 \> 督促状 \> 督促状の確認と処理** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-186">ヘッダーの督促状コードが **督促状 1** になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="dbb25-187">ただし、トランザクション明細行のコードは、**督促状 2** です。</span><span class="sxs-lookup"><span data-stu-id="dbb25-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="dbb25-188">[![ヘッダーと明細行に異なる督促状コードが表示されていることを確認する](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="dbb25-189">**督促状コードを計算する時に支払とクレジット メモを無視する** オプションが **はい** であるため、コードは異なります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="dbb25-190">この督促状を転記しないでください。</span><span class="sxs-lookup"><span data-stu-id="dbb25-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="dbb25-191">**貸方転記および取立 \> 設定 \> 売掛金勘定パラメーター** に移動し、**回収** タブの **督促状コードを計算する時に支払とクレジット メモを無視する** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="dbb25-192">[![督促状コードを計算する時に支払とクレジット メモを無視するオプションをいいえに設定する](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="dbb25-193">ここで、顧客 US-045 の督促状を再度作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="dbb25-194">**貸方転記および取立 \> 督促状 \> 督促状の作成** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbb25-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="dbb25-195">**請求書** および **訂正票** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="dbb25-196">既定で、**督促状** フィールドを **顧客別取立** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb25-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="dbb25-197">**督促状の日付** フィールドに **1/23/2021** と入力します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="dbb25-198">**対象に含めるレコード** クイック タブで、**フィルター** を選択して、**顧客アカウント** フィールドに、顧客 **US-045** を追加します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="dbb25-199">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-199">Select **OK**.</span></span>
    5. <span data-ttu-id="dbb25-200">**OK** を選択して督促状を作成します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="dbb25-201">**貸方転記および取立 \> 督促状 \> 督促状の確認と処理** に移動して、ヘッダーとトランザクション明細行の督促状コードが **督促状 2** になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbb25-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="dbb25-202">[![ヘッダーと明細行に同じ督促状コードを再度表示する](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="dbb25-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="dbb25-203">**督促状コードを計算する時に支払とクレジット メモを無視する** オプションが **いいえ** に設定されているため、両方の場所に同じコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dbb25-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
