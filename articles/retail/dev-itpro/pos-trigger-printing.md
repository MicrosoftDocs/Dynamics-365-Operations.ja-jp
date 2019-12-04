---
title: Retail Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 11/21/2019
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
ms.openlocfilehash: 0d9ed7f6816d307b337789d72cf72767dcd73620
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824533"
---
# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="c6435-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="c6435-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6435-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c6435-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="c6435-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c6435-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="c6435-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="c6435-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="c6435-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6435-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="c6435-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c6435-108">Continue or cancel an operation.</span></span> <span data-ttu-id="c6435-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c6435-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="c6435-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="c6435-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="c6435-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="c6435-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="c6435-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="c6435-112">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="c6435-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-113">Application triggers</span></span>

| <span data-ttu-id="c6435-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-114">Trigger</span></span>                   | <span data-ttu-id="c6435-115">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-115">Type</span></span>           | <span data-ttu-id="c6435-116">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="c6435-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="c6435-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-118">Non-cancelable</span></span> | <span data-ttu-id="c6435-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-119">Executed after the POS application is started.</span></span> <span data-ttu-id="c6435-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="c6435-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="c6435-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="c6435-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-122">Non-cancelable</span></span> | <span data-ttu-id="c6435-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="c6435-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="c6435-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-125">Cancelable</span></span>     | <span data-ttu-id="c6435-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="c6435-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="c6435-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-128">Non-cancelable</span></span> | <span data-ttu-id="c6435-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="c6435-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="c6435-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-131">Non-cancelable</span></span> | <span data-ttu-id="c6435-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="c6435-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="c6435-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-134">Cancelable</span></span>     | <span data-ttu-id="c6435-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="c6435-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="c6435-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-137">Non-Cancelable</span></span> | <span data-ttu-id="c6435-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="c6435-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="c6435-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-140">Cancelable</span></span>     | <span data-ttu-id="c6435-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="c6435-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="c6435-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-143">Non-Cancelable</span></span> | <span data-ttu-id="c6435-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="c6435-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="c6435-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-146">Cancelable</span></span> | <span data-ttu-id="c6435-147">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-147">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="c6435-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="c6435-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-149">Cancelable</span></span> | <span data-ttu-id="c6435-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="c6435-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="c6435-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-152">Non-Cancelable</span></span> | <span data-ttu-id="c6435-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-153">Executed after the audit event.</span></span>   | 
| <span data-ttu-id="c6435-154">PreOpenUrlTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-154">PreOpenUrlTrigger</span></span>      | <span data-ttu-id="c6435-155">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-155">Cancelable</span></span> | <span data-ttu-id="c6435-156">URLを開く操作の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-156">Executed before the open URL operation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="c6435-157">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-157">Cash management triggers</span></span>

| <span data-ttu-id="c6435-158">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-158">Trigger</span></span>                      | <span data-ttu-id="c6435-159">型</span><span class="sxs-lookup"><span data-stu-id="c6435-159">Type</span></span>           | <span data-ttu-id="c6435-160">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-160">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="c6435-161">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-161">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="c6435-162">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-162">Cancelable</span></span>     | <span data-ttu-id="c6435-163">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-163">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="c6435-164">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-164">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="c6435-165">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-165">Non-cancelable</span></span> | <span data-ttu-id="c6435-166">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-166">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="c6435-167">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-167">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="c6435-168">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-168">Cancelable</span></span>     | <span data-ttu-id="c6435-169">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-169">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="c6435-170">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-170">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="c6435-171">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-171">Non-cancelable</span></span> | <span data-ttu-id="c6435-172">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-172">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="c6435-173">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-173">Customer triggers</span></span>

| <span data-ttu-id="c6435-174">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-174">Trigger</span></span>                   | <span data-ttu-id="c6435-175">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-175">Type</span></span>                    | <span data-ttu-id="c6435-176">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-176">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c6435-177">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-177">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="c6435-178">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-178">Cancelable</span></span>              | <span data-ttu-id="c6435-179">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-179">Executed before adding a customer to the transaction.</span></span>             |
| <span data-ttu-id="c6435-180">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-180">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="c6435-181">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-181">Non-cancelable</span></span>          | <span data-ttu-id="c6435-182">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-182">Executed after adding a customer to the transaction.</span></span>              |
| <span data-ttu-id="c6435-183">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-183">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="c6435-184">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-184">Cancelable</span></span>              | <span data-ttu-id="c6435-185">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-185">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="c6435-186">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-186">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="c6435-187">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-187">Non-cancelable</span></span>          | <span data-ttu-id="c6435-188">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-188">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="c6435-189">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-189">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="c6435-190">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-190">Cancelable</span></span>              | <span data-ttu-id="c6435-191">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-191">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="c6435-192">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-192">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="c6435-193">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-193">Cancelable</span></span>              | <span data-ttu-id="c6435-194">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-194">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="c6435-195">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-195">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="c6435-196">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-196">Non-cancelable</span></span>          | <span data-ttu-id="c6435-197">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-197">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="c6435-198">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-198">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="c6435-199">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-199">Non-cancelable</span></span>          | <span data-ttu-id="c6435-200">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-200">Executed after the loyalty card is issued.</span></span>       |
| <span data-ttu-id="c6435-201">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-201">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="c6435-202">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-202">Cancelable</span></span>          | <span data-ttu-id="c6435-203">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-203">Executed before the customer is created.</span></span>       |
| <span data-ttu-id="c6435-204">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-204">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="c6435-205">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-205">Non-cancelable</span></span>          | <span data-ttu-id="c6435-206">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-206">Executed after the customer is created.</span></span>       |
| <span data-ttu-id="c6435-207">PreSaveCustomerAddressTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-207">PreSaveCustomerAddressTrigger</span></span>      | <span data-ttu-id="c6435-208">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-208">Cancelable</span></span>              | <span data-ttu-id="c6435-209">顧客の住所が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-209">Executed before the customer address is saved.</span></span>            |
| <span data-ttu-id="c6435-210">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-210">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="c6435-211">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-211">Cancelable</span></span>          | <span data-ttu-id="c6435-212">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-212">Executed before getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="c6435-213">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-213">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="c6435-214">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-214">Non-cancelable</span></span>          | <span data-ttu-id="c6435-215">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-215">Executed after getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="c6435-216">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-216">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="c6435-217">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-217">Cancelable</span></span>          | <span data-ttu-id="c6435-218">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-218">Executed before displaying the loyalty card balance.</span></span>       |



## <a name="discount-triggers"></a><span data-ttu-id="c6435-219">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-219">Discount triggers</span></span>

| <span data-ttu-id="c6435-220">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-220">Trigger</span></span>                         | <span data-ttu-id="c6435-221">型</span><span class="sxs-lookup"><span data-stu-id="c6435-221">Type</span></span>           | <span data-ttu-id="c6435-222">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-222">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c6435-223">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-223">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="c6435-224">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-224">Cancelable</span></span>     | <span data-ttu-id="c6435-225">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-225">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="c6435-226">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-226">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="c6435-227">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-227">Non-cancelable</span></span> | <span data-ttu-id="c6435-228">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-228">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="c6435-229">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-229">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="c6435-230">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-230">Cancelable</span></span>     | <span data-ttu-id="c6435-231">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-231">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="c6435-232">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-232">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="c6435-233">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-233">Non-cancelable</span></span> | <span data-ttu-id="c6435-234">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-234">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="c6435-235">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-235">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="c6435-236">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-236">Cancelable</span></span>     | <span data-ttu-id="c6435-237">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-237">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="c6435-238">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-238">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="c6435-239">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-239">Non-cancelable</span></span> | <span data-ttu-id="c6435-240">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-240">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="c6435-241">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-241">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="c6435-242">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-242">Cancelable</span></span>     | <span data-ttu-id="c6435-243">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-243">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="c6435-244">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-244">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="c6435-245">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-245">Non-cancelable</span></span> | <span data-ttu-id="c6435-246">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-246">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="c6435-247">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-247">PreAddCouponTrigger</span></span>             | <span data-ttu-id="c6435-248">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-248">Cancelable</span></span>     | <span data-ttu-id="c6435-249">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-249">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="c6435-250">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-250">PostAddCouponTrigger</span></span>            | <span data-ttu-id="c6435-251">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-251">Non-cancelable</span></span> | <span data-ttu-id="c6435-252">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-252">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="c6435-253">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-253">Operation triggers</span></span>

| <span data-ttu-id="c6435-254">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-254">Trigger</span></span>              | <span data-ttu-id="c6435-255">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-255">Type</span></span>           | <span data-ttu-id="c6435-256">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-256">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="c6435-257">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-257">PreOperationTrigger</span></span>  | <span data-ttu-id="c6435-258">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-258">Cancelable</span></span>     | <span data-ttu-id="c6435-259">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="c6435-259">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="c6435-260">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c6435-260">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="c6435-261">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-261">PreOperationValidationTrigger</span></span> | <span data-ttu-id="c6435-262">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-262">Cancelable</span></span> | <span data-ttu-id="c6435-263">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="c6435-263">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="c6435-264">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-264">OperationFailureTrigger</span></span> | <span data-ttu-id="c6435-265">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-265">Non-cancelable</span></span> | <span data-ttu-id="c6435-266">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="c6435-266">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="c6435-267">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-267">PostOperationTrigger</span></span> | <span data-ttu-id="c6435-268">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-268">Non-cancelable</span></span> | <span data-ttu-id="c6435-269">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="c6435-269">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="c6435-270">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c6435-270">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="c6435-271">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-271">Payment triggers</span></span>

| <span data-ttu-id="c6435-272">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-272">Trigger</span></span>                 | <span data-ttu-id="c6435-273">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-273">Type</span></span>           | <span data-ttu-id="c6435-274">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-274">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="c6435-275">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-275">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="c6435-276">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-276">Cancelable</span></span>     | <span data-ttu-id="c6435-277">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-277">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="c6435-278">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-278">PrePaymentTrigger</span></span>       | <span data-ttu-id="c6435-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-279">Cancelable</span></span>     | <span data-ttu-id="c6435-280">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-280">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="c6435-281">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-281">PostPaymentTrigger</span></span>      | <span data-ttu-id="c6435-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-282">Non-cancelable</span></span> | <span data-ttu-id="c6435-283">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-283">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="c6435-284">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-284">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="c6435-285">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-285">Cancelable</span></span>     | <span data-ttu-id="c6435-286">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-286">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="c6435-287">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-287">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="c6435-288">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-288">Non-cancelable</span></span> | <span data-ttu-id="c6435-289">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-289">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="c6435-290">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-290">Printing Triggers</span></span>

| <span data-ttu-id="c6435-291">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-291">Trigger</span></span>                    | <span data-ttu-id="c6435-292">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-292">Type</span></span>       | <span data-ttu-id="c6435-293">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-293">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="c6435-294">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-294">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="c6435-295">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-295">Cancelable</span></span> | <span data-ttu-id="c6435-296">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-296">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="c6435-297">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-297">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="c6435-298">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-298">Non-cancelable</span></span> | <span data-ttu-id="c6435-299">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-299">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="c6435-300">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-300">Product triggers</span></span>

| <span data-ttu-id="c6435-301">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-301">Trigger</span></span>                    | <span data-ttu-id="c6435-302">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-302">Type</span></span>           | <span data-ttu-id="c6435-303">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-303">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6435-304">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-304">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="c6435-305">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-305">Non-cancelable</span></span> | <span data-ttu-id="c6435-306">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-306">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="c6435-307">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-307">PreProductSaleTrigger</span></span>      | <span data-ttu-id="c6435-308">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-308">Cancelable</span></span>     | <span data-ttu-id="c6435-309">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-309">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="c6435-310">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-310">PostProductSaleTrigger</span></span>     | <span data-ttu-id="c6435-311">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-311">Non-cancelable</span></span> | <span data-ttu-id="c6435-312">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-312">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="c6435-313">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-313">PreReturnProductTrigger</span></span>    | <span data-ttu-id="c6435-314">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-314">Cancelable</span></span>     | <span data-ttu-id="c6435-315">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-315">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="c6435-316">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-316">PostReturnProductTrigger</span></span>   | <span data-ttu-id="c6435-317">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-317">Non-cancelable</span></span> | <span data-ttu-id="c6435-318">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-318">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="c6435-319">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-319">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="c6435-320">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-320">Cancelable</span></span>     | <span data-ttu-id="c6435-321">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-321">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="c6435-322">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-322">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="c6435-323">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-323">Non-cancelable</span></span> | <span data-ttu-id="c6435-324">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-324">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="c6435-325">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-325">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="c6435-326">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-326">Cancelable</span></span>     | <span data-ttu-id="c6435-327">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-327">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="c6435-328">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-328">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="c6435-329">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-329">Non-cancelable</span></span> | <span data-ttu-id="c6435-330">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-330">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="c6435-331">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-331">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="c6435-332">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-332">Cancelable</span></span>     | <span data-ttu-id="c6435-333">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-333">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="c6435-334">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-334">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="c6435-335">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-335">Non-cancelable</span></span> | <span data-ttu-id="c6435-336">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-336">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="c6435-337">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-337">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="c6435-338">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-338">Cancelable</span></span>     | <span data-ttu-id="c6435-339">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-339">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="c6435-340">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-340">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="c6435-341">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-341">Non-cancelable</span></span> | <span data-ttu-id="c6435-342">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-342">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="c6435-343">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-343">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="c6435-344">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-344">Non-cancelable</span></span> | <span data-ttu-id="c6435-345">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-345">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="c6435-346">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-346">Sales order triggers</span></span>

| <span data-ttu-id="c6435-347">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-347">Trigger</span></span>                 | <span data-ttu-id="c6435-348">型</span><span class="sxs-lookup"><span data-stu-id="c6435-348">Type</span></span>           | <span data-ttu-id="c6435-349">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-349">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="c6435-350">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-350">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="c6435-351">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-351">Cancelable</span></span>     | <span data-ttu-id="c6435-352">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-352">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="c6435-353">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-353">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="c6435-354">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-354">Non-cancelable</span></span> | <span data-ttu-id="c6435-355">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-355">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="c6435-356">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-356">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="c6435-357">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-357">Cancelable</span></span>     | <span data-ttu-id="c6435-358">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-358">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="c6435-359">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-359">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="c6435-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-360">Cancelable</span></span>     | <span data-ttu-id="c6435-361">顧客注文時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-361">Executed before the shipping origin is changed during a customer order.</span></span>|
| <span data-ttu-id="c6435-362">PreGetFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-362">PreGetFulfillmentLinesTrigger</span></span>     | <span data-ttu-id="c6435-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-363">Cancelable</span></span>     | <span data-ttu-id="c6435-364">注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-364">Executed before the Order fulfillment lines are loaded in the Order fulfillment view.</span></span>|
| <span data-ttu-id="c6435-365">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-365">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="c6435-366">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-366">Cancelable</span></span>     | <span data-ttu-id="c6435-367">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-367">Executed before the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="c6435-368">PostShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-368">PostShipFulfillmentLinesTrigger</span></span>   | <span data-ttu-id="c6435-369">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-369">Non-Cancelable</span></span>     | <span data-ttu-id="c6435-370">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-370">Executed after the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="c6435-371">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-371">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="c6435-372">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-372">Cancelable</span></span>     | <span data-ttu-id="c6435-373">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-373">Executed before the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="c6435-374">PostMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-374">PostMarkFulfillmentLinesAsPackedTrigger</span></span>   | <span data-ttu-id="c6435-375">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-375">Non-Cancelable</span></span>     | <span data-ttu-id="c6435-376">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-376">Executed after the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="c6435-377">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-377">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="c6435-378">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-378">Cancelable</span></span>     | <span data-ttu-id="c6435-379">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-379">Executed before the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="c6435-380">PostCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-380">PostCreatePackingSlipTrigger</span></span>  | <span data-ttu-id="c6435-381">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-381">Non-Cancelable</span></span>     | <span data-ttu-id="c6435-382">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-382">Executed after the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="c6435-383">PostReturnInvoicedSalesLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-383">PostReturnInvoicedSalesLinesTrigger</span></span>   | <span data-ttu-id="c6435-384">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-384">Non-Cancelable</span></span>     | <span data-ttu-id="c6435-385">返品対象として 1 つ以上の請求書が選択された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-385">Executed after one or more invoices selected for return.</span></span>|


## <a name="shift-triggers"></a><span data-ttu-id="c6435-386">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-386">Shift triggers</span></span>
| <span data-ttu-id="c6435-387">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-387">Trigger</span></span>              | <span data-ttu-id="c6435-388">型</span><span class="sxs-lookup"><span data-stu-id="c6435-388">Type</span></span>           | <span data-ttu-id="c6435-389">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-389">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="c6435-390">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-390">PostOpenShiftTrigger</span></span> | <span data-ttu-id="c6435-391">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-391">Non-cancelable</span></span> | <span data-ttu-id="c6435-392">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-392">This trigger is executed after the new shift is opened.</span></span> |
| <span data-ttu-id="c6435-393">PreCloseShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-393">PreCloseShiftTrigger</span></span> | <span data-ttu-id="c6435-394">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-394">Cancelable</span></span> | <span data-ttu-id="c6435-395">このトリガーは、シフトが開かれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-395">This trigger is executed before the shift is closed.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="c6435-396">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-396">Tax override triggers</span></span>

| <span data-ttu-id="c6435-397">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-397">Trigger</span></span>                           | <span data-ttu-id="c6435-398">型</span><span class="sxs-lookup"><span data-stu-id="c6435-398">Type</span></span>           | <span data-ttu-id="c6435-399">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-399">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="c6435-400">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-400">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="c6435-401">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-401">Cancelable</span></span>     | <span data-ttu-id="c6435-402">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-402">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="c6435-403">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-403">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="c6435-404">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-404">Non-cancelable</span></span> | <span data-ttu-id="c6435-405">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-405">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="c6435-406">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-406">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="c6435-407">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-407">Cancelable</span></span>     | <span data-ttu-id="c6435-408">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-408">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="c6435-409">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-409">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="c6435-410">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-410">Non-cancelable</span></span> | <span data-ttu-id="c6435-411">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-411">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="c6435-412">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-412">Transaction triggers</span></span>

| <span data-ttu-id="c6435-413">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-413">Trigger</span></span>                            | <span data-ttu-id="c6435-414">種類</span><span class="sxs-lookup"><span data-stu-id="c6435-414">Type</span></span>           | <span data-ttu-id="c6435-415">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-415">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="c6435-416">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-416">BeginTransactionTrigger</span></span>            | <span data-ttu-id="c6435-417">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-417">Non-cancelable</span></span> | <span data-ttu-id="c6435-418">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-418">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="c6435-419">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-419">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="c6435-420">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-420">Cancelable</span></span>     | <span data-ttu-id="c6435-421">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-421">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="c6435-422">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-422">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="c6435-423">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-423">Cancelable</span></span>     | <span data-ttu-id="c6435-424">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-424">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="c6435-425">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-425">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="c6435-426">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-426">Non-cancelable</span></span> | <span data-ttu-id="c6435-427">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-427">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="c6435-428">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-428">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="c6435-429">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-429">Cancelable</span></span>     | <span data-ttu-id="c6435-430">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c6435-430">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="c6435-431">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-431">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="c6435-432">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-432">Non-cancelable</span></span> | <span data-ttu-id="c6435-433">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c6435-433">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="c6435-434">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-434">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="c6435-435">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-435">Cancelable</span></span>     | <span data-ttu-id="c6435-436">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-436">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="c6435-437">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-437">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="c6435-438">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-438">Non-cancelable</span></span> | <span data-ttu-id="c6435-439">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-439">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="c6435-440">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-440">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="c6435-441">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-441">Cancelable</span></span>     | <span data-ttu-id="c6435-442">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-442">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="c6435-443">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-443">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="c6435-444">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-444">Non-cancelable</span></span> | <span data-ttu-id="c6435-445">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-445">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="c6435-446">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-446">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="c6435-447">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-447">Cancelable</span></span>     | <span data-ttu-id="c6435-448">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-448">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="c6435-449">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-449">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="c6435-450">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-450">Non-cancelable</span></span> | <span data-ttu-id="c6435-451">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-451">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="c6435-452">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-452">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="c6435-453">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-453">Non-cancelable</span></span> | <span data-ttu-id="c6435-454">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-454">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="c6435-455">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-455">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="c6435-456">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-456">Cancelable</span></span>     | <span data-ttu-id="c6435-457">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-457">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="c6435-458">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-458">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="c6435-459">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="c6435-459">Non-Cancelable</span></span> | <span data-ttu-id="c6435-460">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-460">Executed after the customer order is recalled.</span></span>        |

## <a name="reason-code-triggers"></a><span data-ttu-id="c6435-461">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-461">Reason code triggers</span></span>
| <span data-ttu-id="c6435-462">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-462">Trigger</span></span>              | <span data-ttu-id="c6435-463">型</span><span class="sxs-lookup"><span data-stu-id="c6435-463">Type</span></span>           | <span data-ttu-id="c6435-464">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-464">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="c6435-465">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="c6435-465">PostGetReasonCodeLine</span></span> | <span data-ttu-id="c6435-466">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-466">Cancelable</span></span> | <span data-ttu-id="c6435-467">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-467">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |

## <a name="transfer-order-triggers"></a><span data-ttu-id="c6435-468">移動オーダー トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-468">Transfer Order triggers</span></span>
| <span data-ttu-id="c6435-469">トリガー</span><span class="sxs-lookup"><span data-stu-id="c6435-469">Trigger</span></span>              | <span data-ttu-id="c6435-470">型</span><span class="sxs-lookup"><span data-stu-id="c6435-470">Type</span></span>           | <span data-ttu-id="c6435-471">説明</span><span class="sxs-lookup"><span data-stu-id="c6435-471">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="c6435-472">PreCreateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-472">PreCreateTransferOrderTrigger</span></span> | <span data-ttu-id="c6435-473">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-473">Cancelable</span></span> | <span data-ttu-id="c6435-474">このトリガーは、移動オーダーが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-474">This trigger is executed before the transfer order is created (executed after the order input).</span></span> |
| <span data-ttu-id="c6435-475">PreUpdateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="c6435-475">PreUpdateTransferOrderTrigger</span></span> | <span data-ttu-id="c6435-476">解約可能</span><span class="sxs-lookup"><span data-stu-id="c6435-476">Cancelable</span></span> | <span data-ttu-id="c6435-477">このトリガーは、移動オーダーが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-477">This trigger is executed before the transfer order is updated.</span></span> |


## <a name="business-scenario"></a><span data-ttu-id="c6435-478">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="c6435-478">Business scenario</span></span>
<span data-ttu-id="c6435-479">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-479">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="c6435-480">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="c6435-480">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="c6435-481">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6435-481">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="c6435-482">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="c6435-482">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="c6435-483">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="c6435-483">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="c6435-484">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="c6435-484">Implement a trigger</span></span>

1. <span data-ttu-id="c6435-485">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="c6435-485">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="c6435-486">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="c6435-486">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="c6435-487">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6435-487">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="c6435-488">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6435-488">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="c6435-489">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="c6435-489">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="c6435-490">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="c6435-490">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="c6435-491">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="c6435-491">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="c6435-492">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="c6435-492">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="c6435-493">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c6435-493">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="c6435-494">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="c6435-494">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="c6435-495">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c6435-495">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="c6435-496">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="c6435-496">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="c6435-497">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="c6435-497">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="c6435-498">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="c6435-498">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="c6435-499">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c6435-499">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="c6435-500">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6435-500">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="c6435-501">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="c6435-501">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="c6435-502">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="c6435-502">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="c6435-503">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c6435-503">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="c6435-504">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-504">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="c6435-505">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6435-505">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="c6435-506">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="c6435-506">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="c6435-507">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="c6435-507">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="c6435-508">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="c6435-508">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="c6435-509">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="c6435-509">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="c6435-510">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="c6435-510">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="c6435-511">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c6435-511">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="c6435-512">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="c6435-512">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="c6435-513">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="c6435-513">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="c6435-514">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6435-514">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="c6435-515">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="c6435-515">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6435-516">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c6435-516">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="c6435-517">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="c6435-517">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="c6435-518">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c6435-518">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="c6435-519">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c6435-519">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="c6435-520">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="c6435-520">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="c6435-521">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c6435-521">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="c6435-522">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="c6435-522">Compile and build the project.</span></span>
12. <span data-ttu-id="c6435-523">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c6435-523">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="c6435-524">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c6435-524">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="c6435-525">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c6435-525">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="c6435-526">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="c6435-526">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="c6435-527">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="c6435-527">Save and close the file.</span></span>
17. <span data-ttu-id="c6435-528">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="c6435-528">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="c6435-529">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="c6435-529">Add the custom receipt layout</span></span>

1. <span data-ttu-id="c6435-530">Dynamics 365 Retail を開きます。</span><span class="sxs-lookup"><span data-stu-id="c6435-530">Open Dynamics 365 Retail.</span></span>
2. <span data-ttu-id="c6435-531">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-531">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="c6435-532">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-532">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="c6435-533">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6435-533">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="c6435-534">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6435-534">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="c6435-535">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="c6435-535">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="c6435-536">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="c6435-536">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="c6435-537">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-537">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="c6435-538">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="c6435-538">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="c6435-539">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="c6435-539">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="c6435-540">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-540">Click **Save**.</span></span>
9. <span data-ttu-id="c6435-541">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-541">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="c6435-542">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6435-542">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="c6435-543">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-543">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="c6435-544">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6435-544">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="c6435-545">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-545">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="c6435-546">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-546">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="c6435-547">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="c6435-547">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="c6435-548">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c6435-548">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="c6435-549">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-549">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="c6435-550">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6435-550">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="c6435-551">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="c6435-551">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="c6435-552">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-552">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="c6435-553">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="c6435-553">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="c6435-554">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="c6435-554">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="c6435-555">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-555">Click **Save**.</span></span>
6. <span data-ttu-id="c6435-556">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6435-556">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="c6435-557">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6435-557">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="c6435-558">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="c6435-558">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="c6435-559">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="c6435-559">Validate the extension</span></span>

1. <span data-ttu-id="c6435-560">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="c6435-560">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="c6435-561">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="c6435-561">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="c6435-562">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="c6435-562">Suspend the transaction.</span></span>
4. <span data-ttu-id="c6435-563">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="c6435-563">The custom receipt should print.</span></span>
