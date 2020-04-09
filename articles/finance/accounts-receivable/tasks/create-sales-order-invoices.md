---
title: 販売注文請求書の作成
description: このタスク ガイドでは、販売注文の請求操作について説明します。請求書の結合やバッチ処理も含みます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c504ef36f61613c7aa7db5a1e5ddba6e69cd7285
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140276"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="248cf-103">販売注文請求書の作成</span><span class="sxs-lookup"><span data-stu-id="248cf-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="248cf-104">このタスク ガイドでは、販売注文の請求操作について説明します。請求書の結合やバッチ処理も含みます。</span><span class="sxs-lookup"><span data-stu-id="248cf-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="248cf-105">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="248cf-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="248cf-106">販売注文から請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="248cf-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="248cf-107">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > 出荷済で未請求の販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="248cf-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="248cf-108">一覧で販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="248cf-109">**アクション ウィンドウ**で、**請求書 > 生成 > 請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="248cf-110">この販売注文に関連付けられる複数の梱包明細があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="248cf-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="248cf-111">この場合、梱包明細番号ではなく <multiple> という表示になります。</span><span class="sxs-lookup"><span data-stu-id="248cf-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="248cf-112">**パラメーター** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="248cf-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="248cf-113">請求書に転記するには、転記を「オン」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="248cf-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="248cf-114">また、転記をオフにし、請求書の印刷のみを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="248cf-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="248cf-115">ただし、請求書のほかに、見積請求書の作成でも同じ操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="248cf-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="248cf-116">このオプションはバッチ ジョブに使用されます。</span><span class="sxs-lookup"><span data-stu-id="248cf-116">This option is used for batch jobs.</span></span> <span data-ttu-id="248cf-117">クエリは、バッチ ジョブの実行時に実行されます。</span><span class="sxs-lookup"><span data-stu-id="248cf-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="248cf-118">**印刷**フィールドで、「変更後」を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="248cf-119">**請求書の印刷**に対して**オン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="248cf-120">印刷管理では、請求書を複数印刷できます。また、請求書を PDF ファイルとして電子メールで送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="248cf-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="248cf-121">**請求金額の印刷**フィールドで、「集計」を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="248cf-122">**小切手の与信限度額**フィールドで、「残高」を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="248cf-123">**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="248cf-124">注文を 1 つの請求書に連結します。</span><span class="sxs-lookup"><span data-stu-id="248cf-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="248cf-125">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="248cf-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="248cf-126">未処理請求書が複数ある顧客を検索します。</span><span class="sxs-lookup"><span data-stu-id="248cf-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="248cf-127">同じ顧客からの複数の未処理販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="248cf-128">**アクション ウィンドウ**で、**請求書 > 生成 > 請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="248cf-129">**パラメーター** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="248cf-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="248cf-130">**数量**フィールドで「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="248cf-131">概要セクションに 2 つの請求書が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="248cf-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="248cf-132">ここでは、それらを 1 つの請求書にマージします。</span><span class="sxs-lookup"><span data-stu-id="248cf-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="248cf-133">**集計更新**フィールドで、「請求元仕入先」を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="248cf-134">**調整**をクリックすると、販売注文を 1 つの請求書にマージします。</span><span class="sxs-lookup"><span data-stu-id="248cf-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="248cf-135">2 つの販売注文が 1 つの請求書にマージされました。</span><span class="sxs-lookup"><span data-stu-id="248cf-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="248cf-136">**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="248cf-137">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="248cf-138">バッチの請求書転記</span><span class="sxs-lookup"><span data-stu-id="248cf-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="248cf-139">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 請求書 > バッチ請求 > 請求書**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="248cf-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="248cf-140">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-140">Click **Select**.</span></span>
3. <span data-ttu-id="248cf-141">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-141">Click **OK**.</span></span>
4. <span data-ttu-id="248cf-142">**バッチ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-142">Click **Batch**.</span></span>
5. <span data-ttu-id="248cf-143">**バッチ処理**で、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="248cf-144">**再実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="248cf-145">**日数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="248cf-145">Select **Days**.</span></span>
8. <span data-ttu-id="248cf-146">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-146">Click **OK**.</span></span>
9. <span data-ttu-id="248cf-147">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-147">Click **OK**.</span></span>
10. <span data-ttu-id="248cf-148">**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="248cf-149">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="248cf-149">Click **Yes**.</span></span>

