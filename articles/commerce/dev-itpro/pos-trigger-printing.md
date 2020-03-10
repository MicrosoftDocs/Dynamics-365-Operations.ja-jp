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
ms.openlocfilehash: 49763cb6b9979fd0b9249527cc598804eb9239af
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070780"
---
# <a name="modern-pos-mpos-triggers-and-printing"></a>Modern POS (MPOS) のトリガーと印刷

[!include [banner](../../includes/banner.md)]

トリガーを使用すると、いずれかの Retail Modern POS の操作前後に発生するイベントを取得できます。 トリガーを使用すると、以下の実行を可能にする複数のビジネス ロジック シナリオがサポートされます。 
- 操作の実行前または完了後に、カスタム ロジックを挿入します。 これには、すべての POS 操作の開始と終了時に実行される PreOperationTrigger と PostOperationTrigger と呼ばれる操作固有のトリガーと汎用トリガーが含まれます。  
- 操作を続行またはキャンセルします。 たとえば、検証が失敗するかまたはエラーが返される場合、前のトリガーで操作をキャンセルできます。 ポスト トリガーはキャンセル可能ではありません。
- 標準ロジックが実行された後にカスタム メッセージを表示するか、カスタム フィールドを挿入するシナリオでは、ポスト トリガーを使用します。 


次のテーブルは、使用可能なトリガーをリストし、それらを取り消すことができるかどうかを示しています。

## <a name="application-triggers"></a>アプリケーション トリガー

| トリガー                   | 種類           | 説明                                                                                                                                          |
|---------------------------|----------------|--------------|
| ApplicationStartTrigger   | キャンセル不可 | POS アプリケーションが開始した後に実行されます。 以前実行された内容はどれでも元に戻すかキャンセルすることができます。 |
| ApplicationSuspendTrigger | キャンセル不可 | POS アプリケーションが中断した後に実行されます。                                                                                     |
| PreLogOnTriggerTrigger    | 解約可能     | POS ログ オン前に実行されます。                                                                                                      |
| PostLogOnTriggerTrigger   | キャンセル不可 | POS ログ オン後に実行されます。                                                                                                       |
| PostLogOffTrigger         | キャンセル不可 | POS ログ オフ後に実行されます。                                                                                                      | 
| PreLockTerminalTrigger    | 解約可能     | POS レジスターのロック前に実行されます。  |
| PostLockTerminalTrigger   | キャンセル不可 | POS レジスターのロック後に実行されます。   | 
| PreUnlockTerminalTrigger         | 解約可能     | POS レジスターのロック解除前に実行されます。  |
| PostDeviceActivationTrigger      | キャンセル不可 | POS のアクティブ化後に実行されます。   | 
| PreElevateUserTrigger      | 解約可能 | マネージャー オーバーライドの前に実行されます。   | 
| PreRegisterAuditEventTrigger      | 解約可能 | 監査イベントの前に実行されます。   | 
| PostRegisterAuditEventTrigger      | キャンセル不可 | 監査イベントの後に実行されます。   | 
| PreOpenUrlTrigger      | 解約可能 | URLを開く操作の前に実行されます。   | 


## <a name="cash-management-triggers"></a>現金管理トリガー

| トリガー                      | 型           | 説明                                                 |
|------------------------------|----------------|-------------------------------------------------------------|
| PreTenderDeclarationTrigger  | 解約可能     | POS の支払または入金申告前に実行されます。 |
| PostTenderDeclarationTrigger | キャンセル不可 | POS の支払または入金申告後に実行されます。  |
| PreFloatEntryTrigger         | 解約可能     | POS 釣銭入力の前に実行されます。 |
| PostFloatEntryTrigger        | キャンセル不可 | POS 釣銭入力の後に実行されます。  |    


## <a name="customer-triggers"></a>顧客トリガー

| トリガー                   | 種類                    | 説明                                                        |
|---------------------------|-------------------------|--------------------------------------------------------------------|
| PreCustomerAddTrigger     | 解約可能              | トランザクションに顧客を追加する前に実行されます。             |
| PostCustomerAddTrigger    | キャンセル不可          | トランザクションに顧客を追加した後に実行されます。              |
| PreCustomerClearTrigger   | 解約可能              | 顧客がカートから削除する前に実行されます。 |
| PostCustomerClearTrigger  | キャンセル不可          | 顧客がカートから削除した後に実行されます。 |
| PreCustomerSetTrigger     | 解約可能              | 顧客がカートに追加される前に実行されます。            |
| PreCustomerSearchTrigger  | 解約可能              | 顧客検索が行われる前に実行されます。      |
| PostCustomerSearchTrigger | キャンセル不可          | 顧客検索が行われた後に実行されます。       |
| PostIssueLoyaltyCardTrigger  | キャンセル不可          | ロイヤルティ カードが発行された後に実行されます。       |
| PreCustomerSaveTrigger  | 解約可能          | 顧客を作成する前に実行されます。       |
| PostCustomerSaveTrigger  | キャンセル不可          | 顧客を作成した後に実行されます。       |
| PreSaveCustomerAddressTrigger      | 解約可能              | 顧客の住所が保存される前に実行されます。            |
| PreGetLoyaltyCardBalanceTrigger  | 解約可能          | ロイヤルティ カード残高を取得する前に実行されます。       |
| PostGetLoyaltyCardBalanceTrigger  | キャンセル不可          | ロイヤルティ カード残高を取得した後に実行されます。       |
| PreDisplayLoyaltyCardBalanceTrigger  | 解約可能          | ロイヤルティ カード残高を表示する前に実行されます。       |



## <a name="discount-triggers"></a>割引のトリガー

| トリガー                         | 型           | 説明                                                                     |
|---------------------------------|----------------|---------------------------------------------------------------------------------|
| PreLineDiscountAmountTrigger    | 解約可能     | 行割引金額がカート行に追加される前に実行されます。 |
| PostLineDiscountAmountTrigger   | キャンセル不可 | 行割引金額がカート行に追加した後に実行されます。     |
| PreLineDiscountPercentTrigger   | 解約可能     | 行割引率がカート行に追加される前に実行されます。   |
| PostLineDiscountPercentTrigger  | キャンセル不可 | 行割引率がカート行に追加した後に実行されます。    |
| PreTotalDiscountAmountTrigger   | 解約可能     | 合計割引額がカートに追加される前に実行されます。       |
| PostTotalDiscountAmountTrigger  | キャンセル不可 | 合計金額がカートに追加した後に実行されます。          |
| PreTotalDiscountPercentTrigger  | 解約可能     | 合計割引額がカートに追加される前に実行されます。       |
| PostTotalDiscountPercentTrigger | キャンセル不可 | 合計割引額がカートに追加した後に実行されます。        |
| PreAddCouponTrigger             | 解約可能     | 割引クーポンをカートに追加する前に実行されます。             |
| PostAddCouponTrigger            | キャンセル不可 | 割引クーポンをカートに追加した後に実行されます。              |

## <a name="operation-triggers"></a>工程のトリガー

| トリガー              | 種類           | 説明                                                                                                                                           |
|----------------------|----------------|-------------------------|
| PreOperationTrigger  | 解約可能     | すべての POS 操作前に実行される一般的なトリガー。 POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。 |
| PreOperationValidationTrigger | 解約可能 | 操作の検証が始まる前に実行される一般的なトリガー。   |
| OperationFailureTrigger | キャンセル不可 | 任意の POS 操作が失敗した後で実行される一般的なトリガー。  |
| PostOperationTrigger | キャンセル不可 | すべての POS 操作の後に実行される一般的なトリガー。 POS 操作で使用できる特定のトリガーがない場合は、このトリガーを使用することができます。  |

## <a name="payment-triggers"></a>支払トリガー

| トリガー                 | 種類           | 説明                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| PreAddTenderLineTrigger | 解約可能     | 支払行がカートに追加される前に実行されます。 |
| PrePaymentTrigger       | 解約可能     | POS で支払ボタンをクリックした後に実行されます。     |
| PostPaymentTrigger      | キャンセル不可 | すべての支払い処理が完了した後に実行されます。  |
| PreVoidPaymentTrigger   | 解約可能     | POS で支払行が無効になる前に実行されます。  |
| PostVoidPaymentTrigger  | キャンセル不可 | POS で支払行が無効になった後に実行されます。   |

## <a name="printing-triggers"></a>印刷トリガー

| トリガー                    | 種類       | 説明                                                                                                     |
|----------------------------|------------|--------|
| PrePrintReceiptCopyTrigger | 解約可能 | レシートのコピーが、表示仕訳帳の画面またはレシート表示ー画面から印刷される前に実行されます。 |
| PostReceiptPromptTrigger   | キャンセル不可 | レシート プロンプト (レシートを印刷するかどうか) 後に実行されます。 |

## <a name="product-triggers"></a>製品トリガー

| トリガー                    | 種類           | 説明                                                                          |
|----------------------------|----------------|--------------------------------------------------------------------------------------|
| PostGetSerialNumberTrigger | キャンセル不可 | シリアル番号がカートに追加された後に実行されます。           |
| PreProductSaleTrigger      | 解約可能     | 製品がカートに追加される前に実行されます。                   |
| PostProductSaleTrigger     | キャンセル不可 | 製品がカートに追加された後に実行されます。                    |
| PreReturnProductTrigger    | 解約可能     | 返品がカートに追加される前に実行されます。            |
| PostReturnProductTrigger   | キャンセル不可 | 返品がカートに追加された後に実行されます。             |
| PreSetQuantityTrigger      | 解約可能     | 数量情報がカート行で更新される前に実行されます。  |
| PostSetQuantityTrigger     | キャンセル不可 | 数量情報がカート行で更新となった後に実行されます。   |
| PrePriceOverrideTrigger    | 解約可能     | 価格がカート行に上書きされる前に実行されます。               |
| PostPriceOverrideTrigger   | キャンセル不可 | 価格がカート行に上書きされた後に実行されます。                |
| PreClearQuantityTrigger    | 解約可能     | 数量情報がカート行から削除になる前に実行されます。|
| PostClearQuantityTrigger   | キャンセル不可 | 数量情報がカート行から削除になった後に実行されます。 |
| PreVoidProductsTrigger     | 解約可能     | 製品がカートから無効となる前に実行されます。                   |
| PostVoidProductsTrigger    | キャンセル不可 | 製品がカートから無効となった後に実行されます。                    |
| PostPriceCheckTrigger      | キャンセル不可 | 製品の価格確認が行われた後に実行されます。          |

## <a name="sales-order-triggers"></a>販売注文トリガー

| トリガー                 | 型           | 説明                                                         |
|-------------------------|----------------|---------------------------------------------------------------------|
| PreRecallCustomerOrderTrigger     | 解約可能     | 顧客の注文がリコールされる前に実行されます。 |
| PostRecallCustomerOrderTrigger    | キャンセル不可 | 顧客の注文がリコールされた後に実行されます。  |
| PrePickUpCustomerOrderLinesTrigger    | 解約可能     | 顧客注文明細行が選択される前に実行されます。  |
| PreChangeShippingOriginTrigger    | 解約可能     | 顧客注文時に出荷元が変更される前に実行されます。|
| PreGetFulfillmentLinesTrigger     | 解約可能     | 注文フルフィルメント明細行が注文フルフィルメント ビューに読み込まれる前に実行されます。|
| PreShipFulfillmentLinesTrigger    | 解約可能     | **出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われる前に実行されます。|
| PostShipFulfillmentLinesTrigger   | キャンセル不可     | **出荷**ボタンを選択することで、注文フルフィルメント ビューから出荷が行われた後に実行されます。|
| PreMarkFulfillmentLinesAsPackedTrigger    | 解約可能     | **梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされる前に実行されます。|
| PostMarkFulfillmentLinesAsPackedTrigger   | キャンセル不可     | **梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包オプションとしてマークがトリガーされた後に実行されます。|
| PreCreatePackingSlipTrigger   | 解約可能     | **梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされる前に実行されます。|
| PostCreatePackingSlipTrigger  | キャンセル不可     | **梱包**ボタンを選択することで、注文フルフィルメント ビューから梱包明細オプションがトリガーされた後に実行されます。|
| PostReturnInvoicedSalesLinesTrigger   | キャンセル不可     | 返品対象として 1 つ以上の請求書が選択された後に実行されます。|


## <a name="shift-triggers"></a>シフト トリガー
| トリガー              | 型           | 説明                                             |
|----------------------|----------------|---------------------------------------------------------|
| PostOpenShiftTrigger | キャンセル不可 | このトリガーは、新しいシフトが開かれた後に実行されます。 |
| PreCloseShiftTrigger | 解約可能 | このトリガーは、シフトが開かれる前に実行されます。 |

## <a name="tax-override-triggers"></a>税上書きトリガー

| トリガー                           | 型           | 説明                                                                                     |
|-----------------------------------|----------------|---------------|
| PreOverrideLineProductTaxTrigger  | 解約可能     | 税額またはコードがカート行に上書きされる前に実行されます。           |
| PostOverrideLineProductTaxTrigger | キャンセル不可 | 税額またはコードがカート行に上書きされた後に実行されます。            |
| PreOverrideTransactionTaxTrigger  | 解約可能     | 税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。 |
| PostOverrideTransactionTaxTrigger | キャンセル不可 | 税額またはコードがカートまたはトランザクションに上書きされる前に実行されます。 |

## <a name="transaction-triggers"></a>トランザクションのトリガー

| トリガー                            | 種類           | 説明                                                                                                                  |
|------------------------------------|----------------|-------------------------------|
| BeginTransactionTrigger            | キャンセル不可 | トランザクションが初期化される前に実行されます。  |
| PreConfirmReturnTransactionTrigger | 解約可能     | 返品トランザクションが確認される前に実行されます。  |
| PreReturnTransactionTrigger        | 解約可能     | 返品トランザクションが処理される前に実行されます。 |
| PostReturnTransactionTrigger       | キャンセル不可 | 返品トランザクションが処理された後に実行されます。   |
| PreEndTransactionTrigger           | 解約可能     | 終了トランザクション要求が呼び出される前に実行され、DB への変更をコミットしてトランザクションを閉じます。 |
| PostEndTransactionTrigger          | キャンセル不可 | 終了トランザクション要求が呼び出された後に実行され、DB への変更をコミットしてトランザクションを閉じます。  |
| PreVoidTransactionTrigger          | 解約可能     | トランザクションが無効になる前に実行されます。         |
| PostVoidTransactionTrigger         | キャンセル不可 | トランザクションが無効となった後に実行されます。        |
| PreSuspendTransactionTrigger       | 解約可能     | トランザクションが中断する前に実行されます。   
| PostSuspendTransactionTrigger      | キャンセル不可 | トランザクションが中断した後に実行されます。    |
| PreRecallTransactionTrigger        | 解約可能     | トランザクションまたは注文がリコールされる前に実行されます。 |
| PostRecallTransactionTrigger       | キャンセル不可 | トランザクションまたは注文がリコールされた後に実行されます。  |
| PostCartCheckoutTrigger            | キャンセル不可 | チェックアウト プロセスの完了後に実行されます。     |
| PreRecallTransactionTrigger        | 解約可能     | 顧客の注文がリコールされる前に実行されます。       |
| PostRecallTransactionTrigger       | キャンセル不可 | 顧客の注文がリコールされた後に実行されます。        |
| PreSelectTransactionPaymentMethodTrigger       | 解約可能 |  ユーザーが**カート ビュー - 合計**パネルで**合計**を選択すると、使用可能な支払方法が表示され、このトリガーはこのダイアログが表示される前に実行されます。 このトリガーから利用可能な支払方法を変更するための拡張コードを使用できます。      |

## <a name="reason-code-triggers"></a>理由コード トリガー
| トリガー              | 型           | 説明                                             |
|----------------------|----------------|---------------------------------------------------------|
| PostGetReasonCodeLine | 解約可能 | このトリガーは、理由コードが入力された後 (理由コードがカートに追加される前) に実行されます。 |

## <a name="transfer-order-triggers"></a>移動オーダー トリガー
| トリガー              | 型           | 説明                                             |
|----------------------|----------------|---------------------------------------------------------|
| PreCreateTransferOrderTrigger | 解約可能 | このトリガーは、移動オーダーが作成される前に実行 (注文入力後に実行) されます。 |
| PreUpdateTransferOrderTrigger | 解約可能 | このトリガーは、移動オーダーが更新される前に実行されます。 |


## <a name="business-scenario"></a>ビジネス シナリオ
この例では、ユーザーがトランザクションを中断したときに、カスタム レシートが印刷されます。 この例では、**PostSuspendTransactionTrigger** トリガーを実装し、既存の周辺機器 API を使用してカスタム レシートを印刷します。

このシナリオを実装するには、次の手順を行う必要があります。

1. **POS 拡張機能:** **PostSuspendTransactionTrigger** トリガーを実装し、CRT から受領書データを取得して、印刷用のプリンタに送信します。 
2. **CRT 拡張:** 印刷対象の受領書データを生成します。

## <a name="implement-a-trigger"></a>トリガーの実装

1. 管理者モードで Visual Studio 2015 を開きます。
2. **ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。
3. **POS.Extensions** プロジェクトで、**SuspendReceiptSample** という名前の新しいフォルダーを作成します。
4. **SuspendReceiptSample** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。
5. **TriggersHandlers** フォルダーに、**PostSuspendTransactionTrigger.ts** という名前の新しい Typescript ファイルを追加します。
6. 次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。

   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ObjectExtensions } from "PosApi/TypeExtensions";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { PrinterPrintRequest, PrinterPrintResponse } from "PosApi/Consume/Peripherals";
   import { GetHardwareProfileClientRequest, GetHardwareProfileClientResponse } from "PosApi/Consume/Device";
   import { GetReceiptsClientRequest, GetReceiptsClientResponse } from "PosApi/Consume/SalesOrders";
   ```
   
7. **PostSuspendTransactionTrigger** という名前の新しいクラスを作成し、**PostSuspendTransactionTrigger** から拡張します。
 
    ```typescript
    export default class PostSuspendTransactionTrigger extends Triggers.PostSuspendTransactionTrigger { }
    ```
8. トリガーの**実行**メソッドを実装し、レシート プロファイルを取得して、カスタムのレシートを印刷します。
   
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
   
   全体の例は次のようになります。

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
9. 新しい .json ファイルを **SuspendReceiptSample** フォルダーの下に作成し、**manifest.json** という名前を付けます。
10. **manifest.json** の自動生成されたコードを次のコードに置き換えます。

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
11. **extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**SuspendReceiptSample** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。

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
12. **tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。 POS では、このファイルを使用して、拡張機能を追加または除外します。 既定では、リストに除外されたすべての拡張リストが含まれています。 POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。

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
13. プロジェクトをコンパイル、およびリビルドします。

## <a name="override-the-crt-receipt-request-to-generate-the-receipt-data"></a>受領書データを生成するために CRT 受領要求を上書きする


このセクションでは、中断されたトランザクションのレシートを印刷するために既存の CRT 要求を上書きする方法について説明します。 


1. Visual Studio 2015 を起動します。
2. **ファイル**メニューで、**開く \> プロジェクト/ソリューション**を選択します。 テンプレート プロジェクト (**SampleCRTExtension.csproj**) を検索します。
3. テンプレート プロジェクト **Runtime.Extensions.SuspendReceiptSample** を名前変更します。
4. オプション: 既定の名前空間を変更します。
5. 出力アセンブリ **Contoso.Commerce.Runtime.SuspendReceiptSample** を名前変更します。
6. プロジェクト内で、新しい要求クラス ファイルを追加し、**GetCustomReceiptsRequestHandler.cs** いう名前をつけます。
7. 次のコードをコピーして、クラスに貼り付けます。 コピーする前に、自動的に生成されたコードを削除します。

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

8. 次のコードをコピーして、カート テーブルからトランザクションを読み取る新しいメソッドを追加するクラスに貼り付けます。中断されたトランザクションは、この時点ではコマース トランザクション テーブルに作成されていないためです。 カート トランザクションを販売トランザクションに変換する必要があります。 入庫オブジェクトは販売トランザクションしか読み込むことができないため、この変換が必要です。

    > [!NOTE]
    > 完了したトランザクションに対するカスタム レシートを印刷する必要がある場合、買い物カゴ トランザクションを取得して販売トランザクションに変換する必要はありません。 トランザクションが完了したため、既に販売トランザクションに変換されました。

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

9. 次のコードをコピーして、HQ で定義されているカスタムの受領書フォーマットに基づき販売トランザクション情報を使用して、受領書フォーマットを作成する新しいメソッドを追加するクラスに貼り付けます。

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

10. 次のコードをコピーして、確認受入応答を上書きする新しいメソッドを追加するクラスに貼り付けます。 この方法は、要求を処理し、応答を返します。

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

    全体的なコードは、次のようになります。

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

11. プロジェクトをコンパイル、およびビルドします。
12. 出力ディレクトリに移動し、出力アセンブリをコピーします。
13. **…\\RetailServer\\webroot\\bin\\ext** フォルダに移動し、アセンブリに貼り付けます。
14. また、**…\\RetailSDK\\参照**フォルダーでアセンブリを貼り付けます。
15. **commerceruntime.ext.config**ファイルを開き、\<構成\>セクションでカスタム アセンブリ情報を追加します。

    ```xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SuspendReceiptSample" />
    ```

16. ファイルを保存して閉じます。
17. Commerce Scale Unit を再起動して新しいアセンブリを読み込んでください。

## <a name="add-the-custom-receipt-layout"></a>カスタム レシート レイアウトの追加

1. Dynamics 365 Commerce を開きます。
2. **Retail とコマース** > **チャネル設定** > **POS 設定** > **POS** > **受領書フォーマット**の順に移動します。
3. **受領書フォーマット**内の**新規**をクリックします。
4. **提出した受領書フォーマット** フィールドに、**中断**という形式名を入力します。 **受領書タイプ** フィールドで、**CustomReceiptType7** を選択します。
5. **デザイナー**をクリックし、入庫デザイナーを開きます。
6. インストールするようメッセージが表示されたら、指示に従います。 Azure Active Directory (AAD) 資格情報を入力し、デザイナーを起動します。
7. 必須のフィールドをヘッダー、明細行、またはフッターにドラッグおよびドロップします。 または、コピー機能を使用して既存のレシートの形式からコピーし、それを編集します。
8. **保存**をクリックします。
9. **Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **視覚プロファイル**の順に移動します。
10. **電子メール受信** プロファイルまたは保存するプロファイルを選択します。 **一般**タブの**追加**ボタンをクリックします。
11. **受領書タイプ**で、**CustomReceiptType7** を選択し、**受領書フォーマット**で**中断**を選択します。
12. **Retail とコマース > Retail とコマース IT > 配送スケジュール**の順に移動します。
13. **レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。 要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。 

## <a name="configure-the-xps-printer-for-quick-testing"></a>クイック テスト用の XPS プリンタのコンフィギュレーション

1. **Retail とコマース** > **チャネル設定** > **POS 設定** > **POS プロファイル** > **ハードウェア プロファイル**の順に移動します。
2. デバイスで使用しているハードウェア プロファイルを選択します。 たとえば、デモ データのすべてのヒューストン デバイスは **HW002** を使用します。
3. 操作バーの**編集**をクリックします。
4. **プリンター** FastTab を展開します。 **プリンター** ドロップダウン リストで、**Windows ドライバー**を選択し、デバイス名フィールドに **Microsoft XPS ドキュメント ライター**と入力します。
5. **保存**をクリックします。
6. **Retail とコマース** > **Retail とコマース IT** > **配送スケジュール**の順に移動します。
7. **レジスター (1090)** を選択し、アクション バーで **今すぐ実行** をクリックします。 要求するメッセージが表示されたら、**はい** をクリックしてジョブを実行します。 

## <a name="validate-the-extension"></a>拡張機能の検証

1. **F5** キーを押し、POS を展開してカスタマイズをテストします。
2. POS が開始されると、POS にサインインし、トランザクションへ品目を追加します。
3. トランザクションを中断します。
4. カスタム レシートが印刷されます。
