---
title: 非画面デザイナー ベース POS ビューへのカスタム コントロールの追加
description: このトピックでは、非画面レイアウト デザイナー ベース ビューにカスタム コントロールを追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 12/08/2017
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
ms.openlocfilehash: 6745f9bda9bab80e58783077508e84b145f09a4f
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129141"
---
# <a name="add-custom-controls-to-non-screen-designer-based-pos-views"></a><span data-ttu-id="4f13d-103">非画面デザイナー ベース POS ビューへのカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="4f13d-103">Add custom controls to non-screen designer-based POS views</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f13d-104">カスタム コントロールを追加することにより、Dynamics 365 Commerce POS ビューに表示される情報を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-104">You can enhance the information displayed on a Dynamics 365 Commerce POS view by adding custom controls.</span></span> <span data-ttu-id="4f13d-105">カスタム コントロールを使用すると、POS の既存のビューにカスタム情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-105">A custom control allows you to add your own custom information to the existing POS views.</span></span> <span data-ttu-id="4f13d-106">カスタム コントロールは、POS 拡張フレームワークを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-106">Custom controls can be implemented by using the POS extension framework.</span></span> <span data-ttu-id="4f13d-107">現時点では、実行時にカスタム コントロールを目的の場所に配置することはできません。POS は POS を固定位置にロードします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-107">Currently, you cannot place the custom control in the desired location, at runtime, POS will load it in a fixed position.</span></span>

<span data-ttu-id="4f13d-108">このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-108">This topic applies to Dynamics 365 for Finance and Operations, and Dynamics 365 Retail with Platform update 8, and Retail Application update 4 hotfix.</span></span> 

<span data-ttu-id="4f13d-109">次のテーブルに、カスタム コントロールをサポートする非画面レイアウト デザイナーベース ビューを示します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-109">The following table lists the non-screen layout designer-based views that support custom controls.</span></span>

| <span data-ttu-id="4f13d-110">POS ビュー</span><span class="sxs-lookup"><span data-stu-id="4f13d-110">POS views</span></span>              | <span data-ttu-id="4f13d-111">カスタム コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="4f13d-111">Support custom control</span></span> | <span data-ttu-id="4f13d-112">カスタム コントロールの数</span><span class="sxs-lookup"><span data-stu-id="4f13d-112">Number of custom controls</span></span> |
|------------------------|------------------------|--------------------------|
| <span data-ttu-id="4f13d-113">顧客の追加/編集表示</span><span class="sxs-lookup"><span data-stu-id="4f13d-113">Customer Add/Edit view</span></span> | <span data-ttu-id="4f13d-114">有</span><span class="sxs-lookup"><span data-stu-id="4f13d-114">Yes</span></span>                    | <span data-ttu-id="4f13d-115">倍数</span><span class="sxs-lookup"><span data-stu-id="4f13d-115">Multiple</span></span>                 |
| <span data-ttu-id="4f13d-116">アドレスの追加/編集表示</span><span class="sxs-lookup"><span data-stu-id="4f13d-116">Address Add/Edit view</span></span>  | <span data-ttu-id="4f13d-117">有</span><span class="sxs-lookup"><span data-stu-id="4f13d-117">Yes</span></span>                    | <span data-ttu-id="4f13d-118">倍数</span><span class="sxs-lookup"><span data-stu-id="4f13d-118">Multiple</span></span>                 |
| <span data-ttu-id="4f13d-119">顧客の詳細表示</span><span class="sxs-lookup"><span data-stu-id="4f13d-119">Customer details view</span></span>  | <span data-ttu-id="4f13d-120">有</span><span class="sxs-lookup"><span data-stu-id="4f13d-120">Yes</span></span>                    | <span data-ttu-id="4f13d-121">倍数</span><span class="sxs-lookup"><span data-stu-id="4f13d-121">Multiple</span></span>                 |
| <span data-ttu-id="4f13d-122">製品詳細表示</span><span class="sxs-lookup"><span data-stu-id="4f13d-122">Product details view</span></span>   | <span data-ttu-id="4f13d-123">有</span><span class="sxs-lookup"><span data-stu-id="4f13d-123">Yes</span></span>                    | <span data-ttu-id="4f13d-124">倍数</span><span class="sxs-lookup"><span data-stu-id="4f13d-124">Multiple</span></span>                 |
| <span data-ttu-id="4f13d-125">価格の確認ビュー</span><span class="sxs-lookup"><span data-stu-id="4f13d-125">Price check view</span></span>       | <span data-ttu-id="4f13d-126">有</span><span class="sxs-lookup"><span data-stu-id="4f13d-126">Yes</span></span>                    | <span data-ttu-id="4f13d-127">倍数</span><span class="sxs-lookup"><span data-stu-id="4f13d-127">Multiple</span></span>                 |

<span data-ttu-id="4f13d-128">次のテーブルに、カスタム コントロールをサポートする画面レイアウト デザイナー ベースビューを示します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-128">The following table lists the screen layout designer based-views that support custom controls.</span></span>

| <span data-ttu-id="4f13d-129">POS ビュー</span><span class="sxs-lookup"><span data-stu-id="4f13d-129">POS views</span></span> | <span data-ttu-id="4f13d-130">カスタム コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="4f13d-130">Support custom control</span></span> | <span data-ttu-id="4f13d-131">カスタム コントロールの数</span><span class="sxs-lookup"><span data-stu-id="4f13d-131">Number of custom controls</span></span> |
|-----------|------------------------|--------------------------|
| <span data-ttu-id="4f13d-132">カート ビュー</span><span class="sxs-lookup"><span data-stu-id="4f13d-132">Cart view</span></span> | <span data-ttu-id="4f13d-133">有</span><span class="sxs-lookup"><span data-stu-id="4f13d-133">Yes</span></span>                    | <span data-ttu-id="4f13d-134">10</span><span class="sxs-lookup"><span data-stu-id="4f13d-134">10</span></span>                       |

## <a name="create-the-custom-control"></a><span data-ttu-id="4f13d-135">カスタム コントロールの作成</span><span class="sxs-lookup"><span data-stu-id="4f13d-135">Create the custom control</span></span>

<span data-ttu-id="4f13d-136">次の例では、拡張機能を使用して既存の POS ビューの 1 つにカスタム コントロールを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4f13d-136">The following example demonstrates how to add a custom control to one of the  existing POS views using extensions.</span></span> <span data-ttu-id="4f13d-137">たとえば、4 つの列を持つ、カスタム データのリストを追加することによって製品の詳細ビューで製品の使用可能な情報を表示したとします - 場所、在庫、引当済、および注文済。</span><span class="sxs-lookup"><span data-stu-id="4f13d-137">For example, suppose  you want to show the product availability information in the product details view by adding custom data list that has four columns - Location, Inventory, Reserved, and Ordered.</span></span>

<span data-ttu-id="4f13d-138">カスタム コントロールは、カスタム情報を表示する HTML ページです。</span><span class="sxs-lookup"><span data-stu-id="4f13d-138">A custom control is an HTML page with the custom information to be displayed.</span></span> <span data-ttu-id="4f13d-139">対応する Typescript ファイルには、コントロールのロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f13d-139">A corresponding Typescript file contains the logic for the control.</span></span> 

1. <span data-ttu-id="4f13d-140">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-140">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="4f13d-141">**\RetailSDK\POS** から Modern POS を開きます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-141">Open Modern POS from **\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="4f13d-142">**POS.Extensions** プロジェクトで、**ProdDetailsCustomColumnExtensions** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-142">Under the **POS.Extensions** project, create a new folder named **ProdDetailsCustomColumnExtensions**.</span></span>
4. <span data-ttu-id="4f13d-143">**ProdDetailsCustomColumnExtensions** の下で **ViewExtensions** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-143">Under **ProdDetailsCustomColumnExtensions**, create a new folder named **ViewExtensions**.</span></span>
5. <span data-ttu-id="4f13d-144">**ViewExtensions** の下で **SimpleProductDetails** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-144">Under **ViewExtensions**, create new folder named **SimpleProductDetails**.</span></span>
6. <span data-ttu-id="4f13d-145">**SimpleProductDetails** フォルダー内に新しい HTML ファイルを追加し、**ProductAvailabilityPanel.html** という名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-145">Add a new HTML file inside the **SimpleProductDetails** folder and name it **ProductAvailabilityPanel.html**.</span></span>  
7. <span data-ttu-id="4f13d-146">**ProductAvailabilityPanel.html** を開き、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-146">Open **ProductAvailabilityPanel.html** and add the following code.</span></span> <span data-ttu-id="4f13d-147">このコードは、POS データ リスト コントロールを追加して、製品の可用性情報とコントロールの幅を表示します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-147">The code adds a POS data list control to show the product availability information and the width of the control.</span></span>

    ```html
    <!DOCTYPE html>
    <html lang="en" xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title></title>
    </head>
    <body>
        <!-- Note: The element ID is different than the ID generated by the POS extensibility framework. This 'template' ID is not used by the POS extensibility framework. -->
        <script id="Microsoft_Pos_Extensibility_Samples_ProductAvailabilityPanel" type="text/html">
            <h2 class="marginTop8 marginBottom8" data-bind="text: title"></h2>
            <div class="width400 grow col">
                <div id="Microsot_Pos_Extensibility_Samples_ProductAvailabilityPanel_DataList" data-bind="msPosDataList: dataList"></div>
            </div>
        </script>
    </body>
    </html>
    ```
    
8. <span data-ttu-id="4f13d-148">**SimpleProductDetails** フォルダーに、新しい Typescript ファイルを追加し、**ProductAvailabilityPanel.ts** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-148">In the **SimpleProductDetails** folder, add a new typescript file and name it **ProductAvailabilityPanel.ts**.</span></span>
9. <span data-ttu-id="4f13d-149">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-149">Add the following **import** statements to import the relevant entities and context.</span></span>

    ```typescript
    import {

        SimpleProductDetailsCustomControlBase,
        ISimpleProductDetailsCustomControlState,
        ISimpleProductDetailsCustomControlContext

    } from "PosApi/Extend/Views/SimpleProductDetailsView";

    import { InventoryLookupOperationRequest, InventoryLookupOperationResponse } from "PosApi/Consume/OrgUnits";
    import { ClientEntities, ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions } from "PosApi/TypeExtensions";
    import { DataList, SelectionMode } from "PosUISdk/Controls/DataList";
    ```
    
10. <span data-ttu-id="4f13d-150">**ProductAvailabilityPanel** という名前の新しいクラスを作成し、**SimpleProductDetailsCustomControlBase** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-150">Create a new class named **ProductAvailabilityPanel** and extend it from **SimpleProductDetailsCustomControlBase**.</span></span>

    ```typescript
    export default class ProductAvailabilityPanel extends SimpleProductDetailsCustomControlBase { }
    ```

11. <span data-ttu-id="4f13d-151">クラス内で、状態およびデータ リスト情報に対して次の変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-151">Inside the class, declare the following variables for state and data list information.</span></span>
 
    ```typescript
    private static readonly TEMPLATE_ID: string = "Microsot_Pos_Extensibility_Samples_ProductAvailabilityPanel";
    public readonly orgUnitAvailabilities: ObservableArray<ProxyEntities.OrgUnitAvailability>;
    public readonly dataList: DataList<ProxyEntities.OrgUnitAvailability>;
    public readonly title: Observable<string>;
    private _state: ISimpleProductDetailsCustomControlState;
    ```
12. <span data-ttu-id="4f13d-152">クラスのコンストラクターメソッドを追加して、データ リストの列を初期化します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-152">Add a class constructor method to initialize the data list columns.</span></span>

    ```typescript
    constructor(id: string, context: ISimpleProductDetailsCustomControlContext) {

        super(id, context);
        this.orgUnitAvailabilities = ko.observableArray([]);
        this.title = ko.observable("Product Availability");
        this.dataList = new DataList<ProxyEntities.OrgUnitAvailability>({
            columns: [

                {
                    title: "Location",
                    ratio: 31,
                    collapseOrder: 4,
                    minWidth: 100,
                    computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                        return value.OrgUnitLocation.OrgUnitName;

                    }

                },

                {
                    title: "Inventory",
                    ratio: 23,
                    collapseOrder: 3,
                    minWidth: 60,
                    computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                        return ArrayExtensions.hasElements(value.ItemAvailabilities) ? value.ItemAvailabilities[0].AvailableQuantity.toString() : "0";
                    }

                },

                {
                    title: "Reserved",
                    ratio: 23,
                    collapseOrder: 1,
                    minWidth: 60,
                    computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                        return ArrayExtensions.hasElements(value.ItemAvailabilities) ? value.ItemAvailabilities[0].PhysicalReserved.toString() : "0";
                    }
                },

                {
                    title: "Ordered",
                    ratio: 23,
                    collapseOrder: 2,
                    minWidth: 60,
                    computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                        return ArrayExtensions.hasElements(value.ItemAvailabilities) ? value.ItemAvailabilities[0].OrderedSum.toString() : "0";
                    }
                }

            ],

            itemDataSource: this.orgUnitAvailabilities,
            selectionMode: SelectionMode.None

        });

    }
    ```
13. <span data-ttu-id="4f13d-153">HTML コントロールをバインドする **OnReady** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-153">Add the **OnReady** method to bind the HTML control.</span></span>

    ```typescript
    public onReady(element: HTMLElement): void {

        ko.applyBindingsToNode(element, {
            template: {
                name: ProductAvailabilityPanel.TEMPLATE_ID,
                data: this

            }

        });
    }
    ```

14. <span data-ttu-id="4f13d-154">**init** メソッドを追加して、ページが読み込まれたときに製品使用可能性の詳細を取得し、データがフェッチされ、データ リストで更新されるようにします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-154">Add the **init** method to get the product availability details so when the page loads, the data is fetched and updated in the data list.</span></span>
 
     ```typescript
    public init(state: ISimpleProductDetailsCustomControlState): void {

        this._state = state;
        let correlationId: string = this.context.logger.getNewCorrelationId();
        if(!this._state.isSelectionMode) {
        this.isVisible = true;

        let request: InventoryLookupOperationRequest<InventoryLookupOperationResponse> =
            new InventoryLookupOperationRequest<InventoryLookupOperationResponse>
                (this._state.product.RecordId, correlationId);
        this.context.runtime.executeAsync(request)
            .then((result: ClientEntities.ICancelableDataResult<InventoryLookupOperationResponse>) => {

                if (!result.canceled) {
                    this.orgUnitAvailabilities(result.data.orgUnitAvailability);
                }

            }).catch((reason: any) => {
                this.context.logger.logError(JSON.stringify(reason), correlationId);

            });
    }

    }
    ```
   
    <span data-ttu-id="4f13d-155">コード例全体を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-155">The entire code example is shown below.</span></span>
   
    ```typescript
    import {
        SimpleProductDetailsCustomControlBase,
        ISimpleProductDetailsCustomControlState,
        ISimpleProductDetailsCustomControlContext
    } from "PosApi/Extend/Views/SimpleProductDetailsView";

    import { InventoryLookupOperationRequest, InventoryLookupOperationResponse } from "PosApi/Consume/OrgUnits";
    import { ClientEntities, ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions } from "PosApi/TypeExtensions";
    import { DataList, SelectionMode } from "PosUISdk/Controls/DataList";
    export default class ProductAvailabilityPanel extends SimpleProductDetailsCustomControlBase {

        private static readonly TEMPLATE_ID: string = "Microsot_Pos_Extensibility_Samples_ProductAvailabilityPanel";
        public readonly orgUnitAvailabilities: ObservableArray<ProxyEntities.OrgUnitAvailability>;
        public readonly dataList: DataList<ProxyEntities.OrgUnitAvailability>;
        public readonly title: Observable<string>;
        private _state: ISimpleProductDetailsCustomControlState;

        constructor(id: string, context: ISimpleProductDetailsCustomControlContext) {
            super(id, context);
            this.orgUnitAvailabilities = ko.observableArray([]);
            this.title = ko.observable("Product Availability");
            this.dataList = new DataList<ProxyEntities.OrgUnitAvailability>({

                columns: [
                    {
                        title: "Location",
                        ratio: 31,
                        collapseOrder: 4,
                        minWidth: 100,
                        computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                            return value.OrgUnitLocation.OrgUnitName;
                        }
                    },

                    {
                        title: "Inventory",
                        ratio: 23,
                        collapseOrder: 3,
                        minWidth: 60,
                        computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                            return ArrayExtensions.hasElements(value.ItemAvailabilities) ? 
                            value.ItemAvailabilities[0].AvailableQuantity.toString() : "0";
                        }
                    },

                    {
                        title: "Reserved",
                        ratio: 23,
                        collapseOrder: 1,
                        minWidth: 60,
                        computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                            return ArrayExtensions.hasElements(value.ItemAvailabilities) ? 
                            value.ItemAvailabilities[0].PhysicalReserved.toString() : "0";
                        }
                    },

                    {
                        title: "Ordered",
                        ratio: 23,
                        collapseOrder: 2,
                        minWidth: 60,
                        computeValue: (value: ProxyEntities.OrgUnitAvailability): string => {
                            return ArrayExtensions.hasElements(value.ItemAvailabilities) ? 
                            value.ItemAvailabilities[0].OrderedSum.toString() : "0";
                        }

                    }

                ],

                itemDataSource: this.orgUnitAvailabilities,
                selectionMode: SelectionMode.None
            });

        }

        /**
        * Binds the control to the specified element.
        * @param {HTMLElement} element The element to which the control should be bound.
        */

        public onReady(element: HTMLElement): void {
            ko.applyBindingsToNode(element, {
                template: {
                    name: ProductAvailabilityPanel.TEMPLATE_ID,
                    data: this

                }

            });

        }

        /**
        * Initializes the control.
        * @param {ISimpleProductDetailsCustomControlState} state The initial state of the page used to initialize the control.
        */

        public init(state: ISimpleProductDetailsCustomControlState): void {
            this._state = state;
            let correlationId: string = this.context.logger.getNewCorrelationId();
            if (!this._state.isSelectionMode) {
                this.isVisible = true;
                let request: InventoryLookupOperationRequest<InventoryLookupOperationResponse> =
                    new InventoryLookupOperationRequest<InventoryLookupOperationResponse>
                        (this._state.product.RecordId, correlationId);
                this.context.runtime.executeAsync(request)
                    .then((result: ClientEntities.ICancelableDataResult<InventoryLookupOperationResponse>) => {
                        if (!result.canceled) {
                            this.orgUnitAvailabilities(result.data.orgUnitAvailability);
                        }

                    }).catch((reason: any) => {
                        this.context.logger.logError(JSON.stringify(reason), correlationId);

                    });
            }
        }
    }
    ```
15. <span data-ttu-id="4f13d-156">新しい .json ファイルを **ProdDetailsCustomColumnExtensions** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-156">Create a new .json file and under the **ProdDetailsCustomColumnExtensions** folder and name it **manifest.json**.</span></span>

16. <span data-ttu-id="4f13d-157">**manifest.json** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-157">In the **manifest.json** file, add the following code.</span></span>

    ```typescript
     {

        "$schema": "../manifestSchema.json",
            "name": "Pos_Extensibility_Samples",
                "publisher": "Microsoft",
                    "version": "7.2.0",
                        "minimumPosVersion": "7.2.0.0",
                            "components": {
            "extend": {
                "views": {
                    "SimpleProductDetailsView": {
                        "controlsConfig": {
                            "customControls": [
                                {

                                    "controlName": "productAvailabilityPanel",
                                    "htmlPath": "ViewExtensions/SimpleProductDetails/ProductAvailabilityPanel.html",
                                    "modulePath": "ViewExtensions/SimpleProductDetails/ProductAvailabilityPanel"
                                }
                            ]

                        }
                    }
                }
            }
        }
    }
    ```

17. <span data-ttu-id="4f13d-158">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**ProdDetailsCustomColumnExtensions** サンプルを追加し、実行時に POS に拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-158">Open the **extensions.json** file under the **POS.Extensions** project and add the **ProdDetailsCustomColumnExtensions** samples, so during runtime POS will include the extension.</span></span>
 
     ```typescript
     {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions2"
            },
            {
                "baseUrl": "ProdDetailsCustomColumnExtensions"
            }
        ]
    }
    ```

18. <span data-ttu-id="4f13d-159">**tsconfig.json** を開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-159">Open the **tsconfig.json** and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="4f13d-160">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-160">POS uses this file to include or exclude extensions.</span></span> <span data-ttu-id="4f13d-161">既定では、リストに除外された拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f13d-161">By default, the list contains the excluded extensions list.</span></span> <span data-ttu-id="4f13d-162">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子リストから拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f13d-162">If you want to include any extension part of the POS, then you need add the extension folder name and comment out the extension from the extension list as shown.</span></span>
 
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
        //"ProdDetailsCustomColumnExtensions"
    ],
    ```
19. <span data-ttu-id="4f13d-163">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-163">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="4f13d-164">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="4f13d-164">Validate the customization</span></span>

1. <span data-ttu-id="4f13d-165">**F5** キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-165">Press **F5** and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="4f13d-166">POS の起動後、POS にログインします。</span><span class="sxs-lookup"><span data-stu-id="4f13d-166">After POS launches, login to POS.</span></span> <span data-ttu-id="4f13d-167">任意の製品を検索し、製品詳細ビュー移動します。</span><span class="sxs-lookup"><span data-stu-id="4f13d-167">Search for any product and navigate to the product details view.</span></span> <span data-ttu-id="4f13d-168">追加したカスタム コントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f13d-168">You should see the custom control that you added.</span></span>
