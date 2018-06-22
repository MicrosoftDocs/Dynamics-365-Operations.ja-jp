---
title: "Retail Modern POS のトリガーと印刷"
description: "トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。"
author: mugunthanm
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 002cb6c25f40d9e1ab737d90f7841d12e4bec570
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="retail-modern-pos-triggers-and-printing"></a><span data-ttu-id="e2d80-103">Retail Modern POS のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="e2d80-103">Retail Modern POS triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2d80-104">トリガーを使用すると、Retail Modern POS の操作前または後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="e2d80-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="e2d80-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="e2d80-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="e2d80-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-108">Continue or cancel an operation.</span></span> <span data-ttu-id="e2d80-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="e2d80-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="e2d80-110">Post-triggers are not cancelable.</span></span> 
- <span data-ttu-id="e2d80-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 

<span data-ttu-id="e2d80-112">このトピックは、プラットフォーム更新プログラム 8 および Retail アプリケーション更新プログラム 4 修正プログラムを備えた、Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-112">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="e2d80-113">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="e2d80-113">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="e2d80-114">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-114">Application triggers</span></span>

| <span data-ttu-id="e2d80-115">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-115">Trigger</span></span>                   | <span data-ttu-id="e2d80-116">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-116">Type</span></span>           | <span data-ttu-id="e2d80-117">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-117">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="e2d80-118">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-118">ApplicationStartTrigger</span></span>   | <span data-ttu-id="e2d80-119">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-119">Non-cancelable</span></span> | <span data-ttu-id="e2d80-120">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-120">Executed after the POS application is started.</span></span> <span data-ttu-id="e2d80-121">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-121">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="e2d80-122">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-122">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="e2d80-123">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-123">Non-cancelable</span></span> | <span data-ttu-id="e2d80-124">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-124">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="e2d80-125">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-125">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="e2d80-126">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-126">Cancelable</span></span>     | <span data-ttu-id="e2d80-127">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-127">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="e2d80-128">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-128">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="e2d80-129">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-129">Non-cancelable</span></span> | <span data-ttu-id="e2d80-130">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-130">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="e2d80-131">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-131">PostLogOffTrigger</span></span>         | <span data-ttu-id="e2d80-132">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-132">Non-cancelable</span></span> | <span data-ttu-id="e2d80-133">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-133">Executed after the POS log off.</span></span>                                                                                                      |

## <a name="cash-nanagement-triggers"></a><span data-ttu-id="e2d80-134">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-134">Cash nanagement triggers</span></span>

| <span data-ttu-id="e2d80-135">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-135">Trigger</span></span>                      | <span data-ttu-id="e2d80-136">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-136">Type</span></span>           | <span data-ttu-id="e2d80-137">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-137">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="e2d80-138">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-138">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="e2d80-139">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-139">Cancelable</span></span>     | <span data-ttu-id="e2d80-140">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-140">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="e2d80-141">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-141">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="e2d80-142">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-142">Non-cancelable</span></span> | <span data-ttu-id="e2d80-143">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-143">Executed after the POS tender declaration.</span></span>  |

## <a name="customer-triggers"></a><span data-ttu-id="e2d80-144">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-144">Customer triggers</span></span>

| <span data-ttu-id="e2d80-145">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-145">Trigger</span></span>                   | <span data-ttu-id="e2d80-146">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-146">Type</span></span>                    | <span data-ttu-id="e2d80-147">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-147">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e2d80-148">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-148">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="e2d80-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-149">Cancelable</span></span>              | <span data-ttu-id="e2d80-150">新しい顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-150">Executed before creating a new customer.</span></span>             |
| <span data-ttu-id="e2d80-151">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-151">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="e2d80-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-152">Non-cancelable</span></span>          | <span data-ttu-id="e2d80-153">新しい顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-153">Executed after creating a new customer.</span></span>              |
| <span data-ttu-id="e2d80-154">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-154">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="e2d80-155">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-155">PreCustomerClearTrigger</span></span> | <span data-ttu-id="e2d80-156">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-156">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="e2d80-157">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-157">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="e2d80-158">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-158">Non-cancelable</span></span>          | <span data-ttu-id="e2d80-159">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-159">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="e2d80-160">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-160">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="e2d80-161">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-161">Cancelable</span></span>              | <span data-ttu-id="e2d80-162">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-162">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="e2d80-163">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-163">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="e2d80-164">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-164">Cancelable</span></span>              | <span data-ttu-id="e2d80-165">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-165">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="e2d80-166">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-166">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="e2d80-167">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-167">Non-cancelable</span></span>          | <span data-ttu-id="e2d80-168">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-168">Executed after customer search is performed.</span></span>       |

## <a name="discount-triggers"></a><span data-ttu-id="e2d80-169">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-169">Discount triggers</span></span>

| <span data-ttu-id="e2d80-170">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-170">Trigger</span></span>                         | <span data-ttu-id="e2d80-171">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-171">Type</span></span>           | <span data-ttu-id="e2d80-172">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-172">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e2d80-173">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-173">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="e2d80-174">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-174">Cancelable</span></span>     | <span data-ttu-id="e2d80-175">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-175">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="e2d80-176">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-176">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="e2d80-177">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-177">Non-cancelable</span></span> | <span data-ttu-id="e2d80-178">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-178">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="e2d80-179">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-179">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="e2d80-180">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-180">Cancelable</span></span>     | <span data-ttu-id="e2d80-181">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-181">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="e2d80-182">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-182">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="e2d80-183">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-183">Non-cancelable</span></span> | <span data-ttu-id="e2d80-184">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-184">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="e2d80-185">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-185">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="e2d80-186">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-186">Cancelable</span></span>     | <span data-ttu-id="e2d80-187">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-187">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="e2d80-188">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-188">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="e2d80-189">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-189">Non-cancelable</span></span> | <span data-ttu-id="e2d80-190">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-190">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="e2d80-191">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-191">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="e2d80-192">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-192">Cancelable</span></span>     | <span data-ttu-id="e2d80-193">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-193">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="e2d80-194">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-194">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="e2d80-195">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-195">Non-cancelable</span></span> | <span data-ttu-id="e2d80-196">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-196">Executed after total discount percent added to the cart.</span></span>        |

## <a name="operation-triggers"></a><span data-ttu-id="e2d80-197">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-197">Operation triggers</span></span>

| <span data-ttu-id="e2d80-198">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-198">Trigger</span></span>              | <span data-ttu-id="e2d80-199">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-199">Type</span></span>           | <span data-ttu-id="e2d80-200">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-200">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="e2d80-201">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-201">PreOperationTrigger</span></span>  | <span data-ttu-id="e2d80-202">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-202">Cancelable</span></span>     | <span data-ttu-id="e2d80-203">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="e2d80-203">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="e2d80-204">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-204">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="e2d80-205">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-205">PostOperationTrigger</span></span> | <span data-ttu-id="e2d80-206">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-206">Non-cancelable</span></span> | <span data-ttu-id="e2d80-207">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="e2d80-207">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="e2d80-208">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-208">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="e2d80-209">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-209">Payment triggers</span></span>

| <span data-ttu-id="e2d80-210">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-210">Trigger</span></span>                 | <span data-ttu-id="e2d80-211">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-211">Type</span></span>           | <span data-ttu-id="e2d80-212">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-212">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="e2d80-213">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-213">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="e2d80-214">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-214">Cancelable</span></span>     | <span data-ttu-id="e2d80-215">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-215">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="e2d80-216">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-216">PrePaymentTrigger</span></span>       | <span data-ttu-id="e2d80-217">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-217">Cancelable</span></span>     | <span data-ttu-id="e2d80-218">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-218">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="e2d80-219">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-219">PostPaymentTrigger</span></span>      | <span data-ttu-id="e2d80-220">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-220">Non-cancelable</span></span> | <span data-ttu-id="e2d80-221">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-221">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="e2d80-222">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-222">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="e2d80-223">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-223">Cancelable</span></span>     | <span data-ttu-id="e2d80-224">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-224">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="e2d80-225">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-225">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="e2d80-226">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-226">Non-cancelable</span></span> | <span data-ttu-id="e2d80-227">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-227">Executed after the payment line is voided in POS.</span></span>   |

<span data-ttu-id="e2d80-228">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-228">Printing Triggers</span></span>

| <span data-ttu-id="e2d80-229">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-229">Trigger</span></span>                    | <span data-ttu-id="e2d80-230">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-230">Type</span></span>       | <span data-ttu-id="e2d80-231">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-231">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="e2d80-232">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-232">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="e2d80-233">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-233">Cancelable</span></span> | <span data-ttu-id="e2d80-234">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-234">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="e2d80-235">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-235">Product triggers</span></span>

| <span data-ttu-id="e2d80-236">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-236">Trigger</span></span>                    | <span data-ttu-id="e2d80-237">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-237">Type</span></span>           | <span data-ttu-id="e2d80-238">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-238">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d80-239">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-239">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="e2d80-240">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-240">Non-cancelable</span></span> | <span data-ttu-id="e2d80-241">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-241">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="e2d80-242">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-242">PreProductSaleTrigger</span></span>      | <span data-ttu-id="e2d80-243">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-243">Cancelable</span></span>     | <span data-ttu-id="e2d80-244">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-244">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="e2d80-245">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-245">PostProductSaleTrigger</span></span>     | <span data-ttu-id="e2d80-246">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-246">Non-cancelable</span></span> | <span data-ttu-id="e2d80-247">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-247">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="e2d80-248">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-248">PreReturnProductTrigger</span></span>    | <span data-ttu-id="e2d80-249">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-249">Cancelable</span></span>     | <span data-ttu-id="e2d80-250">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-250">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="e2d80-251">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-251">PostReturnProductTrigger</span></span>   | <span data-ttu-id="e2d80-252">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-252">Non-cancelable</span></span> | <span data-ttu-id="e2d80-253">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-253">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="e2d80-254">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-254">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="e2d80-255">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-255">Cancelable</span></span>     | <span data-ttu-id="e2d80-256">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-256">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="e2d80-257">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-257">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="e2d80-258">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-258">Non-cancelable</span></span> | <span data-ttu-id="e2d80-259">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-259">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="e2d80-260">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-260">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="e2d80-261">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-261">Cancelable</span></span>     | <span data-ttu-id="e2d80-262">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-262">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="e2d80-263">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-263">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="e2d80-264">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-264">Non-cancelable</span></span> | <span data-ttu-id="e2d80-265">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-265">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="e2d80-266">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-266">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="e2d80-267">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-267">Cancelable</span></span>     | <span data-ttu-id="e2d80-268">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-268">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="e2d80-269">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-269">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="e2d80-270">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-270">Non-cancelable</span></span> | <span data-ttu-id="e2d80-271">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-271">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="e2d80-272">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-272">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="e2d80-273">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-273">Cancelable</span></span>     | <span data-ttu-id="e2d80-274">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-274">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="e2d80-275">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-275">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="e2d80-276">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-276">Non-cancelable</span></span> | <span data-ttu-id="e2d80-277">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-277">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="e2d80-278">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-278">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="e2d80-279">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-279">Non-cancelable</span></span> | <span data-ttu-id="e2d80-280">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-280">Executed after the price check for the product is executed.</span></span>          |

## <a name="shift-triggers"></a><span data-ttu-id="e2d80-281">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-281">Shift triggers</span></span>
<span data-ttu-id="e2d80-282">| トリガー              | タイプ           | 説明                                             ||----------------------|----------------|---------------------------------------------------------| | PostOpenShiftTrigger | キャンセル不可 | 新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-282">| Trigger              | Type           | Description                                             ||----------------------|----------------|---------------------------------------------------------| | PostOpenShiftTrigger | Non-cancelable | Executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="e2d80-283">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-283">Tax override triggers</span></span>

| <span data-ttu-id="e2d80-284">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-284">Trigger</span></span>                           | <span data-ttu-id="e2d80-285">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-285">Type</span></span>           | <span data-ttu-id="e2d80-286">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-286">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="e2d80-287">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-287">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="e2d80-288">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-288">Cancelable</span></span>     | <span data-ttu-id="e2d80-289">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-289">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="e2d80-290">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-290">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="e2d80-291">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-291">Non-cancelable</span></span> | <span data-ttu-id="e2d80-292">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-292">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="e2d80-293">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-293">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="e2d80-294">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-294">Cancelable</span></span>     | <span data-ttu-id="e2d80-295">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-295">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="e2d80-296">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-296">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="e2d80-297">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-297">Non-cancelable</span></span> | <span data-ttu-id="e2d80-298">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-298">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="e2d80-299">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-299">Transaction triggers</span></span>

| <span data-ttu-id="e2d80-300">トリガー</span><span class="sxs-lookup"><span data-stu-id="e2d80-300">Trigger</span></span>                            | <span data-ttu-id="e2d80-301">種類</span><span class="sxs-lookup"><span data-stu-id="e2d80-301">Type</span></span>           | <span data-ttu-id="e2d80-302">説明</span><span class="sxs-lookup"><span data-stu-id="e2d80-302">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="e2d80-303">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-303">BeginTransactionTrigger</span></span>            | <span data-ttu-id="e2d80-304">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-304">Non-cancelable</span></span> | <span data-ttu-id="e2d80-305">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-305">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="e2d80-306">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-306">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="e2d80-307">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-307">Cancelable</span></span>     | <span data-ttu-id="e2d80-308">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-308">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="e2d80-309">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-309">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="e2d80-310">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-310">Cancelable</span></span>     | <span data-ttu-id="e2d80-311">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-311">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="e2d80-312">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-312">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="e2d80-313">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-313">Non-cancelable</span></span> | <span data-ttu-id="e2d80-314">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-314">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="e2d80-315">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-315">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="e2d80-316">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-316">Cancelable</span></span>     | <span data-ttu-id="e2d80-317">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-317">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="e2d80-318">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-318">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="e2d80-319">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-319">Non-cancelable</span></span> | <span data-ttu-id="e2d80-320">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-320">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="e2d80-321">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-321">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="e2d80-322">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-322">Cancelable</span></span>     | <span data-ttu-id="e2d80-323">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-323">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="e2d80-324">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-324">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="e2d80-325">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-325">Non-cancelable</span></span> | <span data-ttu-id="e2d80-326">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-326">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="e2d80-327">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-327">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="e2d80-328">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-328">Cancelable</span></span>     | <span data-ttu-id="e2d80-329">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-329">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="e2d80-330">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-330">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="e2d80-331">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-331">Non-cancelable</span></span> | <span data-ttu-id="e2d80-332">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-332">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="e2d80-333">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-333">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="e2d80-334">解約可能</span><span class="sxs-lookup"><span data-stu-id="e2d80-334">Cancelable</span></span>     | <span data-ttu-id="e2d80-335">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-335">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="e2d80-336">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-336">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="e2d80-337">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-337">Non-cancelable</span></span> | <span data-ttu-id="e2d80-338">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-338">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="e2d80-339">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d80-339">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="e2d80-340">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="e2d80-340">Non-cancelable</span></span> | <span data-ttu-id="e2d80-341">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-341">Executed after the checkout process is completed.</span></span>    |

## <a name="how-to-implement-a-trigger"></a><span data-ttu-id="e2d80-342">トリガーを実装する方法</span><span class="sxs-lookup"><span data-stu-id="e2d80-342">How to implement a trigger</span></span>

<span data-ttu-id="e2d80-343">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-343">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="e2d80-344">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-344">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

1. <span data-ttu-id="e2d80-345">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-345">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="e2d80-346">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-346">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="e2d80-347">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-347">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="e2d80-348">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-348">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="e2d80-349">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-349">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="e2d80-350">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-350">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="e2d80-351">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-351">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="e2d80-352">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-352">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
   ```typescript
    public execute(options: Triggers.IPostSuspendTransactionTriggerOptions): Promise < void> {
        this.context.logger.logVerbose("Executing PostSuspendTransactionTrigger with options " + JSON.stringify(options) + ".");
        if(ObjectExtensions.isNullOrUndefined(options) || ObjectExtensions.isNullOrUndefined(options.cart)) {
           
           // This will never happen, but is included to demonstrate how to return a rejected promise when validation fails.
           
           let error: ClientEntities.ExtensionError
                = new ClientEntities.ExtensionError("The options provided to the PostSuspendTransactionTrigger were invalid.");
            return Promise.reject(error);
        } else {
            return this.context.runtime.executeAsync(new GetHardwareProfileClientRequest())
                .then((response: ClientEntities.ICancelableDataResult<GetHardwareProfileClientResponse>)
                    : Promise<ClientEntities.ICancelableDataResult<GetReceiptsClientResponse>> => {
                    let hardwareProfile: ProxyEntities.HardwareProfile = response.data.result;
                    // Gets the receipts.
                    let salesOrderId: string = options.cart.Id;
                    let receiptRetrievalCriteria: ProxyEntities.ReceiptRetrievalCriteria = {
                        IsCopy: false,
                        IsRemoteTransaction: false,
                        IsPreview: false,
                        QueryBySalesId: true,
                        ReceiptTypeValue: ProxyEntities.ReceiptType.CustomReceipt7,
                        HardwareProfileId: hardwareProfile.ProfileId
                    };
                    let getReceiptsClientRequest: GetReceiptsClientRequest<GetReceiptsClientResponse> =
                        new GetReceiptsClientRequest(salesOrderId, receiptRetrievalCriteria);
                    return this.context.runtime.executeAsync(getReceiptsClientRequest);
                })
                .then((response: ClientEntities.ICancelableDataResult<GetReceiptsClientResponse>)
                    : Promise<ClientEntities.ICancelableDataResult<PrinterPrintResponse>> => {
                    let receipts: ProxyEntities.Receipt[] = response.data.result;
                    // Prints the receipts.
                    let printerPrintRequest: PrinterPrintRequest<PrinterPrintResponse> = new PrinterPrintRequest(receipts);
                    return this.context.runtime.executeAsync(printerPrintRequest);
                }).then((): Promise<void> => {
                    // Resolves to a void result when fulfilled.
                    return Promise.resolve();
                }).catch((reason: any): Promise<void> => {
                    // Resolves to a void result when rejected. This matches existing POS printing behavior.
                    this.context.logger.logError("PostSuspendTransactionTrigger execute error: " + JSON.stringify(reason));
                    return Promise.resolve();
                });
        }
    }
   ```
   <span data-ttu-id="e2d80-353">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e2d80-353">The entire example should look like the following.</span></span>

```typescript
    import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
    import { ObjectExtensions } from "PosApi/TypeExtensions";
    import { ClientEntities, ProxyEntities } from "PosApi/Entities";
    import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
    import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
    import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
    
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger {
    
    /**
        * Executes the trigger functionality.
        * @param {Triggers.IPostSuspendTransactionTriggerOptions} options The options provided to the trigger.
    */
        public execute(options: Triggers.IPostSuspendTransactionTriggerOptions): Promise<void> {
            this.context.logger.logVerbose("Executing PostSuspendTransactionTrigger with options " + JSON.stringify(options) + ".");
            if (ObjectExtensions.isNullOrUndefined(options) || ObjectExtensions.isNullOrUndefined(options.cart)) {
                // This will never happen, but is included to demonstrate how to return a rejected promise when validation fails.
                let error: ClientEntities.ExtensionError
                    = new ClientEntities.ExtensionError("The options provided to the PostSuspendTransactionTrigger were invalid.");
                return Promise.reject(error);
            } else {
                return this.context.runtime.executeAsync(new GetHardwareProfileClientRequest())
                    .then((response: ClientEntities.ICancelableDataResult<GetHardwareProfileClientResponse>)
                        : Promise<ClientEntities.ICancelableDataResult<GetReceiptsClientResponse>> => {
                        let hardwareProfile: ProxyEntities.HardwareProfile = response.data.result;
                        // Gets the receipts.
                        let salesOrderId: string = options.cart.Id;
                        let receiptRetrievalCriteria: ProxyEntities.ReceiptRetrievalCriteria = {
                            IsCopy: false,
                            IsRemoteTransaction: false,
                            IsPreview: false,
                            QueryBySalesId: true,
                            ReceiptTypeValue: ProxyEntities.ReceiptType.CustomReceipt7,
                            HardwareProfileId: hardwareProfile.ProfileId
                        };
                        let getReceiptsClientRequest: GetReceiptsClientRequest<GetReceiptsClientResponse> =
                            new GetReceiptsClientRequest(salesOrderId, receiptRetrievalCriteria);
                        return this.context.runtime.executeAsync(getReceiptsClientRequest);
                    })
                    .then((response: ClientEntities.ICancelableDataResult<GetReceiptsClientResponse>)
                        : Promise<ClientEntities.ICancelableDataResult<PrinterPrintResponse>> => {
                        let receipts: ProxyEntities.Receipt[] = response.data.result;
                        // Prints the receipts.
                        let printerPrintRequest: PrinterPrintRequest<PrinterPrintResponse> = new PrinterPrintRequest(receipts);
                        return this.context.runtime.executeAsync(printerPrintRequest);
                    }).then((): Promise<void> => {
                        // Resolves to a void result when fulfilled.
                        return Promise.resolve();
                    }).catch((reason: any): Promise<void> => {
                        // Resolves to a void result when rejected. This matches existing POS printing behavior.
                        this.context.logger.logError("PostSuspendTransactionTrigger execute error: " + JSON.stringify(reason));
                        return Promise.resolve();
                    });
            }
        }
    }
```
9. <span data-ttu-id="e2d80-354">新しい .json ファイルを **POSAPIExtension** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-354">Create a new .json file under the **POSAPIExtension** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="e2d80-355">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-355">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

```typescript
    {
        "$schema": "../manifestSchema.json",
            "name": "Pos_Extensibility_SuspendTransactionReceiptSample",
                "publisher": "Microsoft",
                    "version": "7.2.0",
                        "minimumPosVersion": "7.2.0.0",
                            "components": {
            "extend": {
                "triggers": [
                    {
                        "triggerType": "PostSuspendTransaction",
                        "modulePath": "TriggersHandlers/PostSuspendTransactionTrigger"
                    }
                ]
            }
        }
    }
```
11. <span data-ttu-id="e2d80-356">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-356">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions2"
            },
            {
                "baseUrl": "SuspendReceiptSample"
            }
        ]
    }
```
12. <span data-ttu-id="e2d80-357">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-357">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="e2d80-358">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-358">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="e2d80-359">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2d80-359">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="e2d80-360">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2d80-360">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

```typescript
    "exclude": [
        "AuditEventExtensionSample",
        "B2BSample",
        "CustomerSearchWithAttributesSample",
        "FiscalRegisterSample",
        "PaymentSample",
        "PromotionsSample",
        "SalesTransactionSignatureSample",
        "SampleExtensions",
        //"SampleExtensions2",
        "StoreHoursSample",
        "SuspendTransactionReceiptSample"
        //"POSAPIExtension",
        //"CustomColumnExtensions",
        //"EODSample",
        //"ProdDetailsCustomColumnExtensions",
        //"SerachExtension",
        //"SuspendReceiptSample"
    ],
```
13. <span data-ttu-id="e2d80-361">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-361">Compile and rebuild the project.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="e2d80-362">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="e2d80-362">Add the custom receipt layout</span></span>

1. <span data-ttu-id="e2d80-363">Dynamics 365 for Finance and Operations, Enterprise edition を開きます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-363">Open Dynamics 365 for Finance and Operations, Enterpise edition.</span></span>
2. <span data-ttu-id="e2d80-364">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-364">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="e2d80-365">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-365">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="e2d80-366">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-366">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="e2d80-367">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-367">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="e2d80-368">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-368">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="e2d80-369">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="e2d80-369">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="e2d80-370">デザイナーを起動する Azure Active Directory (AAD) の資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-370">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="e2d80-371">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-371">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="e2d80-372">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-372">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="e2d80-373">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-373">Click **Save**.</span></span>
9. <span data-ttu-id="e2d80-374">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-374">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="e2d80-375">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-375">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="e2d80-376">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-376">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="e2d80-377">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-377">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="e2d80-378">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-378">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="e2d80-379">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-379">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="e2d80-380">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-380">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="e2d80-381">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e2d80-381">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="e2d80-382">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-382">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="e2d80-383">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-383">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="e2d80-384">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-384">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="e2d80-385">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-385">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="e2d80-386">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-386">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="e2d80-387">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-387">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="e2d80-388">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-388">Click **Save**.</span></span>
6. <span data-ttu-id="e2d80-389">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-389">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="e2d80-390">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-390">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="e2d80-391">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-391">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="e2d80-392">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="e2d80-392">Validate the extension</span></span>

1. <span data-ttu-id="e2d80-393">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="e2d80-393">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="e2d80-394">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-394">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="e2d80-395">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="e2d80-395">Suspend the transaction.</span></span>
4. <span data-ttu-id="e2d80-396">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="e2d80-396">The custom receipt should print.</span></span>

