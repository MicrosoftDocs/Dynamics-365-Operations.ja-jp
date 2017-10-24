--- 
title: "自由書式の請求書の作成"
description: "このタスク ガイドでは、自由書式の請求書の作成について説明します。"
author: mikefalkner
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
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="70d81-103">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="70d81-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70d81-104">このタスク ガイドでは、自由書式の請求書の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="70d81-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="70d81-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="70d81-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="70d81-106">[売掛金勘定] > [請求書] > [すべての自由書式の請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="70d81-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="70d81-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-107">Click New.</span></span>
3. <span data-ttu-id="70d81-108">[顧客口座] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="70d81-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="70d81-109">請求先/元 ID は、既定では、顧客口座に使用される口座と同じになります。</span><span class="sxs-lookup"><span data-stu-id="70d81-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="70d81-110">請求書が転記されていない場合、勘定状態は [処理中] から始まります。</span><span class="sxs-lookup"><span data-stu-id="70d81-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="70d81-111">請求書番号は、請求書の転記時に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="70d81-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="70d81-112">SEPA 委任状を使用している場合、口座引落の委任状は、顧客口座の選択時に自動的に委任状から作成されます。</span><span class="sxs-lookup"><span data-stu-id="70d81-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="70d81-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70d81-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="70d81-114">主勘定のフィールドに、分析コードなしで勘定番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="70d81-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="70d81-115">また、主勘定について 1 文字以上を入力し、ルックアップを使用して勘定を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="70d81-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="70d81-116">このガイドの後のほうで、分析コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="70d81-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="70d81-117">[明細行の詳細] クイック タブを展開すると、自分の主勘定に分析コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="70d81-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="70d81-118">[財務分析コード行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="70d81-119">分析コードは、選択した明細行のみに有効です。</span><span class="sxs-lookup"><span data-stu-id="70d81-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="70d81-120">売上税グループは、顧客から入力されます。</span><span class="sxs-lookup"><span data-stu-id="70d81-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="70d81-121">顧客に売上税グループがない場合、主勘定の売上税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="70d81-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="70d81-122">品目の売上税グループは、主勘定から作成されます。</span><span class="sxs-lookup"><span data-stu-id="70d81-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="70d81-123">主勘定に品目売上税グループがない場合、総勘定元帳の売上税パラメーターの品目売上税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="70d81-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="70d81-124">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70d81-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="70d81-125">数量はオプションです。</span><span class="sxs-lookup"><span data-stu-id="70d81-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="70d81-126">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70d81-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="70d81-127">単価はオプションです。</span><span class="sxs-lookup"><span data-stu-id="70d81-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="70d81-128">金額は、数量に単価を乗じて計算されます。</span><span class="sxs-lookup"><span data-stu-id="70d81-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="70d81-129">ただし、金額を入力してその計算を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="70d81-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="70d81-130">請求書の売上税の計算を表示するには、[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="70d81-131">このページで売上税金額を確認するか、[調整] タブで金額を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="70d81-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="70d81-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-132">Click OK.</span></span>
12. <span data-ttu-id="70d81-133">請求書に手数料を追加するには、[手数料] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="70d81-134">[諸費用コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70d81-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="70d81-135">[諸費用金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70d81-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="70d81-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="70d81-136">Close the page.</span></span>
16. <span data-ttu-id="70d81-137">請求書集計表の詳細および合計を表示するには、[合計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="70d81-138">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-138">Click Close.</span></span>
18. <span data-ttu-id="70d81-139">[転記] をクリックして請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="70d81-139">Click Post to post the invoice.</span></span> <span data-ttu-id="70d81-140">転記する前にキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="70d81-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="70d81-141">請求書の印刷タイミングの変更: [現在] を選択すると、各請求書の更新時に印刷します。[後] を選択すると、すべての請求書を更新した後に印刷します。</span><span class="sxs-lookup"><span data-stu-id="70d81-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="70d81-142">顧客の与信限度額の転記前チェックの方法を変更する場合は、与信限度額のタイプを変更します。</span><span class="sxs-lookup"><span data-stu-id="70d81-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="70d81-143">請求書を印刷する場合、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="70d81-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="70d81-144">請求書を転記する場合、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="70d81-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="70d81-145">転記せずに請求書を印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="70d81-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="70d81-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70d81-146">Click OK.</span></span>


