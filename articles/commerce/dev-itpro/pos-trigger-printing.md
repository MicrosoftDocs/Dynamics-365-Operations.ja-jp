---
title: Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、任意の Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 07/13/2020
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
ms.openlocfilehash: c18efb796111ab6109eba3d848fae5007945e32b
ms.sourcegitcommit: d98f597feeeba6ba0fa32ce7a7d94bda328f074c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577430"
---
# <a name="pos-triggers"></a><span data-ttu-id="269de-103">POS トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-103">POS triggers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="269de-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="269de-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="269de-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="269de-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="269de-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="269de-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="269de-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="269de-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="269de-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="269de-108">Continue or cancel an operation.</span></span> <span data-ttu-id="269de-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="269de-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="269de-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="269de-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="269de-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="269de-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="269de-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="269de-112">The following table lists the available triggers and denotes whether they can be canceled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="269de-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-113">Application triggers</span></span>

| <span data-ttu-id="269de-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-114">Trigger</span></span>                   | <span data-ttu-id="269de-115">種類</span><span class="sxs-lookup"><span data-stu-id="269de-115">Type</span></span>           | <span data-ttu-id="269de-116">説明</span><span class="sxs-lookup"><span data-stu-id="269de-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="269de-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="269de-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-118">Non-cancelable</span></span> | <span data-ttu-id="269de-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-119">Executed after the POS application is started.</span></span> <span data-ttu-id="269de-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="269de-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="269de-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="269de-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-122">Non-cancelable</span></span> | <span data-ttu-id="269de-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="269de-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="269de-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-125">Cancelable</span></span>     | <span data-ttu-id="269de-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="269de-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="269de-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-128">Non-cancelable</span></span> | <span data-ttu-id="269de-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="269de-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="269de-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-131">Non-cancelable</span></span> | <span data-ttu-id="269de-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="269de-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="269de-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-134">Cancelable</span></span>     | <span data-ttu-id="269de-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="269de-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="269de-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-137">Non-Cancelable</span></span> | <span data-ttu-id="269de-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="269de-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="269de-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-140">Cancelable</span></span>     | <span data-ttu-id="269de-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="269de-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="269de-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-143">Non-Cancelable</span></span> | <span data-ttu-id="269de-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="269de-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="269de-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-146">Cancelable</span></span> | <span data-ttu-id="269de-147">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-147">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="269de-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="269de-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-149">Cancelable</span></span> | <span data-ttu-id="269de-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="269de-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="269de-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-152">Non-Cancelable</span></span> | <span data-ttu-id="269de-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-153">Executed after the audit event.</span></span>   | 
| <span data-ttu-id="269de-154">PreOpenUrlTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-154">PreOpenUrlTrigger</span></span>      | <span data-ttu-id="269de-155">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-155">Cancelable</span></span> | <span data-ttu-id="269de-156">URLを開く操作の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-156">Executed before the open URL operation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="269de-157">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-157">Cash management triggers</span></span>

| <span data-ttu-id="269de-158">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-158">Trigger</span></span>                      | <span data-ttu-id="269de-159">型</span><span class="sxs-lookup"><span data-stu-id="269de-159">Type</span></span>           | <span data-ttu-id="269de-160">説明</span><span class="sxs-lookup"><span data-stu-id="269de-160">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="269de-161">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-161">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="269de-162">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-162">Cancelable</span></span>     | <span data-ttu-id="269de-163">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-163">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="269de-164">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-164">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="269de-165">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-165">Non-cancelable</span></span> | <span data-ttu-id="269de-166">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-166">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="269de-167">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-167">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="269de-168">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-168">Cancelable</span></span>     | <span data-ttu-id="269de-169">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-169">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="269de-170">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-170">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="269de-171">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-171">Non-cancelable</span></span> | <span data-ttu-id="269de-172">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-172">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="269de-173">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-173">Customer triggers</span></span>

| <span data-ttu-id="269de-174">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-174">Trigger</span></span>                   | <span data-ttu-id="269de-175">種類</span><span class="sxs-lookup"><span data-stu-id="269de-175">Type</span></span>                    | <span data-ttu-id="269de-176">説明</span><span class="sxs-lookup"><span data-stu-id="269de-176">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="269de-177">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-177">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="269de-178">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-178">Cancelable</span></span>              | <span data-ttu-id="269de-179">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-179">Executed before adding a customer to the transaction.</span></span>             |
| <span data-ttu-id="269de-180">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-180">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="269de-181">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-181">Non-cancelable</span></span>          | <span data-ttu-id="269de-182">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-182">Executed after adding a customer to the transaction.</span></span>              |
| <span data-ttu-id="269de-183">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-183">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="269de-184">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-184">Cancelable</span></span>              | <span data-ttu-id="269de-185">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-185">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="269de-186">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-186">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="269de-187">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-187">Non-cancelable</span></span>          | <span data-ttu-id="269de-188">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-188">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="269de-189">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-189">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="269de-190">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-190">Cancelable</span></span>              | <span data-ttu-id="269de-191">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-191">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="269de-192">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-192">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="269de-193">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-193">Cancelable</span></span>              | <span data-ttu-id="269de-194">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-194">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="269de-195">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-195">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="269de-196">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-196">Non-cancelable</span></span>          | <span data-ttu-id="269de-197">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-197">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="269de-198">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-198">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="269de-199">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-199">Non-cancelable</span></span>          | <span data-ttu-id="269de-200">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-200">Executed after the loyalty card is issued.</span></span>       |
| <span data-ttu-id="269de-201">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-201">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="269de-202">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-202">Cancelable</span></span>          | <span data-ttu-id="269de-203">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-203">Executed before the customer is created.</span></span>       |
| <span data-ttu-id="269de-204">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-204">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="269de-205">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-205">Non-cancelable</span></span>          | <span data-ttu-id="269de-206">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-206">Executed after the customer is created.</span></span>       |
| <span data-ttu-id="269de-207">PreSaveCustomerAddressTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-207">PreSaveCustomerAddressTrigger</span></span>      | <span data-ttu-id="269de-208">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-208">Cancelable</span></span>              | <span data-ttu-id="269de-209">顧客の住所が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-209">Executed before the customer address is saved.</span></span>            |
| <span data-ttu-id="269de-210">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-210">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="269de-211">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-211">Cancelable</span></span>          | <span data-ttu-id="269de-212">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-212">Executed before getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="269de-213">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-213">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="269de-214">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-214">Non-cancelable</span></span>          | <span data-ttu-id="269de-215">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-215">Executed after getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="269de-216">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-216">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="269de-217">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-217">Cancelable</span></span>          | <span data-ttu-id="269de-218">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-218">Executed before displaying the loyalty card balance.</span></span>       |



## <a name="discount-triggers"></a><span data-ttu-id="269de-219">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="269de-219">Discount triggers</span></span>

| <span data-ttu-id="269de-220">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-220">Trigger</span></span>                         | <span data-ttu-id="269de-221">型</span><span class="sxs-lookup"><span data-stu-id="269de-221">Type</span></span>           | <span data-ttu-id="269de-222">説明</span><span class="sxs-lookup"><span data-stu-id="269de-222">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="269de-223">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-223">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="269de-224">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-224">Cancelable</span></span>     | <span data-ttu-id="269de-225">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-225">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="269de-226">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-226">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="269de-227">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-227">Non-cancelable</span></span> | <span data-ttu-id="269de-228">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-228">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="269de-229">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-229">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="269de-230">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-230">Cancelable</span></span>     | <span data-ttu-id="269de-231">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-231">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="269de-232">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-232">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="269de-233">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-233">Non-cancelable</span></span> | <span data-ttu-id="269de-234">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-234">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="269de-235">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-235">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="269de-236">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-236">Cancelable</span></span>     | <span data-ttu-id="269de-237">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-237">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="269de-238">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-238">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="269de-239">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-239">Non-cancelable</span></span> | <span data-ttu-id="269de-240">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-240">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="269de-241">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-241">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="269de-242">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-242">Cancelable</span></span>     | <span data-ttu-id="269de-243">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-243">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="269de-244">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-244">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="269de-245">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-245">Non-cancelable</span></span> | <span data-ttu-id="269de-246">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-246">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="269de-247">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-247">PreAddCouponTrigger</span></span>             | <span data-ttu-id="269de-248">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-248">Cancelable</span></span>     | <span data-ttu-id="269de-249">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-249">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="269de-250">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-250">PostAddCouponTrigger</span></span>            | <span data-ttu-id="269de-251">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-251">Non-cancelable</span></span> | <span data-ttu-id="269de-252">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-252">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="269de-253">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="269de-253">Operation triggers</span></span>

| <span data-ttu-id="269de-254">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-254">Trigger</span></span>              | <span data-ttu-id="269de-255">種類</span><span class="sxs-lookup"><span data-stu-id="269de-255">Type</span></span>           | <span data-ttu-id="269de-256">説明</span><span class="sxs-lookup"><span data-stu-id="269de-256">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="269de-257">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-257">PreOperationTrigger</span></span>  | <span data-ttu-id="269de-258">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-258">Cancelable</span></span>     | <span data-ttu-id="269de-259">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="269de-259">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="269de-260">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="269de-260">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="269de-261">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-261">PreOperationValidationTrigger</span></span> | <span data-ttu-id="269de-262">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-262">Cancelable</span></span> | <span data-ttu-id="269de-263">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="269de-263">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="269de-264">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-264">OperationFailureTrigger</span></span> | <span data-ttu-id="269de-265">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-265">Non-cancelable</span></span> | <span data-ttu-id="269de-266">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="269de-266">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="269de-267">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-267">PostOperationTrigger</span></span> | <span data-ttu-id="269de-268">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-268">Non-cancelable</span></span> | <span data-ttu-id="269de-269">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="269de-269">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="269de-270">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="269de-270">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="269de-271">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-271">Payment triggers</span></span>

| <span data-ttu-id="269de-272">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-272">Trigger</span></span>                 | <span data-ttu-id="269de-273">種類</span><span class="sxs-lookup"><span data-stu-id="269de-273">Type</span></span>           | <span data-ttu-id="269de-274">説明</span><span class="sxs-lookup"><span data-stu-id="269de-274">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="269de-275">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-275">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="269de-276">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-276">Cancelable</span></span>     | <span data-ttu-id="269de-277">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-277">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="269de-278">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-278">PrePaymentTrigger</span></span>       | <span data-ttu-id="269de-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-279">Cancelable</span></span>     | <span data-ttu-id="269de-280">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-280">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="269de-281">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-281">PostPaymentTrigger</span></span>      | <span data-ttu-id="269de-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-282">Non-cancelable</span></span> | <span data-ttu-id="269de-283">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-283">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="269de-284">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-284">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="269de-285">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-285">Cancelable</span></span>     | <span data-ttu-id="269de-286">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-286">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="269de-287">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-287">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="269de-288">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-288">Non-cancelable</span></span> | <span data-ttu-id="269de-289">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-289">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="269de-290">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-290">Printing Triggers</span></span>

| <span data-ttu-id="269de-291">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-291">Trigger</span></span>                    | <span data-ttu-id="269de-292">種類</span><span class="sxs-lookup"><span data-stu-id="269de-292">Type</span></span>       | <span data-ttu-id="269de-293">説明</span><span class="sxs-lookup"><span data-stu-id="269de-293">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="269de-294">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-294">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="269de-295">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-295">Cancelable</span></span> | <span data-ttu-id="269de-296">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-296">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="269de-297">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-297">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="269de-298">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-298">Non-cancelable</span></span> | <span data-ttu-id="269de-299">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-299">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="269de-300">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-300">Product triggers</span></span>

| <span data-ttu-id="269de-301">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-301">Trigger</span></span>                    | <span data-ttu-id="269de-302">種類</span><span class="sxs-lookup"><span data-stu-id="269de-302">Type</span></span>           | <span data-ttu-id="269de-303">説明</span><span class="sxs-lookup"><span data-stu-id="269de-303">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="269de-304">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-304">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="269de-305">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-305">Non-cancelable</span></span> | <span data-ttu-id="269de-306">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-306">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="269de-307">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-307">PreProductSaleTrigger</span></span>      | <span data-ttu-id="269de-308">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-308">Cancelable</span></span>     | <span data-ttu-id="269de-309">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-309">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="269de-310">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-310">PostProductSaleTrigger</span></span>     | <span data-ttu-id="269de-311">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-311">Non-cancelable</span></span> | <span data-ttu-id="269de-312">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-312">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="269de-313">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-313">PreReturnProductTrigger</span></span>    | <span data-ttu-id="269de-314">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-314">Cancelable</span></span>     | <span data-ttu-id="269de-315">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-315">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="269de-316">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-316">PostReturnProductTrigger</span></span>   | <span data-ttu-id="269de-317">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-317">Non-cancelable</span></span> | <span data-ttu-id="269de-318">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-318">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="269de-319">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-319">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="269de-320">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-320">Cancelable</span></span>     | <span data-ttu-id="269de-321">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-321">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="269de-322">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-322">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="269de-323">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-323">Non-cancelable</span></span> | <span data-ttu-id="269de-324">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-324">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="269de-325">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-325">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="269de-326">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-326">Cancelable</span></span>     | <span data-ttu-id="269de-327">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-327">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="269de-328">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-328">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="269de-329">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-329">Non-cancelable</span></span> | <span data-ttu-id="269de-330">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-330">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="269de-331">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-331">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="269de-332">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-332">Cancelable</span></span>     | <span data-ttu-id="269de-333">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-333">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="269de-334">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-334">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="269de-335">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-335">Non-cancelable</span></span> | <span data-ttu-id="269de-336">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-336">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="269de-337">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-337">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="269de-338">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-338">Cancelable</span></span>     | <span data-ttu-id="269de-339">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-339">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="269de-340">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-340">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="269de-341">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-341">Non-cancelable</span></span> | <span data-ttu-id="269de-342">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-342">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="269de-343">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-343">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="269de-344">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-344">Non-cancelable</span></span> | <span data-ttu-id="269de-345">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-345">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="269de-346">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-346">Sales order triggers</span></span>

| <span data-ttu-id="269de-347">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-347">Trigger</span></span>                 | <span data-ttu-id="269de-348">型</span><span class="sxs-lookup"><span data-stu-id="269de-348">Type</span></span>           | <span data-ttu-id="269de-349">説明</span><span class="sxs-lookup"><span data-stu-id="269de-349">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="269de-350">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-350">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="269de-351">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-351">Cancelable</span></span>     | <span data-ttu-id="269de-352">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-352">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="269de-353">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-353">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="269de-354">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-354">Non-cancelable</span></span> | <span data-ttu-id="269de-355">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-355">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="269de-356">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-356">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="269de-357">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-357">Cancelable</span></span>     | <span data-ttu-id="269de-358">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-358">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="269de-359">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-359">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="269de-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-360">Cancelable</span></span>     | <span data-ttu-id="269de-361">顧客注文時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-361">Executed before the shipping origin is changed during a customer order.</span></span>|
| <span data-ttu-id="269de-362">PreGetFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-362">PreGetFulfillmentLinesTrigger</span></span>     | <span data-ttu-id="269de-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-363">Cancelable</span></span>     | <span data-ttu-id="269de-364">注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-364">Executed before the Order fulfillment lines are loaded in the Order fulfillment view.</span></span>|
| <span data-ttu-id="269de-365">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-365">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="269de-366">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-366">Cancelable</span></span>     | <span data-ttu-id="269de-367">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-367">Executed before the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="269de-368">PostShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-368">PostShipFulfillmentLinesTrigger</span></span>   | <span data-ttu-id="269de-369">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-369">Non-Cancelable</span></span>     | <span data-ttu-id="269de-370">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-370">Executed after the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="269de-371">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-371">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="269de-372">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-372">Cancelable</span></span>     | <span data-ttu-id="269de-373">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-373">Executed before the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="269de-374">PostMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-374">PostMarkFulfillmentLinesAsPackedTrigger</span></span>   | <span data-ttu-id="269de-375">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-375">Non-Cancelable</span></span>     | <span data-ttu-id="269de-376">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-376">Executed after the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="269de-377">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-377">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="269de-378">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-378">Cancelable</span></span>     | <span data-ttu-id="269de-379">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-379">Executed before the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="269de-380">PostCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-380">PostCreatePackingSlipTrigger</span></span>  | <span data-ttu-id="269de-381">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-381">Non-Cancelable</span></span>     | <span data-ttu-id="269de-382">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-382">Executed after the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="269de-383">PostReturnInvoicedSalesLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-383">PostReturnInvoicedSalesLinesTrigger</span></span>   | <span data-ttu-id="269de-384">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-384">Non-Cancelable</span></span>     | <span data-ttu-id="269de-385">返品対象として 1 つ以上の請求書が選択された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-385">Executed after one or more invoices selected for return.</span></span>|
| <span data-ttu-id="269de-386">PreResendEmailReceiptTrigger (10.0.13)</span><span class="sxs-lookup"><span data-stu-id="269de-386">PreResendEmailReceiptTrigger (10.0.13)</span></span>    | <span data-ttu-id="269de-387">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-387">Cancelable</span></span>     | <span data-ttu-id="269de-388">仕訳帳ビューを表示から電子メールを送信する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-388">Executed before sending the email from the Show journal view.</span></span>|



## <a name="shift-triggers"></a><span data-ttu-id="269de-389">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-389">Shift triggers</span></span>
| <span data-ttu-id="269de-390">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-390">Trigger</span></span>              | <span data-ttu-id="269de-391">種類</span><span class="sxs-lookup"><span data-stu-id="269de-391">Type</span></span>           | <span data-ttu-id="269de-392">説明</span><span class="sxs-lookup"><span data-stu-id="269de-392">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="269de-393">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-393">PostOpenShiftTrigger</span></span> | <span data-ttu-id="269de-394">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-394">Non-cancelable</span></span> | <span data-ttu-id="269de-395">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-395">This trigger is executed after the new shift is opened.</span></span> |
| <span data-ttu-id="269de-396">PreCloseShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-396">PreCloseShiftTrigger</span></span> | <span data-ttu-id="269de-397">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-397">Cancelable</span></span> | <span data-ttu-id="269de-398">このトリガーは、シフトが開かれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-398">This trigger is executed before the shift is closed.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="269de-399">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="269de-399">Tax override triggers</span></span>

| <span data-ttu-id="269de-400">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-400">Trigger</span></span>                           | <span data-ttu-id="269de-401">型</span><span class="sxs-lookup"><span data-stu-id="269de-401">Type</span></span>           | <span data-ttu-id="269de-402">説明</span><span class="sxs-lookup"><span data-stu-id="269de-402">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="269de-403">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-403">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="269de-404">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-404">Cancelable</span></span>     | <span data-ttu-id="269de-405">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-405">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="269de-406">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-406">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="269de-407">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-407">Non-cancelable</span></span> | <span data-ttu-id="269de-408">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-408">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="269de-409">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-409">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="269de-410">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-410">Cancelable</span></span>     | <span data-ttu-id="269de-411">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-411">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="269de-412">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-412">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="269de-413">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-413">Non-cancelable</span></span> | <span data-ttu-id="269de-414">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-414">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="269de-415">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="269de-415">Transaction triggers</span></span>

| <span data-ttu-id="269de-416">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-416">Trigger</span></span>                            | <span data-ttu-id="269de-417">種類</span><span class="sxs-lookup"><span data-stu-id="269de-417">Type</span></span>           | <span data-ttu-id="269de-418">説明</span><span class="sxs-lookup"><span data-stu-id="269de-418">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="269de-419">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-419">BeginTransactionTrigger</span></span>            | <span data-ttu-id="269de-420">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-420">Non-cancelable</span></span> | <span data-ttu-id="269de-421">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-421">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="269de-422">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-422">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="269de-423">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-423">Cancelable</span></span>     | <span data-ttu-id="269de-424">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-424">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="269de-425">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-425">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="269de-426">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-426">Cancelable</span></span>     | <span data-ttu-id="269de-427">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-427">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="269de-428">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-428">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="269de-429">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-429">Non-cancelable</span></span> | <span data-ttu-id="269de-430">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-430">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="269de-431">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-431">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="269de-432">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-432">Cancelable</span></span>     | <span data-ttu-id="269de-433">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="269de-433">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="269de-434">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-434">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="269de-435">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-435">Non-cancelable</span></span> | <span data-ttu-id="269de-436">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="269de-436">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="269de-437">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-437">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="269de-438">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-438">Cancelable</span></span>     | <span data-ttu-id="269de-439">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-439">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="269de-440">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-440">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="269de-441">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-441">Non-cancelable</span></span> | <span data-ttu-id="269de-442">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-442">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="269de-443">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-443">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="269de-444">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-444">Cancelable</span></span>     | <span data-ttu-id="269de-445">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-445">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="269de-446">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-446">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="269de-447">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-447">Non-cancelable</span></span> | <span data-ttu-id="269de-448">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-448">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="269de-449">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-449">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="269de-450">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-450">Cancelable</span></span>     | <span data-ttu-id="269de-451">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-451">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="269de-452">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-452">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="269de-453">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-453">Non-cancelable</span></span> | <span data-ttu-id="269de-454">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-454">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="269de-455">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-455">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="269de-456">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-456">Non-cancelable</span></span> | <span data-ttu-id="269de-457">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-457">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="269de-458">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-458">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="269de-459">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-459">Cancelable</span></span>     | <span data-ttu-id="269de-460">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-460">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="269de-461">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-461">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="269de-462">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="269de-462">Non-Cancelable</span></span> | <span data-ttu-id="269de-463">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-463">Executed after the customer order is recalled.</span></span>        |
| <span data-ttu-id="269de-464">PreSelectTransactionPaymentMethodTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-464">PreSelectTransactionPaymentMethodTrigger</span></span>       | <span data-ttu-id="269de-465">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-465">Cancelable</span></span> |  <span data-ttu-id="269de-466">ユーザーが**カート ビュー - 合計**パネルで**合計**を選択すると、使用可能な支払方法が表示され、このトリガーはこのダイアログが表示される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-466">When the user selects the **Totals** button in the **Cart view - totals** panel, the available payment methods are shown and this trigger will get executed before this dialog is shown.</span></span> <span data-ttu-id="269de-467">このトリガーから利用可能な支払方法を変更するための拡張コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="269de-467">You can us extension code to modify the available payment methods from this trigger.</span></span>      |
| <span data-ttu-id="269de-468">PreShipSelectedCartLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-468">PreShipSelectedCartLinesTrigger</span></span>       | <span data-ttu-id="269de-469">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-469">Cancelable</span></span> |  <span data-ttu-id="269de-470">製品が出荷対象として選択されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-470">Executed when the product is selected for shipping.</span></span>      |

## <a name="reason-code-triggers"></a><span data-ttu-id="269de-471">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-471">Reason code triggers</span></span>
| <span data-ttu-id="269de-472">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-472">Trigger</span></span>              | <span data-ttu-id="269de-473">種類</span><span class="sxs-lookup"><span data-stu-id="269de-473">Type</span></span>           | <span data-ttu-id="269de-474">説明</span><span class="sxs-lookup"><span data-stu-id="269de-474">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="269de-475">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="269de-475">PostGetReasonCodeLine</span></span> | <span data-ttu-id="269de-476">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-476">Cancelable</span></span> | <span data-ttu-id="269de-477">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-477">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |

## <a name="transfer-order-triggers"></a><span data-ttu-id="269de-478">移動オーダー トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-478">Transfer Order triggers</span></span>
| <span data-ttu-id="269de-479">トリガー</span><span class="sxs-lookup"><span data-stu-id="269de-479">Trigger</span></span>              | <span data-ttu-id="269de-480">型</span><span class="sxs-lookup"><span data-stu-id="269de-480">Type</span></span>           | <span data-ttu-id="269de-481">説明</span><span class="sxs-lookup"><span data-stu-id="269de-481">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="269de-482">PreCreateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-482">PreCreateTransferOrderTrigger</span></span> | <span data-ttu-id="269de-483">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-483">Cancelable</span></span> | <span data-ttu-id="269de-484">このトリガーは、移動オーダーが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="269de-484">This trigger is executed before the transfer order is created (executed after the order input).</span></span> |
| <span data-ttu-id="269de-485">PreUpdateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="269de-485">PreUpdateTransferOrderTrigger</span></span> | <span data-ttu-id="269de-486">解約可能</span><span class="sxs-lookup"><span data-stu-id="269de-486">Cancelable</span></span> | <span data-ttu-id="269de-487">このトリガーは、移動オーダーが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="269de-487">This trigger is executed before the transfer order is updated.</span></span> |


## <a name="business-scenario"></a><span data-ttu-id="269de-488">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="269de-488">Business scenario</span></span>
<span data-ttu-id="269de-489">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="269de-489">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="269de-490">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="269de-490">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="269de-491">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="269de-491">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="269de-492">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="269de-492">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="269de-493">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="269de-493">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="269de-494">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="269de-494">Implement a trigger</span></span>

1. <span data-ttu-id="269de-495">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="269de-495">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="269de-496">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="269de-496">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="269de-497">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="269de-497">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="269de-498">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="269de-498">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="269de-499">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="269de-499">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="269de-500">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="269de-500">Add the following **import** statements to import the relevant entities and context.</span></span>

   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
   
7. <span data-ttu-id="269de-501">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="269de-501">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
    ```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
    ```
8. <span data-ttu-id="269de-502">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="269de-502">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
   
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
   
   <span data-ttu-id="269de-503">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="269de-503">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="269de-504">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="269de-504">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="269de-505">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="269de-505">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="269de-506">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="269de-506">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="269de-507">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="269de-507">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="269de-508">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="269de-508">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="269de-509">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="269de-509">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="269de-510">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="269de-510">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="269de-511">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="269de-511">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="269de-512">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="269de-512">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="269de-513">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="269de-513">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="269de-514">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="269de-514">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="269de-515">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="269de-515">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="269de-516">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="269de-516">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="269de-517">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="269de-517">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="269de-518">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="269de-518">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="269de-519">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="269de-519">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="269de-520">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="269de-520">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="269de-521">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="269de-521">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="269de-522">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="269de-522">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="269de-523">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点ではコマース トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="269de-523">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the commerce transaction table.</span></span> <span data-ttu-id="269de-524">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="269de-524">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="269de-525">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="269de-525">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="269de-526">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="269de-526">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="269de-527">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="269de-527">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="269de-528">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="269de-528">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="269de-529">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="269de-529">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="269de-530">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="269de-530">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="269de-531">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="269de-531">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="269de-532">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="269de-532">Compile and build the project.</span></span>
12. <span data-ttu-id="269de-533">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="269de-533">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="269de-534">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="269de-534">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="269de-535">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="269de-535">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="269de-536">**commerceruntime.ext.config** ファイルを開き、\<composition\> セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="269de-536">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="269de-537">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="269de-537">Save and close the file.</span></span>
17. <span data-ttu-id="269de-538">Commerce Scale Unit を再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="269de-538">Restart the Commerce Scale Unit to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="269de-539">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="269de-539">Add the custom receipt layout</span></span>

1. <span data-ttu-id="269de-540">Dynamics 365 Commerce を開きます。</span><span class="sxs-lookup"><span data-stu-id="269de-540">Open Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="269de-541">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="269de-541">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="269de-542">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-542">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="269de-543">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="269de-543">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="269de-544">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="269de-544">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="269de-545">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="269de-545">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="269de-546">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="269de-546">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="269de-547">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="269de-547">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="269de-548">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="269de-548">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="269de-549">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="269de-549">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="269de-550">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-550">Click **Save**.</span></span>
9. <span data-ttu-id="269de-551">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **視覚プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="269de-551">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="269de-552">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="269de-552">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="269de-553">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-553">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="269de-554">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="269de-554">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="269de-555">**Retail とコマース > Retail とコマース IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="269de-555">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="269de-556">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-556">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="269de-557">要求するメッセージが表示されたら、**はい**をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="269de-557">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="269de-558">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="269de-558">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="269de-559">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="269de-559">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="269de-560">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="269de-560">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="269de-561">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="269de-561">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="269de-562">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-562">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="269de-563">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="269de-563">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="269de-564">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="269de-564">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="269de-565">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-565">Click **Save**.</span></span>
6. <span data-ttu-id="269de-566">**Retail とコマース** > **Retail とコマース IT** > **配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="269de-566">Go to **Retail and Commerce** > **Retail and Commerce IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="269de-567">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="269de-567">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="269de-568">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="269de-568">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="269de-569">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="269de-569">Validate the extension</span></span>

1. <span data-ttu-id="269de-570">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="269de-570">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="269de-571">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="269de-571">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="269de-572">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="269de-572">Suspend the transaction.</span></span>
4. <span data-ttu-id="269de-573">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="269de-573">The custom receipt should print.</span></span>
