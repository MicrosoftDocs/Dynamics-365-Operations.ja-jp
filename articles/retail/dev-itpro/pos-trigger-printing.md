---
title: "Retail Modern POS (MPOS) のトリガーと印刷"
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
ms.sourcegitcommit: 87663bae532f68c8dbc306b51bf591f33f7f4d63
ms.openlocfilehash: 17fdecd4e471e7f2eaa553c11aab7c4f9030f148
ms.contentlocale: ja-jp
ms.lasthandoff: 10/04/2018

---

# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="cff0d-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="cff0d-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cff0d-104">トリガーを使用すると、Retail Modern POS の操作前または後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="cff0d-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="cff0d-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="cff0d-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="cff0d-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-108">Continue or cancel an operation.</span></span> <span data-ttu-id="cff0d-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="cff0d-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="cff0d-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="cff0d-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 

<span data-ttu-id="cff0d-112">このトピックは、プラットフォーム更新プログラム 8 および Retail アプリケーション更新プログラム 4 修正プログラムを備えた、Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail に適用されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-112">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="cff0d-113">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="cff0d-113">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="cff0d-114">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-114">Application triggers</span></span>

| <span data-ttu-id="cff0d-115">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-115">Trigger</span></span>                   | <span data-ttu-id="cff0d-116">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-116">Type</span></span>           | <span data-ttu-id="cff0d-117">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-117">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="cff0d-118">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-118">ApplicationStartTrigger</span></span>   | <span data-ttu-id="cff0d-119">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-119">Non-cancelable</span></span> | <span data-ttu-id="cff0d-120">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-120">Executed after the POS application is started.</span></span> <span data-ttu-id="cff0d-121">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-121">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="cff0d-122">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-122">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="cff0d-123">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-123">Non-cancelable</span></span> | <span data-ttu-id="cff0d-124">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-124">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="cff0d-125">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-125">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="cff0d-126">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-126">Cancelable</span></span>     | <span data-ttu-id="cff0d-127">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-127">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="cff0d-128">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-128">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="cff0d-129">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-129">Non-cancelable</span></span> | <span data-ttu-id="cff0d-130">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-130">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="cff0d-131">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-131">PostLogOffTrigger</span></span>         | <span data-ttu-id="cff0d-132">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-132">Non-cancelable</span></span> | <span data-ttu-id="cff0d-133">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-133">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="cff0d-134">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-134">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="cff0d-135">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-135">Cancelable</span></span>     | <span data-ttu-id="cff0d-136">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-136">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="cff0d-137">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-137">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="cff0d-138">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-138">Non-Cancelable</span></span> | <span data-ttu-id="cff0d-139">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-139">Executed after the POS register lock.</span></span>   |     

## <a name="cash-management-triggers"></a><span data-ttu-id="cff0d-140">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-140">Cash management triggers</span></span>

| <span data-ttu-id="cff0d-141">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-141">Trigger</span></span>                      | <span data-ttu-id="cff0d-142">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-142">Type</span></span>           | <span data-ttu-id="cff0d-143">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-143">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="cff0d-144">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-144">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="cff0d-145">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-145">Cancelable</span></span>     | <span data-ttu-id="cff0d-146">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-146">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="cff0d-147">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-147">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="cff0d-148">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-148">Non-cancelable</span></span> | <span data-ttu-id="cff0d-149">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-149">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="cff0d-150">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-150">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="cff0d-151">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-151">Cancelable</span></span>     | <span data-ttu-id="cff0d-152">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-152">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="cff0d-153">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-153">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="cff0d-154">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-154">Non-cancelable</span></span> | <span data-ttu-id="cff0d-155">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-155">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="cff0d-156">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-156">Customer triggers</span></span>

| <span data-ttu-id="cff0d-157">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-157">Trigger</span></span>                   | <span data-ttu-id="cff0d-158">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-158">Type</span></span>                    | <span data-ttu-id="cff0d-159">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-159">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cff0d-160">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-160">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="cff0d-161">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-161">Cancelable</span></span>              | <span data-ttu-id="cff0d-162">新しい顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-162">Executed before creating a new customer.</span></span>             |
| <span data-ttu-id="cff0d-163">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-163">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="cff0d-164">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-164">Non-cancelable</span></span>          | <span data-ttu-id="cff0d-165">新しい顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-165">Executed after creating a new customer.</span></span>              |
| <span data-ttu-id="cff0d-166">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-166">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="cff0d-167">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-167">PreCustomerClearTrigger</span></span> | <span data-ttu-id="cff0d-168">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-168">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="cff0d-169">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-169">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="cff0d-170">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-170">Non-cancelable</span></span>          | <span data-ttu-id="cff0d-171">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-171">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="cff0d-172">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-172">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="cff0d-173">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-173">Cancelable</span></span>              | <span data-ttu-id="cff0d-174">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-174">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="cff0d-175">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-175">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="cff0d-176">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-176">Cancelable</span></span>              | <span data-ttu-id="cff0d-177">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-177">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="cff0d-178">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-178">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="cff0d-179">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-179">Non-cancelable</span></span>          | <span data-ttu-id="cff0d-180">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-180">Executed after customer search is performed.</span></span>       |

## <a name="discount-triggers"></a><span data-ttu-id="cff0d-181">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-181">Discount triggers</span></span>

| <span data-ttu-id="cff0d-182">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-182">Trigger</span></span>                         | <span data-ttu-id="cff0d-183">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-183">Type</span></span>           | <span data-ttu-id="cff0d-184">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-184">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="cff0d-185">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-185">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="cff0d-186">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-186">Cancelable</span></span>     | <span data-ttu-id="cff0d-187">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-187">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="cff0d-188">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-188">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="cff0d-189">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-189">Non-cancelable</span></span> | <span data-ttu-id="cff0d-190">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-190">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="cff0d-191">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-191">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="cff0d-192">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-192">Cancelable</span></span>     | <span data-ttu-id="cff0d-193">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-193">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="cff0d-194">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-194">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="cff0d-195">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-195">Non-cancelable</span></span> | <span data-ttu-id="cff0d-196">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-196">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="cff0d-197">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-197">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="cff0d-198">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-198">Cancelable</span></span>     | <span data-ttu-id="cff0d-199">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-199">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="cff0d-200">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-200">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="cff0d-201">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-201">Non-cancelable</span></span> | <span data-ttu-id="cff0d-202">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-202">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="cff0d-203">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-203">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="cff0d-204">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-204">Cancelable</span></span>     | <span data-ttu-id="cff0d-205">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-205">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="cff0d-206">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-206">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="cff0d-207">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-207">Non-cancelable</span></span> | <span data-ttu-id="cff0d-208">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-208">Executed after total discount percent added to the cart.</span></span>        |

## <a name="operation-triggers"></a><span data-ttu-id="cff0d-209">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-209">Operation triggers</span></span>

| <span data-ttu-id="cff0d-210">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-210">Trigger</span></span>              | <span data-ttu-id="cff0d-211">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-211">Type</span></span>           | <span data-ttu-id="cff0d-212">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-212">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="cff0d-213">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-213">PreOperationTrigger</span></span>  | <span data-ttu-id="cff0d-214">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-214">Cancelable</span></span>     | <span data-ttu-id="cff0d-215">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="cff0d-215">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="cff0d-216">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-216">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="cff0d-217">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-217">PostOperationTrigger</span></span> | <span data-ttu-id="cff0d-218">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-218">Non-cancelable</span></span> | <span data-ttu-id="cff0d-219">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="cff0d-219">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="cff0d-220">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-220">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="cff0d-221">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-221">Payment triggers</span></span>

| <span data-ttu-id="cff0d-222">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-222">Trigger</span></span>                 | <span data-ttu-id="cff0d-223">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-223">Type</span></span>           | <span data-ttu-id="cff0d-224">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-224">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="cff0d-225">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-225">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="cff0d-226">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-226">Cancelable</span></span>     | <span data-ttu-id="cff0d-227">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-227">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="cff0d-228">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-228">PrePaymentTrigger</span></span>       | <span data-ttu-id="cff0d-229">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-229">Cancelable</span></span>     | <span data-ttu-id="cff0d-230">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-230">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="cff0d-231">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-231">PostPaymentTrigger</span></span>      | <span data-ttu-id="cff0d-232">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-232">Non-cancelable</span></span> | <span data-ttu-id="cff0d-233">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-233">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="cff0d-234">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-234">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="cff0d-235">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-235">Cancelable</span></span>     | <span data-ttu-id="cff0d-236">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-236">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="cff0d-237">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-237">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="cff0d-238">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-238">Non-cancelable</span></span> | <span data-ttu-id="cff0d-239">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-239">Executed after the payment line is voided in POS.</span></span>   |

<span data-ttu-id="cff0d-240">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-240">Printing Triggers</span></span>

| <span data-ttu-id="cff0d-241">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-241">Trigger</span></span>                    | <span data-ttu-id="cff0d-242">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-242">Type</span></span>       | <span data-ttu-id="cff0d-243">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-243">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="cff0d-244">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-244">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="cff0d-245">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-245">Cancelable</span></span> | <span data-ttu-id="cff0d-246">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-246">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="cff0d-247">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-247">Product triggers</span></span>

| <span data-ttu-id="cff0d-248">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-248">Trigger</span></span>                    | <span data-ttu-id="cff0d-249">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-249">Type</span></span>           | <span data-ttu-id="cff0d-250">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-250">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cff0d-251">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-251">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="cff0d-252">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-252">Non-cancelable</span></span> | <span data-ttu-id="cff0d-253">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-253">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="cff0d-254">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-254">PreProductSaleTrigger</span></span>      | <span data-ttu-id="cff0d-255">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-255">Cancelable</span></span>     | <span data-ttu-id="cff0d-256">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-256">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="cff0d-257">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-257">PostProductSaleTrigger</span></span>     | <span data-ttu-id="cff0d-258">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-258">Non-cancelable</span></span> | <span data-ttu-id="cff0d-259">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-259">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="cff0d-260">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-260">PreReturnProductTrigger</span></span>    | <span data-ttu-id="cff0d-261">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-261">Cancelable</span></span>     | <span data-ttu-id="cff0d-262">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-262">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="cff0d-263">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-263">PostReturnProductTrigger</span></span>   | <span data-ttu-id="cff0d-264">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-264">Non-cancelable</span></span> | <span data-ttu-id="cff0d-265">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-265">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="cff0d-266">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-266">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="cff0d-267">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-267">Cancelable</span></span>     | <span data-ttu-id="cff0d-268">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-268">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="cff0d-269">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-269">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="cff0d-270">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-270">Non-cancelable</span></span> | <span data-ttu-id="cff0d-271">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-271">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="cff0d-272">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-272">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="cff0d-273">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-273">Cancelable</span></span>     | <span data-ttu-id="cff0d-274">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-274">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="cff0d-275">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-275">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="cff0d-276">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-276">Non-cancelable</span></span> | <span data-ttu-id="cff0d-277">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-277">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="cff0d-278">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-278">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="cff0d-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-279">Cancelable</span></span>     | <span data-ttu-id="cff0d-280">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-280">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="cff0d-281">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-281">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="cff0d-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-282">Non-cancelable</span></span> | <span data-ttu-id="cff0d-283">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-283">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="cff0d-284">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-284">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="cff0d-285">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-285">Cancelable</span></span>     | <span data-ttu-id="cff0d-286">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-286">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="cff0d-287">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-287">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="cff0d-288">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-288">Non-cancelable</span></span> | <span data-ttu-id="cff0d-289">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-289">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="cff0d-290">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-290">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="cff0d-291">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-291">Non-cancelable</span></span> | <span data-ttu-id="cff0d-292">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-292">Executed after the price check for the product is executed.</span></span>          |

## <a name="shift-triggers"></a><span data-ttu-id="cff0d-293">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-293">Shift triggers</span></span>
| <span data-ttu-id="cff0d-294">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-294">Trigger</span></span>              | <span data-ttu-id="cff0d-295">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-295">Type</span></span>           | <span data-ttu-id="cff0d-296">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-296">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="cff0d-297">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-297">PostOpenShiftTrigger</span></span> | <span data-ttu-id="cff0d-298">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-298">Non-cancelable</span></span> | <span data-ttu-id="cff0d-299">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-299">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="cff0d-300">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-300">Tax override triggers</span></span>

| <span data-ttu-id="cff0d-301">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-301">Trigger</span></span>                           | <span data-ttu-id="cff0d-302">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-302">Type</span></span>           | <span data-ttu-id="cff0d-303">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-303">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="cff0d-304">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-304">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="cff0d-305">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-305">Cancelable</span></span>     | <span data-ttu-id="cff0d-306">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-306">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="cff0d-307">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-307">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="cff0d-308">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-308">Non-cancelable</span></span> | <span data-ttu-id="cff0d-309">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-309">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="cff0d-310">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-310">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="cff0d-311">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-311">Cancelable</span></span>     | <span data-ttu-id="cff0d-312">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-312">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="cff0d-313">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-313">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="cff0d-314">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-314">Non-cancelable</span></span> | <span data-ttu-id="cff0d-315">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-315">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="cff0d-316">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-316">Transaction triggers</span></span>

| <span data-ttu-id="cff0d-317">トリガー</span><span class="sxs-lookup"><span data-stu-id="cff0d-317">Trigger</span></span>                            | <span data-ttu-id="cff0d-318">種類</span><span class="sxs-lookup"><span data-stu-id="cff0d-318">Type</span></span>           | <span data-ttu-id="cff0d-319">説明</span><span class="sxs-lookup"><span data-stu-id="cff0d-319">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="cff0d-320">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-320">BeginTransactionTrigger</span></span>            | <span data-ttu-id="cff0d-321">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-321">Non-cancelable</span></span> | <span data-ttu-id="cff0d-322">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-322">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="cff0d-323">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-323">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="cff0d-324">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-324">Cancelable</span></span>     | <span data-ttu-id="cff0d-325">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-325">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="cff0d-326">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-326">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="cff0d-327">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-327">Cancelable</span></span>     | <span data-ttu-id="cff0d-328">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-328">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="cff0d-329">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-329">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="cff0d-330">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-330">Non-cancelable</span></span> | <span data-ttu-id="cff0d-331">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-331">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="cff0d-332">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-332">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="cff0d-333">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-333">Cancelable</span></span>     | <span data-ttu-id="cff0d-334">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-334">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="cff0d-335">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-335">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="cff0d-336">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-336">Non-cancelable</span></span> | <span data-ttu-id="cff0d-337">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-337">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="cff0d-338">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-338">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="cff0d-339">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-339">Cancelable</span></span>     | <span data-ttu-id="cff0d-340">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-340">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="cff0d-341">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-341">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="cff0d-342">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-342">Non-cancelable</span></span> | <span data-ttu-id="cff0d-343">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-343">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="cff0d-344">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-344">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="cff0d-345">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-345">Cancelable</span></span>     | <span data-ttu-id="cff0d-346">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-346">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="cff0d-347">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-347">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="cff0d-348">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-348">Non-cancelable</span></span> | <span data-ttu-id="cff0d-349">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-349">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="cff0d-350">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-350">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="cff0d-351">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-351">Cancelable</span></span>     | <span data-ttu-id="cff0d-352">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-352">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="cff0d-353">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-353">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="cff0d-354">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-354">Non-cancelable</span></span> | <span data-ttu-id="cff0d-355">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-355">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="cff0d-356">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-356">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="cff0d-357">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-357">Non-cancelable</span></span> | <span data-ttu-id="cff0d-358">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-358">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="cff0d-359">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-359">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="cff0d-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="cff0d-360">Cancelable</span></span>     | <span data-ttu-id="cff0d-361">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-361">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="cff0d-362">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="cff0d-362">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="cff0d-363">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="cff0d-363">Non-Cancelable</span></span> | <span data-ttu-id="cff0d-364">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-364">Executed after the customer order is recalled.</span></span>        |

## <a name="business-scenario"></a><span data-ttu-id="cff0d-365">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="cff0d-365">Business scenario</span></span>
<span data-ttu-id="cff0d-366">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-366">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="cff0d-367">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-367">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="cff0d-368">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff0d-368">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="cff0d-369">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-369">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="cff0d-370">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-370">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="cff0d-371">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="cff0d-371">Implement a trigger</span></span>

1. <span data-ttu-id="cff0d-372">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-372">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="cff0d-373">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-373">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="cff0d-374">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-374">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="cff0d-375">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-375">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="cff0d-376">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-376">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="cff0d-377">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-377">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="cff0d-378">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-378">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="cff0d-379">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-379">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="cff0d-380">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="cff0d-380">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="cff0d-381">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-381">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="cff0d-382">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-382">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="cff0d-383">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-383">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="cff0d-384">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-384">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="cff0d-385">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-385">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="cff0d-386">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cff0d-386">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="cff0d-387">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff0d-387">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="cff0d-388">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-388">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="cff0d-389">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="cff0d-389">Override the CRT receipt request to generate the receipt data</span></span>

<span data-ttu-id="cff0d-390">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-390">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> <span data-ttu-id="cff0d-391">このセクションは、Microsoft Dynamics 365 for Finance and Operations またはプラットフォーム更新プログラム 8 を備えた Microsoft Dynamics 365 for Retail に適用可能です。</span><span class="sxs-lookup"><span data-stu-id="cff0d-391">This section is applicable to Microsoft Dynamics 365 for Finance and Operations or Microsoft Dynamics 365 for Retail with platform update 8.</span></span>

1. <span data-ttu-id="cff0d-392">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-392">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="cff0d-393">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-393">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="cff0d-394">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-394">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="cff0d-395">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-395">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="cff0d-396">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-396">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="cff0d-397">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-397">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="cff0d-398">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-398">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="cff0d-399">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-399">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="cff0d-400">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-400">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="cff0d-401">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="cff0d-401">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="cff0d-402">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff0d-402">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="cff0d-403">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="cff0d-403">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cff0d-404">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cff0d-404">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="cff0d-405">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="cff0d-405">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="cff0d-406">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-406">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="cff0d-407">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-407">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="cff0d-408">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-408">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="cff0d-409">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="cff0d-409">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="cff0d-410">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-410">Compile and build the project.</span></span>
12. <span data-ttu-id="cff0d-411">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-411">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="cff0d-412">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-412">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="cff0d-413">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-413">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="cff0d-414">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-414">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="cff0d-415">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-415">Save and close the file.</span></span>
17. <span data-ttu-id="cff0d-416">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="cff0d-416">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="cff0d-417">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="cff0d-417">Add the custom receipt layout</span></span>

1. <span data-ttu-id="cff0d-418">Dynamics 365 for Finance and Operations, Enterprise edition を開きます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-418">Open Dynamics 365 for Finance and Operations, Enterpise edition.</span></span>
2. <span data-ttu-id="cff0d-419">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-419">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="cff0d-420">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-420">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="cff0d-421">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-421">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="cff0d-422">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-422">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="cff0d-423">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-423">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="cff0d-424">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="cff0d-424">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="cff0d-425">デザイナーを起動する Azure Active Directory (AAD) の資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-425">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="cff0d-426">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-426">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="cff0d-427">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-427">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="cff0d-428">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-428">Click **Save**.</span></span>
9. <span data-ttu-id="cff0d-429">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-429">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="cff0d-430">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-430">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="cff0d-431">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-431">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="cff0d-432">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-432">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="cff0d-433">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-433">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="cff0d-434">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-434">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="cff0d-435">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-435">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="cff0d-436">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cff0d-436">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="cff0d-437">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-437">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="cff0d-438">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-438">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="cff0d-439">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-439">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="cff0d-440">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-440">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="cff0d-441">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-441">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="cff0d-442">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-442">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="cff0d-443">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-443">Click **Save**.</span></span>
6. <span data-ttu-id="cff0d-444">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-444">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="cff0d-445">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-445">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="cff0d-446">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-446">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="cff0d-447">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="cff0d-447">Validate the extension</span></span>

1. <span data-ttu-id="cff0d-448">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="cff0d-448">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="cff0d-449">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-449">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="cff0d-450">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="cff0d-450">Suspend the transaction.</span></span>
4. <span data-ttu-id="cff0d-451">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="cff0d-451">The custom receipt should print.</span></span>

