--- 
title: "自由書式の請求書の作成"
description: "この記事は、自由書式の請求書を作成する方法を示します。"
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
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
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: ja-jp
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="1b364-103">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="1b364-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b364-104">この記事は、自由書式の請求書を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1b364-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="1b364-105">この手順については、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b364-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="1b364-106">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="1b364-106">Create a free text invoice</span></span>

1. <span data-ttu-id="1b364-107">[売掛金勘定] > [請求書] > [すべての自由書式の請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1b364-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="1b364-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-108">Click New.</span></span>
3. <span data-ttu-id="1b364-109">[顧客口座] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b364-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="1b364-110">請求先/元 ID は、既定では、顧客口座に使用される口座と同じになります。</span><span class="sxs-lookup"><span data-stu-id="1b364-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="1b364-111">請求書が転記されていない場合、勘定状態は [処理中] から始まります。</span><span class="sxs-lookup"><span data-stu-id="1b364-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="1b364-112">請求書番号は、請求書の転記時に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1b364-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="1b364-113">SEPA 委任状を使用している場合、口座引落の委任状は、顧客口座の選択時に自動的に委任状から作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b364-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="1b364-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b364-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1b364-115">主勘定のフィールドに、分析コードなしで勘定番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b364-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="1b364-116">また、主勘定について 1 文字以上を入力し、ルックアップを使用して勘定を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="1b364-117">このガイドの後のほうで、分析コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1b364-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="1b364-118">[明細行の詳細] クイック タブを展開すると、自分の主勘定に分析コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="1b364-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="1b364-119">[財務分析コード行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="1b364-120">分析コードは、選択した明細行のみに有効です。</span><span class="sxs-lookup"><span data-stu-id="1b364-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="1b364-121">売上税グループは、顧客から入力されます。</span><span class="sxs-lookup"><span data-stu-id="1b364-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="1b364-122">顧客に売上税グループがない場合、主勘定の売上税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b364-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="1b364-123">品目の売上税グループは、主勘定から作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b364-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="1b364-124">主勘定に品目売上税グループがない場合、総勘定元帳の売上税パラメーターの品目売上税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b364-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="1b364-125">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b364-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1b364-126">数量はオプションです。</span><span class="sxs-lookup"><span data-stu-id="1b364-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="1b364-127">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b364-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="1b364-128">単価はオプションです。</span><span class="sxs-lookup"><span data-stu-id="1b364-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="1b364-129">金額は、数量に単価を乗じて計算されます。</span><span class="sxs-lookup"><span data-stu-id="1b364-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="1b364-130">ただし、金額を入力してその計算を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="1b364-131">請求書の売上税の計算を表示するには、[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="1b364-132">このページで売上税金額を確認するか、[調整] タブで金額を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="1b364-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-133">Click OK.</span></span>
12. <span data-ttu-id="1b364-134">請求書に手数料を追加するには、[手数料] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="1b364-135">[諸費用コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b364-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="1b364-136">[諸費用金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b364-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="1b364-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1b364-137">Close the page.</span></span>
16. <span data-ttu-id="1b364-138">請求書集計表の詳細および合計を表示するには、[合計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="1b364-139">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-139">Click Close.</span></span>
18. <span data-ttu-id="1b364-140">[転記] をクリックして請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="1b364-140">Click Post to post the invoice.</span></span> <span data-ttu-id="1b364-141">転記する前にキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="1b364-142">請求書の印刷タイミングの変更: [現在] を選択すると、各請求書の更新時に印刷します。[後] を選択すると、すべての請求書を更新した後に印刷します。</span><span class="sxs-lookup"><span data-stu-id="1b364-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="1b364-143">顧客の与信限度額の転記前チェックの方法を変更する場合は、与信限度額のタイプを変更します。</span><span class="sxs-lookup"><span data-stu-id="1b364-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="1b364-144">請求書を印刷する場合、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b364-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="1b364-145">請求書を転記する場合、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b364-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="1b364-146">転記せずに請求書を印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="1b364-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="1b364-148">行のコピー</span><span class="sxs-lookup"><span data-stu-id="1b364-148">Copy lines</span></span>
<span data-ttu-id="1b364-149">自由書式の請求書の明細行をコピーするには、1 つ以上の明細行を選択し、選択した明細行のコピーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b364-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="1b364-150">必要なコピーの数を指定することができ、メモおよび添付ファイルもコピーできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="1b364-151">配分のコピー、または転記時の再作成ができます。</span><span class="sxs-lookup"><span data-stu-id="1b364-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="1b364-152">明細行をコピーした後は、必要に応じて情報を編集できます。</span><span class="sxs-lookup"><span data-stu-id="1b364-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="1b364-153">テンプレートから自由書式の請求書を作成</span><span class="sxs-lookup"><span data-stu-id="1b364-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="1b364-154">テンプレートから自由書式の請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1b364-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="1b364-155">請求書タブのテンプレートから新規を選択する場合、新しい自由書式の請求書のテンプレート名および顧客 ID を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1b364-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="1b364-156">支払条件および顧客からの支払方法などの既定値を選択することができ、またテンプレートに保存されている値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="1b364-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="1b364-157">新しい自由書式の請求書が作成され、その請求書の値を編集することができます。</span><span class="sxs-lookup"><span data-stu-id="1b364-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


