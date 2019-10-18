---
title: 自由書式の請求書の作成
description: このトピックでは、自由書式の請求書を作成する方法を説明します。
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178711"
---
# <a name="create-free-text-invoices"></a><span data-ttu-id="1f5c4-103">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="1f5c4-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f5c4-104">このトピックでは、自由書式の請求書を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="1f5c4-105">手順については、**USMF** というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="1f5c4-106">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="1f5c4-106">Create a free text invoice</span></span>

1. <span data-ttu-id="1f5c4-107">**売掛金勘定 \> 請求書 \> すべての自由書式の請求書**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="1f5c4-108">**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-108">Select **New**.</span></span>
3. <span data-ttu-id="1f5c4-109">**顧客口座**フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="1f5c4-110">既定では、顧客口座として選択されている口座は、請求先/元 ID として使用されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="1f5c4-111">請求書が転記されていない場合、勘定状態は**処理中**から始まります。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="1f5c4-112">請求書番号は、請求書の転記時に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="1f5c4-113">単一ユーロ支払地域 (SEPA) 委任状を使用している場合、口座引落の委任状は、顧客口座の選択時に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="1f5c4-114">**説明**フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="1f5c4-115">**主勘定**のフィールドに、分析コードを持たない勘定番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="1f5c4-116">このトピックで後述する分析コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="1f5c4-117">また、主勘定について 1 文字以上を入力し、ルックアップを使用して勘定を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="1f5c4-118">**明細行の詳細**クイック タブを選択して、主勘定に分析コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="1f5c4-119">**財務分析コード行**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="1f5c4-120">分析コードは、選択した明細行のみに有効です。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="1f5c4-121">売上税グループの既定値は、顧客から入力されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="1f5c4-122">顧客に売上税グループがない場合、主勘定の売上税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="1f5c4-123">品目の売上税グループは、主勘定から入力されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="1f5c4-124">主勘定に品目売上税グループがない場合、総勘定元帳の売上税パラメーターで指定された品目売上税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="1f5c4-125">オプション: **数量**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="1f5c4-126">オプション: **単価**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="1f5c4-127">金額は、数量に単価を乗じて計算されます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="1f5c4-128">ただし、金額を入力してその計算を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="1f5c4-129">**売上税**を選択して、請求書について計算される売上税を表示します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="1f5c4-130">このページで売上税金額を確認するか、**調整**タブで金額を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="1f5c4-131"> **OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-131">Select **OK**.</span></span>
12. <span data-ttu-id="1f5c4-132">**手数料**を選択して、請求書に手数料を追加します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="1f5c4-133">**諸費用コード**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="1f5c4-134">**諸費用金額**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="1f5c4-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-135">Close the page.</span></span>
16. <span data-ttu-id="1f5c4-136">**合計**を選択し、請求書集計表の詳細および合計を表示します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="1f5c4-137">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-137">Select **Close**.</span></span>
18. <span data-ttu-id="1f5c4-138">**転記**を選択して請求書を転記します。、</span><span class="sxs-lookup"><span data-stu-id="1f5c4-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="1f5c4-139">実際に転記する前にも、キャンセルする機会があります。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="1f5c4-140">請求書の印刷タイミングを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="1f5c4-141">**現在**を選択して、各請求書の更新時に印刷します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="1f5c4-142">**変更後**を選択して、すべての請求書が更新されてから印刷します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="1f5c4-143">請求書が転記される前に、顧客の与信限度額の検証方法を変更するには、**与信限度額のタイプ**フィールドで値を変更します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="1f5c4-144">請求書を印刷するには、オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="1f5c4-145">請求書を転記するには、オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="1f5c4-146">転記せずに請求書を印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="1f5c4-147"> **OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="1f5c4-148">行のコピー</span><span class="sxs-lookup"><span data-stu-id="1f5c4-148">Copy lines</span></span>
<span data-ttu-id="1f5c4-149">自由書式の請求書の明細行をコピーするには、1 つ以上の明細行を選択し、**選択した明細行のコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="1f5c4-150">必要なコピーの数を指定することができ、メモおよび添付ファイルもコピーできます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="1f5c4-151">配分のコピー、または転記時の再作成ができます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="1f5c4-152">明細行をコピーした後は、必要に応じて情報を編集できます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="1f5c4-153">テンプレートから自由書式の請求書を作成</span><span class="sxs-lookup"><span data-stu-id="1f5c4-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="1f5c4-154">テンプレートから自由書式の請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="1f5c4-155">**請求書**タブの**新しいコピー元テンプレート**を選択する場合、新しい自由書式の請求書のテンプレート名および顧客 ID を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="1f5c4-156">支払条件および顧客からの支払方法などの既定値は、顧客から自動的に入力したり、またはテンプレートに保存されている値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="1f5c4-157">新しい自由書式の請求書が作成され、必要に応じてその値を編集することができます。</span><span class="sxs-lookup"><span data-stu-id="1f5c4-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
