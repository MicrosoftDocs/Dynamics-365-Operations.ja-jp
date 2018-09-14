--- 
title: "督促状順序の作成"
description: "このタスク ガイドを使用し、督促状順序を作成します。"
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="63fd0-103">督促状順序の作成</span><span class="sxs-lookup"><span data-stu-id="63fd0-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63fd0-104">このタスク ガイドを使用し、督促状順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="63fd0-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="63fd0-106">[貸方転記および取立] > [設定] > [督促状の順序の設定] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="63fd0-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63fd0-107">Click New.</span></span>
3. <span data-ttu-id="63fd0-108">[督促状順序] フィールドに、順序を表す順序 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="63fd0-109">転記プロファイルを設定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="63fd0-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="63fd0-111">支払条件はオプションです。</span><span class="sxs-lookup"><span data-stu-id="63fd0-111">The terms of payment is optional.</span></span> <span data-ttu-id="63fd0-112">値をここに入力した場合、督促状手数料の請求書は、顧客に保存されている支払条件ではなく、これらの支払条件を使用します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="63fd0-113">[督促状コード] フィールドで、送信したい最初の督促状のコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="63fd0-114">最初の督促状は、請求書の期日、この行の [日] フィールドに支払い猶予期間として入力した値、この行で入力したその他の情報に従って作成されます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="63fd0-115">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="63fd0-116">手数料の通貨の既定値は、顧客通貨となります。</span><span class="sxs-lookup"><span data-stu-id="63fd0-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="63fd0-117">この通貨コードは、請求書通貨とは異なります。</span><span class="sxs-lookup"><span data-stu-id="63fd0-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="63fd0-118">順番で送信される次の督促状を追加するには [追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63fd0-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="63fd0-119">多くの場合、最初の督促状は警告目的のみです。</span><span class="sxs-lookup"><span data-stu-id="63fd0-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="63fd0-120">必要に応じて手数料を追加できます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="63fd0-121">[督促状コード] フィールドで、順番で送信される次の督促状を選択します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="63fd0-122">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="63fd0-123">主勘定のフィールドで、手数料に使用される収益勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="63fd0-124">この督促状の転記時に請求される手数料を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="63fd0-125">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="63fd0-126">費用に基づいて売上税を計算する必要がある場合、品目売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="63fd0-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="63fd0-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="63fd0-128">督促状を送信する前に必要な最小期限切れ残高を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="63fd0-129">支払猶予日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="63fd0-130">これは、督促状が生成される期日から数えた日数です。</span><span class="sxs-lookup"><span data-stu-id="63fd0-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="63fd0-131">計算に使用される期日は、督促状順序における督促状の位置によって異なります:   ⦁    督促状 1 の支払猶予期間は請求書の期日に関連しています。</span><span class="sxs-lookup"><span data-stu-id="63fd0-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="63fd0-132">⦁ 督促状 2 以降の支払猶予期間は、売掛金勘定パラメータのページの [督促状コードの更新] フィールドの選択によって、以前の督促状が転記又は印刷される日付と連動しています。</span><span class="sxs-lookup"><span data-stu-id="63fd0-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="63fd0-133">順番で送信される最後の督促状を追加するには [追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63fd0-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="63fd0-134">督促状順序の督促状コードは 5 つまで追加できます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="63fd0-135">[督促状コード] フィールドで、順番で送信される次の督促状を選択します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="63fd0-136">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="63fd0-137">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="63fd0-138">[手数料] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="63fd0-139">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="63fd0-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="63fd0-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="63fd0-141">[最小期限切れ残高] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="63fd0-142">[日] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="63fd0-143">このチェック ボックスをオンにすると、顧客の追加配送と請求が停止されます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="63fd0-144">顧客勘定をブロック解除するには、[顧客] ページの請求と出荷の保留中フィールドで [いいえ] を選択してください。</span><span class="sxs-lookup"><span data-stu-id="63fd0-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="63fd0-145">クイック タブの [注記] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="63fd0-146">選択した督促状コードの督促状に表示されるテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="63fd0-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="63fd0-147">メモ ボックスの上部にある [翻訳] メニューを使用して、このテキストを複数の言語に変換できます。</span><span class="sxs-lookup"><span data-stu-id="63fd0-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


