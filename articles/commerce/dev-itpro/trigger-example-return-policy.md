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
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 65863
ms.assetid: 539105e2-097d-4723-84a1-8084c2c32652
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 07235088e2163d0894393293794d4d4d4ca520eb
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070786"
---
# <a name="implement-a-return-policy-by-using-triggers"></a>トリガーを使用して返品ポリシーを実装してください

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。 バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。 これらのバージョンでは、オーバーレイせずに拡張モデルに従います。

このトピックでは、トリガーを使用して新しいポリシーを実装する方法の例を 2 つ示しています。

このトピックの例では、新しい返品ポリシーがあることを前提としています。 返品の最長期間は 30 日間で、購入日から 30 日を超えて返品することはできません。 また、レジ担当者またはマネージャーは、1 回のトランザクションで 3 つ以上の品目を無効にすることはできません。

## <a name="extend-the-mpos-trigger"></a>MPOS トリガーを拡張
1.  Visual Studio を管理者としてオープンします。
2.  Modern POS ソリューションを K:\\RainMainStab\\7.0.1265.3014\\小売\\サービス\\RetailSDK\\コード\\POS から開きます。
3.  **トリガー** フォルダーの下の POS.Core プロジェクトに新しい TypeScript ファイルを追加し、ExtensionTrigger.ts という名前をつけます。
4.  トリガー インターフェイスへの参照を追加し、コードの新しいモジュールを作成します。 ExtensionTrigger.ts ファイルに次のコードを追加します。

    ```typescript
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
    ```

## <a name="scenario-1-30day-return-policy"></a>シナリオ 1: 30 日返品ポリシー
30日間の返品ポリシーを実装するには、新しいクラスを作成し、IPreConfirmReturnTransactionTrigger インターフェイスを実装して、IPreConfrimReturnTransactionTrigger を拡張します。 このトリガーは、トランザクションから項目を返す前に呼び出されます。

1.  モジュール Commerce.Triggers.Samples で IPreConfirmReturnTransactionTrigger を実装する新しいクラスを作成します。 次のコードの例に示すように、PreConfirmReturnTransactionTrigger と名前を付けます。

    ```typescript
    /*** Implementation of a pre-confirm return transaction trigger that validates that the transaction being returned is within the return period. */
    export class PreConfirmReturnTransactionTrigger implements IPreConfirmReturnTransactionTrigger {
    }
    ```

2.  インターフェイスから**実行**メソッドを実装して、返品条件を検証するコードを追加します。

    ```typescript
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
    ```

## <a name="scenario-2-limit-of-three-returns-per-transaction"></a>シナリオ 2: トランザクションごとに返品 3 回の制限
3 回限りの制限を実装するには、新しいクラスを作成し、IPreVoidProductsTrigger インターフェイスを実装します。 このトリガーは、トランザクション内の項目を無効にする前に呼び出されます。

1.  モジュール Commerce.Triggers.Samples で IPreVoidProductsTrigger インターフェイスを実装する PreVoidProductsTrigger という名前の新しいクラスを作成します。 このコードは、前の手順で作成した PreConfirmReturnTransactionTrigger クラスの外にあることを確認します。

    ```typescript
    /*** Implementation of a pre-customer add trigger that is used to ensure a blocked customer is not added to sale. */
    export class PreVoidProductsTrigger implements IPreVoidProductsTrigger {
    }
    ```

2.  インターフェイスから**実行**メソッドを実装して、無効条件を検証するコードを追加します。

    ```typescript
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
    ```

3.  MPOS ログオン後に 2 つのトリガーを登録します。 上記の手順で作成した 2 つのクラスの後、同じモジュールの Commerce.Triggers.Samples 内にある同じファイルに、次のコードをコピーします。

    ```typescript
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
    ```

4.  DOMCOntentLoaded イベント中に PostLogon トリガーを登録します。 Commerce.Triggers.Samples モジュール内のすべてのクラスの外に、次のコードをコピーします。

    ```typescript
    /**
    * Trigger types that do not support conditional registration should be registered when the DOMContentLoaded event is fired.
    * @remarks These trigger types include: ApplicationStart, PreLogOn, and PostLogOn.
    */
    document.addEventListener("DOMContentLoaded", function (): void {
        Commerce.Triggers.TriggerManager.instance.register(
        Commerce.Triggers.NonCancelableTriggerType.PostLogOn,
        new Commerce.Triggers.Samples.ConditionalRegistrationPostLogOnTrigger());
    });
    ```

## <a name="build-the-project"></a>プロジェクトの構築
1.  プロジェクトをコンパイル、およびリビルドします。
2.  Visual Studio で**配置ボタン**をクリックして、ローカル コンピューターに MPOS を展開します。 "プロジェクトの POS.App を開始できる前に展開する必要があります" というエラー メッセージが表示された場合、下記の手順に従い、エラーを解決し、再試行します。
3.  Visual Studio で ModernPOS ソリューションを右クリックし、**プロパティ**をクリックします。
4.  **プロパティ** ウィンドウで、**コンフィギュレーション**を選択します。
5.  Pos.App プロジェクトの **展開** チェック ボックスを選択し、**OK** をクリックします。

## <a name="validate-the-customization"></a>カスタマイズの検証
1.  オペレーター ID に 000160、パスワードに 123 を使用して MPOS にログインします。 販売トランザクションを比較します。
2.  **仕訳帳の表示**をクリックし、商品を返送してください。 「返却できません。返却日を過ぎています」というエラー メッセージが表示されます。
3.  別の新しいトランザクションを作成し、4 つの異なるアイテムを追加します。 4 つのアイテムすべてを返すようにしてください。 4番目の項目に関してエラーが発生し、「無効はこれ以上許されません」 というメッセージが表示されます。

> [!NOTE]
> サンプルコードでは、期間を 100 ミリ秒として返すので、すぐにコードをテストすることができます。 必要に応じて、コンフィギュレーションを変更する必要があります。
