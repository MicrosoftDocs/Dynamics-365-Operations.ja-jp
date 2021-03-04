---
title: 販売時点管理 (POS) API または POS 拡張からの工程を呼び出す
description: Retail POS API を使用すると、拡張機能を構築したり、POS に新しい機能を追加したりすることができます。
author: mugunthanm
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: a4cc8cffddd0f86fa5eaad7b0b78edaf7cd91c6c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681524"
---
# <a name="call-point-of-sale-pos-apis-or-operations-from-pos-extensions"></a>販売時点管理 (POS) API または POS 拡張からの工程を呼び出す

[!include [banner](../../includes/banner.md)]

Retail POS API を使用すると、拡張機能を構築したり、POS に新しい機能を追加したりすることができます。 たとえば、製品の詳細を取得し、価格を変更し、またはカートに品目を追加する新しい機能を追加する場合は、その作業を行うための POS API を呼び出します。 POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。 Commerce Runtime (RT)、POS、およびハードウェア ステーションの拡張パターンはすべて、要求/応答パターンを使用します。 

このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。  

## <a name="scenarios"></a>シナリオ
POS API は、3 つのさまざまなシナリオに分類されます。

- **消費** - 拡張機能のパブリック API を使用します。 
- **拡張** - 一部の追加ロジックを実行するパブリック API を拡張します。 
- **作成** - POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。 

## <a name="consume-pos-apis-in-extensions"></a>拡張機能で POS API を使用する
API は要求/応答パターンを使用して公開されるため、ビジネス ロジックを実装するための外部 Web サービス呼び出しを行うことができます。 たとえばが、品目の価格を変更する場合、**PriceOverrideOperationRequest** を呼び出します。 API は、CRT、周辺機器、保存操作などのモジュールによりサブカテゴリ化されます。 

多くの新しい API が追加されました。 すべての API のリストは **…Retail SDK\\POS\\Extensions\\Pos.Api.d.ts** ファイルで探すことができます。 

### <a name="how-to-consume-an-api-in-an-extension"></a>拡張機能で API を使用する方法
拡張機能で  API を使用するには、次の手順を実行します。

1. 管理者モードで Visual Studio 2015 を開きます。
2. **ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。
3. **POS.Extensions** プロジェクトで、**POSAPIExtension** という名前の新しいフォルダーを作成します。
4. **POSAPIExtension** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。
5. **TriggersHandlers** フォルダーに、新しい Typescript ファイルを追加し、**PreEndTransactionTrigger.ts** と名前を付けます。
6. 次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。
   ```typescript
   import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
   import { ClientEntities, ProxyEntities } from "PosApi/Entities";
   import { ObjectExtensions, StringExtensions } from "PosApi/TypeExtensions";
   import {
       GetCurrentCartClientRequest, GetCurrentCartClientResponse,
       SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse
   } from "PosApi/Consume/Cart";

   import {
       GetCustomerClientRequest, GetCustomerClientResponse,
   } from "PosApi/Consume/Customer";

   import { ShowMessageDialogClientRequest, ShowMessageDialogClientResponse } from "PosApi/Consume/Dialogs";
   ```
7. **PreEndTransactionTrigger** と呼ばれる新しいクラスを作成し、**PreEndTransactionTrigger** から拡張します。
    ```typescript
        export default class PreEndTransactionTrigger extends Triggers.PreEndTransactionTrigger { }
    ```
8. クラス内で、属性名と値の例に対して次の変数を宣言します。
    ```typescript
    private static CART_ATTRIBUTE_NAME: string = "ATT SAMPLE";
    private static CART_ATTRIBUTE_VALUE_TRUE: string = "True";
    private static CART_ATTRIBUTE_VALUE_FALSE: string = "False";
    private static DIALOG_RESULT_YES: string = "yes";
    private static DIALOG_RESULT_NO: string = "no";
    private static DIALOG_YES_BUTTON_ID: string = "CART_PreEndTransactionTrigger_MessageDialog_Yes";
    private static DIALOG_NO_BUTTON_ID: string = "CART_PreEndTransactionTrigger_MessageDialog_No";
    ```
9. トリガー **実行** メソッドを実装し、既存の POS API を呼び出します。 **execute** メソッドは、API を呼び出して現在の買い物カゴと顧客を取得し、買い物カゴに属性を保存します。
    ```typescript
        public execute(options: Triggers.IPreEndTransactionTriggerOptions): Promise<ClientEntities.ICancelable> {
            console.log("Executing PreEndTransactionTrigger with options " + JSON.stringify(options) + ".");

            let currentCart: ProxyEntities.Cart;
            return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())
                .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):
                    Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {
                    currentCart = getCurrentCartClientResponse.data.result;

                    // Gets the current customer.

                    let result: Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>>;
                    if (!ObjectExtensions.isNullOrUndefined(currentCart) && !ObjectExtensions.isNullOrUndefined(currentCart.CustomerId)) {
                        let getCurrentCustomerClientRequest: GetCustomerClientRequest<GetCustomerClientResponse> =
                            new GetCustomerClientRequest(currentCart.CustomerId);
                        result = this.context.runtime.executeAsync<GetCustomerClientResponse>(getCurrentCustomerClientRequest);
                    } else {
                        result = Promise.resolve({ canceled: false, data: new GetCustomerClientResponse(null) });
                    }

                    return result;
                })
                .then((getCurrentCustomerClientResponse: ClientEntities.ICancelableDataResult<GetCustomerClientResponse>):
                    Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>> => {
                    let currentCustomer: ProxyEntities.Customer = getCurrentCustomerClientResponse.data.result;
                    let result: Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>>;

                    if (!ObjectExtensions.isNullOrUndefined(currentCart)

                        && !ObjectExtensions.isNullOrUndefined(currentCustomer)) {

                        let yesButton: ClientEntities.Dialogs.IDialogResultButton = {

                            id: PreEndTransactionTrigger.DIALOG_YES_BUTTON_ID,
                            label: "Yes", // "Yes"

                            result: PreEndTransactionTrigger.DIALOG_RESULT_YES
                        };

                        let noButton: ClientEntities.Dialogs.IDialogResultButton = {
                            id: PreEndTransactionTrigger.DIALOG_NO_BUTTON_ID,
                            label: "No", // "No"
                            result: PreEndTransactionTrigger.DIALOG_RESULT_NO
                        };

                        let showMessageDialogClientRequestOptions: ClientEntities.Dialogs.IMessageDialogOptions = {
                            title: "Save attribute - Sample",
                            subTitle: StringExtensions.EMPTY,
                            message: "Save attribute ?",
                            button1: yesButton,
                            button2: noButton

                        };

                        let showMessageDialogClientRequest: ShowMessageDialogClientRequest<ShowMessageDialogClientResponse> =
                            new ShowMessageDialogClientRequest(showMessageDialogClientRequestOptions);
                        result = this.context.runtime.executeAsync<ShowMessageDialogClientResponse>(showMessageDialogClientRequest);
                    } else {
                        result = Promise.resolve({ canceled: false, data: new ShowMessageDialogClientResponse(null) });
                    }
                    return result;
                })

                .then((showMessageDialogClientResponse: ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>):
                    Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>> => {

                    // Save the attribute value depending on the dialog result.
                    let messageDialogResult: ClientEntities.Dialogs.IMessageDialogResult = showMessageDialogClientResponse.data.result;
                    let result: Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>>;

                    if (!ObjectExtensions.isNullOrUndefined(messageDialogResult)) {
                        let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();
                        attributeValue.Name = PreEndTransactionTrigger.CART_ATTRIBUTE_NAME;
                        attributeValue.TextValue = messageDialogResult.dialogResult === PreEndTransactionTrigger.DIALOG_RESULT_YES ?
                            PreEndTransactionTrigger.CART_ATTRIBUTE_VALUE_TRUE : PreEndTransactionTrigger.CART_ATTRIBUTE_VALUE_FALSE;

                        let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];
                        let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =
                            new SaveAttributesOnCartClientRequest(attributeValues);
                        result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
                    } else {
                        result = Promise.resolve({ canceled: false, data: new SaveAttributesOnCartClientResponse(null) });
                    }
                    return result;
                });
        }
    ```

    全体的なコードは次の例のようになります。 
    
    ```typescript
    import * as Triggers from "PosApi/Extend/Triggers/TransactionTriggers";
    import { ClientEntities, ProxyEntities } from "PosApi/Entities";
    import { ObjectExtensions, StringExtensions } from "PosApi/TypeExtensions";
    import {

        GetCurrentCartClientRequest, GetCurrentCartClientResponse,
        SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse

    } from "PosApi/Consume/Cart";

    import {

        GetCustomerClientRequest, GetCustomerClientResponse,
    } from "PosApi/Consume/Customer";

    import { ShowMessageDialogClientRequest, ShowMessageDialogClientResponse } from "PosApi/Consume/Dialogs";

    /**
    * Example implementation of an PreEndTransactionTrigger trigger that logs to the console.
    */

    export default class PreEndTransactionTrigger extends Triggers.PreEndTransactionTrigger {
        private static CART_ATTRIBUTE_NAME: string = "ATT SAMPLE";
        private static CART_ATTRIBUTE_VALUE_TRUE: string = "True";
        private static CART_ATTRIBUTE_VALUE_FALSE: string = "False";
        private static DIALOG_RESULT_YES: string = "yes";
        private static DIALOG_RESULT_NO: string = "no";
        private static DIALOG_YES_BUTTON_ID: string = "CART_PreEndTransactionTrigger_MessageDialog_Yes";
        private static DIALOG_NO_BUTTON_ID: string = " CART_PreEndTransactionTrigger_MessageDialog_No";

        /**
        * Executes the trigger functionality.
        * @param {Triggers.IPreEndTransactionTriggerOptions} options The options provided to the trigger.
        */

        public execute(options: Triggers.IPreEndTransactionTriggerOptions): Promise<ClientEntities.ICancelable> {
            console.log("Executing PreEndTransactionTrigger with options " + JSON.stringify(options) + ".");

            let currentCart: ProxyEntities.Cart;
            return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())
                .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):
                    Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {
                    currentCart = getCurrentCartClientResponse.data.result;

                    // Gets the current customer.

                    let result: Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>>;
                    if (!ObjectExtensions.isNullOrUndefined(currentCart) && !ObjectExtensions.isNullOrUndefined(currentCart.CustomerId)) {
                        let getCurrentCustomerClientRequest: GetCustomerClientRequest<GetCustomerClientResponse> =
                            new GetCustomerClientRequest(currentCart.CustomerId);
                        result = this.context.runtime.executeAsync<GetCustomerClientResponse>(getCurrentCustomerClientRequest);
                    } else {
                        result = Promise.resolve({ canceled: false, data: new GetCustomerClientResponse(null) });
                    }

                    return result;
                })
                .then((getCurrentCustomerClientResponse: ClientEntities.ICancelableDataResult<GetCustomerClientResponse>):
                    Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>> => {
                    let currentCustomer: ProxyEntities.Customer = getCurrentCustomerClientResponse.data.result;
                    let result: Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>>;

                    if (!ObjectExtensions.isNullOrUndefined(currentCart)

                        && !ObjectExtensions.isNullOrUndefined(currentCustomer)) {

                        let yesButton: ClientEntities.Dialogs.IDialogResultButton = {

                            id: PreEndTransactionTrigger.DIALOG_YES_BUTTON_ID,
                            label: "Yes", // "Yes"

                            result: PreEndTransactionTrigger.DIALOG_RESULT_YES
                        };

                        let noButton: ClientEntities.Dialogs.IDialogResultButton = {
                            id: PreEndTransactionTrigger.DIALOG_NO_BUTTON_ID,
                            label: "No", // "No"
                            result: PreEndTransactionTrigger.DIALOG_RESULT_NO
                        };

                        let showMessageDialogClientRequestOptions: ClientEntities.Dialogs.IMessageDialogOptions = {
                            title: "Save attribute - Sample",
                            subTitle: StringExtensions.EMPTY,
                            message: "Save attribute ?",
                            button1: yesButton,
                            button2: noButton

                        };

                        let showMessageDialogClientRequest: ShowMessageDialogClientRequest<ShowMessageDialogClientResponse> =
                            new ShowMessageDialogClientRequest(showMessageDialogClientRequestOptions);
                        result = this.context.runtime.executeAsync<ShowMessageDialogClientResponse>(showMessageDialogClientRequest);
                    } else {
                        result = Promise.resolve({ canceled: false, data: new ShowMessageDialogClientResponse(null) });
                    }
                    return result;
                })

                .then((showMessageDialogClientResponse: ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>):
                    Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>> => {

                    // Save the attribute value depending on the dialog result.
                    let messageDialogResult: ClientEntities.Dialogs.IMessageDialogResult = showMessageDialogClientResponse.data.result;
                    let result: Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>>;

                    if (!ObjectExtensions.isNullOrUndefined(messageDialogResult)) {
                        let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();
                        attributeValue.Name = PreEndTransactionTrigger.CART_ATTRIBUTE_NAME;
                        attributeValue.TextValue = messageDialogResult.dialogResult === PreEndTransactionTrigger.DIALOG_RESULT_YES ?
                            PreEndTransactionTrigger.CART_ATTRIBUTE_VALUE_TRUE : PreEndTransactionTrigger.CART_ATTRIBUTE_VALUE_FALSE;

                        let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];
                        let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =
                            new SaveAttributesOnCartClientRequest(attributeValues);
                        result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
                    } else {
                        result = Promise.resolve({ canceled: false, data: new SaveAttributesOnCartClientResponse(null) });
                    }
                    return result;
                });
        }
    }
    ```
10. 新しい json ファイルを POSAPIExtension フォルダーの下に作成し、manifest.json という名前を付けます。

11. manifest.json ファイルに、次のコードをコピーして貼り付けます。 このコードをコピーする前に、既定で生成されたコードを削除してください。
    ```typescript
    {

        "$schema": "../manifestSchema.json",
            "name": "Pos_Extensibility_APISample",
                "publisher": "Microsoft",
                    "version": "7.2.0",
                        "minimumPosVersion": "7.2.0.0",
                            "components": {
            "extend": {
                "triggers": [
                    {
                        "triggerType": "PreEndTransaction",
                        "modulePath": "TriggersHandlers/PreEndTransactionTrigger"
                    }]
            }
        }
    }
    ```
12. **extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**POSAPIExtension** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。
    ```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions2"
            },
            {
                "baseUrl": "POSAPIExtension"
            }
        ]
    }
    ```
    
    > [!NOTE]
    > extension.json ファイルには少なくとも 2 つの拡張子フォルダ名が含まれている必要があるため、**SampleExtensions** フォルダー名は削除しないでください。

13. **tsconfig.json** を開き、拡張パッケージ フォルダーを除外リストからコメントアウトします。 POS では、このファイルを使用して、拡張機能を追加または除外します。 既定では、リストに除外されているすべての拡張子が含まれています。POS の一部である拡張子を含める場合は、拡張フォルダー名を追加し、示されている拡張リストから拡張子をコメント アウトする必要があります。

    > [!NOTE]
    > SampleExtensions2 と POSAPIExtension の両方をコメント アウトします。
    
    
    ```typescript
    "exclude": [

        "AuditEventExtensionSample",
        "B2BSample",
        "CustomerSearchWithAttributesSample",
        "FiscalRegisterSample",
        "PaymentSample",
        "PromotionsSample",
        "SalesTransactionSignatureSample",
        //"SampleExtensions2",
        "SampleExtensions",
        "StoreHoursSample",
        "SuspendTransactionReceiptSample",
        "CustomControlExtensions"
        //"POSAPIExtension"

    ],
    ```
14. **POS 拡張機能** プロジェクトを選択し、ソリューション エクスプローラーで **ファイルをすべて表示** をクリックします。
15. 右クリックし、プロジェクトに **SampleExtensions2** フォルダーを追加します。
16. プロジェクトをコンパイル、およびリビルドします。

## <a name="test-the-extension"></a>拡張のテスト

1.  F5 キーを押し、POS を展開してカスタマイズをテストします。
2.  POS にログインし、任意の品目をトランザクションに追加します。
3.  トランザクションに顧客を追加します。
4.  **支払** ボタンをクリックし、トランザクションをコミットします。 属性を保存するかどうかをたずねるダイアログ ボックスが表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]