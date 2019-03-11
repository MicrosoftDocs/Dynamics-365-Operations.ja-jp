---
title: Retail Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 01/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: bfc4ef7d73ddf44e730a4c28dc46960d4afa5e6c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369410"
---
# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="d5e37-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="d5e37-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5e37-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="d5e37-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="d5e37-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="d5e37-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="d5e37-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-108">Continue or cancel an operation.</span></span> <span data-ttu-id="d5e37-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="d5e37-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="d5e37-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="d5e37-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 

<span data-ttu-id="d5e37-112">このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 for Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-112">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="d5e37-113">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="d5e37-113">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="d5e37-114">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-114">Application triggers</span></span>

| <span data-ttu-id="d5e37-115">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-115">Trigger</span></span>                   | <span data-ttu-id="d5e37-116">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-116">Type</span></span>           | <span data-ttu-id="d5e37-117">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-117">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="d5e37-118">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-118">ApplicationStartTrigger</span></span>   | <span data-ttu-id="d5e37-119">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-119">Non-cancelable</span></span> | <span data-ttu-id="d5e37-120">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-120">Executed after the POS application is started.</span></span> <span data-ttu-id="d5e37-121">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-121">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="d5e37-122">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-122">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="d5e37-123">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-123">Non-cancelable</span></span> | <span data-ttu-id="d5e37-124">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-124">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="d5e37-125">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-125">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="d5e37-126">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-126">Cancelable</span></span>     | <span data-ttu-id="d5e37-127">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-127">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="d5e37-128">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-128">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="d5e37-129">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-129">Non-cancelable</span></span> | <span data-ttu-id="d5e37-130">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-130">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="d5e37-131">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-131">PostLogOffTrigger</span></span>         | <span data-ttu-id="d5e37-132">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-132">Non-cancelable</span></span> | <span data-ttu-id="d5e37-133">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-133">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="d5e37-134">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-134">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="d5e37-135">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-135">Cancelable</span></span>     | <span data-ttu-id="d5e37-136">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-136">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="d5e37-137">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-137">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="d5e37-138">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-138">Non-Cancelable</span></span> | <span data-ttu-id="d5e37-139">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-139">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="d5e37-140">PostDeviceActivation</span><span class="sxs-lookup"><span data-stu-id="d5e37-140">PostDeviceActivation</span></span>      | <span data-ttu-id="d5e37-141">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-141">Non-Cancelable</span></span> | <span data-ttu-id="d5e37-142">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-142">Executed after the POS activation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="d5e37-143">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-143">Cash management triggers</span></span>

| <span data-ttu-id="d5e37-144">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-144">Trigger</span></span>                      | <span data-ttu-id="d5e37-145">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-145">Type</span></span>           | <span data-ttu-id="d5e37-146">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-146">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="d5e37-147">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-147">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="d5e37-148">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-148">Cancelable</span></span>     | <span data-ttu-id="d5e37-149">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-149">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="d5e37-150">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-150">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="d5e37-151">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-151">Non-cancelable</span></span> | <span data-ttu-id="d5e37-152">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-152">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="d5e37-153">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-153">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="d5e37-154">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-154">Cancelable</span></span>     | <span data-ttu-id="d5e37-155">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-155">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="d5e37-156">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-156">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="d5e37-157">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-157">Non-cancelable</span></span> | <span data-ttu-id="d5e37-158">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-158">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="d5e37-159">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-159">Customer triggers</span></span>

| <span data-ttu-id="d5e37-160">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-160">Trigger</span></span>                   | <span data-ttu-id="d5e37-161">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-161">Type</span></span>                    | <span data-ttu-id="d5e37-162">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-162">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d5e37-163">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-163">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="d5e37-164">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-164">Cancelable</span></span>              | <span data-ttu-id="d5e37-165">新しい顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-165">Executed before creating a new customer.</span></span>             |
| <span data-ttu-id="d5e37-166">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-166">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="d5e37-167">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-167">Non-cancelable</span></span>          | <span data-ttu-id="d5e37-168">新しい顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-168">Executed after creating a new customer.</span></span>              |
| <span data-ttu-id="d5e37-169">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-169">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="d5e37-170">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-170">PreCustomerClearTrigger</span></span> | <span data-ttu-id="d5e37-171">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-171">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="d5e37-172">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-172">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="d5e37-173">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-173">Non-cancelable</span></span>          | <span data-ttu-id="d5e37-174">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-174">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="d5e37-175">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-175">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="d5e37-176">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-176">Cancelable</span></span>              | <span data-ttu-id="d5e37-177">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-177">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="d5e37-178">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-178">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="d5e37-179">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-179">Cancelable</span></span>              | <span data-ttu-id="d5e37-180">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-180">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="d5e37-181">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-181">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="d5e37-182">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-182">Non-cancelable</span></span>          | <span data-ttu-id="d5e37-183">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-183">Executed after customer search is performed.</span></span>       |

## <a name="discount-triggers"></a><span data-ttu-id="d5e37-184">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-184">Discount triggers</span></span>

| <span data-ttu-id="d5e37-185">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-185">Trigger</span></span>                         | <span data-ttu-id="d5e37-186">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-186">Type</span></span>           | <span data-ttu-id="d5e37-187">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-187">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d5e37-188">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-188">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="d5e37-189">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-189">Cancelable</span></span>     | <span data-ttu-id="d5e37-190">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-190">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="d5e37-191">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-191">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="d5e37-192">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-192">Non-cancelable</span></span> | <span data-ttu-id="d5e37-193">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-193">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="d5e37-194">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-194">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="d5e37-195">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-195">Cancelable</span></span>     | <span data-ttu-id="d5e37-196">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-196">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="d5e37-197">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-197">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="d5e37-198">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-198">Non-cancelable</span></span> | <span data-ttu-id="d5e37-199">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-199">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="d5e37-200">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-200">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="d5e37-201">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-201">Cancelable</span></span>     | <span data-ttu-id="d5e37-202">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-202">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d5e37-203">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-203">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="d5e37-204">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-204">Non-cancelable</span></span> | <span data-ttu-id="d5e37-205">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-205">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="d5e37-206">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-206">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="d5e37-207">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-207">Cancelable</span></span>     | <span data-ttu-id="d5e37-208">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-208">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d5e37-209">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-209">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="d5e37-210">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-210">Non-cancelable</span></span> | <span data-ttu-id="d5e37-211">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-211">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="d5e37-212">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-212">PreAddCouponTrigger</span></span>             | <span data-ttu-id="d5e37-213">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-213">Cancelable</span></span>     | <span data-ttu-id="d5e37-214">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-214">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="d5e37-215">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-215">PostAddCouponTrigger</span></span>            | <span data-ttu-id="d5e37-216">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-216">Non-cancelable</span></span> | <span data-ttu-id="d5e37-217">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-217">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="d5e37-218">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-218">Operation triggers</span></span>

| <span data-ttu-id="d5e37-219">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-219">Trigger</span></span>              | <span data-ttu-id="d5e37-220">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-220">Type</span></span>           | <span data-ttu-id="d5e37-221">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-221">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="d5e37-222">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-222">PreOperationTrigger</span></span>  | <span data-ttu-id="d5e37-223">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-223">Cancelable</span></span>     | <span data-ttu-id="d5e37-224">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d5e37-224">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="d5e37-225">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-225">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="d5e37-226">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-226">PostOperationTrigger</span></span> | <span data-ttu-id="d5e37-227">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-227">Non-cancelable</span></span> | <span data-ttu-id="d5e37-228">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d5e37-228">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="d5e37-229">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-229">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="d5e37-230">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-230">Payment triggers</span></span>

| <span data-ttu-id="d5e37-231">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-231">Trigger</span></span>                 | <span data-ttu-id="d5e37-232">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-232">Type</span></span>           | <span data-ttu-id="d5e37-233">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-233">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d5e37-234">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-234">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="d5e37-235">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-235">Cancelable</span></span>     | <span data-ttu-id="d5e37-236">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-236">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="d5e37-237">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-237">PrePaymentTrigger</span></span>       | <span data-ttu-id="d5e37-238">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-238">Cancelable</span></span>     | <span data-ttu-id="d5e37-239">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-239">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="d5e37-240">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-240">PostPaymentTrigger</span></span>      | <span data-ttu-id="d5e37-241">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-241">Non-cancelable</span></span> | <span data-ttu-id="d5e37-242">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-242">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="d5e37-243">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-243">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="d5e37-244">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-244">Cancelable</span></span>     | <span data-ttu-id="d5e37-245">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-245">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="d5e37-246">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-246">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="d5e37-247">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-247">Non-cancelable</span></span> | <span data-ttu-id="d5e37-248">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-248">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="d5e37-249">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-249">Printing Triggers</span></span>

| <span data-ttu-id="d5e37-250">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-250">Trigger</span></span>                    | <span data-ttu-id="d5e37-251">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-251">Type</span></span>       | <span data-ttu-id="d5e37-252">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-252">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="d5e37-253">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-253">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="d5e37-254">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-254">Cancelable</span></span> | <span data-ttu-id="d5e37-255">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-255">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="d5e37-256">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-256">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="d5e37-257">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-257">Non-cancelable</span></span> | <span data-ttu-id="d5e37-258">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-258">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="d5e37-259">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-259">Product triggers</span></span>

| <span data-ttu-id="d5e37-260">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-260">Trigger</span></span>                    | <span data-ttu-id="d5e37-261">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-261">Type</span></span>           | <span data-ttu-id="d5e37-262">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-262">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e37-263">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-263">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="d5e37-264">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-264">Non-cancelable</span></span> | <span data-ttu-id="d5e37-265">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-265">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="d5e37-266">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-266">PreProductSaleTrigger</span></span>      | <span data-ttu-id="d5e37-267">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-267">Cancelable</span></span>     | <span data-ttu-id="d5e37-268">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-268">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="d5e37-269">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-269">PostProductSaleTrigger</span></span>     | <span data-ttu-id="d5e37-270">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-270">Non-cancelable</span></span> | <span data-ttu-id="d5e37-271">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-271">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="d5e37-272">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-272">PreReturnProductTrigger</span></span>    | <span data-ttu-id="d5e37-273">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-273">Cancelable</span></span>     | <span data-ttu-id="d5e37-274">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-274">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="d5e37-275">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-275">PostReturnProductTrigger</span></span>   | <span data-ttu-id="d5e37-276">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-276">Non-cancelable</span></span> | <span data-ttu-id="d5e37-277">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-277">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="d5e37-278">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-278">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="d5e37-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-279">Cancelable</span></span>     | <span data-ttu-id="d5e37-280">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-280">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="d5e37-281">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-281">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="d5e37-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-282">Non-cancelable</span></span> | <span data-ttu-id="d5e37-283">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-283">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="d5e37-284">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-284">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="d5e37-285">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-285">Cancelable</span></span>     | <span data-ttu-id="d5e37-286">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-286">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="d5e37-287">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-287">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="d5e37-288">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-288">Non-cancelable</span></span> | <span data-ttu-id="d5e37-289">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-289">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="d5e37-290">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-290">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="d5e37-291">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-291">Cancelable</span></span>     | <span data-ttu-id="d5e37-292">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-292">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="d5e37-293">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-293">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="d5e37-294">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-294">Non-cancelable</span></span> | <span data-ttu-id="d5e37-295">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-295">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="d5e37-296">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-296">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="d5e37-297">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-297">Cancelable</span></span>     | <span data-ttu-id="d5e37-298">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-298">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="d5e37-299">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-299">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="d5e37-300">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-300">Non-cancelable</span></span> | <span data-ttu-id="d5e37-301">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-301">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="d5e37-302">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-302">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="d5e37-303">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-303">Non-cancelable</span></span> | <span data-ttu-id="d5e37-304">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-304">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="d5e37-305">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-305">Sales order triggers</span></span>

| <span data-ttu-id="d5e37-306">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-306">Trigger</span></span>                 | <span data-ttu-id="d5e37-307">型</span><span class="sxs-lookup"><span data-stu-id="d5e37-307">Type</span></span>           | <span data-ttu-id="d5e37-308">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-308">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d5e37-309">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-309">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="d5e37-310">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-310">Cancelable</span></span>     | <span data-ttu-id="d5e37-311">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-311">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="d5e37-312">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-312">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="d5e37-313">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-313">Non-cancelable</span></span> | <span data-ttu-id="d5e37-314">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-314">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="d5e37-315">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-315">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="d5e37-316">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-316">Cancelable</span></span>     | <span data-ttu-id="d5e37-317">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-317">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="d5e37-318">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-318">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="d5e37-319">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-319">Cancelable</span></span>     | <span data-ttu-id="d5e37-320">顧客先発注時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-320">Executed before the shipping origin is changed during customer order.</span></span>|

## <a name="shift-triggers"></a><span data-ttu-id="d5e37-321">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-321">Shift triggers</span></span>
| <span data-ttu-id="d5e37-322">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-322">Trigger</span></span>              | <span data-ttu-id="d5e37-323">型</span><span class="sxs-lookup"><span data-stu-id="d5e37-323">Type</span></span>           | <span data-ttu-id="d5e37-324">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-324">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d5e37-325">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-325">PostOpenShiftTrigger</span></span> | <span data-ttu-id="d5e37-326">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-326">Non-cancelable</span></span> | <span data-ttu-id="d5e37-327">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-327">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="d5e37-328">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-328">Tax override triggers</span></span>

| <span data-ttu-id="d5e37-329">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-329">Trigger</span></span>                           | <span data-ttu-id="d5e37-330">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-330">Type</span></span>           | <span data-ttu-id="d5e37-331">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-331">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="d5e37-332">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-332">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="d5e37-333">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-333">Cancelable</span></span>     | <span data-ttu-id="d5e37-334">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-334">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="d5e37-335">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-335">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="d5e37-336">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-336">Non-cancelable</span></span> | <span data-ttu-id="d5e37-337">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-337">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="d5e37-338">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-338">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="d5e37-339">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-339">Cancelable</span></span>     | <span data-ttu-id="d5e37-340">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-340">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="d5e37-341">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-341">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="d5e37-342">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-342">Non-cancelable</span></span> | <span data-ttu-id="d5e37-343">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-343">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="d5e37-344">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-344">Transaction triggers</span></span>

| <span data-ttu-id="d5e37-345">トリガー</span><span class="sxs-lookup"><span data-stu-id="d5e37-345">Trigger</span></span>                            | <span data-ttu-id="d5e37-346">種類</span><span class="sxs-lookup"><span data-stu-id="d5e37-346">Type</span></span>           | <span data-ttu-id="d5e37-347">説明</span><span class="sxs-lookup"><span data-stu-id="d5e37-347">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="d5e37-348">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-348">BeginTransactionTrigger</span></span>            | <span data-ttu-id="d5e37-349">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-349">Non-cancelable</span></span> | <span data-ttu-id="d5e37-350">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-350">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="d5e37-351">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-351">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="d5e37-352">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-352">Cancelable</span></span>     | <span data-ttu-id="d5e37-353">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-353">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="d5e37-354">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-354">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="d5e37-355">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-355">Cancelable</span></span>     | <span data-ttu-id="d5e37-356">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-356">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="d5e37-357">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-357">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="d5e37-358">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-358">Non-cancelable</span></span> | <span data-ttu-id="d5e37-359">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-359">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="d5e37-360">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-360">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="d5e37-361">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-361">Cancelable</span></span>     | <span data-ttu-id="d5e37-362">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-362">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="d5e37-363">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-363">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="d5e37-364">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-364">Non-cancelable</span></span> | <span data-ttu-id="d5e37-365">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-365">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="d5e37-366">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-366">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="d5e37-367">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-367">Cancelable</span></span>     | <span data-ttu-id="d5e37-368">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-368">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="d5e37-369">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-369">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="d5e37-370">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-370">Non-cancelable</span></span> | <span data-ttu-id="d5e37-371">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-371">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="d5e37-372">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-372">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="d5e37-373">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-373">Cancelable</span></span>     | <span data-ttu-id="d5e37-374">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-374">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="d5e37-375">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-375">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="d5e37-376">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-376">Non-cancelable</span></span> | <span data-ttu-id="d5e37-377">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-377">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="d5e37-378">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-378">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d5e37-379">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-379">Cancelable</span></span>     | <span data-ttu-id="d5e37-380">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-380">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="d5e37-381">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-381">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d5e37-382">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-382">Non-cancelable</span></span> | <span data-ttu-id="d5e37-383">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-383">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="d5e37-384">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-384">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="d5e37-385">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-385">Non-cancelable</span></span> | <span data-ttu-id="d5e37-386">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-386">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="d5e37-387">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-387">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d5e37-388">解約可能</span><span class="sxs-lookup"><span data-stu-id="d5e37-388">Cancelable</span></span>     | <span data-ttu-id="d5e37-389">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-389">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="d5e37-390">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d5e37-390">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d5e37-391">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d5e37-391">Non-Cancelable</span></span> | <span data-ttu-id="d5e37-392">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-392">Executed after the customer order is recalled.</span></span>        |

## <a name="business-scenario"></a><span data-ttu-id="d5e37-393">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="d5e37-393">Business scenario</span></span>
<span data-ttu-id="d5e37-394">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-394">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="d5e37-395">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-395">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="d5e37-396">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e37-396">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="d5e37-397">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-397">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="d5e37-398">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-398">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="d5e37-399">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="d5e37-399">Implement a trigger</span></span>

1. <span data-ttu-id="d5e37-400">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-400">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="d5e37-401">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-401">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="d5e37-402">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-402">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d5e37-403">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-403">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="d5e37-404">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-404">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="d5e37-405">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-405">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="d5e37-406">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-406">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="d5e37-407">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-407">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="d5e37-408">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d5e37-408">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="d5e37-409">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-409">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="d5e37-410">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-410">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="d5e37-411">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-411">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="d5e37-412">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-412">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="d5e37-413">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-413">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="d5e37-414">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5e37-414">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="d5e37-415">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e37-415">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="d5e37-416">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-416">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="d5e37-417">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="d5e37-417">Override the CRT receipt request to generate the receipt data</span></span>

<span data-ttu-id="d5e37-418">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-418">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> <span data-ttu-id="d5e37-419">このセクションでは、Microsoft Dynamics 365 for Finance and Operations または Microsoft Dynamics 365 for Retail プラットフォーム更新プログラム 8 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-419">This section is applicable to Microsoft Dynamics 365 for Finance and Operations or Microsoft Dynamics 365 for Retail with platform update 8.</span></span>

1. <span data-ttu-id="d5e37-420">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-420">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="d5e37-421">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-421">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="d5e37-422">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-422">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="d5e37-423">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-423">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d5e37-424">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-424">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="d5e37-425">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-425">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="d5e37-426">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-426">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="d5e37-427">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-427">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="d5e37-428">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-428">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="d5e37-429">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="d5e37-429">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="d5e37-430">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e37-430">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="d5e37-431">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="d5e37-431">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5e37-432">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d5e37-432">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="d5e37-433">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="d5e37-433">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="d5e37-434">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-434">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="d5e37-435">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-435">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="d5e37-436">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-436">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="d5e37-437">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d5e37-437">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="d5e37-438">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-438">Compile and build the project.</span></span>
12. <span data-ttu-id="d5e37-439">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-439">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="d5e37-440">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-440">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="d5e37-441">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-441">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="d5e37-442">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-442">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="d5e37-443">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-443">Save and close the file.</span></span>
17. <span data-ttu-id="d5e37-444">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="d5e37-444">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="d5e37-445">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="d5e37-445">Add the custom receipt layout</span></span>

1. <span data-ttu-id="d5e37-446">Dynamics 365 for Finance and Operations Enterprise Edition を開きます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-446">Open Dynamics 365 for Finance and Operations, Enterpise edition.</span></span>
2. <span data-ttu-id="d5e37-447">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-447">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="d5e37-448">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-448">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="d5e37-449">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-449">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="d5e37-450">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-450">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="d5e37-451">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-451">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="d5e37-452">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="d5e37-452">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="d5e37-453">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-453">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="d5e37-454">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-454">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="d5e37-455">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-455">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="d5e37-456">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-456">Click **Save**.</span></span>
9. <span data-ttu-id="d5e37-457">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-457">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="d5e37-458">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-458">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="d5e37-459">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-459">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="d5e37-460">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-460">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="d5e37-461">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-461">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="d5e37-462">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-462">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d5e37-463">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-463">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="d5e37-464">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d5e37-464">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="d5e37-465">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-465">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="d5e37-466">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-466">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="d5e37-467">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-467">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="d5e37-468">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-468">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="d5e37-469">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-469">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="d5e37-470">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-470">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="d5e37-471">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-471">Click **Save**.</span></span>
6. <span data-ttu-id="d5e37-472">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-472">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="d5e37-473">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-473">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d5e37-474">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-474">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="d5e37-475">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="d5e37-475">Validate the extension</span></span>

1. <span data-ttu-id="d5e37-476">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="d5e37-476">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="d5e37-477">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-477">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="d5e37-478">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="d5e37-478">Suspend the transaction.</span></span>
4. <span data-ttu-id="d5e37-479">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d5e37-479">The custom receipt should print.</span></span>
