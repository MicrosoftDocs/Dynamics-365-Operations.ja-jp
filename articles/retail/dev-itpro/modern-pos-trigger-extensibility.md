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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 82eab3c07cd78fde9ccc97bb695284c113c6a85a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="retail-modern-pos-mpos-and-cloud-pos-trigger-extensibility"></a>Retail Modern POS (MPOS) およびクラウド POS のトリガー拡張機能

> [!NOTE]
> このトピックは、Dynamics 365 for Finance and Operations の 7.1 およびそれ以降のバージョンに適用可能です。 バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。 これらのバージョンでは、オーバーレイせずに拡張モデルに従います。

このトピックでは、Modern POS と Cloud POS のクライアント側のトリガー機能について説明します。

<a name="trigger-overview"></a>トリガーの概要
----------------

トリガーは、Microsoft Dynamics 365 for Retail が Retail POS に対して発生するイベントです。 トリガーを使用すると、操作の前後にカスタム コードを挿入できます。 トリガーには事前トリガーと事後トリガーの 2 種類があります。

| プレトリガー                                                                                                                                                                                                                                                    | ポスト トリガー                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 操作を実行する前に、カスタム コードを挿入するためにプレトリガーを使用できます。 たとえば、顧客が購買のクーポンを使用する場合、有効期限が切れておらず、以前に使用されていないクーポンを検証するカスタム コードを挿入するための事前トリガーを使用できます。 | ポスト トリガーを使うと、完了した工程に応答するカスタム コードを挿入できます。 たとえば、**CustomerAdd** 操作後に実行し、顧客の誕生日である場合は、レジ担当者が顧客の幸せな誕生日を祈るよう指示するコードを記述できます。 |

### <a name="trigger-types"></a>トリガーのタイプ

Modern POS およびクラウド POS では、トリガーはキャンセル可能かキャンセル可能ではないかのいずれかです。

| 解約可能                                                                                                                                                                                                                                                                                                                                                                                                              | キャンセル不可                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ICancelableTriggerCancelable** トリガーを拡張するトリガー実装は、成功、失敗、または取り消しが可能です。 ワークフローの実行は、エラーを表示せずにキャンセルされます。 たとえば、ユーザーが支払/入金のためにロイヤルティ ポイントを使用することを確認するトリガーです。 ユーザーが**いいえ**と選択した場合、ユーザーにエラー メッセージが表示されずに、ロイヤルティ情報を入力するワークフローがキャンセルされます。 | **ITriggerNon-cancelable** トリガーを拡張するトリガー実装は、成功または失敗のいずれかが可能です。 トリガーが成功した場合、ワークフローを続行します。 トリガーが失敗すると、UI にメッセージが表示されます。 たとえば、販売および返品のために個別のトランザクションを作成するレジ担当者に対してガイドライン指示をすることによりスウェーデン語のローカライズ要件をサポートするトリガーです。 |

### <a name="guidelines"></a>ガイドライン

-   **トリガーの登録** – すべてのトリガーは、**TriggerManager::register** メソッドを使用して登録する必要があります。 **ApplicationStart**、**PreLogOn**、および **PostLogOn** トリガーは、**DOMContentLoaded** イベントが発生したときに呼び出される関数内で登録する必要があります。 他のトリガーは、同じ方法で登録することができますが、条件付きで登録することもできます。
    -   **条件付き登録** - トリガーを登録するかどうかの決定がチャネル内の情報に基づいている場合、条件付きでトリガーを登録できます。 条件付きの登録を **PostLogOn** トリガー内で実行する必要があります。 **注記:** 条件付きの登録は、アプリケーションの読み込み後最初のサインイン時にのみ実行することが重要です。 実装例については、この記事の後半のサンプル コードを参照してください。
-   **トリガーの実装** – 「サポートされているトリガー イベント」セクションに一覧表示されている各トリガー イベントには、関連付けられているトリガー インターフェイスがあります。 これらのトリガー インターフェイスは、アプリケーションとトリガー実装との間の契約を定義します。 各トリガーは、登録されているトリガー イベント タイプに関連付けられている定義済みインターフェースを実装する必要があります。

### <a name="triggers-execution-workflow"></a>トリガー実行ワークフロー

次の図は、**ItemSaleOperation** ワークフロー/操作のプリトリガーとポストトリガーの実行ワークフローを示しています。 

[![トリガー実行フロー](./media/trigger-execution-flow.png)](./media/trigger-execution-flow.png)

### <a name="supported-trigger-events"></a>サポートされているトリガー イベント

すべての操作でトリガーされる操作前後のトリガーとともに、次のトリガーがそのまま使用できます。

-   アプリケーション トリガー
    -   解約可能
        -   **PreLogOn** – Modern POS にサインインする前に呼び出されます
            -   operatorId
    -   キャンセル不可
        -   **ApplicationStart** - アプリケーションの起動時に呼び出される
        -   **ApplicationSuspend** - アプリケーションが中断されたときに呼び出される
        -   **PostLogOff** – サインアウトの操作が完了した後に呼び出されます
        -   **PostLogOn** – サインインの操作が完了した後に呼び出されます
-   現金管理トリガー
    -   解約可能
        -   **PreTenderDeclaration** – 支払/入金申告操作が実行される前に呼び出されます
    -   キャンセル不可
        -   **PostTenderDeclaration** – 支払/入金申告ワークフローの最後のステップとして呼び出されます
-   顧客トリガー
    -   解約可能
        -   **PreCustomerAdd** – 新しい顧客が作成される前に呼び出されます
        -   **PreCustomerClear** – 顧客が現在のトランザクションから消去される前に呼び出されます
        -   **PreCustomerSearch** – 顧客の検索前に呼び出されます
        -   **PreCustomerSet** – 顧客がトランザクションを開始する前に呼び出されます
    -   キャンセル不可
        -   **PostCustomerAdd** – 新しい顧客が作成された後に呼び出されます
        -   **PostCustomerClear** – 顧客がトランザクションから消去された後に呼び出されます
        -   **PostCustomerSearch** – 顧客の検索後に呼び出されます
-   割引のトリガー
    -   解約可能
        -   **PreLineDiscountAmount** – 検証によって割引が適用可能かどうかが判断された後、行割引金額操作中に呼び出されます
        -   **PreLineDiscountPercent** – 検証によって割引が適用可能かどうかが判断された後、行割引率操作中に呼び出されます
        -   **PreTotalDiscountAmount** – 検証によって割引が適用可能かどうかが判断された後、合計割引金額操作中に呼び出されます
        -   **PreTotalDiscountPercent** – 検証によって割引が適用可能かどうかが判断された後、割引金額率操作中に呼び出されます
    -   キャンセル不可
        -   **PostLineDiscountAmount** - 行割引金額のワークフローの最後のステップとして呼び出されます
        -   **PostLineDiscountPercent** – 行割引率のワークフローの最後のステップとして呼び出されます
        -   **PostTotalDiscountAmount** – 合計割引金額のワークフローの最後のステップとして呼び出されます
        -   **PostTotalDiscountPercent** – 合計割引率のワークフローの最後のステップとして呼び出されます
-   工程のトリガー
    -   解約可能
        -   **PreOperation** – 毎回の操作を実行する前、プリハンドラーおよび操作検証の前に呼び出されます
    -   キャンセル不可
        -   **OperationFailure** – 操作が失敗したときに呼び出され、復旧アクションを実行するために使用できます
        -   **PostOperation** – 操作が正常に終了したときに呼び出されます
-   支払トリガー
    -   解約可能
        -   **PreAddTenderLine** – 支払/入金の明細行がトランザクションに追加される前に呼び出されます
        -   **PrePayment** – 支払操作が開始される前に呼び出されます
        -   **PreVoidPayment** – 支払の無効化操作が開始される前に呼び出されます
    -   キャンセル不可
        -   **PostPayment** – 支払が追加された後に呼び出されます
        -   **PostVoidPayment** – 支払が無効にされた後に呼び出されます
-   印刷トリガー
    -   解約可能
        -   **PrePrintReceiptCopy** – レシートのコピーが印刷される前に呼び出されます
-   製品トリガー
    -   解約可能
        -   **PreClearQuantity** – 数量のクリア操作前に呼び出されます
        -   **PrePriceOverride** – 価格上書き操作前に呼び出されます
        -   **PreProductSale** – 品目販売操作前に呼び出されます
        -   **PreReturnProduct** – 返品操作前に呼び出されます
        -   **PreSetQuantity** – 数量の設定操作前に呼び出されます
        -   **PreVoidProducts** – ユーザーがトランザクションを無効化することを確認した後、トランザクションが無効化される前に呼び出されます
    -   キャンセル不可
        -   **PostClearQuantity** – 数量のクリア操作後に呼び出されます
        -   **PostPriceOverride** – 価格上書き操作後に呼び出されます
        -   **PostProductSale** – 品目販売操作後に呼び出されます
        -   **PostReturnProduct** – 返品操作後に呼び出されます
        -   **PostSetQuantity** – 数量の設定操作後に呼び出されます
        -   **PostVoidProducts** – 製品の無効化操作後に呼び出される
-   トランザクションのトリガー
    -   解約可能
        -   **PreConfirmReturnTransaction** – 返品するトランザクションを検索した後に呼び出されますが、カート明細行が返品可能と表示される前に呼び出されます
        -   **PreEndTransaction** – 販売トランザクションが完了する前に呼び出されます
        -   **PreRecallTransaction** – トランザクションが取り消される前に呼び出されます
        -   **PreReturnTransaction** – トランザクションが戻される前に呼び出されます
        -   **PreSuspendTransaction** – トランザクションが中断される前に呼び出されます
        -   **PreVoidTransaction** – トランザクションが無効化される前に呼び出されます
    -   キャンセル不可
        -   **BeginTransaction** - カートが作成され、トランザクションが開始される前に呼び出されます。
        -   **PostEndTransaction** – 販売トランザクションが完了した後に呼び出されます
        -   **PostRecallTransaction** – トランザクションが取り消された後に呼び出されます
        -   **PostReturnTransaction** – 返品のためにトランザクションの品目がカートに追加された後に呼び出されます
        -   **PostSuspendTransaction** – トランザクションを中断した後に呼び出されます
        -   **PostVoidTransaction** – トランザクションが無効化された後に呼び出されます

## <a name="trigger-example-implementation"></a>トリガー実装の例
トリガーを理解する最善の方法は、サンプルの実装シナリオを調べることです。

### <a name="modern-poscloud-pos-changes-to-support-swedish-localization-requirements-by-using-pos-triggers"></a>POS トリガーを使用したスウェーデン ローカライズ要件をサポートするための Modern POS/クラウド POS の変更

会計帳簿が接続されている場合、取引は返品と販売の両方の操作を行うことができません。 **IPreProductSaleTrigger** トリガーはこの状況が発生した場合にこれを検出するように実装されまたキャッシャーに確認するメッセージを表示します。 これは、スウェーデンの要件です。

1.  **IPreProductSaleTrigger** トリガーを実装して状況を検出し、レジ担当者に確認するメッセージを表示します。
2.  実装クラス内の **実行** メソッドにトリガー ビジネス ロジックを記述します。
3.  **DOMContentLoad** イベントで **PostLogonTrigger** 実装の一部としてトリガーを登録します。 

[![Trigger01](./media/trigger01.png)](./media/trigger01.png)

**目的:** 最新の POS / Cloud POS を、会計登録に接続されているときに、スウェーデン語のローカライズ要件を実装して同じトランザクションに売却と返品の両方の行が含まれないようにカスタマイズします。 Modern POS プロジェクトを開き、トリガーの実装を追加するために新しい TypeScript (.ts) ファイルを追加します。 弊社のカスタマイズを製品コードから切り離してアップグレードを管理しやすくするために、カスタマイズ用の新しい TypeScript ファイルを作成します。

1.  管理者として Microsoft Visual Studio 2015 を起動します。
2.  Modern POS ソリューションを、Retail SDK ディレクトリから開く:
    -   クラウド ホストしているコンピュータを使用している場合、パスは I:/RetailSDK になります。
    -   ローカルにダウンロードしたマシンを使用している場合は、パスは C:\\Microsoft Dynamics AX\\70\\Retail SDK です。

3.  POS.Core\\Triggers\\ に、**TriggerSample.ts** という名前の新しい TypeScript ファイルを作成します。 

[![Trigger02](./media/trigger02-1024x411.png)](./media/trigger02.png)

4.  TriggerSample.ts ファイルに次のコードを追加します。

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

5.  TriggerSample.ts ファイルを検査して **IPreProductSaleTrigger** の実装を確認します。

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

6.  **ValidateProductSalePreProductSaleTrigger** の登録を検査します。

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

7.  トリガーが登録されている **performRegistration** メソッドを検査します。

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

8.  **DOMContentLoad** イベントで **PostLogonTrigger** の登録を検査します。

        /**
        * Trigger types that do not support conditional registration should be registered when the DOMContentLoaded event is fired.
        * @remarks These trigger types include: ApplicationStart, PreLogOn and PostLogOn.
        */
        document.addEventListener("DOMContentLoaded", function (): void {
            Commerce.Triggers.TriggerManager.instance.register(
            Commerce.Triggers.NonCancelableTriggerType.PostLogOn,
            new Commerce.Triggers.Samples.ConditionalRegistrationPostLogOnTrigger());
        });

9.  実装を確認するため Modern POS をコンパイル、およびリビルドします。
    1.  **仕訳帳の表示**に移動し、返すトランザクションを選択します。 トランザクションに複数の明細行がある場合は、1 つの行を返します。 返品明細行は、カートに追加する必要があります。
    2.  左のナビゲーション ウィンドウで、製品検索 (検索アイコン) を使用して、「シャツ」のテキストを検索します。
    3.  シャツ製品のいずれかを選択し、アプリケーション バーで、**今すぐ売る** をクリックします。
    4.  **IPreProductSaleTrigger** トリガーを実行されていることを確認します。 同じトランザクションの販売および返品が実行できないことを示すメッセージが表示されるはずです。






