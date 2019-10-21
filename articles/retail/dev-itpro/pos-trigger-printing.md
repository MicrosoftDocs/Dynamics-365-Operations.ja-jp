---
title: Retail Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 08/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: 2b45b806a2aabda5d933cd25edcea9bc87d67e38
ms.sourcegitcommit: 2555acfd855fc18ff3ba432ba2cf7633a8f1653c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2019
ms.locfileid: "2238560"
---
# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="f051e-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="f051e-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f051e-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="f051e-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="f051e-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f051e-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="f051e-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="f051e-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="f051e-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f051e-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="f051e-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="f051e-108">Continue or cancel an operation.</span></span> <span data-ttu-id="f051e-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="f051e-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="f051e-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="f051e-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="f051e-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="f051e-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="f051e-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f051e-112">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="f051e-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-113">Application triggers</span></span>

| <span data-ttu-id="f051e-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-114">Trigger</span></span>                   | <span data-ttu-id="f051e-115">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-115">Type</span></span>           | <span data-ttu-id="f051e-116">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="f051e-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="f051e-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-118">Non-cancelable</span></span> | <span data-ttu-id="f051e-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-119">Executed after the POS application is started.</span></span> <span data-ttu-id="f051e-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="f051e-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="f051e-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="f051e-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-122">Non-cancelable</span></span> | <span data-ttu-id="f051e-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="f051e-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="f051e-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-125">Cancelable</span></span>     | <span data-ttu-id="f051e-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="f051e-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="f051e-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-128">Non-cancelable</span></span> | <span data-ttu-id="f051e-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="f051e-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="f051e-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-131">Non-cancelable</span></span> | <span data-ttu-id="f051e-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="f051e-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="f051e-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-134">Cancelable</span></span>     | <span data-ttu-id="f051e-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="f051e-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="f051e-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-137">Non-Cancelable</span></span> | <span data-ttu-id="f051e-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="f051e-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="f051e-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-140">Cancelable</span></span>     | <span data-ttu-id="f051e-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="f051e-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="f051e-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-143">Non-Cancelable</span></span> | <span data-ttu-id="f051e-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="f051e-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="f051e-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-146">Cancelable</span></span> | <span data-ttu-id="f051e-147">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-147">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="f051e-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="f051e-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-149">Cancelable</span></span> | <span data-ttu-id="f051e-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="f051e-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="f051e-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-152">Non-Cancelable</span></span> | <span data-ttu-id="f051e-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-153">Executed after the audit event.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="f051e-154">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-154">Cash management triggers</span></span>

| <span data-ttu-id="f051e-155">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-155">Trigger</span></span>                      | <span data-ttu-id="f051e-156">型</span><span class="sxs-lookup"><span data-stu-id="f051e-156">Type</span></span>           | <span data-ttu-id="f051e-157">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-157">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="f051e-158">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-158">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="f051e-159">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-159">Cancelable</span></span>     | <span data-ttu-id="f051e-160">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-160">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="f051e-161">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-161">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="f051e-162">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-162">Non-cancelable</span></span> | <span data-ttu-id="f051e-163">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-163">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="f051e-164">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-164">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="f051e-165">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-165">Cancelable</span></span>     | <span data-ttu-id="f051e-166">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-166">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="f051e-167">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-167">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="f051e-168">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-168">Non-cancelable</span></span> | <span data-ttu-id="f051e-169">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-169">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="f051e-170">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-170">Customer triggers</span></span>

| <span data-ttu-id="f051e-171">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-171">Trigger</span></span>                   | <span data-ttu-id="f051e-172">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-172">Type</span></span>                    | <span data-ttu-id="f051e-173">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-173">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="f051e-174">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-174">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="f051e-175">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-175">Cancelable</span></span>              | <span data-ttu-id="f051e-176">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-176">Executed before adding a customer to the transaction.</span></span>             |
| <span data-ttu-id="f051e-177">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-177">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="f051e-178">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-178">Non-cancelable</span></span>          | <span data-ttu-id="f051e-179">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-179">Executed after adding a customer to the transaction.</span></span>              |
| <span data-ttu-id="f051e-180">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-180">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="f051e-181">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-181">Cancelable</span></span>              | <span data-ttu-id="f051e-182">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-182">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="f051e-183">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-183">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="f051e-184">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-184">Non-cancelable</span></span>          | <span data-ttu-id="f051e-185">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-185">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="f051e-186">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-186">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="f051e-187">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-187">Cancelable</span></span>              | <span data-ttu-id="f051e-188">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-188">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="f051e-189">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-189">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="f051e-190">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-190">Cancelable</span></span>              | <span data-ttu-id="f051e-191">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-191">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="f051e-192">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-192">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="f051e-193">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-193">Non-cancelable</span></span>          | <span data-ttu-id="f051e-194">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-194">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="f051e-195">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-195">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="f051e-196">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-196">Non-cancelable</span></span>          | <span data-ttu-id="f051e-197">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-197">Executed after the loyalty card is issued.</span></span>       |
| <span data-ttu-id="f051e-198">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-198">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="f051e-199">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-199">Cancelable</span></span>          | <span data-ttu-id="f051e-200">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-200">Executed before the customer is created.</span></span>       |
| <span data-ttu-id="f051e-201">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-201">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="f051e-202">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-202">Non-cancelable</span></span>          | <span data-ttu-id="f051e-203">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-203">Executed after the customer is created.</span></span>       |
| <span data-ttu-id="f051e-204">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-204">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="f051e-205">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-205">Cancelable</span></span>          | <span data-ttu-id="f051e-206">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-206">Executed before getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="f051e-207">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-207">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="f051e-208">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-208">Non-cancelable</span></span>          | <span data-ttu-id="f051e-209">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-209">Executed after getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="f051e-210">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-210">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="f051e-211">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-211">Cancelable</span></span>          | <span data-ttu-id="f051e-212">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-212">Executed before displaying the loyalty card balance.</span></span>       |



## <a name="discount-triggers"></a><span data-ttu-id="f051e-213">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-213">Discount triggers</span></span>

| <span data-ttu-id="f051e-214">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-214">Trigger</span></span>                         | <span data-ttu-id="f051e-215">型</span><span class="sxs-lookup"><span data-stu-id="f051e-215">Type</span></span>           | <span data-ttu-id="f051e-216">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-216">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f051e-217">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-217">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="f051e-218">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-218">Cancelable</span></span>     | <span data-ttu-id="f051e-219">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-219">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="f051e-220">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-220">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="f051e-221">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-221">Non-cancelable</span></span> | <span data-ttu-id="f051e-222">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-222">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="f051e-223">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-223">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="f051e-224">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-224">Cancelable</span></span>     | <span data-ttu-id="f051e-225">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-225">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="f051e-226">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-226">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="f051e-227">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-227">Non-cancelable</span></span> | <span data-ttu-id="f051e-228">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-228">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="f051e-229">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-229">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="f051e-230">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-230">Cancelable</span></span>     | <span data-ttu-id="f051e-231">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-231">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="f051e-232">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-232">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="f051e-233">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-233">Non-cancelable</span></span> | <span data-ttu-id="f051e-234">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-234">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="f051e-235">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-235">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="f051e-236">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-236">Cancelable</span></span>     | <span data-ttu-id="f051e-237">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-237">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="f051e-238">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-238">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="f051e-239">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-239">Non-cancelable</span></span> | <span data-ttu-id="f051e-240">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-240">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="f051e-241">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-241">PreAddCouponTrigger</span></span>             | <span data-ttu-id="f051e-242">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-242">Cancelable</span></span>     | <span data-ttu-id="f051e-243">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-243">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="f051e-244">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-244">PostAddCouponTrigger</span></span>            | <span data-ttu-id="f051e-245">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-245">Non-cancelable</span></span> | <span data-ttu-id="f051e-246">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-246">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="f051e-247">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-247">Operation triggers</span></span>

| <span data-ttu-id="f051e-248">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-248">Trigger</span></span>              | <span data-ttu-id="f051e-249">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-249">Type</span></span>           | <span data-ttu-id="f051e-250">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-250">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="f051e-251">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-251">PreOperationTrigger</span></span>  | <span data-ttu-id="f051e-252">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-252">Cancelable</span></span>     | <span data-ttu-id="f051e-253">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="f051e-253">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="f051e-254">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f051e-254">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="f051e-255">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-255">PreOperationValidationTrigger</span></span> | <span data-ttu-id="f051e-256">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-256">Cancelable</span></span> | <span data-ttu-id="f051e-257">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="f051e-257">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="f051e-258">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-258">OperationFailureTrigger</span></span> | <span data-ttu-id="f051e-259">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-259">Non-cancelable</span></span> | <span data-ttu-id="f051e-260">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="f051e-260">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="f051e-261">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-261">PostOperationTrigger</span></span> | <span data-ttu-id="f051e-262">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-262">Non-cancelable</span></span> | <span data-ttu-id="f051e-263">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="f051e-263">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="f051e-264">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f051e-264">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="f051e-265">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-265">Payment triggers</span></span>

| <span data-ttu-id="f051e-266">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-266">Trigger</span></span>                 | <span data-ttu-id="f051e-267">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-267">Type</span></span>           | <span data-ttu-id="f051e-268">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-268">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="f051e-269">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-269">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="f051e-270">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-270">Cancelable</span></span>     | <span data-ttu-id="f051e-271">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-271">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="f051e-272">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-272">PrePaymentTrigger</span></span>       | <span data-ttu-id="f051e-273">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-273">Cancelable</span></span>     | <span data-ttu-id="f051e-274">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-274">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="f051e-275">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-275">PostPaymentTrigger</span></span>      | <span data-ttu-id="f051e-276">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-276">Non-cancelable</span></span> | <span data-ttu-id="f051e-277">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-277">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="f051e-278">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-278">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="f051e-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-279">Cancelable</span></span>     | <span data-ttu-id="f051e-280">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-280">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="f051e-281">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-281">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="f051e-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-282">Non-cancelable</span></span> | <span data-ttu-id="f051e-283">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-283">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="f051e-284">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-284">Printing Triggers</span></span>

| <span data-ttu-id="f051e-285">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-285">Trigger</span></span>                    | <span data-ttu-id="f051e-286">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-286">Type</span></span>       | <span data-ttu-id="f051e-287">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-287">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="f051e-288">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-288">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="f051e-289">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-289">Cancelable</span></span> | <span data-ttu-id="f051e-290">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-290">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="f051e-291">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-291">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="f051e-292">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-292">Non-cancelable</span></span> | <span data-ttu-id="f051e-293">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-293">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="f051e-294">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-294">Product triggers</span></span>

| <span data-ttu-id="f051e-295">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-295">Trigger</span></span>                    | <span data-ttu-id="f051e-296">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-296">Type</span></span>           | <span data-ttu-id="f051e-297">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-297">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f051e-298">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-298">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="f051e-299">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-299">Non-cancelable</span></span> | <span data-ttu-id="f051e-300">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-300">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="f051e-301">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-301">PreProductSaleTrigger</span></span>      | <span data-ttu-id="f051e-302">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-302">Cancelable</span></span>     | <span data-ttu-id="f051e-303">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-303">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="f051e-304">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-304">PostProductSaleTrigger</span></span>     | <span data-ttu-id="f051e-305">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-305">Non-cancelable</span></span> | <span data-ttu-id="f051e-306">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-306">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="f051e-307">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-307">PreReturnProductTrigger</span></span>    | <span data-ttu-id="f051e-308">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-308">Cancelable</span></span>     | <span data-ttu-id="f051e-309">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-309">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="f051e-310">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-310">PostReturnProductTrigger</span></span>   | <span data-ttu-id="f051e-311">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-311">Non-cancelable</span></span> | <span data-ttu-id="f051e-312">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-312">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="f051e-313">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-313">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="f051e-314">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-314">Cancelable</span></span>     | <span data-ttu-id="f051e-315">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-315">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="f051e-316">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-316">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="f051e-317">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-317">Non-cancelable</span></span> | <span data-ttu-id="f051e-318">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-318">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="f051e-319">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-319">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="f051e-320">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-320">Cancelable</span></span>     | <span data-ttu-id="f051e-321">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-321">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="f051e-322">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-322">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="f051e-323">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-323">Non-cancelable</span></span> | <span data-ttu-id="f051e-324">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-324">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="f051e-325">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-325">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="f051e-326">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-326">Cancelable</span></span>     | <span data-ttu-id="f051e-327">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-327">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="f051e-328">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-328">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="f051e-329">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-329">Non-cancelable</span></span> | <span data-ttu-id="f051e-330">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-330">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="f051e-331">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-331">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="f051e-332">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-332">Cancelable</span></span>     | <span data-ttu-id="f051e-333">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-333">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="f051e-334">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-334">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="f051e-335">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-335">Non-cancelable</span></span> | <span data-ttu-id="f051e-336">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-336">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="f051e-337">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-337">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="f051e-338">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-338">Non-cancelable</span></span> | <span data-ttu-id="f051e-339">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-339">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="f051e-340">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-340">Sales order triggers</span></span>

| <span data-ttu-id="f051e-341">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-341">Trigger</span></span>                 | <span data-ttu-id="f051e-342">型</span><span class="sxs-lookup"><span data-stu-id="f051e-342">Type</span></span>           | <span data-ttu-id="f051e-343">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-343">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="f051e-344">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-344">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="f051e-345">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-345">Cancelable</span></span>     | <span data-ttu-id="f051e-346">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-346">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="f051e-347">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-347">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="f051e-348">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-348">Non-cancelable</span></span> | <span data-ttu-id="f051e-349">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-349">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="f051e-350">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-350">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="f051e-351">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-351">Cancelable</span></span>     | <span data-ttu-id="f051e-352">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-352">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="f051e-353">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-353">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="f051e-354">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-354">Cancelable</span></span>     | <span data-ttu-id="f051e-355">顧客先発注時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-355">Executed before the shipping origin is changed during customer order.</span></span>|
| <span data-ttu-id="f051e-356">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-356">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="f051e-357">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-357">Cancelable</span></span>     | <span data-ttu-id="f051e-358">出荷ボタンをクリックすることで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-358">Executed before the shipping is done from the Order fulfillment view by clicking the ship button.</span></span>|
| <span data-ttu-id="f051e-359">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-359">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="f051e-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-360">Cancelable</span></span>     | <span data-ttu-id="f051e-361">梱包ボタンをクリックすることで、注文フルフィルメント ビューから梱包としてマーク オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-361">Executed before the mark as packed option is triggered from the order fulfillment view by clicking the Pack button.</span></span>|
| <span data-ttu-id="f051e-362">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-362">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="f051e-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-363">Cancelable</span></span>     | <span data-ttu-id="f051e-364">梱包明細の作成オプションがトリガーされる前に、注文フルフィルメント ビューから梱包ボタンをクリックして実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-364">Executed before the create packing slip option triggered is from the order fulfillment view by clicking the Pack button.</span></span>|


## <a name="shift-triggers"></a><span data-ttu-id="f051e-365">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-365">Shift triggers</span></span>
| <span data-ttu-id="f051e-366">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-366">Trigger</span></span>              | <span data-ttu-id="f051e-367">型</span><span class="sxs-lookup"><span data-stu-id="f051e-367">Type</span></span>           | <span data-ttu-id="f051e-368">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-368">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="f051e-369">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-369">PostOpenShiftTrigger</span></span> | <span data-ttu-id="f051e-370">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-370">Non-cancelable</span></span> | <span data-ttu-id="f051e-371">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-371">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="f051e-372">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-372">Tax override triggers</span></span>

| <span data-ttu-id="f051e-373">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-373">Trigger</span></span>                           | <span data-ttu-id="f051e-374">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-374">Type</span></span>           | <span data-ttu-id="f051e-375">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-375">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="f051e-376">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-376">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="f051e-377">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-377">Cancelable</span></span>     | <span data-ttu-id="f051e-378">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-378">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="f051e-379">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-379">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="f051e-380">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-380">Non-cancelable</span></span> | <span data-ttu-id="f051e-381">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-381">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="f051e-382">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-382">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="f051e-383">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-383">Cancelable</span></span>     | <span data-ttu-id="f051e-384">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-384">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="f051e-385">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-385">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="f051e-386">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-386">Non-cancelable</span></span> | <span data-ttu-id="f051e-387">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-387">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="f051e-388">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-388">Transaction triggers</span></span>

| <span data-ttu-id="f051e-389">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-389">Trigger</span></span>                            | <span data-ttu-id="f051e-390">種類</span><span class="sxs-lookup"><span data-stu-id="f051e-390">Type</span></span>           | <span data-ttu-id="f051e-391">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-391">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="f051e-392">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-392">BeginTransactionTrigger</span></span>            | <span data-ttu-id="f051e-393">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-393">Non-cancelable</span></span> | <span data-ttu-id="f051e-394">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-394">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="f051e-395">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-395">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="f051e-396">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-396">Cancelable</span></span>     | <span data-ttu-id="f051e-397">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-397">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="f051e-398">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-398">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="f051e-399">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-399">Cancelable</span></span>     | <span data-ttu-id="f051e-400">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-400">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="f051e-401">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-401">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="f051e-402">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-402">Non-cancelable</span></span> | <span data-ttu-id="f051e-403">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-403">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="f051e-404">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-404">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="f051e-405">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-405">Cancelable</span></span>     | <span data-ttu-id="f051e-406">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f051e-406">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="f051e-407">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-407">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="f051e-408">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-408">Non-cancelable</span></span> | <span data-ttu-id="f051e-409">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f051e-409">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="f051e-410">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-410">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="f051e-411">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-411">Cancelable</span></span>     | <span data-ttu-id="f051e-412">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-412">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="f051e-413">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-413">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="f051e-414">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-414">Non-cancelable</span></span> | <span data-ttu-id="f051e-415">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-415">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="f051e-416">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-416">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="f051e-417">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-417">Cancelable</span></span>     | <span data-ttu-id="f051e-418">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-418">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="f051e-419">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-419">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="f051e-420">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-420">Non-cancelable</span></span> | <span data-ttu-id="f051e-421">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-421">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="f051e-422">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-422">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="f051e-423">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-423">Cancelable</span></span>     | <span data-ttu-id="f051e-424">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-424">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="f051e-425">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-425">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="f051e-426">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-426">Non-cancelable</span></span> | <span data-ttu-id="f051e-427">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-427">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="f051e-428">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-428">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="f051e-429">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-429">Non-cancelable</span></span> | <span data-ttu-id="f051e-430">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-430">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="f051e-431">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-431">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="f051e-432">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-432">Cancelable</span></span>     | <span data-ttu-id="f051e-433">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-433">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="f051e-434">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="f051e-434">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="f051e-435">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="f051e-435">Non-Cancelable</span></span> | <span data-ttu-id="f051e-436">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-436">Executed after the customer order is recalled.</span></span>        |

## <a name="reason-code-triggers"></a><span data-ttu-id="f051e-437">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-437">Reason code triggers</span></span>
| <span data-ttu-id="f051e-438">トリガー</span><span class="sxs-lookup"><span data-stu-id="f051e-438">Trigger</span></span>              | <span data-ttu-id="f051e-439">型</span><span class="sxs-lookup"><span data-stu-id="f051e-439">Type</span></span>           | <span data-ttu-id="f051e-440">説明</span><span class="sxs-lookup"><span data-stu-id="f051e-440">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="f051e-441">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="f051e-441">PostGetReasonCodeLine</span></span> | <span data-ttu-id="f051e-442">解約可能</span><span class="sxs-lookup"><span data-stu-id="f051e-442">Cancelable</span></span> | <span data-ttu-id="f051e-443">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-443">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |


## <a name="business-scenario"></a><span data-ttu-id="f051e-444">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="f051e-444">Business scenario</span></span>
<span data-ttu-id="f051e-445">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-445">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="f051e-446">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f051e-446">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="f051e-447">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f051e-447">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="f051e-448">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="f051e-448">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="f051e-449">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="f051e-449">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="f051e-450">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="f051e-450">Implement a trigger</span></span>

1. <span data-ttu-id="f051e-451">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="f051e-451">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="f051e-452">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="f051e-452">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="f051e-453">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f051e-453">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="f051e-454">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f051e-454">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="f051e-455">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="f051e-455">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="f051e-456">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="f051e-456">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="f051e-457">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="f051e-457">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="f051e-458">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f051e-458">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="f051e-459">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f051e-459">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="f051e-460">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f051e-460">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="f051e-461">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f051e-461">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="f051e-462">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="f051e-462">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="f051e-463">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="f051e-463">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="f051e-464">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="f051e-464">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="f051e-465">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f051e-465">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="f051e-466">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f051e-466">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="f051e-467">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="f051e-467">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="f051e-468">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="f051e-468">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="f051e-469">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f051e-469">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="f051e-470">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-470">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="f051e-471">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f051e-471">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="f051e-472">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="f051e-472">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="f051e-473">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="f051e-473">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="f051e-474">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="f051e-474">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="f051e-475">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="f051e-475">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="f051e-476">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="f051e-476">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="f051e-477">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f051e-477">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="f051e-478">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="f051e-478">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="f051e-479">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="f051e-479">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="f051e-480">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f051e-480">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="f051e-481">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="f051e-481">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f051e-482">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f051e-482">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="f051e-483">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="f051e-483">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="f051e-484">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f051e-484">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="f051e-485">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f051e-485">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="f051e-486">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="f051e-486">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="f051e-487">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f051e-487">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="f051e-488">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="f051e-488">Compile and build the project.</span></span>
12. <span data-ttu-id="f051e-489">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f051e-489">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="f051e-490">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f051e-490">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="f051e-491">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f051e-491">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="f051e-492">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="f051e-492">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="f051e-493">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="f051e-493">Save and close the file.</span></span>
17. <span data-ttu-id="f051e-494">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="f051e-494">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="f051e-495">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="f051e-495">Add the custom receipt layout</span></span>

1. <span data-ttu-id="f051e-496">Dynamics 365 Retail を開きます。</span><span class="sxs-lookup"><span data-stu-id="f051e-496">Open Dynamics 365 Retail.</span></span>
2. <span data-ttu-id="f051e-497">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-497">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="f051e-498">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-498">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="f051e-499">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f051e-499">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="f051e-500">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f051e-500">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="f051e-501">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="f051e-501">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="f051e-502">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="f051e-502">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="f051e-503">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-503">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="f051e-504">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="f051e-504">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="f051e-505">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="f051e-505">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="f051e-506">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-506">Click **Save**.</span></span>
9. <span data-ttu-id="f051e-507">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-507">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="f051e-508">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f051e-508">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="f051e-509">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-509">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="f051e-510">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f051e-510">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="f051e-511">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-511">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="f051e-512">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-512">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="f051e-513">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="f051e-513">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="f051e-514">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f051e-514">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="f051e-515">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-515">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="f051e-516">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f051e-516">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="f051e-517">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="f051e-517">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="f051e-518">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-518">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="f051e-519">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="f051e-519">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="f051e-520">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="f051e-520">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="f051e-521">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-521">Click **Save**.</span></span>
6. <span data-ttu-id="f051e-522">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f051e-522">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="f051e-523">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f051e-523">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="f051e-524">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="f051e-524">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="f051e-525">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="f051e-525">Validate the extension</span></span>

1. <span data-ttu-id="f051e-526">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="f051e-526">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="f051e-527">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f051e-527">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="f051e-528">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="f051e-528">Suspend the transaction.</span></span>
4. <span data-ttu-id="f051e-529">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f051e-529">The custom receipt should print.</span></span>
