---
title: テンプレートを使用した仕訳入力の作成
description: 転記済みの仕訳帳伝票は伝票テンプレートとして保存され、新しい仕訳伝票に適用できます。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a749740b62e39202d502a112f947679f85ca085
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562508"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="69501-103">テンプレートを使用した仕訳入力の作成</span><span class="sxs-lookup"><span data-stu-id="69501-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69501-104">転記済みの仕訳帳伝票は伝票テンプレートとして保存され、新しい仕訳伝票に適用できます。</span><span class="sxs-lookup"><span data-stu-id="69501-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="69501-105">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="69501-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="69501-106">[総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="69501-106">General ledger > Journal entries > General journals.</span></span> <span data-ttu-id="69501-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-107">Click New.</span></span>
    * <span data-ttu-id="69501-108">この手順は、仕訳伝票の作成および転記によって開始されますが、以前に転記された仕訳伝票をテンプレートとして保存できます。</span><span class="sxs-lookup"><span data-stu-id="69501-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
2. <span data-ttu-id="69501-109">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="69501-109">In the Name field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="69501-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="69501-110">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="69501-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="69501-112">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-112">Click Lines.</span></span>
6. <span data-ttu-id="69501-113">勘定タイプの勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-113">Enter an account for the Account type.</span></span>
7. <span data-ttu-id="69501-114">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-114">In the Description field, type a value.</span></span>
8. <span data-ttu-id="69501-115">[借方] フィールドに、金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-115">Enter an amount in the Debit field.</span></span>
9. <span data-ttu-id="69501-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-116">Click New.</span></span>
10. <span data-ttu-id="69501-117">異なるタイプの勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-117">Enter a different account for the Account type.</span></span>
11. <span data-ttu-id="69501-118">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-118">In the Description field, type a value.</span></span>
12. <span data-ttu-id="69501-119">[借方] フィールドに、金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-119">Enter an amount in the Debit field.</span></span>
13. <span data-ttu-id="69501-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-120">Click New.</span></span>
14. <span data-ttu-id="69501-121">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="69501-121">In the Account field, specify the desired values.</span></span>
15. <span data-ttu-id="69501-122">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-122">In the Description field, type a value.</span></span>
16. <span data-ttu-id="69501-123">伝票の収支を合わせるために [貸方] フィールドに金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-123">Enter an amount in the Credit field to balance the voucher.</span></span>
17. <span data-ttu-id="69501-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-124">Click Post.</span></span>
18. <span data-ttu-id="69501-125">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-125">Click Functions.</span></span>
19. <span data-ttu-id="69501-126">[伝票テンプレートの保存] をクリックする</span><span class="sxs-lookup"><span data-stu-id="69501-126">Click Save voucher template.</span></span>
20. <span data-ttu-id="69501-127">この手順は、パーセント テンプレート タイプとします。</span><span class="sxs-lookup"><span data-stu-id="69501-127">This procedure assumes a Percent Template type.</span></span> <span data-ttu-id="69501-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-128">Click OK.</span></span>
    * <span data-ttu-id="69501-129">• 割合: 伝票の金額が比率係数に変換されるため、伝票テンプレートが選択されている場合に、全ての金額が適用可能となります。</span><span class="sxs-lookup"><span data-stu-id="69501-129">• Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>  <span data-ttu-id="69501-130">• 金額: 実際の金額は保存され、適用されます。</span><span class="sxs-lookup"><span data-stu-id="69501-130">• Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="69501-131">[一般仕訳帳] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-131">Click General journals.</span></span>
22. <span data-ttu-id="69501-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-132">Click New.</span></span>
23. <span data-ttu-id="69501-133">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="69501-133">In the Name field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="69501-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="69501-135">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-135">Click Lines.</span></span>
26. <span data-ttu-id="69501-136">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-136">Click Functions.</span></span>
27. <span data-ttu-id="69501-137">[伝票テンプレートの選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-137">Click Select voucher template.</span></span>
28. <span data-ttu-id="69501-138">先ほど作成したテンプレートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="69501-138">Find the template that you created earlier.</span></span> <span data-ttu-id="69501-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-139">Click OK.</span></span>
    * <span data-ttu-id="69501-140">[前のステップ] をクリックし、他のテンプレートが見つかる場合、適切なテンプレートを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69501-140">You may need to click Previous step and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="69501-141">[金額] フィールドに、伝票に適用する金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="69501-141">In the Amount field, enter the amount to be applied to the voucher.</span></span>
    * <span data-ttu-id="69501-142">伝票テンプレートが [割合] タイプ場合にのみ、金額フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="69501-142">The amount field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="69501-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69501-143">Click OK.</span></span>

