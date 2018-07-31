---
title: "Retail Modern POS のトリガーと印刷"
description: "トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。"
author: mugunthanm
manager: AnnBe
ms.date: 07/09/2018
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
ms.sourcegitcommit: f2e3a40f58b57785079e1940b2d24a3598a3ad1b
ms.openlocfilehash: 618f8572f6d6ead6e8838b2aca84fc0ee823b42a
ms.contentlocale: ja-jp
ms.lasthandoff: 07/09/2018

---

# <a name="retail-modern-pos-triggers-and-printing"></a><span data-ttu-id="678aa-103">Retail Modern POS のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="678aa-103">Retail Modern POS triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="678aa-104">トリガーを使用すると、Retail Modern POS の操作前または後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="678aa-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="678aa-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="678aa-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="678aa-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="678aa-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="678aa-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="678aa-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="678aa-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="678aa-108">Continue or cancel an operation.</span></span> <span data-ttu-id="678aa-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="678aa-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="678aa-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="678aa-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="678aa-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="678aa-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 

<span data-ttu-id="678aa-112">このトピックは、プラットフォーム更新プログラム 8 および Retail アプリケーション更新プログラム 4 修正プログラムを備えた、Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail に適用されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-112">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="678aa-113">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="678aa-113">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="678aa-114">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-114">Application triggers</span></span>

| <span data-ttu-id="678aa-115">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-115">Trigger</span></span>                   | <span data-ttu-id="678aa-116">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-116">Type</span></span>           | <span data-ttu-id="678aa-117">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-117">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="678aa-118">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-118">ApplicationStartTrigger</span></span>   | <span data-ttu-id="678aa-119">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-119">Non-cancelable</span></span> | <span data-ttu-id="678aa-120">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-120">Executed after the POS application is started.</span></span> <span data-ttu-id="678aa-121">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="678aa-121">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="678aa-122">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-122">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="678aa-123">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-123">Non-cancelable</span></span> | <span data-ttu-id="678aa-124">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-124">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="678aa-125">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-125">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="678aa-126">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-126">Cancelable</span></span>     | <span data-ttu-id="678aa-127">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-127">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="678aa-128">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-128">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="678aa-129">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-129">Non-cancelable</span></span> | <span data-ttu-id="678aa-130">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-130">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="678aa-131">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-131">PostLogOffTrigger</span></span>         | <span data-ttu-id="678aa-132">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-132">Non-cancelable</span></span> | <span data-ttu-id="678aa-133">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-133">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="678aa-134">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-134">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="678aa-135">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-135">Cancelable</span></span>     | <span data-ttu-id="678aa-136">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-136">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="678aa-137">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-137">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="678aa-138">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-138">Non-Cancelable</span></span> | <span data-ttu-id="678aa-139">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-139">Executed after the POS register lock.</span></span>   |     

## <a name="cash-nanagement-triggers"></a><span data-ttu-id="678aa-140">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-140">Cash nanagement triggers</span></span>

| <span data-ttu-id="678aa-141">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-141">Trigger</span></span>                      | <span data-ttu-id="678aa-142">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-142">Type</span></span>           | <span data-ttu-id="678aa-143">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-143">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="678aa-144">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-144">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="678aa-145">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-145">Cancelable</span></span>     | <span data-ttu-id="678aa-146">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-146">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="678aa-147">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-147">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="678aa-148">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-148">Non-cancelable</span></span> | <span data-ttu-id="678aa-149">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-149">Executed after the POS tender declaration.</span></span>  |

## <a name="customer-triggers"></a><span data-ttu-id="678aa-150">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-150">Customer triggers</span></span>

| <span data-ttu-id="678aa-151">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-151">Trigger</span></span>                   | <span data-ttu-id="678aa-152">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-152">Type</span></span>                    | <span data-ttu-id="678aa-153">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-153">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="678aa-154">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-154">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="678aa-155">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-155">Cancelable</span></span>              | <span data-ttu-id="678aa-156">新しい顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-156">Executed before creating a new customer.</span></span>             |
| <span data-ttu-id="678aa-157">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-157">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="678aa-158">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-158">Non-cancelable</span></span>          | <span data-ttu-id="678aa-159">新しい顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-159">Executed after creating a new customer.</span></span>              |
| <span data-ttu-id="678aa-160">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-160">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="678aa-161">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-161">PreCustomerClearTrigger</span></span> | <span data-ttu-id="678aa-162">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-162">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="678aa-163">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-163">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="678aa-164">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-164">Non-cancelable</span></span>          | <span data-ttu-id="678aa-165">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-165">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="678aa-166">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-166">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="678aa-167">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-167">Cancelable</span></span>              | <span data-ttu-id="678aa-168">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-168">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="678aa-169">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-169">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="678aa-170">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-170">Cancelable</span></span>              | <span data-ttu-id="678aa-171">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-171">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="678aa-172">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-172">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="678aa-173">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-173">Non-cancelable</span></span>          | <span data-ttu-id="678aa-174">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-174">Executed after customer search is performed.</span></span>       |

## <a name="discount-triggers"></a><span data-ttu-id="678aa-175">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-175">Discount triggers</span></span>

| <span data-ttu-id="678aa-176">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-176">Trigger</span></span>                         | <span data-ttu-id="678aa-177">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-177">Type</span></span>           | <span data-ttu-id="678aa-178">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-178">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="678aa-179">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-179">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="678aa-180">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-180">Cancelable</span></span>     | <span data-ttu-id="678aa-181">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-181">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="678aa-182">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-182">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="678aa-183">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-183">Non-cancelable</span></span> | <span data-ttu-id="678aa-184">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-184">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="678aa-185">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-185">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="678aa-186">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-186">Cancelable</span></span>     | <span data-ttu-id="678aa-187">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-187">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="678aa-188">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-188">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="678aa-189">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-189">Non-cancelable</span></span> | <span data-ttu-id="678aa-190">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-190">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="678aa-191">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-191">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="678aa-192">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-192">Cancelable</span></span>     | <span data-ttu-id="678aa-193">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-193">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="678aa-194">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-194">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="678aa-195">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-195">Non-cancelable</span></span> | <span data-ttu-id="678aa-196">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-196">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="678aa-197">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-197">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="678aa-198">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-198">Cancelable</span></span>     | <span data-ttu-id="678aa-199">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-199">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="678aa-200">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-200">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="678aa-201">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-201">Non-cancelable</span></span> | <span data-ttu-id="678aa-202">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-202">Executed after total discount percent added to the cart.</span></span>        |

## <a name="operation-triggers"></a><span data-ttu-id="678aa-203">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-203">Operation triggers</span></span>

| <span data-ttu-id="678aa-204">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-204">Trigger</span></span>              | <span data-ttu-id="678aa-205">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-205">Type</span></span>           | <span data-ttu-id="678aa-206">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-206">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="678aa-207">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-207">PreOperationTrigger</span></span>  | <span data-ttu-id="678aa-208">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-208">Cancelable</span></span>     | <span data-ttu-id="678aa-209">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="678aa-209">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="678aa-210">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="678aa-210">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="678aa-211">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-211">PostOperationTrigger</span></span> | <span data-ttu-id="678aa-212">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-212">Non-cancelable</span></span> | <span data-ttu-id="678aa-213">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="678aa-213">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="678aa-214">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="678aa-214">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="678aa-215">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-215">Payment triggers</span></span>

| <span data-ttu-id="678aa-216">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-216">Trigger</span></span>                 | <span data-ttu-id="678aa-217">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-217">Type</span></span>           | <span data-ttu-id="678aa-218">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-218">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="678aa-219">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-219">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="678aa-220">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-220">Cancelable</span></span>     | <span data-ttu-id="678aa-221">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-221">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="678aa-222">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-222">PrePaymentTrigger</span></span>       | <span data-ttu-id="678aa-223">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-223">Cancelable</span></span>     | <span data-ttu-id="678aa-224">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-224">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="678aa-225">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-225">PostPaymentTrigger</span></span>      | <span data-ttu-id="678aa-226">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-226">Non-cancelable</span></span> | <span data-ttu-id="678aa-227">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-227">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="678aa-228">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-228">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="678aa-229">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-229">Cancelable</span></span>     | <span data-ttu-id="678aa-230">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-230">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="678aa-231">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-231">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="678aa-232">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-232">Non-cancelable</span></span> | <span data-ttu-id="678aa-233">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-233">Executed after the payment line is voided in POS.</span></span>   |

<span data-ttu-id="678aa-234">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-234">Printing Triggers</span></span>

| <span data-ttu-id="678aa-235">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-235">Trigger</span></span>                    | <span data-ttu-id="678aa-236">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-236">Type</span></span>       | <span data-ttu-id="678aa-237">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-237">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="678aa-238">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-238">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="678aa-239">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-239">Cancelable</span></span> | <span data-ttu-id="678aa-240">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-240">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="678aa-241">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-241">Product triggers</span></span>

| <span data-ttu-id="678aa-242">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-242">Trigger</span></span>                    | <span data-ttu-id="678aa-243">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-243">Type</span></span>           | <span data-ttu-id="678aa-244">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-244">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="678aa-245">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-245">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="678aa-246">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-246">Non-cancelable</span></span> | <span data-ttu-id="678aa-247">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-247">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="678aa-248">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-248">PreProductSaleTrigger</span></span>      | <span data-ttu-id="678aa-249">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-249">Cancelable</span></span>     | <span data-ttu-id="678aa-250">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-250">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="678aa-251">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-251">PostProductSaleTrigger</span></span>     | <span data-ttu-id="678aa-252">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-252">Non-cancelable</span></span> | <span data-ttu-id="678aa-253">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-253">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="678aa-254">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-254">PreReturnProductTrigger</span></span>    | <span data-ttu-id="678aa-255">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-255">Cancelable</span></span>     | <span data-ttu-id="678aa-256">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-256">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="678aa-257">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-257">PostReturnProductTrigger</span></span>   | <span data-ttu-id="678aa-258">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-258">Non-cancelable</span></span> | <span data-ttu-id="678aa-259">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-259">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="678aa-260">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-260">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="678aa-261">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-261">Cancelable</span></span>     | <span data-ttu-id="678aa-262">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-262">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="678aa-263">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-263">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="678aa-264">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-264">Non-cancelable</span></span> | <span data-ttu-id="678aa-265">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-265">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="678aa-266">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-266">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="678aa-267">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-267">Cancelable</span></span>     | <span data-ttu-id="678aa-268">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-268">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="678aa-269">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-269">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="678aa-270">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-270">Non-cancelable</span></span> | <span data-ttu-id="678aa-271">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-271">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="678aa-272">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-272">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="678aa-273">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-273">Cancelable</span></span>     | <span data-ttu-id="678aa-274">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-274">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="678aa-275">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-275">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="678aa-276">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-276">Non-cancelable</span></span> | <span data-ttu-id="678aa-277">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-277">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="678aa-278">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-278">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="678aa-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-279">Cancelable</span></span>     | <span data-ttu-id="678aa-280">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-280">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="678aa-281">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-281">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="678aa-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-282">Non-cancelable</span></span> | <span data-ttu-id="678aa-283">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-283">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="678aa-284">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-284">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="678aa-285">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-285">Non-cancelable</span></span> | <span data-ttu-id="678aa-286">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-286">Executed after the price check for the product is executed.</span></span>          |

## <a name="shift-triggers"></a><span data-ttu-id="678aa-287">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-287">Shift triggers</span></span>
| <span data-ttu-id="678aa-288">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-288">Trigger</span></span>              | <span data-ttu-id="678aa-289">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-289">Type</span></span>           | <span data-ttu-id="678aa-290">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-290">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="678aa-291">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-291">PostOpenShiftTrigger</span></span> | <span data-ttu-id="678aa-292">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-292">Non-cancelable</span></span> | <span data-ttu-id="678aa-293">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-293">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="678aa-294">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-294">Tax override triggers</span></span>

| <span data-ttu-id="678aa-295">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-295">Trigger</span></span>                           | <span data-ttu-id="678aa-296">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-296">Type</span></span>           | <span data-ttu-id="678aa-297">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-297">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="678aa-298">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-298">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="678aa-299">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-299">Cancelable</span></span>     | <span data-ttu-id="678aa-300">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-300">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="678aa-301">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-301">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="678aa-302">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-302">Non-cancelable</span></span> | <span data-ttu-id="678aa-303">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-303">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="678aa-304">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-304">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="678aa-305">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-305">Cancelable</span></span>     | <span data-ttu-id="678aa-306">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-306">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="678aa-307">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-307">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="678aa-308">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-308">Non-cancelable</span></span> | <span data-ttu-id="678aa-309">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-309">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="678aa-310">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-310">Transaction triggers</span></span>

| <span data-ttu-id="678aa-311">トリガー</span><span class="sxs-lookup"><span data-stu-id="678aa-311">Trigger</span></span>                            | <span data-ttu-id="678aa-312">種類</span><span class="sxs-lookup"><span data-stu-id="678aa-312">Type</span></span>           | <span data-ttu-id="678aa-313">説明</span><span class="sxs-lookup"><span data-stu-id="678aa-313">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="678aa-314">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-314">BeginTransactionTrigger</span></span>            | <span data-ttu-id="678aa-315">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-315">Non-cancelable</span></span> | <span data-ttu-id="678aa-316">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-316">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="678aa-317">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-317">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="678aa-318">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-318">Cancelable</span></span>     | <span data-ttu-id="678aa-319">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-319">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="678aa-320">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-320">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="678aa-321">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-321">Cancelable</span></span>     | <span data-ttu-id="678aa-322">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-322">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="678aa-323">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-323">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="678aa-324">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-324">Non-cancelable</span></span> | <span data-ttu-id="678aa-325">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-325">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="678aa-326">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-326">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="678aa-327">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-327">Cancelable</span></span>     | <span data-ttu-id="678aa-328">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="678aa-328">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="678aa-329">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-329">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="678aa-330">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-330">Non-cancelable</span></span> | <span data-ttu-id="678aa-331">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="678aa-331">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="678aa-332">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-332">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="678aa-333">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-333">Cancelable</span></span>     | <span data-ttu-id="678aa-334">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-334">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="678aa-335">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-335">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="678aa-336">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-336">Non-cancelable</span></span> | <span data-ttu-id="678aa-337">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-337">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="678aa-338">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-338">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="678aa-339">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-339">Cancelable</span></span>     | <span data-ttu-id="678aa-340">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-340">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="678aa-341">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-341">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="678aa-342">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-342">Non-cancelable</span></span> | <span data-ttu-id="678aa-343">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-343">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="678aa-344">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-344">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="678aa-345">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-345">Cancelable</span></span>     | <span data-ttu-id="678aa-346">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-346">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="678aa-347">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-347">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="678aa-348">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-348">Non-cancelable</span></span> | <span data-ttu-id="678aa-349">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-349">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="678aa-350">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-350">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="678aa-351">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-351">Non-cancelable</span></span> | <span data-ttu-id="678aa-352">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-352">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="678aa-353">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-353">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="678aa-354">解約可能</span><span class="sxs-lookup"><span data-stu-id="678aa-354">Cancelable</span></span>     | <span data-ttu-id="678aa-355">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-355">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="678aa-356">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="678aa-356">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="678aa-357">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="678aa-357">Non-Cancelable</span></span> | <span data-ttu-id="678aa-358">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-358">Executed after the customer order is recalled.</span></span>        |

## <a name="business-scenario"></a><span data-ttu-id="678aa-359">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="678aa-359">Business scenario</span></span>
<span data-ttu-id="678aa-360">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-360">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="678aa-361">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="678aa-361">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="678aa-362">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="678aa-362">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="678aa-363">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="678aa-363">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="678aa-364">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="678aa-364">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="678aa-365">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="678aa-365">Implement a trigger</span></span>

1. <span data-ttu-id="678aa-366">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="678aa-366">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="678aa-367">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="678aa-367">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="678aa-368">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="678aa-368">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="678aa-369">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="678aa-369">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="678aa-370">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="678aa-370">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="678aa-371">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="678aa-371">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="678aa-372">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="678aa-372">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="678aa-373">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="678aa-373">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="678aa-374">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="678aa-374">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="678aa-375">新しい .json ファイルを **POSAPIExtension** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="678aa-375">Create a new .json file under the **POSAPIExtension** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="678aa-376">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="678aa-376">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="678aa-377">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="678aa-377">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="678aa-378">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="678aa-378">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="678aa-379">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="678aa-379">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="678aa-380">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="678aa-380">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="678aa-381">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="678aa-381">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="678aa-382">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="678aa-382">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="678aa-383">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="678aa-383">Override the CRT receipt request to generate the receipt data</span></span>

<span data-ttu-id="678aa-384">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="678aa-384">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> <span data-ttu-id="678aa-385">このセクションは、Microsoft Dynamics 365 for Finance and Operations またはプラットフォーム更新プログラム 8 を備えた Microsoft Dynamics 365 for Retail に適用可能です。</span><span class="sxs-lookup"><span data-stu-id="678aa-385">This section is applicable to Microsoft Dynamics 365 for Finance and Operations or Microsoft Dynamics 365 for Retail with platform update 8.</span></span>

1. <span data-ttu-id="678aa-386">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="678aa-386">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="678aa-387">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="678aa-387">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="678aa-388">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="678aa-388">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="678aa-389">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="678aa-389">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="678aa-390">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="678aa-390">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="678aa-391">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="678aa-391">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="678aa-392">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="678aa-392">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="678aa-393">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="678aa-393">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="678aa-394">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="678aa-394">Before you copy it, delete the automatically generated code.</span></span>

    ```C#
    namespace Contoso
    {
        namespace Commerce.Runtime.ReceiptsSample
        {
            using System.Collections.Generic;
            using System.Collections.ObjectModel;
            using Microsoft.Dynamics.Commerce.Runtime;
            using Microsoft.Dynamics.Commerce.Runtime.DataModel;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.Workflow;

            /// <summary>
            /// The request handler for GetCustomReceiptsRequestHandler class.
            /// </summary>

            /// <remarks>
            /// This is an example of how to print custom types of receipts. In this example the receipt is for a transaction as opposed to
            /// a sales order. The implementation converts the transaction to a sales order so that existing receipt fields can be used.
            /// </remarks>

            public class GetCustomReceiptsRequestHandler : SingleRequestHandler<GetCustomReceiptsRequest, GetReceiptResponse>
            {
            }
        }
    }
    ```

8. <span data-ttu-id="678aa-395">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="678aa-395">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="678aa-396">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678aa-396">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="678aa-397">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="678aa-397">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="678aa-398">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="678aa-398">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="678aa-399">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="678aa-399">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

    ```C#
    private SalesOrder GetSalesOrderForTransactionWithId(RequestContext requestContext, string transactionId)
    {
        SalesOrder salesOrder = new SalesOrder();
        var getCartRequest = new GetCartRequest(new CartSearchCriteria(transactionId), QueryResultSettings.SingleRecord);
        var getCartResponse = requestContext.Execute<GetCartResponse>(getCartRequest);
        SalesTransaction salesTransaction = getCartResponse.Transactions.SingleOrDefault(); ;
        if (salesTransaction != null)
        {
            // The sales transaction is converted into a sales order so that existing receipt fields can be used.
            salesOrder.CopyFrom<SalesTransaction>(salesTransaction);
        }
        else
        {
            throw new DataValidationException(
                DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_ObjectNotFound,
                string.Format("Unable to get the sales transaction. ID: {0}", transactionId));
        }
        return salesOrder;
    }
    ```

9. <span data-ttu-id="678aa-400">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="678aa-400">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

    ```C#
    private Collection<Receipt> GetCustomReceipts(SalesOrder salesOrder, ReceiptRetrievalCriteria criteria)
    {
        Collection<Receipt> result = new Collection<Receipt>();
        var getReceiptServiceRequest = new GetReceiptServiceRequest(
            salesOrder,
            new Collection<ReceiptType> { criteria.ReceiptType },
            salesOrder.TenderLines,
            criteria.IsCopy,
            criteria.IsPreview,
            criteria.HardwareProfileId);
        ReadOnlyCollection<Receipt> customReceipts = this.Context.Execute<GetReceiptServiceResponse>(getReceiptServiceRequest).Receipts;
        result.AddRange(customReceipts);
        return result;
    }
    ```

10. <span data-ttu-id="678aa-401">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="678aa-401">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="678aa-402">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="678aa-402">This method processes the request and returns the response.</span></span>

    ```C#
    protected override GetReceiptResponse Process(GetCustomReceiptsRequest request)
    {
        ThrowIf.Null(request, "request");
        ThrowIf.Null(request.ReceiptRetrievalCriteria, "request.ReceiptRetrievalCriteria");

        // The sales order that we are printing receipts for is retrieved.
        SalesOrder salesOrder = this.GetSalesOrderForTransactionWithId(request.RequestContext, request.TransactionId);

        // Custom receipts are printed.
        Collection<Receipt> result = new Collection<Receipt>();
        switch (request.ReceiptRetrievalCriteria.ReceiptType)
        {
            // An example of getting custom receipts.
            case ReceiptType.CustomReceipt7:
            {
                IEnumerable<Receipt> customReceipts = this.GetCustomReceipts(salesOrder, request.ReceiptRetrievalCriteria);
                result.AddRange(customReceipts);
            }
            break;
            default:

            // Add more logic to handle more types of custom receipt types.

            break;
        }
        return new GetReceiptResponse(new ReadOnlyCollection<Receipt>(result));
    }
    ```

    <span data-ttu-id="678aa-403">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="678aa-403">The overall code should look like this.</span></span>

    ```C#
    /**
     * SAMPLE CODE NOTICE
     *
     * THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
     * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
     * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
     * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
     */

    namespace Contoso
    {
        namespace Commerce.Runtime.ReceiptsSample
        {
            using System.Collections.Generic;
            using System.Collections.ObjectModel;
            using Microsoft.Dynamics.Commerce.Runtime;
            using Microsoft.Dynamics.Commerce.Runtime.DataModel;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.Workflow;

            /// <summary>
            /// The request handler for GetCustomReceiptsRequestHandler class.
            /// </summary>

            /// <remarks>
            /// This is an example of how to print custom types of receipts. In this example the receipt is for a transaction as opposed to
            /// a sales order. The implementation converts the transaction to a sales order so that existing receipt fields can be used.
            /// </remarks>

            public class GetCustomReceiptsRequestHandler : SingleRequestHandler<GetCustomReceiptsRequest, GetReceiptResponse>
            {

                /// <summary>
                /// Processes the GetCustomReceiptsRequest to return the set of receipts. The request should not be null.
                /// </summary>

                /// <param name="request">The request parameter.</param>

                /// <returns>The GetReceiptResponse.</returns>

                protected override GetReceiptResponse Process(GetCustomReceiptsRequest request)
                {
                    ThrowIf.Null(request, "request");
                    ThrowIf.Null(request.ReceiptRetrievalCriteria, "request.ReceiptRetrievalCriteria");

                    // The sales order that we are printing receipts for is retrieved.
                    SalesOrder salesOrder = this.GetSalesOrderForTransactionWithId(request.RequestContext, request.TransactionId);

                    // Custom receipts are printed.
                    Collection<Receipt> result = new Collection<Receipt>();
                    switch (request.ReceiptRetrievalCriteria.ReceiptType)
                    {
                        // An example of getting custom receipts.
                        case ReceiptType.CustomReceipt7:
                        {
                            IEnumerable<Receipt> customReceipts = this.GetCustomReceipts(salesOrder, request.ReceiptRetrievalCriteria);
                            result.AddRange(customReceipts);
                        }
                        break;
                        default:

                        // Add more logic to handle more types of custom receipt types.

                        break;
                    }
                    return new GetReceiptResponse(new ReadOnlyCollection<Receipt>(result));
                }

                /// <summary>
                /// Gets a sales order for the transaction with the given identifier.
                /// </summary>

                /// <param name="requestContext">The request context.</param>
                /// <param name="transactionId">The transaction identifier.</param>

                /// <returns>The sales order.</returns>

                private SalesOrder GetSalesOrderForTransactionWithId(RequestContext requestContext, string transactionId)
                {
                    SalesOrder salesOrder = new SalesOrder();
                    var getCartRequest = new GetCartRequest(new CartSearchCriteria(transactionId), QueryResultSettings.SingleRecord);
                    var getCartResponse = requestContext.Execute<GetCartResponse>(getCartRequest);
                    SalesTransaction salesTransaction = getCartResponse.Transactions.SingleOrDefault(); ;
                    if (salesTransaction != null)
                    {
                        // The sales transaction is converted into a sales order so that existing receipt fields can be used.
                        salesOrder.CopyFrom<SalesTransaction>(salesTransaction);
                    }
                    else
                    {
                        throw new DataValidationException(
                        DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_ObjectNotFound,
                        string.Format("Unable to get the sales transaction. ID: {0}", transactionId));
                    }
                    return salesOrder;
                }

                /// <summary>
                /// An example to get a custom receipt.
                /// </summary>

                /// <param name="salesOrder">The sales order that we are printing receipts for.</param>
                /// <param name="criteria">The receipt retrieval criteria.</param>

                /// <returns>A collection of receipts.</returns>

                private Collection<Receipt> GetCustomReceipts(SalesOrder salesOrder, ReceiptRetrievalCriteria criteria)
                {
                    Collection<Receipt> result = new Collection<Receipt>();
                    var getReceiptServiceRequest = new GetReceiptServiceRequest(
                        salesOrder,
                        new Collection<ReceiptType> { criteria.ReceiptType },
                        salesOrder.TenderLines,
                        criteria.IsCopy,
                        criteria.IsPreview,
                        criteria.HardwareProfileId);
                    ReadOnlyCollection<Receipt> customReceipts = this.Context.Execute<GetReceiptServiceResponse>(getReceiptServiceRequest).Receipts;
                    result.AddRange(customReceipts);
                    return result;
                }
            }
        }
    }
    ```

11. <span data-ttu-id="678aa-404">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="678aa-404">Compile and build the project.</span></span>
12. <span data-ttu-id="678aa-405">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="678aa-405">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="678aa-406">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="678aa-406">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="678aa-407">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="678aa-407">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="678aa-408">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="678aa-408">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="678aa-409">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="678aa-409">Save and close the file.</span></span>
17. <span data-ttu-id="678aa-410">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="678aa-410">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="678aa-411">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="678aa-411">Add the custom receipt layout</span></span>

1. <span data-ttu-id="678aa-412">Dynamics 365 for Finance and Operations, Enterprise edition を開きます。</span><span class="sxs-lookup"><span data-stu-id="678aa-412">Open Dynamics 365 for Finance and Operations, Enterpise edition.</span></span>
2. <span data-ttu-id="678aa-413">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="678aa-413">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="678aa-414">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-414">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="678aa-415">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="678aa-415">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="678aa-416">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="678aa-416">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="678aa-417">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="678aa-417">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="678aa-418">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="678aa-418">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="678aa-419">デザイナーを起動する Azure Active Directory (AAD) の資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="678aa-419">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="678aa-420">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="678aa-420">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="678aa-421">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="678aa-421">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="678aa-422">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-422">Click **Save**.</span></span>
9. <span data-ttu-id="678aa-423">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="678aa-423">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="678aa-424">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="678aa-424">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="678aa-425">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-425">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="678aa-426">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="678aa-426">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="678aa-427">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="678aa-427">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="678aa-428">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-428">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="678aa-429">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="678aa-429">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="678aa-430">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="678aa-430">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="678aa-431">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="678aa-431">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="678aa-432">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="678aa-432">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="678aa-433">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="678aa-433">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="678aa-434">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-434">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="678aa-435">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="678aa-435">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="678aa-436">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="678aa-436">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="678aa-437">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-437">Click **Save**.</span></span>
6. <span data-ttu-id="678aa-438">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="678aa-438">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="678aa-439">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="678aa-439">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="678aa-440">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="678aa-440">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="678aa-441">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="678aa-441">Validate the extension</span></span>

1. <span data-ttu-id="678aa-442">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="678aa-442">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="678aa-443">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="678aa-443">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="678aa-444">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="678aa-444">Suspend the transaction.</span></span>
4. <span data-ttu-id="678aa-445">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="678aa-445">The custom receipt should print.</span></span>

