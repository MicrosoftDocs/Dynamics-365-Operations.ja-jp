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
# <a name="call-point-of-sale-pos-apis-or-operations-from-pos-extensions"></a><span data-ttu-id="7ba5f-103">販売時点管理 (POS) API または POS 拡張からの工程を呼び出す</span><span class="sxs-lookup"><span data-stu-id="7ba5f-103">Call point of sale (POS) APIs or operations from POS extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ba5f-104">Retail POS API を使用すると、拡張機能を構築したり、POS に新しい機能を追加したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-104">The Retail POS APIs help you to build extensions or add new features to POS.</span></span> <span data-ttu-id="7ba5f-105">たとえば、製品の詳細を取得し、価格を変更し、またはカートに品目を追加する新しい機能を追加する場合は、その作業を行うための POS API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-105">For example, if you wanted to add new features that would retrieve product details, change a price, or add an item to a cart, you would call the POS APIs to do that work.</span></span> <span data-ttu-id="7ba5f-106">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-106">The POS APIs simplify the extension pattern and provide continuous support to build the extensions.</span></span> <span data-ttu-id="7ba5f-107">Commerce Runtime (RT)、POS、およびハードウェア ステーションの拡張パターンはすべて、要求/応答パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-107">The extension patterns for Commerce Runtime (RT), POS, and Hardware Station now all use the request/response pattern.</span></span> 

<span data-ttu-id="7ba5f-108">このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-108">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="7ba5f-109">シナリオ</span><span class="sxs-lookup"><span data-stu-id="7ba5f-109">Scenarios</span></span>
<span data-ttu-id="7ba5f-110">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-110">The POS APIs are categorized into three different scenarios.</span></span>

- <span data-ttu-id="7ba5f-111">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-111">**Consume** - Consume the public APIs in your extension.</span></span> 
- <span data-ttu-id="7ba5f-112">**拡張** - 一部の追加ロジックを実行するパブリック API を拡張します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-112">**Extend** - Extend the public APIs to do some additional logic.</span></span> 
- <span data-ttu-id="7ba5f-113">**作成** - POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-113">**Create** - Create new APIs using the POS interface, which can then be used across your extensions.</span></span> 

## <a name="consume-pos-apis-in-extensions"></a><span data-ttu-id="7ba5f-114">拡張機能で POS API を使用する</span><span class="sxs-lookup"><span data-stu-id="7ba5f-114">Consume POS APIs in extensions</span></span>
<span data-ttu-id="7ba5f-115">API は要求/応答パターンを使用して公開されるため、ビジネス ロジックを実装するための外部 Web サービス呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-115">Because the APIs are exposed using a request/response pattern, you can make an external web service call to implement your business logic.</span></span> <span data-ttu-id="7ba5f-116">たとえばが、品目の価格を変更する場合、**PriceOverrideOperationRequest** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-116">For example, is you wanted to change the price of an item, you would call **PriceOverrideOperationRequest**.</span></span> <span data-ttu-id="7ba5f-117">API は、CRT、周辺機器、保存操作などのモジュールによりサブカテゴリ化されます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-117">The APIs are subcategorized by modules such as CRT, peripherals, and store operations.</span></span> 

<span data-ttu-id="7ba5f-118">多くの新しい API が追加されました。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-118">Many new APIs have been added.</span></span> <span data-ttu-id="7ba5f-119">すべての API のリストは **…Retail SDK\\POS\\Extensions\\Pos.Api.d.ts** ファイルで探すことができます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-119">You can find a list of all the APIs in the file **…Retail SDK\\POS\\Extensions\\Pos.Api.d.ts**.</span></span> 

### <a name="how-to-consume-an-api-in-an-extension"></a><span data-ttu-id="7ba5f-120">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="7ba5f-120">How to consume an API in an extension</span></span>
<span data-ttu-id="7ba5f-121">拡張機能で  API を使用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-121">To consume APIs in an extension, follow these steps:</span></span>

1. <span data-ttu-id="7ba5f-122">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-122">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="7ba5f-123">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-123">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="7ba5f-124">**POS.Extensions** プロジェクトで、**POSAPIExtension** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-124">Under the **POS.Extensions** project create a new folder named **POSAPIExtension**.</span></span>
4. <span data-ttu-id="7ba5f-125">**POSAPIExtension** の下で **TriggersHandlers** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-125">Under **POSAPIExtension**, create a new folder named **TriggersHandlers**.</span></span>
5. <span data-ttu-id="7ba5f-126">**TriggersHandlers** フォルダーに、新しい Typescript ファイルを追加し、**PreEndTransactionTrigger.ts** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-126">In the **TriggersHandlers** folder, add a new Typescript file and name it **PreEndTransactionTrigger.ts**.</span></span>
6. <span data-ttu-id="7ba5f-127">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-127">Add the following **import** statements to import the relevant entities and context.</span></span>
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
7. <span data-ttu-id="7ba5f-128">**PreEndTransactionTrigger** と呼ばれる新しいクラスを作成し、**PreEndTransactionTrigger** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-128">Create a new class called **PreEndTransactionTrigger** and extend it from **PreEndTransactionTrigger**.</span></span>
    ```typescript
        export default class PreEndTransactionTrigger extends Triggers.PreEndTransactionTrigger { }
    ```
8. <span data-ttu-id="7ba5f-129">クラス内で、属性名と値の例に対して次の変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-129">Inside the class declare the following variables for the attributes names and sample values.</span></span>
    ```typescript
    private static CART_ATTRIBUTE_NAME: string = "ATT SAMPLE";
    private static CART_ATTRIBUTE_VALUE_TRUE: string = "True";
    private static CART_ATTRIBUTE_VALUE_FALSE: string = "False";
    private static DIALOG_RESULT_YES: string = "yes";
    private static DIALOG_RESULT_NO: string = "no";
    private static DIALOG_YES_BUTTON_ID: string = "CART_PreEndTransactionTrigger_MessageDialog_Yes";
    private static DIALOG_NO_BUTTON_ID: string = "CART_PreEndTransactionTrigger_MessageDialog_No";
    ```
9. <span data-ttu-id="7ba5f-130">トリガー **実行** メソッドを実装し、既存の POS API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-130">Implement the trigger **execute** method and call the existing POS APIs.</span></span> <span data-ttu-id="7ba5f-131">**execute** メソッドは、API を呼び出して現在の買い物カゴと顧客を取得し、買い物カゴに属性を保存します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-131">The **execute** method calls APIs to get the current cart and customer, and then saves the attributes on the cart.</span></span>
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

    <span data-ttu-id="7ba5f-132">全体的なコードは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-132">The overall code should look like the following example.</span></span> 
    
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
10. <span data-ttu-id="7ba5f-133">新しい json ファイルを POSAPIExtension フォルダーの下に作成し、manifest.json という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-133">Create a new json file under the POSAPIExtension folder and name it manifest.json.</span></span>

11. <span data-ttu-id="7ba5f-134">manifest.json ファイルに、次のコードをコピーして貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-134">In the manifest.json file, copy and paste the following code.</span></span> <span data-ttu-id="7ba5f-135">このコードをコピーする前に、既定で生成されたコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-135">Delete the default generated code before copying this code.</span></span>
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
12. <span data-ttu-id="7ba5f-136">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**POSAPIExtension** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-136">Open the **extensions.json** file under the **POS.Extensions** project and update it with the **POSAPIExtension** samples, so that POS during runtime will include this extension.</span></span>
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
    > <span data-ttu-id="7ba5f-137">extension.json ファイルには少なくとも 2 つの拡張子フォルダ名が含まれている必要があるため、**SampleExtensions** フォルダー名は削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-137">The extension.json file must contain at least two extensions folder names so don’t remove the **SampleExtensions** folder name.</span></span>

13. <span data-ttu-id="7ba5f-138">**tsconfig.json** を開き、拡張パッケージ フォルダーを除外リストからコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-138">Open **tsconfig.json** and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="7ba5f-139">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-139">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="7ba5f-140">既定では、リストに除外されているすべての拡張子が含まれています。POS の一部である拡張子を含める場合は、拡張フォルダー名を追加し、示されている拡張リストから拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-140">By default, the list contains all the excluded extensions, if you want to include any extensions that are part of the POS, then you need add the extension folder name and comment out the extension from the extension list as shown.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ba5f-141">SampleExtensions2 と POSAPIExtension の両方をコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-141">Comment out both SampleExtensions2 and POSAPIExtension.</span></span>
    
    
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
14. <span data-ttu-id="7ba5f-142">**POS 拡張機能** プロジェクトを選択し、ソリューション エクスプローラーで **ファイルをすべて表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-142">Select the **POS.Extensions** project and click **Show all Files** in Solution Explorer.</span></span>
15. <span data-ttu-id="7ba5f-143">右クリックし、プロジェクトに **SampleExtensions2** フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-143">Right-click and include the **SampleExtensions2** folder in the project.</span></span>
16. <span data-ttu-id="7ba5f-144">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-144">Compile and rebuild the project.</span></span>

## <a name="test-the-extension"></a><span data-ttu-id="7ba5f-145">拡張のテスト</span><span class="sxs-lookup"><span data-stu-id="7ba5f-145">Test the extension</span></span>

1.  <span data-ttu-id="7ba5f-146">F5 キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-146">Press F5 and deploy the POS to test your customization.</span></span>
2.  <span data-ttu-id="7ba5f-147">POS にログインし、任意の品目をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-147">Sign in to POS and add any item to a transaction.</span></span>
3.  <span data-ttu-id="7ba5f-148">トランザクションに顧客を追加します。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-148">Add any customer to a transaction.</span></span>
4.  <span data-ttu-id="7ba5f-149">**支払** ボタンをクリックし、トランザクションをコミットします。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-149">Click the **Pay** button and commit the transaction.</span></span> <span data-ttu-id="7ba5f-150">属性を保存するかどうかをたずねるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ba5f-150">A dialog box should display asking if you want to save the attribute.</span></span>
