---
title: 自由書式の請求書テンプレートの作成
description: この手順は、自由書式の請求書テンプレートを作成する方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee4fff7b148396faecef899c7a75365d3e1f47f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991168"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="bdf05-103">自由書式の請求書テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="bdf05-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdf05-104">このチュートリアルでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="bdf05-105">この手順は A/R 請求書の管理および処理を担当するユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="bdf05-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="bdf05-106">テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="bdf05-106">Create a template</span></span>

1. <span data-ttu-id="bdf05-107">[売掛金勘定] > [請求書] > [定期請求書] > [自由書式の請求書テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="bdf05-108">請求明細行、請求金、勘定の配分テンプレート、および勘定科目の情報を記載できる自由書式の請求書テンプレートを作成するためには、このフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="bdf05-109">[新規] をクリックし、新しい自由書式の請求書テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="bdf05-110">[テンプレート名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="bdf05-111">「テンプレート名」によって自由書式の請求書テンプレートを個別に識別します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="bdf05-112">同じ「テンプレート名」を持つテンプレートを 2 つ以上設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="bdf05-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="bdf05-113">[説明] フィールドにテンプレートの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="bdf05-114">請求明細行タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="bdf05-115">[説明] フィールドに、請求明細行の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="bdf05-116">[主勘定] フィールドで、収益勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="bdf05-117">顧客転記プロファイル ページにある請求合計額に対応する顧客貸方の相殺トランザクション勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="bdf05-118">[売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bdf05-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bdf05-119">現在の請求明細行の売上税グループは、顧客勘定の既定売上税グループです。</span><span class="sxs-lookup"><span data-stu-id="bdf05-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="bdf05-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdf05-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bdf05-121">[品目別税金グループ] フィールドで、現在の請求明細行の品目売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="bdf05-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdf05-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="bdf05-123">[単価] フィールドで、請求明細行の単位あたりの価格を入力または表示します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="bdf05-124">この金額は [単価] フィールドによって加算され、請求明細行の金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="bdf05-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="bdf05-125">自由書式の請求書のテンプレートに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="bdf05-126">[説明] フィールドに、請求明細行の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="bdf05-127">[主勘定] フィールドで、収益勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="bdf05-128">顧客転記プロファイル ページにある請求合計額に対応する顧客貸方の相殺トランザクション勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="bdf05-129">[売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bdf05-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bdf05-130">現在の請求明細行の売上税グループは、顧客勘定の既定売上税グループです。</span><span class="sxs-lookup"><span data-stu-id="bdf05-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="bdf05-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdf05-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="bdf05-132">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bdf05-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bdf05-133">現在の請求明細行の品目消費税グループ。</span><span class="sxs-lookup"><span data-stu-id="bdf05-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="bdf05-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdf05-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="bdf05-135">請求明細行の単位数を入力または表示します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="bdf05-136">この数は [単価] フィールドの値によって加算され、請求明細行の金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="bdf05-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="bdf05-137">請求明細行の単位あたりの価格を入力または表示します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="bdf05-138">この金額は [単価] フィールドの値によって加算され、請求明細行の金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="bdf05-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="bdf05-139">明細行と子行の勘定配布を表示および変更します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="bdf05-140">勘定配布は収益、税金、雑費などの金額がどのように自由書式の請求書に計上されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="bdf05-141">選択した請求明細行の勘定配布を更新します。</span><span class="sxs-lookup"><span data-stu-id="bdf05-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="bdf05-142">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdf05-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="bdf05-143">自由書式の請求書をテンプレートとして保存</span><span class="sxs-lookup"><span data-stu-id="bdf05-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="bdf05-144">既存の自由書式の請求書をテンプレートとして保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="bdf05-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="bdf05-145">請求書タブからテンプレートに保存を選択する場合、テンプレートの名前および説明を指定してください。</span><span class="sxs-lookup"><span data-stu-id="bdf05-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="bdf05-146">その名前のテンプレートが既に存在する場合、同じ名前のテンプレートが既に存在しているという通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bdf05-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="bdf05-147">OK をクリックして置き換えることもできます。</span><span class="sxs-lookup"><span data-stu-id="bdf05-147">You can still click on Ok to replace it.</span></span> 
