---
title: 販売時点管理 (POS) デュアル ディスプレイ ビューの拡張
description: このトピックでは、ユーザー情報が表示されるように、POS デュアル ディスプレイ ビューを拡張する方法について説明します。
author: mugunthanm
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 9d2bc42d4da0b13bb882b2708d6fb6944ad739cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792993"
---
# <a name="extend-the-point-of-sale-pos-dual-display-view"></a><span data-ttu-id="2f395-103">販売時点管理 (POS) デュアル ディスプレイ ビューの拡張</span><span class="sxs-lookup"><span data-stu-id="2f395-103">Extend the point of sale (POS) Dual display view</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2f395-104">このトピックでは、ユーザー情報が表示されるように、販売時点管理 (POS) デュアル ディスプレイ ビューを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f395-104">This topic explains how to extend the point of sale (POS) Dual display view so that it shows custom information.</span></span> <span data-ttu-id="2f395-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations 7.2 または Microsoft Dynamics 365 Retail 7.2 および KB 4091080 とそれ以降のバージョンが適用されます。</span><span class="sxs-lookup"><span data-stu-id="2f395-105">This topic is applicable to Microsoft Dynamics 365 for Finance and Operations 7.2 or Microsoft Dynamics 365 Retail 7.2 with KB 4091080, and later versions.</span></span>

<span data-ttu-id="2f395-106">POS デュアル ディスプレイ ビューを拡張するには、カスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-106">You can extend the POS Dual display view by adding a custom control.</span></span> <span data-ttu-id="2f395-107">カスタム コントロールでは、カスタム情報を表示する画像、POS データ リスト、ラベルなどを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f395-107">In the custom control, you can add images, POS data lists, labels, and so on, to show custom information.</span></span>

> [!NOTE]
> <span data-ttu-id="2f395-108">POS デュアル ディスプレイ ビューのみを拡張するには、カスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-108">You can extend the POS Dual display view only by adding a custom control.</span></span> <span data-ttu-id="2f395-109">カスタム コントロールは、POS デュアル ディスプレイ ビューに表示される標準的な内容を上書きします。</span><span class="sxs-lookup"><span data-stu-id="2f395-109">The custom control will override the standard content that is shown in the POS Dual display view.</span></span> <span data-ttu-id="2f395-110">デュアル ディスプレイ カスタム コントロールとデュアル ディスプレイに関連するその他の拡張機能の詳細情報は、拡張機能の詳細ビューには表示されません。</span><span class="sxs-lookup"><span data-stu-id="2f395-110">The dual display custom control and other extension details information related to dual display will not be shown in the extension details view.</span></span>

## <a name="required-steps"></a><span data-ttu-id="2f395-111">必要なステップ</span><span class="sxs-lookup"><span data-stu-id="2f395-111">Required steps</span></span>

<span data-ttu-id="2f395-112">POS デュアル ディスプレイ ビューをカスタマイズするために必要な手順の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="2f395-112">Here is an overview of the steps that are required in order to customize the POS Dual display view.</span></span>

1. <span data-ttu-id="2f395-113">デュアル ディスプレイを有効にするハードウェア プロファイルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2f395-113">Configure the hardware profile to enable dual display.</span></span>
2. <span data-ttu-id="2f395-114">POS.Extensions プロジェクトに、POS デュアル ディスプレイ ビューの拡張ためのフォルダを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-114">Create a folder in the POS.Extensions project for extension of the POS Dual display view.</span></span>
3. <span data-ttu-id="2f395-115">カスタム情報を含む新しいカスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-115">Add a new custom control that includes custom information.</span></span>
4. <span data-ttu-id="2f395-116">POS デュアル ディスプレイ ビューの拡張子を使用して、manifest.json ファイルと extensions.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="2f395-116">Update the manifest.json and extensions.json files with the extension of the POS Dual display view.</span></span>
5. <span data-ttu-id="2f395-117">変更を配置し、カスタマイズを検証します。</span><span class="sxs-lookup"><span data-stu-id="2f395-117">Deploy the changes, and validate the customization.</span></span>

## <a name="scenario-or-business-problem"></a><span data-ttu-id="2f395-118">シナリオまたはビジネスの問題</span><span class="sxs-lookup"><span data-stu-id="2f395-118">Scenario or business problem</span></span>

<span data-ttu-id="2f395-119">POS デュアル ディスプレイ ビューにカスタム コントロール列を追加して、カートの詳細と顧客および店舗の従業員に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="2f395-119">You will add a custom control column in the POS Dual display view to show the cart details and information about the customer and the store employee.</span></span>

## <a name="configure-the-hardware-profile-to-enable-dual-display"></a><span data-ttu-id="2f395-120">デュアル ディスプレイを有効にするハードウェア プロファイルをコンフィギュレーションします</span><span class="sxs-lookup"><span data-stu-id="2f395-120">Configure the hardware profile to enable dual display</span></span>

1. <span data-ttu-id="2f395-121">クライアントにサイン インします。</span><span class="sxs-lookup"><span data-stu-id="2f395-121">Sign in to the client.</span></span>
2. <span data-ttu-id="2f395-122">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f395-122">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
3. <span data-ttu-id="2f395-123">レジスタにリンクしているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f395-123">Select the hardware profile that is linked to your register.</span></span>
4. <span data-ttu-id="2f395-124">**デュアル ディスプレイ** タブで、**デュアル ディスプレイの使用** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f395-124">On the **Dual display** tab, set the **Dual display in use** option to **Yes**.</span></span>
5. <span data-ttu-id="2f395-125">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f395-125">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
6. <span data-ttu-id="2f395-126">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f395-126">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

> [!NOTE]
> <span data-ttu-id="2f395-127">エンド ツー エンド (E2E) サンプルを \\RetailSDK\\POS\\拡張機能\\DualDisplaySample で検索できます。</span><span class="sxs-lookup"><span data-stu-id="2f395-127">You can find the end-to-end (E2E) sample in …\\RetailSDK\\POS\\Extensions\\DualDisplaySample.</span></span>

## <a name="add-a-new-custom-control-for-extension-of-the-pos-dual-display-view"></a><span data-ttu-id="2f395-128">POS デュアル ディスプレイ ビューの拡張子の新しいカスタム コントロールを追加</span><span class="sxs-lookup"><span data-stu-id="2f395-128">Add a new custom control for extension of the POS Dual display view</span></span>

1. <span data-ttu-id="2f395-129">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="2f395-129">Start Microsoft Visual Studio 2015 in Administrator mode.</span></span>
2. <span data-ttu-id="2f395-130">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="2f395-130">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="2f395-131">**POS.Extensions** プロジェクトで、**DualDisplayExtension** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-131">Under the **POS.Extensions** project, create a folder that is named **DualDisplayExtension**.</span></span>
4. <span data-ttu-id="2f395-132">**DualDisplayExtension** フォルダーで、**CustomControl** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-132">Under the **DualDisplayExtension** folder, create a folder that is named **CustomControl**.</span></span>
5. <span data-ttu-id="2f395-133">**CustomControl** フォルダーで、**DualDisplayCustomControl.html** という HTML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-133">In the **CustomControl** folder, create a HTML file that is named **DualDisplayCustomControl.html**.</span></span>

    <span data-ttu-id="2f395-134">HTML ファイルで、買い物カゴの詳細を表示するデータ リスト コントロール、合計金額、顧客名、従業員名、およびサインイン ステータスを表示するテキスト コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-134">In the HTML file, you will add a data list control to show the cart details, and text controls to show the total amount, customer name, employee name, and sign-in status.</span></span>

6. <span data-ttu-id="2f395-135">次のコードをコピーして、**DualDisplayCustomControl.html** ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2f395-135">Copy the following code, and paste it into the **DualDisplayCustomControl.html** file.</span></span>

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

    <span data-ttu-id="2f395-136">次に、フィールド名をローカライズするために使用されるリソース ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-136">Next, you will add the resource file that is used to localize the field name.</span></span>

7. <span data-ttu-id="2f395-137">**DualDisplayExtension** フォルダーで、**Resources** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-137">Under the **DualDisplayExtension** folder, create a folder that is named **Resources**.</span></span>
8. <span data-ttu-id="2f395-138">**Resources** フォルダーで、**Strings** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-138">Under the **Resources** folder, create a folder that is named **Strings**.</span></span>
9. <span data-ttu-id="2f395-139">**Strings** フォルダーで、**en-US** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-139">Under the **Strings** folder, create a folder that is named **en-US**.</span></span>
10. <span data-ttu-id="2f395-140">en-US フォルダで新しいリソース ファイルを追加し、ファイル拡張子を resources.resjson に変更し、および resources.resjson ファイルの中身をコピーし以下のリソース文字列に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2f395-140">In the en-US folder add a new resources file and and change the file extension and name to resources.resjson and inside the resources.resjson file copy paste the below resource strings.</span></span>

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

11. <span data-ttu-id="2f395-141">**CustomControl** フォルダーで、**DualDisplayCustomControl.html** という TypeScript ファイル (.ts file) を作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-141">In the **CustomControl** folder, create a TypeScript file (.ts file) that is named **DualDisplayCustomControl.ts**.</span></span>
12. <span data-ttu-id="2f395-142">次のコードをコピーして、**DualDisplayCustomControl.ts** ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2f395-142">Copy the following code, and paste it into the **DualDisplayCustomControl.ts** file.</span></span> <span data-ttu-id="2f395-143">このコードは関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="2f395-143">This code imports the relevant entities and context.</span></span>

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

13. <span data-ttu-id="2f395-144">**DualDisplayCustomControl.ts** ファイルで、**DualDisplayCustomControl** というクラスを作成し、**DualDisplayCustomControlBase** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="2f395-144">In the **DualDisplayCustomControl.ts** file, create a class that is named **DualDisplayCustomControl**, and extend it from the **DualDisplayCustomControlBase** class.</span></span> <span data-ttu-id="2f395-145">**DualDisplayCustomControlBase** クラスから拡張し、デュアル ディスプレイで公開されているすべてのイベントを取得します。</span><span class="sxs-lookup"><span data-stu-id="2f395-145">You extend from the **DualDisplayCustomControlBase** class to get all the events that are exposed for dual display.</span></span>

    ```typescript
    export default class DualDisplayCustomControl extends DualDisplayCustomControlBase { }
    ```

14. <span data-ttu-id="2f395-146">**DualDisplayCustomControl** クラス内で、買い物カゴ、顧客、および従業員の詳細を取得するのに次の変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-146">Inside the **DualDisplayCustomControl** class, add the following variables to get the cart, customer, and employee details.</span></span>

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

15. <span data-ttu-id="2f395-147">クラスのコンストラクター メソッドを作成して、すべての変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="2f395-147">Create a class constructor method to initialize all the variables.</span></span>

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

16. <span data-ttu-id="2f395-148">**onReady** メソッドを追加して、コントロールを指定した HTML 要素にバインドします。</span><span class="sxs-lookup"><span data-stu-id="2f395-148">Add the **onReady** method to bind the control to the specified HTML element.</span></span>

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

17. <span data-ttu-id="2f395-149">すべてのコントロールを初期化する **init** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-149">Add the **init** method to initialize all the controls.</span></span>

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

    <span data-ttu-id="2f395-150">全体のクラスがどのように見えるかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2f395-150">Here is what the overall class should look like.</span></span>

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

18. <span data-ttu-id="2f395-151">**DualDisplayExtension** フォルダーで、**manifest.json** という名前の JavaScript Object Notation (JSON) ファイル (.json ファイル) を作成します。</span><span class="sxs-lookup"><span data-stu-id="2f395-151">In the **DualDisplayExtension** folder, create a JavaScript Object Notation (JSON) file (.json file) that is named **manifest.json**.</span></span>
19. <span data-ttu-id="2f395-152">次のコードをコピーして、**manifest.json** ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2f395-152">Copy the following code, and paste it into the **manifest.json** file.</span></span> <span data-ttu-id="2f395-153">このコードをコピーする前に、既定で生成されたコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="2f395-153">Delete the default generated code before you copy this code.</span></span>

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

20. <span data-ttu-id="2f395-154">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**DualDisplayExtension** サンプルで更新します。</span><span class="sxs-lookup"><span data-stu-id="2f395-154">Open the **extensions.json** file under the **POS.Extensions** project, and update it with the **DualDisplayExtension** samples.</span></span> <span data-ttu-id="2f395-155">このようにして、実行時に POS にこの拡張が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f395-155">In that way, the POS will include this extension during runtime.</span></span>

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

21. <span data-ttu-id="2f395-156">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストでコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="2f395-156">Open the **tsconfig.json** file, and comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="2f395-157">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="2f395-157">The POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="2f395-158">既定では、リストにすべての除外された拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f395-158">By default, the list contains all the excluded extensions.</span></span> <span data-ttu-id="2f395-159">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、拡張リストの拡張をコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="2f395-159">If you want to include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the extension list, as shown here.</span></span>

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

22. <span data-ttu-id="2f395-160">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="2f395-160">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="2f395-161">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="2f395-161">Validate the customization</span></span>

1. <span data-ttu-id="2f395-162">オペレーター ID に **000160**、パスワードに **123** を使用して Retail Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2f395-162">Sign in to Retail Modern POS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="2f395-163">ようこそ画面で、**現在のトランザクション** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f395-163">On the welcome screen, select the **Current transaction** button.</span></span>
3. <span data-ttu-id="2f395-164">品目をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-164">Add any item to the transaction.</span></span> <span data-ttu-id="2f395-165">たとえば、品目番号 **0005** を追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-165">For example, add item number **0005**.</span></span>
4. <span data-ttu-id="2f395-166">顧客をトランザクションへ追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-166">Add any customer to transaction.</span></span> <span data-ttu-id="2f395-167">たとえば、**Karen Berg** を追加します。</span><span class="sxs-lookup"><span data-stu-id="2f395-167">For example, add **Karen Berg**.</span></span>
5. <span data-ttu-id="2f395-168">デュアル ディスプレイには、買い物カゴ、合計、従業員、および顧客の詳細が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f395-168">The dual display should show the cart, total, employee, and customer details.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]