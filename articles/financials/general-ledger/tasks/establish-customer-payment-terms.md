--- 
title: "顧客支払条件の設定"
description: "この手順では、現金割引と期日の設定を定義します。"
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e8b4a8f304f8d4b7323b1432413e183df74060eb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="2a917-103">顧客支払条件の設定</span><span class="sxs-lookup"><span data-stu-id="2a917-103">Establish customer payment terms</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a917-104">この手順では、現金割引と期日の設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="2a917-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="2a917-105">このタスク ガイドでは、デモ会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a917-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="2a917-106">[売掛金勘定] > [支払設定] > [支払期日] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a917-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="2a917-107">支払条件の設定は、売掛金勘定または買掛金勘定で共有されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="2a917-108">モジュールでそれを定義した場合、他のモジュールでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a917-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="2a917-109">このタスク ガイドでは、売掛金勘定に基づいてすべての支払条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="2a917-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="2a917-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a917-110">Click New.</span></span>
    * <span data-ttu-id="2a917-111">支払条件が、特定の曜日 (火曜日、月曜日など) または月の特定の日付 (5 日目、10 日目など) と規定されている場合、支払期日を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a917-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="2a917-112">[支払期日] フィールドに、支払期日の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="2a917-113">[説明] フィールドに、支払期日の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="2a917-114">[週]/[月] フィールドで、週または月を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="2a917-115">月曜日など曜日を入力する場合は、「週」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="2a917-116">10 日など月内の日付を入力する場合、月を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="2a917-117">この例の場合、[月] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="2a917-118">[月の日付] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="2a917-119">日付は、「10 日」ではなく、「10」などの数値を入力してください。</span><span class="sxs-lookup"><span data-stu-id="2a917-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="2a917-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a917-120">Click Save.</span></span>
8. <span data-ttu-id="2a917-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2a917-121">Close the page.</span></span>
9. <span data-ttu-id="2a917-122">[売掛金勘定] > [支払設定] > [支払条件] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a917-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="2a917-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a917-123">Click New.</span></span>
    * <span data-ttu-id="2a917-124">支払条件は期日を計算する方法を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="2a917-125">現金割引日の設定は個別のページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="2a917-126">[支払条件] フィールドに、支払条件の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="2a917-127">[説明] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="2a917-128">代金引換払い (COD)、正味、当月などの支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="2a917-129">支払方法は期日計算の開始方法を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="2a917-130">たとえば、期日が常に請求日後から一定の日数または月数を数えた日付である場合、正味が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="2a917-131">代金引換払 (COD) は、支払が請求書に必要な時に使用され、期日は計算されません。</span><span class="sxs-lookup"><span data-stu-id="2a917-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="2a917-132">このタスク ガイドの [現在の月] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="2a917-133">特定の曜日または日付を計算に含める場合は支払期日を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="2a917-134">支払条件によって、月単位または日単位で数量を入力できます。</span><span class="sxs-lookup"><span data-stu-id="2a917-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="2a917-135">または支払スケジュールまたは支払期日を使用して、支払方法の終了時点で「追加」します。</span><span class="sxs-lookup"><span data-stu-id="2a917-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="2a917-136">期日が常に翌月の 10 日目になる場合、10 日の支払期日を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="2a917-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a917-137">Click Save.</span></span>
16. <span data-ttu-id="2a917-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2a917-138">Close the page.</span></span>
17. <span data-ttu-id="2a917-139">[売掛金勘定] > [支払設定] > [現金割引] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a917-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="2a917-140">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a917-140">Click New.</span></span>
    * <span data-ttu-id="2a917-141">このページは現金割引日を計算する方法を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="2a917-142">[現金割引] フィールドに、現金割引の IDを入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="2a917-143">[説明] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="2a917-144">階層化された現金割引が使用できる場合は、この新しい現金割引の後に、該当する次の割引コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="2a917-145">現金割引日を計算するのに使用される日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-145">Enter the number of days used to calculate the cash discount date.</span></span>
    * <span data-ttu-id="2a917-146">正味原則をオンにすると、日数が請求日に追加され、現金割引日が計算されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="2a917-147">現金割引率 (%) を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="2a917-148">現金割引が転記される顧客請求書用の主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="2a917-149">[割引の相手勘定] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="2a917-150">「請求明細行の勘定」を選択した場合、現金割引は、仕入先請求書明細行の同じ資産/経費用主勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="2a917-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="2a917-151">「仕入先請求書用に主勘定を使用する」を選択した場合、現金割引は、「仕入先請求書用主勘定」に定義する主勘定に転記されるようになります。</span><span class="sxs-lookup"><span data-stu-id="2a917-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="2a917-152">この例では、「仕入先請求書用に主勘定を使用する」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a917-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="2a917-153">現金割引が転記される仕入先請求書用の主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a917-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="2a917-154">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a917-154">Click Save.</span></span>


