---
title: Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、任意の Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: af42ef0480d5a5c61cb69841dc161cabe0a06caa
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004654"
---
# <a name="modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="6e0f5-103">Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="6e0f5-103">Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e0f5-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="6e0f5-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="6e0f5-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="6e0f5-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="6e0f5-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-108">Continue or cancel an operation.</span></span> <span data-ttu-id="6e0f5-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="6e0f5-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="6e0f5-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="6e0f5-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-112">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="6e0f5-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-113">Application triggers</span></span>

| <span data-ttu-id="6e0f5-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-114">Trigger</span></span>                   | <span data-ttu-id="6e0f5-115">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-115">Type</span></span>           | <span data-ttu-id="6e0f5-116">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="6e0f5-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="6e0f5-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-118">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-119">Executed after the POS application is started.</span></span> <span data-ttu-id="6e0f5-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="6e0f5-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="6e0f5-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-122">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="6e0f5-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="6e0f5-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-125">Cancelable</span></span>     | <span data-ttu-id="6e0f5-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="6e0f5-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="6e0f5-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-128">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="6e0f5-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="6e0f5-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-131">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="6e0f5-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="6e0f5-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-134">Cancelable</span></span>     | <span data-ttu-id="6e0f5-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="6e0f5-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="6e0f5-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-137">Non-Cancelable</span></span> | <span data-ttu-id="6e0f5-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="6e0f5-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="6e0f5-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-140">Cancelable</span></span>     | <span data-ttu-id="6e0f5-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="6e0f5-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="6e0f5-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-143">Non-Cancelable</span></span> | <span data-ttu-id="6e0f5-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="6e0f5-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="6e0f5-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-146">Cancelable</span></span> | <span data-ttu-id="6e0f5-147">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-147">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="6e0f5-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="6e0f5-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-149">Cancelable</span></span> | <span data-ttu-id="6e0f5-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="6e0f5-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="6e0f5-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-152">Non-Cancelable</span></span> | <span data-ttu-id="6e0f5-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-153">Executed after the audit event.</span></span>   | 
| <span data-ttu-id="6e0f5-154">PreOpenUrlTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-154">PreOpenUrlTrigger</span></span>      | <span data-ttu-id="6e0f5-155">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-155">Cancelable</span></span> | <span data-ttu-id="6e0f5-156">URLを開く操作の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-156">Executed before the open URL operation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="6e0f5-157">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-157">Cash management triggers</span></span>

| <span data-ttu-id="6e0f5-158">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-158">Trigger</span></span>                      | <span data-ttu-id="6e0f5-159">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-159">Type</span></span>           | <span data-ttu-id="6e0f5-160">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-160">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="6e0f5-161">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-161">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="6e0f5-162">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-162">Cancelable</span></span>     | <span data-ttu-id="6e0f5-163">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-163">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="6e0f5-164">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-164">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="6e0f5-165">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-165">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-166">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-166">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="6e0f5-167">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-167">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="6e0f5-168">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-168">Cancelable</span></span>     | <span data-ttu-id="6e0f5-169">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-169">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="6e0f5-170">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-170">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="6e0f5-171">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-171">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-172">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-172">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="6e0f5-173">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-173">Customer triggers</span></span>

| <span data-ttu-id="6e0f5-174">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-174">Trigger</span></span>                   | <span data-ttu-id="6e0f5-175">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-175">Type</span></span>                    | <span data-ttu-id="6e0f5-176">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-176">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6e0f5-177">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-177">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="6e0f5-178">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-178">Cancelable</span></span>              | <span data-ttu-id="6e0f5-179">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-179">Executed before adding a customer to the transaction.</span></span>             |
| <span data-ttu-id="6e0f5-180">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-180">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="6e0f5-181">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-181">Non-cancelable</span></span>          | <span data-ttu-id="6e0f5-182">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-182">Executed after adding a customer to the transaction.</span></span>              |
| <span data-ttu-id="6e0f5-183">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-183">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="6e0f5-184">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-184">Cancelable</span></span>              | <span data-ttu-id="6e0f5-185">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-185">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="6e0f5-186">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-186">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="6e0f5-187">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-187">Non-cancelable</span></span>          | <span data-ttu-id="6e0f5-188">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-188">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="6e0f5-189">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-189">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="6e0f5-190">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-190">Cancelable</span></span>              | <span data-ttu-id="6e0f5-191">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-191">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="6e0f5-192">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-192">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="6e0f5-193">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-193">Cancelable</span></span>              | <span data-ttu-id="6e0f5-194">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-194">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="6e0f5-195">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-195">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="6e0f5-196">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-196">Non-cancelable</span></span>          | <span data-ttu-id="6e0f5-197">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-197">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="6e0f5-198">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-198">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="6e0f5-199">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-199">Non-cancelable</span></span>          | <span data-ttu-id="6e0f5-200">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-200">Executed after the loyalty card is issued.</span></span>       |
| <span data-ttu-id="6e0f5-201">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-201">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="6e0f5-202">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-202">Cancelable</span></span>          | <span data-ttu-id="6e0f5-203">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-203">Executed before the customer is created.</span></span>       |
| <span data-ttu-id="6e0f5-204">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-204">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="6e0f5-205">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-205">Non-cancelable</span></span>          | <span data-ttu-id="6e0f5-206">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-206">Executed after the customer is created.</span></span>       |
| <span data-ttu-id="6e0f5-207">PreSaveCustomerAddressTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-207">PreSaveCustomerAddressTrigger</span></span>      | <span data-ttu-id="6e0f5-208">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-208">Cancelable</span></span>              | <span data-ttu-id="6e0f5-209">顧客の住所が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-209">Executed before the customer address is saved.</span></span>            |
| <span data-ttu-id="6e0f5-210">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-210">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="6e0f5-211">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-211">Cancelable</span></span>          | <span data-ttu-id="6e0f5-212">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-212">Executed before getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="6e0f5-213">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-213">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="6e0f5-214">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-214">Non-cancelable</span></span>          | <span data-ttu-id="6e0f5-215">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-215">Executed after getting the loyalty card balance.</span></span>       |
| <span data-ttu-id="6e0f5-216">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-216">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="6e0f5-217">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-217">Cancelable</span></span>          | <span data-ttu-id="6e0f5-218">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-218">Executed before displaying the loyalty card balance.</span></span>       |



## <a name="discount-triggers"></a><span data-ttu-id="6e0f5-219">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-219">Discount triggers</span></span>

| <span data-ttu-id="6e0f5-220">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-220">Trigger</span></span>                         | <span data-ttu-id="6e0f5-221">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-221">Type</span></span>           | <span data-ttu-id="6e0f5-222">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-222">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="6e0f5-223">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-223">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="6e0f5-224">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-224">Cancelable</span></span>     | <span data-ttu-id="6e0f5-225">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-225">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="6e0f5-226">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-226">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="6e0f5-227">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-227">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-228">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-228">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="6e0f5-229">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-229">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="6e0f5-230">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-230">Cancelable</span></span>     | <span data-ttu-id="6e0f5-231">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-231">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="6e0f5-232">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-232">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="6e0f5-233">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-233">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-234">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-234">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="6e0f5-235">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-235">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="6e0f5-236">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-236">Cancelable</span></span>     | <span data-ttu-id="6e0f5-237">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-237">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="6e0f5-238">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-238">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="6e0f5-239">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-239">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-240">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-240">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="6e0f5-241">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-241">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="6e0f5-242">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-242">Cancelable</span></span>     | <span data-ttu-id="6e0f5-243">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-243">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="6e0f5-244">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-244">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="6e0f5-245">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-245">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-246">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-246">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="6e0f5-247">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-247">PreAddCouponTrigger</span></span>             | <span data-ttu-id="6e0f5-248">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-248">Cancelable</span></span>     | <span data-ttu-id="6e0f5-249">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-249">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="6e0f5-250">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-250">PostAddCouponTrigger</span></span>            | <span data-ttu-id="6e0f5-251">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-251">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-252">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-252">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="6e0f5-253">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-253">Operation triggers</span></span>

| <span data-ttu-id="6e0f5-254">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-254">Trigger</span></span>              | <span data-ttu-id="6e0f5-255">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-255">Type</span></span>           | <span data-ttu-id="6e0f5-256">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-256">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="6e0f5-257">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-257">PreOperationTrigger</span></span>  | <span data-ttu-id="6e0f5-258">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-258">Cancelable</span></span>     | <span data-ttu-id="6e0f5-259">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-259">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="6e0f5-260">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-260">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="6e0f5-261">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-261">PreOperationValidationTrigger</span></span> | <span data-ttu-id="6e0f5-262">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-262">Cancelable</span></span> | <span data-ttu-id="6e0f5-263">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-263">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="6e0f5-264">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-264">OperationFailureTrigger</span></span> | <span data-ttu-id="6e0f5-265">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-265">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-266">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-266">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="6e0f5-267">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-267">PostOperationTrigger</span></span> | <span data-ttu-id="6e0f5-268">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-268">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-269">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-269">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="6e0f5-270">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-270">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="6e0f5-271">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-271">Payment triggers</span></span>

| <span data-ttu-id="6e0f5-272">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-272">Trigger</span></span>                 | <span data-ttu-id="6e0f5-273">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-273">Type</span></span>           | <span data-ttu-id="6e0f5-274">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-274">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e0f5-275">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-275">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="6e0f5-276">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-276">Cancelable</span></span>     | <span data-ttu-id="6e0f5-277">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-277">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="6e0f5-278">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-278">PrePaymentTrigger</span></span>       | <span data-ttu-id="6e0f5-279">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-279">Cancelable</span></span>     | <span data-ttu-id="6e0f5-280">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-280">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="6e0f5-281">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-281">PostPaymentTrigger</span></span>      | <span data-ttu-id="6e0f5-282">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-282">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-283">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-283">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="6e0f5-284">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-284">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="6e0f5-285">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-285">Cancelable</span></span>     | <span data-ttu-id="6e0f5-286">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-286">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="6e0f5-287">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-287">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="6e0f5-288">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-288">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-289">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-289">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="6e0f5-290">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-290">Printing Triggers</span></span>

| <span data-ttu-id="6e0f5-291">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-291">Trigger</span></span>                    | <span data-ttu-id="6e0f5-292">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-292">Type</span></span>       | <span data-ttu-id="6e0f5-293">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-293">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="6e0f5-294">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-294">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="6e0f5-295">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-295">Cancelable</span></span> | <span data-ttu-id="6e0f5-296">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-296">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="6e0f5-297">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-297">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="6e0f5-298">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-298">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-299">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-299">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="6e0f5-300">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-300">Product triggers</span></span>

| <span data-ttu-id="6e0f5-301">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-301">Trigger</span></span>                    | <span data-ttu-id="6e0f5-302">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-302">Type</span></span>           | <span data-ttu-id="6e0f5-303">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-303">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0f5-304">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-304">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="6e0f5-305">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-305">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-306">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-306">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="6e0f5-307">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-307">PreProductSaleTrigger</span></span>      | <span data-ttu-id="6e0f5-308">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-308">Cancelable</span></span>     | <span data-ttu-id="6e0f5-309">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-309">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="6e0f5-310">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-310">PostProductSaleTrigger</span></span>     | <span data-ttu-id="6e0f5-311">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-311">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-312">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-312">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="6e0f5-313">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-313">PreReturnProductTrigger</span></span>    | <span data-ttu-id="6e0f5-314">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-314">Cancelable</span></span>     | <span data-ttu-id="6e0f5-315">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-315">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="6e0f5-316">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-316">PostReturnProductTrigger</span></span>   | <span data-ttu-id="6e0f5-317">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-317">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-318">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-318">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="6e0f5-319">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-319">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="6e0f5-320">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-320">Cancelable</span></span>     | <span data-ttu-id="6e0f5-321">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-321">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="6e0f5-322">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-322">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="6e0f5-323">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-323">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-324">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-324">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="6e0f5-325">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-325">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="6e0f5-326">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-326">Cancelable</span></span>     | <span data-ttu-id="6e0f5-327">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-327">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="6e0f5-328">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-328">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="6e0f5-329">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-329">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-330">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-330">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="6e0f5-331">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-331">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="6e0f5-332">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-332">Cancelable</span></span>     | <span data-ttu-id="6e0f5-333">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-333">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="6e0f5-334">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-334">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="6e0f5-335">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-335">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-336">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-336">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="6e0f5-337">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-337">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="6e0f5-338">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-338">Cancelable</span></span>     | <span data-ttu-id="6e0f5-339">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-339">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="6e0f5-340">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-340">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="6e0f5-341">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-341">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-342">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-342">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="6e0f5-343">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-343">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="6e0f5-344">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-344">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-345">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-345">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="6e0f5-346">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-346">Sales order triggers</span></span>

| <span data-ttu-id="6e0f5-347">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-347">Trigger</span></span>                 | <span data-ttu-id="6e0f5-348">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-348">Type</span></span>           | <span data-ttu-id="6e0f5-349">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-349">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e0f5-350">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-350">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="6e0f5-351">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-351">Cancelable</span></span>     | <span data-ttu-id="6e0f5-352">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-352">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="6e0f5-353">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-353">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="6e0f5-354">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-354">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-355">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-355">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="6e0f5-356">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-356">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="6e0f5-357">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-357">Cancelable</span></span>     | <span data-ttu-id="6e0f5-358">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-358">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="6e0f5-359">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-359">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="6e0f5-360">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-360">Cancelable</span></span>     | <span data-ttu-id="6e0f5-361">顧客注文時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-361">Executed before the shipping origin is changed during a customer order.</span></span>|
| <span data-ttu-id="6e0f5-362">PreGetFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-362">PreGetFulfillmentLinesTrigger</span></span>     | <span data-ttu-id="6e0f5-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-363">Cancelable</span></span>     | <span data-ttu-id="6e0f5-364">注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-364">Executed before the Order fulfillment lines are loaded in the Order fulfillment view.</span></span>|
| <span data-ttu-id="6e0f5-365">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-365">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="6e0f5-366">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-366">Cancelable</span></span>     | <span data-ttu-id="6e0f5-367">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-367">Executed before the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="6e0f5-368">PostShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-368">PostShipFulfillmentLinesTrigger</span></span>   | <span data-ttu-id="6e0f5-369">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-369">Non-Cancelable</span></span>     | <span data-ttu-id="6e0f5-370">**出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-370">Executed after the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="6e0f5-371">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-371">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="6e0f5-372">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-372">Cancelable</span></span>     | <span data-ttu-id="6e0f5-373">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-373">Executed before the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="6e0f5-374">PostMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-374">PostMarkFulfillmentLinesAsPackedTrigger</span></span>   | <span data-ttu-id="6e0f5-375">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-375">Non-Cancelable</span></span>     | <span data-ttu-id="6e0f5-376">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-376">Executed after the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="6e0f5-377">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-377">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="6e0f5-378">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-378">Cancelable</span></span>     | <span data-ttu-id="6e0f5-379">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-379">Executed before the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="6e0f5-380">PostCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-380">PostCreatePackingSlipTrigger</span></span>  | <span data-ttu-id="6e0f5-381">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-381">Non-Cancelable</span></span>     | <span data-ttu-id="6e0f5-382">**梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-382">Executed after the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="6e0f5-383">PostReturnInvoicedSalesLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-383">PostReturnInvoicedSalesLinesTrigger</span></span>   | <span data-ttu-id="6e0f5-384">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-384">Non-Cancelable</span></span>     | <span data-ttu-id="6e0f5-385">返品対象として 1 つ以上の請求書が選択された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-385">Executed after one or more invoices selected for return.</span></span>|


## <a name="shift-triggers"></a><span data-ttu-id="6e0f5-386">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-386">Shift triggers</span></span>
| <span data-ttu-id="6e0f5-387">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-387">Trigger</span></span>              | <span data-ttu-id="6e0f5-388">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-388">Type</span></span>           | <span data-ttu-id="6e0f5-389">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-389">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="6e0f5-390">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-390">PostOpenShiftTrigger</span></span> | <span data-ttu-id="6e0f5-391">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-391">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-392">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-392">This trigger is executed after the new shift is opened.</span></span> |
| <span data-ttu-id="6e0f5-393">PreCloseShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-393">PreCloseShiftTrigger</span></span> | <span data-ttu-id="6e0f5-394">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-394">Cancelable</span></span> | <span data-ttu-id="6e0f5-395">このトリガーは、シフトが開かれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-395">This trigger is executed before the shift is closed.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="6e0f5-396">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-396">Tax override triggers</span></span>

| <span data-ttu-id="6e0f5-397">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-397">Trigger</span></span>                           | <span data-ttu-id="6e0f5-398">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-398">Type</span></span>           | <span data-ttu-id="6e0f5-399">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-399">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="6e0f5-400">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-400">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="6e0f5-401">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-401">Cancelable</span></span>     | <span data-ttu-id="6e0f5-402">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-402">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="6e0f5-403">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-403">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="6e0f5-404">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-404">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-405">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-405">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="6e0f5-406">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-406">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="6e0f5-407">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-407">Cancelable</span></span>     | <span data-ttu-id="6e0f5-408">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-408">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="6e0f5-409">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-409">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="6e0f5-410">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-410">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-411">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-411">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="6e0f5-412">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-412">Transaction triggers</span></span>

| <span data-ttu-id="6e0f5-413">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-413">Trigger</span></span>                            | <span data-ttu-id="6e0f5-414">種類</span><span class="sxs-lookup"><span data-stu-id="6e0f5-414">Type</span></span>           | <span data-ttu-id="6e0f5-415">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-415">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="6e0f5-416">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-416">BeginTransactionTrigger</span></span>            | <span data-ttu-id="6e0f5-417">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-417">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-418">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-418">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="6e0f5-419">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-419">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="6e0f5-420">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-420">Cancelable</span></span>     | <span data-ttu-id="6e0f5-421">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-421">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="6e0f5-422">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-422">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="6e0f5-423">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-423">Cancelable</span></span>     | <span data-ttu-id="6e0f5-424">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-424">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="6e0f5-425">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-425">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="6e0f5-426">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-426">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-427">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-427">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="6e0f5-428">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-428">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="6e0f5-429">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-429">Cancelable</span></span>     | <span data-ttu-id="6e0f5-430">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-430">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="6e0f5-431">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-431">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="6e0f5-432">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-432">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-433">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-433">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="6e0f5-434">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-434">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="6e0f5-435">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-435">Cancelable</span></span>     | <span data-ttu-id="6e0f5-436">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-436">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="6e0f5-437">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-437">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="6e0f5-438">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-438">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-439">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-439">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="6e0f5-440">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-440">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="6e0f5-441">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-441">Cancelable</span></span>     | <span data-ttu-id="6e0f5-442">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-442">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="6e0f5-443">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-443">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="6e0f5-444">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-444">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-445">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-445">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="6e0f5-446">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-446">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="6e0f5-447">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-447">Cancelable</span></span>     | <span data-ttu-id="6e0f5-448">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-448">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="6e0f5-449">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-449">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="6e0f5-450">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-450">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-451">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-451">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="6e0f5-452">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-452">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="6e0f5-453">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-453">Non-cancelable</span></span> | <span data-ttu-id="6e0f5-454">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-454">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="6e0f5-455">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-455">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="6e0f5-456">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-456">Cancelable</span></span>     | <span data-ttu-id="6e0f5-457">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-457">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="6e0f5-458">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-458">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="6e0f5-459">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="6e0f5-459">Non-Cancelable</span></span> | <span data-ttu-id="6e0f5-460">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-460">Executed after the customer order is recalled.</span></span>        |
| <span data-ttu-id="6e0f5-461">PreSelectTransactionPaymentMethodTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-461">PreSelectTransactionPaymentMethodTrigger</span></span>       | <span data-ttu-id="6e0f5-462">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-462">Cancelable</span></span> |  <span data-ttu-id="6e0f5-463">ユーザーが**カート ビュー - 合計**パネルで**合計**を選択すると、使用可能な支払方法が表示され、このトリガーはこのダイアログが表示される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-463">When the user selects the **Totals** button in the **Cart view - totals** panel, the available payment methods are shown and this trigger will get executed before this dialog is shown.</span></span> <span data-ttu-id="6e0f5-464">このトリガーから利用可能な支払方法を変更するための拡張コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-464">You can us extension code to modify the available payment methods from this trigger.</span></span>      |

## <a name="reason-code-triggers"></a><span data-ttu-id="6e0f5-465">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-465">Reason code triggers</span></span>
| <span data-ttu-id="6e0f5-466">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-466">Trigger</span></span>              | <span data-ttu-id="6e0f5-467">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-467">Type</span></span>           | <span data-ttu-id="6e0f5-468">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-468">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="6e0f5-469">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="6e0f5-469">PostGetReasonCodeLine</span></span> | <span data-ttu-id="6e0f5-470">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-470">Cancelable</span></span> | <span data-ttu-id="6e0f5-471">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-471">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |

## <a name="transfer-order-triggers"></a><span data-ttu-id="6e0f5-472">移動オーダー トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-472">Transfer Order triggers</span></span>
| <span data-ttu-id="6e0f5-473">トリガー</span><span class="sxs-lookup"><span data-stu-id="6e0f5-473">Trigger</span></span>              | <span data-ttu-id="6e0f5-474">型</span><span class="sxs-lookup"><span data-stu-id="6e0f5-474">Type</span></span>           | <span data-ttu-id="6e0f5-475">説明</span><span class="sxs-lookup"><span data-stu-id="6e0f5-475">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="6e0f5-476">PreCreateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-476">PreCreateTransferOrderTrigger</span></span> | <span data-ttu-id="6e0f5-477">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-477">Cancelable</span></span> | <span data-ttu-id="6e0f5-478">このトリガーは、移動オーダーが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-478">This trigger is executed before the transfer order is created (executed after the order input).</span></span> |
| <span data-ttu-id="6e0f5-479">PreUpdateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="6e0f5-479">PreUpdateTransferOrderTrigger</span></span> | <span data-ttu-id="6e0f5-480">解約可能</span><span class="sxs-lookup"><span data-stu-id="6e0f5-480">Cancelable</span></span> | <span data-ttu-id="6e0f5-481">このトリガーは、移動オーダーが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-481">This trigger is executed before the transfer order is updated.</span></span> |


## <a name="business-scenario"></a><span data-ttu-id="6e0f5-482">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="6e0f5-482">Business scenario</span></span>
<span data-ttu-id="6e0f5-483">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-483">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="6e0f5-484">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-484">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="6e0f5-485">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-485">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="6e0f5-486">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-486">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="6e0f5-487">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-487">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="6e0f5-488">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="6e0f5-488">Implement a trigger</span></span>

1. <span data-ttu-id="6e0f5-489">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-489">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="6e0f5-490">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-490">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="6e0f5-491">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-491">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="6e0f5-492">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-492">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="6e0f5-493">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-493">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="6e0f5-494">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-494">Add the following **import** statements to import the relevant entities and context.</span></span>

   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
   
7. <span data-ttu-id="6e0f5-495">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-495">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
    ```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
    ```
8. <span data-ttu-id="6e0f5-496">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-496">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
   
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
   
   <span data-ttu-id="6e0f5-497">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-497">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="6e0f5-498">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-498">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="6e0f5-499">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-499">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="6e0f5-500">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-500">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="6e0f5-501">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-501">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="6e0f5-502">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-502">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="6e0f5-503">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-503">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="6e0f5-504">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-504">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="6e0f5-505">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-505">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="6e0f5-506">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="6e0f5-506">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="6e0f5-507">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-507">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="6e0f5-508">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-508">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="6e0f5-509">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-509">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="6e0f5-510">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-510">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="6e0f5-511">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-511">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="6e0f5-512">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-512">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="6e0f5-513">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-513">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="6e0f5-514">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-514">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="6e0f5-515">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-515">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="6e0f5-516">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-516">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="6e0f5-517">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点ではコマース トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-517">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the commerce transaction table.</span></span> <span data-ttu-id="6e0f5-518">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-518">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="6e0f5-519">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-519">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e0f5-520">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-520">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="6e0f5-521">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-521">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="6e0f5-522">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-522">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="6e0f5-523">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-523">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="6e0f5-524">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-524">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="6e0f5-525">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-525">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="6e0f5-526">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-526">Compile and build the project.</span></span>
12. <span data-ttu-id="6e0f5-527">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-527">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="6e0f5-528">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-528">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="6e0f5-529">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-529">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="6e0f5-530">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-530">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="6e0f5-531">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-531">Save and close the file.</span></span>
17. <span data-ttu-id="6e0f5-532">Commerce Scale Unit を再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-532">Restart the Commerce Scale Unit to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="6e0f5-533">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="6e0f5-533">Add the custom receipt layout</span></span>

1. <span data-ttu-id="6e0f5-534">Dynamics 365 Commerce を開きます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-534">Open Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="6e0f5-535">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-535">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="6e0f5-536">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-536">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="6e0f5-537">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-537">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="6e0f5-538">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-538">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="6e0f5-539">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-539">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="6e0f5-540">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-540">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="6e0f5-541">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-541">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="6e0f5-542">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-542">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="6e0f5-543">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-543">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="6e0f5-544">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-544">Click **Save**.</span></span>
9. <span data-ttu-id="6e0f5-545">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **視覚プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-545">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="6e0f5-546">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-546">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="6e0f5-547">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-547">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="6e0f5-548">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-548">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="6e0f5-549">**Retail とコマース > Retail とコマース IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-549">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="6e0f5-550">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-550">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="6e0f5-551">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-551">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="6e0f5-552">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e0f5-552">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="6e0f5-553">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-553">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="6e0f5-554">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-554">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="6e0f5-555">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-555">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="6e0f5-556">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-556">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="6e0f5-557">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-557">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="6e0f5-558">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-558">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="6e0f5-559">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-559">Click **Save**.</span></span>
6. <span data-ttu-id="6e0f5-560">**Retail とコマース** > **Retail とコマース IT** > **配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-560">Go to **Retail and Commerce** > **Retail and Commerce IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="6e0f5-561">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-561">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="6e0f5-562">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-562">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="6e0f5-563">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="6e0f5-563">Validate the extension</span></span>

1. <span data-ttu-id="6e0f5-564">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-564">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="6e0f5-565">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-565">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="6e0f5-566">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-566">Suspend the transaction.</span></span>
4. <span data-ttu-id="6e0f5-567">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="6e0f5-567">The custom receipt should print.</span></span>
