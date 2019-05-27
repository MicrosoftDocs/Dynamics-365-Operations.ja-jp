---
title: トリガーを使用して返品ポリシーを実装してください
description: このトピックでは、トリガーを使用して新しいポリシーを実装する方法の例を 2 つ示しています。
author: mugunthanm
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 65863
ms.assetid: 539105e2-097d-4723-84a1-8084c2c32652
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 24a4f98a3675057b03592653cc5e9ad74ebeaf6c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537521"
---
# <a name="implement-a-return-policy-by-using-triggers"></a><span data-ttu-id="613af-103">トリガーを使用して返品ポリシーを実装してください</span><span class="sxs-lookup"><span data-stu-id="613af-103">Implement a return policy by using triggers</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="613af-104">このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="613af-104">This topic is applicable for Dynamics 365 for Finance and Operations version 7.1 and earlier.</span></span> <span data-ttu-id="613af-105">バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="613af-105">This implementation is not supported for versions 7.2 and higher.</span></span> <span data-ttu-id="613af-106">これらのバージョンでは、オーバーレイせずに拡張モデルに従います。</span><span class="sxs-lookup"><span data-stu-id="613af-106">For those versions, follow the extension model without overlayering.</span></span>

<span data-ttu-id="613af-107">このトピックでは、トリガーを使用して新しいポリシーを実装する方法の例を 2 つ示しています。</span><span class="sxs-lookup"><span data-stu-id="613af-107">This topic has two examples that show how you can implement a new policy using a trigger.</span></span>

<span data-ttu-id="613af-108">このトピックの例では、新しい返品ポリシーがあることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="613af-108">The examples in this topic assume that you have a new return policy.</span></span> <span data-ttu-id="613af-109">返品の最長期間は 30 日間で、購入日から 30 日を超えて返品することはできません。</span><span class="sxs-lookup"><span data-stu-id="613af-109">The maximum time period for returning an item is 30 days and no item may be returned more than 30 days after the date of purchase.</span></span> <span data-ttu-id="613af-110">また、レジ担当者またはマネージャーは、1 回のトランザクションで 3 つ以上の品目を無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="613af-110">Additionally, the cashier or manager is not allowed to void more than three items in a single transaction.</span></span>

## <a name="extend-the-mpos-trigger"></a><span data-ttu-id="613af-111">MPOS トリガーを拡張</span><span class="sxs-lookup"><span data-stu-id="613af-111">Extend the MPOS trigger</span></span>
1.  <span data-ttu-id="613af-112">Visual Studio を管理者としてオープンします。</span><span class="sxs-lookup"><span data-stu-id="613af-112">Open Visual Studio as an administrator.</span></span>
2.  <span data-ttu-id="613af-113">Modern POS ソリューションを K:\\RainMainStab\\7.0.1265.3014\\小売\\サービス\\RetailSDK\\コード\\POS から開きます。</span><span class="sxs-lookup"><span data-stu-id="613af-113">Open the Modern POS solution from K:\\RainMainStab\\7.0.1265.3014\\retail\\Services\\RetailSDK\\Code\\POS.</span></span>
3.  <span data-ttu-id="613af-114">**トリガー** フォルダーの下の POS.Core プロジェクトに新しい TypeScript ファイルを追加し、ExtensionTrigger.ts という名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="613af-114">Add new a TypeScript file in the POS.Core project, under the **Triggers** folder, and name it ExtensionTrigger.ts.</span></span>
4.  <span data-ttu-id="613af-115">トリガー インターフェイスへの参照を追加し、コードの新しいモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="613af-115">Add reference to the triggers interface and create a new module for the code.</span></span> <span data-ttu-id="613af-116">ExtensionTrigger.ts ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="613af-116">In the ExtensionTrigger.ts file, add the following code.</span></span>

        <///<reference path="TransactionTriggers.ts" />
        ///<reference path="TriggerHelper.ts" />
        ///<reference path="TriggerManager.ts" />
        ///<reference path="ApplicationTriggers.ts" />
        ///<reference path="ProductTriggers.ts" />
        ///<reference path="../IAsyncResult.ts" />
        ///<reference path="../Entities/CommerceTypes.g.ts" />
        ///<reference path='ITrigger.ts' />
        module Commerce.Triggers.Samples {
            "use strict";
        }

## <a name="scenario-1-30day-return-policy"></a><span data-ttu-id="613af-117">シナリオ 1: 30 日返品ポリシー</span><span class="sxs-lookup"><span data-stu-id="613af-117">Scenario 1: 30day return policy</span></span>
<span data-ttu-id="613af-118">30日間の返品ポリシーを実装するには、新しいクラスを作成し、IPreConfirmReturnTransactionTrigger インターフェイスを実装して、IPreConfrimReturnTransactionTrigger を拡張します。</span><span class="sxs-lookup"><span data-stu-id="613af-118">To implement the 30-day return policy, extend the IPreConfrimReturnTransactionTrigger by creating a new class and implementing the IPreConfirmReturnTransactionTrigger interface.</span></span> <span data-ttu-id="613af-119">このトリガーは、トランザクションから項目を返す前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="613af-119">This trigger will be invoked before returning any item from the transaction.</span></span>

1.  <span data-ttu-id="613af-120">モジュール Commerce.Triggers.Samples で IPreConfirmReturnTransactionTrigger を実装する新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="613af-120">Create a new class that implements IPreConfirmReturnTransactionTrigger in the module Commerce.Triggers.Samples.</span></span> <span data-ttu-id="613af-121">次のコードの例に示すように、PreConfirmReturnTransactionTrigger と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="613af-121">Name it PreConfirmReturnTransactionTrigger, as shown in the following code example.</span></span>

        /*** Implementation of a pre-confirm return transaction trigger that validates that the transaction being returned is within the return period. */
        export class PreConfirmReturnTransactionTrigger implements IPreConfirmReturnTransactionTrigger {
        }

2.  <span data-ttu-id="613af-122">インターフェイスから**実行**メソッドを実装して、返品条件を検証するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="613af-122">Implement the **execute** method from the interface and add code to validate the return condition.</span></span>

        private static MILLISECONDS_PER_DAY: number = 100;
        private static RETURN_PERIOD_IN_DAYS: number = 0;
        private static RETURN_PERIOD_ENDED_ERROR_CODE: string = "Cannot return, you are past return date";
        /*** Executes the trigger. */
        public execute(options: IPreConfirmReturnTransactionTriggerOptions):     Commerce.IAsyncResult<Commerce.ICancelableResult> {
            var timeDiff: number = Math.abs(new Date().getTime() - options.originalTransaction.BusinessDate.getTime());
            var diffDays: number = Math.ceil(timeDiff / PreConfirmReturnTransactionTrigger.MILLISECONDS_PER_DAY);
            if (diffDays > PreConfirmReturnTransactionTrigger.RETURN_PERIOD_IN_DAYS) {
                var error: Proxy.Entities.Error = new     Proxy.Entities.Error(PreConfirmReturnTransactionTrigger.RETURN_PERIOD_ENDED_ERROR_CODE);
                return Commerce.AsyncResult.createRejected([error]);
            }
            return Commerce.AsyncResult.createResolved({ canceled: false });
        }

## <a name="scenario-2-limit-of-three-returns-per-transaction"></a><span data-ttu-id="613af-123">シナリオ 2: トランザクションごとに返品 3 回の制限</span><span class="sxs-lookup"><span data-stu-id="613af-123">Scenario 2: Limit of three returns per transaction</span></span>
<span data-ttu-id="613af-124">3 回限りの制限を実装するには、新しいクラスを作成し、IPreVoidProductsTrigger インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="613af-124">To implement the three-time limit, create a new class and implement the IPreVoidProductsTrigger interface.</span></span> <span data-ttu-id="613af-125">このトリガーは、トランザクション内の項目を無効にする前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="613af-125">This trigger will be invoked before voiding any item in a transaction.</span></span>

1.  <span data-ttu-id="613af-126">モジュール Commerce.Triggers.Samples で IPreVoidProductsTrigger インターフェイスを実装する PreVoidProductsTrigger という名前の新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="613af-126">Create a new class named PreVoidProductsTrigger that implements the IPreVoidProductsTrigger interface in the module Commerce.Triggers.Samples.</span></span> <span data-ttu-id="613af-127">このコードは、前の手順で作成した PreConfirmReturnTransactionTrigger クラスの外にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="613af-127">Make sure this code is outside of the PreConfirmReturnTransactionTrigger class that you created in the previous step.</span></span>

        /*** Implementation of a pre-customer add trigger that is used to ensure a blocked customer is not added to sale. */
        export class PreVoidProductsTrigger implements IPreVoidProductsTrigger {
        }

2.  <span data-ttu-id="613af-128">インターフェイスから**実行**メソッドを実装して、無効条件を検証するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="613af-128">Implement the **execute** method from the interface and add the code to validate the void condition.</span></span>

        private static VOID_ERROR_CODE: string = "Void is not allowed anymore.";
        /*** Executes the trigger. */
        public execute(options: IPreVoidProductsTriggerOptions): IAsyncResult<ICancelableResult> {
            var result: AsyncResult<ICancelableResult> = new AsyncResult<ICancelableResult>(null);
            if (!options.cartLines[0].IsVoided && this.getVoidedQuantity(options.cart) > 2) {
                var error: Proxy.Entities.Error =
                new Proxy.Entities.Error(PreVoidProductsTrigger.VOID_ERROR_CODE);
                result.reject([error]);
            } else {
                result.resolve({ canceled: false });
            }
            return result;
        }

        private getVoidedQuantity(cart: Proxy.Entities.Cart): number {
            var voidedQuantity: number = 0;
            cart.CartLines.forEach((cartLine: Proxy.Entities.CartLine) => {
            if (cartLine.IsVoided) {
                voidedQuantity = voidedQuantity + 1;
            }
            });
            return voidedQuantity;
        }

3.  <span data-ttu-id="613af-129">MPOS ログオン後に 2 つのトリガーを登録します。</span><span class="sxs-lookup"><span data-stu-id="613af-129">Register the two triggers after the MPOS logon.</span></span> <span data-ttu-id="613af-130">上記の手順で作成した 2 つのクラスの後、同じモジュールの Commerce.Triggers.Samples 内にある同じファイルに、次のコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="613af-130">Copy the following code to the same file after the two classes that you created in the previous steps but within the same module Commerce.Triggers.Samples.</span></span>

        /*** Implementation of a post log on trigger that is used to perform conditional registration of other triggers.*/
        export class ConditionalRegistrationPostLogOnTrigger implements IPostLogOnTrigger {
            private static alreadyRegistered: boolean = false;
            /*** Executes the trigger.*/
            public execute(options: IPostLogOnTriggerOptions): IVoidAsyncResult {
                // Check to ensure the triggers have not already been registered.
                if (!ConditionalRegistrationPostLogOnTrigger.alreadyRegistered) {
                    this.performRegistration();
                    // Set already registered field to true to prevent duplicate trigger registration.
                    ConditionalRegistrationPostLogOnTrigger.alreadyRegistered = true;
                }
                return VoidAsyncResult.createResolved();
            }

            /*** Perform the conditional registration of triggers.*/
            private performRegistration(): void {
            var conditionIsMet: boolean = true;
            TriggerManager.instance.register(
                CancelableTriggerType.PreVoidProducts,
                new PreVoidProductsTrigger());
            if (conditionIsMet) {
                TriggerManager.instance.register(
                CancelableTriggerType.PreReturnTransaction,
                new PreConfirmReturnTransactionTrigger());
        }}}

4.  <span data-ttu-id="613af-131">DOMCOntentLoaded イベント中に PostLogon トリガーを登録します。</span><span class="sxs-lookup"><span data-stu-id="613af-131">Register the PostLogon trigger during the DOMCOntentLoaded event.</span></span> <span data-ttu-id="613af-132">Commerce.Triggers.Samples モジュール内のすべてのクラスの外に、次のコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="613af-132">Copy the following code outside of all the classes but within the module Commerce.Triggers.Samples.</span></span>

        /**
        * Trigger types that do not support conditional registration should be registered when the DOMContentLoaded event is fired.
        * @remarks These trigger types include: ApplicationStart, PreLogOn, and PostLogOn.
        */
        document.addEventListener("DOMContentLoaded", function (): void {
            Commerce.Triggers.TriggerManager.instance.register(
            Commerce.Triggers.NonCancelableTriggerType.PostLogOn,
            new Commerce.Triggers.Samples.ConditionalRegistrationPostLogOnTrigger());
        });

## <a name="build-the-project"></a><span data-ttu-id="613af-133">プロジェクトの構築</span><span class="sxs-lookup"><span data-stu-id="613af-133">Build the project</span></span>
1.  <span data-ttu-id="613af-134">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="613af-134">Compile and rebuild the project.</span></span>
2.  <span data-ttu-id="613af-135">Visual Studio で**配置ボタン**をクリックして、ローカル コンピューターに MPOS を展開します。</span><span class="sxs-lookup"><span data-stu-id="613af-135">Deploy the MPOS in Local Machine by clicking the **Deploy** button in Visual Studio.</span></span> <span data-ttu-id="613af-136">"プロジェクトの POS.App を開始できる前に展開する必要があります" というエラー メッセージが表示された場合、下記の手順に従い、エラーを解決し、再試行します。</span><span class="sxs-lookup"><span data-stu-id="613af-136">If you get an error which states that “The project POS.App needs to be deployed before it can be started.”, then follow the steps below to resolve the error and try again.</span></span>
3.  <span data-ttu-id="613af-137">Visual Studio で ModernPOS ソリューションを右クリックし、**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="613af-137">Right-click the ModernPOS solution in Visual Studio and click **Properties**.</span></span>
4.  <span data-ttu-id="613af-138">**プロパティ** ウィンドウで、**コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="613af-138">In the **Property** window, select **Configuration**.</span></span>
5.  <span data-ttu-id="613af-139">Pos.App プロジェクトの **展開** チェック ボックスを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="613af-139">Select the **Deploy** check box for the Pos.App project and click **OK**.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="613af-140">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="613af-140">Validate the customization</span></span>
1.  <span data-ttu-id="613af-141">オペレーター ID に 000160、パスワードに 123 を使用して MPOS にログインします。</span><span class="sxs-lookup"><span data-stu-id="613af-141">Log in to MPOS using 000160 as the operator ID and 123 as the password.</span></span> <span data-ttu-id="613af-142">販売トランザクションを比較します。</span><span class="sxs-lookup"><span data-stu-id="613af-142">Complete a sales transaction.</span></span>
2.  <span data-ttu-id="613af-143">**仕訳帳の表示**をクリックし、商品を返送してください。</span><span class="sxs-lookup"><span data-stu-id="613af-143">Click **Show Journal** and try to return the merchandise.</span></span> <span data-ttu-id="613af-144">「返却できません。返却日を過ぎています」というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="613af-144">You will get the error message “Cannot return, you are past return date”.</span></span>
3.  <span data-ttu-id="613af-145">別の新しいトランザクションを作成し、4 つの異なるアイテムを追加します。</span><span class="sxs-lookup"><span data-stu-id="613af-145">Create another new transaction and add four different items.</span></span> <span data-ttu-id="613af-146">4 つのアイテムすべてを返すようにしてください。</span><span class="sxs-lookup"><span data-stu-id="613af-146">Try to return all four items.</span></span> <span data-ttu-id="613af-147">4番目の項目に関してエラーが発生し、「無効はこれ以上許されません」 というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="613af-147">You will get an error for the fourth item with the message, "Void is not allowed anymore.”</span></span>

> [!NOTE]
> <span data-ttu-id="613af-148">サンプルコードでは、期間を 100 ミリ秒として返すので、すぐにコードをテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="613af-148">In the sample code, the return the time period is configured as 100 ms, so that you can test your code immediately.</span></span> <span data-ttu-id="613af-149">必要に応じて、コンフィギュレーションを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="613af-149">You should change the configuration as needed.</span></span>
