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
ms.openlocfilehash: 25aacafac8e0c6dd137e013fadded5a41abb2aee
ms.sourcegitcommit: dbf560d131ef5a230303ba7b9294e453b799dcc2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "403761"
---
# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="efa57-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="efa57-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efa57-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="efa57-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="efa57-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="efa57-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="efa57-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="efa57-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="efa57-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="efa57-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="efa57-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="efa57-108">Continue or cancel an operation.</span></span> <span data-ttu-id="efa57-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="efa57-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="efa57-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="efa57-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="efa57-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="efa57-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 

<span data-ttu-id="efa57-112">このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 for Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-112">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="efa57-113">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="efa57-113">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="efa57-114">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-114">Application triggers</span></span>

| <span data-ttu-id="efa57-115">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-115">Trigger</span></span>                   | <span data-ttu-id="efa57-116">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-116">Type</span></span>           | <span data-ttu-id="efa57-117">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-117">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="efa57-118">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-118">ApplicationStartTrigger</span></span>   | <span data-ttu-id="efa57-119">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-119">Non-cancelable</span></span> | <span data-ttu-id="efa57-120">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-120">Executed after the POS application is started.</span></span> <span data-ttu-id="efa57-121">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="efa57-121">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="efa57-122">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-122">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="efa57-123">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-123">Non-cancelable</span></span> | <span data-ttu-id="efa57-124">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-124">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="efa57-125">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-125">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="efa57-126">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-126">Cancelable</span></span>     | <span data-ttu-id="efa57-127">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-127">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="efa57-128">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-128">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="efa57-129">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-129">Non-cancelable</span></span> | <span data-ttu-id="efa57-130">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-130">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="efa57-131">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-131">PostLogOffTrigger</span></span>         | <span data-ttu-id="efa57-132">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-132">Non-cancelable</span></span> | <span data-ttu-id="efa57-133">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-133">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="efa57-134">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-134">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="efa57-135">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-135">Cancelable</span></span>     | <span data-ttu-id="efa57-136">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-136">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="efa57-137">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-137">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="efa57-138">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-138">Non-Cancelable</span></span> | <span data-ttu-id="efa57-139">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-139">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="efa57-140">PostDeviceActivation</span><span class="sxs-lookup"><span data-stu-id="efa57-140">PostDeviceActivation</span></span>      | <span data-ttu-id="efa57-141">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-141">Non-Cancelable</span></span> | <span data-ttu-id="efa57-142">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-142">Executed after the POS activation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="efa57-143">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-143">Cash management triggers</span></span>

| <span data-ttu-id="efa57-144">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-144">Trigger</span></span>                      | <span data-ttu-id="efa57-145">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-145">Type</span></span>           | <span data-ttu-id="efa57-146">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-146">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="efa57-147">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-147">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="efa57-148">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-148">Cancelable</span></span>     | <span data-ttu-id="efa57-149">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-149">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="efa57-150">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-150">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="efa57-151">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-151">Non-cancelable</span></span> | <span data-ttu-id="efa57-152">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-152">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="efa57-153">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-153">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="efa57-154">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-154">Cancelable</span></span>     | <span data-ttu-id="efa57-155">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-155">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="efa57-156">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-156">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="efa57-157">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-157">Non-cancelable</span></span> | <span data-ttu-id="efa57-158">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-158">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="efa57-159">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-159">Customer triggers</span></span>

| <span data-ttu-id="efa57-160">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-160">Trigger</span></span>                   | <span data-ttu-id="efa57-161">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-161">Type</span></span>                    | <span data-ttu-id="efa57-162">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-162">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="efa57-163">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-163">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="efa57-164">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-164">Cancelable</span></span>              | <span data-ttu-id="efa57-165">新しい顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-165">Executed before creating a new customer.</span></span>             |
| <span data-ttu-id="efa57-166">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-166">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="efa57-167">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-167">Non-cancelable</span></span>          | <span data-ttu-id="efa57-168">新しい顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-168">Executed after creating a new customer.</span></span>              |
| <span data-ttu-id="efa57-169">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-169">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="efa57-170">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-170">PreCustomerClearTrigger</span></span> | <span data-ttu-id="efa57-171">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-171">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="efa57-172">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-172">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="efa57-173">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-173">Non-cancelable</span></span>          | <span data-ttu-id="efa57-174">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-174">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="efa57-175">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-175">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="efa57-176">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-176">Cancelable</span></span>              | <span data-ttu-id="efa57-177">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-177">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="efa57-178">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-178">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="efa57-179">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-179">Cancelable</span></span>              | <span data-ttu-id="efa57-180">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-180">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="efa57-181">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-181">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="efa57-182">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-182">Non-cancelable</span></span>          | <span data-ttu-id="efa57-183">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-183">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="efa57-184">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-184">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="efa57-185">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-185">Non-cancelable</span></span>          | <span data-ttu-id="efa57-186">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-186">Executed after the loyalty card is issued.</span></span>       |

## <a name="discount-triggers"></a><span data-ttu-id="efa57-187">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-187">Discount triggers</span></span>

| <span data-ttu-id="efa57-188">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-188">Trigger</span></span>                         | <span data-ttu-id="efa57-189">型</span><span class="sxs-lookup"><span data-stu-id="efa57-189">Type</span></span>           | <span data-ttu-id="efa57-190">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-190">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="efa57-191">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-191">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="efa57-192">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-192">Cancelable</span></span>     | <span data-ttu-id="efa57-193">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-193">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="efa57-194">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-194">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="efa57-195">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-195">Non-cancelable</span></span> | <span data-ttu-id="efa57-196">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-196">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="efa57-197">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-197">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="efa57-198">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-198">Cancelable</span></span>     | <span data-ttu-id="efa57-199">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-199">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="efa57-200">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-200">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="efa57-201">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-201">Non-cancelable</span></span> | <span data-ttu-id="efa57-202">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-202">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="efa57-203">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-203">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="efa57-204">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-204">Cancelable</span></span>     | <span data-ttu-id="efa57-205">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-205">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="efa57-206">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-206">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="efa57-207">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-207">Non-cancelable</span></span> | <span data-ttu-id="efa57-208">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-208">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="efa57-209">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-209">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="efa57-210">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-210">Cancelable</span></span>     | <span data-ttu-id="efa57-211">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-211">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="efa57-212">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-212">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="efa57-213">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-213">Non-cancelable</span></span> | <span data-ttu-id="efa57-214">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-214">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="efa57-215">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-215">PreAddCouponTrigger</span></span>             | <span data-ttu-id="efa57-216">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-216">Cancelable</span></span>     | <span data-ttu-id="efa57-217">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-217">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="efa57-218">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-218">PostAddCouponTrigger</span></span>            | <span data-ttu-id="efa57-219">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-219">Non-cancelable</span></span> | <span data-ttu-id="efa57-220">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-220">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="efa57-221">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-221">Operation triggers</span></span>

| <span data-ttu-id="efa57-222">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-222">Trigger</span></span>              | <span data-ttu-id="efa57-223">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-223">Type</span></span>           | <span data-ttu-id="efa57-224">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-224">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="efa57-225">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-225">PreOperationTrigger</span></span>  | <span data-ttu-id="efa57-226">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-226">Cancelable</span></span>     | <span data-ttu-id="efa57-227">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="efa57-227">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="efa57-228">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="efa57-228">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="efa57-229">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-229">PreOperationValidationTrigger</span></span> | <span data-ttu-id="efa57-230">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-230">Cancelable</span></span> | <span data-ttu-id="efa57-231">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="efa57-231">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="efa57-232">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-232">OperationFailureTrigger</span></span> | <span data-ttu-id="efa57-233">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-233">Non-cancelable</span></span> | <span data-ttu-id="efa57-234">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="efa57-234">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="efa57-235">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-235">PostOperationTrigger</span></span> | <span data-ttu-id="efa57-236">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-236">Non-cancelable</span></span> | <span data-ttu-id="efa57-237">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="efa57-237">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="efa57-238">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="efa57-238">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="efa57-239">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-239">Payment triggers</span></span>

| <span data-ttu-id="efa57-240">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-240">Trigger</span></span>                 | <span data-ttu-id="efa57-241">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-241">Type</span></span>           | <span data-ttu-id="efa57-242">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-242">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="efa57-243">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-243">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="efa57-244">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-244">Cancelable</span></span>     | <span data-ttu-id="efa57-245">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-245">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="efa57-246">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-246">PrePaymentTrigger</span></span>       | <span data-ttu-id="efa57-247">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-247">Cancelable</span></span>     | <span data-ttu-id="efa57-248">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-248">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="efa57-249">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-249">PostPaymentTrigger</span></span>      | <span data-ttu-id="efa57-250">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-250">Non-cancelable</span></span> | <span data-ttu-id="efa57-251">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-251">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="efa57-252">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-252">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="efa57-253">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-253">Cancelable</span></span>     | <span data-ttu-id="efa57-254">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-254">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="efa57-255">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-255">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="efa57-256">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-256">Non-cancelable</span></span> | <span data-ttu-id="efa57-257">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-257">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="efa57-258">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-258">Printing Triggers</span></span>

| <span data-ttu-id="efa57-259">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-259">Trigger</span></span>                    | <span data-ttu-id="efa57-260">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-260">Type</span></span>       | <span data-ttu-id="efa57-261">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-261">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="efa57-262">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-262">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="efa57-263">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-263">Cancelable</span></span> | <span data-ttu-id="efa57-264">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-264">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="efa57-265">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-265">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="efa57-266">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-266">Non-cancelable</span></span> | <span data-ttu-id="efa57-267">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-267">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="efa57-268">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-268">Product triggers</span></span>

| <span data-ttu-id="efa57-269">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-269">Trigger</span></span>                    | <span data-ttu-id="efa57-270">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-270">Type</span></span>           | <span data-ttu-id="efa57-271">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-271">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="efa57-272">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-272">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="efa57-273">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-273">Non-cancelable</span></span> | <span data-ttu-id="efa57-274">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-274">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="efa57-275">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-275">PreProductSaleTrigger</span></span>      | <span data-ttu-id="efa57-276">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-276">Cancelable</span></span>     | <span data-ttu-id="efa57-277">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-277">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="efa57-278">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-278">PostProductSaleTrigger</span></span>     | <span data-ttu-id="efa57-279">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-279">Non-cancelable</span></span> | <span data-ttu-id="efa57-280">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-280">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="efa57-281">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-281">PreReturnProductTrigger</span></span>    | <span data-ttu-id="efa57-282">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-282">Cancelable</span></span>     | <span data-ttu-id="efa57-283">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-283">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="efa57-284">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-284">PostReturnProductTrigger</span></span>   | <span data-ttu-id="efa57-285">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-285">Non-cancelable</span></span> | <span data-ttu-id="efa57-286">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-286">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="efa57-287">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-287">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="efa57-288">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-288">Cancelable</span></span>     | <span data-ttu-id="efa57-289">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-289">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="efa57-290">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-290">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="efa57-291">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-291">Non-cancelable</span></span> | <span data-ttu-id="efa57-292">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-292">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="efa57-293">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-293">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="efa57-294">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-294">Cancelable</span></span>     | <span data-ttu-id="efa57-295">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-295">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="efa57-296">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-296">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="efa57-297">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-297">Non-cancelable</span></span> | <span data-ttu-id="efa57-298">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-298">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="efa57-299">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-299">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="efa57-300">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-300">Cancelable</span></span>     | <span data-ttu-id="efa57-301">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-301">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="efa57-302">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-302">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="efa57-303">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-303">Non-cancelable</span></span> | <span data-ttu-id="efa57-304">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-304">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="efa57-305">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-305">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="efa57-306">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-306">Cancelable</span></span>     | <span data-ttu-id="efa57-307">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-307">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="efa57-308">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-308">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="efa57-309">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-309">Non-cancelable</span></span> | <span data-ttu-id="efa57-310">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-310">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="efa57-311">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-311">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="efa57-312">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-312">Non-cancelable</span></span> | <span data-ttu-id="efa57-313">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-313">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="efa57-314">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-314">Sales order triggers</span></span>

| <span data-ttu-id="efa57-315">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-315">Trigger</span></span>                 | <span data-ttu-id="efa57-316">型</span><span class="sxs-lookup"><span data-stu-id="efa57-316">Type</span></span>           | <span data-ttu-id="efa57-317">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-317">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="efa57-318">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-318">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="efa57-319">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-319">Cancelable</span></span>     | <span data-ttu-id="efa57-320">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-320">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="efa57-321">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-321">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="efa57-322">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-322">Non-cancelable</span></span> | <span data-ttu-id="efa57-323">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-323">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="efa57-324">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-324">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="efa57-325">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-325">Cancelable</span></span>     | <span data-ttu-id="efa57-326">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-326">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="efa57-327">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-327">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="efa57-328">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-328">Cancelable</span></span>     | <span data-ttu-id="efa57-329">顧客先発注時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-329">Executed before the shipping origin is changed during customer order.</span></span>|

## <a name="shift-triggers"></a><span data-ttu-id="efa57-330">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-330">Shift triggers</span></span>
| <span data-ttu-id="efa57-331">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-331">Trigger</span></span>              | <span data-ttu-id="efa57-332">型</span><span class="sxs-lookup"><span data-stu-id="efa57-332">Type</span></span>           | <span data-ttu-id="efa57-333">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-333">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="efa57-334">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-334">PostOpenShiftTrigger</span></span> | <span data-ttu-id="efa57-335">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-335">Non-cancelable</span></span> | <span data-ttu-id="efa57-336">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-336">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="efa57-337">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-337">Tax override triggers</span></span>

| <span data-ttu-id="efa57-338">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-338">Trigger</span></span>                           | <span data-ttu-id="efa57-339">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-339">Type</span></span>           | <span data-ttu-id="efa57-340">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-340">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="efa57-341">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-341">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="efa57-342">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-342">Cancelable</span></span>     | <span data-ttu-id="efa57-343">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-343">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="efa57-344">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-344">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="efa57-345">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-345">Non-cancelable</span></span> | <span data-ttu-id="efa57-346">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-346">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="efa57-347">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-347">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="efa57-348">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-348">Cancelable</span></span>     | <span data-ttu-id="efa57-349">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-349">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="efa57-350">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-350">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="efa57-351">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-351">Non-cancelable</span></span> | <span data-ttu-id="efa57-352">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-352">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="efa57-353">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-353">Transaction triggers</span></span>

| <span data-ttu-id="efa57-354">トリガー</span><span class="sxs-lookup"><span data-stu-id="efa57-354">Trigger</span></span>                            | <span data-ttu-id="efa57-355">種類</span><span class="sxs-lookup"><span data-stu-id="efa57-355">Type</span></span>           | <span data-ttu-id="efa57-356">説明</span><span class="sxs-lookup"><span data-stu-id="efa57-356">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="efa57-357">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-357">BeginTransactionTrigger</span></span>            | <span data-ttu-id="efa57-358">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-358">Non-cancelable</span></span> | <span data-ttu-id="efa57-359">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-359">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="efa57-360">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-360">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="efa57-361">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-361">Cancelable</span></span>     | <span data-ttu-id="efa57-362">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-362">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="efa57-363">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-363">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="efa57-364">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-364">Cancelable</span></span>     | <span data-ttu-id="efa57-365">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-365">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="efa57-366">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-366">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="efa57-367">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-367">Non-cancelable</span></span> | <span data-ttu-id="efa57-368">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-368">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="efa57-369">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-369">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="efa57-370">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-370">Cancelable</span></span>     | <span data-ttu-id="efa57-371">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="efa57-371">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="efa57-372">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-372">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="efa57-373">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-373">Non-cancelable</span></span> | <span data-ttu-id="efa57-374">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="efa57-374">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="efa57-375">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-375">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="efa57-376">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-376">Cancelable</span></span>     | <span data-ttu-id="efa57-377">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-377">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="efa57-378">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-378">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="efa57-379">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-379">Non-cancelable</span></span> | <span data-ttu-id="efa57-380">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-380">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="efa57-381">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-381">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="efa57-382">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-382">Cancelable</span></span>     | <span data-ttu-id="efa57-383">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-383">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="efa57-384">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-384">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="efa57-385">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-385">Non-cancelable</span></span> | <span data-ttu-id="efa57-386">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-386">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="efa57-387">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-387">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="efa57-388">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-388">Cancelable</span></span>     | <span data-ttu-id="efa57-389">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-389">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="efa57-390">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-390">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="efa57-391">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-391">Non-cancelable</span></span> | <span data-ttu-id="efa57-392">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-392">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="efa57-393">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-393">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="efa57-394">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-394">Non-cancelable</span></span> | <span data-ttu-id="efa57-395">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-395">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="efa57-396">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-396">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="efa57-397">解約可能</span><span class="sxs-lookup"><span data-stu-id="efa57-397">Cancelable</span></span>     | <span data-ttu-id="efa57-398">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-398">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="efa57-399">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="efa57-399">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="efa57-400">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="efa57-400">Non-Cancelable</span></span> | <span data-ttu-id="efa57-401">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-401">Executed after the customer order is recalled.</span></span>        |

## <a name="business-scenario"></a><span data-ttu-id="efa57-402">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="efa57-402">Business scenario</span></span>
<span data-ttu-id="efa57-403">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-403">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="efa57-404">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="efa57-404">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="efa57-405">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="efa57-405">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="efa57-406">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="efa57-406">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="efa57-407">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="efa57-407">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="efa57-408">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="efa57-408">Implement a trigger</span></span>

1. <span data-ttu-id="efa57-409">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="efa57-409">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="efa57-410">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="efa57-410">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="efa57-411">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="efa57-411">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="efa57-412">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="efa57-412">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="efa57-413">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="efa57-413">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="efa57-414">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="efa57-414">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="efa57-415">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="efa57-415">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="efa57-416">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="efa57-416">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="efa57-417">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="efa57-417">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="efa57-418">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="efa57-418">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="efa57-419">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="efa57-419">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="efa57-420">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="efa57-420">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="efa57-421">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="efa57-421">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="efa57-422">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="efa57-422">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="efa57-423">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="efa57-423">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="efa57-424">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="efa57-424">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="efa57-425">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="efa57-425">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="efa57-426">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="efa57-426">Override the CRT receipt request to generate the receipt data</span></span>

<span data-ttu-id="efa57-427">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="efa57-427">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> <span data-ttu-id="efa57-428">このセクションでは、Microsoft Dynamics 365 for Finance and Operations または Microsoft Dynamics 365 for Retail プラットフォーム更新プログラム 8 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-428">This section is applicable to Microsoft Dynamics 365 for Finance and Operations or Microsoft Dynamics 365 for Retail with platform update 8.</span></span>

1. <span data-ttu-id="efa57-429">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-429">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="efa57-430">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="efa57-430">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="efa57-431">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="efa57-431">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="efa57-432">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="efa57-432">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="efa57-433">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="efa57-433">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="efa57-434">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="efa57-434">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="efa57-435">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="efa57-435">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="efa57-436">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="efa57-436">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="efa57-437">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="efa57-437">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="efa57-438">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="efa57-438">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="efa57-439">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efa57-439">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="efa57-440">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="efa57-440">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efa57-441">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="efa57-441">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="efa57-442">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="efa57-442">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="efa57-443">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="efa57-443">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="efa57-444">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="efa57-444">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="efa57-445">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="efa57-445">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="efa57-446">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="efa57-446">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="efa57-447">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="efa57-447">Compile and build the project.</span></span>
12. <span data-ttu-id="efa57-448">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="efa57-448">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="efa57-449">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="efa57-449">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="efa57-450">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="efa57-450">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="efa57-451">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="efa57-451">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="efa57-452">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="efa57-452">Save and close the file.</span></span>
17. <span data-ttu-id="efa57-453">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="efa57-453">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="efa57-454">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="efa57-454">Add the custom receipt layout</span></span>

1. <span data-ttu-id="efa57-455">Dynamics 365 for Finance and Operations Enterprise Edition を開きます。</span><span class="sxs-lookup"><span data-stu-id="efa57-455">Open Dynamics 365 for Finance and Operations, Enterpise edition.</span></span>
2. <span data-ttu-id="efa57-456">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-456">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="efa57-457">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-457">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="efa57-458">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="efa57-458">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="efa57-459">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="efa57-459">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="efa57-460">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="efa57-460">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="efa57-461">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="efa57-461">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="efa57-462">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-462">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="efa57-463">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="efa57-463">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="efa57-464">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="efa57-464">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="efa57-465">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-465">Click **Save**.</span></span>
9. <span data-ttu-id="efa57-466">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-466">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="efa57-467">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="efa57-467">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="efa57-468">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-468">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="efa57-469">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="efa57-469">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="efa57-470">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-470">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="efa57-471">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-471">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="efa57-472">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="efa57-472">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="efa57-473">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="efa57-473">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="efa57-474">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-474">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="efa57-475">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="efa57-475">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="efa57-476">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="efa57-476">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="efa57-477">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-477">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="efa57-478">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="efa57-478">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="efa57-479">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="efa57-479">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="efa57-480">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-480">Click **Save**.</span></span>
6. <span data-ttu-id="efa57-481">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="efa57-481">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="efa57-482">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="efa57-482">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="efa57-483">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="efa57-483">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="efa57-484">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="efa57-484">Validate the extension</span></span>

1. <span data-ttu-id="efa57-485">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="efa57-485">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="efa57-486">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="efa57-486">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="efa57-487">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="efa57-487">Suspend the transaction.</span></span>
4. <span data-ttu-id="efa57-488">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="efa57-488">The custom receipt should print.</span></span>
