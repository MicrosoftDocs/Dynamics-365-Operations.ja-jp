---
title: 督促状順序の作成
description: このタスク ガイドを使用し、督促状順序を作成します。
author: mikefalkner
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2500bdaa7107c24f7cb95249208b7ac2a2958fed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971556"
---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="6a735-103">督促状順序の作成</span><span class="sxs-lookup"><span data-stu-id="6a735-103">Create a collection letter sequence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a735-104">このタスク ガイドを使用し、督促状順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="6a735-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="6a735-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a735-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6a735-106">ナビゲーション ウィンドウで、**モジュール > クレジットおよびコレクション > 設定 > 督促状順序の設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a735-106">In the Navigation pane, go to **Modules > Credit and collections > Setup > Set up collection letter sequence**.</span></span>
2. <span data-ttu-id="6a735-107">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a735-107">Click **New**.</span></span>
3. <span data-ttu-id="6a735-108">**督促状順序** フィールドに、順序を表す順序 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-108">In the **Collection letter sequence** field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="6a735-109">転記プロファイルを設定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a735-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="6a735-110">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-110">In the **Description** field, type a value.</span></span>  <span data-ttu-id="6a735-111">支払条件はオプションです。</span><span class="sxs-lookup"><span data-stu-id="6a735-111">The terms of payment is optional.</span></span> <span data-ttu-id="6a735-112">値をここに入力した場合、督促状手数料の請求書は、顧客に保存されている支払条件ではなく、これらの支払条件を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a735-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="6a735-113">**督促状コード** フィールドで、送信したい最初の督促状のコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a735-113">In the **Collection letter code** field, select the code for the first collection letter that you want to send.</span></span> <span data-ttu-id="6a735-114">最初の督促状は、請求書の期日、この行の [日] フィールドに支払い猶予期間として入力した値、この行で入力したその他の情報に従って作成されます。</span><span class="sxs-lookup"><span data-stu-id="6a735-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="6a735-115">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-115">In the **Description** field, type a value.</span></span> <span data-ttu-id="6a735-116">手数料の通貨の既定値は、顧客通貨となります。</span><span class="sxs-lookup"><span data-stu-id="6a735-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="6a735-117">この通貨コードは、請求書通貨とは異なります。</span><span class="sxs-lookup"><span data-stu-id="6a735-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="6a735-118">順番で送信される次の督促状を追加するには **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a735-118">Click **Add** to add the next collection letter that will be sent in the sequence.</span></span> <span data-ttu-id="6a735-119">多くの場合、最初の督促状は警告目的のみです。</span><span class="sxs-lookup"><span data-stu-id="6a735-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="6a735-120">必要に応じて手数料を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6a735-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="6a735-121">[督促状コード] フィールドで、順番で送信される次の督促状を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a735-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="6a735-122">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-122">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="6a735-123">**主勘定** フィールドで、手数料に使用される収益勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a735-123">In the **Main account** field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="6a735-124">この督促状の転記時に請求される手数料を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="6a735-125">**品目売上税グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a735-125">In the **Item sales tax group** field, click the drop down button to open the lookup.</span></span> <span data-ttu-id="6a735-126">費用に基づいて売上税を計算する必要がある場合、品目売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a735-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="6a735-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a735-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6a735-128">**最小期限切れ残高** フィールドで、督促状を送信する前に必要な最小期限切れ残高を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-128">In the **Minimum overdue balance** field, enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="6a735-129">**日** フィールドに、支払猶予日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-129">In the **Days** field, enter the number of grace days that you will allow.</span></span> <span data-ttu-id="6a735-130">これは、督促状が生成される期日から数えた日数です。</span><span class="sxs-lookup"><span data-stu-id="6a735-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="6a735-131">計算に使用される期日は、督促状順序における督促状の位置によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6a735-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:</span></span>
    - <span data-ttu-id="6a735-132">督促状 1 の支払猶予期間は請求書の期日に関連しています。</span><span class="sxs-lookup"><span data-stu-id="6a735-132">The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>
    - <span data-ttu-id="6a735-133">督促状 2 以降の支払猶予期間は、売掛金勘定パラメーターのページの、督促状コードの更新フィールドの選択によって、以前の督促状が転記又は印刷される日付と連動しています。</span><span class="sxs-lookup"><span data-stu-id="6a735-133">The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="6a735-134">順番で送信される最後の督促状を追加するには **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a735-134">Click **Add** to add the last collection letter in the sequence.</span></span> <span data-ttu-id="6a735-135">督促状順序の督促状コードは 5 つまで追加できます。</span><span class="sxs-lookup"><span data-stu-id="6a735-135">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="6a735-136">**督促状コード** フィールドで、順番で送信される次の督促状を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a735-136">In the **Collection letter code** field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="6a735-137">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-137">In the **Description** field, type a value.</span></span>
19. <span data-ttu-id="6a735-138">**主勘定** フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a735-138">In the **Main account** field, specify the desired values.</span></span>
20. <span data-ttu-id="6a735-139">**手数料** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-139">In the **Fee in currency** field, enter a number.</span></span>
21. <span data-ttu-id="6a735-140">**品目売上税グループ** フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a735-140">In the **Item sales tax group** field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="6a735-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a735-141">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="6a735-142">**最小期限切れ残高** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-142">In the **Minimum overdue balance** field, enter a number.</span></span>
24. <span data-ttu-id="6a735-143">**日** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-143">In the **Days** field, enter a number.</span></span>
25. <span data-ttu-id="6a735-144">**ブロック** チェック ボックスをオンにすると、顧客の追加配送と請求が停止されます。</span><span class="sxs-lookup"><span data-stu-id="6a735-144">Select the **Block** check box to stop the customer from additional deliveries and invoicing.</span></span> <span data-ttu-id="6a735-145">顧客勘定をブロック解除するには、顧客ページの請求と出荷の保留中フィールドで **いいえ** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="6a735-145">To unblock the account, select **No** in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="6a735-146">**注記** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="6a735-146">Expand the **Note** fastTab.</span></span>
27. <span data-ttu-id="6a735-147">選択した督促状コードの督促状に表示されるテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="6a735-147">Enter the text to appear on the collection letter for the selected collection letter code.</span></span> <span data-ttu-id="6a735-148">メモ ボックスの上部にある [翻訳] メニューを使用して、このテキストを複数の言語に変換できます。</span><span class="sxs-lookup"><span data-stu-id="6a735-148">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  

