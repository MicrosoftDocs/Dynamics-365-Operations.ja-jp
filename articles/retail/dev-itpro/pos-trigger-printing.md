---
title: Retail Modern POS (MPOS) のトリガーと印刷
description: トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。
author: mugunthanm
manager: AnnBe
ms.date: 04/26/2019
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
ms.openlocfilehash: 30916a0d3e953da3c7f63293b84d5cd2e83c8d68
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833744"
---
# <a name="retail-modern-pos-mpos-triggers-and-printing"></a><span data-ttu-id="62685-103">Retail Modern POS (MPOS) のトリガーと印刷</span><span class="sxs-lookup"><span data-stu-id="62685-103">Retail Modern POS (MPOS) triggers and printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62685-104">トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="62685-104">You can use triggers to capture events that occur before or after Retail Modern POS operations.</span></span> <span data-ttu-id="62685-105">トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="62685-105">Using triggers supports several business logic scenarios that enable you to do the following:</span></span> 
- <span data-ttu-id="62685-106">操作の実行前または完了後に、カスタム ロジックを挿入します。</span><span class="sxs-lookup"><span data-stu-id="62685-106">Insert custom logic before the operation runs or after it has completed.</span></span> <span data-ttu-id="62685-107">これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="62685-107">This includes operation-specific triggers and generic triggers called the PreOperationTrigger and PostOperationTrigger, which run at the beginning and end of all POS operations.</span></span>  
- <span data-ttu-id="62685-108">操作を続行またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="62685-108">Continue or cancel an operation.</span></span> <span data-ttu-id="62685-109">たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="62685-109">For example, if your validation fails or returns an error, then you can cancel the operation in pre-trigger.</span></span> <span data-ttu-id="62685-110">ポスト トリガーはキャンセル可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="62685-110">Post-triggers are not cancelable.</span></span>
- <span data-ttu-id="62685-111">標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。</span><span class="sxs-lookup"><span data-stu-id="62685-111">Use the post-trigger for scenarios where you want to show custom messages or insert custom fields after the standard logic is performed.</span></span> 

<span data-ttu-id="62685-112">このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 for Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="62685-112">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="62685-113">次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="62685-113">The following table lists the available triggers and denotes whether they can be cancelled.</span></span>

## <a name="application-triggers"></a><span data-ttu-id="62685-114">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-114">Application triggers</span></span>

| <span data-ttu-id="62685-115">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-115">Trigger</span></span>                   | <span data-ttu-id="62685-116">種類</span><span class="sxs-lookup"><span data-stu-id="62685-116">Type</span></span>           | <span data-ttu-id="62685-117">説明</span><span class="sxs-lookup"><span data-stu-id="62685-117">Description</span></span>                                                                                                                                          |
|---------------------------|----------------|--------------|
| <span data-ttu-id="62685-118">ApplicationStartTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-118">ApplicationStartTrigger</span></span>   | <span data-ttu-id="62685-119">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-119">Non-cancelable</span></span> | <span data-ttu-id="62685-120">POS アプリケーションが開始した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-120">Executed after the POS application is started.</span></span> <span data-ttu-id="62685-121">以前実行された内容はどれでも元に戻すかキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="62685-121">You can revert or cancel whatever executed previously.</span></span> |
| <span data-ttu-id="62685-122">ApplicationSuspendTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-122">ApplicationSuspendTrigger</span></span> | <span data-ttu-id="62685-123">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-123">Non-cancelable</span></span> | <span data-ttu-id="62685-124">POS アプリケーションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-124">Executed after the POS application is suspended.</span></span>                                                                                     |
| <span data-ttu-id="62685-125">PreLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-125">PreLogOnTriggerTrigger</span></span>    | <span data-ttu-id="62685-126">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-126">Cancelable</span></span>     | <span data-ttu-id="62685-127">POS ログ オン前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-127">Executed before the POS log on.</span></span>                                                                                                      |
| <span data-ttu-id="62685-128">PostLogOnTriggerTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-128">PostLogOnTriggerTrigger</span></span>   | <span data-ttu-id="62685-129">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-129">Non-cancelable</span></span> | <span data-ttu-id="62685-130">POS ログ オン後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-130">Executed after the POS log on.</span></span>                                                                                                       |
| <span data-ttu-id="62685-131">PostLogOffTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-131">PostLogOffTrigger</span></span>         | <span data-ttu-id="62685-132">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-132">Non-cancelable</span></span> | <span data-ttu-id="62685-133">POS ログ オフ後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-133">Executed after the POS log off.</span></span>                                                                                                      | 
| <span data-ttu-id="62685-134">PreLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-134">PreLockTerminalTrigger</span></span>    | <span data-ttu-id="62685-135">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-135">Cancelable</span></span>     | <span data-ttu-id="62685-136">POS レジスターのロック前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-136">Executed before the POS register lock.</span></span>  |
| <span data-ttu-id="62685-137">PostLockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-137">PostLockTerminalTrigger</span></span>   | <span data-ttu-id="62685-138">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-138">Non-Cancelable</span></span> | <span data-ttu-id="62685-139">POS レジスターのロック後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-139">Executed after the POS register lock.</span></span>   | 
| <span data-ttu-id="62685-140">PreUnlockTerminalTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-140">PreUnlockTerminalTrigger</span></span>         | <span data-ttu-id="62685-141">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-141">Cancelable</span></span>     | <span data-ttu-id="62685-142">POS レジスターのロック解除前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-142">Executed before the POS register is unlocked.</span></span>  |
| <span data-ttu-id="62685-143">PostDeviceActivationTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-143">PostDeviceActivationTrigger</span></span>      | <span data-ttu-id="62685-144">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-144">Non-Cancelable</span></span> | <span data-ttu-id="62685-145">POS のアクティブ化後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-145">Executed after the POS activation.</span></span>   | 
| <span data-ttu-id="62685-146">PreElevateUserTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-146">PreElevateUserTrigger</span></span>      | <span data-ttu-id="62685-147">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-147">Cancelable</span></span> | <span data-ttu-id="62685-148">マネージャー オーバーライドの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-148">Executed before the manager override.</span></span>   | 
| <span data-ttu-id="62685-149">PreRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-149">PreRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="62685-150">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-150">Cancelable</span></span> | <span data-ttu-id="62685-151">監査イベントの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-151">Executed before the audit event.</span></span>   | 
| <span data-ttu-id="62685-152">PostRegisterAuditEventTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-152">PostRegisterAuditEventTrigger</span></span>      | <span data-ttu-id="62685-153">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-153">Non-Cancelable</span></span> | <span data-ttu-id="62685-154">監査イベントの後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-154">Executed after the audit event.</span></span>   | 


## <a name="cash-management-triggers"></a><span data-ttu-id="62685-155">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-155">Cash management triggers</span></span>

| <span data-ttu-id="62685-156">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-156">Trigger</span></span>                      | <span data-ttu-id="62685-157">型</span><span class="sxs-lookup"><span data-stu-id="62685-157">Type</span></span>           | <span data-ttu-id="62685-158">説明</span><span class="sxs-lookup"><span data-stu-id="62685-158">Description</span></span>                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="62685-159">PreTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-159">PreTenderDeclarationTrigger</span></span>  | <span data-ttu-id="62685-160">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-160">Cancelable</span></span>     | <span data-ttu-id="62685-161">POS の支払または入金申告前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-161">Executed before the POS tender declaration.</span></span> |
| <span data-ttu-id="62685-162">PostTenderDeclarationTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-162">PostTenderDeclarationTrigger</span></span> | <span data-ttu-id="62685-163">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-163">Non-cancelable</span></span> | <span data-ttu-id="62685-164">POS の支払または入金申告後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-164">Executed after the POS tender declaration.</span></span>  |
| <span data-ttu-id="62685-165">PreFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-165">PreFloatEntryTrigger</span></span>         | <span data-ttu-id="62685-166">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-166">Cancelable</span></span>     | <span data-ttu-id="62685-167">POS 釣銭入力の前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-167">Executed before the POS float entry.</span></span> |
| <span data-ttu-id="62685-168">PostFloatEntryTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-168">PostFloatEntryTrigger</span></span>        | <span data-ttu-id="62685-169">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-169">Non-cancelable</span></span> | <span data-ttu-id="62685-170">POS 釣銭入力の後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-170">Executed after the POS float entry.</span></span>  |    


## <a name="customer-triggers"></a><span data-ttu-id="62685-171">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-171">Customer triggers</span></span>

| <span data-ttu-id="62685-172">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-172">Trigger</span></span>                   | <span data-ttu-id="62685-173">種類</span><span class="sxs-lookup"><span data-stu-id="62685-173">Type</span></span>                    | <span data-ttu-id="62685-174">説明</span><span class="sxs-lookup"><span data-stu-id="62685-174">Description</span></span>                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="62685-175">PreCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-175">PreCustomerAddTrigger</span></span>     | <span data-ttu-id="62685-176">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-176">Cancelable</span></span>              | <span data-ttu-id="62685-177">新しい顧客を作成する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-177">Executed before creating a new customer.</span></span>             |
| <span data-ttu-id="62685-178">PostCustomerAddTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-178">PostCustomerAddTrigger</span></span>    | <span data-ttu-id="62685-179">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-179">Non-cancelable</span></span>          | <span data-ttu-id="62685-180">新しい顧客を作成した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-180">Executed after creating a new customer.</span></span>              |
| <span data-ttu-id="62685-181">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-181">PreCustomerClearTrigger</span></span>   | <span data-ttu-id="62685-182">PreCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-182">PreCustomerClearTrigger</span></span> | <span data-ttu-id="62685-183">顧客がカートから削除する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-183">Executed before the customer cleared from the cart.</span></span> |
| <span data-ttu-id="62685-184">PostCustomerClearTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-184">PostCustomerClearTrigger</span></span>  | <span data-ttu-id="62685-185">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-185">Non-cancelable</span></span>          | <span data-ttu-id="62685-186">顧客がカートから削除した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-186">Executed after the customer cleared from the cart.</span></span> |
| <span data-ttu-id="62685-187">PreCustomerSetTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-187">PreCustomerSetTrigger</span></span>     | <span data-ttu-id="62685-188">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-188">Cancelable</span></span>              | <span data-ttu-id="62685-189">顧客がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-189">Executed before the customer is added to the cart.</span></span>            |
| <span data-ttu-id="62685-190">PreCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-190">PreCustomerSearchTrigger</span></span>  | <span data-ttu-id="62685-191">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-191">Cancelable</span></span>              | <span data-ttu-id="62685-192">顧客検索が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-192">Executed before customer search is performed.</span></span>      |
| <span data-ttu-id="62685-193">PostCustomerSearchTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-193">PostCustomerSearchTrigger</span></span> | <span data-ttu-id="62685-194">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-194">Non-cancelable</span></span>          | <span data-ttu-id="62685-195">顧客検索が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-195">Executed after customer search is performed.</span></span>       |
| <span data-ttu-id="62685-196">PostIssueLoyaltyCardTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-196">PostIssueLoyaltyCardTrigger</span></span>  | <span data-ttu-id="62685-197">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-197">Non-cancelable</span></span>          | <span data-ttu-id="62685-198">ロイヤルティ カードが発行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-198">Executed after the loyalty card is issued.</span></span>       |

## <a name="discount-triggers"></a><span data-ttu-id="62685-199">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="62685-199">Discount triggers</span></span>

| <span data-ttu-id="62685-200">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-200">Trigger</span></span>                         | <span data-ttu-id="62685-201">型</span><span class="sxs-lookup"><span data-stu-id="62685-201">Type</span></span>           | <span data-ttu-id="62685-202">説明</span><span class="sxs-lookup"><span data-stu-id="62685-202">Description</span></span>                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="62685-203">PreLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-203">PreLineDiscountAmountTrigger</span></span>    | <span data-ttu-id="62685-204">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-204">Cancelable</span></span>     | <span data-ttu-id="62685-205">行割引金額がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-205">Executed before line discount amount is added to the cart line.</span></span> |
| <span data-ttu-id="62685-206">PostLineDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-206">PostLineDiscountAmountTrigger</span></span>   | <span data-ttu-id="62685-207">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-207">Non-cancelable</span></span> | <span data-ttu-id="62685-208">行割引金額がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-208">Executed after line discount amount added to the cart line.</span></span>     |
| <span data-ttu-id="62685-209">PreLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-209">PreLineDiscountPercentTrigger</span></span>   | <span data-ttu-id="62685-210">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-210">Cancelable</span></span>     | <span data-ttu-id="62685-211">行割引率がカート行に追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-211">Executed before line discount percent added to the cart line.</span></span>   |
| <span data-ttu-id="62685-212">PostLineDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-212">PostLineDiscountPercentTrigger</span></span>  | <span data-ttu-id="62685-213">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-213">Non-cancelable</span></span> | <span data-ttu-id="62685-214">行割引率がカート行に追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-214">Executed after line discount percent added to the cart line.</span></span>    |
| <span data-ttu-id="62685-215">PreTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-215">PreTotalDiscountAmountTrigger</span></span>   | <span data-ttu-id="62685-216">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-216">Cancelable</span></span>     | <span data-ttu-id="62685-217">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-217">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="62685-218">PostTotalDiscountAmountTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-218">PostTotalDiscountAmountTrigger</span></span>  | <span data-ttu-id="62685-219">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-219">Non-cancelable</span></span> | <span data-ttu-id="62685-220">合計金額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-220">Executed after total amount percent added to the cart.</span></span>          |
| <span data-ttu-id="62685-221">PreTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-221">PreTotalDiscountPercentTrigger</span></span>  | <span data-ttu-id="62685-222">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-222">Cancelable</span></span>     | <span data-ttu-id="62685-223">合計割引額がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-223">Executed before total discount percent added to the cart.</span></span>       |
| <span data-ttu-id="62685-224">PostTotalDiscountPercentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-224">PostTotalDiscountPercentTrigger</span></span> | <span data-ttu-id="62685-225">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-225">Non-cancelable</span></span> | <span data-ttu-id="62685-226">合計割引額がカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-226">Executed after total discount percent added to the cart.</span></span>        |
| <span data-ttu-id="62685-227">PreAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-227">PreAddCouponTrigger</span></span>             | <span data-ttu-id="62685-228">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-228">Cancelable</span></span>     | <span data-ttu-id="62685-229">割引クーポンをカートに追加する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-229">Executed before adding discount coupon to the cart.</span></span>             |
| <span data-ttu-id="62685-230">PostAddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-230">PostAddCouponTrigger</span></span>            | <span data-ttu-id="62685-231">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-231">Non-cancelable</span></span> | <span data-ttu-id="62685-232">割引クーポンをカートに追加した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-232">Executed after adding discount coupon to the cart.</span></span>              |

## <a name="operation-triggers"></a><span data-ttu-id="62685-233">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="62685-233">Operation triggers</span></span>

| <span data-ttu-id="62685-234">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-234">Trigger</span></span>              | <span data-ttu-id="62685-235">種類</span><span class="sxs-lookup"><span data-stu-id="62685-235">Type</span></span>           | <span data-ttu-id="62685-236">説明</span><span class="sxs-lookup"><span data-stu-id="62685-236">Description</span></span>                                                                                                                                           |
|----------------------|----------------|-------------------------|
| <span data-ttu-id="62685-237">PreOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-237">PreOperationTrigger</span></span>  | <span data-ttu-id="62685-238">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-238">Cancelable</span></span>     | <span data-ttu-id="62685-239">すべての POS 操作前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="62685-239">Generic trigger executed before all POS operations.</span></span> <span data-ttu-id="62685-240">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="62685-240">You can use this trigger if there is no specific trigger available for a POS operation.</span></span> |
| <span data-ttu-id="62685-241">PreOperationValidationTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-241">PreOperationValidationTrigger</span></span> | <span data-ttu-id="62685-242">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-242">Cancelable</span></span> | <span data-ttu-id="62685-243">操作の検証が始まる前に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="62685-243">Generic trigger executed before the operation validation begins.</span></span>   |
| <span data-ttu-id="62685-244">OperationFailureTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-244">OperationFailureTrigger</span></span> | <span data-ttu-id="62685-245">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-245">Non-cancelable</span></span> | <span data-ttu-id="62685-246">任意の POS 操作が失敗した後で実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="62685-246">Generic trigger executed after any POS operation failed.</span></span>  |
| <span data-ttu-id="62685-247">PostOperationTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-247">PostOperationTrigger</span></span> | <span data-ttu-id="62685-248">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-248">Non-cancelable</span></span> | <span data-ttu-id="62685-249">すべての POS 操作の後に実行される一般的なトリガー。</span><span class="sxs-lookup"><span data-stu-id="62685-249">Generic trigger executed after all POS operations.</span></span> <span data-ttu-id="62685-250">POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="62685-250">You can use this trigger if there is no specific trigger available for a POS operation.</span></span>  |

## <a name="payment-triggers"></a><span data-ttu-id="62685-251">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-251">Payment triggers</span></span>

| <span data-ttu-id="62685-252">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-252">Trigger</span></span>                 | <span data-ttu-id="62685-253">種類</span><span class="sxs-lookup"><span data-stu-id="62685-253">Type</span></span>           | <span data-ttu-id="62685-254">説明</span><span class="sxs-lookup"><span data-stu-id="62685-254">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="62685-255">PreAddTenderLineTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-255">PreAddTenderLineTrigger</span></span> | <span data-ttu-id="62685-256">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-256">Cancelable</span></span>     | <span data-ttu-id="62685-257">支払行がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-257">Executed before the payment line is added to the cart.</span></span> |
| <span data-ttu-id="62685-258">PrePaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-258">PrePaymentTrigger</span></span>       | <span data-ttu-id="62685-259">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-259">Cancelable</span></span>     | <span data-ttu-id="62685-260">POS で支払ボタンをクリックした後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-260">Executed after you click the pay button in POS.</span></span>     |
| <span data-ttu-id="62685-261">PostPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-261">PostPaymentTrigger</span></span>      | <span data-ttu-id="62685-262">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-262">Non-cancelable</span></span> | <span data-ttu-id="62685-263">すべての支払い処理が完了した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-263">Executed after all the payment processing is done.</span></span>  |
| <span data-ttu-id="62685-264">PreVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-264">PreVoidPaymentTrigger</span></span>   | <span data-ttu-id="62685-265">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-265">Cancelable</span></span>     | <span data-ttu-id="62685-266">POS で支払行が無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-266">Executed before the payment line is voided in POS.</span></span>  |
| <span data-ttu-id="62685-267">PostVoidPaymentTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-267">PostVoidPaymentTrigger</span></span>  | <span data-ttu-id="62685-268">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-268">Non-cancelable</span></span> | <span data-ttu-id="62685-269">POS で支払行が無効になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-269">Executed after the payment line is voided in POS.</span></span>   |

## <a name="printing-triggers"></a><span data-ttu-id="62685-270">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-270">Printing Triggers</span></span>

| <span data-ttu-id="62685-271">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-271">Trigger</span></span>                    | <span data-ttu-id="62685-272">種類</span><span class="sxs-lookup"><span data-stu-id="62685-272">Type</span></span>       | <span data-ttu-id="62685-273">説明</span><span class="sxs-lookup"><span data-stu-id="62685-273">Description</span></span>                                                                                                     |
|----------------------------|------------|--------|
| <span data-ttu-id="62685-274">PrePrintReceiptCopyTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-274">PrePrintReceiptCopyTrigger</span></span> | <span data-ttu-id="62685-275">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-275">Cancelable</span></span> | <span data-ttu-id="62685-276">レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-276">Executed before the receipt copy is printed form the show journal screen or receipt view screen.</span></span> |
| <span data-ttu-id="62685-277">PostReceiptPromptTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-277">PostReceiptPromptTrigger</span></span>   | <span data-ttu-id="62685-278">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-278">Non-cancelable</span></span> | <span data-ttu-id="62685-279">レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-279">Executed after the receipt prompt - Do you want to print or not print receipt.</span></span> |

## <a name="product-triggers"></a><span data-ttu-id="62685-280">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-280">Product triggers</span></span>

| <span data-ttu-id="62685-281">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-281">Trigger</span></span>                    | <span data-ttu-id="62685-282">種類</span><span class="sxs-lookup"><span data-stu-id="62685-282">Type</span></span>           | <span data-ttu-id="62685-283">説明</span><span class="sxs-lookup"><span data-stu-id="62685-283">Description</span></span>                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62685-284">PostGetSerialNumberTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-284">PostGetSerialNumberTrigger</span></span> | <span data-ttu-id="62685-285">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-285">Non-cancelable</span></span> | <span data-ttu-id="62685-286">シリアル番号がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-286">Executed after the serial number is added to the cart line.</span></span>           |
| <span data-ttu-id="62685-287">PreProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-287">PreProductSaleTrigger</span></span>      | <span data-ttu-id="62685-288">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-288">Cancelable</span></span>     | <span data-ttu-id="62685-289">製品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-289">Executed before the product is added to the cart.</span></span>                   |
| <span data-ttu-id="62685-290">PostProductSaleTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-290">PostProductSaleTrigger</span></span>     | <span data-ttu-id="62685-291">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-291">Non-cancelable</span></span> | <span data-ttu-id="62685-292">製品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-292">Executed after the product is added to the cart.</span></span>                    |
| <span data-ttu-id="62685-293">PreReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-293">PreReturnProductTrigger</span></span>    | <span data-ttu-id="62685-294">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-294">Cancelable</span></span>     | <span data-ttu-id="62685-295">返品がカートに追加される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-295">Executed before the return product is added to the cart.</span></span>            |
| <span data-ttu-id="62685-296">PostReturnProductTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-296">PostReturnProductTrigger</span></span>   | <span data-ttu-id="62685-297">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-297">Non-cancelable</span></span> | <span data-ttu-id="62685-298">返品がカートに追加された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-298">Executed after the return product is added to the cart.</span></span>             |
| <span data-ttu-id="62685-299">PreSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-299">PreSetQuantityTrigger</span></span>      | <span data-ttu-id="62685-300">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-300">Cancelable</span></span>     | <span data-ttu-id="62685-301">数量情報がカート行で更新される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-301">Executed before the quantity information is updated in the cart line.</span></span>  |
| <span data-ttu-id="62685-302">PostSetQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-302">PostSetQuantityTrigger</span></span>     | <span data-ttu-id="62685-303">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-303">Non-cancelable</span></span> | <span data-ttu-id="62685-304">数量情報がカート行で更新となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-304">Executed after the quantity information is updated in the cart line.</span></span>   |
| <span data-ttu-id="62685-305">PrePriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-305">PrePriceOverrideTrigger</span></span>    | <span data-ttu-id="62685-306">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-306">Cancelable</span></span>     | <span data-ttu-id="62685-307">価格がカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-307">Executed before the price is overridden for a cart line.</span></span>               |
| <span data-ttu-id="62685-308">PostPriceOverrideTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-308">PostPriceOverrideTrigger</span></span>   | <span data-ttu-id="62685-309">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-309">Non-cancelable</span></span> | <span data-ttu-id="62685-310">価格がカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-310">Executed after the price is overridden for a cart line.</span></span>                |
| <span data-ttu-id="62685-311">PreClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-311">PreClearQuantityTrigger</span></span>    | <span data-ttu-id="62685-312">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-312">Cancelable</span></span>     | <span data-ttu-id="62685-313">数量情報がカート行から削除になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-313">Executed before the quantity information is cleared from the cart line.</span></span>|
| <span data-ttu-id="62685-314">PostClearQuantityTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-314">PostClearQuantityTrigger</span></span>   | <span data-ttu-id="62685-315">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-315">Non-cancelable</span></span> | <span data-ttu-id="62685-316">数量情報がカート行から削除になった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-316">Executed after the quantity information is cleared from the cart line.</span></span> |
| <span data-ttu-id="62685-317">PreVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-317">PreVoidProductsTrigger</span></span>     | <span data-ttu-id="62685-318">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-318">Cancelable</span></span>     | <span data-ttu-id="62685-319">製品がカートから無効となる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-319">Executed before the product is voided from the cart.</span></span>                   |
| <span data-ttu-id="62685-320">PostVoidProductsTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-320">PostVoidProductsTrigger</span></span>    | <span data-ttu-id="62685-321">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-321">Non-cancelable</span></span> | <span data-ttu-id="62685-322">製品がカートから無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-322">Executed after the product is voided from the cart.</span></span>                    |
| <span data-ttu-id="62685-323">PostPriceCheckTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-323">PostPriceCheckTrigger</span></span>      | <span data-ttu-id="62685-324">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-324">Non-cancelable</span></span> | <span data-ttu-id="62685-325">製品の価格確認が行われた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-325">Executed after the price check for the product is executed.</span></span>          |

## <a name="sales-order-triggers"></a><span data-ttu-id="62685-326">販売注文トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-326">Sales order triggers</span></span>

| <span data-ttu-id="62685-327">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-327">Trigger</span></span>                 | <span data-ttu-id="62685-328">型</span><span class="sxs-lookup"><span data-stu-id="62685-328">Type</span></span>           | <span data-ttu-id="62685-329">説明</span><span class="sxs-lookup"><span data-stu-id="62685-329">Description</span></span>                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="62685-330">PreRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-330">PreRecallCustomerOrderTrigger</span></span>     | <span data-ttu-id="62685-331">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-331">Cancelable</span></span>     | <span data-ttu-id="62685-332">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-332">Executed before the customer order is recalled.</span></span> |
| <span data-ttu-id="62685-333">PostRecallCustomerOrderTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-333">PostRecallCustomerOrderTrigger</span></span>    | <span data-ttu-id="62685-334">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-334">Non-cancelable</span></span> | <span data-ttu-id="62685-335">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-335">Executed after the customer order is recalled.</span></span>  |
| <span data-ttu-id="62685-336">PrePickUpCustomerOrderLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-336">PrePickUpCustomerOrderLinesTrigger</span></span>    | <span data-ttu-id="62685-337">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-337">Cancelable</span></span>     | <span data-ttu-id="62685-338">顧客注文明細行が選択される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-338">Executed before the customer order lines are picked.</span></span>  |
| <span data-ttu-id="62685-339">PreChangeShippingOriginTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-339">PreChangeShippingOriginTrigger</span></span>    | <span data-ttu-id="62685-340">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-340">Cancelable</span></span>     | <span data-ttu-id="62685-341">顧客先発注時に出荷元が変更される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-341">Executed before the shipping origin is changed during customer order.</span></span>|
| <span data-ttu-id="62685-342">PreShipFulfillmentLinesTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-342">PreShipFulfillmentLinesTrigger</span></span>    | <span data-ttu-id="62685-343">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-343">Cancelable</span></span>     | <span data-ttu-id="62685-344">出荷ボタンをクリックすることで、注文フルフィルメント ビューから出荷が行われる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-344">Executed before the shipping is done from the Order fulfillment view by clicking the ship button.</span></span>|
| <span data-ttu-id="62685-345">PreMarkFulfillmentLinesAsPackedTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-345">PreMarkFulfillmentLinesAsPackedTrigger</span></span>    | <span data-ttu-id="62685-346">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-346">Cancelable</span></span>     | <span data-ttu-id="62685-347">梱包ボタンをクリックすることで、注文フルフィルメント ビューから梱包としてマーク オプションがトリガーされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-347">Executed before the mark as packed option is triggered from the order fulfillment view by clicking the Pack button.</span></span>|
| <span data-ttu-id="62685-348">PreCreatePackingSlipTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-348">PreCreatePackingSlipTrigger</span></span>   | <span data-ttu-id="62685-349">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-349">Cancelable</span></span>     | <span data-ttu-id="62685-350">梱包明細の作成オプションがトリガーされる前に、注文フルフィルメント ビューから梱包ボタンをクリックして実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-350">Executed before the create packing slip option triggered is from the order fulfillment view by clicking the Pack button.</span></span>|


## <a name="shift-triggers"></a><span data-ttu-id="62685-351">シフト トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-351">Shift triggers</span></span>
| <span data-ttu-id="62685-352">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-352">Trigger</span></span>              | <span data-ttu-id="62685-353">型</span><span class="sxs-lookup"><span data-stu-id="62685-353">Type</span></span>           | <span data-ttu-id="62685-354">説明</span><span class="sxs-lookup"><span data-stu-id="62685-354">Description</span></span>                                             |
|----------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="62685-355">PostOpenShiftTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-355">PostOpenShiftTrigger</span></span> | <span data-ttu-id="62685-356">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-356">Non-cancelable</span></span> | <span data-ttu-id="62685-357">このトリガーは、新しいシフトが開かれた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-357">This trigger is executed after the new shift is opened.</span></span> |

## <a name="tax-override-triggers"></a><span data-ttu-id="62685-358">税上書きトリガー</span><span class="sxs-lookup"><span data-stu-id="62685-358">Tax override triggers</span></span>

| <span data-ttu-id="62685-359">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-359">Trigger</span></span>                           | <span data-ttu-id="62685-360">種類</span><span class="sxs-lookup"><span data-stu-id="62685-360">Type</span></span>           | <span data-ttu-id="62685-361">説明</span><span class="sxs-lookup"><span data-stu-id="62685-361">Description</span></span>                                                                                     |
|-----------------------------------|----------------|---------------|
| <span data-ttu-id="62685-362">PreOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-362">PreOverrideLineProductTaxTrigger</span></span>  | <span data-ttu-id="62685-363">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-363">Cancelable</span></span>     | <span data-ttu-id="62685-364">税額またはコードがカート行に上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-364">Executed before the tax amount or code is overridden for a cart line.</span></span>           |
| <span data-ttu-id="62685-365">PostOverrideLineProductTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-365">PostOverrideLineProductTaxTrigger</span></span> | <span data-ttu-id="62685-366">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-366">Non-cancelable</span></span> | <span data-ttu-id="62685-367">税額またはコードがカート行に上書きされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-367">Executed after the tax amount or code is overridden for a cart line.</span></span>            |
| <span data-ttu-id="62685-368">PreOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-368">PreOverrideTransactionTaxTrigger</span></span>  | <span data-ttu-id="62685-369">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-369">Cancelable</span></span>     | <span data-ttu-id="62685-370">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-370">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |
| <span data-ttu-id="62685-371">PostOverrideTransactionTaxTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-371">PostOverrideTransactionTaxTrigger</span></span> | <span data-ttu-id="62685-372">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-372">Non-cancelable</span></span> | <span data-ttu-id="62685-373">税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-373">Executed before the tax amount or code is overridden for a cart or transaction.</span></span> |

## <a name="transaction-triggers"></a><span data-ttu-id="62685-374">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="62685-374">Transaction triggers</span></span>

| <span data-ttu-id="62685-375">トリガー</span><span class="sxs-lookup"><span data-stu-id="62685-375">Trigger</span></span>                            | <span data-ttu-id="62685-376">種類</span><span class="sxs-lookup"><span data-stu-id="62685-376">Type</span></span>           | <span data-ttu-id="62685-377">説明</span><span class="sxs-lookup"><span data-stu-id="62685-377">Description</span></span>                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| <span data-ttu-id="62685-378">BeginTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-378">BeginTransactionTrigger</span></span>            | <span data-ttu-id="62685-379">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-379">Non-cancelable</span></span> | <span data-ttu-id="62685-380">トランザクションが初期化される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-380">Executed before the transaction is initialized.</span></span>  |
| <span data-ttu-id="62685-381">PreConfirmReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-381">PreConfirmReturnTransactionTrigger</span></span> | <span data-ttu-id="62685-382">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-382">Cancelable</span></span>     | <span data-ttu-id="62685-383">返品トランザクションが確認される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-383">Executed before the return transaction is confirmed.</span></span>  |
| <span data-ttu-id="62685-384">PreReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-384">PreReturnTransactionTrigger</span></span>        | <span data-ttu-id="62685-385">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-385">Cancelable</span></span>     | <span data-ttu-id="62685-386">返品トランザクションが処理される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-386">Executed before the return transaction is processed.</span></span> |
| <span data-ttu-id="62685-387">PostReturnTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-387">PostReturnTransactionTrigger</span></span>       | <span data-ttu-id="62685-388">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-388">Non-cancelable</span></span> | <span data-ttu-id="62685-389">返品トランザクションが処理された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-389">Executed after the return transaction is processed.</span></span>   |
| <span data-ttu-id="62685-390">PreEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-390">PreEndTransactionTrigger</span></span>           | <span data-ttu-id="62685-391">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-391">Cancelable</span></span>     | <span data-ttu-id="62685-392">終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62685-392">Executed before the end transaction request is called to commit the changes to DB and close the transaction.</span></span> |
| <span data-ttu-id="62685-393">PostEndTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-393">PostEndTransactionTrigger</span></span>          | <span data-ttu-id="62685-394">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-394">Non-cancelable</span></span> | <span data-ttu-id="62685-395">終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62685-395">Executed after the end transaction request is called to commit the changes to DB and close the transaction.</span></span>  |
| <span data-ttu-id="62685-396">PreVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-396">PreVoidTransactionTrigger</span></span>          | <span data-ttu-id="62685-397">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-397">Cancelable</span></span>     | <span data-ttu-id="62685-398">トランザクションが無効になる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-398">Executed before the transaction is voided.</span></span>         |
| <span data-ttu-id="62685-399">PostVoidTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-399">PostVoidTransactionTrigger</span></span>         | <span data-ttu-id="62685-400">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-400">Non-cancelable</span></span> | <span data-ttu-id="62685-401">トランザクションが無効となった後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-401">Executed after the transaction is voided.</span></span>        |
| <span data-ttu-id="62685-402">PreSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-402">PreSuspendTransactionTrigger</span></span>       | <span data-ttu-id="62685-403">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-403">Cancelable</span></span>     | <span data-ttu-id="62685-404">トランザクションが中断する前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-404">Executed before the transaction is suspended.</span></span>   
| <span data-ttu-id="62685-405">PostSuspendTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-405">PostSuspendTransactionTrigger</span></span>      | <span data-ttu-id="62685-406">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-406">Non-cancelable</span></span> | <span data-ttu-id="62685-407">トランザクションが中断した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-407">Executed after the transaction is suspended.</span></span>    |
| <span data-ttu-id="62685-408">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-408">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="62685-409">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-409">Cancelable</span></span>     | <span data-ttu-id="62685-410">トランザクションまたは注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-410">Executed before the transaction or order is recalled.</span></span> |
| <span data-ttu-id="62685-411">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-411">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="62685-412">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-412">Non-cancelable</span></span> | <span data-ttu-id="62685-413">トランザクションまたは注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-413">Executed after the transaction or order is recalled.</span></span>  |
| <span data-ttu-id="62685-414">PostCartCheckoutTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-414">PostCartCheckoutTrigger</span></span>            | <span data-ttu-id="62685-415">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-415">Non-cancelable</span></span> | <span data-ttu-id="62685-416">チェックアウト プロセスの完了後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-416">Executed after the checkout process is completed.</span></span>     |
| <span data-ttu-id="62685-417">PreRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-417">PreRecallTransactionTrigger</span></span>        | <span data-ttu-id="62685-418">解約可能</span><span class="sxs-lookup"><span data-stu-id="62685-418">Cancelable</span></span>     | <span data-ttu-id="62685-419">顧客の注文がリコールされる前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-419">Executed before the customer order is recalled.</span></span>       |
| <span data-ttu-id="62685-420">PostRecallTransactionTrigger</span><span class="sxs-lookup"><span data-stu-id="62685-420">PostRecallTransactionTrigger</span></span>       | <span data-ttu-id="62685-421">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="62685-421">Non-Cancelable</span></span> | <span data-ttu-id="62685-422">顧客の注文がリコールされた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="62685-422">Executed after the customer order is recalled.</span></span>        |

## <a name="business-scenario"></a><span data-ttu-id="62685-423">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="62685-423">Business scenario</span></span>
<span data-ttu-id="62685-424">この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="62685-424">In this example, a custom receipt is printed when the user suspends a transaction.</span></span> <span data-ttu-id="62685-425">この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="62685-425">This example implements the **PostSuspendTransactionTrigger** trigger and prints the custom receipt using the existing print peripheral API.</span></span>

<span data-ttu-id="62685-426">このシナリオを実装するには、次の手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="62685-426">To implement this scenario, you must complete these steps.</span></span>

1. <span data-ttu-id="62685-427">**POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。</span><span class="sxs-lookup"><span data-stu-id="62685-427">**POS extension:** Implement the **PostSuspendTransactionTrigger** trigger to get the receipt data from CRT and send it to the printer for printing.</span></span> 
2. <span data-ttu-id="62685-428">**CRT 拡張:** 印刷対象の受領書データを生成します。</span><span class="sxs-lookup"><span data-stu-id="62685-428">**CRT extension:** Generate the receipt data for printing.</span></span>

## <a name="implement-a-trigger"></a><span data-ttu-id="62685-429">トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="62685-429">Implement a trigger</span></span>

1. <span data-ttu-id="62685-430">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="62685-430">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="62685-431">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="62685-431">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="62685-432">**POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="62685-432">Under the **POS.Extensions** project, create a new folder named **SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="62685-433">**SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="62685-433">Under **SuspendReceiptSample**, create new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="62685-434">**TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="62685-434">In the **TriggersHandlers** folder, add a new Typescript file named **PostSuspendTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="62685-435">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="62685-435">Add the following **import** statements to import the relevant entities and context.</span></span>
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
7. <span data-ttu-id="62685-436">**PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="62685-436">Create a new class named **PostSuspendTransactionTrigger** and extend it from **PostSuspendTransactionTrigger**.</span></span>
 
```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
```
8. <span data-ttu-id="62685-437">トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="62685-437">Implement the trigger's **execute** method to get the receipt profile and print the custom receipt:</span></span>
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
   <span data-ttu-id="62685-438">全体の例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="62685-438">The entire example should look like the following.</span></span>

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
9. <span data-ttu-id="62685-439">新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="62685-439">Create a new .json file under the **SuspendReceiptSample** folder and name it **manifest.json**.</span></span>
10. <span data-ttu-id="62685-440">**manifest.json** の自動生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="62685-440">Replace the autogenerated code in **manifest.json** with the following code.</span></span>

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
11. <span data-ttu-id="62685-441">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="62685-441">Open the **extensions.json** file in the **POS.Extensions** project and update it with the **SuspendReceiptSample** samples, so that during runtime POS will include this extension.</span></span>

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
12. <span data-ttu-id="62685-442">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="62685-442">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="62685-443">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="62685-443">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="62685-444">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="62685-444">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="62685-445">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62685-445">If you want to include an extension that is part of the POS, then add the extension folder name and comment out the extension from the extension, as shown.</span></span>

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
13. <span data-ttu-id="62685-446">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="62685-446">Compile and rebuild the project.</span></span>

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a><span data-ttu-id="62685-447">受領書データを生成するために CRT 受領要求を上書きする</span><span class="sxs-lookup"><span data-stu-id="62685-447">Override the CRT receipt request to generate the receipt data</span></span>

<span data-ttu-id="62685-448">このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="62685-448">This section explains how to override the existing CRT request to print a receipt for suspended transactions.</span></span> <span data-ttu-id="62685-449">このセクションでは、Microsoft Dynamics 365 for Finance and Operations または Microsoft Dynamics 365 for Retail プラットフォーム更新プログラム 8 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="62685-449">This section is applicable to Microsoft Dynamics 365 for Finance and Operations or Microsoft Dynamics 365 for Retail with platform update 8.</span></span>

1. <span data-ttu-id="62685-450">Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="62685-450">Start Visual Studio 2015.</span></span>
2. <span data-ttu-id="62685-451">**ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62685-451">On the **File** menu, select **Open \> Project/Solution**.</span></span> <span data-ttu-id="62685-452">テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。</span><span class="sxs-lookup"><span data-stu-id="62685-452">Find the template project (**SampleCRTExtension.csproj**).</span></span>
3. <span data-ttu-id="62685-453">テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="62685-453">Rename the template project **Runtime.Extensions.SuspendReceiptSample**.</span></span>
4. <span data-ttu-id="62685-454">オプション: 既定の名前空間を変更します。</span><span class="sxs-lookup"><span data-stu-id="62685-454">Optional: Change the default namespace.</span></span>
5. <span data-ttu-id="62685-455">出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。</span><span class="sxs-lookup"><span data-stu-id="62685-455">Rename the output assembly **Contoso.Commerce.Runtime.SuspendReceiptSample**.</span></span>
6. <span data-ttu-id="62685-456">プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="62685-456">Inside the project, add a new request class file, and name it **GetCustomReceiptsRequestHandler.cs**.</span></span>
7. <span data-ttu-id="62685-457">次のコードをコピーして、クラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="62685-457">Copy the following code, and paste it inside the class.</span></span> <span data-ttu-id="62685-458">コピーする前に、自動的に生成されたコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="62685-458">Before you copy it, delete the automatically generated code.</span></span>

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

8. <span data-ttu-id="62685-459">次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点では小売トランザクション テーブルに作成されていないためです。</span><span class="sxs-lookup"><span data-stu-id="62685-459">Copy the following code, and paste it inside the class to add a new method to read the transaction from the cart table, because suspended transactions aren't yet created in the retail transaction table.</span></span> <span data-ttu-id="62685-460">カート トランザクションを販売トランザクションに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62685-460">You must then convert the cart transaction to sales transaction.</span></span> <span data-ttu-id="62685-461">入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="62685-461">This conversion is required because the receipt object can understand only sales transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62685-462">完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="62685-462">If you're printing a custom receipt for a completed transaction, you have don't have to get the cart transaction and convert it to a sales transaction.</span></span> <span data-ttu-id="62685-463">トランザクションが完了したため、既に販売トランザクションに変換されました。</span><span class="sxs-lookup"><span data-stu-id="62685-463">It has already been converted to a sales transaction, because the transaction is completed.</span></span>

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

9. <span data-ttu-id="62685-464">次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="62685-464">Copy the following code, and paste it into the class to add a new method to construct the receipt format by using the sales transaction information, based on the custom receipt format that is defined in HQ.</span></span>

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

10. <span data-ttu-id="62685-465">次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="62685-465">Copy the following code, and paste it into the class to add a new method to override the get receipt response.</span></span> <span data-ttu-id="62685-466">この方法は、要求を処理し、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="62685-466">This method processes the request and returns the response.</span></span>

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

    <span data-ttu-id="62685-467">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="62685-467">The overall code should look like this.</span></span>

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

11. <span data-ttu-id="62685-468">プロジェクトをコンパイル、およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="62685-468">Compile and build the project.</span></span>
12. <span data-ttu-id="62685-469">出力ディレクトリに移動し、出力アセンブリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="62685-469">Go to the output directory, and copy the output assembly.</span></span>
13. <span data-ttu-id="62685-470">**…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="62685-470">Navigate to the **…\\RetailServer\\webroot\\bin\\ext** folder, and paste the assembly.</span></span>
14. <span data-ttu-id="62685-471">また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="62685-471">Also paste the assembly in the **…\\RetailSDK\\References** folder.</span></span>
15. <span data-ttu-id="62685-472">**commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="62685-472">Open the **commerceruntime.ext.config** file, and add the custom assembly information under the \<composition\> section.</span></span>

    ```
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. <span data-ttu-id="62685-473">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="62685-473">Save and close the file.</span></span>
17. <span data-ttu-id="62685-474">Retail サーバーを再起動して新しいアセンブリを読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="62685-474">Restart the Retail Server to load the new assembly.</span></span>

## <a name="add-the-custom-receipt-layout"></a><span data-ttu-id="62685-475">カスタム レシート レイアウトの追加</span><span class="sxs-lookup"><span data-stu-id="62685-475">Add the custom receipt layout</span></span>

1. <span data-ttu-id="62685-476">Dynamics 365 for Finance and Operations Enterprise Edition を開きます。</span><span class="sxs-lookup"><span data-stu-id="62685-476">Open Dynamics 365 for Finance and Operations, Enterpise edition.</span></span>
2. <span data-ttu-id="62685-477">**小売** > **チャンネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62685-477">Go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Receipts formats**.</span></span>
3. <span data-ttu-id="62685-478">**受領書フォーマット**内の**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-478">Click **New** in **Receipts formats**.</span></span>
4. <span data-ttu-id="62685-479">**提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。</span><span class="sxs-lookup"><span data-stu-id="62685-479">In the **Receipt format filed** field, enter the format name **Suspend**.</span></span> <span data-ttu-id="62685-480">**受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62685-480">In the **Receipt type** field, select **CustomReceiptType7**.</span></span>
5. <span data-ttu-id="62685-481">**デザイナー**をクリックし、入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="62685-481">Click **Designer** to open the receipt designer.</span></span>
6. <span data-ttu-id="62685-482">インストールするようメッセージが表示されたら、指示に従います。</span><span class="sxs-lookup"><span data-stu-id="62685-482">Follow the instructions if prompted to install.</span></span> <span data-ttu-id="62685-483">Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="62685-483">Enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
7. <span data-ttu-id="62685-484">必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。</span><span class="sxs-lookup"><span data-stu-id="62685-484">Drag and drop the required field into the header, lines, or footer.</span></span> <span data-ttu-id="62685-485">または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。</span><span class="sxs-lookup"><span data-stu-id="62685-485">Or, copy the from existing receipt format by using the copy feature and then edit it.</span></span>
8. <span data-ttu-id="62685-486">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-486">Click **Save**.</span></span>
9. <span data-ttu-id="62685-487">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **レシート プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62685-487">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Receipt profiles**.</span></span>
10. <span data-ttu-id="62685-488">**電子メール受信** プロファイルまたは保存するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="62685-488">Select the **Email receipt** profile or the that profile you store.</span></span> <span data-ttu-id="62685-489">**一般**タブの**追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-489">Click the **Add** button in the **General** tab.</span></span>
11. <span data-ttu-id="62685-490">**受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62685-490">In the **Receipt type**, select **CustomReceiptType7** and in the **Receipt format** select **Suspend**.</span></span>
12. <span data-ttu-id="62685-491">**小売 > 小売 IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62685-491">Go to **Retail > Retail IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="62685-492">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-492">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="62685-493">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="62685-493">When prompted, click **Yes** to run the job.</span></span> 

## <a name="configure-the-xps-printer-for-quick-testing"></a><span data-ttu-id="62685-494">クイック テスト用の XPS プリンタのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="62685-494">Configure the XPS printer for quick testing</span></span>

1. <span data-ttu-id="62685-495">**小売** > **チャンネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62685-495">Go to **Retail** > **Channel setup** > **POS setup** > **POS profiles** > **Hardware profiles**.</span></span>
2. <span data-ttu-id="62685-496">デバイスで使用しているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="62685-496">Select the hardware profile that your device is using.</span></span> <span data-ttu-id="62685-497">たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。</span><span class="sxs-lookup"><span data-stu-id="62685-497">For example, in the demo data all the Houston devices uses **HW002**.</span></span>
3. <span data-ttu-id="62685-498">操作バーの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-498">Click **Edit** in the action bar.</span></span>
4. <span data-ttu-id="62685-499">**プリンター** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="62685-499">Expand the **Printer** FastTab.</span></span> <span data-ttu-id="62685-500">**プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。</span><span class="sxs-lookup"><span data-stu-id="62685-500">In the **Printer** drop-down list, select **Windows driver** and in the device name field enter **Microsoft XPS Document Writer**.</span></span>
5. <span data-ttu-id="62685-501">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-501">Click **Save**.</span></span>
6. <span data-ttu-id="62685-502">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62685-502">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
7. <span data-ttu-id="62685-503">**レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62685-503">Select **Registers (1090)** and click **Run now** in the action bar.</span></span> <span data-ttu-id="62685-504">要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="62685-504">When prompted, click **Yes** to run the job.</span></span> 

## <a name="validate-the-extension"></a><span data-ttu-id="62685-505">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="62685-505">Validate the extension</span></span>

1. <span data-ttu-id="62685-506">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="62685-506">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="62685-507">POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="62685-507">After the POS starts, sign in to POS and add an item to a transaction.</span></span>
3. <span data-ttu-id="62685-508">トランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="62685-508">Suspend the transaction.</span></span>
4. <span data-ttu-id="62685-509">カスタム レシートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="62685-509">The custom receipt should print.</span></span>
