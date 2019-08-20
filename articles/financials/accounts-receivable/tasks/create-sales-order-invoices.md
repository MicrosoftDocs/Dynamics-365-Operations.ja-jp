---
title: 販売注文請求書の作成
description: このタスク ガイドでは、販売注文の請求操作について説明します。請求書の結合やバッチ処理も含みます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: ba8e0f02f2d1eb12cecc2c434fbca1e198cddbe9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842956"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="41f45-103">販売注文請求書の作成</span><span class="sxs-lookup"><span data-stu-id="41f45-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41f45-104">このタスク ガイドでは、販売注文の請求操作について説明します。請求書の結合やバッチ処理も含みます。</span><span class="sxs-lookup"><span data-stu-id="41f45-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="41f45-105">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="41f45-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="41f45-106">販売注文から請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="41f45-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="41f45-107">[売掛金勘定] > [注文] > [出荷済で未請求の販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="41f45-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="41f45-108">一覧で販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="41f45-109">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="41f45-110">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-110">Click Invoice.</span></span>
    * <span data-ttu-id="41f45-111">この販売注文に関連付けられる複数の梱包明細があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="41f45-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="41f45-112">この場合、梱包明細番号ではなく <multiple> という表示になります。</span><span class="sxs-lookup"><span data-stu-id="41f45-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="41f45-113">[パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="41f45-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="41f45-114">請求書に転記するには、転記を「オン」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41f45-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="41f45-115">また、転記をオフにし、請求書の印刷のみを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="41f45-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="41f45-116">ただし、請求書のほかに、見積請求書の作成でも同じ操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="41f45-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="41f45-117">このオプションはバッチ ジョブに使用されます。</span><span class="sxs-lookup"><span data-stu-id="41f45-117">This option is used for batch jobs.</span></span> <span data-ttu-id="41f45-118">クエリは、バッチ ジョブの実行時に実行されます。</span><span class="sxs-lookup"><span data-stu-id="41f45-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="41f45-119">[印刷] フィールドで [変更後] を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="41f45-120">[請求書の印刷] に対してオンを選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="41f45-121">印刷管理では、請求書を複数印刷できます。また、請求書を PDF ファイルとして電子メールで送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="41f45-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="41f45-122">[請求金額の印刷] フィールドで [集計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="41f45-123">小切手の与信限度額フィールドで [残高] を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="41f45-124">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="41f45-125">注文を 1 つの請求書に連結します。</span><span class="sxs-lookup"><span data-stu-id="41f45-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="41f45-126">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="41f45-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="41f45-127">未処理請求書が複数ある顧客を検索します。</span><span class="sxs-lookup"><span data-stu-id="41f45-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="41f45-128">未処理販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-128">Select an open sales order.</span></span>
4. <span data-ttu-id="41f45-129">同一の顧客の未処理の販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="41f45-130">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="41f45-131">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-131">Click Invoice.</span></span>
7. <span data-ttu-id="41f45-132">[パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="41f45-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="41f45-133">[数量] フィールドで、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="41f45-134">概要セクションに 2 つの請求書が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="41f45-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="41f45-135">ここでは、それらを 1 つの請求書にマージします。</span><span class="sxs-lookup"><span data-stu-id="41f45-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="41f45-136">[集計更新] フィールドで [請求元仕入先] を選択します。</span><span class="sxs-lookup"><span data-stu-id="41f45-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="41f45-137">調整をクリックすると、販売注文を 1 つの請求書にマージします。</span><span class="sxs-lookup"><span data-stu-id="41f45-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="41f45-138">2 つの販売注文が 1 つの請求書にマージされました。</span><span class="sxs-lookup"><span data-stu-id="41f45-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="41f45-139">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-139">Click Cancel.</span></span>
12. <span data-ttu-id="41f45-140">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="41f45-141">バッチの請求書転記</span><span class="sxs-lookup"><span data-stu-id="41f45-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="41f45-142">[売掛金勘定] > [請求書] > [バッチ請求] > [請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="41f45-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="41f45-143">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-143">Click Select.</span></span>
3. <span data-ttu-id="41f45-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-144">Click OK.</span></span>
4. <span data-ttu-id="41f45-145">[バッチ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-145">Click Batch.</span></span>
5. <span data-ttu-id="41f45-146">バッチ処理を有効にするには [はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="41f45-147">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-147">Click Recurrence.</span></span>
7. <span data-ttu-id="41f45-148">日数の選択</span><span class="sxs-lookup"><span data-stu-id="41f45-148">Select Days</span></span>
8. <span data-ttu-id="41f45-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-149">Click OK.</span></span>
9. <span data-ttu-id="41f45-150">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-150">Click OK.</span></span>
10. <span data-ttu-id="41f45-151">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-151">Click Cancel.</span></span>
11. <span data-ttu-id="41f45-152">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41f45-152">Click Yes.</span></span>

