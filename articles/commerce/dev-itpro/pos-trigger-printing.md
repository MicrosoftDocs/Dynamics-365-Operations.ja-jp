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
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: 4fdbe10ca39f0ff5eab45d0734959f76acac2ea9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681506"
---
# <a name="pos-triggers"></a><span data-ttu-id="d4685-103">POS トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-103">POS triggers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4685-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d4685-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="d4685-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d4685-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="d4685-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d4685-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="d4685-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4685-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="d4685-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d4685-108">Continue or cancel an operation.</span></span> <span data-ttu-id="d4685-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="d4685-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="d4685-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="d4685-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="d4685-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d4685-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="d4685-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="d4685-112">The following table lists the available triggers and denotes whether they can be canceled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="d4685-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-113">Application triggers</span></span>

| <span data-ttu-id="d4685-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-114">Trigger</span></span>                   | <span data-ttu-id="d4685-115">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-115">Type</span></span>           | <span data-ttu-id="d4685-116">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="d4685-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="d4685-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-118">Non-cancelable</span></span> | <span data-ttu-id="d4685-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-119">Executed after the POS application is started.</span></span> <span data-ttu-id="d4685-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="d4685-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="d4685-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="d4685-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-122">Non-cancelable</span></span> | <span data-ttu-id="d4685-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="d4685-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="d4685-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-125">Cancelable</span></span>     | <span data-ttu-id="d4685-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="d4685-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="d4685-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-128">Non-cancelable</span></span> | <span data-ttu-id="d4685-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="d4685-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="d4685-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-131">Non-cancelable</span></span> | <span data-ttu-id="d4685-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="d4685-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="d4685-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-134">Cancelable</span></span>     | <span data-ttu-id="d4685-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="d4685-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="d4685-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-137">Non-Cancelable</span></span> | <span data-ttu-id="d4685-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="d4685-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="d4685-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-140">Cancelable</span></span>     | <span data-ttu-id="d4685-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="d4685-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="d4685-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-143">Non-Cancelable</span></span> | <span data-ttu-id="d4685-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="d4685-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="d4685-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-146">Cancelable</span></span> | <span data-ttu-id="d4685-147">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-147">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="d4685-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="d4685-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-149">Cancelable</span></span> | <span data-ttu-id="d4685-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="d4685-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="d4685-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-152">Non-Cancelable</span></span> | <span data-ttu-id="d4685-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-153">Executed after the audit event.</span></span>   | 
| <span data-ttu-id="d4685-154">PreOpenUrlTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-154">PreOpenUrlTrigger</span></span>      | <span data-ttu-id="d4685-155">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-155">Cancelable</span></span> | <span data-ttu-id="d4685-156">URLを開く操作の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-156">Executed before the open URL operation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="d4685-157">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-157">Cash management triggers</span></span>

| <span data-ttu-id="d4685-158">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-158">Trigger</span></span>                      | <span data-ttu-id="d4685-159">型</span><span class="sxs-lookup"><span data-stu-id="d4685-159">Type</span></span>           | <span data-ttu-id="d4685-160">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-160">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="d4685-161">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-161">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="d4685-162">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-162">Cancelable</span></span>     | <span data-ttu-id="d4685-163">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-163">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="d4685-164">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-164">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="d4685-165">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-165">Non-cancelable</span></span> | <span data-ttu-id="d4685-166">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-166">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="d4685-167">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-167">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="d4685-168">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-168">Cancelable</span></span>     | <span data-ttu-id="d4685-169">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-169">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="d4685-170">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-170">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="d4685-171">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-171">Non-cancelable</span></span> | <span data-ttu-id="d4685-172">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-172">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="d4685-173">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-173">Customer triggers</span></span>

| <span data-ttu-id="d4685-174">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-174">Trigger</span></span>                   | <span data-ttu-id="d4685-175">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-175">Type</span></span>                    | <span data-ttu-id="d4685-176">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-176">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d4685-177">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-177">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="d4685-178">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-178">Cancelable</span></span>              | <span data-ttu-id="d4685-179">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-179">Executed before adding a customer to the transaction.</span></span>             |
| <span data-ttu-id="d4685-180">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-180">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="d4685-181">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-181">Non-cancelable</span></span>          | <span data-ttu-id="d4685-182">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-182">Executed after adding a customer to the transaction.</span></span>              |
| <span data-ttu-id="d4685-183">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-183">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="d4685-184">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-184">Cancelable</span></span>              | <span data-ttu-id="d4685-185">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-185">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="d4685-186">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-186">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="d4685-187">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-187">Non-cancelable</span></span>          | <span data-ttu-id="d4685-188">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-188">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="d4685-189">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-189">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="d4685-190">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-190">Cancelable</span></span>              | <span data-ttu-id="d4685-191">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-191">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="d4685-192">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-192">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="d4685-193">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-193">Cancelable</span></span>              | <span data-ttu-id="d4685-194">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-194">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="d4685-195">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-195">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="d4685-196">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-196">Non-cancelable</span></span>          | <span data-ttu-id="d4685-197">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-197">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="d4685-198">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-198">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="d4685-199">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-199">Non-cancelable</span></span>          | <span data-ttu-id="d4685-200">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-200">Executed after the loyalty card is issued.</span></span>       |
| <span data-ttu-id="d4685-201">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-201">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="d4685-202">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-202">Cancelable</span></span>          | <span data-ttu-id="d4685-203">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-203">Executed before the customer is created.</span></span>       |
| <span data-ttu-id="d4685-204">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-204">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="d4685-205">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-205">Non-cancelable</span></span>          | <span data-ttu-id="d4685-206">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-206">Executed after the customer is created.</span></span>       |
| <span data-ttu-id="d4685-207">PreSaveCustomerAddressTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-207">PreSaveCustomerAddressTrigger</span></span>      | <span data-ttu-id="d4685-208">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-208">Cancelable</span></span>              | <span data-ttu-id="d4685-209">顧客の住所が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-209">Executed before the customer address is saved.</span></span>            |
| <span data-ttu-id="d4685-210">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-210">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d4685-211">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-211">Cancelable</span></span>          | <span data-ttu-id="d4685-212">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-212">Executed before getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="d4685-213">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-213">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d4685-214">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-214">Non-cancelable</span></span>          | <span data-ttu-id="d4685-215">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-215">Executed after getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="d4685-216">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-216">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d4685-217">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-217">Cancelable</span></span>          | <span data-ttu-id="d4685-218">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-218">Executed before displaying the loyalty card balance.</span></span>       |



## <a name="discount-triggers"></a><span data-ttu-id="d4685-219">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-219">Discount triggers</span></span>

| <span data-ttu-id="d4685-220">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-220">Trigger</span></span>                         | <span data-ttu-id="d4685-221">型</span><span class="sxs-lookup"><span data-stu-id="d4685-221">Type</span></span>           | <span data-ttu-id="d4685-222">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-222">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d4685-223">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-223">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="d4685-224">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-224">Cancelable</span></span>     | <span data-ttu-id="d4685-225">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-225">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="d4685-226">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-226">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="d4685-227">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-227">Non-cancelable</span></span> | <span data-ttu-id="d4685-228">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-228">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="d4685-229">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-229">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="d4685-230">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-230">Cancelable</span></span>     | <span data-ttu-id="d4685-231">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-231">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="d4685-232">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-232">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="d4685-233">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-233">Non-cancelable</span></span> | <span data-ttu-id="d4685-234">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-234">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="d4685-235">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-235">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="d4685-236">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-236">Cancelable</span></span>     | <span data-ttu-id="d4685-237">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-237">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d4685-238">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-238">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="d4685-239">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-239">Non-cancelable</span></span> | <span data-ttu-id="d4685-240">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-240">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="d4685-241">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-241">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="d4685-242">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-242">Cancelable</span></span>     | <span data-ttu-id="d4685-243">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-243">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d4685-244">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-244">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="d4685-245">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-245">Non-cancelable</span></span> | <span data-ttu-id="d4685-246">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-246">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="d4685-247">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-247">PreAddCouponTrigger</span></span>             | <span data-ttu-id="d4685-248">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-248">Cancelable</span></span>     | <span data-ttu-id="d4685-249">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-249">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="d4685-250">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-250">PostAddCouponTrigger</span></span>            | <span data-ttu-id="d4685-251">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-251">Non-cancelable</span></span> | <span data-ttu-id="d4685-252">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-252">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="d4685-253">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-253">Operation triggers</span></span>

| <span data-ttu-id="d4685-254">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-254">Trigger</span></span>              | <span data-ttu-id="d4685-255">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-255">Type</span></span>           | <span data-ttu-id="d4685-256">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-256">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="d4685-257">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-257">PreOperationTrigger</span></span>  | <span data-ttu-id="d4685-258">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-258">Cancelable</span></span>     | <span data-ttu-id="d4685-259">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d4685-259">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="d4685-260">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d4685-260">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="d4685-261">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-261">PreOperationValidationTrigger</span></span> | <span data-ttu-id="d4685-262">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-262">Cancelable</span></span> | <span data-ttu-id="d4685-263">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d4685-263">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="d4685-264">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-264">OperationFailureTrigger</span></span> | <span data-ttu-id="d4685-265">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-265">Non-cancelable</span></span> | <span data-ttu-id="d4685-266">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d4685-266">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="d4685-267">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-267">PostOperationTrigger</span></span> | <span data-ttu-id="d4685-268">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-268">Non-cancelable</span></span> | <span data-ttu-id="d4685-269">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d4685-269">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="d4685-270">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d4685-270">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="d4685-271">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-271">Payment triggers</span></span>

| <span data-ttu-id="d4685-272">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-272">Trigger</span></span>                 | <span data-ttu-id="d4685-273">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-273">Type</span></span>           | <span data-ttu-id="d4685-274">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-274">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4685-275">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-275">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="d4685-276">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-276">Cancelable</span></span>     | <span data-ttu-id="d4685-277">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-277">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="d4685-278">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-278">PrePaymentTrigger</span></span>       | <span data-ttu-id="d4685-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-279">Cancelable</span></span>     | <span data-ttu-id="d4685-280">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-280">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="d4685-281">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-281">PostPaymentTrigger</span></span>      | <span data-ttu-id="d4685-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-282">Non-cancelable</span></span> | <span data-ttu-id="d4685-283">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-283">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="d4685-284">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-284">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="d4685-285">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-285">Cancelable</span></span>     | <span data-ttu-id="d4685-286">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-286">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="d4685-287">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-287">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="d4685-288">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-288">Non-cancelable</span></span> | <span data-ttu-id="d4685-289">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-289">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="d4685-290">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-290">Printing Triggers</span></span>

| <span data-ttu-id="d4685-291">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-291">Trigger</span></span>                    | <span data-ttu-id="d4685-292">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-292">Type</span></span>       | <span data-ttu-id="d4685-293">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-293">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="d4685-294">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-294">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="d4685-295">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-295">Cancelable</span></span> | <span data-ttu-id="d4685-296">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-296">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="d4685-297">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-297">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="d4685-298">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-298">Non-cancelable</span></span> | <span data-ttu-id="d4685-299">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-299">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="d4685-300">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-300">Product triggers</span></span>

| <span data-ttu-id="d4685-301">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-301">Trigger</span></span>                    | <span data-ttu-id="d4685-302">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-302">Type</span></span>           | <span data-ttu-id="d4685-303">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-303">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4685-304">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-304">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="d4685-305">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-305">Non-cancelable</span></span> | <span data-ttu-id="d4685-306">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-306">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="d4685-307">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-307">PreProductSaleTrigger</span></span>      | <span data-ttu-id="d4685-308">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-308">Cancelable</span></span>     | <span data-ttu-id="d4685-309">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-309">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="d4685-310">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-310">PostProductSaleTrigger</span></span>     | <span data-ttu-id="d4685-311">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-311">Non-cancelable</span></span> | <span data-ttu-id="d4685-312">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-312">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="d4685-313">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-313">PreReturnProductTrigger</span></span>    | <span data-ttu-id="d4685-314">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-314">Cancelable</span></span>     | <span data-ttu-id="d4685-315">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-315">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="d4685-316">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-316">PostReturnProductTrigger</span></span>   | <span data-ttu-id="d4685-317">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-317">Non-cancelable</span></span> | <span data-ttu-id="d4685-318">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-318">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="d4685-319">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-319">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="d4685-320">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-320">Cancelable</span></span>     | <span data-ttu-id="d4685-321">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-321">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="d4685-322">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-322">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="d4685-323">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-323">Non-cancelable</span></span> | <span data-ttu-id="d4685-324">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-324">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="d4685-325">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-325">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="d4685-326">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-326">Cancelable</span></span>     | <span data-ttu-id="d4685-327">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-327">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="d4685-328">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-328">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="d4685-329">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-329">Non-cancelable</span></span> | <span data-ttu-id="d4685-330">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-330">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="d4685-331">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-331">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="d4685-332">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-332">Cancelable</span></span>     | <span data-ttu-id="d4685-333">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-333">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="d4685-334">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-334">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="d4685-335">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-335">Non-cancelable</span></span> | <span data-ttu-id="d4685-336">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-336">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="d4685-337">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-337">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="d4685-338">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-338">Cancelable</span></span>     | <span data-ttu-id="d4685-339">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-339">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="d4685-340">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-340">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="d4685-341">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-341">Non-cancelable</span></span> | <span data-ttu-id="d4685-342">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-342">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="d4685-343">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-343">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="d4685-344">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-344">Non-cancelable</span></span> | <span data-ttu-id="d4685-345">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-345">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="d4685-346">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-346">Sales order triggers</span></span>

| <span data-ttu-id="d4685-347">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-347">Trigger</span></span>                 | <span data-ttu-id="d4685-348">型</span><span class="sxs-lookup"><span data-stu-id="d4685-348">Type</span></span>           | <span data-ttu-id="d4685-349">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-349">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4685-350">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-350">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="d4685-351">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-351">Cancelable</span></span>     | <span data-ttu-id="d4685-352">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-352">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="d4685-353">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-353">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="d4685-354">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-354">Non-cancelable</span></span> | <span data-ttu-id="d4685-355">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-355">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="d4685-356">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-356">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="d4685-357">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-357">Cancelable</span></span>     | <span data-ttu-id="d4685-358">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-358">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="d4685-359">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-359">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="d4685-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-360">Cancelable</span></span>     | <span data-ttu-id="d4685-361">顧客注文時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-361">Executed before the shipping origin is changed during a customer order.</span></span>|
| <span data-ttu-id="d4685-362">PreGetFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-362">PreGetFulfillmentLinesTrigger</span></span>     | <span data-ttu-id="d4685-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-363">Cancelable</span></span>     | <span data-ttu-id="d4685-364">注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-364">Executed before the Order fulfillment lines are loaded in the Order fulfillment view.</span></span>|
| <span data-ttu-id="d4685-365">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-365">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="d4685-366">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-366">Cancelable</span></span>     | <span data-ttu-id="d4685-367">**出荷** ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-367">Executed before the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="d4685-368">PostShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-368">PostShipFulfillmentLinesTrigger</span></span>   | <span data-ttu-id="d4685-369">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-369">Non-Cancelable</span></span>     | <span data-ttu-id="d4685-370">**出荷** ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-370">Executed after the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="d4685-371">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-371">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="d4685-372">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-372">Cancelable</span></span>     | <span data-ttu-id="d4685-373">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-373">Executed before the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d4685-374">PostMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-374">PostMarkFulfillmentLinesAsPackedTrigger</span></span>   | <span data-ttu-id="d4685-375">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-375">Non-Cancelable</span></span>     | <span data-ttu-id="d4685-376">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-376">Executed after the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d4685-377">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-377">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="d4685-378">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-378">Cancelable</span></span>     | <span data-ttu-id="d4685-379">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-379">Executed before the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d4685-380">PostCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-380">PostCreatePackingSlipTrigger</span></span>  | <span data-ttu-id="d4685-381">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-381">Non-Cancelable</span></span>     | <span data-ttu-id="d4685-382">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-382">Executed after the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d4685-383">PostReturnInvoicedSalesLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-383">PostReturnInvoicedSalesLinesTrigger</span></span>   | <span data-ttu-id="d4685-384">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-384">Non-Cancelable</span></span>     | <span data-ttu-id="d4685-385">返品対象として 1 つ以上の請求書が選択された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-385">Executed after one or more invoices selected for return.</span></span>|
| <span data-ttu-id="d4685-386">PreResendEmailReceiptTrigger (10.0.13)</span><span class="sxs-lookup"><span data-stu-id="d4685-386">PreResendEmailReceiptTrigger (10.0.13)</span></span>    | <span data-ttu-id="d4685-387">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-387">Cancelable</span></span>     | <span data-ttu-id="d4685-388">仕訳帳ビューを表示から電子メールを送信する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-388">Executed before sending the email from the Show journal view.</span></span>|



## <a name="shift-triggers"></a><span data-ttu-id="d4685-389">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-389">Shift triggers</span></span>

| <span data-ttu-id="d4685-390">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-390">Trigger</span></span>              | <span data-ttu-id="d4685-391">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-391">Type</span></span>           | <span data-ttu-id="d4685-392">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-392">Description</span></span>                                             | <span data-ttu-id="d4685-393">リリース</span><span class="sxs-lookup"><span data-stu-id="d4685-393">Release</span></span>    |
|----------------------|----------------|---------------------------------------------------------|--------------|
| <span data-ttu-id="d4685-394">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-394">PostOpenShiftTrigger</span></span> | <span data-ttu-id="d4685-395">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-395">Non-cancelable</span></span> | <span data-ttu-id="d4685-396">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-396">This trigger is executed after the new shift is opened.</span></span> |     |
| <span data-ttu-id="d4685-397">PreCloseShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-397">PreCloseShiftTrigger</span></span> | <span data-ttu-id="d4685-398">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-398">Cancelable</span></span> | <span data-ttu-id="d4685-399">このトリガーは、シフトが開かれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-399">This trigger is executed before the shift is closed.</span></span> |    |
| <span data-ttu-id="d4685-400">PreResumeShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-400">PreResumeShiftTrigger</span></span> | <span data-ttu-id="d4685-401">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-401">Cancelable</span></span> | <span data-ttu-id="d4685-402">このトリガーは、シフトが再開される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-402">This trigger is executed before the shift is resumed.</span></span> |<span data-ttu-id="d4685-403">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d4685-403">10.0.16</span></span>   |
| <span data-ttu-id="d4685-404">PostResumeShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-404">PostResumeShiftTrigger</span></span> | <span data-ttu-id="d4685-405">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-405">Non-cancelable</span></span> | <span data-ttu-id="d4685-406">このトリガーは、シフトが再開された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-406">This trigger is executed after the shift is resumed.</span></span> | <span data-ttu-id="d4685-407">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d4685-407">10.0.16</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="d4685-408">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-408">Tax override triggers</span></span>

| <span data-ttu-id="d4685-409">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-409">Trigger</span></span>                           | <span data-ttu-id="d4685-410">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-410">Type</span></span>           | <span data-ttu-id="d4685-411">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-411">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="d4685-412">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-412">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="d4685-413">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-413">Cancelable</span></span>     | <span data-ttu-id="d4685-414">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-414">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="d4685-415">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-415">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="d4685-416">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-416">Non-cancelable</span></span> | <span data-ttu-id="d4685-417">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-417">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="d4685-418">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-418">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="d4685-419">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-419">Cancelable</span></span>     | <span data-ttu-id="d4685-420">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-420">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="d4685-421">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-421">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="d4685-422">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-422">Non-cancelable</span></span> | <span data-ttu-id="d4685-423">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-423">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="d4685-424">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-424">Transaction triggers</span></span>

| <span data-ttu-id="d4685-425">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-425">Trigger</span></span>                            | <span data-ttu-id="d4685-426">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-426">Type</span></span>           | <span data-ttu-id="d4685-427">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-427">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="d4685-428">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-428">BeginTransactionTrigger</span></span>            | <span data-ttu-id="d4685-429">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-429">Non-cancelable</span></span> | <span data-ttu-id="d4685-430">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-430">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="d4685-431">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-431">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="d4685-432">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-432">Cancelable</span></span>     | <span data-ttu-id="d4685-433">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-433">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="d4685-434">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-434">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="d4685-435">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-435">Cancelable</span></span>     | <span data-ttu-id="d4685-436">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-436">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="d4685-437">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-437">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="d4685-438">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-438">Non-cancelable</span></span> | <span data-ttu-id="d4685-439">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-439">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="d4685-440">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-440">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="d4685-441">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-441">Cancelable</span></span>     | <span data-ttu-id="d4685-442">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d4685-442">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="d4685-443">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-443">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="d4685-444">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-444">Non-cancelable</span></span> | <span data-ttu-id="d4685-445">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d4685-445">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="d4685-446">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-446">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="d4685-447">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-447">Cancelable</span></span>     | <span data-ttu-id="d4685-448">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-448">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="d4685-449">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-449">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="d4685-450">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-450">Non-cancelable</span></span> | <span data-ttu-id="d4685-451">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-451">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="d4685-452">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-452">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="d4685-453">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-453">Cancelable</span></span>     | <span data-ttu-id="d4685-454">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-454">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="d4685-455">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-455">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="d4685-456">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-456">Non-cancelable</span></span> | <span data-ttu-id="d4685-457">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-457">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="d4685-458">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-458">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d4685-459">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-459">Cancelable</span></span>     | <span data-ttu-id="d4685-460">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-460">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="d4685-461">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-461">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d4685-462">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-462">Non-cancelable</span></span> | <span data-ttu-id="d4685-463">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-463">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="d4685-464">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-464">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="d4685-465">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-465">Non-cancelable</span></span> | <span data-ttu-id="d4685-466">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-466">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="d4685-467">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-467">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d4685-468">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-468">Cancelable</span></span>     | <span data-ttu-id="d4685-469">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-469">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="d4685-470">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-470">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d4685-471">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d4685-471">Non-Cancelable</span></span> | <span data-ttu-id="d4685-472">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-472">Executed after the customer order is recalled.</span></span>        |
| <span data-ttu-id="d4685-473">PreSelectTransactionPaymentMethodTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-473">PreSelectTransactionPaymentMethodTrigger</span></span>       | <span data-ttu-id="d4685-474">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-474">Cancelable</span></span> |  <span data-ttu-id="d4685-475">ユーザーが **カート ビュー - 合計** パネルで **合計** を選択すると、使用可能な支払方法が表示され、このトリガーはこのダイアログが表示される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-475">When the user selects the **Totals** button in the **Cart view - totals** panel, the available payment methods are shown and this trigger will get executed before this dialog is shown.</span></span> <span data-ttu-id="d4685-476">このトリガーから利用可能な支払方法を変更するための拡張コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d4685-476">You can us extension code to modify the available payment methods from this trigger.</span></span>      |
| <span data-ttu-id="d4685-477">PreShipSelectedCartLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-477">PreShipSelectedCartLinesTrigger</span></span>       | <span data-ttu-id="d4685-478">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-478">Cancelable</span></span> |  <span data-ttu-id="d4685-479">製品が出荷対象として選択されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-479">Executed when the product is selected for shipping.</span></span>      |

## <a name="reason-code-triggers"></a><span data-ttu-id="d4685-480">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-480">Reason code triggers</span></span>
| <span data-ttu-id="d4685-481">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-481">Trigger</span></span>              | <span data-ttu-id="d4685-482">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-482">Type</span></span>           | <span data-ttu-id="d4685-483">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-483">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d4685-484">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="d4685-484">PostGetReasonCodeLine</span></span> | <span data-ttu-id="d4685-485">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-485">Cancelable</span></span> | <span data-ttu-id="d4685-486">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-486">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |

## <a name="transfer-order-triggers"></a><span data-ttu-id="d4685-487">移動オーダー トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-487">Transfer Order triggers</span></span>
| <span data-ttu-id="d4685-488">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-488">Trigger</span></span>              | <span data-ttu-id="d4685-489">型</span><span class="sxs-lookup"><span data-stu-id="d4685-489">Type</span></span>           | <span data-ttu-id="d4685-490">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-490">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d4685-491">PreCreateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-491">PreCreateTransferOrderTrigger</span></span> | <span data-ttu-id="d4685-492">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-492">Cancelable</span></span> | <span data-ttu-id="d4685-493">このトリガーは、移動オーダーが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-493">This trigger is executed before the transfer order is created (executed after the order input).</span></span> |
| <span data-ttu-id="d4685-494">PreUpdateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-494">PreUpdateTransferOrderTrigger</span></span> | <span data-ttu-id="d4685-495">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-495">Cancelable</span></span> | <span data-ttu-id="d4685-496">このトリガーは、移動オーダーが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-496">This trigger is executed before the transfer order is updated.</span></span> |

## <a name="inventory-triggers"></a><span data-ttu-id="d4685-497">在庫トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-497">Inventory triggers</span></span>
| <span data-ttu-id="d4685-498">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-498">Trigger</span></span>              | <span data-ttu-id="d4685-499">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-499">Type</span></span>           | <span data-ttu-id="d4685-500">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-500">Description</span></span>                                             | <span data-ttu-id="d4685-501">リリース</span><span class="sxs-lookup"><span data-stu-id="d4685-501">Release</span></span>     |
|----------------------|----------------|---------------------------------------------------------|--------------------------|
| <span data-ttu-id="d4685-502">PreCreateInventoryDocumentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-502">PreCreateInventoryDocumentTrigger</span></span> | <span data-ttu-id="d4685-503">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-503">Cancelable</span></span> | <span data-ttu-id="d4685-504">このトリガーは、入庫/出庫ドキュメントが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-504">This trigger is executed before the inbound/outbound document is created (executed after the order input).</span></span> | <span data-ttu-id="d4685-505">10.0.15</span><span class="sxs-lookup"><span data-stu-id="d4685-505">10.0.15</span></span> |
| <span data-ttu-id="d4685-506">PreUpdateInventoryDocumentTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-506">PreUpdateInventoryDocumentTrigger</span></span> | <span data-ttu-id="d4685-507">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-507">Cancelable</span></span> | <span data-ttu-id="d4685-508">このトリガーは、入庫/出庫ドキュメントが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-508">This trigger is executed before the inbound/outbound document is updated.</span></span> | <span data-ttu-id="d4685-509">10.0.15</span><span class="sxs-lookup"><span data-stu-id="d4685-509">10.0.15</span></span> |

## <a name="stock-count-triggers"></a><span data-ttu-id="d4685-510">在庫数のトリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-510">Stock count triggers</span></span>

| <span data-ttu-id="d4685-511">トリガー</span><span class="sxs-lookup"><span data-stu-id="d4685-511">Trigger</span></span>              | <span data-ttu-id="d4685-512">種類</span><span class="sxs-lookup"><span data-stu-id="d4685-512">Type</span></span>           | <span data-ttu-id="d4685-513">説明</span><span class="sxs-lookup"><span data-stu-id="d4685-513">Description</span></span>                                             | <span data-ttu-id="d4685-514">リリース</span><span class="sxs-lookup"><span data-stu-id="d4685-514">Release</span></span>    |
|----------------------|----------------|---------------------------------------------------------|--------------|
| <span data-ttu-id="d4685-515">PreAdjustStockCountLineQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-515">PreAdjustStockCountLineQuantityTrigger</span></span> | <span data-ttu-id="d4685-516">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-516">Cancelable</span></span> | <span data-ttu-id="d4685-517">このトリガーは、明細行の在庫数が調整される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-517">This trigger is executed before the stock count for a line is adjusted.</span></span> |<span data-ttu-id="d4685-518">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d4685-518">10.0.16</span></span>    |
| <span data-ttu-id="d4685-519">PreSaveStockCountJournalTrigger</span><span class="sxs-lookup"><span data-stu-id="d4685-519">PreSaveStockCountJournalTrigger</span></span> | <span data-ttu-id="d4685-520">解約可能</span><span class="sxs-lookup"><span data-stu-id="d4685-520">Cancelable</span></span> | <span data-ttu-id="d4685-521">このトリガーは、在庫数仕訳帳が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-521">This trigger is executed before the stock count journal is saved.</span></span> | <span data-ttu-id="d4685-522">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d4685-522">10.0.16</span></span> |

## <a name="business-scenario"></a><span data-ttu-id="d4685-523">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="d4685-523">Business scenario</span></span>
<span data-ttu-id="d4685-524">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-524">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="d4685-525">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d4685-525">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="d4685-526">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4685-526">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="d4685-527">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="d4685-527">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="d4685-528">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="d4685-528">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="d4685-529">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="d4685-529">Implement a trigger</span></span>

1. <span data-ttu-id="d4685-530">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="d4685-530">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="d4685-531">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="d4685-531">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="d4685-532">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d4685-532">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d4685-533">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d4685-533">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="d4685-534">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d4685-534">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="d4685-535">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d4685-535">Add the following **import** statements to import the relevant entities and context.</span></span>

   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
   
7. <span data-ttu-id="d4685-536">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="d4685-536">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
    ```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
    ```
8. <span data-ttu-id="d4685-537">トリガーの **実行** メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d4685-537">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
   
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
   
   <span data-ttu-id="d4685-538">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d4685-538">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="d4685-539">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d4685-539">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="d4685-540">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d4685-540">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="d4685-541">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d4685-541">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="d4685-542">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="d4685-542">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="d4685-543">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="d4685-543">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="d4685-544">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d4685-544">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="d4685-545">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4685-545">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="d4685-546">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="d4685-546">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="d4685-547">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="d4685-547">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="d4685-548">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4685-548">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="d4685-549">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-549">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="d4685-550">**ファイル** メニューで、**開く \> プロジェクト/ソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4685-550">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="d4685-551">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="d4685-551">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="d4685-552">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d4685-552">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d4685-553">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="d4685-553">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="d4685-554">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d4685-554">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="d4685-555">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="d4685-555">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="d4685-556">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d4685-556">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="d4685-557">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="d4685-557">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="d4685-558">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点ではコマース トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="d4685-558">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the commerce transaction table.</span></span> <span data-ttu-id="d4685-559">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4685-559">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="d4685-560">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="d4685-560">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4685-561">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d4685-561">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="d4685-562">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="d4685-562">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="d4685-563">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d4685-563">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="d4685-564">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d4685-564">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="d4685-565">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="d4685-565">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="d4685-566">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d4685-566">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="d4685-567">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="d4685-567">Compile and build the project.</span></span>
12. <span data-ttu-id="d4685-568">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d4685-568">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="d4685-569">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d4685-569">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="d4685-570">また、**…\\RetailSDK\\参照** フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d4685-570">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="d4685-571">**commerceruntime.ext.config** ファイルを開き、\<composition\> セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="d4685-571">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="d4685-572">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="d4685-572">Save and close the file.</span></span>
17. <span data-ttu-id="d4685-573">Commerce Scale Unit を再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="d4685-573">Restart the Commerce Scale Unit to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="d4685-574">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="d4685-574">Add the custom receipt layout</span></span>

1. <span data-ttu-id="d4685-575">Dynamics 365 Commerce を開きます。</span><span class="sxs-lookup"><span data-stu-id="d4685-575">Open Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="d4685-576">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS** > **受領書フォーマット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-576">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="d4685-577">**受領書フォーマット** 内の **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-577">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="d4685-578">**提出した受領書フォーマット** フィールドに、**中断** という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4685-578">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="d4685-579">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4685-579">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="d4685-580">**デザイナー** をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="d4685-580">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="d4685-581">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="d4685-581">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="d4685-582">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-582">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="d4685-583">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="d4685-583">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="d4685-584">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="d4685-584">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="d4685-585">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-585">Click **Save**.</span></span>
9. <span data-ttu-id="d4685-586">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **視覚プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-586">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="d4685-587">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d4685-587">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="d4685-588">**一般** タブの **追加** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-588">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="d4685-589">**受領書タイプ** で、**CustomReceiptType7** を選択し、**受領書フォーマット** で **中断** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4685-589">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="d4685-590">**Retail とコマース > Retail とコマース IT > 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-590">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="d4685-591">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-591">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d4685-592">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d4685-592">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="d4685-593">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d4685-593">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="d4685-594">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-594">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="d4685-595">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d4685-595">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="d4685-596">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4685-596">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="d4685-597">操作バーの **編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-597">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="d4685-598">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="d4685-598">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="d4685-599">**プリンター** ドロップダウン リストで、**Windows ドライバー** を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d4685-599">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="d4685-600">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-600">Click **Save**.</span></span>
6. <span data-ttu-id="d4685-601">**Retail とコマース** > **Retail とコマース IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4685-601">Go to **Retail and Commerce** > **Retail and Commerce IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="d4685-602">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4685-602">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d4685-603">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d4685-603">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="d4685-604">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="d4685-604">Validate the extension</span></span>

1. <span data-ttu-id="d4685-605">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="d4685-605">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="d4685-606">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d4685-606">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="d4685-607">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="d4685-607">Suspend the transaction.</span></span>
4. <span data-ttu-id="d4685-608">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d4685-608">The custom receipt should print.</span></span>
