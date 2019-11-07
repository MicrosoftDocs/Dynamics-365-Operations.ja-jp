---
title: Retail Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 10/07/2019
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
ms.openlocfilehash: 3bf04344b95a6cb1a18f0cb789e4f5883d8e01ca
ms.sourcegitcommit: a3fbcd63f10f204350a058a124ba80abeb34309e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2019
ms.locfileid: "2564182"
---
# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="d58d7-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="d58d7-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d58d7-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="d58d7-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="d58d7-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="d58d7-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="d58d7-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-108">Continue or cancel an operation.</span></span> <span data-ttu-id="d58d7-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="d58d7-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="d58d7-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="d58d7-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="d58d7-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="d58d7-112">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="d58d7-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-113">Application triggers</span></span>

| <span data-ttu-id="d58d7-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-114">Trigger</span></span>                   | <span data-ttu-id="d58d7-115">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-115">Type</span></span>           | <span data-ttu-id="d58d7-116">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="d58d7-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="d58d7-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-118">Non-cancelable</span></span> | <span data-ttu-id="d58d7-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-119">Executed after the POS application is started.</span></span> <span data-ttu-id="d58d7-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="d58d7-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="d58d7-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-122">Non-cancelable</span></span> | <span data-ttu-id="d58d7-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="d58d7-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="d58d7-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-125">Cancelable</span></span>     | <span data-ttu-id="d58d7-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="d58d7-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="d58d7-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-128">Non-cancelable</span></span> | <span data-ttu-id="d58d7-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="d58d7-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="d58d7-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-131">Non-cancelable</span></span> | <span data-ttu-id="d58d7-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="d58d7-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="d58d7-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-134">Cancelable</span></span>     | <span data-ttu-id="d58d7-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="d58d7-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="d58d7-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-137">Non-Cancelable</span></span> | <span data-ttu-id="d58d7-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="d58d7-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="d58d7-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-140">Cancelable</span></span>     | <span data-ttu-id="d58d7-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="d58d7-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="d58d7-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-143">Non-Cancelable</span></span> | <span data-ttu-id="d58d7-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="d58d7-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="d58d7-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-146">Cancelable</span></span> | <span data-ttu-id="d58d7-147">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-147">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="d58d7-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="d58d7-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-149">Cancelable</span></span> | <span data-ttu-id="d58d7-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="d58d7-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="d58d7-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-152">Non-Cancelable</span></span> | <span data-ttu-id="d58d7-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-153">Executed after the audit event.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="d58d7-154">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-154">Cash management triggers</span></span>

| <span data-ttu-id="d58d7-155">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-155">Trigger</span></span>                      | <span data-ttu-id="d58d7-156">型</span><span class="sxs-lookup"><span data-stu-id="d58d7-156">Type</span></span>           | <span data-ttu-id="d58d7-157">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-157">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="d58d7-158">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-158">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="d58d7-159">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-159">Cancelable</span></span>     | <span data-ttu-id="d58d7-160">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-160">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="d58d7-161">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-161">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="d58d7-162">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-162">Non-cancelable</span></span> | <span data-ttu-id="d58d7-163">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-163">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="d58d7-164">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-164">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="d58d7-165">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-165">Cancelable</span></span>     | <span data-ttu-id="d58d7-166">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-166">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="d58d7-167">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-167">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="d58d7-168">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-168">Non-cancelable</span></span> | <span data-ttu-id="d58d7-169">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-169">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="d58d7-170">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-170">Customer triggers</span></span>

| <span data-ttu-id="d58d7-171">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-171">Trigger</span></span>                   | <span data-ttu-id="d58d7-172">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-172">Type</span></span>                    | <span data-ttu-id="d58d7-173">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-173">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d58d7-174">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-174">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="d58d7-175">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-175">Cancelable</span></span>              | <span data-ttu-id="d58d7-176">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-176">Executed before adding a customer to the transaction.</span></span>             |
| <span data-ttu-id="d58d7-177">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-177">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="d58d7-178">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-178">Non-cancelable</span></span>          | <span data-ttu-id="d58d7-179">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-179">Executed after adding a customer to the transaction.</span></span>              |
| <span data-ttu-id="d58d7-180">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-180">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="d58d7-181">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-181">Cancelable</span></span>              | <span data-ttu-id="d58d7-182">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-182">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="d58d7-183">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-183">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="d58d7-184">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-184">Non-cancelable</span></span>          | <span data-ttu-id="d58d7-185">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-185">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="d58d7-186">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-186">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="d58d7-187">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-187">Cancelable</span></span>              | <span data-ttu-id="d58d7-188">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-188">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="d58d7-189">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-189">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="d58d7-190">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-190">Cancelable</span></span>              | <span data-ttu-id="d58d7-191">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-191">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="d58d7-192">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-192">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="d58d7-193">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-193">Non-cancelable</span></span>          | <span data-ttu-id="d58d7-194">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-194">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="d58d7-195">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-195">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="d58d7-196">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-196">Non-cancelable</span></span>          | <span data-ttu-id="d58d7-197">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-197">Executed after the loyalty card is issued.</span></span>       |
| <span data-ttu-id="d58d7-198">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-198">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="d58d7-199">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-199">Cancelable</span></span>          | <span data-ttu-id="d58d7-200">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-200">Executed before the customer is created.</span></span>       |
| <span data-ttu-id="d58d7-201">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-201">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="d58d7-202">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-202">Non-cancelable</span></span>          | <span data-ttu-id="d58d7-203">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-203">Executed after the customer is created.</span></span>       |
| <span data-ttu-id="d58d7-204">PreSaveCustomerAddressTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-204">PreSaveCustomerAddressTrigger</span></span>      | <span data-ttu-id="d58d7-205">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-205">Cancelable</span></span>              | <span data-ttu-id="d58d7-206">顧客の住所が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-206">Executed before the customer address is saved.</span></span>            |
| <span data-ttu-id="d58d7-207">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-207">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d58d7-208">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-208">Cancelable</span></span>          | <span data-ttu-id="d58d7-209">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-209">Executed before getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="d58d7-210">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-210">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d58d7-211">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-211">Non-cancelable</span></span>          | <span data-ttu-id="d58d7-212">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-212">Executed after getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="d58d7-213">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-213">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d58d7-214">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-214">Cancelable</span></span>          | <span data-ttu-id="d58d7-215">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-215">Executed before displaying the loyalty card balance.</span></span>       |



## <a name="discount-triggers"></a><span data-ttu-id="d58d7-216">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-216">Discount triggers</span></span>

| <span data-ttu-id="d58d7-217">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-217">Trigger</span></span>                         | <span data-ttu-id="d58d7-218">型</span><span class="sxs-lookup"><span data-stu-id="d58d7-218">Type</span></span>           | <span data-ttu-id="d58d7-219">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-219">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d58d7-220">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-220">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="d58d7-221">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-221">Cancelable</span></span>     | <span data-ttu-id="d58d7-222">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-222">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="d58d7-223">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-223">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="d58d7-224">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-224">Non-cancelable</span></span> | <span data-ttu-id="d58d7-225">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-225">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="d58d7-226">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-226">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="d58d7-227">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-227">Cancelable</span></span>     | <span data-ttu-id="d58d7-228">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-228">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="d58d7-229">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-229">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="d58d7-230">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-230">Non-cancelable</span></span> | <span data-ttu-id="d58d7-231">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-231">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="d58d7-232">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-232">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="d58d7-233">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-233">Cancelable</span></span>     | <span data-ttu-id="d58d7-234">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-234">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d58d7-235">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-235">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="d58d7-236">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-236">Non-cancelable</span></span> | <span data-ttu-id="d58d7-237">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-237">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="d58d7-238">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-238">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="d58d7-239">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-239">Cancelable</span></span>     | <span data-ttu-id="d58d7-240">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-240">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d58d7-241">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-241">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="d58d7-242">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-242">Non-cancelable</span></span> | <span data-ttu-id="d58d7-243">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-243">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="d58d7-244">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-244">PreAddCouponTrigger</span></span>             | <span data-ttu-id="d58d7-245">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-245">Cancelable</span></span>     | <span data-ttu-id="d58d7-246">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-246">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="d58d7-247">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-247">PostAddCouponTrigger</span></span>            | <span data-ttu-id="d58d7-248">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-248">Non-cancelable</span></span> | <span data-ttu-id="d58d7-249">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-249">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="d58d7-250">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-250">Operation triggers</span></span>

| <span data-ttu-id="d58d7-251">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-251">Trigger</span></span>              | <span data-ttu-id="d58d7-252">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-252">Type</span></span>           | <span data-ttu-id="d58d7-253">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-253">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="d58d7-254">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-254">PreOperationTrigger</span></span>  | <span data-ttu-id="d58d7-255">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-255">Cancelable</span></span>     | <span data-ttu-id="d58d7-256">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d58d7-256">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="d58d7-257">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-257">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="d58d7-258">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-258">PreOperationValidationTrigger</span></span> | <span data-ttu-id="d58d7-259">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-259">Cancelable</span></span> | <span data-ttu-id="d58d7-260">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d58d7-260">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="d58d7-261">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-261">OperationFailureTrigger</span></span> | <span data-ttu-id="d58d7-262">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-262">Non-cancelable</span></span> | <span data-ttu-id="d58d7-263">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d58d7-263">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="d58d7-264">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-264">PostOperationTrigger</span></span> | <span data-ttu-id="d58d7-265">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-265">Non-cancelable</span></span> | <span data-ttu-id="d58d7-266">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d58d7-266">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="d58d7-267">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-267">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="d58d7-268">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-268">Payment triggers</span></span>

| <span data-ttu-id="d58d7-269">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-269">Trigger</span></span>                 | <span data-ttu-id="d58d7-270">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-270">Type</span></span>           | <span data-ttu-id="d58d7-271">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-271">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d58d7-272">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-272">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="d58d7-273">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-273">Cancelable</span></span>     | <span data-ttu-id="d58d7-274">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-274">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="d58d7-275">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-275">PrePaymentTrigger</span></span>       | <span data-ttu-id="d58d7-276">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-276">Cancelable</span></span>     | <span data-ttu-id="d58d7-277">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-277">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="d58d7-278">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-278">PostPaymentTrigger</span></span>      | <span data-ttu-id="d58d7-279">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-279">Non-cancelable</span></span> | <span data-ttu-id="d58d7-280">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-280">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="d58d7-281">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-281">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="d58d7-282">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-282">Cancelable</span></span>     | <span data-ttu-id="d58d7-283">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-283">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="d58d7-284">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-284">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="d58d7-285">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-285">Non-cancelable</span></span> | <span data-ttu-id="d58d7-286">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-286">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="d58d7-287">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-287">Printing Triggers</span></span>

| <span data-ttu-id="d58d7-288">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-288">Trigger</span></span>                    | <span data-ttu-id="d58d7-289">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-289">Type</span></span>       | <span data-ttu-id="d58d7-290">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-290">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="d58d7-291">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-291">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="d58d7-292">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-292">Cancelable</span></span> | <span data-ttu-id="d58d7-293">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-293">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="d58d7-294">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-294">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="d58d7-295">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-295">Non-cancelable</span></span> | <span data-ttu-id="d58d7-296">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-296">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="d58d7-297">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-297">Product triggers</span></span>

| <span data-ttu-id="d58d7-298">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-298">Trigger</span></span>                    | <span data-ttu-id="d58d7-299">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-299">Type</span></span>           | <span data-ttu-id="d58d7-300">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-300">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d58d7-301">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-301">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="d58d7-302">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-302">Non-cancelable</span></span> | <span data-ttu-id="d58d7-303">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-303">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="d58d7-304">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-304">PreProductSaleTrigger</span></span>      | <span data-ttu-id="d58d7-305">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-305">Cancelable</span></span>     | <span data-ttu-id="d58d7-306">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-306">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="d58d7-307">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-307">PostProductSaleTrigger</span></span>     | <span data-ttu-id="d58d7-308">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-308">Non-cancelable</span></span> | <span data-ttu-id="d58d7-309">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-309">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="d58d7-310">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-310">PreReturnProductTrigger</span></span>    | <span data-ttu-id="d58d7-311">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-311">Cancelable</span></span>     | <span data-ttu-id="d58d7-312">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-312">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="d58d7-313">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-313">PostReturnProductTrigger</span></span>   | <span data-ttu-id="d58d7-314">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-314">Non-cancelable</span></span> | <span data-ttu-id="d58d7-315">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-315">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="d58d7-316">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-316">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="d58d7-317">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-317">Cancelable</span></span>     | <span data-ttu-id="d58d7-318">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-318">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="d58d7-319">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-319">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="d58d7-320">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-320">Non-cancelable</span></span> | <span data-ttu-id="d58d7-321">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-321">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="d58d7-322">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-322">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="d58d7-323">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-323">Cancelable</span></span>     | <span data-ttu-id="d58d7-324">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-324">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="d58d7-325">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-325">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="d58d7-326">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-326">Non-cancelable</span></span> | <span data-ttu-id="d58d7-327">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-327">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="d58d7-328">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-328">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="d58d7-329">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-329">Cancelable</span></span>     | <span data-ttu-id="d58d7-330">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-330">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="d58d7-331">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-331">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="d58d7-332">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-332">Non-cancelable</span></span> | <span data-ttu-id="d58d7-333">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-333">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="d58d7-334">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-334">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="d58d7-335">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-335">Cancelable</span></span>     | <span data-ttu-id="d58d7-336">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-336">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="d58d7-337">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-337">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="d58d7-338">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-338">Non-cancelable</span></span> | <span data-ttu-id="d58d7-339">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-339">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="d58d7-340">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-340">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="d58d7-341">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-341">Non-cancelable</span></span> | <span data-ttu-id="d58d7-342">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-342">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="d58d7-343">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-343">Sales order triggers</span></span>

| <span data-ttu-id="d58d7-344">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-344">Trigger</span></span>                 | <span data-ttu-id="d58d7-345">型</span><span class="sxs-lookup"><span data-stu-id="d58d7-345">Type</span></span>           | <span data-ttu-id="d58d7-346">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-346">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d58d7-347">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-347">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="d58d7-348">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-348">Cancelable</span></span>     | <span data-ttu-id="d58d7-349">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-349">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="d58d7-350">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-350">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="d58d7-351">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-351">Non-cancelable</span></span> | <span data-ttu-id="d58d7-352">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-352">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="d58d7-353">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-353">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="d58d7-354">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-354">Cancelable</span></span>     | <span data-ttu-id="d58d7-355">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-355">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="d58d7-356">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-356">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="d58d7-357">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-357">Cancelable</span></span>     | <span data-ttu-id="d58d7-358">顧客注文時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-358">Executed before the shipping origin is changed during a customer order.</span></span>|
| <span data-ttu-id="d58d7-359">PreGetFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-359">PreGetFulfillmentLinesTrigger</span></span>     | <span data-ttu-id="d58d7-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-360">Cancelable</span></span>     | <span data-ttu-id="d58d7-361">注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-361">Executed before the Order fulfillment lines are loaded in the Order fulfillment view.</span></span>|
| <span data-ttu-id="d58d7-362">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-362">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="d58d7-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-363">Cancelable</span></span>     | <span data-ttu-id="d58d7-364">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-364">Executed before the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="d58d7-365">PostShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-365">PostShipFulfillmentLinesTrigger</span></span>   | <span data-ttu-id="d58d7-366">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-366">Non-Cancelable</span></span>     | <span data-ttu-id="d58d7-367">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-367">Executed after the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="d58d7-368">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-368">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="d58d7-369">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-369">Cancelable</span></span>     | <span data-ttu-id="d58d7-370">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-370">Executed before the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d58d7-371">PostMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-371">PostMarkFulfillmentLinesAsPackedTrigger</span></span>   | <span data-ttu-id="d58d7-372">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-372">Non-Cancelable</span></span>     | <span data-ttu-id="d58d7-373">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-373">Executed after the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d58d7-374">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-374">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="d58d7-375">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-375">Cancelable</span></span>     | <span data-ttu-id="d58d7-376">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-376">Executed before the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d58d7-377">PostCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-377">PostCreatePackingSlipTrigger</span></span>  | <span data-ttu-id="d58d7-378">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-378">Non-Cancelable</span></span>     | <span data-ttu-id="d58d7-379">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-379">Executed after the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|


## <a name="shift-triggers"></a><span data-ttu-id="d58d7-380">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-380">Shift triggers</span></span>
| <span data-ttu-id="d58d7-381">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-381">Trigger</span></span>              | <span data-ttu-id="d58d7-382">型</span><span class="sxs-lookup"><span data-stu-id="d58d7-382">Type</span></span>           | <span data-ttu-id="d58d7-383">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-383">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d58d7-384">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-384">PostOpenShiftTrigger</span></span> | <span data-ttu-id="d58d7-385">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-385">Non-cancelable</span></span> | <span data-ttu-id="d58d7-386">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-386">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="d58d7-387">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-387">Tax override triggers</span></span>

| <span data-ttu-id="d58d7-388">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-388">Trigger</span></span>                           | <span data-ttu-id="d58d7-389">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-389">Type</span></span>           | <span data-ttu-id="d58d7-390">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-390">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="d58d7-391">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-391">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="d58d7-392">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-392">Cancelable</span></span>     | <span data-ttu-id="d58d7-393">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-393">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="d58d7-394">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-394">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="d58d7-395">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-395">Non-cancelable</span></span> | <span data-ttu-id="d58d7-396">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-396">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="d58d7-397">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-397">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="d58d7-398">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-398">Cancelable</span></span>     | <span data-ttu-id="d58d7-399">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-399">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="d58d7-400">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-400">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="d58d7-401">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-401">Non-cancelable</span></span> | <span data-ttu-id="d58d7-402">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-402">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="d58d7-403">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-403">Transaction triggers</span></span>

| <span data-ttu-id="d58d7-404">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-404">Trigger</span></span>                            | <span data-ttu-id="d58d7-405">種類</span><span class="sxs-lookup"><span data-stu-id="d58d7-405">Type</span></span>           | <span data-ttu-id="d58d7-406">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-406">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="d58d7-407">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-407">BeginTransactionTrigger</span></span>            | <span data-ttu-id="d58d7-408">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-408">Non-cancelable</span></span> | <span data-ttu-id="d58d7-409">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-409">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="d58d7-410">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-410">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="d58d7-411">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-411">Cancelable</span></span>     | <span data-ttu-id="d58d7-412">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-412">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="d58d7-413">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-413">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="d58d7-414">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-414">Cancelable</span></span>     | <span data-ttu-id="d58d7-415">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-415">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="d58d7-416">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-416">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="d58d7-417">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-417">Non-cancelable</span></span> | <span data-ttu-id="d58d7-418">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-418">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="d58d7-419">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-419">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="d58d7-420">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-420">Cancelable</span></span>     | <span data-ttu-id="d58d7-421">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-421">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="d58d7-422">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-422">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="d58d7-423">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-423">Non-cancelable</span></span> | <span data-ttu-id="d58d7-424">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-424">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="d58d7-425">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-425">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="d58d7-426">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-426">Cancelable</span></span>     | <span data-ttu-id="d58d7-427">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-427">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="d58d7-428">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-428">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="d58d7-429">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-429">Non-cancelable</span></span> | <span data-ttu-id="d58d7-430">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-430">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="d58d7-431">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-431">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="d58d7-432">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-432">Cancelable</span></span>     | <span data-ttu-id="d58d7-433">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-433">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="d58d7-434">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-434">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="d58d7-435">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-435">Non-cancelable</span></span> | <span data-ttu-id="d58d7-436">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-436">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="d58d7-437">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-437">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d58d7-438">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-438">Cancelable</span></span>     | <span data-ttu-id="d58d7-439">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-439">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="d58d7-440">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-440">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d58d7-441">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-441">Non-cancelable</span></span> | <span data-ttu-id="d58d7-442">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-442">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="d58d7-443">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-443">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="d58d7-444">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-444">Non-cancelable</span></span> | <span data-ttu-id="d58d7-445">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-445">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="d58d7-446">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-446">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d58d7-447">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-447">Cancelable</span></span>     | <span data-ttu-id="d58d7-448">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-448">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="d58d7-449">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d58d7-449">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d58d7-450">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d58d7-450">Non-Cancelable</span></span> | <span data-ttu-id="d58d7-451">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-451">Executed after the customer order is recalled.</span></span>        |

## <a name="reason-code-triggers"></a><span data-ttu-id="d58d7-452">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-452">Reason code triggers</span></span>
| <span data-ttu-id="d58d7-453">トリガー</span><span class="sxs-lookup"><span data-stu-id="d58d7-453">Trigger</span></span>              | <span data-ttu-id="d58d7-454">型</span><span class="sxs-lookup"><span data-stu-id="d58d7-454">Type</span></span>           | <span data-ttu-id="d58d7-455">説明</span><span class="sxs-lookup"><span data-stu-id="d58d7-455">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d58d7-456">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="d58d7-456">PostGetReasonCodeLine</span></span> | <span data-ttu-id="d58d7-457">解約可能</span><span class="sxs-lookup"><span data-stu-id="d58d7-457">Cancelable</span></span> | <span data-ttu-id="d58d7-458">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-458">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |


## <a name="business-scenario"></a><span data-ttu-id="d58d7-459">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="d58d7-459">Business scenario</span></span>
<span data-ttu-id="d58d7-460">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-460">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="d58d7-461">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-461">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="d58d7-462">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d58d7-462">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="d58d7-463">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-463">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="d58d7-464">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-464">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="d58d7-465">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="d58d7-465">Implement a trigger</span></span>

1. <span data-ttu-id="d58d7-466">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-466">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="d58d7-467">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-467">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="d58d7-468">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-468">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d58d7-469">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-469">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="d58d7-470">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-470">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="d58d7-471">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-471">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="d58d7-472">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-472">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="d58d7-473">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-473">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="d58d7-474">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d58d7-474">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="d58d7-475">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-475">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="d58d7-476">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-476">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="d58d7-477">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-477">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="d58d7-478">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-478">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="d58d7-479">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-479">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="d58d7-480">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d58d7-480">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="d58d7-481">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d58d7-481">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="d58d7-482">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-482">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="d58d7-483">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="d58d7-483">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="d58d7-484">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-484">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="d58d7-485">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-485">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="d58d7-486">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-486">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="d58d7-487">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-487">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="d58d7-488">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-488">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d58d7-489">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-489">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="d58d7-490">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-490">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="d58d7-491">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-491">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="d58d7-492">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-492">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="d58d7-493">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-493">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="d58d7-494">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="d58d7-494">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="d58d7-495">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d58d7-495">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="d58d7-496">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="d58d7-496">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d58d7-497">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d58d7-497">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="d58d7-498">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="d58d7-498">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="d58d7-499">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-499">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="d58d7-500">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-500">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="d58d7-501">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-501">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="d58d7-502">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d58d7-502">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="d58d7-503">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-503">Compile and build the project.</span></span>
12. <span data-ttu-id="d58d7-504">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-504">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="d58d7-505">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-505">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="d58d7-506">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-506">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="d58d7-507">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-507">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="d58d7-508">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-508">Save and close the file.</span></span>
17. <span data-ttu-id="d58d7-509">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="d58d7-509">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="d58d7-510">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="d58d7-510">Add the custom receipt layout</span></span>

1. <span data-ttu-id="d58d7-511">Dynamics 365 Retail を開きます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-511">Open Dynamics 365 Retail.</span></span>
2. <span data-ttu-id="d58d7-512">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-512">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="d58d7-513">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-513">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="d58d7-514">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-514">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="d58d7-515">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-515">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="d58d7-516">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-516">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="d58d7-517">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="d58d7-517">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="d58d7-518">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-518">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="d58d7-519">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-519">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="d58d7-520">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-520">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="d58d7-521">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-521">Click **Save**.</span></span>
9. <span data-ttu-id="d58d7-522">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-522">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="d58d7-523">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-523">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="d58d7-524">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-524">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="d58d7-525">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-525">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="d58d7-526">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-526">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="d58d7-527">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-527">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d58d7-528">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-528">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="d58d7-529">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d58d7-529">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="d58d7-530">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-530">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="d58d7-531">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-531">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="d58d7-532">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-532">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="d58d7-533">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-533">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="d58d7-534">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-534">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="d58d7-535">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-535">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="d58d7-536">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-536">Click **Save**.</span></span>
6. <span data-ttu-id="d58d7-537">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-537">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="d58d7-538">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-538">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d58d7-539">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-539">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="d58d7-540">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="d58d7-540">Validate the extension</span></span>

1. <span data-ttu-id="d58d7-541">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="d58d7-541">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="d58d7-542">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-542">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="d58d7-543">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="d58d7-543">Suspend the transaction.</span></span>
4. <span data-ttu-id="d58d7-544">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d58d7-544">The custom receipt should print.</span></span>
