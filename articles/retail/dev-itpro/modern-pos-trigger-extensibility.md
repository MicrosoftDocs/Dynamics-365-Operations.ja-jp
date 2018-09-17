---
title: "Retail Modern POS (MPOS) およびクラウド POS のトリガー拡張機能"
description: "このトピックでは、Modern POS と Cloud POS のクライアント側のトリガー機能について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17751
ms.assetid: 6767d342-73e0-432b-a02f-ea8191464506
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 779376807af5294ddcd996934582d03ff57c0e7b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/17/2018

---

# <a name="retail-modern-pos-mpos-and-cloud-pos-trigger-extensibility"></a><span data-ttu-id="7401b-103">Retail Modern POS (MPOS) およびクラウド POS のトリガー拡張機能</span><span class="sxs-lookup"><span data-stu-id="7401b-103">Retail Modern POS (MPOS) and Cloud POS trigger extensibility</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7401b-104">このトピックは、Dynamics 365 for Finance and Operations の 7.1 およびそれ以降のバージョンに適用可能です。</span><span class="sxs-lookup"><span data-stu-id="7401b-104">This topic is applicable for Dynamics 365 for Finance and Operations version 7.1 and earlier.</span></span> <span data-ttu-id="7401b-105">バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7401b-105">This implementation is not supported for versions 7.2 and higher.</span></span> <span data-ttu-id="7401b-106">これらのバージョンでは、オーバーレイせずに拡張モデルに従います。</span><span class="sxs-lookup"><span data-stu-id="7401b-106">For those versions, follow the extension model without overlayering.</span></span>

<span data-ttu-id="7401b-107">このトピックでは、Modern POS と Cloud POS のクライアント側のトリガー機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7401b-107">This topic explains the client-side trigger functionality in Modern POS and Cloud POS.</span></span>

<a name="trigger-overview"></a><span data-ttu-id="7401b-108">トリガーの概要</span><span class="sxs-lookup"><span data-stu-id="7401b-108">Trigger overview</span></span>
----------------

<span data-ttu-id="7401b-109">トリガーは、Microsoft Dynamics 365 for Retail が Retail POS に対して発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="7401b-109">Triggers are events that are raised by Microsoft Dynamics 365 for Retail for Retail POS.</span></span> <span data-ttu-id="7401b-110">トリガーを使用すると、操作の前後にカスタム コードを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-110">Triggers let you insert custom code before or after operations.</span></span> <span data-ttu-id="7401b-111">トリガーには事前トリガーと事後トリガーの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="7401b-111">There are two kinds of triggers: pre-triggers and post-triggers.</span></span>

| <span data-ttu-id="7401b-112">プレトリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-112">Pre-triggers</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="7401b-113">ポスト トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-113">Post-triggers</span></span>                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7401b-114">操作を実行する前に、カスタム コードを挿入するためにプレトリガーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-114">Pre-triggers can be used to insert custom code before an operation is run.</span></span> <span data-ttu-id="7401b-115">たとえば、顧客が購買のクーポンを使用する場合、有効期限が切れておらず、以前に使用されていないクーポンを検証するカスタム コードを挿入するための事前トリガーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-115">For example, if a customer uses a coupon for a purchase, you can use a pre-trigger to insert custom code to validate that the coupon hasn't expired and hasn't previously been used.</span></span> | <span data-ttu-id="7401b-116">ポスト トリガーを使うと、完了した工程に応答するカスタム コードを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-116">Post-triggers can be used to insert custom code that responds to a completed operation.</span></span> <span data-ttu-id="7401b-117">たとえば、**CustomerAdd** 操作後に実行し、顧客の誕生日である場合は、レジ担当者が顧客の幸せな誕生日を祈るよう指示するコードを記述できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-117">For example, you can write code that runs after the **CustomerAdd** operation and prompts the cashier to wish the customer a happy birthday if it's the customer’s birthday.</span></span> |

### <a name="trigger-types"></a><span data-ttu-id="7401b-118">トリガーのタイプ</span><span class="sxs-lookup"><span data-stu-id="7401b-118">Trigger types</span></span>

<span data-ttu-id="7401b-119">Modern POS およびクラウド POS では、トリガーはキャンセル可能かキャンセル可能ではないかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="7401b-119">In Modern POS and Cloud POS, triggers are either cancelable or non-cancelable.</span></span>

| <span data-ttu-id="7401b-120">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-120">Cancelable</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="7401b-121">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-121">Non-cancelable</span></span>                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7401b-122">**ICancelableTriggerCancelable** トリガーを拡張するトリガー実装は、成功、失敗、または取り消しが可能です。</span><span class="sxs-lookup"><span data-stu-id="7401b-122">Trigger implementations that extend **ICancelableTriggerCancelable** triggers can succeed, fail, or be canceled.</span></span> <span data-ttu-id="7401b-123">ワークフローの実行は、エラーを表示せずにキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="7401b-123">Execution of the workflow is canceled without displaying an error.</span></span> <span data-ttu-id="7401b-124">たとえば、ユーザーが支払/入金のためにロイヤルティ ポイントを使用することを確認するトリガーです。</span><span class="sxs-lookup"><span data-stu-id="7401b-124">An example is a trigger to confirm that the user wants to use his or her loyalty points for tender.</span></span> <span data-ttu-id="7401b-125">ユーザーが**いいえ**と選択した場合、ユーザーにエラー メッセージが表示されずに、ロイヤルティ情報を入力するワークフローがキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="7401b-125">If the user selects **No**, the workflow to enter loyalty information is canceled without showing an error message to the user.</span></span> | <span data-ttu-id="7401b-126">**ITriggerNon-cancelable** トリガーを拡張するトリガー実装は、成功または失敗のいずれかが可能です。</span><span class="sxs-lookup"><span data-stu-id="7401b-126">Trigger implementations that extend **ITriggerNon-cancelable** triggers can either succeed or fail.</span></span> <span data-ttu-id="7401b-127">トリガーが成功した場合、ワークフローを続行します。</span><span class="sxs-lookup"><span data-stu-id="7401b-127">If the trigger succeeds, the workflow continues.</span></span> <span data-ttu-id="7401b-128">トリガーが失敗すると、UI にメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7401b-128">If the trigger fails, a message appears in the UI.</span></span> <span data-ttu-id="7401b-129">たとえば、販売および返品のために個別のトランザクションを作成するレジ担当者に対してガイドライン指示をすることによりスウェーデン語のローカライズ要件をサポートするトリガーです。</span><span class="sxs-lookup"><span data-stu-id="7401b-129">An example is a trigger to support Swedish localization requirements by guiding the cashier to create separate transactions for sales and returns.</span></span> |

### <a name="guidelines"></a><span data-ttu-id="7401b-130">ガイドライン</span><span class="sxs-lookup"><span data-stu-id="7401b-130">Guidelines</span></span>

-   <span data-ttu-id="7401b-131">**トリガーの登録** – すべてのトリガーは、**TriggerManager::register** メソッドを使用して登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7401b-131">**Trigger registration** – All triggers should be registered by using the **TriggerManager::register** method.</span></span> <span data-ttu-id="7401b-132">**ApplicationStart**、**PreLogOn**、および **PostLogOn** トリガーは、**DOMContentLoaded** イベントが発生したときに呼び出される関数内で登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7401b-132">The **ApplicationStart**, **PreLogOn**, and **PostLogOn** triggers must be registered inside a function that is called when the **DOMContentLoaded** event is raised.</span></span> <span data-ttu-id="7401b-133">他のトリガーは、同じ方法で登録することができますが、条件付きで登録することもできます。</span><span class="sxs-lookup"><span data-stu-id="7401b-133">Other triggers can be registered in the same manner, but they can also be registered conditionally.</span></span>
    -   <span data-ttu-id="7401b-134">**条件付き登録** - トリガーを登録するかどうかの決定がチャネル内の情報に基づいている場合、条件付きでトリガーを登録できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-134">**Conditional registration** – If the decision about whether to register a trigger is based on information in the channel, the trigger can be registered conditionally.</span></span> <span data-ttu-id="7401b-135">条件付きの登録を **PostLogOn** トリガー内で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7401b-135">Conditional registration should be performed inside a **PostLogOn** trigger.</span></span> <span data-ttu-id="7401b-136">**注記:** 条件付きの登録は、アプリケーションの読み込み後最初のサインイン時にのみ実行することが重要です。</span><span class="sxs-lookup"><span data-stu-id="7401b-136">**Note:** It's important that the conditional registration be performed only during the first sign-in after the app has been loaded.</span></span> <span data-ttu-id="7401b-137">実装例については、この記事の後半のサンプル コードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7401b-137">For an example implementation, see the sample code later in this article.</span></span>
-   <span data-ttu-id="7401b-138">**トリガーの実装** – 「サポートされているトリガー イベント」セクションに一覧表示されている各トリガー イベントには、関連付けられているトリガー インターフェイスがあります。</span><span class="sxs-lookup"><span data-stu-id="7401b-138">**Trigger implementation** – Each trigger event that is listed in the "Supported trigger events" section has a trigger interface that is associated with it.</span></span> <span data-ttu-id="7401b-139">これらのトリガー インターフェイスは、アプリケーションとトリガー実装との間の契約を定義します。</span><span class="sxs-lookup"><span data-stu-id="7401b-139">These trigger interfaces define the contract between the application and the trigger implementations.</span></span> <span data-ttu-id="7401b-140">各トリガーは、登録されているトリガー イベント タイプに関連付けられている定義済みインターフェースを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7401b-140">Each trigger should implement the predefined interface that is associated with the trigger event type that it's registered for.</span></span>

### <a name="triggers-execution-workflow"></a><span data-ttu-id="7401b-141">トリガー実行ワークフロー</span><span class="sxs-lookup"><span data-stu-id="7401b-141">Triggers execution workflow</span></span>

<span data-ttu-id="7401b-142">次の図は、**ItemSaleOperation** ワークフロー/操作のプリトリガーとポストトリガーの実行ワークフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="7401b-142">The following diagram shows the execution workflow for both pre-triggers and post-triggers for the **ItemSaleOperation** workflow/operation.</span></span> 

<span data-ttu-id="7401b-143">[![トリガー実行フロー](./media/trigger-execution-flow.png)](./media/trigger-execution-flow.png)</span><span class="sxs-lookup"><span data-stu-id="7401b-143">[![Trigger Execution Flow](./media/trigger-execution-flow.png)](./media/trigger-execution-flow.png)</span></span>

### <a name="supported-trigger-events"></a><span data-ttu-id="7401b-144">サポートされているトリガー イベント</span><span class="sxs-lookup"><span data-stu-id="7401b-144">Supported trigger events</span></span>

<span data-ttu-id="7401b-145">すべての操作でトリガーされる操作前後のトリガーとともに、次のトリガーがそのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="7401b-145">Together with pre-operation and post-operation triggers that are triggered for every operation, the following triggers are supported out of the box:</span></span>

-   <span data-ttu-id="7401b-146">アプリケーション トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-146">Application triggers</span></span>
    -   <span data-ttu-id="7401b-147">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-147">Cancelable</span></span>
        -   <span data-ttu-id="7401b-148">**PreLogOn** – Modern POS にサインインする前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-148">**PreLogOn** – Called before sign-in to Modern POS</span></span>
            -   <span data-ttu-id="7401b-149">operatorId</span><span class="sxs-lookup"><span data-stu-id="7401b-149">operatorId</span></span>
    -   <span data-ttu-id="7401b-150">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-150">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-151">**ApplicationStart** - アプリケーションの起動時に呼び出される</span><span class="sxs-lookup"><span data-stu-id="7401b-151">**ApplicationStart** – Called when the application is launched</span></span>
        -   <span data-ttu-id="7401b-152">**ApplicationSuspend** - アプリケーションが中断されたときに呼び出される</span><span class="sxs-lookup"><span data-stu-id="7401b-152">**ApplicationSuspend** – Called when the application is suspended</span></span>
        -   <span data-ttu-id="7401b-153">**PostLogOff** – サインアウトの操作が完了した後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-153">**PostLogOff** – Called after the sign-out operation is completed</span></span>
        -   <span data-ttu-id="7401b-154">**PostLogOn** – サインインの操作が完了した後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-154">**PostLogOn** – Called after the sign-in operation is completed</span></span>
-   <span data-ttu-id="7401b-155">現金管理トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-155">Cash management triggers</span></span>
    -   <span data-ttu-id="7401b-156">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-156">Cancelable</span></span>
        -   <span data-ttu-id="7401b-157">**PreTenderDeclaration** – 支払/入金申告操作が実行される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-157">**PreTenderDeclaration** – Called before the tender declaration operation is run</span></span>
    -   <span data-ttu-id="7401b-158">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-158">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-159">**PostTenderDeclaration** – 支払/入金申告ワークフローの最後のステップとして呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-159">**PostTenderDeclaration** – Called as the last step in the tender declaration workflow</span></span>
-   <span data-ttu-id="7401b-160">顧客トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-160">Customer triggers</span></span>
    -   <span data-ttu-id="7401b-161">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-161">Cancelable</span></span>
        -   <span data-ttu-id="7401b-162">**PreCustomerAdd** – 新しい顧客が作成される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-162">**PreCustomerAdd** – Called before a new customer is created</span></span>
        -   <span data-ttu-id="7401b-163">**PreCustomerClear** – 顧客が現在のトランザクションから消去される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-163">**PreCustomerClear** – Called before the customer is cleared from the current transaction</span></span>
        -   <span data-ttu-id="7401b-164">**PreCustomerSearch** – 顧客の検索前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-164">**PreCustomerSearch** – Called before a search for a customer</span></span>
        -   <span data-ttu-id="7401b-165">**PreCustomerSet** – 顧客がトランザクションを開始する前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-165">**PreCustomerSet** – Called before the customer is set on the transaction</span></span>
    -   <span data-ttu-id="7401b-166">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-166">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-167">**PostCustomerAdd** – 新しい顧客が作成された後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-167">**PostCustomerAdd** – Called after a new customer is created</span></span>
        -   <span data-ttu-id="7401b-168">**PostCustomerClear** – 顧客がトランザクションから消去された後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-168">**PostCustomerClear** – Called after the customer is cleared from the transaction</span></span>
        -   <span data-ttu-id="7401b-169">**PostCustomerSearch** – 顧客の検索後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-169">**PostCustomerSearch** – Called after a search for a customer</span></span>
-   <span data-ttu-id="7401b-170">割引のトリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-170">Discount triggers</span></span>
    -   <span data-ttu-id="7401b-171">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-171">Cancelable</span></span>
        -   <span data-ttu-id="7401b-172">**PreLineDiscountAmount** – 検証によって割引が適用可能かどうかが判断された後、行割引金額操作中に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-172">**PreLineDiscountAmount** – Called during the line discount amount operation, after validation determines whether a discount can be applied</span></span>
        -   <span data-ttu-id="7401b-173">**PreLineDiscountPercent** – 検証によって割引が適用可能かどうかが判断された後、行割引率操作中に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-173">**PreLineDiscountPercent** – Called during the line discount percent operation, after validation determines whether a discount can be applied</span></span>
        -   <span data-ttu-id="7401b-174">**PreTotalDiscountAmount** – 検証によって割引が適用可能かどうかが判断された後、合計割引金額操作中に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-174">**PreTotalDiscountAmount** – Called during the total discount amount operation, after validation determines whether a discount can be applied</span></span>
        -   <span data-ttu-id="7401b-175">**PreTotalDiscountPercent** – 検証によって割引が適用可能かどうかが判断された後、割引金額率操作中に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-175">**PreTotalDiscountPercent** – Called during the total discount percent operation, after validation determines whether a discount can be applied</span></span>
    -   <span data-ttu-id="7401b-176">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-176">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-177">**PostLineDiscountAmount** - 行割引金額のワークフローの最後のステップとして呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-177">**PostLineDiscountAmount** - Called as the last step in the line discount amount workflow</span></span>
        -   <span data-ttu-id="7401b-178">**PostLineDiscountPercent** – 行割引率のワークフローの最後のステップとして呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-178">**PostLineDiscountPercent** – Called as the last step in the line discount percent workflow</span></span>
        -   <span data-ttu-id="7401b-179">**PostTotalDiscountAmount** – 合計割引金額のワークフローの最後のステップとして呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-179">**PostTotalDiscountAmount** – Called as the last step in the total discount amount workflow</span></span>
        -   <span data-ttu-id="7401b-180">**PostTotalDiscountPercent** – 合計割引率のワークフローの最後のステップとして呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-180">**PostTotalDiscountPercent** – Called as the last step in the total discount percent workflow</span></span>
-   <span data-ttu-id="7401b-181">工程のトリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-181">Operation triggers</span></span>
    -   <span data-ttu-id="7401b-182">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-182">Cancelable</span></span>
        -   <span data-ttu-id="7401b-183">**PreOperation** – 毎回の操作を実行する前、プリハンドラーおよび操作検証の前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-183">**PreOperation** – Called before every operation is run, before the prehandler and operation validators</span></span>
    -   <span data-ttu-id="7401b-184">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-184">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-185">**OperationFailure** – 操作が失敗したときに呼び出され、復旧アクションを実行するために使用できます</span><span class="sxs-lookup"><span data-stu-id="7401b-185">**OperationFailure** – Called when an operation fails, and can be used to perform recovery actions</span></span>
        -   <span data-ttu-id="7401b-186">**PostOperation** – 操作が正常に終了したときに呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-186">**PostOperation** – Called when an operation is completed successfully</span></span>
-   <span data-ttu-id="7401b-187">支払トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-187">Payment triggers</span></span>
    -   <span data-ttu-id="7401b-188">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-188">Cancelable</span></span>
        -   <span data-ttu-id="7401b-189">**PreAddTenderLine** – 支払/入金の明細行がトランザクションに追加される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-189">**PreAddTenderLine** – Called before a tender line is added to the transaction</span></span>
        -   <span data-ttu-id="7401b-190">**PrePayment** – 支払操作が開始される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-190">**PrePayment** – Called before any payment operation is started</span></span>
        -   <span data-ttu-id="7401b-191">**PreVoidPayment** – 支払の無効化操作が開始される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-191">**PreVoidPayment** – Called before the void payment operation is started</span></span>
    -   <span data-ttu-id="7401b-192">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-192">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-193">**PostPayment** – 支払が追加された後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-193">**PostPayment** – Called after the payment has been added</span></span>
        -   <span data-ttu-id="7401b-194">**PostVoidPayment** – 支払が無効にされた後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-194">**PostVoidPayment** – Called after the payment has been voided</span></span>
-   <span data-ttu-id="7401b-195">印刷トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-195">Printing triggers</span></span>
    -   <span data-ttu-id="7401b-196">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-196">Cancelable</span></span>
        -   <span data-ttu-id="7401b-197">**PrePrintReceiptCopy** – レシートのコピーが印刷される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-197">**PrePrintReceiptCopy** – Called before a copy of the receipt is printed</span></span>
-   <span data-ttu-id="7401b-198">製品トリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-198">Product Triggers</span></span>
    -   <span data-ttu-id="7401b-199">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-199">Cancelable</span></span>
        -   <span data-ttu-id="7401b-200">**PreClearQuantity** – 数量のクリア操作前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-200">**PreClearQuantity** – Called before the clear quantity operation</span></span>
        -   <span data-ttu-id="7401b-201">**PrePriceOverride** – 価格上書き操作前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-201">**PrePriceOverride** – Called before the price override operation</span></span>
        -   <span data-ttu-id="7401b-202">**PreProductSale** – 品目販売操作前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-202">**PreProductSale** – Called before the item sale operation</span></span>
        -   <span data-ttu-id="7401b-203">**PreReturnProduct** – 返品操作前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-203">**PreReturnProduct** – Called before the return product operation</span></span>
        -   <span data-ttu-id="7401b-204">**PreSetQuantity** – 数量の設定操作前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-204">**PreSetQuantity** – Called before the set quantity operation</span></span>
        -   <span data-ttu-id="7401b-205">**PreVoidProducts** – ユーザーがトランザクションを無効化することを確認した後、トランザクションが無効化される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-205">**PreVoidProducts** – Called after the user confirms that he or she wants to void the transaction, but before the transaction is voided</span></span>
    -   <span data-ttu-id="7401b-206">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-206">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-207">**PostClearQuantity** – 数量のクリア操作後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-207">**PostClearQuantity** – Called after the clear quantity operation</span></span>
        -   <span data-ttu-id="7401b-208">**PostPriceOverride** – 価格上書き操作後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-208">**PostPriceOverride** – Called after the price override operation</span></span>
        -   <span data-ttu-id="7401b-209">**PostProductSale** – 品目販売操作後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-209">**PostProductSale** – Called after the item sale operation</span></span>
        -   <span data-ttu-id="7401b-210">**PostReturnProduct** – 返品操作後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-210">**PostReturnProduct** – Called after the return product operation</span></span>
        -   <span data-ttu-id="7401b-211">**PostSetQuantity** – 数量の設定操作後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-211">**PostSetQuantity** – Called after the set quantity operation</span></span>
        -   <span data-ttu-id="7401b-212">**PostVoidProducts** – 製品の無効化操作後に呼び出される</span><span class="sxs-lookup"><span data-stu-id="7401b-212">**PostVoidProducts** – Called after the void products operation</span></span>
-   <span data-ttu-id="7401b-213">トランザクションのトリガー</span><span class="sxs-lookup"><span data-stu-id="7401b-213">Transaction triggers</span></span>
    -   <span data-ttu-id="7401b-214">解約可能</span><span class="sxs-lookup"><span data-stu-id="7401b-214">Cancelable</span></span>
        -   <span data-ttu-id="7401b-215">**PreConfirmReturnTransaction** – 返品するトランザクションを検索した後に呼び出されますが、カート明細行が返品可能と表示される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-215">**PreConfirmReturnTransaction** – Called after a search for a transaction to return, but before the cart lines appear as available for return</span></span>
        -   <span data-ttu-id="7401b-216">**PreEndTransaction** – 販売トランザクションが完了する前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-216">**PreEndTransaction** – Called before a sales transaction is completed</span></span>
        -   <span data-ttu-id="7401b-217">**PreRecallTransaction** – トランザクションが取り消される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-217">**PreRecallTransaction** – Called before a transaction is recalled</span></span>
        -   <span data-ttu-id="7401b-218">**PreReturnTransaction** – トランザクションが戻される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-218">**PreReturnTransaction** – Called before a transaction is returned</span></span>
        -   <span data-ttu-id="7401b-219">**PreSuspendTransaction** – トランザクションが中断される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-219">**PreSuspendTransaction** – Called before a transaction is suspended</span></span>
        -   <span data-ttu-id="7401b-220">**PreVoidTransaction** – トランザクションが無効化される前に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-220">**PreVoidTransaction** – Called before a transaction is voided</span></span>
    -   <span data-ttu-id="7401b-221">キャンセル不可</span><span class="sxs-lookup"><span data-stu-id="7401b-221">Non-cancelable</span></span>
        -   <span data-ttu-id="7401b-222">**BeginTransaction** - カートが作成され、トランザクションが開始される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7401b-222">**BeginTransaction** – Called before a cart is created and a transaction is started</span></span>
        -   <span data-ttu-id="7401b-223">**PostEndTransaction** – 販売トランザクションが完了した後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-223">**PostEndTransaction** – Called after a sales transaction is completed</span></span>
        -   <span data-ttu-id="7401b-224">**PostRecallTransaction** – トランザクションが取り消された後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-224">**PostRecallTransaction** – Called after a transaction is recalled</span></span>
        -   <span data-ttu-id="7401b-225">**PostReturnTransaction** – 返品のためにトランザクションの品目がカートに追加された後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-225">**PostReturnTransaction** – Called after items from a transaction are added to the cart for return</span></span>
        -   <span data-ttu-id="7401b-226">**PostSuspendTransaction** – トランザクションを中断した後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-226">**PostSuspendTransaction** – Called after suspending a transaction</span></span>
        -   <span data-ttu-id="7401b-227">**PostVoidTransaction** – トランザクションが無効化された後に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="7401b-227">**PostVoidTransaction** – Called after a transaction is voided</span></span>

## <a name="trigger-example-implementation"></a><span data-ttu-id="7401b-228">トリガー実装の例</span><span class="sxs-lookup"><span data-stu-id="7401b-228">Trigger example implementation</span></span>
<span data-ttu-id="7401b-229">トリガーを理解する最善の方法は、サンプルの実装シナリオを調べることです。</span><span class="sxs-lookup"><span data-stu-id="7401b-229">The best way to understand triggers is to look at a sample implementation scenario.</span></span>

### <a name="modern-poscloud-pos-changes-to-support-swedish-localization-requirements-by-using-pos-triggers"></a><span data-ttu-id="7401b-230">POS トリガーを使用したスウェーデン ローカライズ要件をサポートするための Modern POS/クラウド POS の変更</span><span class="sxs-lookup"><span data-stu-id="7401b-230">Modern POS/Cloud POS changes to support Swedish localization requirements by using POS triggers</span></span>

<span data-ttu-id="7401b-231">会計帳簿が接続されている場合、取引は返品と販売の両方の操作を行うことができません。</span><span class="sxs-lookup"><span data-stu-id="7401b-231">Transactions can't have both return and sale operations if a fiscal register is connected.</span></span> <span data-ttu-id="7401b-232">**IPreProductSaleTrigger** トリガーはこの状況が発生した場合にこれを検出するように実装されまたキャッシャーに確認するメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="7401b-232">An **IPreProductSaleTrigger** trigger is implemented to detect this situation if it occurs and to show a message to prompt the cashier.</span></span> <span data-ttu-id="7401b-233">これは、スウェーデンの要件です。</span><span class="sxs-lookup"><span data-stu-id="7401b-233">This is a requirement in Sweden.</span></span>

1.  <span data-ttu-id="7401b-234">**IPreProductSaleTrigger** トリガーを実装して状況を検出し、レジ担当者に確認するメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="7401b-234">Implement an **IPreProductSaleTrigger** trigger to detect the situation and show a message to prompt the cashier.</span></span>
2.  <span data-ttu-id="7401b-235">実装クラス内の **実行** メソッドにトリガー ビジネス ロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="7401b-235">Write trigger business logic in the **Execute** method in the implementation class.</span></span>
3.  <span data-ttu-id="7401b-236">**DOMContentLoad** イベントで **PostLogonTrigger** 実装の一部としてトリガーを登録します。</span><span class="sxs-lookup"><span data-stu-id="7401b-236">Register the trigger as part of the **PostLogonTrigger** implementation on the **DOMContentLoad** event.</span></span> 

<span data-ttu-id="7401b-237">[![Trigger01](./media/trigger01.png)](./media/trigger01.png)</span><span class="sxs-lookup"><span data-stu-id="7401b-237">[![Trigger01](./media/trigger01.png)](./media/trigger01.png)</span></span>

<span data-ttu-id="7401b-238">**目的:** 最新の POS / Cloud POS を、会計登録に接続されているときに、スウェーデン語のローカライズ要件を実装して同じトランザクションに売却と返品の両方の行が含まれないようにカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="7401b-238">**Purpose:** To customize Modern POS/Cloud POS to implement the Swedish localization requirement that the same transaction not include both sale and return lines when a fiscal register is connected.</span></span> <span data-ttu-id="7401b-239">Modern POS プロジェクトを開き、トリガーの実装を追加するために新しい TypeScript (.ts) ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="7401b-239">Open a Modern POS project, and add a new TypeScript (.ts) file to add the trigger implementation.</span></span> <span data-ttu-id="7401b-240">弊社のカスタマイズを製品コードから切り離してアップグレードを管理しやすくするために、カスタマイズ用の新しい TypeScript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7401b-240">We are creating a new TypeScript file for our customization to keep our customization separate from the product code and make upgrades easier to manage.</span></span>

1.  <span data-ttu-id="7401b-241">管理者として Microsoft Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="7401b-241">Start Microsoft Visual Studio 2015 as an administrator.</span></span>
2.  <span data-ttu-id="7401b-242">Modern POS ソリューションを、Retail SDK ディレクトリから開く:</span><span class="sxs-lookup"><span data-stu-id="7401b-242">Open the Modern POS solution from the Retail SDK directory:</span></span>
    -   <span data-ttu-id="7401b-243">クラウド ホストしているコンピュータを使用している場合、パスは I:/RetailSDK になります。</span><span class="sxs-lookup"><span data-stu-id="7401b-243">If you're using a cloud-hosted computer, the path is I:/RetailSDK.</span></span>
    -   <span data-ttu-id="7401b-244">ローカルにダウンロードしたマシンを使用している場合は、パスは C:\\Microsoft Dynamics AX\\70\\Retail SDK です。</span><span class="sxs-lookup"><span data-stu-id="7401b-244">If you're using a locally downloaded machine, the path is C:\\Microsoft Dynamics AX\\70\\Retail SDK.</span></span>

3.  <span data-ttu-id="7401b-245">POS.Core\\Triggers\\ に、**TriggerSample.ts** という名前の新しい TypeScript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7401b-245">In POS.Core\\Triggers\\, create a new TypeScript file that is named **TriggerSample.ts**.</span></span> 

<span data-ttu-id="7401b-246">[![Trigger02](./media/trigger02-1024x411.png)](./media/trigger02.png)</span><span class="sxs-lookup"><span data-stu-id="7401b-246">[![Trigger02](./media/trigger02-1024x411.png)](./media/trigger02.png)</span></span>

4.  <span data-ttu-id="7401b-247">TriggerSample.ts ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="7401b-247">Add the following code to the TriggerSample.ts file.</span></span>

        ///<reference path="ITrigger.ts" />
        ///<reference path="ApplicationTriggers.ts" />
        ///<reference path="TransactionTriggers.ts" />
        module Commerce.Triggers.Samples {
            "use strict";
            /**
             * Implementation of a pre product sale trigger that is used to ensure there are no return lines in the cart.
             */
            export class ValidateProductSalePreProductSaleTrigger implements IPreProductSaleTrigger {
                private static SALE_NOT_ALLOWED_IN_SAME_TRANSACTION_AS_RETURN_ERROR_CODE: string = "Return and sale not allowed in same transaction";
                /**
                 * Executes the trigger.
                 */
                public execute(options: Operations.IItemSaleOperationOptions): IAsyncResult<ICancelableResult> {
                    var hasReturnLine: boolean = Session.instance.cart.CartLines.some((cartLine: Proxy.Entities.CartLine): boolean => {
                        return cartLine.Quantity < 0 && !cartLine.IsVoided;
                    });
                    var result: AsyncResult<ICancelableResult> = new AsyncResult<ICancelableResult>(null);
                    if (hasReturnLine) {
                        var error: Proxy.Entities.Error =
                            new Proxy.Entities.Error(ValidateProductSalePreProductSaleTrigger.SALE_NOT_ALLOWED_IN_SAME_TRANSACTION_AS_RETURN_ERROR_CODE);
                        result.reject([error]);
                    } else {
                        result.resolve({ canceled: false });
                    }
                    return result;
                }
            }
            /**
             * Implementation of a post log on trigger that is used to perform conidtional registration of other triggers.
             */
            export class ConditionalRegistrationPostLogOnTrigger implements IPostLogOnTrigger {
                private static alreadyRegistered: boolean = false;
                /**
                 * Executes the trigger.
                 */
                public execute(options: IPostLogOnTriggerOptions): IVoidAsyncResult {
                    // Check to ensure the triggers have not already been registered.
                    if (!ConditionalRegistrationPostLogOnTrigger.alreadyRegistered) {
                        this.performRegistration();
                        // Set already registered field to true to prevent duplicate trigger registration.
                        ConditionalRegistrationPostLogOnTrigger.alreadyRegistered = true;
                    }
                    return VoidAsyncResult.createResolved();
                }
                /**
                 * Perform the conditional registration of triggers.
                 */
                private performRegistration(): void {
                    var conditionIsMet: boolean = true;
                    if (conditionIsMet) {              
                        TriggerManager.instance.register(
                            CancelableTriggerType.PreProductSale,
                            new ValidateProductSalePreProductSaleTrigger());
                    }
                }
            }
        }
        /**
         * Trigger types that do not support conditional registration should be registered when the DOMContentLoaded event is fired.
         * @remarks These trigger types include: ApplicationStart, PreLogOn and PostLogOn.
         */
        document.addEventListener("DOMContentLoaded", function (): void {
            Commerce.Triggers.TriggerManager.instance.register(
                Commerce.Triggers.NonCancelableTriggerType.PostLogOn,
                new Commerce.Triggers.Samples.ConditionalRegistrationPostLogOnTrigger());
        });

5.  <span data-ttu-id="7401b-248">TriggerSample.ts ファイルを検査して **IPreProductSaleTrigger** の実装を確認します。</span><span class="sxs-lookup"><span data-stu-id="7401b-248">Inspect the TriggerSample.ts file to see the implementation of **IPreProductSaleTrigger**.</span></span>

        export class ValidateProductSalePreProductSaleTrigger implements IPreProductSaleTrigger {
            private static SALE_NOT_ALLOWED_IN_SAME_TRANSACTION_AS_RETURN_ERROR_CODE: string = "Return and sale not allowed in same transaction";       
            /**
            * Executes the trigger.
            */
            public execute(options: Operations.IItemSaleOperationOptions): IAsyncResult<ICancelableResult> {
                var hasReturnLine: boolean = Session.instance.cart.CartLines.some((cartLine: Proxy.Entities.CartLine): boolean => {
                    return cartLine.Quantity < 0 && !cartLine.IsVoided;
                });
                var result: AsyncResult<ICancelableResult> = new AsyncResult<ICancelableResult>(null);
                if (hasReturnLine) {
                    var error: Proxy.Entities.Error =
                    new Proxy.Entities.Error(ValidateProductSalePreProductSaleTrigger.SALE_NOT_ALLOWED_IN_SAME_TRANSACTION_AS_RETURN_ERROR_CODE);
                    result.reject([error]);
                } else {
                    result.resolve({ canceled: false });
                }
                return result;
            }    
        }

6.  <span data-ttu-id="7401b-249">**ValidateProductSalePreProductSaleTrigger** の登録を検査します。</span><span class="sxs-lookup"><span data-stu-id="7401b-249">Inspect the registration of **ValidateProductSalePreProductSaleTrigger**.</span></span>

        /**
        * Implementation of a post log on trigger that is used to perform conidtional registration of other triggers.
        */
        export class ConditionalRegistrationPostLogOnTrigger implements IPostLogOnTrigger {
            private static alreadyRegistered: boolean = false;
            /**
            * Executes the trigger.
            */
            public execute(options: IPostLogOnTriggerOptions): IVoidAsyncResult {
                // Check to ensure the triggers have not already been registered.
                if (!ConditionalRegistrationPostLogOnTrigger.alreadyRegistered) {
                    this.performRegistration();
                // Set already registered field to true to prevent duplicate trigger registration.
                ConditionalRegistrationPostLogOnTrigger.alreadyRegistered = true;
            }
            return VoidAsyncResult.createResolved();
        }

7.  <span data-ttu-id="7401b-250">トリガーが登録されている **performRegistration** メソッドを検査します。</span><span class="sxs-lookup"><span data-stu-id="7401b-250">Inspect the **performRegistration** method where the trigger is registered.</span></span>

        private performRegistration(): void {
            var conditionIsMet: boolean = true;
            if (conditionIsMet) {
                //TriggerManager.instance.register(
                //    CancelableTriggerType.PreConfirmReturnTransaction,
                //    new ValidateReturnPreConfirmReturnTransactionTrigger());
                TriggerManager.instance.register(
                    CancelableTriggerType.PreProductSale,
                    new ValidateProductSalePreProductSaleTrigger());
                //TriggerManager.instance.register(
                //    NonCancelableTriggerType.PostCustomerAdd,
                //    new GiveBirthDayDiscountTrigger());
        }

8.  <span data-ttu-id="7401b-251">**DOMContentLoad** イベントで **PostLogonTrigger** の登録を検査します。</span><span class="sxs-lookup"><span data-stu-id="7401b-251">Inspect the registration of **PostLogonTrigger** on the **DOMContentLoad** event.</span></span>

        /**
        * Trigger types that do not support conditional registration should be registered when the DOMContentLoaded event is fired.
        * @remarks These trigger types include: ApplicationStart, PreLogOn and PostLogOn.
        */
        document.addEventListener("DOMContentLoaded", function (): void {
            Commerce.Triggers.TriggerManager.instance.register(
            Commerce.Triggers.NonCancelableTriggerType.PostLogOn,
            new Commerce.Triggers.Samples.ConditionalRegistrationPostLogOnTrigger());
        });

9.  <span data-ttu-id="7401b-252">実装を確認するため Modern POS をコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="7401b-252">Compile and rebuild Modern POS to verify the implementation:</span></span>
    1.  <span data-ttu-id="7401b-253">**仕訳帳の表示**に移動し、返すトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7401b-253">Go to **Show Journal**, and select a transaction to return.</span></span> <span data-ttu-id="7401b-254">トランザクションに複数の明細行がある場合は、1 つの行を返します。</span><span class="sxs-lookup"><span data-stu-id="7401b-254">If the transaction has multiple lines, return one line.</span></span> <span data-ttu-id="7401b-255">返品明細行は、カートに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7401b-255">A return line should be added in the cart.</span></span>
    2.  <span data-ttu-id="7401b-256">左のナビゲーション ウィンドウで、製品検索 (検索アイコン) を使用して、「シャツ」のテキストを検索します。</span><span class="sxs-lookup"><span data-stu-id="7401b-256">In the left navigation pane, use product search (the search icon) to search for the text "shirt."</span></span>
    3.  <span data-ttu-id="7401b-257">シャツ製品のいずれかを選択し、アプリケーション バーで、**今すぐ売る** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7401b-257">Select one of the shirt products, and then, on the app bar, click **Sell now**.</span></span>
    4.  <span data-ttu-id="7401b-258">**IPreProductSaleTrigger** トリガーを実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7401b-258">Observe that **IPreProductSaleTrigger** trigger is run.</span></span> <span data-ttu-id="7401b-259">同じトランザクションの販売および返品が実行できないことを示すメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="7401b-259">You should receive a message that states that you can't perform a sale and a return in same transaction.</span></span>






