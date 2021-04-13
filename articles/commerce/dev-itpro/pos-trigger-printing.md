---
title: Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、任意の Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: 6e7ba56b295c41fe7e28f74c95f50275008ce9da
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794337"
---
# <a name="pos-triggers"></a><span data-ttu-id="d6f73-103">POS トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-103">POS triggers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6f73-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="d6f73-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="d6f73-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="d6f73-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="d6f73-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-108">Continue or cancel an operation.</span></span> <span data-ttu-id="d6f73-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="d6f73-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="d6f73-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="d6f73-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 


<span data-ttu-id="d6f73-112">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="d6f73-112">The following table lists the available triggers and denotes whether they can be canceled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="d6f73-113">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-113">Application triggers</span></span>

| <span data-ttu-id="d6f73-114">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-114">Trigger</span></span>                   | <span data-ttu-id="d6f73-115">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-115">Type</span></span>           | <span data-ttu-id="d6f73-116">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-116">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="d6f73-117">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-117">ApplicationStartTrigger</span></span>   | <span data-ttu-id="d6f73-118">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-118">Non-cancelable</span></span> | <span data-ttu-id="d6f73-119">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-119">Executed after the POS application is started.</span></span> <span data-ttu-id="d6f73-120">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-120">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="d6f73-121">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-121">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="d6f73-122">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-122">Non-cancelable</span></span> | <span data-ttu-id="d6f73-123">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-123">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="d6f73-124">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-124">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="d6f73-125">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-125">Cancelable</span></span>     | <span data-ttu-id="d6f73-126">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-126">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="d6f73-127">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-127">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="d6f73-128">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-128">Non-cancelable</span></span> | <span data-ttu-id="d6f73-129">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-129">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="d6f73-130">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-130">PostLogOffTrigger</span></span>         | <span data-ttu-id="d6f73-131">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-131">Non-cancelable</span></span> | <span data-ttu-id="d6f73-132">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-132">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="d6f73-133">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-133">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="d6f73-134">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-134">Cancelable</span></span>     | <span data-ttu-id="d6f73-135">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-135">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="d6f73-136">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-136">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="d6f73-137">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-137">Non-Cancelable</span></span> | <span data-ttu-id="d6f73-138">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-138">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="d6f73-139">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-139">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="d6f73-140">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-140">Cancelable</span></span>     | <span data-ttu-id="d6f73-141">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-141">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="d6f73-142">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-142">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="d6f73-143">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-143">Non-Cancelable</span></span> | <span data-ttu-id="d6f73-144">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-144">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="d6f73-145">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-145">PreElevateUserTrigger</span></span>      | <span data-ttu-id="d6f73-146">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-146">Cancelable</span></span> | <span data-ttu-id="d6f73-147">マネージャーのオーバーライド前に実行されるこのトリガーは、Microsoft Azure Active Directory (Azure AD) 以外のユーザー認証に対してのみ機能します。Azure AD が有効になっている場合、このトリガーは機能しません。</span><span class="sxs-lookup"><span data-stu-id="d6f73-147">Executed before the manager override, this trigger will only work for non Microsoft Azure Active Directory (Azure AD) user authentication, if Azure AD is enabled this trigger will not work.</span></span>   | 
| <span data-ttu-id="d6f73-148">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-148">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="d6f73-149">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-149">Cancelable</span></span> | <span data-ttu-id="d6f73-150">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-150">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="d6f73-151">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-151">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="d6f73-152">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-152">Non-Cancelable</span></span> | <span data-ttu-id="d6f73-153">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-153">Executed after the audit event.</span></span>   | 
| <span data-ttu-id="d6f73-154">PreOpenUrlTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-154">PreOpenUrlTrigger</span></span>      | <span data-ttu-id="d6f73-155">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-155">Cancelable</span></span> | <span data-ttu-id="d6f73-156">URLを開く操作の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-156">Executed before the open URL operation.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="d6f73-157">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-157">Cash management triggers</span></span>

| <span data-ttu-id="d6f73-158">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-158">Trigger</span></span>                      | <span data-ttu-id="d6f73-159">型</span><span class="sxs-lookup"><span data-stu-id="d6f73-159">Type</span></span>           | <span data-ttu-id="d6f73-160">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-160">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="d6f73-161">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-161">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="d6f73-162">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-162">Cancelable</span></span>     | <span data-ttu-id="d6f73-163">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-163">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="d6f73-164">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-164">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="d6f73-165">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-165">Non-cancelable</span></span> | <span data-ttu-id="d6f73-166">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-166">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="d6f73-167">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-167">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="d6f73-168">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-168">Cancelable</span></span>     | <span data-ttu-id="d6f73-169">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-169">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="d6f73-170">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-170">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="d6f73-171">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-171">Non-cancelable</span></span> | <span data-ttu-id="d6f73-172">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-172">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="d6f73-173">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-173">Customer triggers</span></span>

| <span data-ttu-id="d6f73-174">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-174">Trigger</span></span>                   | <span data-ttu-id="d6f73-175">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-175">Type</span></span>                    | <span data-ttu-id="d6f73-176">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-176">Description</span></span>                                                        |<span data-ttu-id="d6f73-177">リリース</span><span class="sxs-lookup"><span data-stu-id="d6f73-177">Release</span></span>    |
|---------------------------|-------------------------|--------------------------------------------------------------------|-----------|
| <span data-ttu-id="d6f73-178">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-178">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="d6f73-179">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-179">Cancelable</span></span>              | <span data-ttu-id="d6f73-180">トランザクションに顧客を追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-180">Executed before adding a customer to the transaction.</span></span>             |  |
| <span data-ttu-id="d6f73-181">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-181">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="d6f73-182">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-182">Non-cancelable</span></span>          | <span data-ttu-id="d6f73-183">トランザクションに顧客を追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-183">Executed after adding a customer to the transaction.</span></span>              |  |
| <span data-ttu-id="d6f73-184">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-184">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="d6f73-185">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-185">Cancelable</span></span>              | <span data-ttu-id="d6f73-186">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-186">Executed before the customer cleared from the cart.</span></span> |    |
| <span data-ttu-id="d6f73-187">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-187">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="d6f73-188">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-188">Non-cancelable</span></span>          | <span data-ttu-id="d6f73-189">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-189">Executed after the customer cleared from the cart.</span></span> |     |
| <span data-ttu-id="d6f73-190">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-190">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="d6f73-191">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-191">Cancelable</span></span>              | <span data-ttu-id="d6f73-192">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-192">Executed before the customer is added to the cart.</span></span>            |  |
| <span data-ttu-id="d6f73-193">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-193">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="d6f73-194">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-194">Cancelable</span></span>              | <span data-ttu-id="d6f73-195">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-195">Executed before customer search is performed.</span></span>      |     |
| <span data-ttu-id="d6f73-196">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-196">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="d6f73-197">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-197">Non-cancelable</span></span>          | <span data-ttu-id="d6f73-198">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-198">Executed after customer search is performed.</span></span>       |     |
| <span data-ttu-id="d6f73-199">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-199">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="d6f73-200">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-200">Non-cancelable</span></span>          | <span data-ttu-id="d6f73-201">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-201">Executed after the loyalty card is issued.</span></span>       |    |
| <span data-ttu-id="d6f73-202">PreCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-202">PreCustomerSaveTrigger</span></span>  | <span data-ttu-id="d6f73-203">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-203">Cancelable</span></span>          | <span data-ttu-id="d6f73-204">顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-204">Executed before the customer is created.</span></span>       |   |
| <span data-ttu-id="d6f73-205">PostCustomerSaveTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-205">PostCustomerSaveTrigger</span></span>  | <span data-ttu-id="d6f73-206">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-206">Non-cancelable</span></span>          | <span data-ttu-id="d6f73-207">顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-207">Executed after the customer is created.</span></span>       |   |
| <span data-ttu-id="d6f73-208">PreSaveCustomerAddressTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-208">PreSaveCustomerAddressTrigger</span></span>      | <span data-ttu-id="d6f73-209">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-209">Cancelable</span></span>              | <span data-ttu-id="d6f73-210">顧客の住所が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-210">Executed before the customer address is saved.</span></span>            |     |
| <span data-ttu-id="d6f73-211">PreGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-211">PreGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d6f73-212">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-212">Cancelable</span></span>          | <span data-ttu-id="d6f73-213">ロイヤルティ カード残高を取得する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-213">Executed before getting the loyalty card balance.</span></span>       |     |
| <span data-ttu-id="d6f73-214">PostGetLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-214">PostGetLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d6f73-215">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-215">Non-cancelable</span></span>          | <span data-ttu-id="d6f73-216">ロイヤルティ カード残高を取得した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-216">Executed after getting the loyalty card balance.</span></span>       |     |
| <span data-ttu-id="d6f73-217">PreDisplayLoyaltyCardBalanceTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-217">PreDisplayLoyaltyCardBalanceTrigger</span></span>  | <span data-ttu-id="d6f73-218">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-218">Cancelable</span></span>          | <span data-ttu-id="d6f73-219">ロイヤルティ カード残高を表示する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-219">Executed before displaying the loyalty card balance.</span></span>       |  |
| <span data-ttu-id="d6f73-220">PreCustomerEditTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-220">PreCustomerEditTrigger</span></span>  | <span data-ttu-id="d6f73-221">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-221">Cancelable</span></span>          | <span data-ttu-id="d6f73-222">顧客を編集する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-222">Executed before editing the Customer.</span></span>       | <span data-ttu-id="d6f73-223">10.0.19</span><span class="sxs-lookup"><span data-stu-id="d6f73-223">10.0.19</span></span> |



## <a name="discount-triggers"></a><span data-ttu-id="d6f73-224">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-224">Discount triggers</span></span>

| <span data-ttu-id="d6f73-225">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-225">Trigger</span></span>                         | <span data-ttu-id="d6f73-226">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-226">Type</span></span>           | <span data-ttu-id="d6f73-227">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-227">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d6f73-228">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-228">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="d6f73-229">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-229">Cancelable</span></span>     | <span data-ttu-id="d6f73-230">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-230">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="d6f73-231">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-231">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="d6f73-232">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-232">Non-cancelable</span></span> | <span data-ttu-id="d6f73-233">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-233">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="d6f73-234">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-234">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="d6f73-235">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-235">Cancelable</span></span>     | <span data-ttu-id="d6f73-236">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-236">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="d6f73-237">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-237">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="d6f73-238">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-238">Non-cancelable</span></span> | <span data-ttu-id="d6f73-239">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-239">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="d6f73-240">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-240">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="d6f73-241">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-241">Cancelable</span></span>     | <span data-ttu-id="d6f73-242">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-242">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d6f73-243">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-243">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="d6f73-244">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-244">Non-cancelable</span></span> | <span data-ttu-id="d6f73-245">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-245">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="d6f73-246">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-246">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="d6f73-247">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-247">Cancelable</span></span>     | <span data-ttu-id="d6f73-248">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-248">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="d6f73-249">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-249">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="d6f73-250">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-250">Non-cancelable</span></span> | <span data-ttu-id="d6f73-251">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-251">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="d6f73-252">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-252">PreAddCouponTrigger</span></span>             | <span data-ttu-id="d6f73-253">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-253">Cancelable</span></span>     | <span data-ttu-id="d6f73-254">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-254">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="d6f73-255">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-255">PostAddCouponTrigger</span></span>            | <span data-ttu-id="d6f73-256">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-256">Non-cancelable</span></span> | <span data-ttu-id="d6f73-257">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-257">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="d6f73-258">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-258">Operation triggers</span></span>

| <span data-ttu-id="d6f73-259">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-259">Trigger</span></span>              | <span data-ttu-id="d6f73-260">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-260">Type</span></span>           | <span data-ttu-id="d6f73-261">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-261">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="d6f73-262">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-262">PreOperationTrigger</span></span>  | <span data-ttu-id="d6f73-263">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-263">Cancelable</span></span>     | <span data-ttu-id="d6f73-264">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d6f73-264">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="d6f73-265">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-265">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="d6f73-266">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-266">PreOperationValidationTrigger</span></span> | <span data-ttu-id="d6f73-267">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-267">Cancelable</span></span> | <span data-ttu-id="d6f73-268">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d6f73-268">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="d6f73-269">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-269">OperationFailureTrigger</span></span> | <span data-ttu-id="d6f73-270">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-270">Non-cancelable</span></span> | <span data-ttu-id="d6f73-271">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d6f73-271">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="d6f73-272">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-272">PostOperationTrigger</span></span> | <span data-ttu-id="d6f73-273">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-273">Non-cancelable</span></span> | <span data-ttu-id="d6f73-274">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="d6f73-274">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="d6f73-275">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-275">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="d6f73-276">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-276">Payment triggers</span></span>

| <span data-ttu-id="d6f73-277">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-277">Trigger</span></span>                 | <span data-ttu-id="d6f73-278">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-278">Type</span></span>           | <span data-ttu-id="d6f73-279">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-279">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d6f73-280">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-280">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="d6f73-281">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-281">Cancelable</span></span>     | <span data-ttu-id="d6f73-282">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-282">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="d6f73-283">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-283">PrePaymentTrigger</span></span>       | <span data-ttu-id="d6f73-284">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-284">Cancelable</span></span>     | <span data-ttu-id="d6f73-285">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-285">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="d6f73-286">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-286">PostPaymentTrigger</span></span>      | <span data-ttu-id="d6f73-287">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-287">Non-cancelable</span></span> | <span data-ttu-id="d6f73-288">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-288">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="d6f73-289">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-289">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="d6f73-290">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-290">Cancelable</span></span>     | <span data-ttu-id="d6f73-291">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-291">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="d6f73-292">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-292">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="d6f73-293">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-293">Non-cancelable</span></span> | <span data-ttu-id="d6f73-294">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-294">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="d6f73-295">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-295">Printing Triggers</span></span>

| <span data-ttu-id="d6f73-296">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-296">Trigger</span></span>                    | <span data-ttu-id="d6f73-297">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-297">Type</span></span>       | <span data-ttu-id="d6f73-298">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-298">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="d6f73-299">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-299">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="d6f73-300">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-300">Cancelable</span></span> | <span data-ttu-id="d6f73-301">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-301">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="d6f73-302">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-302">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="d6f73-303">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-303">Non-cancelable</span></span> | <span data-ttu-id="d6f73-304">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-304">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="d6f73-305">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-305">Product triggers</span></span>

| <span data-ttu-id="d6f73-306">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-306">Trigger</span></span>                    | <span data-ttu-id="d6f73-307">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-307">Type</span></span>           | <span data-ttu-id="d6f73-308">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-308">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f73-309">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-309">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="d6f73-310">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-310">Non-cancelable</span></span> | <span data-ttu-id="d6f73-311">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-311">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="d6f73-312">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-312">PreProductSaleTrigger</span></span>      | <span data-ttu-id="d6f73-313">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-313">Cancelable</span></span>     | <span data-ttu-id="d6f73-314">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-314">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="d6f73-315">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-315">PostProductSaleTrigger</span></span>     | <span data-ttu-id="d6f73-316">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-316">Non-cancelable</span></span> | <span data-ttu-id="d6f73-317">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-317">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="d6f73-318">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-318">PreReturnProductTrigger</span></span>    | <span data-ttu-id="d6f73-319">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-319">Cancelable</span></span>     | <span data-ttu-id="d6f73-320">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-320">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="d6f73-321">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-321">PostReturnProductTrigger</span></span>   | <span data-ttu-id="d6f73-322">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-322">Non-cancelable</span></span> | <span data-ttu-id="d6f73-323">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-323">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="d6f73-324">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-324">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="d6f73-325">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-325">Cancelable</span></span>     | <span data-ttu-id="d6f73-326">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-326">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="d6f73-327">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-327">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="d6f73-328">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-328">Non-cancelable</span></span> | <span data-ttu-id="d6f73-329">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-329">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="d6f73-330">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-330">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="d6f73-331">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-331">Cancelable</span></span>     | <span data-ttu-id="d6f73-332">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-332">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="d6f73-333">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-333">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="d6f73-334">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-334">Non-cancelable</span></span> | <span data-ttu-id="d6f73-335">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-335">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="d6f73-336">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-336">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="d6f73-337">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-337">Cancelable</span></span>     | <span data-ttu-id="d6f73-338">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-338">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="d6f73-339">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-339">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="d6f73-340">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-340">Non-cancelable</span></span> | <span data-ttu-id="d6f73-341">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-341">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="d6f73-342">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-342">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="d6f73-343">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-343">Cancelable</span></span>     | <span data-ttu-id="d6f73-344">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-344">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="d6f73-345">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-345">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="d6f73-346">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-346">Non-cancelable</span></span> | <span data-ttu-id="d6f73-347">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-347">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="d6f73-348">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-348">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="d6f73-349">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-349">Non-cancelable</span></span> | <span data-ttu-id="d6f73-350">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-350">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="d6f73-351">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-351">Sales order triggers</span></span>

| <span data-ttu-id="d6f73-352">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-352">Trigger</span></span>                 | <span data-ttu-id="d6f73-353">型</span><span class="sxs-lookup"><span data-stu-id="d6f73-353">Type</span></span>           | <span data-ttu-id="d6f73-354">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-354">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d6f73-355">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-355">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="d6f73-356">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-356">Cancelable</span></span>     | <span data-ttu-id="d6f73-357">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-357">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="d6f73-358">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-358">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="d6f73-359">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-359">Non-cancelable</span></span> | <span data-ttu-id="d6f73-360">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-360">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="d6f73-361">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-361">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="d6f73-362">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-362">Cancelable</span></span>     | <span data-ttu-id="d6f73-363">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-363">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="d6f73-364">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-364">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="d6f73-365">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-365">Cancelable</span></span>     | <span data-ttu-id="d6f73-366">顧客注文時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-366">Executed before the shipping origin is changed during a customer order.</span></span>|
| <span data-ttu-id="d6f73-367">PreGetFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-367">PreGetFulfillmentLinesTrigger</span></span>     | <span data-ttu-id="d6f73-368">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-368">Cancelable</span></span>     | <span data-ttu-id="d6f73-369">注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-369">Executed before the Order fulfillment lines are loaded in the Order fulfillment view.</span></span>|
| <span data-ttu-id="d6f73-370">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-370">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="d6f73-371">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-371">Cancelable</span></span>     | <span data-ttu-id="d6f73-372">**出荷** ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-372">Executed before the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="d6f73-373">PostShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-373">PostShipFulfillmentLinesTrigger</span></span>   | <span data-ttu-id="d6f73-374">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-374">Non-Cancelable</span></span>     | <span data-ttu-id="d6f73-375">**出荷** ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-375">Executed after the shipping is done from the Order fulfillment view by selecting the **Ship** button.</span></span>|
| <span data-ttu-id="d6f73-376">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-376">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="d6f73-377">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-377">Cancelable</span></span>     | <span data-ttu-id="d6f73-378">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-378">Executed before the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d6f73-379">PostMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-379">PostMarkFulfillmentLinesAsPackedTrigger</span></span>   | <span data-ttu-id="d6f73-380">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-380">Non-Cancelable</span></span>     | <span data-ttu-id="d6f73-381">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-381">Executed after the mark as packed option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d6f73-382">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-382">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="d6f73-383">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-383">Cancelable</span></span>     | <span data-ttu-id="d6f73-384">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-384">Executed before the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d6f73-385">PostCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-385">PostCreatePackingSlipTrigger</span></span>  | <span data-ttu-id="d6f73-386">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-386">Non-Cancelable</span></span>     | <span data-ttu-id="d6f73-387">**梱包** ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-387">Executed after the create packing slip option is triggered from the order fulfillment view by selecting the **Pack** button.</span></span>|
| <span data-ttu-id="d6f73-388">PostReturnInvoicedSalesLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-388">PostReturnInvoicedSalesLinesTrigger</span></span>   | <span data-ttu-id="d6f73-389">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-389">Non-Cancelable</span></span>     | <span data-ttu-id="d6f73-390">返品対象として 1 つ以上の請求書が選択された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-390">Executed after one or more invoices selected for return.</span></span>|
| <span data-ttu-id="d6f73-391">PreResendEmailReceiptTrigger (10.0.13)</span><span class="sxs-lookup"><span data-stu-id="d6f73-391">PreResendEmailReceiptTrigger (10.0.13)</span></span>    | <span data-ttu-id="d6f73-392">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-392">Cancelable</span></span>     | <span data-ttu-id="d6f73-393">仕訳帳ビューを表示から電子メールを送信する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-393">Executed before sending the email from the Show journal view.</span></span>|
| <span data-ttu-id="d6f73-394">PreRecallCustomerQuoteTrigger (10.0.18)</span><span class="sxs-lookup"><span data-stu-id="d6f73-394">PreRecallCustomerQuoteTrigger (10.0.18)</span></span>   | <span data-ttu-id="d6f73-395">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-395">Cancelable</span></span>     | <span data-ttu-id="d6f73-396">顧客見積がリコール注文ビューからリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-396">Executed before the customer quote is recalled from the recall order view.</span></span>|
| <span data-ttu-id="d6f73-397">PostRecallCustomerQuoteTrigger (10.0.18)</span><span class="sxs-lookup"><span data-stu-id="d6f73-397">PostRecallCustomerQuoteTrigger (10.0.18)</span></span>  | <span data-ttu-id="d6f73-398">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-398">Non-Cancelable</span></span>     | <span data-ttu-id="d6f73-399">顧客見積がリコール注文ビューからリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-399">Executed after the customer quote is recalled from the recall order view.</span></span>|



## <a name="shift-triggers"></a><span data-ttu-id="d6f73-400">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-400">Shift triggers</span></span>

| <span data-ttu-id="d6f73-401">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-401">Trigger</span></span>              | <span data-ttu-id="d6f73-402">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-402">Type</span></span>           | <span data-ttu-id="d6f73-403">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-403">Description</span></span>                                             | <span data-ttu-id="d6f73-404">リリース</span><span class="sxs-lookup"><span data-stu-id="d6f73-404">Release</span></span>    |
|----------------------|----------------|---------------------------------------------------------|--------------|
| <span data-ttu-id="d6f73-405">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-405">PostOpenShiftTrigger</span></span> | <span data-ttu-id="d6f73-406">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-406">Non-cancelable</span></span> | <span data-ttu-id="d6f73-407">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-407">This trigger is executed after the new shift is opened.</span></span> |     |
| <span data-ttu-id="d6f73-408">PreCloseShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-408">PreCloseShiftTrigger</span></span> | <span data-ttu-id="d6f73-409">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-409">Cancelable</span></span> | <span data-ttu-id="d6f73-410">このトリガーは、シフトが開かれる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-410">This trigger is executed before the shift is closed.</span></span> |    |
| <span data-ttu-id="d6f73-411">PreResumeShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-411">PreResumeShiftTrigger</span></span> | <span data-ttu-id="d6f73-412">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-412">Cancelable</span></span> | <span data-ttu-id="d6f73-413">このトリガーは、シフトが再開される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-413">This trigger is executed before the shift is resumed.</span></span> |<span data-ttu-id="d6f73-414">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d6f73-414">10.0.16</span></span>   |
| <span data-ttu-id="d6f73-415">PostResumeShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-415">PostResumeShiftTrigger</span></span> | <span data-ttu-id="d6f73-416">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-416">Non-cancelable</span></span> | <span data-ttu-id="d6f73-417">このトリガーは、シフトが再開された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-417">This trigger is executed after the shift is resumed.</span></span> | <span data-ttu-id="d6f73-418">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d6f73-418">10.0.16</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="d6f73-419">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-419">Tax override triggers</span></span>

| <span data-ttu-id="d6f73-420">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-420">Trigger</span></span>                           | <span data-ttu-id="d6f73-421">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-421">Type</span></span>           | <span data-ttu-id="d6f73-422">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-422">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="d6f73-423">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-423">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="d6f73-424">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-424">Cancelable</span></span>     | <span data-ttu-id="d6f73-425">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-425">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="d6f73-426">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-426">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="d6f73-427">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-427">Non-cancelable</span></span> | <span data-ttu-id="d6f73-428">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-428">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="d6f73-429">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-429">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="d6f73-430">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-430">Cancelable</span></span>     | <span data-ttu-id="d6f73-431">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-431">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="d6f73-432">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-432">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="d6f73-433">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-433">Non-cancelable</span></span> | <span data-ttu-id="d6f73-434">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-434">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="d6f73-435">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-435">Transaction triggers</span></span>

| <span data-ttu-id="d6f73-436">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-436">Trigger</span></span>                            | <span data-ttu-id="d6f73-437">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-437">Type</span></span>           | <span data-ttu-id="d6f73-438">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-438">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="d6f73-439">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-439">BeginTransactionTrigger</span></span>            | <span data-ttu-id="d6f73-440">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-440">Non-cancelable</span></span> | <span data-ttu-id="d6f73-441">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-441">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="d6f73-442">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-442">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="d6f73-443">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-443">Cancelable</span></span>     | <span data-ttu-id="d6f73-444">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-444">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="d6f73-445">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-445">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="d6f73-446">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-446">Cancelable</span></span>     | <span data-ttu-id="d6f73-447">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-447">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="d6f73-448">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-448">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="d6f73-449">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-449">Non-cancelable</span></span> | <span data-ttu-id="d6f73-450">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-450">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="d6f73-451">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-451">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="d6f73-452">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-452">Cancelable</span></span>     | <span data-ttu-id="d6f73-453">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-453">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="d6f73-454">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-454">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="d6f73-455">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-455">Non-cancelable</span></span> | <span data-ttu-id="d6f73-456">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-456">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="d6f73-457">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-457">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="d6f73-458">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-458">Cancelable</span></span>     | <span data-ttu-id="d6f73-459">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-459">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="d6f73-460">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-460">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="d6f73-461">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-461">Non-cancelable</span></span> | <span data-ttu-id="d6f73-462">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-462">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="d6f73-463">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-463">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="d6f73-464">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-464">Cancelable</span></span>     | <span data-ttu-id="d6f73-465">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-465">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="d6f73-466">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-466">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="d6f73-467">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-467">Non-cancelable</span></span> | <span data-ttu-id="d6f73-468">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-468">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="d6f73-469">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-469">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d6f73-470">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-470">Cancelable</span></span>     | <span data-ttu-id="d6f73-471">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-471">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="d6f73-472">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-472">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d6f73-473">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-473">Non-cancelable</span></span> | <span data-ttu-id="d6f73-474">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-474">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="d6f73-475">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-475">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="d6f73-476">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-476">Non-cancelable</span></span> | <span data-ttu-id="d6f73-477">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-477">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="d6f73-478">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-478">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="d6f73-479">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-479">Cancelable</span></span>     | <span data-ttu-id="d6f73-480">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-480">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="d6f73-481">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-481">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="d6f73-482">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="d6f73-482">Non-Cancelable</span></span> | <span data-ttu-id="d6f73-483">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-483">Executed after the customer order is recalled.</span></span>        |
| <span data-ttu-id="d6f73-484">PreSelectTransactionPaymentMethodTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-484">PreSelectTransactionPaymentMethodTrigger</span></span>       | <span data-ttu-id="d6f73-485">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-485">Cancelable</span></span> |  <span data-ttu-id="d6f73-486">ユーザーが **カート ビュー - 合計** パネルで **合計** を選択すると、使用可能な支払方法が表示され、このトリガーはこのダイアログが表示される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-486">When the user selects the **Totals** button in the **Cart view - totals** panel, the available payment methods are shown and this trigger will get executed before this dialog is shown.</span></span> <span data-ttu-id="d6f73-487">このトリガーから利用可能な支払方法を変更するための拡張コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-487">You can us extension code to modify the available payment methods from this trigger.</span></span>      |
| <span data-ttu-id="d6f73-488">PreShipSelectedCartLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-488">PreShipSelectedCartLinesTrigger</span></span>       | <span data-ttu-id="d6f73-489">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-489">Cancelable</span></span> |  <span data-ttu-id="d6f73-490">製品が出荷対象として選択されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-490">Executed when the product is selected for shipping.</span></span>      |

## <a name="reason-code-triggers"></a><span data-ttu-id="d6f73-491">理由コード トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-491">Reason code triggers</span></span>
| <span data-ttu-id="d6f73-492">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-492">Trigger</span></span>              | <span data-ttu-id="d6f73-493">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-493">Type</span></span>           | <span data-ttu-id="d6f73-494">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-494">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d6f73-495">PostGetReasonCodeLine</span><span class="sxs-lookup"><span data-stu-id="d6f73-495">PostGetReasonCodeLine</span></span> | <span data-ttu-id="d6f73-496">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-496">Cancelable</span></span> | <span data-ttu-id="d6f73-497">このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-497">This trigger is executed after the reason code line value is entered (before the reason code is added to the cart).</span></span> |

## <a name="transfer-order-triggers"></a><span data-ttu-id="d6f73-498">移動オーダー トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-498">Transfer Order triggers</span></span>
| <span data-ttu-id="d6f73-499">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-499">Trigger</span></span>              | <span data-ttu-id="d6f73-500">型</span><span class="sxs-lookup"><span data-stu-id="d6f73-500">Type</span></span>           | <span data-ttu-id="d6f73-501">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-501">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="d6f73-502">PreCreateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-502">PreCreateTransferOrderTrigger</span></span> | <span data-ttu-id="d6f73-503">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-503">Cancelable</span></span> | <span data-ttu-id="d6f73-504">このトリガーは、移動オーダーが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-504">This trigger is executed before the transfer order is created (executed after the order input).</span></span> |
| <span data-ttu-id="d6f73-505">PreUpdateTransferOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-505">PreUpdateTransferOrderTrigger</span></span> | <span data-ttu-id="d6f73-506">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-506">Cancelable</span></span> | <span data-ttu-id="d6f73-507">このトリガーは、移動オーダーが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-507">This trigger is executed before the transfer order is updated.</span></span> |

## <a name="inventory-triggers"></a><span data-ttu-id="d6f73-508">在庫トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-508">Inventory triggers</span></span>
| <span data-ttu-id="d6f73-509">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-509">Trigger</span></span>              | <span data-ttu-id="d6f73-510">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-510">Type</span></span>           | <span data-ttu-id="d6f73-511">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-511">Description</span></span>                                             | <span data-ttu-id="d6f73-512">リリース</span><span class="sxs-lookup"><span data-stu-id="d6f73-512">Release</span></span>     |
|----------------------|----------------|---------------------------------------------------------|--------------------------|
| <span data-ttu-id="d6f73-513">PreCreateInventoryDocumentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-513">PreCreateInventoryDocumentTrigger</span></span> | <span data-ttu-id="d6f73-514">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-514">Cancelable</span></span> | <span data-ttu-id="d6f73-515">このトリガーは、入庫/出庫ドキュメントが作成される前に実行 (注文入力後に実行) されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-515">This trigger is executed before the inbound/outbound document is created (executed after the order input).</span></span> | <span data-ttu-id="d6f73-516">10.0.15</span><span class="sxs-lookup"><span data-stu-id="d6f73-516">10.0.15</span></span> |
| <span data-ttu-id="d6f73-517">PreUpdateInventoryDocumentTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-517">PreUpdateInventoryDocumentTrigger</span></span> | <span data-ttu-id="d6f73-518">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-518">Cancelable</span></span> | <span data-ttu-id="d6f73-519">このトリガーは、入庫/出庫ドキュメントが更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-519">This trigger is executed before the inbound/outbound document is updated.</span></span> | <span data-ttu-id="d6f73-520">10.0.15</span><span class="sxs-lookup"><span data-stu-id="d6f73-520">10.0.15</span></span> |

## <a name="stock-count-triggers"></a><span data-ttu-id="d6f73-521">在庫数のトリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-521">Stock count triggers</span></span>

| <span data-ttu-id="d6f73-522">トリガー</span><span class="sxs-lookup"><span data-stu-id="d6f73-522">Trigger</span></span>              | <span data-ttu-id="d6f73-523">種類</span><span class="sxs-lookup"><span data-stu-id="d6f73-523">Type</span></span>           | <span data-ttu-id="d6f73-524">説明</span><span class="sxs-lookup"><span data-stu-id="d6f73-524">Description</span></span>                                             | <span data-ttu-id="d6f73-525">リリース</span><span class="sxs-lookup"><span data-stu-id="d6f73-525">Release</span></span>    |
|----------------------|----------------|---------------------------------------------------------|--------------|
| <span data-ttu-id="d6f73-526">PreAdjustStockCountLineQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-526">PreAdjustStockCountLineQuantityTrigger</span></span> | <span data-ttu-id="d6f73-527">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-527">Cancelable</span></span> | <span data-ttu-id="d6f73-528">このトリガーは、明細行の在庫数が調整される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-528">This trigger is executed before the stock count for a line is adjusted.</span></span> |<span data-ttu-id="d6f73-529">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d6f73-529">10.0.16</span></span>    |
| <span data-ttu-id="d6f73-530">PreSaveStockCountJournalTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f73-530">PreSaveStockCountJournalTrigger</span></span> | <span data-ttu-id="d6f73-531">解約可能</span><span class="sxs-lookup"><span data-stu-id="d6f73-531">Cancelable</span></span> | <span data-ttu-id="d6f73-532">このトリガーは、在庫数仕訳帳が保存される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-532">This trigger is executed before the stock count journal is saved.</span></span> | <span data-ttu-id="d6f73-533">10.0.16</span><span class="sxs-lookup"><span data-stu-id="d6f73-533">10.0.16</span></span> |

## <a name="business-scenario"></a><span data-ttu-id="d6f73-534">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="d6f73-534">Business scenario</span></span>
<span data-ttu-id="d6f73-535">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-535">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="d6f73-536">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-536">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="d6f73-537">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6f73-537">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="d6f73-538">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-538">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="d6f73-539">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-539">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="d6f73-540">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="d6f73-540">Implement a trigger</span></span>

1. <span data-ttu-id="d6f73-541">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-541">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="d6f73-542">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-542">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="d6f73-543">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-543">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d6f73-544">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-544">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="d6f73-545">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-545">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="d6f73-546">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-546">Add the following **import** statements to import the relevant entities and context.</span></span>

   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
   
7. <span data-ttu-id="d6f73-547">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-547">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
    ```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
    ```
8. <span data-ttu-id="d6f73-548">トリガーの **実行** メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-548">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
   
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
   
   <span data-ttu-id="d6f73-549">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d6f73-549">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="d6f73-550">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-550">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="d6f73-551">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-551">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="d6f73-552">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-552">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="d6f73-553">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-553">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="d6f73-554">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-554">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="d6f73-555">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d6f73-555">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="d6f73-556">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6f73-556">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="d6f73-557">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-557">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="d6f73-558">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="d6f73-558">Override the CRT receipt request to generate the receipt data</span></span>


<span data-ttu-id="d6f73-559">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-559">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> 


1. <span data-ttu-id="d6f73-560">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-560">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="d6f73-561">**ファイル** メニューで、**開く \> プロジェクト/ソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-561">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="d6f73-562">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-562">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="d6f73-563">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-563">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="d6f73-564">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-564">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="d6f73-565">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-565">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="d6f73-566">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-566">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="d6f73-567">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-567">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="d6f73-568">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-568">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="d6f73-569">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点ではコマース トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="d6f73-569">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the commerce transaction table.</span></span> <span data-ttu-id="d6f73-570">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6f73-570">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="d6f73-571">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="d6f73-571">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6f73-572">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d6f73-572">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="d6f73-573">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="d6f73-573">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="d6f73-574">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-574">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="d6f73-575">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-575">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="d6f73-576">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-576">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="d6f73-577">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d6f73-577">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="d6f73-578">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-578">Compile and build the project.</span></span>
12. <span data-ttu-id="d6f73-579">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-579">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="d6f73-580">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-580">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="d6f73-581">また、**…\\RetailSDK\\参照** フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-581">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="d6f73-582">**commerceruntime.ext.config** ファイルを開き、\<composition\> セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-582">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="d6f73-583">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-583">Save and close the file.</span></span>
17. <span data-ttu-id="d6f73-584">Commerce Scale Unit を再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="d6f73-584">Restart the Commerce Scale Unit to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="d6f73-585">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="d6f73-585">Add the custom receipt layout</span></span>

1. <span data-ttu-id="d6f73-586">Dynamics 365 Commerce を開きます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-586">Open Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="d6f73-587">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS** > **受領書フォーマット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-587">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="d6f73-588">**受領書フォーマット** 内の **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-588">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="d6f73-589">**提出した受領書フォーマット** フィールドに、**中断** という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-589">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="d6f73-590">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-590">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="d6f73-591">**デザイナー** をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-591">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="d6f73-592">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="d6f73-592">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="d6f73-593">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-593">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="d6f73-594">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-594">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="d6f73-595">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-595">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="d6f73-596">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-596">Click **Save**.</span></span>
9. <span data-ttu-id="d6f73-597">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **視覚プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-597">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="d6f73-598">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-598">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="d6f73-599">**一般** タブの **追加** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-599">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="d6f73-600">**受領書タイプ** で、**CustomReceiptType7** を選択し、**受領書フォーマット** で **中断** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-600">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="d6f73-601">**Retail とコマース > Retail とコマース IT > 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-601">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="d6f73-602">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-602">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d6f73-603">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-603">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="d6f73-604">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d6f73-604">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="d6f73-605">**Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-605">Go to **Retail and Commerce** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="d6f73-606">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-606">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="d6f73-607">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-607">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="d6f73-608">操作バーの **編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-608">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="d6f73-609">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-609">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="d6f73-610">**プリンター** ドロップダウン リストで、**Windows ドライバー** を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-610">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="d6f73-611">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-611">Click **Save**.</span></span>
6. <span data-ttu-id="d6f73-612">**Retail とコマース** > **Retail とコマース IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-612">Go to **Retail and Commerce** > **Retail and Commerce IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="d6f73-613">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-613">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="d6f73-614">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-614">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="d6f73-615">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="d6f73-615">Validate the extension</span></span>

1. <span data-ttu-id="d6f73-616">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="d6f73-616">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="d6f73-617">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-617">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="d6f73-618">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="d6f73-618">Suspend the transaction.</span></span>
4. <span data-ttu-id="d6f73-619">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d6f73-619">The custom receipt should print.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
