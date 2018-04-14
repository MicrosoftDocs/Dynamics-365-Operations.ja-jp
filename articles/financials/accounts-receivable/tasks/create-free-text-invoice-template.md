--- 
title: "自由書式の請求書テンプレートの作成"
description: "このレコードでは、USMF デモ会社を使用します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d785922d1c6775d95ad5697eb6a872434e59c8e4
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="b273f-103">自由書式の請求書テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="b273f-103">Create a free text invoice template</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b273f-104">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b273f-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="b273f-105">記録は A/R の請求書の管理および処理を担当するユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="b273f-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="b273f-106">[売掛金勘定] > [請求書] > [定期請求書] > [自由書式の請求書テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b273f-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="b273f-107">請求明細行、請求金、勘定の配分テンプレート、および勘定科目の情報を記載できる自由書式の請求書テンプレートを作成するためには、このフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="b273f-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="b273f-108">[新規] をクリックし、新しい自由書式の請求書テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="b273f-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="b273f-109">[テンプレート名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b273f-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="b273f-110">「テンプレート名」によって自由書式の請求書テンプレートを個別に識別します。</span><span class="sxs-lookup"><span data-stu-id="b273f-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="b273f-111">同じ「テンプレート名」を持つテンプレートを 2 つ以上設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="b273f-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="b273f-112">[説明] フィールドにテンプレートの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b273f-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="b273f-113">請求明細行タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b273f-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="b273f-114">[説明] フィールドに、請求明細行の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b273f-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="b273f-115">[主勘定] フィールドで、収益勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="b273f-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="b273f-116">顧客転記プロファイル ページにある請求合計額に対応する顧客貸方の相殺トランザクション勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="b273f-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="b273f-117">[売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b273f-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b273f-118">現在の請求明細行の売上税グループは、顧客勘定の既定売上税グループです。</span><span class="sxs-lookup"><span data-stu-id="b273f-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="b273f-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b273f-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b273f-120">[品目別税金グループ] フィールドで、現在の請求明細行の品目売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b273f-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="b273f-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b273f-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b273f-122">[単価] フィールドで、請求明細行の単位あたりの価格を入力または表示します。</span><span class="sxs-lookup"><span data-stu-id="b273f-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="b273f-123">この金額は [単価] フィールドによって加算され、請求明細行の金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="b273f-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="b273f-124">自由書式の請求書のテンプレートに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b273f-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="b273f-125">[説明] フィールドに、請求明細行の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b273f-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="b273f-126">[主勘定] フィールドで、収益勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="b273f-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="b273f-127">顧客転記プロファイル ページにある請求合計額に対応する顧客貸方の相殺トランザクション勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="b273f-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="b273f-128">[売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b273f-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b273f-129">現在の請求明細行の売上税グループは、顧客勘定の既定売上税グループです。</span><span class="sxs-lookup"><span data-stu-id="b273f-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="b273f-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b273f-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b273f-131">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b273f-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b273f-132">現在の請求明細行の品目消費税グループ。</span><span class="sxs-lookup"><span data-stu-id="b273f-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="b273f-133">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b273f-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="b273f-134">請求明細行の単位数を入力または表示します。</span><span class="sxs-lookup"><span data-stu-id="b273f-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="b273f-135">この数は [単価] フィールドの値によって加算され、請求明細行の金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="b273f-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="b273f-136">請求明細行の単位あたりの価格を入力または表示します。</span><span class="sxs-lookup"><span data-stu-id="b273f-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="b273f-137">この金額は [単価] フィールドの値によって加算され、請求明細行の金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="b273f-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="b273f-138">明細行と子行の勘定配布を表示および変更します。</span><span class="sxs-lookup"><span data-stu-id="b273f-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="b273f-139">勘定配布は収益、税金、雑費などの金額がどのように自由書式の請求書に計上されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="b273f-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="b273f-140">選択した請求明細行の勘定配布を更新します。</span><span class="sxs-lookup"><span data-stu-id="b273f-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="b273f-141">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b273f-141">Click Close.</span></span>


