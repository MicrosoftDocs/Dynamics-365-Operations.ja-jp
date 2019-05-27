---
title: 販売時点管理 (POS) デュアル ディスプレイ ビューの拡張
description: このトピックでは、ユーザー情報が表示されるように、POS デュアル ディスプレイ ビューを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 728955ecbf1ff0961be3c07b6dedee6a407a005a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537539"
---
# <a name="extend-the-point-of-sale-pos-dual-display-view"></a><span data-ttu-id="4e7d9-103">販売時点管理 (POS) デュアル ディスプレイ ビューの拡張</span><span class="sxs-lookup"><span data-stu-id="4e7d9-103">Extend the point of sale (POS) Dual display view</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4e7d9-104">このトピックでは、ユーザー情報が表示されるように、販売時点管理 (POS) デュアル ディスプレイ ビューを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-104">This topic explains how to extend the point of sale (POS) Dual display view so that it shows custom information.</span></span> <span data-ttu-id="4e7d9-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations 7.2 または Microsoft Dynamics 365 for Retail 7.2 および KB 4091080 とそれ以降のバージョンが適用されます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-105">This topic is applicable to Microsoft Dynamics 365 for Finance and Operations 7.2 or Microsoft Dynamics 365 for Retail 7.2 with KB 4091080, and later versions.</span></span>

<span data-ttu-id="4e7d9-106">POS デュアル ディスプレイ ビューを拡張するには、カスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-106">You can extend the POS Dual display view by adding a custom control.</span></span> <span data-ttu-id="4e7d9-107">カスタム コントロールでは、カスタム情報を表示する画像、POS データ リスト、ラベルなどを追加できます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-107">In the custom control, you can add images, POS data lists, labels, and so on, to show custom information.</span></span>

> [!NOTE]
> <span data-ttu-id="4e7d9-108">POS デュアル ディスプレイ ビューのみを拡張するには、カスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-108">You can extend the POS Dual display view only by adding a custom control.</span></span> <span data-ttu-id="4e7d9-109">カスタム コントロールは、POS デュアル ディスプレイ ビューに表示される標準的な内容を上書きします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-109">The custom control will override the standard content that is shown in the POS Dual display view.</span></span>

## <a name="required-steps"></a><span data-ttu-id="4e7d9-110">必要なステップ</span><span class="sxs-lookup"><span data-stu-id="4e7d9-110">Required steps</span></span>

<span data-ttu-id="4e7d9-111">POS デュアル ディスプレイ ビューをカスタマイズするために必要な手順の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-111">Here is an overview of the steps that are required in order to customize the POS Dual display view.</span></span>

1. <span data-ttu-id="4e7d9-112">デュアル ディスプレイを有効にするハードウェア プロファイルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-112">Configure the hardware profile to enable dual display.</span></span>
2. <span data-ttu-id="4e7d9-113">POS.Extensions プロジェクトに、POS デュアル ディスプレイ ビューの拡張ためのフォルダを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-113">Create a folder in the POS.Extensions project for extension of the POS Dual display view.</span></span>
3. <span data-ttu-id="4e7d9-114">カスタム情報を含む新しいカスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-114">Add a new custom control that includes custom information.</span></span>
4. <span data-ttu-id="4e7d9-115">POS デュアル ディスプレイ ビューの拡張子を使用して、manifest.json ファイルと extensions.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-115">Update the manifest.json and extensions.json files with the extension of the POS Dual display view.</span></span>
5. <span data-ttu-id="4e7d9-116">変更を配置し、カスタマイズを検証します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-116">Deploy the changes, and validate the customization.</span></span>

## <a name="scenario-or-business-problem"></a><span data-ttu-id="4e7d9-117">シナリオまたはビジネスの問題</span><span class="sxs-lookup"><span data-stu-id="4e7d9-117">Scenario or business problem</span></span>

<span data-ttu-id="4e7d9-118">POS デュアル ディスプレイ ビューにカスタム コントロール列を追加して、カートの詳細と顧客および店舗の従業員に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-118">You will add a custom control column in the POS Dual display view to show the cart details and information about the customer and the store employee.</span></span>

## <a name="configure-the-hardware-profile-to-enable-dual-display"></a><span data-ttu-id="4e7d9-119">デュアル ディスプレイを有効にするハードウェア プロファイルをコンフィギュレーションします</span><span class="sxs-lookup"><span data-stu-id="4e7d9-119">Configure the hardware profile to enable dual display</span></span>

1. <span data-ttu-id="4e7d9-120">Retail または Finance and Operations へのサインイン</span><span class="sxs-lookup"><span data-stu-id="4e7d9-120">Sign in to Retail or Finance and Operations.</span></span>
2. <span data-ttu-id="4e7d9-121">**小売 \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-121">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
3. <span data-ttu-id="4e7d9-122">レジスタにリンクしているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-122">Select the hardware profile that is linked to your register.</span></span>
4. <span data-ttu-id="4e7d9-123">**デュアル ディスプレイ**タブで、**デュアル ディスプレイの使用**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-123">On the **Dual display** tab, set the **Dual display in use** option to **Yes**.</span></span>
5. <span data-ttu-id="4e7d9-124">**小売 \> 小売 IT \> 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-124">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
6. <span data-ttu-id="4e7d9-125">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-125">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

> [!NOTE]
> <span data-ttu-id="4e7d9-126">エンド ツー エンド (E2E) サンプルを \\RetailSDK\\POS\\拡張機能\\DualDisplaySample で検索できます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-126">You can find the end-to-end (E2E) sample in …\\RetailSDK\\POS\\Extensions\\DualDisplaySample.</span></span>

## <a name="add-a-new-custom-control-for-extension-of-the-pos-dual-display-view"></a><span data-ttu-id="4e7d9-127">POS デュアル ディスプレイ ビューの拡張子の新しいカスタム コントロールを追加</span><span class="sxs-lookup"><span data-stu-id="4e7d9-127">Add a new custom control for extension of the POS Dual display view</span></span>

1. <span data-ttu-id="4e7d9-128">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-128">Start Microsoft Visual Studio 2015 in Administrator mode.</span></span>
2. <span data-ttu-id="4e7d9-129">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-129">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="4e7d9-130">**POS.Extensions** プロジェクトで、**DualDisplayExtension** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-130">Under the **POS.Extensions** project, create a folder that is named **DualDisplayExtension**.</span></span>
4. <span data-ttu-id="4e7d9-131">**DualDisplayExtension** フォルダーで、**CustomControl** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-131">Under the **DualDisplayExtension** folder, create a folder that is named **CustomControl**.</span></span>
5. <span data-ttu-id="4e7d9-132">**CustomControl** フォルダーで、**DualDisplayCustomControl.html** という HTML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-132">In the **CustomControl** folder, create a HTML file that is named **DualDisplayCustomControl.html**.</span></span>

    <span data-ttu-id="4e7d9-133">HTML ファイルで、買い物カゴの詳細を表示するデータ リスト コントロール、合計金額、顧客名、従業員名、およびサインイン ステータスを表示するテキスト コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-133">In the HTML file, you will add a data list control to show the cart details, and text controls to show the total amount, customer name, employee name, and sign-in status.</span></span>

6. <span data-ttu-id="4e7d9-134">次のコードをコピーして、**DualDisplayCustomControl.html** ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-134">Copy the following code, and paste it into the **DualDisplayCustomControl.html** file.</span></span>

    ```typescript
    <!DOCTYPE html>
    <html lang="en" xmlns="http://www.w3.org/1999/xhtml">
    <head>
    <meta charset="utf-8" />
    <title></title>
    </head>
    <body>
    <!-- Note: The element ID is different from the ID generated by the POS extensibility framework. This 'template' ID is not used by the POS extensibility framework. -->
    <script id="Microsoft_Pos_Extensibility_Samples_DualDisplay" type="text/html">
    <div class="height100Percent width100Percent">
        <div class="height700 width100Percent no-shrink col marginBottom20">
            <div class="col grow marginBottom48">
                <div id="dualDisplayDataListSample" data-bind="msPosDataList: cartLinesDataList">
                </div>
            </div>
        </div>
        <div class="marginBottom20">
            <h2 class="marginLeft8" data-bind="text: cartTotalAmountLabel">Total Amount:</h2>
            <h2 class="marginLeft8" data-bind="text: cartTotalAmount"></h2>
            <h2 class="marginLeft8" data-bind="text: customerNameLabel">Customer Name:</h2>
            <h2 class="marginLeft8" data-bind="text: customerName"></h2>
            <h2 class="marginLeft8" data-bind="text: customerAccountNumberLabel">Customer Account Number:</h2>
            <h2 class="marginLeft8" data-bind="text: customerAccountNumber"></h2>
            <h2 class="marginLeft8" data-bind="text: isLoggedOn() ? 'logged in' : 'logged out'"></h2>
            <h2 class="marginLeft8" data-bind="text: employeeNameLabel">Employee Name:</h2>
            <h2 class="marginLeft8" data-bind="text: employeeName"></h2>
        </div>
    </div>
    </script>
    </body>
    </html>
    ```

    <span data-ttu-id="4e7d9-135">次に、フィールド名をローカライズするために使用されるリソース ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-135">Next, you will add the resource file that is used to localize the field name.</span></span>

7. <span data-ttu-id="4e7d9-136">**DualDisplayExtension** フォルダーで、**Resources** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-136">Under the **DualDisplayExtension** folder, create a folder that is named **Resources**.</span></span>
8. <span data-ttu-id="4e7d9-137">**Resources** フォルダーで、**Strings** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-137">Under the **Resources** folder, create a folder that is named **Strings**.</span></span>
9. <span data-ttu-id="4e7d9-138">**Strings** フォルダーで、**en-US** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-138">Under the **Strings** folder, create a folder that is named **en-US**.</span></span>
10. <span data-ttu-id="4e7d9-139">en-US フォルダで新しいリソース ファイルを追加し、ファイル拡張子を resources.resjson に変更し、および resources.resjson ファイルの中身をコピーし以下のリソース文字列に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-139">In the en-US folder add a new resources file and and change the file extension and name to resources.resjson and inside the resources.resjson file copy paste the below resource strings.</span></span>

    ```typescript
    //======================================================================================================
    //======================================= Sample comment. ==============================================
    //======================================================================================================

    {
        //======================== extensions strings. ========================

        "string_0" : "ID",
        "_string_0.comment" : "Item ID label text",

        "string_1" : "Name",
        "_string_1.comment" : "Item name label text",

        "string_2" : "Quantity",
        "_string_2.comment" : "Item cost label text",

        "string_3" : "Discount",
        "_string_3.comment" : "Total amount label text",

        "string_4" : "Cost",
        "_string_4.comment" : "Item cost label text",

        "string_5" : "Total Amount:",
        "_string_5.comment" : "Total amount label text",

        "string_6" : "Customer Name:",
        "_string_6.comment" : "Customer name label text",

        "string_7" : "Customer Account Number:",
        "_string_7.comment" : "Customer account number label text",

        "string_8" : "Employee Name:",
        "_string_8.comment" : "Employee name label text"
    }
    ```

11. <span data-ttu-id="4e7d9-140">**CustomControl** フォルダーで、**DualDisplayCustomControl.html** という TypeScript ファイル (.ts file) を作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-140">In the **CustomControl** folder, create a TypeScript file (.ts file) that is named **DualDisplayCustomControl.ts**.</span></span>
12. <span data-ttu-id="4e7d9-141">次のコードをコピーして、**DualDisplayCustomControl.ts** ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-141">Copy the following code, and paste it into the **DualDisplayCustomControl.ts** file.</span></span> <span data-ttu-id="4e7d9-142">このコードは関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-142">This code imports the relevant entities and context.</span></span>

    ```typescript
    import {
        DualDisplayCustomControlBase,
        IDualDisplayCustomControlState,
        IDualDisplayCustomControlContext,
        CartChangedData,
        CustomerChangedData,
        LogOnStatusChangedData
    } from "PosApi/Extend/DualDisplay";
    import { DataList, IDataListState, SelectionMode } from "PosUISdk/Controls/DataList";
    import { ObjectExtensions, StringExtensions } from "PosApi/TypeExtensions";
    import { ProxyEntities } from "PosApi/Entities";
    ```

13. <span data-ttu-id="4e7d9-143">**DualDisplayCustomControl.ts** ファイルで、**DualDisplayCustomControl** というクラスを作成し、**DualDisplayCustomControlBase** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-143">In the **DualDisplayCustomControl.ts** file, create a class that is named **DualDisplayCustomControl**, and extend it from the **DualDisplayCustomControlBase** class.</span></span> <span data-ttu-id="4e7d9-144">**DualDisplayCustomControlBase** クラスから拡張し、デュアル ディスプレイで公開されているすべてのイベントを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-144">You extend from the **DualDisplayCustomControlBase** class to get all the events that are exposed for dual display.</span></span>

    ```typescript
    export default class DualDisplayCustomControl extends DualDisplayCustomControlBase { }
    ```

14. <span data-ttu-id="4e7d9-145">**DualDisplayCustomControl** クラス内で、買い物カゴ、顧客、および従業員の詳細を取得するのに次の変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-145">Inside the **DualDisplayCustomControl** class, add the following variables to get the cart, customer, and employee details.</span></span>

    ```typescript
    private static readonly TEMPLATE_ID: string = "Microsoft_Pos_Extensibility_Samples_DualDisplay";

    // The data list to bind against and display with cart line information.

    public readonly cartLinesDataList: DataList<ProxyEntities.CartLine>;

    // Computed values for binding against.

    public readonly cartTotalAmount: Computed<number>;
    public readonly customerName: Computed<string>;
    public readonly customerAccountNumber: Computed<string>;
    public readonly isLoggedOn: Computed<boolean>;
    public readonly employeeName: Computed<string>;

    // Labels for binding against.

    public readonly cartTotalAmountLabel: string;
    public readonly customerNameLabel: string;
    public readonly customerAccountNumberLabel: string;
    public readonly employeeNameLabel: string;

    // Observable values used for keeping track of state.

    private readonly_cart: Observable<ProxyEntities.Cart>;
    private readonly_cartLinesObservable: ObservableArray<ProxyEntities.CartLine>;
    private readonly_customer: Observable<ProxyEntities.Customer>;
    private readonly_loggedOn: Observable<boolean>;
    private readonly_employee: Observable<ProxyEntities.Employee>; private_selectedTenderLines: ProxyEntities.TenderLine[];
    ```

15. <span data-ttu-id="4e7d9-146">クラスのコンストラクター メソッドを作成して、すべての変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-146">Create a class constructor method to initialize all the variables.</span></span>

    ```typescript
    constructor(id: string, context: IDualDisplayCustomControlContext) {
        super(id, context);

        // Initializes labels.

        this.cartTotalAmountLabel = this.context.resources.getString("string_5");
        this.customerNameLabel = this.context.resources.getString("string_6");
        this.customerAccountNumberLabel = this.context.resources.getString("string_7");
        this.employeeNameLabel = this.context.resources.getString("string_8");

        // Initializes observable and computed values.

        this._cart = ko.observable(null);
        this._cartLinesObservable = ko.observableArray([]);
        this._customer = ko.observable(null);
        this._loggedOn = ko.observable(false);
        this._employee = ko.observable(null);
        this.cartTotalAmount = ko.computed(() => {
            return ObjectExtensions.isNullOrUndefined(this._cart()) ? 0.00 : this._cart().TotalAmount;
        });
        this.customerName = ko.computed(() => {
            return ObjectExtensions.isNullOrUndefined(this._customer()) ? StringExtensions.EMPTY : this._customer().Name;
        });
        this.customerAccountNumber = ko.computed(() => {
            return ObjectExtensions.isNullOrUndefined(this._customer()) ? StringExtensions.EMPTY : this._customer().AccountNumber;
        });
        this.isLoggedOn = ko.computed(() => {
            return this._loggedOn();
        });
        this.employeeName = ko.computed(() => {
            return ObjectExtensions.isNullOrUndefined(this._employee()) ? StringExtensions.EMPTY : this._employee().Name;
        });
        this.cartChangedHandler = (data: CartChangedData) => {
            this._cart(data.cart);
            this._cartLinesObservable(ObjectExtensions.isNullOrUndefined(data.cart) ?[] : data.cart.CartLines)
        };
        this.customerChangedHandler = (data: CustomerChangedData) => {
            this._customer(data.customer);
        };
        this.logOnStatusChangedHandler = (data: LogOnStatusChangedData) => {

            // Displays the busy indicator here, even though it's not necessary, in order to showcase and test the scenario.

            this.isProcessing = true;
            window.setTimeout(() => {
                this.isProcessing = false;
            }, 1000);
            this._loggedOn(data.loggedOn);
            this._employee(data.employee);
        }

        // Initializes the cart lines data list

        let cartLinesDataListOptions: IDataListState<ProxyEntities.CartLine> = {
            selectionMode: SelectionMode.None,
            itemDataSource: this._cartLinesObservable,
            columns:[
                {
                    title: context.resources.getString("string_0"), // ID
                    ratio: 20,
                    collapseOrder: 2,
                    minWidth: 50,
                    computeValue: (cartLine: ProxyEntities.CartLine): string => {
                        return ObjectExtensions.isNullOrUndefined(cartLine.ItemId) ? StringExtensions.EMPTY : cartLine.ItemId;
                    }
                },
                {
                    title: context.resources.getString("string_1"), // Name
                    ratio: 50,
                    collapseOrder: 4,
                    minWidth: 100,
                    computeValue: (cartLine: ProxyEntities.CartLine): string => {
                        return ObjectExtensions.isNullOrUndefined(cartLine.Description) ? StringExtensions.EMPTY : cartLine.Description;
                    }
                },
                {
                    title: context.resources.getString("string_2"), // Quantity
                    ratio: 10,
                    collapseOrder: 3,
                    minWidth: 50,
                    computeValue: (cartLine: ProxyEntities.CartLine): string => {
                        return ObjectExtensions.isNullOrUndefined(cartLine.Quantity) ? StringExtensions.EMPTY : cartLine.Quantity.toString();
                    }
                },
                {
                    title: context.resources.getString("string_3"), // Discount
                    ratio: 10,
                    collapseOrder: 1,
                    minWidth: 50,
                    computeValue: (cartLine: ProxyEntities.CartLine): string => {
                        return ObjectExtensions.isNullOrUndefined(cartLine.DiscountAmount) ? StringExtensions.EMPTY : cartLine.DiscountAmount.toString();
                    }
                },
                {
                    title: context.resources.getString("string_4"), // Cost
                    ratio: 10,
                    collapseOrder: 5,
                    minWidth: 50,
                    computeValue: (cartLine: ProxyEntities.CartLine): string => {
                        return ObjectExtensions.isNullOrUndefined(cartLine.TotalAmount) ? StringExtensions.EMPTY : cartLine.TotalAmount.toString();
                    }
                }
            ]
        };
        this.cartLinesDataList = new DataList(cartLinesDataListOptions);

        // Logs the completion of constructing the DualDisplayCustomControl.

        this.context.logger.logInformational("DualDisplayCustomControl constructed", this.context.logger.getNewCorrelationId());
    }
    ```

16. <span data-ttu-id="4e7d9-147">**onReady** メソッドを追加して、コントロールを指定した HTML 要素にバインドします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-147">Add the **onReady** method to bind the control to the specified HTML element.</span></span>

    ```typescript
    /**
    * Binds the control to the specified element.
    * @param {HTMLElement} element The element to which the control should be bound.
    */

    public onReady(element: HTMLElement): void {
        ko.applyBindingsToNode(element, {
            template: {
                name: DualDisplayCustomControl.TEMPLATE_ID,
                data: this
            }
        });
    }
    ```

17. <span data-ttu-id="4e7d9-148">すべてのコントロールを初期化する **init** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-148">Add the **init** method to initialize all the controls.</span></span>

    ```typescript
    /**
    * Initializes the control.
    * @param {IDualDisplayCustomControlState} state The initial state of the page used to initialize the control.
    */

    public init(state: IDualDisplayCustomControlState): void {
        this._cart(state.cart);
        this._customer(state.customer);
        this._loggedOn(state.loggedOn);
        this._employee(state.employee)
    }
    ```

    <span data-ttu-id="4e7d9-149">全体のクラスがどのように見えるかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-149">Here is what the overall class should look like.</span></span>

    ```typescript
    /**
    * SAMPLE CODE NOTICE
    *
    * THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
    * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
    * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
    * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
    */

    import {
        DualDisplayCustomControlBase,
        IDualDisplayCustomControlState,
        IDualDisplayCustomControlContext,
        CartChangedData,
        CustomerChangedData,
        LogOnStatusChangedData
    } from "PosApi/Extend/DualDisplay";
    import { DataList, IDataListState, SelectionMode } from "PosUISdk/Controls/DataList";
    import { ObjectExtensions, StringExtensions } from "PosApi/TypeExtensions";
    import { ProxyEntities } from "PosApi/Entities";
    export default class DualDisplayCustomControl extends DualDisplayCustomControlBase {
        private static readonly TEMPLATE_ID: string = "Microsoft_Pos_Extensibility_Samples_DualDisplay";

        // The data list to bind against and display with cart line information.

        public readonly cartLinesDataList: DataList<ProxyEntities.CartLine>;

        // Computed values for binding against.

        public readonly cartTotalAmount: Computed<number>;
        public readonly customerName: Computed<string>;
        public readonly customerAccountNumber: Computed<string>;
        public readonly isLoggedOn: Computed<boolean>;
        public readonly employeeName: Computed<string>;

        // Labels for binding against.

        public readonly cartTotalAmountLabel: string;
        public readonly customerNameLabel: string;
        public readonly customerAccountNumberLabel: string;
        public readonly employeeNameLabel: string;

        // Observable values used for keeping track of state.

        private readonly_cart: Observable<ProxyEntities.Cart>;
        private readonly_cartLinesObservable: ObservableArray<ProxyEntities.CartLine>;
        private readonly_customer: Observable<ProxyEntities.Customer>;
        private readonly_loggedOn: Observable<boolean>;
        private readonly_employee: Observable<ProxyEntities.Employee>;
        constructor(id: string, context: IDualDisplayCustomControlContext) {
            super(id, context);

            // Initializes labels.

            this.cartTotalAmountLabel = this.context.resources.getString("string_5");
            this.customerNameLabel = this.context.resources.getString("string_6");
            this.customerAccountNumberLabel = this.context.resources.getString("string_7");
            this.employeeNameLabel = this.context.resources.getString("string_8");

            // Initializes observable and computed values.

            this._cart = ko.observable(null);
            this._cartLinesObservable = ko.observableArray([]);
            this._customer = ko.observable(null);
            this._loggedOn = ko.observable(false);
            this._employee = ko.observable(null);
            this.cartTotalAmount = ko.computed(() => {
                return ObjectExtensions.isNullOrUndefined(this._cart()) ? 0.00 : this._cart().TotalAmount;
            });
            this.customerName = ko.computed(() => {
                return ObjectExtensions.isNullOrUndefined(this._customer()) ? StringExtensions.EMPTY : this._customer().Name;
            });
            this.customerAccountNumber = ko.computed(() => {
                return ObjectExtensions.isNullOrUndefined(this._customer()) ? StringExtensions.EMPTY : this._customer().AccountNumber;
            });
            this.isLoggedOn = ko.computed(() => {
                return this._loggedOn();
            });
            this.employeeName = ko.computed(() => {
                return ObjectExtensions.isNullOrUndefined(this._employee()) ? StringExtensions.EMPTY : this._employee().Name;
            });
            this.cartChangedHandler = (data: CartChangedData) => {
                this._cart(data.cart);
                this._cartLinesObservable(ObjectExtensions.isNullOrUndefined(data.cart) ?[] : data.cart.CartLines)
            };
            this.customerChangedHandler = (data: CustomerChangedData) => {
                this._customer(data.customer);
            };
            this.logOnStatusChangedHandler = (data: LogOnStatusChangedData) => {

                // Displays the busy indicator here, even though it's not necessary, in order to showcase and test the scenario.

                this.isProcessing = true;
                window.setTimeout(() => {
                    this.isProcessing = false;
                }, 1000);
                this._loggedOn(data.loggedOn);
                this._employee(data.employee);
            }

            // Initializes the cart lines data list

            let cartLinesDataListOptions: IDataListState<ProxyEntities.CartLine> = {
                selectionMode: SelectionMode.None,
                itemDataSource: this._cartLinesObservable,
                columns:[
                    {
                        title: context.resources.getString("string_0"), // ID
                        ratio: 20,
                        collapseOrder: 2,
                        minWidth: 50,
                        computeValue: (cartLine: ProxyEntities.CartLine): string => {
                            return ObjectExtensions.isNullOrUndefined(cartLine.ItemId) ? StringExtensions.EMPTY : cartLine.ItemId;
                        }
                    },
                    {
                        title: context.resources.getString("string_1"), // Name
                        ratio: 50,
                        collapseOrder: 4,
                        minWidth: 100,
                        computeValue: (cartLine: ProxyEntities.CartLine): string => {
                            return ObjectExtensions.isNullOrUndefined(cartLine.Description) ? StringExtensions.EMPTY : cartLine.Description;
                        }
                    },
                    {
                        title: context.resources.getString("string_2"), // Quantity
                        ratio: 10,
                        collapseOrder: 3,
                        minWidth: 50,
                        computeValue: (cartLine: ProxyEntities.CartLine): string => {
                            return ObjectExtensions.isNullOrUndefined(cartLine.Quantity) ? StringExtensions.EMPTY : cartLine.Quantity.toString();
                        }
                    },
                    {
                        title: context.resources.getString("string_3"), // Discount
                        ratio: 10,
                        collapseOrder: 1,
                        minWidth: 50,
                        computeValue: (cartLine: ProxyEntities.CartLine): string => {
                            return ObjectExtensions.isNullOrUndefined(cartLine.DiscountAmount) ? StringExtensions.EMPTY : cartLine.DiscountAmount.toString();
                        }
                    },
                    {
                        title: context.resources.getString("string_4"), // Cost
                        ratio: 10,
                        collapseOrder: 5,
                        minWidth: 50,
                        computeValue: (cartLine: ProxyEntities.CartLine): string => {
                            return ObjectExtensions.isNullOrUndefined(cartLine.TotalAmount) ? StringExtensions.EMPTY : cartLine.TotalAmount.toString();
                        }
                    }
                ]
            };
            this.cartLinesDataList = new DataList(cartLinesDataListOptions);

            // Logs the completion of constructing the DualDisplayCustomControl.

            this.context.logger.logInformational("DualDisplayCustomControl constructed", this.context.logger.getNewCorrelationId());
        }

        /**
        * Binds the control to the specified element.
        * @param {HTMLElement} element The element to which the control should be bound.
        */

        public onReady(element: HTMLElement): void {
            ko.applyBindingsToNode(element, {
                template: {
                    name: DualDisplayCustomControl.TEMPLATE_ID,
                    data: this
                }
            });
        }

        /**
        * Initializes the control.
        * @param {IDualDisplayCustomControlState} state The initial state of the page used to initialize the control.
        */

        public init(state: IDualDisplayCustomControlState): void {
            this._cart(state.cart);
            this._customer(state.customer);
            this._loggedOn(state.loggedOn);
            this._employee(state.employee)
        }
    }
    ``` 

18. <span data-ttu-id="4e7d9-150">**DualDisplayExtension** フォルダーで、**manifest.json** という名前の JavaScript Object Notation (JSON) ファイル (.json ファイル) を作成します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-150">In the **DualDisplayExtension** folder, create a JavaScript Object Notation (JSON) file (.json file) that is named **manifest.json**.</span></span>
19. <span data-ttu-id="4e7d9-151">次のコードをコピーして、**manifest.json** ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-151">Copy the following code, and paste it into the **manifest.json** file.</span></span> <span data-ttu-id="4e7d9-152">このコードをコピーする前に、既定で生成されたコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-152">Delete the default generated code before you copy this code.</span></span>

    ```typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_DualDisplaySample",
        "publisher": "Microsoft",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
            "resources": {
                "supportedUICultures": [ "en-US" ],
                "fallbackUICulture": "en-US",
                "culturesDirectoryPath": "Resources/Strings",
                "stringResourcesFileName": "resources.resjson"
            },
            "dualDisplay": {
                "customControl": {
                    "controlName": "DualDisplayCustomControl",
                    "htmlPath": "CustomControl/DualDisplayCustomControl.html",
                    "modulePath": "CustomControl/DualDisplayCustomControl"
                }
            }
        }
    }
    ```

20. <span data-ttu-id="4e7d9-153">**extensions.json**ファイルを **POS.Extensions** プロジェクトで開いて、**DualDisplayExtension** サンプルで更新します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-153">Open the **extensions.json** file under the **POS.Extensions** project, and update it with the **DualDisplayExtension** samples.</span></span> <span data-ttu-id="4e7d9-154">このようにして、実行時に POS にこの拡張が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-154">In that way, the POS will include this extension during runtime.</span></span>

    ```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions"
            },
            {
                "baseUrl": " SampleExtensions2"
            },
            {
                "baseUrl": " DualDisplayExtension"
            }
        ]
    }
    ```

21. <span data-ttu-id="4e7d9-155">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストでコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-155">Open the **tsconfig.json** file, and comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="4e7d9-156">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-156">The POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="4e7d9-157">既定では、リストにすべての除外された拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-157">By default, the list contains all the excluded extensions.</span></span> <span data-ttu-id="4e7d9-158">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、拡張リストの拡張をコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-158">If you want to include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the extension list, as shown here.</span></span>

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
        "SuspendTransactionReceiptSample"
        //"SampleExtensions",
        //"DualDisplayExtension"
    ],
    ```

22. <span data-ttu-id="4e7d9-159">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-159">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="4e7d9-160">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="4e7d9-160">Validate the customization</span></span>

1. <span data-ttu-id="4e7d9-161">オペレーター ID に **000160**、パスワードに **123** を使用して Retail Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-161">Sign in to Retail Modern POS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="4e7d9-162">ようこそ画面で、**現在のトランザクション**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-162">On the welcome screen, select the **Current transaction** button.</span></span>
3. <span data-ttu-id="4e7d9-163">品目をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-163">Add any item to the transaction.</span></span> <span data-ttu-id="4e7d9-164">たとえば、品目番号 **0005** を追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-164">For example, add item number **0005**.</span></span>
4. <span data-ttu-id="4e7d9-165">顧客をトランザクションへ追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-165">Add any customer to transaction.</span></span> <span data-ttu-id="4e7d9-166">たとえば、**Karen Berg** を追加します。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-166">For example, add **Karen Berg**.</span></span>
5. <span data-ttu-id="4e7d9-167">デュアル ディスプレイには、買い物カゴ、合計、従業員、および顧客の詳細が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e7d9-167">The dual display should show the cart, total, employee, and customer details.</span></span>
